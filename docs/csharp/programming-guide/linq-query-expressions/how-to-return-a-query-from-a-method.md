---
title: "如何：從方法傳回查詢 (C# 程式設計手冊) | Microsoft Docs"
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
  - "方法傳回查詢 [C#]"
  - "查詢 [C# 中的 LINQ], 方法傳回查詢"
  - "查詢運算式 [C# 中的 LINQ], 方法傳回查詢"
ms.assetid: 9d6f20a7-f085-44cf-9df3-71948255ec68
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：從方法傳回查詢 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

這個範例會示範如何從方法傳回查詢做為傳回值以及 `out` 參數。  
  
 任何查詢的型別必須是 <xref:System.Collections.IEnumerable> 或 <xref:System.Collections.Generic.IEnumerable%601>，或者是 <xref:System.Linq.IQueryable%601> 一類的衍生型別 \(Derived Type\)。  因此，傳回查詢之方法的任何傳回值或是 `out` 參數也一定具有該型別。  如果方法會將查詢具體化為具象的 <xref:System.Collections.Generic.List%601> 或 <xref:System.Array> 型別，這時便會被視為將傳回查詢結果，而不是傳回查詢本身。  從方法傳回的查詢變數仍然可以加以撰寫或修改。  
  
## 範例  
 在下列範例中，第一個方法會將查詢當做傳回值傳回，第二個方法則會將查詢當做 `out` 參數傳回。  請注意，這兩種情況都是傳回查詢，而不是傳回查詢結果。  
  
 [!CODE [csProgGuideLINQ#80](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#80)]  
  
## 編譯程式碼  
  
-   建立以 .NET Framework 3.5 \(含\) 以後版本為目標的 [!INCLUDE[vs_current_short](../../../csharp/programming-guide/classes-and-structs/includes/vs_current_short_md.md)] 專案。  根據預設，專案有 System.Core.dll 的參考，以及 System.Linq 命名空間的 `using` 指示詞。  
  
-   將類別取代為範例中的程式碼。  
  
-   按 F5 編譯和執行程式。  
  
-   按任何鍵離開主控台視窗。  
  
## 請參閱  
 [LINQ 查詢運算式](../../../csharp/programming-guide/linq-query-expressions/index.md)