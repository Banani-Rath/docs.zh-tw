---
title: "Type parameters cannot be used as qualifiers | Microsoft Docs"
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
  - "vbc32098"
  - "bc32098"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC32098"
ms.assetid: bab05325-dde8-4621-a5f6-368b5b7b2d76
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Type parameters cannot be used as qualifiers
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

程式設計項目是利用包括型別參數的限定性條件字串來限定。  
  
 型別參數代表在建構泛型型別時將要提供之型別的需求。  它不會代表特定的已定義型別。  限定性條件字串必須只包括在編譯時期定義的項目。  
  
 下列陳述式可能產生此錯誤。  
  
```  
Public Function checkText(Of c As System.Windows.Forms.Control)(  
    ByVal badText As String) As Boolean  
  
    Dim saveText As c.Text  
    ' Insert code to look for badText within saveText.  
End Function  
```  
  
 **錯誤 ID**：BC32098  
  
### 若要更正這個錯誤  
  
1.  從限定性條件字串移除型別參數，或將它替換成已定義的型別。  
  
2.  如果您需使用已建構的型別，尋找所限定的程式設計項目，則必須使用其他程式邏輯。  
  
## 請參閱  
 [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)   
 [Visual Basic 中的泛型類型](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)   
 [Type List](../../../visual-basic/language-reference/statements/type-list.md)