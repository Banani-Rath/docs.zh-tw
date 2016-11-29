---
title: "如何：撰寫複製建構函式 (C# 程式設計手冊) | Microsoft Docs"
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
  - "C# 語言, 複製建構函式"
  - "複製建構函式 [C#]"
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：撰寫複製建構函式 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

C\# 不提供物件的複製建構函式，不過，您可以自行撰寫複製建構函式。  
  
## 範例  
 在下列範例中，`Person` [類別](../../../csharp/language-reference/keywords/class.md)會定義接受 `Person` 執行個體做為引數的複製建構函式。  引數的屬性值會指派給新的 `Person` 執行個體的屬性。  程式碼包含替代的複製建構函式，這會傳送您要複製到類別之執行個體建構函式的執行個體的 `Name` 和 `Age` 屬性。  
  
 [!CODE [csProgGuideObjects#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#16)]  
  
## 請參閱  
 <xref:System.ICloneable>   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [類別和結構](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [建構函式](../../../csharp/programming-guide/classes-and-structs/constructors.md)   
 [解構函式](../../../csharp/programming-guide/classes-and-structs/destructors.md)