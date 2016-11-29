---
title: "&lt;example&gt; (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "example XML tag"
  - "<example> XML tag"
ms.assetid: 90eeda1c-3fc4-427c-879c-5046d265a97c
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;example&gt; (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

指定成員的範例。  
  
## 語法  
  
```  
<example>description</example>  
```  
  
#### 參數  
 `description`  
 為程式碼範例的描述。  
  
## 備註  
 `<example>` 標記 \(Tag\) 讓您指定一個範例，說明如何使用方法或其他程式庫成員。  這通常會包含 [\<code\>](../../../visual-basic/language-reference/xmldoc/code.md) 標記的使用。  
  
 使用 [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 這個範例會使用 `<example>` 標記，來包含使用 `ID` 欄位的範例。  
  
 [!CODE [VbVbcnXmlDocComments#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#2)]  
  
## 請參閱  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)