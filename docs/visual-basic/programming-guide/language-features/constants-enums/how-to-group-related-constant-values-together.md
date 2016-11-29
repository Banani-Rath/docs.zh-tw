---
title: "How to: Group Related Constant Values Together (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "enumerations [Visual Basic], constants"
  - "constants, grouping together"
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Group Related Constant Values Together (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

列舉型別 \(Enumeration\) 是將相關的常數值群組在一起的最佳方式。  可在類別或模組的宣告區段中使用 `Enum` 陳述式 \(Statement\) 建立列舉型別。  如需詳細資訊，請參閱 [How to: Declare an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)。  
  
### 若要群組相關的常數值  
  
1.  撰寫宣告，此宣告內含程式碼存取層級、`Enum` 關鍵字和有效名稱。  此範例建立 `Private` 列舉型別 `temperatureValues`。  
  
     [!CODE [VbEnumsTask#21](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#21)]  
  
2.  定義列舉型別中的常數。  此範例建立 `Public` 列舉型別 `temperatureValues`，並指定它的值。  
  
     [!CODE [VbEnumsTask#1](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#1)]  
  
## 請參閱  
 [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)   
 [How to: Refer to an Enumeration Member](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)   
 [When to Use an Enumeration](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)   
 [Constants Overview](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)   
 [Constant and Literal Data Types](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)   
 [Constants and Enumerations](../../../../visual-basic/language-reference/constants-and-enumerations.md)