---
title: "如何：分組查詢結果 (C# 程式設計手冊) | Microsoft Docs"
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
  - "group 子句範例 [C# 中的 LINQ]"
  - "群組 [C# 中的 LINQ]"
  - "查詢 [C# 中的 LINQ], 群組"
  - "查詢運算式 [C# 中的 LINQ], 群組"
ms.assetid: ee981053-3392-4245-a8c2-b3730211da0d
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：分組查詢結果 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

群組是 [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)] 的其中一個最強大的功能。  下列範例顯示如何以不同的方式群組資料：  
  
-   使用單一屬性。  
  
-   使用字串屬性的第一個字母。  
  
-   使用計算的數字範圍。  
  
-   使用 Boolean 述詞或其他運算式。  
  
-   使用複合索引鍵。  
  
 此外，最後兩個查詢會將其結果投射至只包含學生姓名的新匿名型別。  如需詳細資訊，請參閱 [group 子句](../../../csharp/language-reference/keywords/group-clause.md)。  
  
## 範例  
 本主題的所有範例都使用下列 Helper 類別和資料來源。  
  
 [!CODE [csProgGuideLINQ#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#15)]  
  
## 範例  
 下列範例顯示如何使用項目的單一屬性做為群組索引鍵，以群組來源項目。  在此案例中，索引鍵是一個 `string`，也就是學生的姓氏。  也可能使用索引鍵的子字串。  群組作業會使用型別的預設相等比較子。  
  
 將下列方法貼至 `StudentClass` 類別。  將 `Main` 方法中的呼叫陳述式變更為 `sc.GroupBySingleProperty()`。  
  
 [!CODE [csProgGuideLINQ#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#17)]  
  
## 範例  
 下列範例顯示如何使用群組索引鍵之物件屬性以外的其他項目，群組來源項目。  在此範例中，索引鍵是學生姓氏的第一個字母。  
  
 將下列方法貼至 `StudentClass` 類別。  將 `Main` 方法中的呼叫陳述式變更為 `sc.GroupBySubstring()`。  
  
 [!CODE [csProgGuideLINQ#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#18)]  
  
## 範例  
 下列範例顯示如何使用數字範圍做為群組索引鍵，來群組來源項目。  然後查詢會將結果投射至匿名型別，該型別只包含學生的姓名及其所屬的百分位數範圍。  使用匿名型別的原因是因為不需要使用完整的 `Student` 物件顯示結果。  `GetPercentile` 是 Helper 函式，會根據學生的平均分數計算百分位數。  此方法會傳回介於 0 和 10 之間的整數。  
  
 [!CODE [csProgGuideLINQ#50](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#50)]  
  
 將下列方法貼至 `StudentClass` 類別。  將 `Main` 方法中的呼叫陳述式變更為 `sc.GroupByRange()`。  
  
 [!CODE [csProgGuideLINQ#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#19)]  
  
## 範例  
 下列範例顯示如何使用 Boolean 比較運算式來群組來源項目。  在此範例中，Boolean 運算式會測試學生的平均測驗分數是否高於 75。  如前述範例所示，結果會投射至匿名型別，因為不需要完整的來源項目。  請注意，匿名型別中的屬性會變成 `Key` 成員上的屬性，並且可以在執行查詢時以名稱存取。  
  
 將下列方法貼至 `StudentClass` 類別。  將 `Main` 方法中的呼叫陳述式變更為 `sc.GroupByBoolean()`。  
  
 [!CODE [csProgGuideLINQ#20](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#20)]  
  
## 範例  
 下列範例顯示如何使用匿名型別，封裝包含多個值的索引鍵。  在此範例中，第一個索引鍵值是學生姓氏的第一個字母。  第二個索引鍵值是 Boolean，指定第一次測驗時學生的分數是否高於 85 分。  您可以依索引鍵中的任何屬性排序群組。  
  
 將下列方法貼至 `StudentClass` 類別。  將 `Main` 方法中的呼叫陳述式變更為 `sc.GroupByCompositeKey()`。  
  
 [!CODE [csProgGuideLINQ#21](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#21)]  
  
## 編譯程式碼  
 將您要測試的每一個方法複製並貼至 `StudentClass` 類別。  將方法的呼叫陳述式加入至 `Main` 方法，然後按 F5。  
  
 在配合應用程式調整這些方法時，請注意，LINQ 需要 [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] 3.5 或 4 版，而且專案必須包含 System.Core.dll 的參考，以及 System.Linq 的 using 指示詞。  LINQ to SQL、LINQ to XML 和 LINQ to DataSet 型別都需要額外的 using 指示詞和參考。  如需詳細資訊，請參閱 [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md)。  
  
## 請參閱  
 <xref:System.Linq.Enumerable.GroupBy%2A>   
 <xref:System.Linq.IGrouping%602>   
 [LINQ 查詢運算式](../../../csharp/programming-guide/linq-query-expressions/index.md)   
 [group 子句](../../../csharp/language-reference/keywords/group-clause.md)   
 [匿名類型](../../../csharp/programming-guide/classes-and-structs/anonymous-types.md)   
 [如何：在分組作業上執行子查詢](../../../csharp/programming-guide/linq-query-expressions/how-to-perform-a-subquery-on-a-grouping-operation.md)   
 [如何：建立巢狀群組](../../../csharp/programming-guide/linq-query-expressions/how-to-create-a-nested-group.md)   
 [Grouping Data](../../../visual-basic/programming-guide/concepts/linq/grouping-data.md)