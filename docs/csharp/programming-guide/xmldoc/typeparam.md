---
title: "&lt;typeparam&gt; (C# 程式設計手冊) | Microsoft Docs"
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
  - "typeparam"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<typeparam> C# XML 標記"
  - "typeparam C# XML 標記"
ms.assetid: 9b99d400-e911-4e55-99c6-64367c96aa4f
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;typeparam&gt; (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

## 語法  
  
```  
<typeparam name="name">description</typeparam>  
```  
  
#### 參數  
 `name`  
 型別參數的名稱。  以雙引號 \(" "\) 將名稱括起來。  
  
 `description`  
 型別參數的說明。  
  
## 備註  
 `<typeparam>` 標記應該用在泛型型別或方法宣告的註解中，以說明型別參數。  為泛型型別或方法的每個型別參數加入標記。  
  
 如需詳細資訊，請參閱 [泛型](../../../csharp/programming-guide/generics/index.md)。  
  
 `<typeparam>` 標記的文字會顯示在 IntelliSense \([Object Browser Window](http://msdn.microsoft.com/zh-tw/3c7f1673-1f0d-41b1-94ca-a3dcfcb82cda)程式碼結構 Web 報告\) 中。  
  
 使用 [\/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 [!CODE [csProgGuideDocComments#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#13)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [建議使用的文件註解標籤](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)