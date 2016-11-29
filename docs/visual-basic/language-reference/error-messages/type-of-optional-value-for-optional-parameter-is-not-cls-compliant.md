---
title: "Type of optional value for optional parameter &lt;parametername&gt; is not CLS-compliant | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BC40042"
  - "vbc40042"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC40042"
ms.assetid: 1d6eae29-4ad3-4434-bde4-a53b6051adf5
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Type of optional value for optional parameter &lt;parametername&gt; is not CLS-compliant
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

程序已標記為 `<CLSCompliant(True)>`，但所宣告的 [Optional](../../../visual-basic/language-reference/modifiers/optional.md) 參數卻具有不符合標準之型別的預設值。  
  
 程序必須只使用符合 CLS 標準的型別，才能夠符合 [語言獨立性以及與語言無關的元件](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md) \(CLS\) 標準。  這適用於參數型別、傳回型別及其所有區域變數的型別。  也適用於選擇性參數的預設值。  
  
 下列 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 資料型別並非 CLS 相容：  
  
-   [SByte Data Type](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [UInteger Data Type](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [ULong Data Type](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [UShort Data Type](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 當您套用 <xref:System.CLSCompliantAttribute> 屬性至程式設計的項目時，可以將 `isCompliant` 參數的屬性設定為 `True` 或 `False`，表示符合標準或不符合標準。  這個參數沒有預設值，所以您必須提供預設值。  
  
 如果未將 <xref:System.CLSCompliantAttribute> 套用至項目，則此項目會被視為不符合標準。  
  
 根據預設，這是一個警告訊息。  如需隱藏警告或將警告視為錯誤的詳細資訊，請參閱[在 Visual Basic 中設定警告](/visual-studio/ide/configuring-warnings-in-visual-basic)。  
  
 **錯誤 ID：**BC40042  
  
### 若要更正這個錯誤  
  
-   如果選擇性參數必須具有此特殊型別的預設值，請移除 <xref:System.CLSCompliantAttribute>。  程序不可符合 CLS 標準。  
  
-   如果程序必須符合 CLS 標準，請將此預設值的型別變更為最符合 CLS 標準的型別。  例如，如果數值範圍不需要超過 2,147,483,647，您可以使用 `Integer` 來取代 `UInteger`。  如果真的需要擴充的範圍，可以使用 `Long` 來取代 `UInteger`。  
  
-   如果要與 Automation 或 COM 物件進行互動，請記住，某些型別的資料寬度會與 [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] 不同。  例如，`int` 在其他環境中，通常是 16 位元。  如果您所接收的是來自這類元件的 16 位元整數，請在 Managed [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 程式碼中將它宣告為 `Short` 而不是 `Integer`。  
  
## 請參閱  
 [\<PAVE OVER\> Writing CLS\-Compliant Code](http://msdn.microsoft.com/zh-tw/4c705105-69a2-4e5e-b24e-0633bc32c7f3)