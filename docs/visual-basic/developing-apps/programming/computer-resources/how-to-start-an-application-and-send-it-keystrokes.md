---
title: "How to: Start an Application and Send it Keystrokes (Visual Basic) | Microsoft Docs"
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
  - "keystrokes, sending"
  - "Shell command example [Visual Basic]"
  - "processes, starting and sending keystrokes"
  - "SendKeys.SendWait examples"
ms.assetid: f1303184-fce4-44fb-88b4-aac5f42d5d77
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Start an Application and Send it Keystrokes (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

這個範例會使用 `Shell` 函式啟動計算機應用程式，再使用 `My.Computer.Keyboard.SendKeys` 方法傳送按鍵輸入，將兩個數字相乘。  
  
## 範例  
 [!CODE [VbVbalrMyComputer#25](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#25)]  
  
## 穩固程式設計  
 如果找不到具有要求之處理序識別項的應用程式，則會引發 <xref:System.ArgumentException> 例外狀況。  
  
## .NET Framework 安全性  
 呼叫 `Shell` 函式需要完全信任關係 \(<xref:System.Security.SecurityException> 類別\)。  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A>   
 <xref:Microsoft.VisualBasic.Interaction.Shell%2A>   
 <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A>