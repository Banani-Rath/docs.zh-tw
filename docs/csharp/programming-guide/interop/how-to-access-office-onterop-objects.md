---
title: "如何：使用 Visual C# 功能存取 Office Interop 物件 (C# 程式設計指南) | Microsoft Docs"
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
  - "動態 [C#], Office 程式設計"
  - "具名和選擇性引數 [C#], Office 程式設計"
  - "具名引數 [C#], Office 程式設計"
  - "Office 程式設計 [C#]"
  - "選擇性引數 [C#], Office 程式設計"
  - "選擇性參數 [C#], Office 程式設計"
ms.assetid: 041b25c2-3512-4e0f-a4ea-ceb2999e4d5e
caps.latest.revision: 33
caps.handback.revision: 33
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
translationtype: Human Translation
---
# 如何：使用 Visual C# 功能存取 Office Interop 物件 (C# 程式設計指南)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

Visual C\# 2010 開始採用可簡化 Office API 物件存取的新功能。  新功能包括具名引數和選擇性引數、稱為 `dynamic` 的新類型，以及傳遞引數以像是實值參數的形式，參考 COM 方法中參數的能力。  
  
 在本主題中，您將使用新的功能撰寫可建立及顯示 Microsoft Office Excel 工作表的程式碼。  接著，您將要撰寫可加入 Office Word 文件的程式碼，而該文件包含連結至 Excel 工作表的圖示。  
  
 若要完成這個逐步解說，電腦上必須安裝 Microsoft Office Excel 2007 和 Microsoft Office Word 2007 或更新版本。  
  
 如果您使用 [!INCLUDE[windowsver](../../../csharp/programming-guide/interop/includes/windowsver_md.md)] 以前的作業系統，請確定已安裝 [!INCLUDE[dnprdnlong](../../../csharp/programming-guide/events/includes/dnprdnlong_md.md)]。  
  
 [!INCLUDE[note_settings_general](../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### 建立新的主控台應用程式  
  
1.  啟動 Visual Studio。  
  
2.  在 \[檔案\] 功能表中，指向 \[新增\]，然後按一下 \[專案\]。  \[**新增專案**\] 對話方塊隨即出現。  
  
3.  在 \[已安裝的範本\] 窗格中，展開 \[Visual C\#\]，然後按一下 \[Windows\]。  
  
4.  查看 \[新增專案\] 對話方塊頂端，確定已選取 \[.NET Framework 4\] \(或更新版本\) 做為目標架構。  
  
5.  按一下 \[**範本**\] 窗格中的 \[**主控台應用程式**\]。  
  
6.  在 \[名稱\] 欄位中，輸入您專案的名稱。  
  
7.  按一下 \[**確定**\]。  
  
     新的專案隨即會出現在 \[方案總管\] 中。  
  
### 加入參考  
  
1.  在 \[方案總管\] 中，於專案名稱上按一下滑鼠右鍵，然後按一下 \[加入參考\]。  \[加入參考\] 對話方塊隨即出現。  
  
2.  在 \[組件\] 頁面的 \[元件名稱\] 清單中，選取 \[Microsoft.Office.Interop.Word\]，然後按住 CTRL 鍵並選取 \[Microsoft.Office.Interop.Excel\]。  如果看不到組件，則可能需要確定組件已安裝及顯示 \(請參閱[如何：安裝 Office 主要 Interop 組件](../Topic/How%20to:%20Install%20Office%20Primary%20Interop%20Assemblies.md)\)。  
  
3.  按一下 \[**確定**\]。  
  
### 加入必要的 using 指示詞  
  
1.  在 \[方案總管\] 中，於 \[Program.cs\] 檔案上按一下滑鼠右鍵，然後按一下 \[檢視程式碼\]。  
  
2.  將下列 `using` 指示詞加入程式碼檔案頂端。  
  
     [!CODE [csProgGuideOfficeHowTo#1](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#1)]  
  
### 建立銀行帳戶清單  
  
1.  將下列類別定義貼入 **Program.cs** 的 `Program` 類別下方。  
  
     [!CODE [csProgGuideOfficeHowTo#2](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#2)]  
  
2.  將下列程式碼加入 `Main` 方法，以建立含有兩個帳戶的 `bankAccounts` 清單。  
  
     [!CODE [csProgGuideOfficeHowTo#3](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#3)]  
  
### 宣告將帳戶資訊匯出至 Excel 的方法  
  
1.  將下列方法加入 `Program` 類別，以設定 Excel 試算表。  
  
     方法 [Add](http://go.microsoft.com/fwlink/?LinkId=210910) \(英文\) 有選擇性參數，可指定特定範本。  如果您想要使用參數的預設值，則可利用選擇性參數 \([!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 中的新功能\) 省略該參數的引數。  因為下列程式碼中未傳送引數，所以 `Add` 使用預設範本並建立新的活頁簿。  舊版 C\# 中對等的陳述式需要有預留位置引數：`ExcelApp.Workbooks.Add(Type.Missing)`。  
  
     [!CODE [csProgGuideOfficeHowTo#4](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#4)]  
  
2.  在 `DisplayInExcel` 結尾，加入下列程式碼。  程式碼會將值插入工作表第一個資料列的前兩個資料行。  
  
     [!CODE [csProgGuideOfficeHowTo#5](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#5)]  
  
3.  在 `DisplayInExcel` 結尾，加入下列程式碼。  `foreach` 迴圈會將帳戶清單中的資訊，放入工作表連續資料列的前兩個資料行。  
  
     [!CODE [csProgGuideOfficeHowTo#7](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#7)]  
  
4.  在 `DisplayInExcel` 結尾加入下列程式碼，以調整資料行寬度以容納內容。  
  
     [!CODE [csProgGuideOfficeHowTo#13](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#13)]  
  
     舊版 C\# 需要這些作業的明確轉型，因為 `ExcelApp.Columns[1]` 會傳回 `Object`，而 `AutoFit` 是 Excel [Range](http://go.microsoft.com/fwlink/?LinkId=210911) \(英文\) 方法。  下列各行會顯示轉型。  
  
     [!CODE [csProgGuideOfficeHowTo#14](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#14)]  
  
     如果 [\/link](../../../csharp/language-reference/compiler-options/link-compiler-option.md) 編譯器選項參考組件，或者，同樣地，如果 Excel \[內嵌 Interop 類型\] 屬性設定為 true，則 [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 和更新版本會自動將傳回的 `Object` 轉換為 `dynamic`。  這個屬性的預設值為 True。  
  
### 執行專案  
  
1.  在 `Main` 結尾，加入下行。  
  
     [!CODE [csProgGuideOfficeHowTo#8](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#8)]  
  
2.  按下 CTRL\+F5。  
  
     隨即會出現內含兩個帳戶資料的 Excel 工作表。  
  
### 加入 Word 文件  
  
1.  為了說明 [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 和更新版本中加強 Office 程式設計的其他方法，下列程式碼會開啟 Word 應用程式，並建立 Excel 工作表連結的圖示。  
  
     將本步驟稍後提供的 `CreateIconInWordDoc` 方法，貼入 `Program` 類別。  `CreateIconInWordDoc` 使用具名引數和選擇性引數，降低呼叫 [Add](http://go.microsoft.com/fwlink/?LinkId=210937) \(英文\) 和 [PasteSpecial](http://go.microsoft.com/fwlink/?LinkId=147099) \(英文\) 方法的複雜度。  這些呼叫採用 [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 引進的兩個其他新功能，簡化了具有參考參數之 COM 方法的呼叫。  首先，您可以將引數以實值參數的形式傳送到參考參數。  也就是說，可以直接傳送值而無須建立每個參考參數的變數。  編譯器會產生暫存變數來保存引數值，並在從呼叫返回時捨棄變數。  其次，您可以省略引數清單中的 `ref` 關鍵字。  
  
     `Add` 方法有四個參考參數，而且都是選擇性參數。  在 [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 或更新版本中，如果想要使用其預設值，可以省略任何或所有參數的引數。  在 [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp_orcas_long_md.md)] 和舊版本中，必須為每個參數提供引數，且引數必須是變數，因為參數是參考參數。  
  
     `PasteSpecial` 方法會將內容插入剪貼簿。  此方法有七個參考參數，且都是選擇性參數。  下列程式碼指定其中兩個的引數：`Link` 可建立剪貼簿的內容的來源連結，以及 `DisplayAsIcon` 可將連結顯示為圖示。  在 [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 中，可以為這兩者使用具名引數，並省略其他引數。  雖然這些是參考參數，但是您不需要使用 `ref` 關鍵字，或建立傳送為引數的變數。  可以直接傳送值。  在 [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp_orcas_long_md.md)] 和舊版本中，必須為每個參考參數傳送變數引數。  
  
     [!CODE [csProgGuideOfficeHowTo#9](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#9)]  
  
     在 [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp_orcas_long_md.md)] 或舊版語言中，需要有下列更為複雜的程式碼。  
  
     [!CODE [csProgGuideOfficeHowTo#10](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#10)]  
  
2.  在 `Main` 結尾，加入下列陳述式。  
  
     [!CODE [csProgGuideOfficeHowTo#11](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#11)]  
  
3.  在 `DisplayInExcel` 結尾，加入下列陳述式。  `Copy` 方法會將工作表加入剪貼簿。  
  
     [!CODE [csProgGuideOfficeHowTo#12](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#12)]  
  
4.  按下 CTRL\+F5。  
  
     隨即會出現含有圖示的 Word 文件。  按兩下圖示，即可將該工作表帶到前景。  
  
### 設定內嵌 Interop 類型屬性  
  
1.  當您在執行階段呼叫不需要主要 Interop 組件 \(PIA\) 的 COM 類型時，可以使用其他增強功能。  移除與 PIA 的相依性，可達成版本獨立且更容易進行部署。  如需沒有 PIA 的程式設計優點詳細資訊，請參閱[逐步解說：從 Managed 組件內嵌類型](../Topic/Walkthrough:%20Embedding%20Types%20from%20Managed%20Assemblies%20\(C%23%20and%20Visual%20Basic\).md)。  
  
     此外，程式設計會更為容易，因為 COM 方法所需和所傳回的類型可以使用類型 `dynamic` 而非 `Object` 加以呈現。  除非處於執行階段，否則不會評估類型為 `dynamic` 的變數，如此即無須明確轉型。  如需詳細資訊，請參閱[使用動態類型](../../../csharp/programming-guide/types/using-type-dynamic.md)。  
  
     在 [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp_dev10_long_md.md)] 中，預設行為是內嵌類型資訊，而非使用 PIA。  因為使用該預設值，已簡化了數個先前的範例，因為明確轉型已非必要。  例如，`DisplayInExcel` 中的 `worksheet` 宣告，撰寫為 `Excel._Worksheet workSheet = excelApp.ActiveSheet`，而非 `Excel._Worksheet workSheet = (Excel.Worksheet)excelApp.ActiveSheet`。  如果沒有預設值，則相同方法中的 `AutoFit` 呼叫也需要明確轉型，因為 `ExcelApp.Columns[1]` 會傳回 `Object`，而 `AutoFit` 是 Excel 方法。  下列程式碼會顯示轉型。  
  
     [!CODE [csProgGuideOfficeHowTo#14](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#14)]  
  
2.  若要變更預設值，並使用 PIA 而非內嵌類型資訊，請展開 \[方案總管\] 中的 \[參考\] 節點，然後選取 \[Microsoft.Office.Interop.Excel\] 或 \[Microsoft.Office.Interop.Word\]。  
  
3.  如果看不到 \[屬性\] 視窗，請按 **F4** 鍵。  
  
4.  在屬性清單中尋找 \[內嵌 Interop 類型\]，並將其值變更為 \[False\]。  同樣地，也可以在命令提示字元處使用 [\/reference](../../../csharp/language-reference/compiler-options/reference-compiler-option.md) 編譯器選項，而非 [\/link](../../../csharp/language-reference/compiler-options/link-compiler-option.md) 進行編譯。  
  
### 加入表格的其他格式  
  
1.  將 `DisplayInExcel` 中對兩個 `AutoFit` 的呼叫，取代為下列陳述式。  
  
     [!CODE [csProgGuideOfficeHowTo#15](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#15)]  
  
     [AutoFormat](http://go.microsoft.com/fwlink/?LinkId=210948) \(英文\) 方法具有七個實值參數，且全都是選擇性參數。  您可利用具名引數和選擇性引數，提供零個引數、數個引數或所有引數。  在前述陳述式中，只為其中一個參數 \(`Format`\) 提供引數。  因為 `Format` 是參數清單中的第一個參數，所以無須提供參數名稱。  但如果包含參數名稱，則可能較容易了解該陳述式，如下列程式碼所示。  
  
     [!CODE [csProgGuideOfficeHowTo#16](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#16)]  
  
2.  按 CTRL \+ F5 鍵查看結果。  其他格式會列在 [XlRangeAutoFormat](http://go.microsoft.com/fwlink/?LinkId=210967) \(英文\) 列舉中。  
  
3.  請比較步驟 1 中的陳述式與下列程式碼，這樣會顯示 [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp_orcas_long_md.md)] 或舊版本中所需的引數。  
  
     [!CODE [csProgGuideOfficeHowTo#17](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#17)]  
  
## 範例  
 下列程式碼顯示完整範例。  
  
 [!CODE [csProgGuideOfficeHowTo#18](../CodeSnippet/VS_Snippets_VBCSharp/csprogguideofficehowto#18)]  
  
## 請參閱  
 <xref:System.Type.Missing?displayProperty=fullName>   
 [dynamic](../../../csharp/language-reference/keywords/dynamic.md)   
 [使用動態類型](../../../csharp/programming-guide/types/using-type-dynamic.md)   
 [具名和選擇性引數](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)   
 [如何：在 Office 程式設計中使用具名和選擇性引數](../../../csharp/programming-guide/classes-and-structs/how-to-use-named-and-optional-arguments-in-office-programming.md)