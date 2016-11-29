---
title: "Bad DLL calling convention | Microsoft Docs"
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
  - "vbrID49"
dev_langs: 
  - "VB"
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Bad DLL calling convention
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

傳遞至動態連結程式庫 \(DLL\) 的引數，必須完全符合常式所預期的引數。  呼叫慣例可處理引數的數目、型別和順序。  您的程式可能正在呼叫 DLL 中某個常式，並且由錯誤的型別或引數數目進行傳遞。  
  
### 若要更正這個錯誤  
  
1.  請確定所有的引數型別，皆符合您正在呼叫的常式宣告中指定的型別。  
  
2.  請確定您正在傳遞的引數數目，與目前呼叫的常式宣告中的數目相同。  
  
3.  如果 DLL 常式的引數必須為數值，請確定常式宣告中已經將這些引數指定為 `ByVal`。  
  
## 請參閱  
 [Error Types](../../../visual-basic/programming-guide/language-features/error-types.md)   
 [Call Statement](../../../visual-basic/language-reference/statements/call-statement.md)   
 [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md)