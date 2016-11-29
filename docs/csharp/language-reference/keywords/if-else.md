---
title: "if-else (C# 參考) | Microsoft Docs"
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
  - "if_CSharpKeyword"
  - "else"
  - "else_CSharpKeyword"
  - "if"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "else 關鍵字 [C#]"
  - "if 關鍵字 [C#]"
ms.assetid: d9a1d562-8cf5-4bd4-9ba7-8ad970cd25b2
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# if-else (C# 參考)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

`if` 陳述式會根據運算式的 `Boolean` 值識別要執行的陳述式。 在下列範例中，`Boolean` 變數 `result` 設為 `true`，然後以 `if` 陳述式進行檢查。 輸出為 `The condition is true`。  
  
 [!CODE [csrefKeywordsSelection#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#1)]  
  
 您也可以將本主題中的範例放在主控台 App 的 `Main` 方法執行。  
  
 如下列範例所示，`if` 陳述式在 C\# 中可能有兩種形式。  
  
```c#  
  
// if-else statement if (condition) { then-statement; } else { else-statement; } // Next statement in the program. // if statement without an else if (condition) { then-statement; } // Next statement in the program.  
```  
  
 在 `if-else` 陳述式中，如果 `condition` 評估為 true，則執行 `then-statement`。 如果 `condition` 為 false，則執行 `else-statement`。 由於 `condition` 無法同時為 true 和 false，所以 `if-else` 陳述式的 `then-statement` 和 `else-statement` 永遠無法同時執行。 在執行 `then-statement` 或 `else-statement` 後，控制權會轉移到在 `if` 陳述式之後的下一個陳述式。  
  
 在不包含 `else` 陳述式的 `if` 陳述式，如果 `condition` 為 true，則執行 `then-statement`。 如果 `condition` 為 false，控制權會轉移到在 `if` 陳述式之後的下一個陳述式。  
  
 `then-statement` 和 `else-statement` 皆可包含以大括弧括住 \(`{}`\) 的單一陳述式或多個陳述式。 對於單一陳述式，大括弧是選擇項，但建議使用。  
  
 在 `then-statement` 和 `else-statement` 的陳述式可以是任何類型，包括其他在原始 `if` 陳述式內巢狀的 `if` 陳述式。 在巢狀 `if` 陳述式，每個 `else` 子句都隸屬於最後一個沒有相對應 `else` 的 `if`。 在下列範例中，如果 `Result1` 和 `m > 10` 都評估為 true，則會顯示 `n > 20`。 如果 `m > 10` 為 true，但 `n > 20` 是 false，則會顯示 `Result2`。  
  
 [!CODE [csrefKeywordsSelection#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#2)]  
  
 如果相反地，您希望 `Result2` 在 `(m > 10)` 為 false 時顯示，則可以使用大括弧指定關聯，以建立巢狀 `if` 陳述式的開頭和結尾，如下列範例所示。  
  
 [!CODE [csrefKeywordsSelection#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#3)]  
  
 如果條件 `(m > 10)` 評估為 false，就會顯示 `Result2`。  
  
## 範例  
 在下列範例中，將由鍵盤輸入字元，而程式會使用巢狀 `if` 陳述式判斷輸入字元是否為字母字元。 如果輸入字元是字母字元，程式就會檢查輸入的字元是大寫或小寫， 並顯示每一種情況的訊息。  
  
 [!CODE [csrefKeywordsSelection#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#4)]  
  
## 範例  
 如下列程式碼片段所示，您也可以巢狀方式將 `if` 陳述式置於其他區塊內。 此範例將 `if` 以巢狀方式置於兩個 else 區塊和一個 then 區塊內部。 在每個區塊中，註解指定哪些條件為 true 或 false。  
  
 [!CODE [csrefKeywordsSelection#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#5)]  
  
## 範例  
 下列範例會判斷輸入字元是否為小寫字母、大寫字母或數字。 如果這三個條件為 false，字元不是英數字元。 這個範例會顯示每一種情況的訊息。  
  
 [!CODE [csrefKeywordsSelection#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsSelection#6)]  
  
 就像在 else 區塊或 then 區塊中的陳述式可以是任何有效的陳述式一樣，您可以為這個條件使用任何有效的布林運算式。 您可以使用邏輯運算子，例如 [&&](../../../csharp/language-reference/operators/conditional-and-operator.md)、[&](../../../csharp/language-reference/operators/and-operator.md)、[&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md)、[&#124;](../../../csharp/language-reference/operators/or-operator.md) 和 [\!](../../../csharp/language-reference/operators/logical-negation-operator.md)，並撰寫複雜的條件。 下列程式碼顯示範例。  
  
```c#  
// NOT bool result = true; if (!result) { Console.WriteLine("The condition is true (result is false)."); } else { Console.WriteLine("The condition is false (result is true)."); } // Short-circuit AND int m = 9; int n = 7; int p = 5; if (m >= n && m >= p) { Console.WriteLine("Nothing is larger than m."); } // AND and NOT if (m >= n && !(p > m)) { Console.WriteLine("Nothing is larger than m."); } // Short-circuit OR if (m > n || m > p) { Console.WriteLine("m isn't the smallest."); } // NOT and OR m = 4; if (!(m >= n || m >= p)) { Console.WriteLine("Now m is the smallest."); } // Output: // The condition is false (result is true). // Nothing is larger than m. // Nothing is larger than m. // m isn't the smallest. // Now m is the smallest.  
```  
  
## C\# 語言規格  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## 請參閱  
 [C\# 參考](../../../csharp/language-reference/index.md)   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [C\# 關鍵字](../../../csharp/language-reference/keywords/index.md)   
 [?: 運算子](../../../csharp/language-reference/operators/conditional-operator.md)   
 [if\-else 陳述式 \(C\+\+\)](/visual-cpp/cpp/if-else-statement-cpp)   
 [switch](../../../csharp/language-reference/keywords/switch.md)