---
title: "隱含類型陣列 (C# 程式設計手冊) | Microsoft Docs"
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
  - "陣列 [C#], 隱含類型"
  - "C# 語言, 隱含類型陣列"
  - "隱含類型陣列 [C#]"
ms.assetid: e05be95c-6732-403d-ae42-b35f057cbbea
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 隱含類型陣列 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

您可以建立隱含型別的陣列，在其中陣列執行個體的型別是由陣列初始設定式中指定的項目推斷。  任何隱含型別變數的規則都適用於隱含型別陣列。  如需詳細資訊，請參閱[隱含類型區域變數](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md)。  
  
 隱含型別陣列通常是在查詢運算式中與匿名型別及物件和集合初始設定式一起使用。  
  
 下列範例顯示如何建立隱含型別陣列：  
  
 [!CODE [csProgGuideLINQ#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#37)]  
  
 在前述範例中，請注意隱含型別陣列中，初始化陳述式的左側不會使用方括號。  同時請注意，不規則陣列是使用 `new []` 進行初始化，如同一維陣列。  
  
## 物件初始設定式中的隱含型別陣列  
 建立包含陣列的匿名型別時，在型別的物件初始設定式中陣列必須是隱含型別。  在下列範例中，`contacts` 是匿名型別的隱含型別陣列，每個都包含名為 `PhoneNumbers` 的陣列。  請注意，`var` 關鍵字不會在物件初始設定式內部使用。  
  
 [!CODE [csProgGuideLINQ#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#38)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [隱含類型區域變數](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md)   
 [陣列](../../../csharp/programming-guide/arrays/index.md)   
 [匿名類型](../../../csharp/programming-guide/classes-and-structs/anonymous-types.md)   
 [物件和集合初始設定式](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)   
 [var](../../../csharp/language-reference/keywords/var.md)   
 [LINQ 查詢運算式](../../../csharp/programming-guide/linq-query-expressions/index.md)