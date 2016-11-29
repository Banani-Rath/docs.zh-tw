---
title: "| 運算子 (C# 參考) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "|_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "| 運算子 [C#]"
  - "二進位運算子 (|) [C#]"
  - "位元 OR 運算子 [C#]"
ms.assetid: 82d6bb78-54c8-40bf-b679-531180ddaf70
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# | 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

Binary        `|`  運算子已為整數類資料型別及 `bool` 預先定義其運算方式。  對於整數型別，  `|` 會針對其運算元進行位元 OR 運算。  針對 `bool` 運算元，  `|` 會針對其運算元進行邏輯 OR 運算，也就是說，唯有在兩個運算元皆為 `false` 時，結果才會是 `false`。  
  
## 備註  
 使用者定義型別可以多載           `|` 運算子 \(請參閱[運算子](../../../csharp/language-reference/keywords/operator.md)\)。  
  
## 範例  
 [!CODE [csRefOperators#31](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#31)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)