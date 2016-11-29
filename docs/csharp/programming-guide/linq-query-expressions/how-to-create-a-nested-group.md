---
title: "如何：建立巢狀群組 (C# 程式設計手冊) | Microsoft Docs"
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
  - "分組 LINQ 查詢中的群組"
  - "分組 LINQ 查詢"
  - "群組 [C# 中的 LINQ], 巢狀"
  - "巢狀查詢 [C#]"
  - "查詢 [C# 中的 LINQ], 巢狀群組"
  - "查詢運算式 [C# 中的 LINQ], 巢狀群組"
ms.assetid: f48c64af-6d4e-473c-ab27-02f78b5ec2b9
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：建立巢狀群組 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

在下列範例中，會示範如何在 [!INCLUDE[vbteclinq](../../../csharp/includes/vbteclinq_md.md)] 查詢運算式中建立巢狀群組。  按照學年度或是學生年級所建立的每一個群組接著會根據個別學生的名字，進一步的分為子群組。  
  
## 範例  
 [!CODE [csProgGuideLINQ#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#24)]  
  
 請注意，需要三個巢狀 `foreach` 迴圈來反覆查看巢狀群組的內部項目。  
  
## 編譯程式碼  
 這個範例內含在 [如何：查詢物件集合](../../../csharp/programming-guide/linq-query-expressions/how-to-query-a-collection-of-objects.md) 中的範例應用程式中所定義的物件之參考。  若要編譯和執行這個方法，請將方法貼上至該應用程式中的 `StudentClass` 類別，並加入來自 `Main` 方法的呼叫。  
  
 在配合應用程式調整這個方法時，請注意，LINQ 需要 3.5 版的 [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)]，而且專案必須包含 System.Core.dll 的參考，以及 System.Linq 的 using 指示詞。  LINQ to SQL、LINQ to XML 和 LINQ to DataSet 型別需要額外的 Using 和參考。  如需詳細資訊，請參閱 [How to: Create a LINQ Project](../Topic/How%20to:%20Create%20a%20LINQ%20Project.md)。  
  
## 請參閱  
 [LINQ 查詢運算式](../../../csharp/programming-guide/linq-query-expressions/index.md)