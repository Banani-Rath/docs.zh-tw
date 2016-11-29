---
title: "/imports (Visual Basic) | Microsoft Docs"
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
  - "/imports compiler option [Visual Basic]"
  - "imports compiler option [Visual Basic]"
  - "-imports compiler option [Visual Basic]"
ms.assetid: 9a93fb53-c080-497b-bf9b-441022dbbc39
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# /imports (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

從指定的組件 \(Assembly\) 匯入命名空間。  
  
## 語法  
  
```  
/imports:namespaceList  
```  
  
## 引數  
  
|||  
|-|-|  
|詞彙|定義|  
|`namespaceList`|必要項。  要匯入之以逗號分隔的命名空間清單。|  
  
## 備註  
 `/imports` 選項會匯入在目前原始程式檔集合或是從任何參考組件中定義的命名空間。  
  
 以 `/imports` 指定的命名空間成員在編譯的所有原始程式碼檔中都可以使用。  請使用 [Imports Statement \(.NET Namespace and Type\)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)，以使用單一原始程式碼檔內的命名空間。  
  
||  
|-|  
|若要在 Visual Studio 整合式開發環境中設定 \/imports|  
|1.  在 \[**方案總管**\] 中選取專案。  在 \[**專案**\] 功能表上，按一下 \[**屬性**\]。  如需詳細資訊，請參閱[Introduction to the Project Designer](http://msdn.microsoft.com/zh-tw/898dd854-c98d-430c-ba1b-a913ce3c73d7)。<br />2.  按一下 \[**參考**\] 索引標籤。<br />3.  在 \[**加入使用者匯入**\] 按鈕旁的方塊中輸入命名空間名稱。<br />4.  按一下 \[**加入使用者匯入**\] 按鈕。|  
  
## 範例  
 指定 `/imports:system` 時會編譯下列程式碼。  
  
 [!CODE [VbVbalrCompiler#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#21)]  
  
## 請參閱  
 [Visual Basic Command\-Line Compiler](../../../visual-basic/reference/command-line-compiler/index.md)   
 [References and the Imports Statement](../../../visual-basic/programming-guide/program-structure/references-and-the-imports-statement.md)   
 [編譯命令列範例](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)