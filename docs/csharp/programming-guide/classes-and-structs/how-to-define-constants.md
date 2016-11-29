---
title: "如何：在 C# 中定義常數 | Microsoft Docs"
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
  - "C# 語言, 常數"
  - "常數 [C#]"
ms.assetid: 43f511be-346c-4b8a-995e-aded94542ece
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：在 C# 中定義常數
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

常數是欄位，其值是在編譯時期設定並且絕對不能變更。  使用常數提供有意義的名稱，而不是特殊值的數字常值 \(「識別常數」\)。  
  
> [!NOTE]
>  在 C\# 中，[\#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) 前置處理器指示詞 \(Preprocessor Directive\) 無法用於以通常在 C 和 C\+\+ 使用的方式定義常數。  
  
 若要定義整數類資料型別 \(Integral Type\) \(`int`、`byte` 等等\) 的常數值，請使用列舉型別。  如需詳細資訊，請參閱 [enum](../../../csharp/language-reference/keywords/enum.md)。  
  
 若要定義非整數常數，其中一個方法是將常數群組在名為 `Constants` 的單一靜態類別中。  這需要所有常數的參考前面都加上類別名稱，如下列範例所示。  
  
## 範例  
 [!CODE [csProgGuideObjects#89](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#89)]  
  
 使用類別名稱限定詞可以協助確保您和其他使用常數的人都了解它是常數且不能修改。  
  
## 請參閱  
 [類別和結構](../../../csharp/programming-guide/classes-and-structs/index.md)