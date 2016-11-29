---
title: "How to: Log Exceptions in Visual Basic | Microsoft Docs"
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
  - "exceptions, logging"
  - "exceptions, tracking"
ms.assetid: a26c60e2-ae39-444a-aebb-33eccadc0eeb
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Log Exceptions in Visual Basic
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

您可以使用 `My.Application.Log` 和 `My.Log` 物件，記錄應用程式中所發生的例外狀況資訊。  這些範例會顯示如何使用 `My.Application.Log.WriteException` 方法，記錄您明確攔截的例外狀況，以及未處理的例外狀況。  
  
 如需記錄追蹤資訊，請使用 `My.Application.Log.WriteEntry` 方法。  如需詳細資訊，請參閱 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>。  
  
### 若要記錄已處理的例外狀況  
  
1.  建立會產生例外狀況資訊的方法。  
  
     [!CODE [VbVbalrMyApplicationLog#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#9)]  
  
2.  使用 `Try...Catch` 區塊，攔截例外狀況。  
  
     [!CODE [VbVbalrMyApplicationLog#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#6)]  
  
3.  將會產生例外狀況的程式碼放入 `Try` 區塊中。  
  
     取消 `Dim` 和 `MsgBox` 行的註解，會造成 <xref:System.NullReferenceException> 例外狀況。  
  
     [!CODE [VbVbalrMyApplicationLog#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#7)]  
  
4.  在 `Catch` 區塊中，使用 `My.Application.Log.WriteException` 方法寫入例外狀況資訊。  
  
     [!CODE [VbVbalrMyApplicationLog#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#8)]  
  
     下列範例顯示完整記錄已處理的例外狀況的程式碼。  
  
     [!CODE [VbVbalrMyApplicationLog#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#10)]  
  
### 若要記錄未處理的例外狀況  
  
1.  在 \[**方案總管**\] 中選取專案。  在 \[**專案**\] 功能表上，選擇 \[**屬性**\]。  
  
2.  按一下 \[**應用程式**\] 索引標籤。  
  
3.  按一下 \[**檢視應用程式事件**\] 按鈕，開啟 \[程式碼編輯器\]。  
  
     這會開啟 ApplicationEvents.vb 檔案。  
  
4.  在程式碼編輯器中開啟 ApplicationEvents.vb 檔案。  在 \[**一般**\] 功能表上，選擇 \[**MyApplication 事件**\]。  
  
5.  在 \[**宣告**\] 功能表中，選擇 \[**UnhandledException**\]。  
  
     應用程式會在主應用程式執行之前引發 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> 事件。  
  
6.  將 `My.Application.Log.WriteException` 方法加入至 `UnhandledException` 事件處理常式。  
  
     [!CODE [VbVbalrMyApplicationLog#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#4)]  
  
     下列範例顯示完整的程式碼，記錄未處理的例外狀況。  
  
     [!CODE [VbVbalrMyApplicationLog#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#5)]  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [使用應用程式記錄檔](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [如何：寫入記錄訊息](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)   
 [逐步解說：判斷 My.Application.Log 寫入資訊的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)   
 [逐步解說：變更 My.Application.Log 寫入資訊的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)