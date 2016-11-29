---
title: "泛型方法 (C# 程式設計手冊) | Microsoft Docs"
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
  - "泛型 [C#], 方法"
ms.assetid: 673eeea2-4b48-4faa-9c4e-2e89449221b9
caps.latest.revision: 27
caps.handback.revision: 27
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 泛型方法 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

泛型方法是使用型別參數宣告的一種方法，如下所示：  
  
 [!CODE [csProgGuideGenerics#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#22)]  
  
 下列程式碼範例會示範使用 `int` 做為型別引數的來呼叫方法的一種方式：  
  
 [!CODE [csProgGuideGenerics#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#23)]  
  
 您也可以省略型別引數，編譯器將會自行推斷。  下面對 `Swap` 的呼叫相當於前述呼叫：  
  
 [!CODE [csProgGuideGenerics#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#24)]  
  
 相同的型別推斷規則也適用於靜態方法和執行個體方法。  編譯器能夠根據您所傳遞的方法引數來推斷型別參數，但不能單靠條件約束 \(Constraint\) 或傳回值推斷型別參數。  因此，型別推斷不適用於沒有參數的方法。  型別推斷是在編譯時期進行，即在編譯器嘗試解析多載方法簽章之前執行。  編譯器會對共用相同名稱的所有泛型方法套用型別推斷邏輯。  在多載解析步驟中，編譯器只會將型別推斷成功的泛型方法包括在內。  
  
 在泛型類別內，非泛型方法可以存取類別層級的型別參數，如下所示：  
  
 [!CODE [csProgGuideGenerics#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#25)]  
  
 如果您定義會採用相同型別參數做為包含類別的泛型方法，這時因為在方法範圍中，內部 `T` 的引數會隱藏提供給外部 `T` 的引數，而使得編譯器產生 CS0693 警告。  如果您需要以有別於類別具現化 \(Instantiated\) 時所提供的型別引數來呼叫泛型類別方法的彈性，請考慮為該方法之型別參數提供不同的識別項，如下列範例所示的 `GenericList2<T>`。  
  
 [!CODE [csProgGuideGenerics#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#26)]  
  
 您可以使用條件約束，對方法中的型別參數執行更多自訂操作。  這個版本的 `Swap<T>`，現在稱為 `SwapIfGreater<T>`，只能搭配實作 <xref:System.IComparable%601> 的型別引數使用。  
  
 [!CODE [csProgGuideGenerics#27](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#27)]  
  
 泛型方法可依多個型別參數來進行多載。  例如，下列方法都可以位於同一個類別中：  
  
 [!CODE [csProgGuideGenerics#28](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#28)]  
  
## C\# 語言規格  
 如需詳細資訊，請參閱 [C\# 語言規格](../../../csharp/language-reference/language-specification.md)。  
  
## 請參閱  
 <xref:System.Collections.Generic>   
 [C\# 程式設計手冊](../../../csharp/programming-guide/index.md)   
 [泛型簡介](../../../csharp/programming-guide/generics/introduction-to-generics.md)   
 [方法](../../../csharp/programming-guide/classes-and-structs/methods.md)