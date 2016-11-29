---
title: "如何：在十六進位字串和數字類型間轉換 (C# 程式設計手冊) | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "轉換 [C#], 十六進位字串"
  - "十六進位字串 [C#]"
  - "十六進位字串 [C#], 轉換為數字類型"
  - "字串 [C#], 轉換十六進位字串"
ms.assetid: 7115c49f-7d1d-40c3-8bd9-aae0cc1d46b6
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：在十六進位字串和數字類型間轉換 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

本主題中的範例會示範如何執行下列工作：  
  
-   取得 [string](../../../csharp/language-reference/keywords/string.md) 中每個字元的十六進位值。  
  
-   取得對應至十六進位 string 中每個值的 [char](../../../csharp/language-reference/keywords/char.md)。  
  
-   將十六進位 `string` 轉換為 [int](../../../csharp/language-reference/keywords/int.md)。  
  
-   將十六進位 `string` 轉換為 [float](../../../csharp/language-reference/keywords/float.md)。  
  
-   將 [byte](../../../csharp/language-reference/keywords/byte.md) 陣列轉換為十六進位 `string`。  
  
## 範例  
 這個範例會輸出 `string` 中每個字元的十六進位值。  首先，會將 `string` 剖析至字元陣列。  然後，會呼叫每個字元上的 <xref:System.Convert.ToInt32%28System.Char%29> 取得其數值。  最後，它會在 `string` 中將數字格式化為十六進位表示。  
  
 [!CODE [csProgGuideTypes#30](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#30)]  
  
## 範例  
 這個範例會剖析十六進位值的 `string`，並輸出對應至每個十六進位值的字元。  首先，呼叫 [Split\(Char\[\]\)](assetId:///M:System.String.Split(System.Char[])?qualifyHint=False&autoUpgrade=False) 方法取得每個十六進位值，做為陣列中的個別 `string`。  然後呼叫 <xref:System.Convert.ToInt32%28System.String%2CSystem.Int32%29>，將十六進位值轉換為以 [int](../../../csharp/language-reference/keywords/int.md) 表示的十進位值。  會顯示兩種不同的方法，以取得對應至該字元程式碼的字元。  第一個技術會使用 <xref:System.Char.ConvertFromUtf32%28System.Int32%29>，傳回對應至整數引數的字元做為 `string`。  第二個技術會明確將 `int` 轉型為 [char](../../../csharp/language-reference/keywords/char.md)。  
  
 [!CODE [csProgGuideTypes#31](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#31)]  
  
## 範例  
 這個範例會示範另一個方法，經由呼叫 <xref:System.Int32.Parse%28System.String%2CSystem.Globalization.NumberStyles%29> 方法，將十六進位 `string` 轉換為整數。  
  
 [!CODE [csProgGuideTypes#32](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#32)]  
  
## 範例  
 下列範例會示範如何使用 <xref:System.BitConverter?displayProperty=fullName> 類別和 <xref:System.Int32.Parse%2A?displayProperty=fullName> 方法，將十六進位 `string` 轉換為[float](../../../csharp/language-reference/keywords/float.md)。  
  
 [!CODE [csProgGuideTypes#39](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#39)]  
  
## 範例  
 下列範例會示範如何使用 <xref:System.BitConverter?displayProperty=fullName> 類別，將 [byte](../../../csharp/language-reference/keywords/byte.md) 陣列轉換為十六進位字串。  
  
 [!CODE [csProgGuideTypes#38](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#38)]  
  
## 請參閱  
 [標準數值格式字串](../Topic/Standard%20Numeric%20Format%20Strings.md)   
 [類型](../../../csharp/programming-guide/types/index.md)   
 [如何：判斷字串是否表示數值](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)