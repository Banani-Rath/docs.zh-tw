---
title: "Alias Clause (Visual Basic) | Microsoft Docs"
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
  - "vb.Alias"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Alias keyword"
ms.assetid: 58c06b11-465d-4d87-906a-73200a3d7f19
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Alias Clause (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

表示外部程序在 DLL 中的其他名稱。  
  
## 備註  
 `Alias` 關鍵字可用於以下內容中：  
  
 [Declare 陳述式](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
 下列範例中的 `Alias` 關鍵字是用於提供 advapi32.dll 中函式的名稱 `GetUserNameA`，而 `getUserName` 是用於取代這個範例中的名稱。  函式 `getUserName` 是在 Sub `getUser` 中呼叫的，後者會顯示目前使用者的名稱。  
  
 [!CODE [VbVbalrStatements#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#15)]  
  
## 請參閱  
 [關鍵字](../../../visual-basic/language-reference/keywords/index.md)