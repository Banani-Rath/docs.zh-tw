---
title: "const (C# 參考) | Microsoft Docs"
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
  - "const_CSharpKeyword"
  - "const"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "const 關鍵字 [C#]"
ms.assetid: 79eb447c-117b-4418-933f-97c50aa472db
caps.latest.revision: 28
caps.handback.revision: 28
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# const (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

您可以使用 `const` 關鍵字來宣告常數欄位或區域常數。  常數欄位和區域常數不是變數，可能無法修改。  常數可以是數值、布林值、字串或 null 參考。  請勿建立用來表示想隨時變更之資訊的常數。  例如，請勿使用常數欄位來儲存服務的價格、產品版本號碼或公司的品牌名稱。  這些值可能會隨時間變更；此外，由於編譯器會傳播常數，以您的程式庫編譯的其他程式碼必須經過重新編譯，才能看到變更。  另請參閱 [readonly](../../../csharp/language-reference/keywords/readonly.md) 關鍵字。  例如：  
  
```  
  
      const int x = 0;  
public const double gravitationalConstant = 6.673e-11;  
private const string productName = "Visual C#";  
```  
  
## 備註  
 常數宣告的類型指定宣告引入的成員類型。  區域常數或常數欄位的初始設定式必須是可明確轉換成目標類型的常數運算式。  
  
 常數運算式是可在編譯時期完整評估的運算式。  因此，參考類型之常數唯一可能的值為 `string` 和 null 參考。  
  
 常數宣告可以宣告多個常數，例如：  
  
```  
public const double x = 1.0, y = 2.0, z = 3.0;  
```  
  
 常數宣告中不允許使用 `static` 修飾詞。  
  
 常數可以參與常數運算式，如下所示：  
  
```  
public const int c1 = 5;  
public const int c2 = c1 + 100;  
```  
  
> [!NOTE]
>  [readonly](../../../csharp/language-reference/keywords/readonly.md) 關鍵字與 `const` 關鍵字不同。  `const` 欄位只能在欄位的宣告中初始化。  `readonly` 欄位可在宣告或建構函式中初始化。  因此，`readonly` 欄位可能會因使用的建構函式而有不同的值。  此外，雖然 `const` 欄位是編譯時期常數，但 `readonly` 欄位可用於執行階段常數，如下列程式碼所示：`public static readonly uint l1 = (uint)DateTime.Now.Ticks;`  
  
## 範例  
 [!CODE [csrefKeywordsModifiers#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#5)]  
  
## 範例  
 這個範例示範如何將常數當做區域變數來使用。  
  
 [!CODE [csrefKeywordsModifiers#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#6)]  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [修飾詞](../../../csharp/language-reference/keywords/modifiers.md)   
 [readonly](../../../csharp/language-reference/keywords/readonly.md)