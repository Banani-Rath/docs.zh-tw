---
title: "&lt;para&gt; (Visual Basic) | Microsoft Docs"
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
  - "<para> XML tag"
  - "para XML tag"
ms.assetid: a3a18b6c-6416-4358-94ec-37b22675fd37
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# &lt;para&gt; (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

指定已將內容格式化成段落。  
  
## 語法  
  
```  
<para>content</para>  
```  
  
#### 參數  
 `content`  
 為段落內的文字。  
  
## 備註  
 `<para>` 標記 \(Tag\) 適合在標記內使用，例如 [\<summary\>](../../../visual-basic/language-reference/xmldoc/summary.md)、[\<remarks\>](../../../visual-basic/language-reference/xmldoc/remarks.md) 或 [\<returns\>](../../../visual-basic/language-reference/xmldoc/returns.md)，並能讓您將結構加入至文字。  
  
 使用 [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md) 進行編譯，將文件註解處理為檔案。  
  
## 範例  
 這個範例會使用 `<para>` 標記，將 `UpdateRecord` 方法的註解區段分割成兩個段落。  
  
 [!CODE [VbVbcnXmlDocComments#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#6)]  
  
## 請參閱  
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)