---
title: "運算子 (C# 參考) | Microsoft Docs"
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
  - "[]_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "subscript 運算子 [C#]"
  - "方括弧 [ ] 運算子 [C#]"
  - "[] 運算子 [C#]"
  - "indexing 運算子 [C#]"
ms.assetid: 5c16bb45-88f7-45ff-b42c-1af1972b042c
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 運算子 (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

方括弧 \(`[]`\) 可用於陣列、索引子以及屬性 \(Attribute\)。  他們也可以用於指標上。  
  
## 備註  
 陣列型別是 `[]` 接在其後的型別：  
  
 [!CODE [csRefOperators#43](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#43)]  
  
 若要存取陣列項目，便須將所需項目索引以方括弧括住。  
  
 [!CODE [csRefOperators#44](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#44)]  
  
 若陣列的索引超出範圍，便會擲回例外狀況。  
  
 陣列索引運算子不可多載，但型別仍可以定義接受一個或多個參數的索引子或屬性。  索引子參數會由方括弧括住，就像陣列索引一樣。不過索引子參數可以宣告為任何型別，而不像陣列索引必須是整數型別。  
  
 例如，.NET Framework 定義了 `Hashtable` 型別，這個型別會使任意型別的索引鍵和值產生關聯：  
  
 [!CODE [csRefOperators#45](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#45)]  
  
 方括弧也用來指定[屬性](../Topic/Attributes%20\(C%23%20and%20Visual%20Basic\).md)：  
  
 [!CODE [csRefOperators#46](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#46)]  
  
 您可以使用方括弧來指定指標的索引：  
  
 [!CODE [csRefOperators#47](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#47)]  
  
 不執行範圍檢查。  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 運算子](../../../csharp/language-reference/operators/index.md)   
 [陣列](../../../csharp/programming-guide/arrays/index.md)   
 [索引子](../../../csharp/programming-guide/indexers/index.md)   
 [unsafe](../../../csharp/language-reference/keywords/unsafe.md)   
 [fixed 陳述式](../../../csharp/language-reference/keywords/fixed-statement.md)