---
title: "== 運算子 (C# 參考) | Microsoft Docs"
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
  - "==_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "== 運算子 [C#]"
  - "等號比較運算子 [C#]"
ms.assetid: 34c6b597-caa2-4855-a7cd-38ecdd11bd07
caps.latest.revision: 14
caps.handback.revision: 14
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# == 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

對於預先定義的實值型別 \(Value Type\)，等號比較運算子 \(`==`\) 在運算元相等時傳回 true；否則傳回 `false`。  對於 [string](../../../csharp/language-reference/keywords/string.md) 以外的參考型別，若兩個運算元參考到同一物件，`==` 會傳回 `true`。  對於 `string` 型別，`==` 會比較字串的值。  
  
## 備註  
 使用者定義的實值型別可多載 `==` 運算子 \(請參閱[運算子](../../../csharp/language-reference/keywords/operator.md)\)。  雖然 `==` 對預先定義和使用者定義的參考型別之預設運作方法如上所述，但使用者定義的參考型別也可多載此運算子。  如果多載 `==`，則也必須多載 [\!\=](../../../csharp/language-reference/operators/not-equal-operator.md)。  對整數類資料型別執行 \(Integral Type\) 的作業，通常也適用於列舉型別。  
  
## 範例  
 [!CODE [csRefOperators#36](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#36)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)