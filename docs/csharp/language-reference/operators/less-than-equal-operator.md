---
title: "&lt;= 運算子 (C# 參考) | Microsoft Docs"
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
  - "<=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<= 運算子 [C#]"
  - "小於或等於運算子 (<=) [C#]"
ms.assetid: bb0caec9-d253-4105-b8bc-5252233251e4
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;= 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

所有的數字型別和列舉型別都定義了「小於或等於」的關係運算子 \(`<=`\)，如果第一個運算元小於或等於第二個運算元時，會傳回 `true`；否則會傳回 `false`。  
  
## 備註  
 使用者定義型別可以多載 `<=` 運算子。  如需詳細資訊，請參閱 [operator](../../../csharp/language-reference/keywords/operator.md)。  若 `<=` 被多載，則 [\>\=](../../../csharp/language-reference/operators/greater-than-equal-operator.md) 也必須被多載。  對整數類資料型別執行 \(Integral Type\) 的作業，通常也適用於列舉型別。  
  
## 範例  
 [!CODE [csRefOperators#32](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#32)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)   
 [explicit](../../../csharp/language-reference/keywords/explicit.md)