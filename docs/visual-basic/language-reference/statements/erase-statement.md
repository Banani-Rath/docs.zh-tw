---
title: "Erase Statement (Visual Basic) | Microsoft Docs"
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
  - "vb.Erase"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "Erase keyword"
  - "Erase statement"
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Erase Statement (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

可用於釋放陣列變數和解除配置其元素的記憶體。  
  
## 語法  
  
```  
Erase arraylist  
```  
  
## 組件  
 `arraylist`  
 必要項。  可消除的陣列變數清單。  變數之間以逗號 \( , \) 來分隔。  
  
## 備註  
 `Erase` 陳述式只可以出現在程序層次。  這表示您可以在程序內釋放陣列，但是不可以在類別或模組層次釋放陣列。  
  
 `Erase` 陳述式的效用和指派 `Nothing` 給每個陣列變數相同。  
  
## 範例  
 下列範例會使用 `Erase` 陳述式清除兩個陣列，並釋放它們的記憶體 \(分別有 1000 和 100 個儲存項目\)。  然後，`ReDim` 陳述式會將新的陣列執行個體指派給三維陣列。  
  
 [!CODE [VbVbalrStatements#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#19)]  
  
## 請參閱  
 [Nothing](../../../visual-basic/language-reference/nothing.md)   
 [ReDim Statement](../../../visual-basic/language-reference/statements/redim-statement.md)