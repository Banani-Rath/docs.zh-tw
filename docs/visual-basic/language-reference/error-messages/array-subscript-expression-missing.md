---
title: "Array subscript expression missing | Microsoft Docs"
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
  - "bc30306"
  - "vbc30306"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC30306"
ms.assetid: 3c0d9732-ee37-436f-a1df-29d65712f48a
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Array subscript expression missing
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

陣列初始化遺漏一或多個定義陣列界限的註標 \(Subscript\)。  例如，陳述式可能包含運算式 `myArray (5,5,,10)`，其中遺漏了第三個註標。  
  
 **錯誤 ID**︰BC30306  
  
### 若要更正這個錯誤  
  
-   提供遺漏的註標。  
  
## 請參閱  
 [陣列](../../../visual-basic/programming-guide/language-features/arrays/index.md)