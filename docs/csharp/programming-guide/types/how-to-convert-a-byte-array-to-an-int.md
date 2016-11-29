---
title: "如何：將位元組陣列轉換成整數 (C# 程式設計手冊) | Microsoft Docs"
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
  - "位元組陣列 [C#], 轉換為 int"
  - "轉換 [C#], 位元組陣列轉換為 int"
ms.assetid: d6ac20e2-448e-4aea-99b9-faf04c6f1e79
caps.latest.revision: 18
caps.handback.revision: 18
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：將位元組陣列轉換成整數 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

這個範例會示範如何使用 <xref:System.BitConverter> 類別，將位元組陣列轉換為 [int](../../../csharp/language-reference/keywords/int.md)，並轉換回位元組陣列。  例如，您讀取了網路上的位元組之後，您可能需要將位元組轉換為內建資料型別。  除了範例中的 [ToInt32\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToInt32(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False) 方法以外，下表會列出 <xref:System.BitConverter> 類別中的方法，這些方法會將位元組 \(從位元組陣列\) 轉換為內建型別。  
  
|傳回的型別|方法|  
|-----------|--------|  
|`bool`|[ToBoolean\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToBoolean(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`char`|[ToChar\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToChar(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`double`|[ToDouble\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToDouble(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`short`|[ToInt16\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToInt16(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`int`|[ToInt32\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToInt32(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`long`|[ToInt64\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToInt64(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`float`|[ToSingle\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToSingle(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`ushort`|[ToUInt16\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToUInt16(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`uint`|[ToUInt32\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToUInt32(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
|`ulong`|[ToUInt64\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToUInt64(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False)|  
  
## 範例  
 這個範例會初始化位元組陣列，若電腦架構是位元組由小到大 \(也就是說，先儲存較不重要的位元組\) 時將陣列反向，然後呼叫 [ToInt32\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToInt32(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False) 方法，將陣列中的四個位元組轉換為 `int`。  [ToInt32\(Byte\[\], Int32\)](assetId:///M:System.BitConverter.ToInt32(System.Byte[],System.Int32)?qualifyHint=False&autoUpgrade=False) 的第二個引數會指定位元組陣列的起始索引。  
  
> [!NOTE]
>  輸出可能會因電腦架構的位元組順序而有所不同。  
  
 [!CODE [csProgGuideTypes#22](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#22)]  
  
## 範例  
 在這個範例中，會呼叫 <xref:System.BitConverter> 類別的 <xref:System.BitConverter.GetBytes%28System.Int32%29> 方法，將 `int` 轉換為位元組陣列。  
  
> [!NOTE]
>  輸出可能會因電腦架構的位元組順序而有所不同。  
  
 [!CODE [csProgGuideTypes#23](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#23)]  
  
## 請參閱  
 <xref:System.BitConverter>   
 <xref:System.BitConverter.IsLittleEndian>   
 [類型](../../../csharp/programming-guide/types/index.md)