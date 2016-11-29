---
title: "How to: Create a Collection Used by a Collection Initializer (Visual Basic) | Microsoft Docs"
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
  - "collection initializers [Visual Basic]"
ms.assetid: c858db10-424d-47e0-92cd-e08087cc5ebc
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Create a Collection Used by a Collection Initializer (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

當您使用集合初始設定式建立集合時，Visual Basic 編譯器會搜尋集合型別的 `Add` 方法，而且 `Add` 方法的參數型別會與集合初始設定式中的值型別相符。  這個 `Add` 方法是用來將集合初始設定式中的值填入集合。  
  
## 範例  
 下列範例示範 `OrderCollection` 集合，此集合包含可供集合初始設定式用來加入型別為 `Order` 之物件的公用 `Add` 方法。  `Add` 方法可讓您使用縮短的集合初始設定式語法。  
  
 [!CODE [VbVbalrCollectionInitializersHowTo2#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2#4)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo2#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2#1)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo2#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2#2)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo2#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo2#3)]  
  
## 請參閱  
 [Collection Initializers](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)   
 [How to: Create an Add Extension Method Used by a Collection Initializer](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-an-add-extension-method-used-by-a-collection-initializer.md)