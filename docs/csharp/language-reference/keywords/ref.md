---
title: "ref (C# 參考) | Microsoft Docs"
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
  - "ref_CSharpKeyword"
  - "ref"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "參數 [C#], ref"
  - "ref 關鍵字 [C#]"
ms.assetid: b8a5e59c-907d-4065-b41d-95bf4273c0bd
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# ref (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`ref` 關鍵字會導致引數由參考加以傳遞，而非透過值。  由參考傳遞的效果，是呼叫方法中參數的任何變更，都會反映在呼叫方法中。  例如，如果呼叫端傳遞了區域變數運算式或陣列元素存取運算式，且被呼叫的方法取代了 ref 參數所參考的物件，則呼叫端的區域變數或陣列元素現在會參考新的物件。  
  
> [!NOTE]
>  請勿將參考傳遞的概念與參考類型的概念相混淆。  兩個概念並不相同。  方法參數可以由 `ref` 修改，而不論其是否為實值類型或參考類型。  當實值類型由參考傳遞時，沒有 boxing。  
  
 若要使用 `ref` 參數，方法定義和呼叫方法都必須明確使用 `ref` 關鍵字，如下列範例所示。  
  
 [!CODE [csrefKeywordsMethodParams#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#6)]  
  
 傳遞至 `ref` 參數的引數，在傳遞之前必須先初始化。  這點與 `out` 參數不同，其引數不需要在傳遞之前先明確初始化。  如需詳細資訊，請參閱 [out](../../../csharp/language-reference/keywords/out.md)。  
  
 類別的成員不能擁有僅在 `ref` 和 `out` 方面不同的簽章。  如果類型的兩個成員之間唯一的區別在於其中一個具有 `ref` 參數，而另一個具有 `out` 參數，則編譯器會發生錯誤。  例如，下列程式碼不會進行編譯。  
  
 [!CODE [csrefKeywordsMethodParams#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#2)]  
  
 不過，當一種方法具有 `ref` 或 `out` 參數，而另一種方法具有實值參數時，可以完成多載，如下列範例所示。  
  
 [!CODE [csrefKeywordsMethodParams#7](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#7)]  
  
 在需要簽章比對的其他情況 \(如隱藏或覆寫\) 下，`ref` 和 `out` 是簽章的一部分，而且彼此不相符。  
  
 屬性不是變數。  它們都是方法，且不能傳遞給 `ref` 參數。  
  
 如需如何傳遞陣列的詳細資訊，請參閱[使用 ref 和 out 傳遞陣列](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md)。  
  
 您不能將 `ref` 和 `out` 關鍵字用於下列幾種方法：  
  
-   使用 [async](../../../csharp/language-reference/keywords/async.md) 修飾詞定義的非同步方法。  
  
-   Iterator 方法，其包括 [yield return](../../../csharp/language-reference/keywords/yield.md) 或 `yield break` 陳述式。  
  
## 範例  
 前一個範例會示範當您由參考傳遞實值類型時，會發生什麼事。  您也可以使用 `ref` 關鍵字，來傳遞參考類型。  由參考傳遞參考類型，可讓被呼叫的方法取代該參考參數所參考之呼叫方法中的物件。  物件的儲存位置會以參考參數值的方式，傳遞至方法。  如果您變更參數儲存位置中的值 \(指向新的物件\)，則也會變更呼叫端所參考的儲存位置。  下列範例會以 `ref` 參數，傳遞參考類型的執行個體。  如需如何由實值及參考來傳遞參考類型的詳細資訊，請參閱[傳遞參考類型參數](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md)。  
  
 [!CODE [csrefKeywordsMethodParams#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#8)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [傳遞參數](../../../csharp/programming-guide/classes-and-structs/passing-parameters.md)   
 [方法參數](../../../csharp/language-reference/keywords/method-parameters.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)