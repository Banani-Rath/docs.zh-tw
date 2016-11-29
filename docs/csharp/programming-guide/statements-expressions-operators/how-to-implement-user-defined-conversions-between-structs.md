---
title: "如何：在結構之間實作使用者定義的轉換 (C# 程式設計手冊) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "使用者定義的轉換範例 [C#]"
ms.assetid: 97839aef-8fbc-40d5-9769-6b569bc2710b
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：在結構之間實作使用者定義的轉換 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

本範例定義兩個結構：`RomanNumeral` 和 `BinaryNumeral`，並說明它們之間的轉換。  
  
## 範例  
 [!CODE [csProgGuideStatements#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#13)]  
  
## 穩固程式設計  
  
-   在前面的範例中，陳述式：  
  
     [!CODE [csProgGuideStatements#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#14)]  
  
     會執行轉換，從 `RomanNumeral` 轉換為 `BinaryNumeral`。  因為 `RomanNumeral` 和 `BinaryNumeral` 之間並沒有直接轉換，所以使用型別轉換以將 `RomanNumeral` 轉換成 `int`，並且使用另一個型別轉換以將 `int` 轉換成 `BinaryNumeral`。  
  
-   同時，陳述式  
  
     [!CODE [csProgGuideStatements#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#15)]  
  
     會執行轉換，從 `BinaryNumeral` 轉換為 `RomanNumeral`。  因為 `RomanNumeral` 定義了一個從 `BinaryNumeral` 轉換的隱含轉換，所以不需要轉換。  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [轉換運算子](../../../csharp/programming-guide/statements-expressions-operators/conversion-operators.md)