---
title: "如何：組合委派 (多點傳送委派) (C# 程式設計手冊) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "委派 [C#], 組合"
  - "多點傳送委派 [C#]"
ms.assetid: 4e689450-6d0c-46de-acfd-f961018ae5dd
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：組合委派 (多點傳送委派) (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

本範例示範如何建立多點傳送委派。  [delegate](../../../csharp/language-reference/keywords/delegate.md) 物件具有的一種有用屬性，就是可使用 `+` 運算子將多個物件指派給一個委派執行個體。  多點傳送委派包含已指派委派的清單。  呼叫多點傳送委派時，它會依順序叫用清單中的委派。  只有相同型別的委派才能加以結合。  
  
 `-` 運算子可用來從多點傳送委派中移除某個元件委派。  
  
## 範例  
 [!CODE [csProgGuideDelegates#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#11)]  
  
## 請參閱  
 <xref:System.MulticastDelegate>   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [事件](../../../csharp/programming-guide/events/index.md)