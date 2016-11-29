---
title: "Nullable type inference is not supported in this context | Microsoft Docs"
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
  - "vbc36629"
  - "bc36629"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC36629"
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
caps.latest.revision: 5
caps.handback.revision: 5
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Nullable type inference is not supported in this context
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

實值型別和結構可以宣告成可為 Null。  
  
```vb#  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 不過，可為 Null 的宣告和型別推斷不可一起使用。  下列範例會造成此錯誤。  
  
```vb#  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **錯誤 ID**：BC36629  
  
### 若要更正這個錯誤  
  
-   使用 `As` 子句，將變數宣告成可為 Null。  
  
## 請參閱  
 [Nullable Value Types](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)   
 [Local Type Inference](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)