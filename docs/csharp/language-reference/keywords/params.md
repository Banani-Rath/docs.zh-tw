---
title: "params (C# 參考) | Microsoft Docs"
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
  - "params_CSharpKeyword"
  - "params"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "參數 [C#]，params"
  - "params 關鍵字 [C#]"
ms.assetid: 1690815e-b52b-4967-8380-5780aff08012
caps.latest.revision: 24
caps.handback.revision: 24
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# params (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

您可以使用 `params` 關鍵字，指定可接受可變數目引數的[方法參數](../../../csharp/language-reference/keywords/method-parameters.md)。  
  
 您可以傳送在參數宣告終止定之類型的引數逗號分隔清單，或是指定類型的引數陣列。  您也可以不傳送引數。  如果您並未傳送引數，`params` 清單的長度為零。  
  
 在一個方法宣告中的 `params` 關鍵字之後不可再有其他參數，且一個方法宣告中只能有一個 `params` 關鍵字。  
  
## 範例  
 下列範例示範可將引數傳送至 `params` 參數的各種方式。  
  
 [!CODE [csrefKeywordsMethodParams#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#5)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [方法參數](../../../csharp/language-reference/keywords/method-parameters.md)