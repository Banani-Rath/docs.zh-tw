---
title: "Implements Clause (Visual Basic) | Microsoft Docs"
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
  - "vb.ImplementsClause"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "interface implementation, reimplementation"
  - "interface members, reimplementation"
  - "interface members, Implements keyword"
  - "interface members"
  - "members, reimplementation"
  - "interface implementation, Implements keyword"
  - "interface members, implementing"
  - "Implements keyword"
  - "Implements statement, about Implements"
  - "members, implementing"
  - "members, Implements keyword"
  - "reimplementation"
ms.assetid: 5252cdf9-964d-4fc6-af0f-0449b7126b5a
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Implements Clause (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

表示類別或結構成員會為定義於介面中的成員提供實作。  
  
## 備註  
 `Implements` 關鍵字與 [Implements Statement](../../../visual-basic/language-reference/statements/implements-statement.md)不相同。  您會使用 `Implements` 陳述式 \(Statement\)，指定類別或結構實作一個或多個介面，然後針對每個成員使用 `Implements` 關鍵字，以指定所要實作的介面和成員。  
  
 如果一個類別或結構實作了一個介面，則必須在 [Class Statement](../../../visual-basic/language-reference/statements/class-statement.md) 或 [Structure Statement](../../../visual-basic/language-reference/statements/structure-statement.md) 之後直接包含 `Implements` 陳述式，而且必須實作由介面定義的所有成員。  
  
## 重新實作  
 在衍生類別中，您可重新實作已實作基底類別的介面成員。  在下列方面，這與覆寫基底類別成員不同：  
  
-   基底類別成員不需是要重新實作的 [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md)。  
  
-   您可用不同名稱來重新實作該成員。  
  
 `Implements` 關鍵字可用於以下內容中：  
  
 [Event Statement](../../../visual-basic/language-reference/statements/event-statement.md)  
  
 [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub Statement](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## 請參閱  
 [Implements Statement](../../../visual-basic/language-reference/statements/implements-statement.md)   
 [Interface Statement](../../../visual-basic/language-reference/statements/interface-statement.md)   
 [Class Statement](../../../visual-basic/language-reference/statements/class-statement.md)   
 [Structure Statement](../../../visual-basic/language-reference/statements/structure-statement.md)