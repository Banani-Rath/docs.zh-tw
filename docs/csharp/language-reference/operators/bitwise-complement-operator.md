---
title: "~ 運算子 (C# 參考) | Microsoft Docs"
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
  - "~_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "~ [C#], 位元補充運算子"
  - "~ 運算子 [C#]"
  - "位元 (Bitwise) 補充運算子 [C#]"
  - "tilde (~) one's complement 運算子 [C#]"
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# ~ 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`~` 運算子會在運算元上執行反轉每個位元的位元補數運算。  會預先定義 [int](../../../csharp/language-reference/keywords/int.md)、[uint](../../../csharp/language-reference/keywords/uint.md)、[long](../../../csharp/language-reference/keywords/long.md) 和 [ulong](../../../csharp/language-reference/keywords/ulong.md) 的位元補數運算子。  
  
> [!NOTE]
>  `~` 符號也用於宣告解構函式。  如需詳細資訊，請參閱 [解構函式](../../../csharp/programming-guide/classes-and-structs/destructors.md)。  
  
## 備註  
 使用者定義型別可以多載 `~`  運算子。  如需詳細資訊，請參閱 [operator](../../../csharp/language-reference/keywords/operator.md)。  對整數類資料型別執行 \(Integral Type\) 的作業，通常也適用於列舉型別。  
  
## 範例  
 [!CODE [csRefOperators#25](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#25)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)   
 [解構函式](../../../csharp/programming-guide/classes-and-structs/destructors.md)