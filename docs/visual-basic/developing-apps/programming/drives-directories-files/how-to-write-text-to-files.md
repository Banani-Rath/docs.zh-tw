---
title: "How to: Write Text to Files in Visual Basic | Microsoft Docs"
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
  - "files, writing to"
  - "text, writing to files"
  - "writing to files"
  - "examples [Visual Basic], text files"
ms.assetid: 304956eb-530d-4df7-b48f-9b4d1f2581a0
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Write Text to Files in Visual Basic
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

<xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> 方法可以用來將文字寫入檔案。  如果指定的檔案不存在，就會建立檔案。  
  
## 程序  
  
#### 若要將文字寫入檔案  
  
-   使用 `WriteAllText` 方法將文字寫入檔案，並指定要寫入的檔案與文字。  此範例會將 `"This is new text."` 這一行寫入名為 `test.txt` 的檔案，並將文字附加至檔案中現有的文字。  
  
     [!CODE [VbFileIOWrite#3](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOWrite#3)]  
  
#### 若要將連續的字串寫入檔案  
  
-   在字串集合中執行迴圈。  使用 `WriteAllText` 方法將文字寫入檔案，指定要加入的目標檔，並將 `append` 設定為 `True`。  
  
     此範例會將 `Documents and Settings` 目錄中的檔案名稱寫入 `FileList.txt`，並在每個名稱之間插入歸位字元 \(Carriage Return\) 以增加可讀性。  
  
     [!CODE [VbFileIOWrite#4](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIOWrite#4)]  
  
## 穩固程式設計  
 下列情形可能會造成例外狀況 \(Exception\)：  
  
-   因下列其中一項原因而導致路徑無效：它是長度為零的字串、它只包含空白字元、它包含無效的字元，或者它是裝置路徑 \(開頭為 \\\\.  \\\) \(<xref:System.ArgumentException>\).  
  
-   路徑無效，因為它是 `Nothing` \(<xref:System.ArgumentNullException>\)。  
  
-   `File` 指向不存在的路徑 \(<xref:System.IO.FileNotFoundException> 或 <xref:System.IO.DirectoryNotFoundException>\)。  
  
-   檔案正由另一個程序使用中，或發生 I\/O 錯誤 \(<xref:System.IO.IOException>\)。  
  
-   路徑超過系統定義的最大長度 \(<xref:System.IO.PathTooLongException>\)。  
  
-   路徑中的檔案或目錄名稱含有冒號 \(:\)，或者是無效的格式 \(<xref:System.NotSupportedException>\)。  
  
-   使用者缺乏必要的使用權限來檢視路徑 \(<xref:System.Security.SecurityException>\)。  
  
-   磁碟已满，且 `WriteAllText` 的呼叫失敗 \(<xref:System.IO.IOException>\)。  
  
 如果是在部分信任的內容中執行，則程式碼可能會因權限不足而擲回例外狀況。  如需詳細資訊，請參閱[Code Access Security Basics](../Topic/Code%20Access%20Security%20Basics.md)。  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.FileIO.FileSystem>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>   
 [How to: Read from Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-text-files.md)