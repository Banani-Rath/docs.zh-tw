---
title: "Logging Information from the Application (Visual Basic) | Microsoft Docs"
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
  - "Log object"
  - "My.Log object"
  - "applications [Visual Basic], logging information from"
  - "logging"
  - "My.Application.Log object"
  - "examples [Visual Basic], logging application information"
ms.assetid: 8bf4f047-22d6-48d6-aec5-93b98ad5b8e8
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Logging Information from the Application (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

本章節內含的主題會涵蓋如何使用 `My.Application.Log` 或 `My.Log` 物件記錄來自應用程式的資訊，以及如何擴充應用程式的記錄功能。  
  
 `Log` 物件會提供用於將資訊寫入應用程式之記錄檔接聽程式的方法，而 `Log` 物件的進階 `TraceSource` 屬性則會提供詳細的組態資訊。  應用程式的組態檔會設定 `Log` 物件。  
  
 `My.Log` 物件僅適用於 ASP.NET 應用程式。  針對用戶端應用程式，請使用 `My.Application.Log`。  如需詳細資訊，請參閱 <xref:Microsoft.VisualBasic.Logging.Log>。  
  
## 工作  
  
|若要|請參閱|  
|--------|---------|  
|將事件資訊寫入應用程式的記錄檔|[如何：寫入記錄訊息](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)|  
|將例外狀況資訊寫入應用程式的記錄檔|[How to: Log Exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md)|  
|在應用程式啟動和關閉時，將追蹤資訊寫入應用程式的記錄檔|[如何：在應用程式啟動或關閉時記錄訊息](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-messages-when-the-application-starts-or-shuts-down.md)|  
|設定 `My.Application.Log` 將資訊寫入文字檔|[How to: Write Event Information to a Text File](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-event-information-to-a-text-file.md)|  
|設定 `My.Application.Log` 將資訊寫入事件記錄檔|[如何：寫入應用程式事件記錄檔](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-to-an-application-event-log.md)|  
|變更 `My.Application.Log` 寫入資訊的位置|[逐步解說：變更 My.Application.Log 寫入資訊的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)|  
|判斷 `My.Application.Log` 寫入資訊的位置|[逐步解說：判斷 My.Application.Log 寫入資訊的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)|  
|為 `My.Application.Log` 建立自訂的記錄檔接聽程式|[Walkthrough: Creating Custom Log Listeners](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-creating-custom-log-listeners.md)|  
|篩選 `My.Application.Log` 記錄檔的輸出|[Walkthrough: Filtering My.Application.Log Output](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-filtering-my-application-log-output.md)|  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 [使用應用程式記錄檔](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [Troubleshooting: Log Listeners](../../../../visual-basic/developing-apps/programming/log-info/troubleshooting-log-listeners.md)