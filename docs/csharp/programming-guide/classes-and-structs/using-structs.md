---
title: "使用結構 (C# 程式設計手冊) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "結構 [C#], 使用"
ms.assetid: cea4a459-9eb9-442b-8d08-490e0797ba38
caps.latest.revision: 28
caps.handback.revision: 28
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 使用結構 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`struct` 類型很適合用於代表輕量型物件，例如 `Point`、`Rectangle` 和 `Color`。 雖然使用[自動實作的屬性](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md)可以輕鬆地將一個點表示為一個[類別](../../../csharp/language-reference/keywords/class.md)，但是在某些情節中[結構](../../../csharp/language-reference/keywords/struct.md)可能會更有效率。 例如，如果您宣告含有 1000 個 `Point` 物件的陣列，您會配置額外的記憶體來參考每個物件；在此案例下，結構所耗用的記憶體會較少。 因為 [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] 含有名為 <xref:System.Drawing.Point> 的物件，所以本範例中的結構會改稱為 "CoOrds"。  
  
 [!CODE [csProgGuideObjects#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#1)]  
  
 為結構定義預設 \(無參數\) 的建構函式時會發生錯誤。 初始化結構主體中的執行個體欄位時也會發生錯誤。 您只能透過使用參數化建構函式，或在宣告結構後個別存取成員，來將結構成員初始化。 任何私用或其他無法存取的成員，只能在建構函式中初始化。  
  
 當您使用 [new](../../../csharp/language-reference/keywords/new.md) 運算子建立結構物件時，不僅會建立物件，還會呼叫適當的建構函式。 不同於類別，結構不需要使用 `new` 運算子就能具現化。 在此案例下，不會有建構函式呼叫，因此配置會更有效率。 不過，欄位會維持未指派狀態，而且必須等到所有欄位都初始化後才能使用物件。  
  
 當結構包含參考類型作為成員時，必須明確地叫用成員的預設建構函式，否則成員會維持未指派狀態，而且無法使用結構 \(這會產生編譯器錯誤 CS0171\)。  
  
 不同於類別，結構沒有繼承。 結構無法繼承自另一個結構或類別，而且不能作為類別的基底。 不過，結構可以繼承自基底類別 <xref:System.Object>。 結構可以實作介面，而且其作法就跟類別一樣。  
  
 您無法使用關鍵字 `struct` 宣告類別。 在 C\# 中，類別和結構在語意上是不同的。 結構是實值類型，而類別是參考類型。 如需詳細資訊，請參閱[實值類型](../../../csharp/language-reference/keywords/value-types.md)。  
  
 除非您需要參考類型語意，否則系統處理小型類別可能會更有效率 \(如果您改為將其宣告為結構\)。  
  
## 範例 1  
  
### 描述  
 此範例示範如何使用預設和參數化建構函式進行 `struct` 初始化。  
  
### 程式碼  
 [!CODE [csProgGuideObjects#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#1)]  
  
 [!CODE [csProgGuideObjects#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#2)]  
  
## 範例 2  
  
### 描述  
 此範例示範結構特有的功能。 它在建立 CoOrds 物件時並未使用 `new` 運算子。 如果您以 `class` 一字取代 `struct` 一字，將不會編譯程式。  
  
### 程式碼  
 [!CODE [csProgGuideObjects#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#1)]  
  
 [!CODE [csProgGuideObjects#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#3)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [類別和結構](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [結構](../../../csharp/programming-guide/classes-and-structs/structs.md)