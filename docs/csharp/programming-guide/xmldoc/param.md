---
title: "&lt;param&gt; (C# 程式設計手冊) | Microsoft Docs"
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
  - "param"
  - "<param>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<param> C# XML 標記"
  - "param C# XML 標記"
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;param&gt; (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

## 語法  
  
```  
<param name="name">description</param>  
```  
  
#### 參數  
 `name`  
 為方法參數的名稱。  以雙引號 \(" "\) 將名稱括起來。  
  
 `description`  
 參數的描述。  
  
## 備註  
 \<param\> 標記應使用於方法宣告的註解中，以描述該方法其中之一的參數。  若要提供多個參數，請使用多個 \<param\> 標記。  
  
 \<param\> 標記的文字將會顯示在 IntelliSense、物件瀏覽器和程式碼結構 Web 報告中。  
  
 使用 [\/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 [!CODE [csProgGuideDocComments#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#1)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [建議使用的文件註解標籤](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)