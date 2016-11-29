---
title: "Overrides (Visual Basic) | Microsoft Docs"
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
  - "Overrides"
  - "vb.Overrides"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "properties [Visual Basic], redefining"
  - "procedures, overriding"
  - "procedures, redefining"
  - "overriding"
  - "Overrides keyword"
  - "overriding, Overrides keyword"
  - "properties [Visual Basic], overriding"
ms.assetid: 9f5e6144-ce10-465e-842b-1a8f8760af90
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Overrides (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

指定屬性或程序會覆寫繼承自基底類別的同名屬性或程序。  
  
## 備註  
  
## 規則  
  
-   **宣告內容。** 您只能在屬性或程序宣告陳述式中使用 `Overrides`。  
  
-   **結合的修飾詞。** 您不能相同的宣告中同時指定 `Overrides` 與 `Shadows` 或 `Shared`。  因為覆寫項目可隱含覆寫，您無法結合 `Overridable` 與 `Overrides`。  
  
-   **相符簽章。** 此宣告的簽章必須完全符合它覆寫的屬性或程序的*簽章*。  這表示的參數清單必須有相同數目的參數、相同的順序及相同的資料類型。  
  
     除了簽章，覆寫宣告也必須完全符合下列各項：  
  
    -   存取層級  
  
    -   傳回類型 \(如果有的話\)  
  
-   **泛型簽章。** 在泛型程序中，簽章包含類型參數的個數。  因此，覆寫宣告在這方面也必須符合基底類別版本。  
  
-   **其他符合。** 除了符合簽章的基底類別版本，此宣告在下列方面也必須符合它：  
  
    -   存取層級修飾詞 \(例如 [Public](../../../visual-basic/language-reference/modifiers/public.md)\)  
  
    -   每個參數的傳遞機制 \([ByVal](../../../visual-basic/language-reference/modifiers/byval.md) 或 [ByRef](../../../visual-basic/language-reference/modifiers/byref.md)\)  
  
    -   泛型程序的每個類型參數的條件約束清單  
  
-   **遮蔽和覆寫。** 遮蔽和覆寫都會重新定義繼承的項目，但這兩種方法之間有顯著的差異。  如需詳細資訊，請參閱 [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)。  
  
 如果您使用 `Overrides`，編譯器會隱含地新增 `Overloads`，讓程式庫 API 更容易使用 C\#。  
  
 `Overrides` 修飾詞可用於以下內容：  
  
 [Function 陳述式](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property 陳述式](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub 陳述式](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## 請參閱  
 [MustOverride](../../../visual-basic/language-reference/modifiers/mustoverride.md)   
 [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md)   
 [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md)   
 [關鍵字](../../../visual-basic/language-reference/keywords/index.md)   
 [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)   
 [Visual Basic 中的泛型類型](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)   
 [Type List](../../../visual-basic/language-reference/statements/type-list.md)