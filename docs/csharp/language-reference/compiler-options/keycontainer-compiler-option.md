---
title: "/keycontainer (C# Compiler Options) | Microsoft Docs"
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
  - "/keycontainer"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "/keycontainer compiler option [C#]"
  - "keycontainer compiler option [C#]"
  - "-keycontainer compiler option [C#]"
ms.assetid: b3982b6d-2382-4f7e-bebd-ce98eaa30763
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# /keycontainer (C# Compiler Options)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

指定密碼編譯金鑰容器的名稱。  
  
## 語法  
  
```  
/keycontainer:string  
```  
  
## Arguments  
 `string`  
 強式名稱金鑰容器的名稱。  
  
## 備註  
 使用 **\/keycontainer** 選項時，編譯器會將指定容器內的公開金鑰放入組件資訊清單內，並用私密金鑰為最終的組件簽署，建立出共用元件。  若要產生金鑰檔，請在命令列上輸入 sn \-k `file` 。輸入sn \-i 會將金鑰組安裝至容器。  
  
 如果您用 [\/target:module](../../../csharp/language-reference/compiler-options/target-module-compiler-option.md) 進行編譯，金鑰檔案的名稱就會放在模組內，當您使用 [\/addmodule](../../../csharp/language-reference/compiler-options/addmodule-compiler-option.md) 將模組編譯到組件內時才放入組件。  
  
 您也可以為任何 Microsoft Intermediate Language \(MSIL\) 模組，指定這個選項當做原始程式碼中的自訂屬性 \(<xref:System.Reflection.AssemblyKeyNameAttribute?displayProperty=fullName>\)。  
  
 您還可以使用 [\/keyfile](../../../csharp/language-reference/compiler-options/keyfile-compiler-option.md) 將加密資訊傳遞至編譯器。  如果您要將公開金鑰加入至組件資訊清單，但仍要組件經過測試後才簽署，請使用 [\/delaysign](../../../csharp/language-reference/compiler-options/delaysign-compiler-option.md)。  
  
 如需詳細資訊，請參閱[建立和使用強式名稱的組件](../Topic/Creating%20and%20Using%20Strong-Named%20Assemblies.md)以及[延遲簽署組件](../Topic/Delay%20Signing%20an%20Assembly.md)。  
  
### 在 Visual Studio 開發環境中設定這個編譯器選項  
  
1.  Visual Studio 開發環境中沒有這個編譯器選項。  
  
 您可以使用 <xref:VSLangProj.ProjectProperties.AssemblyKeyContainerName%2A>，以程式設計方式存取這個編譯器選項。  
  
## 請參閱  
 [C\# Compiler Options](../../../csharp/language-reference/compiler-options/index.md)   
 [如何：修改專案屬性和組態設定](http://msdn.microsoft.com/zh-tw/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)