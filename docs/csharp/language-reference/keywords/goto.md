---
title: "goto (C# 參考) | Microsoft Docs"
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
  - "goto_CSharpKeyword"
  - "goto"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "goto 關鍵字 [C#]"
ms.assetid: 2c03c9c1-8119-44ef-b740-fb3d287a42fe
caps.latest.revision: 22
caps.handback.revision: 22
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# goto (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`goto` 陳述式將程式控制直接轉移到標記陳述式。  
  
 `goto` 的常見用法是轉移控制至特定的 switch\-case 標記或 `switch` 陳述式中預設的標記。  
  
 `goto` 陳述式對於跳出複雜的巢狀迴圈也很有用。  
  
## 範例  
 下列範例說明在 [switch](../../../csharp/language-reference/keywords/switch.md) 陳述式中使用 `goto`。  
  
 [!CODE [csrefKeywordsJump#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#4)]  
  
## 範例  
 以下的範例說明使用 `goto` 以中斷巢狀迴圈。  
  
 [!CODE [csrefKeywordsJump#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#5)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [goto 陳述式](/visual-cpp/cpp/goto-statement-cpp)   
 [跳躍陳述式](../../../csharp/language-reference/keywords/jump-statements.md)