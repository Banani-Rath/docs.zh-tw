---
title: "多維陣列 (C# 程式設計手冊) | Microsoft Docs"
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
  - "陣列 [C#], 多維"
  - "多維陣列 [C#]"
ms.assetid: 020ce02e-7dff-4273-8e53-bf0b33747232
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 多維陣列 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

陣列可以有一個以上的維度。  例如，下列宣告會建立四列兩行的二維陣列。  
  
 [!CODE [csProgGuideArrays#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#11)]  
  
 下列宣告會建立 4、2 及 3 三個維度的陣列。  
  
 [!CODE [csProgGuideArrays#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#12)]  
  
## 陣列初始化  
 您可以在宣告時初始化陣列，如下列範例所示。  
  
 [!CODE [csProgGuideArrays#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#13)]  
  
 您也可以不指定陣序規範就初始化陣列。  
  
 [!CODE [csProgGuideArrays#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#14)]  
  
 如果您選擇不初始化就宣告陣列變數，您必須使用 `new` 運算子來將陣列指派至變數。  下列範例顯示 `new` 的用法。  
  
 [!CODE [csProgGuideArrays#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#15)]  
  
 下列範例將值指派給特定的陣列元素。  
  
 [!CODE [csProgGuideArrays#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#16)]  
  
 同樣，下列範例會取得特定陣列元素的值，並將其指派給變數 `elementValue`。  
  
 [!CODE [csProgGuideArrays#42](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#42)]  
  
 下列程式碼範例會將陣列元素初始化為預設值 \(除了不規則陣列之外\)。  
  
 [!CODE [csProgGuideArrays#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#17)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [陣列](../../../csharp/programming-guide/arrays/index.md)   
 [一維陣列](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [不規則陣列](../../../csharp/programming-guide/arrays/jagged-arrays.md)