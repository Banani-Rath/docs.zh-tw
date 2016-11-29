---
title: "&#39;Line&#39; statements are no longer supported (Visual Basic Compiler Error) | Microsoft Docs"
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
  - "bc30830"
  - "vbc30830"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30830"
ms.assetid: 4734bc1d-882e-4555-b498-1f1ec0399d16
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &#39;Line&#39; statements are no longer supported (Visual Basic Compiler Error)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

不再支援 Line 陳述式。  檔案 I\/O 功能可做為 `Microsoft.VisualBasic.FileSystem.LineInput` 使用，而圖形功能可做為 `System.Drawing.Graphics.DrawLine` 使用。  
  
 **錯誤 ID︰**BC30830  
  
### 若要更正這個錯誤  
  
1.  如果執行檔案存取，請使用 `Microsoft.VisualBasic.FileSystem.LineInput`。  
  
2.  如果執行圖形，請使用 `System.Drawing.Graphics.Drawline`。  
  
## 請參閱  
 <xref:System.IO>   
 <xref:System.Drawing>   
 [File Access with Visual Basic](../../../visual-basic/developing-apps/programming/drives-directories-files/file-access.md)