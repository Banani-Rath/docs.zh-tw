---
title: "% 運算子 (C# 參考) | Microsoft Docs"
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
  - "%_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "% 運算子 [C#]"
  - "modulus 運算子 [C#]"
ms.assetid: 3b74f4f9-fd9c-45e7-84fa-c8d71a0dfad7
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# % 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`%`運算子會計算後第一個運算元除以第二個的餘數。  所有數字型別都已預先定義的餘數運算子。  
  
## 備註  
 使用者定義型別可多載 `%` 運算子 \(請參閱 [operator](../../../csharp/language-reference/keywords/operator.md)\)。  當多載二元 \(Binary\) 運算子時，同時隱含多載其對應的指派運算子 \(若有的話\)。  
  
## 範例  
 [!CODE [csRefOperators#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#9)]  
  
## 註解  
 請注意與雙精度浮點數型別有關的捨入誤差 \(Round\-Off Error\)。  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)