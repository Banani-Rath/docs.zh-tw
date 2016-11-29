---
title: "Overflow (Visual Basic Run-Time Error) | Microsoft Docs"
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
  - "vbrERRID_Overflow"
dev_langs: 
  - "VB"
ms.assetid: c6a23279-3086-412a-bcff-ff8ed2cb8c6f
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Overflow (Visual Basic Run-Time Error)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

嘗試進行的指派超出設定目標的限制時，就會造成溢位。  
  
### 若要更正這個錯誤  
  
1.  請確定指派、計算和資料型別轉換的結果，在該實值型別許可的變數範圍中不會太大，並且視需要將數值指定到可放置較大數值範圍的型別變數中。  
  
2.  請確定屬性的指派，符合產生屬性的範圍。  
  
3.  請確定計算中所使用之已強制轉換為整數的數字，不會產生大於整數範圍的結果。  
  
## 請參閱  
 <xref:System.Int32.MaxValue?displayProperty=fullName>   
 <xref:System.Double.MaxValue?displayProperty=fullName>   
 [Data Types](../../../visual-basic/language-reference/data-types/data-type-summary.md)   
 [Error Types](../../../visual-basic/programming-guide/language-features/error-types.md)