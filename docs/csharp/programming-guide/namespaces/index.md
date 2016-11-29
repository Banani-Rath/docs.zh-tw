---
title: "命名空間 (C# 程式設計手冊) | Microsoft Docs"
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
  - "C# 語言, 命名空間"
  - "命名空間 [C#]"
ms.assetid: b1c4ab46-3fad-4ffa-9deb-dd50a2d8c65a
caps.latest.revision: 27
caps.handback.revision: 27
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 命名空間 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

C\# 程式設計大量使用命名空間的原因有兩個。  第一，.NET Framework 會使用命名空間組織其多種類別，如下所示：  
  
 [!CODE [csProgGuide#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#22)]  
  
 `System` 是命名空間，而 `Console` 是該命名空間中的類別。  可以使用 `using` 關鍵字，因此就不需要完整名稱，如下列範例所示：  
  
 [!CODE [csProgGuide#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#1)]  
  
 [!CODE [csProgGuide#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#25)]  
  
 如需詳細資訊，請參閱 [using 指示詞](../../../csharp/language-reference/keywords/using-directive.md)。  
  
 第二，宣告您自己的命名空間，將有助於在較大型的程式設計專案中控制類別和方法名稱的範圍。  請使用 [namespace](../../../csharp/language-reference/keywords/namespace.md) 關鍵字宣告命名空間，如下列範例所示：  
  
 [!CODE [csProgGuideNamespaces#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#6)]  
  
## 命名空間概觀  
 命名空間具有下列屬性：  
  
-   命名空間可以用於組織大型的程式碼專案  
  
-   命名空間會以 `.` 運算子分隔  
  
-   `using directive` 消除指定每個類別之命名空間名稱的需要。  
  
-   `global` 命名空間是「根」命名空間，因此 `global::System` 固定會參考 .NET Framework 命名空間 `System`  
  
## 相關章節  
 如需命名空間的詳細資訊，請參閱下列主題：  
  
-   [使用命名空間](../../../csharp/programming-guide/namespaces/using-namespaces.md)  
  
-   [如何：使用全域命名空間別名](../../../csharp/programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)  
  
-   [如何：使用 My 命名空間](../../../csharp/programming-guide/namespaces/how-to-use-the-my-namespace.md)  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [命名空間關鍵字](../../../csharp/language-reference/keywords/namespace-keywords.md)   
 [using 指示詞](../../../csharp/language-reference/keywords/using-directive.md)   
 [:: 運算子](../../../csharp/language-reference/operators/namespace-alias-qualifer.md)   
 [. 運算子](../../../csharp/language-reference/operators/member-access-operator.md)