---
title: "逐步解說：變更 My.Application.Log 寫入資訊的位置 (Visual Basic) | Microsoft Docs"
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
  - "My.Application.Log 物件, 逐步解說"
  - "事件記錄檔, 變更輸出位置"
ms.assetid: ecc74f95-743c-450d-93f6-09a30db0fe4a
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# 逐步解說：變更 My.Application.Log 寫入資訊的位置 (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

您可以使用 `My.Application.Log` 和 `My.Log` 物件來記錄應用程式中發生之事件的相關資訊。 本逐步解說示範如何覆寫預設設定，而且使 `Log` 物件寫入至其他記錄檔接聽程式。  
  
## 必要條件  
 `Log` 物件可以將資訊寫入數個記錄檔接聽程式。 在變更設定前，您需要判斷目前的記錄檔接聽程式設定。 如需詳細資訊，請參閱[逐步解說：判斷 My.Application.Log 寫入資訊的位置](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)。  
  
 您可能會想要檢閱 [How to: Write Event Information to a Text File](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-event-information-to-a-text-file.md) 或 [如何：寫入應用程式事件記錄檔](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-to-an-application-event-log.md)。  
  
### 加入接聽程式  
  
1.  在**方案總管**中，以滑鼠右鍵按一下 app.config 並選擇 \[開啟\]。  
  
     \-或\-  
  
     如果沒有 app.config 檔案︰  
  
    1.  在 \[**專案**\] 功能表中，選擇 \[**加入新項目**\]。  
  
    2.  在 \[加入新項目\] 對話方塊中，選取 \[應用程式組態檔\]。  
  
    3.  按一下 \[加入\]。  
  
2.  找出 `<listeners>` 區段，其位於 `<sources>` 區段中具有 `name` 屬性 "DefaultSource" 的 `<source>` 區段下。`<sources>` 區段位於最上層 `<configuration>` 區段中的 `<system.diagnostics>` 區段。  
  
3.  將這些項目加入至該 `<listeners>` 區段。  
  
    ```  
    <!-- Uncomment to connect the application file log. -->  
    <!-- <add name="FileLog" /> -->  
    <!-- Uncomment to connect the event log. -->  
    <!-- <add name="EventLog" /> -->  
    <!-- Uncomment to connect the event log. -->  
    <!-- <add name="Delimited" /> -->  
    <!-- Uncomment to connect the XML log. -->  
    <!-- <add name="XmlWriter" /> -->  
    <!-- Uncomment to connect the console log. -->  
    <!-- <add name="Console" /> -->  
    ```  
  
4.  取消註解您想要收到 `Log` 訊息的記錄檔接聽程式。  
  
5.  找出位於最上層 `<configuration>` 區段中 `<system.diagnostics>` 區段的 `<sharedListeners>` 區段。  
  
6.  將這些項目加入至該 `<sharedListeners>` 區段。  
  
    ```  
    <add name="FileLog"  
         type="Microsoft.VisualBasic.Logging.FileLogTraceListener,   
               Microsoft.VisualBasic, Version=8.0.0.0,   
               Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"  
         initializeData="FileLogWriter" />  
    <add name="EventLog"  
         type="System.Diagnostics.EventLogTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="sample application"/>  
    <add name="Delimited"   
         type="System.Diagnostics.DelimitedListTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="c:\temp\sampleDelimitedFile.txt"  
         traceOutputOptions="DateTime" />  
    <add name="XmlWriter"  
         type="System.Diagnostics.XmlWriterTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="c:\temp\sampleLogFile.xml" />  
    <add name="Console"  
         type="System.Diagnostics.ConsoleTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="true" />  
    ```  
  
7.  App.config 檔案的內容應該類似下列 XML：  
  
    ```  
    <?xml version="1.0" encoding="utf-8" ?>  
    <configuration>  
      <system.diagnostics>  
        <sources>  
          <!-- This section configures My.Application.Log -->  
          <source name="DefaultSource" switchName="DefaultSwitch">  
            <listeners>  
              <add name="FileLog"/>  
              <!-- Uncomment to connect the application file log. -->  
              <!-- <add name="FileLog" /> -->  
              <!-- Uncomment to connect the event log. -->  
              <!-- <add name="EventLog" /> -->  
              <!-- Uncomment to connect the event log. -->  
              <!-- <add name="Delimited" /> -->  
              <!-- Uncomment to connect the XML log. -->  
              <!-- <add name="XmlWriter" /> -->  
              <!-- Uncomment to connect the console log. -->  
              <!-- <add name="Console" /> -->  
            </listeners>  
          </source>  
        </sources>  
        <switches>  
          <add name="DefaultSwitch" value="Information" />  
        </switches>  
        <sharedListeners>  
          <add name="FileLog"  
               type="Microsoft.VisualBasic.Logging.FileLogTraceListener,   
                     Microsoft.VisualBasic, Version=8.0.0.0,   
                     Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"  
               initializeData="FileLogWriter" />  
          <add name="EventLog"  
               type="System.Diagnostics.EventLogTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="sample application"/>  
          <add name="Delimited"   
               type="System.Diagnostics.DelimitedListTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="c:\temp\sampleDelimitedFile.txt"  
               traceOutputOptions="DateTime" />  
          <add name="XmlWriter"  
               type="System.Diagnostics.XmlWriterTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="c:\temp\sampleLogFile.xml" />  
          <add name="Console"  
               type="System.Diagnostics.ConsoleTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="true" />  
        </sharedListeners>  
      </system.diagnostics>  
    </configuration>  
    ```  
  
### 重新設定接聽程式  
  
1.  從 `<sharedListeners>` 區段找出接聽程式的 `<add>` 項目。  
  
2.  `type` 屬性提供接聽程式類型的名稱。 此類型必須繼承自 <xref:System.Diagnostics.TraceListener> 類別。 使用以強式名稱方式命名的類型名稱來確定使用了正確的類型。 如需詳細資訊，請參閱下列＜參考強制命名的類型＞一節。  
  
     您可以使用的類型如下︰  
  
    -   寫入至檔案記錄檔的 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener?displayProperty=fullName> 接聽程式。  
  
    -   將資訊寫入至由 `initializeData` 參數指定之電腦事件記錄檔的 <xref:System.Diagnostics.EventLogTraceListener?displayProperty=fullName> 接聽程式。  
  
    -   寫入至由 `initializeData` 參數中指定之檔案的 <xref:System.Diagnostics.DelimitedListTraceListener?displayProperty=fullName> 和 <xref:System.Diagnostics.XmlWriterTraceListener?displayProperty=fullName> 接聽程式。  
  
    -   寫入至命令列主控台的 <xref:System.Diagnostics.ConsoleTraceListener?displayProperty=fullName> 接聽程式。  
  
     如需其他記錄檔接聽程式類型在何處寫入資訊的相關資訊，請查閱該類型的文件。  
  
3.  當應用程式建立記錄檔接聽程式物件時，會傳遞 `initializeData` 屬性作為建構函式參數。`initializeData` 屬性的意義取決於追蹤接聽項。  
  
4.  建立記錄檔接聽程式之後，應用程式會設定接聽程式的屬性。 這些屬性由 `<add>` 項目中的其他屬性定義。 如需特定接聽程式屬性的詳細資訊，請參閱該接聽程式類型的文件。  
  
### 參考強式命名的類型  
  
1.  若要確保記錄檔接聽程式使用正確的類型，請務必使用完整類型名稱和強式命名的組件名稱。 強式命名的類型語法如下所示︰  
  
     \<*類型名稱*\>、\<*組件名稱*\>、\<*版本號碼*\>、\<*文化特性*\>、\<*強式名稱*\>  
  
2.  這個程式碼範例示範在此情況下如何判斷完整類型 "System.Diagnostics.FileLogTraceListener" 之強式命名的類型。  
  
     [!CODE [VbVbalrMyApplicationLog#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#15)]  
  
     這就是輸出的資料，並可用於唯一參考強式命名的類型，如上方「加入接聽程式」 程序所示。  
  
     `Microsoft.VisualBasic.Logging.FileLogTraceListener, Microsoft.VisualBasic, Version=8.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a`  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:System.Diagnostics.TraceListener>   
 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener?displayProperty=fullName>   
 <xref:System.Diagnostics.EventLogTraceListener?displayProperty=fullName>   
 [How to: Write Event Information to a Text File](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-event-information-to-a-text-file.md)   
 [如何：寫入應用程式事件記錄檔](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-to-an-application-event-log.md)