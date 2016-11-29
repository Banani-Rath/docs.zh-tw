---
title: "Troubleshooting Inherited Event Handlers in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "troubleshooting events"
  - "inherited events"
  - "troubleshooting Visual Basic, event handlers"
  - "event handling, troubleshooting"
  - "event handlers, troubleshooting"
ms.assetid: e1c8759f-5370-4308-8476-8c48b73509bf
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Troubleshooting Inherited Event Handlers in Visual Basic
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

這個主題列出在繼承元件中事件處理常式時常發生的問題。  
  
## 程序  
  
#### 每次呼叫時事件處理常式程式碼會執行兩次  
  
-   繼承的事件處理常式中絕對不能包括 [Handles](../../../../visual-basic/language-reference/statements/handles-clause.md) 子句。  基底類別中的方法已經與事件相關，所以將隨之引發。  應該移除繼承方法中的 `Handles` 子句。  
  
     [!CODE [VbVbalrEvents#32](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#32)]  
  
-   如果繼承的方法沒有 `Handles` 關鍵字，請驗證程式碼中未包括額外的 [AddHandler Statement](../../../../visual-basic/language-reference/statements/addhandler-statement.md)或任何處理相同事件的其他方法。  
  
## 請參閱  
 [Events](../../../../visual-basic/programming-guide/language-features/events/events.md)