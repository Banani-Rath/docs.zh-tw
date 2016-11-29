---
title: "How to: Create an Add Extension Method Used by a Collection Initializer (Visual Basic) | Microsoft Docs"
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
ms.assetid: f64b52c7-8b11-4410-93a6-cb3aeebcc772
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# How to: Create an Add Extension Method Used by a Collection Initializer (Visual Basic)
[!INCLUDE[vs2017banner](../../../../csharp/includes/vs2017banner.md)]

當您使用集合初始設定式建立集合時，Visual Basic 編譯器會搜尋集合型別的 `Add` 方法，而且 `Add` 方法的參數型別會與集合初始設定式中的值型別相符。  這個 `Add` 方法是用來將集合初始設定式中的值填入集合。  
  
 如果沒有相符的 `Add` 方法存在，而也無法修改集合的程式碼，那麼您可以加入名為 `Add` 的擴充方法，這個擴充方法會接受集合初始設定式所需的參數。  當您使用集合初始設定式來建立泛型集合時，通常都必須這麼做。  
  
## 範例  
 下列範例示範如何將擴充方法加入至泛型 <xref:System.Collections.Generic.List%601> 型別，以便使用集合初始設定式來加入型別為 `Employee` 的物件。  擴充方法可讓您使用縮短的集合初始設定式語法。  
  
 [!CODE [VbVbalrCollectionInitializersHowTo1#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1#1)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo1#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1#2)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo1#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1#3)]  
  
## 請參閱  
 [Collection Initializers](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)   
 [How to: Create a Collection Used by a Collection Initializer](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-a-collection-used-by-a-collection-initializer.md)