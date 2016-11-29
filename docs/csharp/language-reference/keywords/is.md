---
title: "is (C# 參考) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "is_CSharpKeyword"
  - "is"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "is 關鍵字 [C#]"
ms.assetid: bc62316a-d41f-4f90-8300-c6f4f0556e43
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# is (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

檢查物件是否與指定的型別相容。  例如，下列程式碼可以判斷某個物件是否為 `MyObject` 型別 \(或衍生自 `MyObject` 的型別\) 的執行個體：  
  
```  
if (obj is MyObject)  
{  
}  
```  
  
 如果提供的運算式不可為 Null，且提供的物件可在未造成擲回例外狀況之下，將型別轉換成提供的型別，`is` 運算式就會評估為 `true`。  
  
 若運算式已知永遠為 `true` 或永遠為 `false`，`is` 關鍵字就會產生編譯時期警告，但通常會在執行階段評估型別相容性。  
  
 `is` 運算子無法多載。  
  
 請注意，`is` 運算子只會考慮參考轉換、boxing 轉換和 unboxing 轉換三種方式。  而不會考慮使用其他轉換方式，例如使用者定義轉換。  
  
 `is` 運算子的左邊不允許使用匿名方法 \(Anonymous Method\)。  這個例外狀況包括 Lambda 運算式。  
  
## 範例  
 [!CODE [csrefKeywordsOperator#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#4)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [typeof](../../../csharp/language-reference/keywords/typeof.md)   
 [as](../../../csharp/language-reference/keywords/as.md)   
 [運算子關鍵字](../../../csharp/language-reference/keywords/operator-keywords.md)