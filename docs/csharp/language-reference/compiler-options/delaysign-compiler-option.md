---
title: "/delaysign (C# Compiler Options) | Microsoft Docs"
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
  - "/delaysign"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "-delaysign compiler option [C#]"
  - "delaysign compiler option [C#]"
  - "/delaysign compiler option [C#]"
ms.assetid: bcb058eb-2933-4e7f-b356-5c941db4de75
caps.latest.revision: 16
caps.handback.revision: 16
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# /delaysign (C# Compiler Options)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

這個選項會使得編譯器在輸出檔案中保留空間，以便稍後可以加入數位簽章。  
  
## 語法  
  
```  
/delaysign[ + | - ]  
```  
  
## 引數  
 `+` &#124; `-`  
 如果要完整簽名的組件，請使用 **\/delaysign\-**。  如果您只要將公開金鑰放入組件內，請使用 **\/delaysign\+**。  預設值為 **\/delaysign\-**。  
  
## 備註  
 除非 **\/delaysign** 選項是和 [\/keyfile](../../../csharp/language-reference/compiler-options/keyfile-compiler-option.md) 或 [\/keycontainer](../../../csharp/language-reference/compiler-options/keycontainer-compiler-option.md) 一起使用，否則沒有任何效果。  
  
 當您要求完整簽署的組件時，編譯器會雜湊包含資訊清單 \(組件中繼資料\) 的檔案，並且利用私密金鑰簽署該項雜湊。  所產生的數位簽章儲存在包含資訊清單的檔案中。  當延遲簽署組件時，編譯器不會去計算和儲存簽章，但會保留檔案中的空間，以便稍後再加入簽章。  
  
 例如，使用 **\/delaysign\+** 可讓測試器將組件置於全域快取區中。  測試過後，您就可以使用[組件連結器](../Topic/Al.exe%20\(Assembly%20Linker\).md)公用程式，將私密金鑰放在組件內，以完整地簽署組件。  
  
 如需詳細資訊，請參閱[建立和使用強式名稱的組件](../Topic/Creating%20and%20Using%20Strong-Named%20Assemblies.md)以及[延遲簽署組件](../Topic/Delay%20Signing%20an%20Assembly.md)。  
  
### 在 Visual Studio 開發環境中設定這個編譯器選項  
  
1.  開啟專案的 \[**屬性**\] 頁面。  
  
2.  修改 \[**僅延遲簽署**\] 屬性。  
  
 如需如何以程式設計方式設定這個編譯器選項的詳細資訊，請參閱 <xref:VSLangProj80.ProjectProperties3.DelaySign%2A>。  
  
## 請參閱  
 [C\# Compiler Options](../../../csharp/language-reference/compiler-options/index.md)   
 [如何：修改專案屬性和組態設定](http://msdn.microsoft.com/zh-tw/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)