---
title: "My.Request Object | Microsoft Docs"
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
  - "My.MyWebExtension.Request"
  - "My.Request"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Request object"
ms.assetid: 93d5f0e2-6b60-4a2c-8652-d90216f6ad10
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# My.Request Object
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

取得所要求網頁的 <xref:System.Web.HttpRequest> 物件。  
  
## 備註  
 `My.Request` 物件會包含目前 HTTP 要求的相關資訊。  
  
 `My.Request` 物件僅適用於 ASP.NET 應用程式。  
  
## 範例  
 下列範例會取得 `My.Request` 物件的標頭集合，並使用 `My.Response` 物件將該集合寫入 ASP.NET 網頁。  
  
 [!CODE [VbVbalrMyWeb#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyWeb#1)]  
  
## 請參閱  
 <xref:System.Web.HttpRequest>   
 [My.Response Object](../../../visual-basic/language-reference/objects/my-response-object.md)