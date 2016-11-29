---
title: "泛型和屬性 (C# 程式設計手冊) | Microsoft Docs"
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
  - "屬性 [C#], 使用泛型"
  - "泛型 [C#], 屬性"
ms.assetid: da9fc326-4648-454a-8e13-3911a2edefd7
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 泛型和屬性 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

將屬性套用到泛型型別的方式，就跟非泛型型別一樣。  如需套用屬性的詳細資訊，請參閱[屬性](../Topic/Attributes%20\(C%23%20and%20Visual%20Basic\).md)。  
  
 自訂屬性只能參考開放泛型型別 \(即不提供型別引數的泛型型別\)，以及封閉建構的泛型型別 \(即提供引數給所有型別參數的泛型型別\)。  
  
 下列範例使用了這個自訂屬性：  
  
 [!CODE [csProgGuideGenerics#48](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#48)]  
  
 屬性可參考開放泛型型別：  
  
 [!CODE [csProgGuideGenerics#49](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#49)]  
  
 使用適當數目的逗號指定多個型別參數。  在此範例中，`GenericClass2` 具有兩個型別參數：  
  
 [!CODE [csProgGuideGenerics#50](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#50)]  
  
 屬性可參考封閉建構的泛型型別：  
  
 [!CODE [csProgGuideGenerics#51](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#51)]  
  
 參考泛型型別參數的屬性會造成編譯時期錯誤：  
  
 [!CODE [csProgGuideGenerics#52](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#52)]  
  
 泛型型別無法繼承自 <xref:System.Attribute>：  
  
 [!CODE [csProgGuideGenerics#53](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#53)]  
  
 若要取得執行階段的泛型型別或型別參數的詳細資訊，您可以使用 <xref:System.Reflection> 方法。  如需詳細資訊，請參閱[泛型和反映](../../../csharp/programming-guide/generics/generics-and-reflection.md)。  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [泛型](../../../csharp/programming-guide/generics/index.md)   
 [屬性](../Topic/Extending%20Metadata%20Using%20Attributes.md)