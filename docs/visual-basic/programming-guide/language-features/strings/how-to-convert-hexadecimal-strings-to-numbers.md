---
title: "How to: Convert Hexadecimal Strings to Numbers (Visual Basic) | Microsoft Docs"
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
  - "numbers, hexadecimals"
  - "hexadecimals, decimals"
  - "examples [Visual Basic], string conversion"
  - "decimals, hexadecimals"
  - "string conversion, hexadecimal to numbers"
ms.assetid: 76675807-eadb-4c08-bd50-e6c6ff4b8ced
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Convert Hexadecimal Strings to Numbers (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

這個範例會使用 <xref:System.Convert.ToInt32%2A> 方法，將十六進位字串轉換成整數。  
  
### 若要將十六進位字串轉換成數字  
  
-   使用 <xref:System.Convert.ToInt32%2A> 方法，將以 16 為基底表示的數字轉換成整數。  
  
     <xref:System.Convert.ToInt32%2A> 方法的第一個引數是要轉換的字串。  第二個引數會描述數字用以表示的基底，十六進位的基底為 16。  
  
     [!CODE [VbVbalrStrings#62](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#62)]  
  
## 請參閱  
 <xref:Microsoft.VisualBasic.Conversion.Hex%2A>   
 <xref:System.Convert.ToInt32%2A>