---
title: "Order By Clause (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.QueryOrderBy"
  - "vb.QueryAscending"
  - "vb.QueryDescending"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "queries [Visual Basic], Order By"
  - "Order By clause"
  - "Order By statement"
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Order By Clause (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

指定查詢結果的排序次序。  
  
## 語法  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## 組件  
 `orderExp1`  
 必要項。  目前查詢結果的一個或多個欄位，用以識別如何排序傳回的值。  欄位名稱必須以逗號 \(,\) 分隔。  您可以使用 `Ascending` 或 `Descending` 關鍵字，將每個欄位識別為以遞增或遞減順序排序。  如果未指定 `Ascending` 或 `Descending` 關鍵字，預設排序次序是遞增排序。  排序次序欄位優先順序是由左至右。  
  
## 備註  
 您可以使用 `Order By` 子句排序查詢結果。  `Order By` 子句只能根據目前範圍 \(Scope\) 的範圍 \(Range\) 變數排序結果。  例如，`Select` 子句在查詢運算式中引入新的範圍 \(Scope\)，並用新的反覆運算變數代表該範圍 \(Scope\)。  在查詢中 `Select` 子句之前定義的範圍 \(Range\) 變數在 `Select` 子句之後就無法使用。  因此，如果您要依 `Select` 子句中無法使用的欄位排序結果，就必須將 `Order By` 子句放在 `Select` 子句前面。  您必須這麼做的其中一個範例就是依不在傳回結果中的欄位來排序查詢時。  
  
 欄位的遞增和遞減順序是由針對欄位的資料型別實作的 <xref:System.IComparable> 介面決定。  如果資料型別未實作 <xref:System.IComparable> 介面，則會略過排序次序。  
  
## 範例  
 下列查詢運算式會使用 `From` 子句宣告 `books` 集合的範圍 \(Range\) 變數 `book`。  `Order By` 子句會依價格將查詢結果遞增 \(預設值\) 排序。  相同價格的書籍會依標題遞增排序。  `Select` 子句會選取 `Title` 和 `Price` 屬性做為查詢傳回的值。  
  
 [!CODE [VbSimpleQuerySamples#24](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#24)]  
  
## 範例  
 下列查詢運算式會使用 `Order By` 子句依價格將查詢結果遞減排序。  相同價格的書籍會依標題遞增排序。  
  
 [!CODE [VbSimpleQuerySamples#25](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#25)]  
  
## 範例  
 下列查詢運算式會使用 `Select` 子句選取書籍標題、價格、出版日期和作者。  然後針對新的範圍 \(Scope\) 填入 \(Populate\) 範圍 \(Range\) 變數的 `Title`、`Price`、`PublishDate` 和 `Author` 欄位。  `Order By` 子句會先依作者名稱，再依書籍標題，然後依價格排列新的範圍變數 \(Range Variable\)。  每個資料行都以預設順序 \(遞增\) 排序。  
  
 [!CODE [VbSimpleQuerySamples#26](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#26)]  
  
## 請參閱  
 [Introduction to LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)   
 [Queries](../../../visual-basic/language-reference/queries/queries.md)   
 [Select Clause](../../../visual-basic/language-reference/queries/select-clause.md)   
 [From Clause](../../../visual-basic/language-reference/queries/from-clause.md)