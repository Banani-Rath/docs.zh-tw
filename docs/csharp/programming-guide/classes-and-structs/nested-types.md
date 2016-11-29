---
title: "巢狀類型 (C# 程式設計手冊) | Microsoft Docs"
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
  - "巢狀類型 [C#]"
ms.assetid: f2e1b315-e3d1-48ce-977f-7bae0960ba99
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 巢狀類型 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

在[類別](../../../csharp/language-reference/keywords/class.md)或[結構](../../../csharp/language-reference/keywords/struct.md)內定義的型別稱為巢狀型別。  例如：  
  
 [!CODE [csProgGuideObjects#68](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#68)]  
  
 不論外部型別是類別或結構，巢狀型別會預設為 [private](../../../csharp/language-reference/keywords/private.md)，但可以設定為 [public](../../../csharp/language-reference/keywords/public.md)、protected internal、[protected](../../../csharp/language-reference/keywords/protected.md)、[internal](../../../csharp/language-reference/keywords/internal.md) 或 [private](../../../csharp/language-reference/keywords/private.md)。  在先前範例中，`Nested` 無法由外部型別存取，但可以設為 public，如下所示：  
  
 [!CODE [csProgGuideObjects#69](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#69)]  
  
 巢狀或內部型別可存取包含型別或外部型別。  若要存取包含型別，請將它當做建構函式傳遞至巢狀型別。  例如：  
  
 [!CODE [csProgGuideObjects#70](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#70)]  
  
 巢狀型別可以存取其包含型別可存取的所有成員。  它可存取包含型別的 private 和 protected 成員，包括任何繼承的 protected 成員。  
  
 在先前的宣告，`Nested` 類別的完整名稱為 `Container.Nested`。  這是用來建立巢狀類別新執行個體的名稱，如下所示：  
  
 [!CODE [csProgGuideObjects#71](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#71)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [類別和結構](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [存取修飾詞](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)   
 [建構函式](../../../csharp/programming-guide/classes-and-structs/constructors.md)