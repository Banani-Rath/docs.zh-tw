---
title: "How to: Receive Strings From Serial Ports in Visual Basic | Microsoft Docs"
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
  - "serial ports, retrieving strings"
  - "strings [Visual Basic], retrieving from serial ports"
  - "My.Resources object"
ms.assetid: 8371ce2c-e1c7-476b-a86d-9afc2614b6b7
caps.latest.revision: 21
caps.handback.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Receive Strings From Serial Ports in Visual Basic
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

本主題會描述如何在 [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 中使用 `My.Computer.Ports` 接收來自電腦序列埠的字串。  
  
### 若要接收來自序列埠的字串  
  
1.  將傳回字串初始化。  
  
     [!CODE [VbVbalrMyComputer#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#38)]  
  
2.  判斷會由哪個序列埠提供字串，  這個範例假設會是 `COM1`。  
  
3.  請使用 `My.Computer.Ports.OpenSerialPort` 方法取得對連接埠的參考。  如需詳細資訊，請參閱 <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>。  
  
     即使發生例外狀況，`Try...Catch...Finally` 區塊也會允許應用程式關閉序列埠。  所有控制序列埠的程式碼應該都會顯示在這個區塊內。  
  
     [!CODE [VbVbalrMyComputer#39](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#39)]  
  
4.  建立 `Do` 迴圈 \(Loop\) 用於讀取文字行，直到再也沒有可用的文字行為止。  
  
     [!CODE [VbVbalrMyComputer#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#40)]  
  
5.  使用 <xref:System.IO.Ports.SerialPort.ReadLine%2A> 方法，從序列埠讀取下一個可用的文字行。  
  
     [!CODE [VbVbalrMyComputer#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#41)]  
  
6.  使用 `If` 陳述式 \(Statement\) 判斷 <xref:System.IO.Ports.SerialPort.ReadLine%2A> 方法是否傳回 `Nothing` \(這表示再也沒有可用的文字\)。  如果它傳回了 `Nothing`，請結束 `Do` 迴圈。  
  
     [!CODE [VbVbalrMyComputer#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#42)]  
  
7.  將 `Else` 區塊加入至 `If` 陳述式，以便處理已實際讀取到字串的情況。  此區塊會將來自序列埠的字串附加至傳回字串。  
  
     [!CODE [VbVbalrMyComputer#43](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#43)]  
  
8.  傳回字串。  
  
     [!CODE [VbVbalrMyComputer#44](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#44)]  
  
## 範例  
 [!CODE [VbVbalrMyComputer#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#37)]  
  
 這個程式碼範例也可做為 IntelliSense 程式碼片段。  在程式碼片段選擇器中，這個程式碼片段位於 \[**連線和網路**\] 中。  如需詳細資訊，請參閱 [程式碼片段](/visual-studio/ide/code-snippets)。  
  
## 編譯程式碼  
 這個範例會假設電腦所使用的是 `COM1`。  
  
## 穩固程式設計  
 這個範例會假設電腦所使用的是 `COM1`。  為了具有更大的彈性，程式碼應該允許使用者從可用序列埠清單中選取想要的序列埠。  如需詳細資訊，請參閱 [How to: Show Available Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)。  
  
 這個範例使用 `Try...Catch...Finally` 區塊，確定應用程式會關閉連接埠並攔截逾時例外狀況。  如需詳細資訊，請參閱 [Try...Catch...Finally Statement](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)。  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Devices.Ports>   
 <xref:System.IO.Ports.SerialPort?displayProperty=fullName>   
 [How to: Dial Modems Attached to Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-dial-modems-attached-to-serial-ports.md)   
 [How to: Send Strings to Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-send-strings-to-serial-ports.md)   
 [How to: Show Available Serial Ports](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)