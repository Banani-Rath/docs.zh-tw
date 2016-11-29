---
title: "override (C# 參考) | Microsoft Docs"
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
  - "override"
  - "override_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "override 關鍵字 [C#]"
ms.assetid: dd1907a8-acf8-46d3-80b9-c2ca4febada8
caps.latest.revision: 26
caps.handback.revision: 26
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# override (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`override` 修飾詞需要用來擴充或修改繼承的方法、屬性、索引子或事件的抽象或虛擬實作。  
  
## 範例  
 在這個範例中，`Square` 類別 \(Class\) 必須提供 `Area` 的覆寫實作，因為 `Area` 是繼承自抽象的 `ShapesClass`：  
  
 [!CODE [csrefKeywordsModifiers#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#1)]  
  
 `override` 方法提供繼承自基底類別 \(Base Class\) 的新成員實作。  由 `override` 宣告覆寫的方法，就是被覆寫的基底方法。  被覆寫的基底方法必須和 `override` 方法有相同的簽章。  如需繼承 \(Inheritance\) 的詳細資訊，請參閱[繼承](../../../csharp/programming-guide/classes-and-structs/inheritance.md)。  
  
 您不能覆寫非虛擬或靜態方法。  被覆寫的基底方法必須是 `virtual`、`abstract` 或 `override`。  
  
 `override` 宣告不能變更 `virtual` 方法的存取範圍。  `override` 方法和 `virtual` 方法都必須有相同的[存取層級修飾詞](../../../csharp/language-reference/keywords/access-modifiers.md)。  
  
 您不能使用 `new`、`static` 或 `virtual` 修飾詞來修改 `override` 方法。  
  
 覆寫屬性宣告必須指定和所繼承屬性完全相同的存取修飾詞、型別和名稱，且被覆寫的屬性必須是 `virtual`、`abstract` 或 `override`。  
  
 如需如何使用 `override` 關鍵字的詳細資訊，請參閱[使用 Override 和 New 關鍵字的進行版本控制](../../../csharp/programming-guide/classes-and-structs/versioning-with-the-override-and-new-keywords.md) 和[了解使用 Override 和 New 關鍵字的時機](../../../csharp/programming-guide/classes-and-structs/knowing-when-to-use-override-and-new-keywords.md)。  
  
## 範例  
 這個範例會定義名為 `Employee` 的基底類別，以及名為 `SalesEmployee` 的衍生類別。  `SalesEmployee` 類別包含額外的屬性 `salesbonus`，並會覆寫 `CalculatePay` 以便將該方法列入考量。  
  
 [!CODE [csrefKeywordsModifiers#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#9)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [繼承](../../../csharp/programming-guide/classes-and-structs/inheritance.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [修飾詞](../../../csharp/language-reference/keywords/modifiers.md)   
 [abstract](../../../csharp/language-reference/keywords/abstract.md)   
 [虛擬](../../../csharp/language-reference/keywords/virtual.md)   
 [new](../../../csharp/language-reference/keywords/new.md)   
 [多型](../../../csharp/programming-guide/classes-and-structs/polymorphism.md)