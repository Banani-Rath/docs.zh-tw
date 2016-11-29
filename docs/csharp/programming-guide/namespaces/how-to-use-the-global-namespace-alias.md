---
title: "如何：使用全域命名空間別名 (C# 程式設計手冊) | Microsoft Docs"
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
  - "別名 [C#]"
  - "全域命名空間 [C#]"
  - "命名空間 [C#], 全域命名空間限定詞"
ms.assetid: 98a1d89b-3c5a-44f7-8400-c4a3c0ec22a9
caps.latest.revision: 23
caps.handback.revision: 23
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：使用全域命名空間別名 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

能夠存取全域 [namespace](../../../csharp/language-reference/keywords/namespace.md) 中的成員會十分有用，尤其是該成員可能會被其他同名的實體隱藏的時候。  
  
 例如，在下列程式碼中，會將 `Console` 解析為 `TestApp.Console`，而不是 <xref:System> 命名空間中的 `Console` 型別。  
  
 [!CODE [csProgGuide#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#1)]  
  
 [!CODE [csProgGuideNamespaces#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#1)]  
  
 使用 `System.Console` 仍會導致錯誤，因為 `System` 命名空間已被 `TestApp.System` 類別隱藏：  
  
 [!CODE [csProgGuideNamespaces#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#2)]  
  
 不過，您可以使用 `global::System.Console` 解決此錯誤，如下所示：  
  
 [!CODE [csProgGuideNamespaces#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#3)]  
  
 當左邊的識別項為 `global` 時，便會從全域命名空間開始搜尋右邊的識別項。  例如，下面的宣告便將 `TestApp` 當做全域命名空間的成員參考。  
  
 [!CODE [csProgGuideNamespaces#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#4)]  
  
 很明顯地，我們並不建議您建立名為 `System` 的命名空間，而您也不太可能遇到任何發生這種情況的程式碼。  不過，在大型專案中，仍很有可能會發生某些形式的命名空間重複。  在這種情況下，全域命名空間限定詞即可確保您能夠指定根命名空間。  
  
## 範例  
 在這個範例中，命名空間 `System` 是用於包含類別 `TestClass`，因此必須使用 `global::System.Console` 來參考被 `System` 命名空間隱藏的 `System.Console` 類別。  同樣地，別名 `colAlias` 是用於參考命名空間 `System.Collections`，因此，<xref:System.Collections.Hashtable?displayProperty=fullName> 的執行個體是使用這個別名所建立，而不是命名空間。  
  
 [!CODE [csProgGuideNamespaces#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#5)]  
  
  **A 1**  
**B 2**  
**C 3**   
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [命名空間](../../../csharp/programming-guide/namespaces/index.md)   
 [. 運算子](../../../csharp/language-reference/operators/member-access-operator.md)   
 [:: 運算子](../../../csharp/language-reference/operators/namespace-alias-qualifer.md)   
 [extern](../../../csharp/language-reference/keywords/extern.md)