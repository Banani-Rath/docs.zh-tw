---
title: "+= 運算子 (C# 參考) | Microsoft Docs"
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
  - "+=_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "+= 運算子 [C#]"
  - "加法指派運算子 (+=) [C#]"
ms.assetid: 9cdf97e6-331d-492b-85e1-3ec3171484e9
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# += 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

加法指派運算子。  
  
## 備註  
 使用 `+=` 指派運算子的運算式，例如  
  
```  
x += y  
```  
  
 相等於  
  
```  
x = x + y  
```  
  
 不同的是，`x` 只被評估了一次。  [\+ 運算子](../../../csharp/language-reference/operators/addition-operator.md)的意義，與 `x` 和 `y` 的型別有關 \(若是數字運算元會相加，若是字串運算元則是會串連起來等等\)。  
  
 `+=` 運算子無法直接被多載，但使用者定義型別可多載 [\+  運算子](../../../csharp/language-reference/operators/addition-operator.md) \(請參閱[運算子](../../../csharp/language-reference/keywords/operator.md)\)。  
  
 `+=` 運算子也可以用來指定在回應事件時所要呼叫的方法，這類方法稱為事件處理常式。  在這段此內容中，使用 `+=` 運算子稱為「*訂閱事件*」。  如需詳細資訊，請參閱 [如何：訂閱及取消訂閱事件](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)。  和 [委派](../../../csharp/programming-guide/delegates/index.md)。  
  
## 範例  
 [!CODE [csRefOperators#35](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#35)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)