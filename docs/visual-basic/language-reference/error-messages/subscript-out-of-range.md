---
title: "Subscript out of range (Visual Basic) | Microsoft Docs"
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
  - "vbrID9"
dev_langs: 
  - "VB"
ms.assetid: d0344a65-ec02-4caf-8d3c-9977392ca353
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Subscript out of range (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

陣列註標 \(Array Subscript\) 無效，因為它已超出許可範圍。  維度的最低註標永遠為 0，而該維度的最高註標值則是由 `GetUpperBound` 方法傳回。  
  
### 若要更正這個錯誤  
  
-   請將陣列索引變更為有效範圍內的值。  
  
## 請參閱  
 <xref:System.Array.GetUpperBound%2A?displayProperty=fullName>   
 [陣列](../../../visual-basic/programming-guide/language-features/arrays/index.md)