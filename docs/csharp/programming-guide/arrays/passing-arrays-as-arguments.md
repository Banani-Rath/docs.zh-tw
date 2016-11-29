---
title: "傳遞陣列當做引數 (C# 程式設計手冊) | Microsoft Docs"
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
  - "陣列 [C#], 當做引數傳遞"
ms.assetid: f3a0971e-c87c-4a1f-8262-bc0a3b712772
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 傳遞陣列當做引數 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

您可以將陣列當做引數傳遞至方法參數。  由於陣列是參考型別，因此方法可變更元素的值。  
  
## 將一維陣列當做引數傳遞  
 您可以將初始化的一維陣列傳遞至方法。  例如，下列陳述式會傳送陣列至列印方法。  
  
 [!CODE [csProgGuideArrays#34](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#34)]  
  
 下列程式碼顯示列印方法的部分實作。  
  
 [!CODE [csProgGuideArrays#33](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#33)]  
  
 您可以在一個步驟中初始化並傳遞新陣列，如下列範例所示。  
  
 [!CODE [CsProgGuideArrays#35](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#35)]  
  
## 範例  
  
### 描述  
 在下列範例中，會初始化字串陣列，並將其當做引數傳遞至 `PrintArray` 方法做為字串。  方法會顯示陣列的元素。  接著會呼叫 `ChangeArray` 和 `ChangeArrayElement` 方法，示範透過值傳送陣列引數無法避免改變陣列元素。  
  
### 程式碼  
 [!CODE [csProgGuideArrays#30](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#30)]  
  
## 將多維陣列當做引數傳遞  
 傳遞已初始化多維陣列至方法的方式，和傳遞一維陣列相同。  
  
 [!CODE [csProgGuideArrays#41](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#41)]  
  
 下列程式碼顯示列印方法的部分宣告，此方法接受二維陣列做為其引數。  
  
 [!CODE [csProgGuideArrays#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#36)]  
  
 您可以在一個步驟中初始化並傳遞新陣列，如下列範例所示。  
  
 [!CODE [csProgGuideArrays#32](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#32)]  
  
## 範例  
  
### 描述  
 在下列範例中，會初始化整數的二維陣列，並將其傳遞至 `Print2DArray` 方法。  方法會顯示陣列的元素。  
  
### 程式碼  
 [!CODE [csProgGuideArrays#31](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#31)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [陣列](../../../csharp/programming-guide/arrays/index.md)   
 [一維陣列](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md)   
 [多維陣列](../../../csharp/programming-guide/arrays/multidimensional-arrays.md)   
 [不規則陣列](../../../csharp/programming-guide/arrays/jagged-arrays.md)