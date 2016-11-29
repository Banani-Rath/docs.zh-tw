---
title: "&amp;= 運算子 (C# 參考) | Microsoft Docs"
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
  - "&=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "&= 運算子 [C#]"
  - "AND 指派運算子 (&=) [C#]"
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &amp;= 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

AND 指派運算子。  
  
## 備註  
 使用 `&=` 指派運算子的運算式，例如  
  
```  
x &= y  
```  
  
 相等於  
  
```  
x = x & y  
```  
  
 不同的是，`x` 只被評估了一次。  [& 運算子](../../../csharp/language-reference/operators/and-operator.md)會對整數運算元執行位元邏輯 AND 運算，對 `bool` 運算元則是執行邏輯 AND 運算。  
  
 `&=` 運算子無法直接多載，但是使用者定義型別可多載二元 [& 運算子](../../../csharp/language-reference/operators/and-operator.md) \(請參閱 [operator](../../../csharp/language-reference/keywords/operator.md)\)。  
  
## 範例  
 [!CODE [csRefOperators#34](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#34)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)