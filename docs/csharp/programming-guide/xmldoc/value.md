---
title: "&lt;value&gt; (C# 程式設計手冊) | Microsoft Docs"
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
  - "<value>"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "<value> C# XML 標記"
  - "value C# XML 標記"
ms.assetid: 08dbadaf-9ab6-43d9-9493-98e43bed199a
caps.latest.revision: 12
caps.handback.revision: 12
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;value&gt; (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

## 語法  
  
```  
<value>property-description</value>  
```  
  
#### 參數  
 `property-description`  
 屬性的描述。  
  
## 備註  
 \<value\> 標記讓您描述屬性代表的值。  請注意，當您透過 Visual Studio .NET 開發環境的程式碼精靈加入一個屬性時，該新屬性將會加上一個 [\<summary\>](../../../csharp/programming-guide/xmldoc/summary.md) 標記。  接著，您應該手動加入一個 \<value\> 標記，來說明該屬性表示的值。  
  
 使用 [\/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 [!CODE [csProgGuideDocComments#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#14)]  
  
## 請參閱  
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [建議使用的文件註解標籤](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)