---
title: "How to: Convert Strings into an Array of Bytes in Visual Basic | Microsoft Docs"
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
  - "string conversion, arrays"
  - "arrays [Visual Basic], converting strings to"
  - "byte arrays"
  - "examples [Visual Basic], string conversion"
  - "arrays [Visual Basic], byte arrays"
ms.assetid: f477d35c-a3fc-4a30-b1d4-cd0d353aae1d
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Convert Strings into an Array of Bytes in Visual Basic
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

這個主題顯示如何將字串轉換成位元組陣列。  
  
## 範例  
 這個範例會使用 <xref:System.Text.Encoding.Unicode%2A?displayProperty=fullName> 編碼類別的 <xref:System.Text.Encoding.GetBytes%2A> 方法，將字串轉換成位元組陣列。  
  
 [!CODE [VbVbalrStrings#74](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#74)]  
  
 您可以從數個編碼選項中選擇，將字串轉換成位元組陣列：  
  
-   <xref:System.Text.Encoding.ASCII%2A?displayProperty=fullName>：取得 ASCII \(7 位元\) 字元集的編碼方式。  
  
-   <xref:System.Text.Encoding.BigEndianUnicode%2A?displayProperty=fullName>：使用位元組由大到小的位元組順序，取得 UTF\-16 格式的編碼方式。  
  
-   <xref:System.Text.Encoding.Default%2A?displayProperty=fullName>：取得系統之目前 ANSI 字碼頁的編碼方式。  
  
-   <xref:System.Text.Encoding.Unicode%2A?displayProperty=fullName>：使用位元組由小到大的位元組順序，取得 UTF\-16 格式的編碼方式。  
  
-   <xref:System.Text.Encoding.UTF32%2A?displayProperty=fullName>：使用位元組由小到大的位元組順序，取得 UTF\-32 格式的編碼方式。  
  
-   <xref:System.Text.Encoding.UTF7%2A?displayProperty=fullName>：取得 UTF\-7 格式的編碼方式。  
  
-   <xref:System.Text.Encoding.UTF8%2A?displayProperty=fullName>：取得 UTF\-8 格式的編碼方式。  
  
## 請參閱  
 <xref:System.Text.Encoding?displayProperty=fullName>   
 <xref:System.Text.Encoding.GetBytes%2A>   
 [How to: Convert an Array of Bytes into a String in Visual Basic](../../../../visual-basic/programming-guide/language-features/strings/how-to-convert-an-array-of-bytes-into-a-string.md)