---
title: "&lt;c&gt; (Visual Basic) | Microsoft Docs"
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
  - "c XML tag"
  - "<c> XML tag"
ms.assetid: 36ad5d1b-11f7-4012-8932-41962ac327d1
caps.latest.revision: 11
caps.handback.revision: 11
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;c&gt; (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

表示描述內的文字是程式碼。  
  
## 語法  
  
```  
<c>text</c>  
```  
  
#### 參數  
  
|||  
|-|-|  
|參數|描述|  
|`text`|您要指定為程式碼的文字。|  
  
## 備註  
 `<c>` 標記讓您可以指出描述內的文字應該標記為程式碼。  使用 [\<code\>](../../../visual-basic/language-reference/xmldoc/code.md) 來表示要做為程式碼的多行。  
  
 使用 [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 這個範例在摘要區段中使用 `<c>` 標記，表示 `Counter` 是程式碼。  
  
 [!CODE [VbVbcnXmlDocComments#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#1)]  
  
## 請參閱  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)