---
title: "&gt; 運算子 (C# 參考) | Microsoft Docs"
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
  - ">_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "> 運算子 [C#]"
  - "大於運算子 (>) [C#]"
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &gt; 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

所有的數字和列舉型別都定義了「大於」的關係運算子 \(`>`\)，當第一個運算元大於第二個運算元時會傳回 `true`，否則傳回 `false`。  
  
## 備註  
 使用者定義型別可多載 `>` 運算子 \(請參閱 [operator](../../../csharp/language-reference/keywords/operator.md)\)。  如果多載 `>`，則也必須多載 [\<](../../../csharp/language-reference/operators/less-than-operator.md)。  當多載二元 \(Binary\) 運算子時，同時隱含多載其對應的指派運算子 \(若有的話\)。  
  
## 範例  
 [!CODE [csRefOperators#29](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#29)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)   
 [explicit](../../../csharp/language-reference/keywords/explicit.md)