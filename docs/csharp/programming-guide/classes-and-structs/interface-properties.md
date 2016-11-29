---
title: "介面屬性 (C# 程式設計手冊) | Microsoft Docs"
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
  - "介面 [C#], 屬性"
  - "屬性 [C#], 介面上"
ms.assetid: 6503e9ed-33d7-44ec-b4c1-cc16c084b795
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 介面屬性 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

屬性可以在 [interface](../../../csharp/language-reference/keywords/interface.md) 上宣告，  下列是介面索引子存取子的範例：  
  
 [!CODE [csProgGuideProperties#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#14)]  
  
 介面屬性的存取子沒有主體，  因此，存取子的目的是指示屬性是讀寫、唯讀或唯寫。  
  
## 範例  
 在這個範例裡，`IEmployee` 介面有 `Name` 讀寫屬性和 `Counter` 唯讀屬性。  `Employee` 類別實作 `IEmployee` 介面，並且使用這兩個屬性。  程式讀取新員工的名稱和員工的目前編號，並顯示員工名稱和計算過的員工編號。  
  
 您可以使用屬性的完整名稱，這個屬性會參考成員宣告的介面。  例如：  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 這稱為[明確介面實作](../../../csharp/programming-guide/interfaces/explicit-interface-implementation.md)。  例如，如果 `Employee` 類別實作 `ICitizen` 和 `IEmployee` 這兩個介面，而且兩個介面都有 `Name` 屬性，則將會需要明確介面成員實作，  即如下的屬性宣告：  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 在 `IEmployee` 介面上實作 `Name` 屬性，在下列宣告時：  
  
 [!CODE [csProgGuideProperties#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#17)]  
  
 在 `ICitizen` 介面上實作 `Name` 屬性。  
  
 [!CODE [csProgGuideProperties#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#15)]  
  
  **`210 Hazem Abolrous`**    
## 範例輸出  
 `Enter number of employees: 210`  
  
 `Enter the name of the new employee: Hazem Abolrous`  
  
 `The employee information:`  
  
 `Employee number: 211`  
  
 `Employee name: Hazem Abolrous`  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [屬性](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [使用屬性](../../../csharp/programming-guide/classes-and-structs/using-properties.md)   
 [屬性與索引子之間的比較](../../../csharp/programming-guide/indexers/comparison-between-properties-and-indexers.md)   
 [索引子](../../../csharp/programming-guide/indexers/index.md)   
 [介面](../../../csharp/programming-guide/interfaces/index.md)