---
title: "&#39;Set&#39; accessor of property &#39;&lt;propertyname&gt;&#39; is not accessible | Microsoft Docs"
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
  - "vbc31102"
  - "bc31102"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC31102"
ms.assetid: 6f7b31b7-3656-4ae1-8851-90f5f4c6950a
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &#39;Set&#39; accessor of property &#39;&lt;propertyname&gt;&#39; is not accessible
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

陳述式會在沒有屬性之 `Set` 程序的存取權限時，嘗試儲存屬性的值。  
  
 如果 [Set Statement](../../../visual-basic/language-reference/statements/set-statement.md) 是以比 [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md)更受限的存取層級來標記，則在下列情況中嘗試設定屬性值時會失敗：  
  
-   `Set` 陳述式已標記為 [Private](../../../visual-basic/language-reference/modifiers/private.md)，且呼叫程式碼是在定義屬性的類別或結構之外。  
  
-   `Set` 陳述式已標記為 [Protected](../../../visual-basic/language-reference/modifiers/protected.md)，且呼叫程式碼不在定義屬性的類別或結構中，也不在衍生類別中。  
  
-   `Set` 陳述式標記為 [Friend](../../../visual-basic/language-reference/modifiers/friend.md)，且呼叫程式碼不在所定義之屬性所在的同一個組件中。  
  
 **錯誤 ID︰**BC31102  
  
### 若要更正這個錯誤  
  
-   如果您可以控制定義屬性的原始程式碼，請考慮使用與屬性本身相同的存取層級宣告 `Set` 程序。  
  
-   如果您沒有定義該屬性之原始程式碼的控制權，或者必須對 `Set` 程序的存取層級做出比屬性本身更嚴格的限制，則請嘗試將設定屬性值的陳述式移到對該屬性有較佳存取權的程式碼區域。  
  
## 請參閱  
 [屬性程序](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)   
 [How to: Declare a Property with Mixed Access Levels](../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-a-property-with-mixed-access-levels.md)