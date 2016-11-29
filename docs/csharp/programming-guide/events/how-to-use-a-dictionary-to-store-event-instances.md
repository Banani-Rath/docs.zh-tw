---
title: "如何：使用字典儲存事件執行個體 (C# 程式設計手冊) | Microsoft Docs"
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
  - "事件 [C#], 在字典中儲存執行個體"
ms.assetid: 9512c64d-5aaf-40cd-b941-ca2a592f0064
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：使用字典儲存事件執行個體 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`accessor-declarations` 的用法之一是公開大量的事件但不配置每個事件的欄位，而是改用字典來儲存事件執行個體。  不過，這只在您擁有大量的事件，但預期大多數事件都不會實作的情況下才有用。  
  
## 範例  
 [!CODE [csProgGuideEvents#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEvents#9)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [事件](../../../csharp/programming-guide/events/index.md)   
 [委派](../../../csharp/programming-guide/delegates/index.md)