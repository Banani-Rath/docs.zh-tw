---
title: "-- 運算子 (C# 參考) | Microsoft Docs"
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
  - "--_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "-- 運算子 [C#]"
  - "遞減運算子 (--) [C#]"
ms.assetid: 6b9cfe86-63c7-421f-9379-c9690fea8720
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# -- 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

遞減運算子 \(`--`\) 會將其運算元減 1。  遞減運算子可在其運算元之前或之後出現：`--variable` 和 `variable--`。  第一種形式是前置的遞減運算。  這個運算的結果為運算元遞減之後的值。  第二種形式是後置的遞減運算。  這個運算的結果為運算元遞減之前的值。  
  
## 備註  
 數字和列舉型別已預先定義了遞減運算子。  
  
 使用者定義型別可多載 `--` 運算子 \(請參閱 [operator](../../../csharp/language-reference/keywords/operator.md)\)。  對整數類資料型別執行 \(Integral Type\) 的作業，通常也適用於列舉型別。  
  
## 範例  
 [!CODE [csRefOperators#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#8)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)