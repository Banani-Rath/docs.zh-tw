---
title: "&lt;example&gt; (C# 程式設計手冊) | Microsoft Docs"
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
  - "<example>"
  - "example"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<example> C# XML 標記"
  - "C# XML 標記範例"
ms.assetid: 32d6e73b-2554-4abb-83ee-a1e321334fd2
caps.latest.revision: 13
caps.handback.revision: 13
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;example&gt; (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

## 語法  
  
```  
<example>description</example>  
```  
  
#### 參數  
 `description`  
 為程式碼範例的描述。  
  
## 備註  
 \<example\> 標記讓您指定一個範例，說明如何使用方法或其他程式庫成員。  這通常會包含使用 [\<code\>](../../../csharp/programming-guide/xmldoc/code.md) 標記。  
  
 使用 [\/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 [!CODE [csProgGuideDocComments#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#3)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [建議使用的文件註解標籤](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)