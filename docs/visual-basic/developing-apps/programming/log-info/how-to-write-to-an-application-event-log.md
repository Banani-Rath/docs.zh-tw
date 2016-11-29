---
title: "如何：寫入應用程式事件記錄檔 (Visual Basic) | Microsoft Docs"
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
  - "Computer.EventLog 項目"
  - "WriteEntry 方法"
  - "My.Computer.EventLog 項目"
  - "事件記錄檔, 寫入至"
ms.assetid: cadbc8c1-87af-4746-934e-55b79a4f6e2b
caps.latest.revision: 21
caps.handback.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：寫入應用程式事件記錄檔 (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

您可以使用 `My.Application.Log` 和 `My.Log` 物件寫入發生在應用程式中之事件的相關資訊。 此範例示範如何設定事件記錄檔接聽程式，讓 `My.Application.Log` 將追蹤資訊寫入至應用程式事件記錄檔。  
  
 您無法寫入至安全性記錄檔。 要寫入至系統記錄檔，您必須是 LocalSystem 或 Administrator 帳戶的成員。  
  
 若要檢視事件記錄檔，您可以使用 \[伺服器總管\] 或 \[Windows 事件檢視器\]。 如需詳細資訊，請參閱[.NET Framework 中的 ETW 事件](../Topic/ETW%20Events%20in%20the%20.NET%20Framework.md)。  
  
> [!NOTE]
>  在 Windows 95、Windows 98 或 Windows Millennium Edition 上不支援事件記錄檔。  
  
### 加入及設定事件記錄檔接聽程式  
  
1.  在**方案總管**中，以滑鼠右鍵按一下 app.config 並選擇 \[開啟\]。  
  
     \-或\-  
  
     如果沒有 app.config 檔案，  
  
    1.  在 \[**專案**\] 功能表中，選擇 \[**加入新項目**\]。  
  
    2.  在 \[加入新項目\] 對話方塊中，選擇 \[應用程式組態檔\]。  
  
    3.  按一下 \[加入\]。  
  
2.  在應用程式組態檔中找出 `<listeners>` 區段。  
  
     您會找到名稱屬性為 "DefaultSource" 之 `<source>` 區段 \(位於最上層 `<configuration>` 區段底下 `<system.diagnostics>` 區段中\) 中的 `<listeners>` 區段。  
  
3.  將此項目加入至該 `<listeners>` 區段︰  
  
    ```  
    <add name="EventLog"/>  
    ```  
  
4.  找出位於最上層 `<configuration>` 區段中 `<system.diagnostics>` 區段的 `<sharedListeners>` 區段。  
  
5.  將此項目加入至該 `<sharedListeners>` 區段︰  
  
    ```  
    <add name="EventLog"  
        type="System.Diagnostics.EventLogTraceListener, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="APPLICATION_NAME"/>  
    ```  
  
     以應用程式名稱取代 `APPLICATION_NAME`。  
  
    > [!NOTE]
    >  一般而言，應用程式僅將錯誤寫入至事件記錄檔。 如需篩選記錄檔輸出的相關資訊，請參閱 [Walkthrough: Filtering My.Application.Log Output](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-filtering-my-application-log-output.md)。  
  
### 將事件資訊寫入至事件記錄檔  
  
-   使用 `My.Application.Log.WriteEntry` 或 `My.Application.Log.WriteException` 方法，將資訊寫入事件記錄檔。 如需詳細資訊，請參閱[如何：寫入記錄訊息](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)與[How to: Log Exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md)。  
  
     設定組件的事件記錄檔接聽程式之後，接聽程式會接收從該組件寫入的所有訊息 `My.Applcation.Log`。  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [使用應用程式記錄檔](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [How to: Log Exceptions](../../../../visual-basic/developing-apps/programming/log-info/how-to-log-exceptions.md)   
 [逐步解說：判斷 My.Application.Log 寫入資訊的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)