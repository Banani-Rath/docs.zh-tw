---
title: "unsafe (C# 參考) | Microsoft Docs"
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
  - "unsafe_CSharpKeyword"
  - "unsafe"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "unsafe 關鍵字 [C#]"
ms.assetid: 7e818009-1c6e-4b9e-b769-3728a01586a0
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# unsafe (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`unsafe` 關鍵字代表不安全的內容，在任何和指標相關作業中都必須有這個關鍵字。  如需詳細資訊，請參閱 [Unsafe 程式碼和指標](../../../csharp/programming-guide/unsafe-code-pointers/index.md)。  
  
 您可以在型別或成員的宣告中使用 `unsafe` 修飾詞。  如此一來，型別或成員的整個文字範圍 \(Textual Extent\) 就會被視為不安全的內容。  例如，下列為使用 `unsafe` 修飾詞來宣告的方法：  
  
```  
  
      unsafe static void FastCopy(byte[] src, byte[] dst, int count)  
{  
    // Unsafe context: can use pointers here.  
}  
```  
  
 不安全的內容其範圍可以由參數名單延伸到方法的結尾，那麼指標也就可以用於參數名單：  
  
```  
  
unsafe static void FastCopy ( byte* ps, byte* pd, int count ) {...}  
```  
  
 您也可以使用不安全的區塊，啟用這個區塊中 Unsafe 程式碼。  例如：  
  
```  
  
      unsafe  
{  
    // Unsafe context: can use pointers here.  
}  
```  
  
 要編譯 Unsafe 程式碼，您必須指定 [\/unsafe](../../../csharp/language-reference/compiler-options/unsafe-compiler-option.md) 編譯器選項。  Unsafe 程式碼不能由 Common Language Runtime 來驗證。  
  
## 範例  
 [!CODE [csrefKeywordsModifiers#22](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#22)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [fixed 陳述式](../../../csharp/language-reference/keywords/fixed-statement.md)   
 [Unsafe 程式碼和指標](../../../csharp/programming-guide/unsafe-code-pointers/index.md)   
 [固定大小的緩衝區](../../../csharp/programming-guide/unsafe-code-pointers/fixed-size-buffers.md)