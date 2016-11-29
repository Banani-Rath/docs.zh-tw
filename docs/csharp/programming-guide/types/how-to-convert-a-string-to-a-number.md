---
title: "如何：將字串轉換為數值 (C# 程式設計手冊) | Microsoft Docs"
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
  - "轉換 [C#]"
  - "轉換 [C#], 字串為 int"
  - "將字串轉換為 int [C#]"
  - "字串 [C#], 轉換為 int"
ms.assetid: 467b9979-86ee-4afd-b734-30299cda91e3
caps.latest.revision: 34
caps.handback.revision: 34
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：將字串轉換為數值 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

您可以使用 <xref:System.Convert> 類別中的方法，或是使用各種數值類型 \(int、long、float 等等\) 上找到的 `TryParse` 方法，將[字串](../../../csharp/language-reference/keywords/string.md)轉換成數字。  
  
 如果您有一個字串，則呼叫 `TryParse` 方法會稍微更有效率且直接 \(例如，`int.TryParse(“11”)`\)。  使用 `Convert` 方法比實作 <xref:System.IConvertible> 的一般物件更有用。  
  
 您可以在預期字串包含的數值類型上使用 `Parse` 或 `TryParse` 方法，例如 <xref:System.Int32?displayProperty=fullName> 類型。  <xref:System.Convert.ToUInt32%2A?displayProperty=fullName> 方法會在內部使用 <xref:System.Int32.Parse%2A>。  如果字串的格式無效，`Parse` 會擲回例外狀況，而 `TryParse` 會傳回 [false](../../../csharp/language-reference/keywords/false.md)。  
  
## 範例  
 `Parse` 和 `TryParse` 方法會忽略字串開頭和結尾的空格，但所有其他字元必須是來自適當數值類型的字元 \(int、long、ulong、float、decimal 等等\)。  若構成數字的字元內有任何空格，則會造成錯誤。  例如，您可以使用 `decimal.TryParse` 剖析 "10"、"10.3"、"  10  "，但無法使用這個方法來剖析來自 “10X”、“1 0” \(請注意空格\)、"10  3" \(請注意空格\)、"10e1" \(`float.TryParse` 在這裡運作\) 的 10，依此類推。  
  
 下列範例會示範 `Parse` 和 `TryParse` 成功與不成功的呼叫。  
  
 [!CODE [csProgGuideTypes#5555](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#5555)]  
[!CODE [csProgGuideTypes#25](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#25)]  
[!CODE [csProgGuideTypes#26](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#26)]  
[!CODE [csProgGuideTypes#27](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#27)]  
[!CODE [csProgGuideTypes#28](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#28)]  
[!CODE [csProgGuideTypes#100](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#100)]  
  
## 範例  
 下表列出您可以使用的 <xref:System.Convert> 類別的一些方法。  
  
|數字類型|方法|  
|----------|--------|  
|`decimal`|<xref:System.Convert.ToDecimal%28System.String%29>|  
|`float`|<xref:System.Convert.ToSingle%28System.String%29>|  
|`double`|<xref:System.Convert.ToDouble%28System.String%29>|  
|`short`|<xref:System.Convert.ToInt16%28System.String%29>|  
|`int`|<xref:System.Convert.ToInt32%28System.String%29>|  
|`long`|<xref:System.Convert.ToInt64%28System.String%29>|  
|`ushort`|<xref:System.Convert.ToUInt16%28System.String%29>|  
|`uint`|<xref:System.Convert.ToUInt32%28System.String%29>|  
|`ulong`|<xref:System.Convert.ToUInt64%28System.String%29>|  
  
 這個範例會呼叫 <xref:System.Convert.ToInt32%28System.String%29?displayProperty=fullName> 方法，將輸入由 [string](../../../csharp/language-reference/keywords/string.md) 轉換為 [int](../../../csharp/language-reference/keywords/int.md)。  程式碼會攔截由這個方法擲回之兩種最常見的例外狀況，分別是 <xref:System.FormatException> 和 <xref:System.OverflowException>。  如果數字可以遞增而不會造成整數儲存位置溢位，那麼程式會將結果增加 1 並列印輸出。  
  
 [!CODE [csProgGuideTypes#5555](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#5555)]  
[!CODE [csProgGuideTypes#24](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#24)]  
  
## 請參閱  
 [類型](../../../csharp/programming-guide/types/index.md)   
 [如何：判斷字串是否表示數值](../../../csharp/programming-guide/strings/how-to-determine-whether-a-string-represents-a-numeric-value.md)   
 [.NET Framework 4 格式化公用程式](http://code.msdn.microsoft.com/NET-Framework-4-Formatting-9c4dae8d)