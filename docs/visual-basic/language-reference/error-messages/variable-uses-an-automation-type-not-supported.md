---
title: "Variable uses an Automation type not supported in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbrID458"
dev_langs: 
  - "VB"
ms.assetid: bde4f4da-493b-452c-b6e4-1d370edba4cd
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Variable uses an Automation type not supported in Visual Basic
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

您嘗試使用在型別程式庫或物件程式庫 \(具有 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 不支援的資料型別\) 中定義的變數。  
  
### 若要更正這個錯誤  
  
-   使用 [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] 可辨識之型別的變數。  
  
     \-或\-  
  
-   當使用 `FileGet` 或 `FileGetOBject` 時，如果發生這個錯誤，請確定是利用 `FilePut` 或 `FilePutObject` 寫入您所嘗試使用的檔案。  
  
## 請參閱  
 [Data Types](../../../visual-basic/language-reference/data-types/data-type-summary.md)