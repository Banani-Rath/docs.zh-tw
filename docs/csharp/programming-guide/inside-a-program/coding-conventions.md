---
title: "C# 編碼慣例 (C# 程式設計手冊) | Microsoft Docs"
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
  - "C# 語言, 編碼慣例"
  - "編碼慣例, C#"
  - "Visual C#, 編碼慣例"
ms.assetid: f4f60de9-d49b-4fb6-bab1-20e19ea24710
caps.latest.revision: 32
caps.handback.revision: 32
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# C# 編碼慣例 (C# 程式設計手冊)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

[C\# 語言規格](http://go.microsoft.com/fwlink/?LinkId=199552)未定義編碼標準。  但 Microsoft 會利用本主題中的指導方針，開發範例與文件。  
  
 編碼慣例有下列用途：  
  
-   建立外觀一致的程式碼，讓讀者可以專注於內容，而非版面配置。  
  
-   讓讀者可以依據先前的經驗做出假設，更快速地了解程式碼。  
  
-   有助於複製、變更及維護程式碼。  
  
-   示範 C\# 的最佳作法。  
  
## 命名規範  
  
-   在不包含 [using 指示詞](../../../csharp/language-reference/keywords/using-directive.md)的簡短範例中，使用命名空間限定。  如果您知道專案中預設會匯入命名空間，則無須完整限定該命名空間的名稱。  如果限定的名稱太長無法顯示在同一行，則可以在點 \(.\) 之後中斷名稱，如下範例所示。  
  
     [!CODE [csProgGuideCodingConventions#1](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#1)]  
  
-   您無須變更使用 Visual Studio 設計工具所建立的物件之名稱，使其符合其他指導方針。  
  
## 版面配置慣例  
 好的版面配置使用格式設定，來強調程式碼的結構，並讓程式碼更易於閱讀。  Microsoft 範例遵循以下慣例：  
  
-   使用預設程式碼編輯器設定 \(智慧型縮排、四個字元縮排、定位點儲存為空格\)。  如需詳細資訊，請參閱[格式、C\#、文字編輯器、選項](/visual-studio/ide/reference/options-text-editor-csharp-formatting)。  
  
-   每行只撰寫一個陳述式。  
  
-   每行只撰寫一個宣告。  
  
-   如果連續行不會自動縮排，則縮排一個定位停駐點 \(四個空格\)。  
  
-   在方法定義與屬性定義之間新增至少一個空白行。  
  
-   使用括號清楚分隔運算式中的子句，如下列程式碼所示。  
  
     [!CODE [csProgGuideCodingConventions#2](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#2)]  
  
## 註解慣例  
  
-   將註解置於單獨的一行，不在程式碼行結尾處。  
  
-   以大寫字母開始註解文字。  
  
-   以句號結束註解文字。  
  
-   註解分隔符號 \(\/\/\) 與註解文字之間插入一個空格，如下列範例所示。  
  
     [!CODE [csProgGuideCodingConventions#3](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#3)]  
  
-   不要在註解周圍建立格式化的星號區塊。  
  
## 語言指導方針  
 下列各節說明 C\# 小組在準備程式碼範例時應遵循的作法。  
  
### String 資料類型  
  
-   使用 `+` 運算子串連短字串，如下列程式碼所示。  
  
     [!CODE [csProgGuideCodingConventions#6](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#6)]  
  
-   若要在迴圈中附加字串，特別是正在使用大量文字時，請使用 <xref:System.Text.StringBuilder> 物件。  
  
     [!CODE [csProgGuideCodingConventions#7](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#7)]  
  
### 隱含類型區域變數  
  
-   當區域變數的類型明顯來自指派的右側，或精確類型並不重要時，請為該變數使用[隱含類型](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md)。  
  
     [!CODE [csProgGuideCodingConventions#8](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#8)]  
  
-   當類型不是明顯來自指派的右側時，請勿使用 [var](../../../csharp/language-reference/keywords/var.md)。  
  
     [!CODE [csProgGuideCodingConventions#9](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#9)]  
  
-   請勿依賴變數名稱，指定變數的類型。  有可能會不正確。  
  
     [!CODE [csProgGuideCodingConventions#10](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#10)]  
  
-   避免使用 `var` 取代 [dynamic](../../../csharp/language-reference/keywords/dynamic.md)。  
  
-   使用隱含類型，確定 [for](../../../csharp/language-reference/keywords/for.md) 和 [foreach](../../../csharp/language-reference/keywords/foreach-in.md) 迴圈中迴圈變數的類型。  
  
     下列範例在 `for` 陳述式中使用隱含類型。  
  
     [!CODE [csProgGuideCodingConventions#11](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#11)]  
  
     下列範例在 `foreach` 陳述式中使用隱含類型。  
  
     [!CODE [csProgGuideCodingConventions#12](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#12)]  
  
### 不帶正負號的資料類型  
  
-   一般而言，請使用 `int` 而非不帶正負號的類型。  `int` 的使用在 C\# 中非常普遍，當您使用 `int` 時，可更易於與其他程式庫互動。  
  
### 陣列  
  
-   當您在宣告行上初始化陣列時，請使用簡潔的語法。  
  
     [!CODE [csProgGuideCodingConventions#13](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#13)]  
  
### 委派  
  
-   您可以使用簡潔的語法，建立委派類型的執行個體。  
  
     [!CODE [csProgGuideCodingConventions#14](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#14)]  
  
     [!CODE [csProgGuideCodingConventions#15](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#15)]  
  
### 例外狀況處理中的 try\-catch 和 using 陳述式  
  
-   針對大部分例外狀況處理，請使用 [try catch](../../../csharp/language-reference/keywords/try-catch.md) 陳述式。  
  
     [!CODE [csProgGuideCodingConventions#16](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#16)]  
  
-   使用 C\# [using 陳述式](../../../csharp/language-reference/keywords/using-statement.md)，可簡化程式碼。  如果您有 [try\-finally](../../../csharp/language-reference/keywords/try-finally.md) 陳述式，而其中 `finally` 區塊內唯一的程式碼是 <xref:System.IDisposable.Dispose%2A> 方法的呼叫，則請改用 `using` 陳述式。  
  
     [!CODE [csProgGuideCodingConventions#17](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#17)]  
  
### && 和 &#124;&#124; 運算子  
  
-   為避免發生例外狀況，並略過不必要的比較而提升效能，請在進行比較時，使用 [&&](../../../csharp/language-reference/operators/conditional-and-operator.md) 取代 [&](../../../csharp/language-reference/operators/and-operator.md)，並使用 [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md) 取代                                        [&#124;](../../../csharp/language-reference/operators/or-operator.md) ，如下範例所示。  
  
     [!CODE [csProgGuideCodingConventions#18](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#18)]  
  
### New 運算子  
  
-   使用物件執行個體化的簡潔形式，搭配隱含類型，如下宣告所示。  
  
     [!CODE [csProgGuideCodingConventions#19](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#19)]  
  
     前一行相當於下列宣告。  
  
     [!CODE [csProgGuideCodingConventions#20](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#20)]  
  
-   使用物件初始設定式，簡化物件的建立。  
  
     [!CODE [csProgGuideCodingConventions#21](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#21)]  
  
### 事件處理  
  
-   如果要定義稍後不需要移除的事件處理常式，請使用 Lambda 運算式。  
  
     [!CODE [csProgGuideCodingConventions#22](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#22)]  
  
     [!CODE [csProgGuideCodingConventions#23](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#23)]  
  
### 靜態成員  
  
-   使用類別名稱 [ClassName.StaticMember](../../../csharp/language-reference/keywords/static.md)，呼叫 *static* 成員。  這種作法可讓靜態存取更加清晰，從而讓程式碼更易於閱讀。  請勿使用衍生類別的名稱，限定在基底類別中定義的靜態成員。  編譯該程式碼時，如果將具有相同名稱的靜態成員加入衍生類別，則會破壞程式碼的清楚程度，且程式碼之後可能會在中斷。  
  
### LINQ 查詢  
  
-   請為查詢變數使用有意義的名稱。  下列範例對位於西雅圖的客戶，使用 `seattleCustomers`。  
  
     [!CODE [csProgGuideCodingConventions#25](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#25)]  
  
-   使用別名，確保匿名類型的屬性名稱使用 Pascal 大小寫慣例，大寫正確。  
  
     [!CODE [csProgGuideCodingConventions#26](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#26)]  
  
-   當結果中的屬性名稱可能會造成混淆時，請重新命名屬性。  例如，如果查詢傳回了客戶名稱與經銷商 ID，但沒有在結果在將它們保留為 `Name` 和 `ID`，請對它們重新命名，以釐清 `Name` 是客戶的名稱，而 `ID` 是經銷商的 ID。  
  
     [!CODE [csProgGuideCodingConventions#27](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#27)]  
  
-   在查詢變數和範圍變數的宣告中使用隱含類型。  
  
     [!CODE [csProgGuideCodingConventions#25](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#25)]  
  
-   在 [from](../../../csharp/language-reference/keywords/from-clause.md) 子句下對齊查詢子句，如先前範例所示。  
  
-   在其他查詢子句前，使用 [where](../../../csharp/language-reference/keywords/where-clause.md) 子句以確保之後的查詢子句，會對已經過篩選而數量減少的一組資料進行操作。  
  
     [!CODE [csProgGuideCodingConventions#29](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#29)]  
  
-   使用多個 `from` 子句，而非 [join](../../../csharp/language-reference/keywords/join-clause.md) 子句，存取內部集合。  例如，`Student` 物件的集合可能每一個都包含測驗分數的集合。  執行下列查詢時，會傳回每個超過 90 的分數，以及取得該分數的學生姓氏。  
  
     [!CODE [csProgGuideCodingConventions#30](../CodeSnippet/VS_Snippets_VBCSharp/csprogguidecodingconventions#30)]  
  
## 安全性  
 請遵循[Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md)中的指引。  
  
## 請參閱  
 [Visual Basic Coding Conventions](../../../visual-basic/programming-guide/program-structure/coding-conventions.md)   
 [Secure Coding Guidelines](../Topic/Secure%20Coding%20Guidelines.md)