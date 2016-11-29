---
title: "Error creating assembly manifest: &lt;error message&gt; | Microsoft Docs"
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
  - "bc30140"
  - "vbc30140"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30140"
ms.assetid: 1beb5aa0-7b79-4c85-946b-5c2d0a41d1d2
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Error creating assembly manifest: &lt;error message&gt;
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

[!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 編譯器呼叫組件連結器 \(Al.exe，也稱為 Alink\) 使用資訊清單產生組件。  連結器在建立組件的前置發出階段回報了錯誤。  
  
 如果指定的金鑰檔或金鑰容器有問題，便可能發生此情形。  若要完全簽署組件，您必須提供有效的金鑰檔，其中包含公開和私密金鑰的相關資訊。  若要延遲簽署組件，您必須選取 \[僅延遲簽署\] 核取方塊，並提供有效的金鑰檔，其中包含公開金鑰資訊的相關資訊。  延遲簽署組件時不需要私密金鑰。  如需詳細資訊，請參閱[How to: Sign an Assembly \(Visual Studio\)](http://msdn.microsoft.com/zh-tw/f468a7d3-234c-4353-924d-8e0ae5896564)。  
  
 **錯誤 ID︰**BC30140  
  
### 更正這個錯誤  
  
1.  檢查引用的錯誤訊息，並參考主題 [Al.exe Tool Errors and Warnings](http://msdn.microsoft.com/zh-tw/7f125d49-0a03-47a6-9ba9-d61a679a7d4b)，以取得錯誤 AL1019 的進一步說明和建議  
  
2.  如果錯誤持續發生，請收集情況的相關資訊，並通知 Microsoft 產品支援服務。  
  
## 請參閱  
 [How to: Sign an Assembly \(Visual Studio\)](http://msdn.microsoft.com/zh-tw/f468a7d3-234c-4353-924d-8e0ae5896564)   
 [專案設計工具、簽署頁](/visual-studio/ide/reference/signing-page-project-designer)   
 [Al.exe \(組件連結器\)](../Topic/Al.exe%20\(Assembly%20Linker\).md)   
 [Al.exe Tool Errors and Warnings](http://msdn.microsoft.com/zh-tw/7f125d49-0a03-47a6-9ba9-d61a679a7d4b)   
 [告訴我們](/visual-studio/ide/talk-to-us)