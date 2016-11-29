---
title: "如何：處理查詢運算式中的 Null 值 (C# 程式設計手冊) | Microsoft Docs"
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
  - "null 值 [C# 中的 LINQ]"
  - "查詢 [C# 中的 LINQ], null 值"
  - "查詢運算式 [C# 中的 LINQ], null 值"
ms.assetid: cb34f7a1-7ef5-466a-90ba-91da30ab525d
caps.latest.revision: 6
caps.handback.revision: 6
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：處理查詢運算式中的 Null 值 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

這個範例會示範如何處理來源集合中的可能 null 值。  <xref:System.Collections.Generic.IEnumerable%601> 一類的物件集合可以包含其值為 [null](../../../csharp/language-reference/keywords/null.md) 的項目。  如果來源集合為 null，或是包含值為 null 的項目，而且您的查詢不會處理 null 值，這樣當您執行該查詢時，便會擲回 <xref:System.NullReferenceException>。  
  
## 範例  
 您可以用防禦方式來撰寫程式碼，以避免發生下列範例中所示的 null 參考例外狀況 \(Exception\)：  
  
 [!CODE [csProgGuideLINQ#82](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#82)]  
  
 在上述範例中，`where` 子句會篩選掉分類序列 \(Sequence\) 中的所有 null 項目。  這項技巧與 join 子句中的 null 檢查無關。  在此範例中具有 null 值的條件運算式可以運作，因為 `Products.CategoryID` 的型別為 `int?`，而這是 `Nullable<int>` 的簡略表示法。  
  
## 範例  
 在 join 子句中，如果只有一個比較索引鍵是可為 Null 的實值型別，您就可以在查詢運算式中將另一個索引鍵轉型成可為 Null 的型別。  在下列範例中，假設 `EmployeeID` 是包含 `int?` 型別之值的資料行：  
  
 [!CODE [csProgGuideLINQ#83](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#83)]  
  
## 請參閱  
 <xref:System.Nullable%601>   
 [LINQ 查詢運算式](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [可為 Null 的類型](../../../csharp/programming-guide/nullable-types/index.md)