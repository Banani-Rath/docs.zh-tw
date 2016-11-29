---
title: "ULong Data Type (Visual Basic) | Microsoft Docs"
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
  - "vb.ulong"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "numbers, whole"
  - "whole numbers"
  - "integral data types"
  - "integer numbers"
  - "numbers, integer"
  - "integers, data types"
  - "integers, types"
  - "data types [Visual Basic], integral"
  - "literal type characters, UL"
  - "ULong data type"
  - "UL literal type characters"
ms.assetid: 017e0702-774e-44ae-bedc-786b424ca84e
caps.latest.revision: 21
caps.handback.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# ULong Data Type (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

存放不帶正負號的 64 位元 \(8 位元組\) 整數，其值的範圍是從 0 到 18,446,744,073,709,551,615 \(超過 1.84 乘以 10 ^ 19\)。  
  
## 備註  
 使用 `ULong` 資料型別取得對 `UInteger` 而言太大的二進位資料，或取得不帶正負號的最大可能整數值。  
  
 `ULong` 的預設值為 0。  
  
## 程式設計提示  
  
-   **負數：** 由於 `ULong` 是不帶正負號的型別，故無法代表負數。  如果您在評估為 `ULong` 型別的運算式中使用一元 \(Unary\) 減號 \(`-`\) 運算子，則 Visual Basic 會先將運算式轉換為 `Decimal`。  
  
-   **符合 CLS 標準：** `ULong` 資料型別不屬於 [語言獨立性以及與語言無關的元件](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md) \(CLS\) 的一部分，所以符合 CLS 標準的程式碼不可以採納使用此資料型別的元件。  
  
-   **Interop 考量：** 如果您正在使用不是針對 .NET Framework 所撰寫的元件，例如 Automation 或 COM 物件，請記住，如 `ulong` 的型別在其他環境中可以有不同的資料寬度 \(32 位元\)。  如果您要將 32 位元引數傳遞到這類元件，則需將其宣告為 `UInteger` 而不是 Managed Visual Basic 程式碼中的 `ULong`。  
  
     此外，自動化不在 Windows 95、Windows 98、Windows ME，或 Windows 2000 支援 64 位元整數。  您不能在這些平台上，將 Visual Basic `ULong` 引數傳遞到自動化元件。  
  
-   **擴展：** `ULong` 資料型別會擴大至 `Decimal`、`Single` 和 `Double`。  這表示您可以將 `ULong` 轉換成這些類型的任何一項，而不會發生 <xref:System.OverflowException?displayProperty=fullName> 錯誤。  
  
-   **型別字元。** 將常值型別字元 `UL` 附加到常值，會強制其成為 `ULong` 資料型別。  `ULong` 沒有識別項型別字元。  
  
-   **架構型別。** 在 .NET Framework 中對應的型別為 <xref:System.UInt64?displayProperty=fullName> 結構。  
  
## 請參閱  
 <xref:System.UInt64>   
 [Data Types](../../../visual-basic/language-reference/data-types/data-type-summary.md)   
 [Type Conversion Functions](../../../visual-basic/language-reference/functions/type-conversion-functions.md)   
 [轉換摘要](../../../visual-basic/language-reference/keywords/conversion-summary.md)   
 [How to: Call a Windows Function that Takes Unsigned Types](../../../visual-basic/programming-guide/com-interop/how-to-call-a-windows-function-that-takes-unsigned-types.md)   
 [Efficient Use of Data Types](../../../visual-basic/programming-guide/language-features/data-types/efficient-use-of-data-types.md)