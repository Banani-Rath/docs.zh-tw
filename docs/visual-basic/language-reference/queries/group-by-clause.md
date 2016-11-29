---
title: "Group By 子句 (Visual Basic) | Microsoft Docs"
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
  - "vb.QueryGroupByInto"
  - "vb.QueryGroupBy"
  - "vb.QueryGroupRef"
  - "vb.QueryGroupInto"
  - "vb.QueryGroup"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "查詢 [Visual Basic], Group By"
  - "Group By 陳述式"
  - "Group By 子句"
ms.assetid: b1b5dcea-6654-473b-a2db-01f7e4c265d7
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# Group By 子句 (Visual Basic)
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

群組查詢結果的項目。 也可用來將彙總函式套用至每個群組。 群組作業是根據一個或多個索引鍵。  
  
## <a name="syntax"></a>語法  
  
```  
Group [ listField1 [, listField2 [...] ] By keyExp1 [, keyExp2 [...] ]  
  Into aggregateList  
```  
  
## <a name="parts"></a>組件  
  
-   `listField1`, `listField2`  
  
     選擇項。 一或多個查詢變數的欄位，明確識別要包含在群組結果中的欄位。 如果未指定任何欄位，群組結果中會包含查詢變數的所有欄位。  
  
-   `keyExp1`  
  
     必要項。 識別要用來判斷項目群組之索引鍵的運算式。 您可以指定多個索引鍵，指定複合索引鍵。  
  
-   `keyExp2`  
  
     選擇項。 一或多個額外的金鑰，結合了 `keyExp1` 以建立複合索引鍵。  
  
-   `aggregateList`  
  
     必要項。 識別群組彙總方式的一或多個運算式。 若要識別群組結果的成員名稱，請使用 `Group` 關鍵字，它可以是下列任一形式：  
  
    ```  
    Into Group  
    ```  
  
     -或-  
  
    ```  
    Into <alias> = Group  
    ```  
  
     您也可以包含將套用至群組的彙總函式。  
  
## <a name="remarks"></a>備註  
 您可以使用 `Group By` 子句來將查詢的結果分成群組。 群組是根據索引鍵或多個索引鍵所組成的複合索引鍵。 與相符索引鍵值相關聯的項目會包含在相同的群組。  
  
 您使用 `aggregateList` 子句的 `Into` 參數和 `Group` 關鍵字來識別用來參考群組的成員名稱。 您也可以在 `Into` 子句中包含彙總函式來計算群組項目的值。 如需標準彙總函式的清單，請參閱 [Aggregate Clause](../../../visual-basic/language-reference/queries/aggregate-clause.md)。  
  
## <a name="example"></a>範例  
 下列程式碼範例根據客戶的位置 (國家/地區) 進行客戶清單的分組，並提供每個群組中的客戶計數。 結果會依國家/地區名稱排序。 群組結果會依城市名稱排序。  
  
 [!CODE [VbSimpleQuerySamples#11](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#11)]  
  
## <a name="see-also"></a>另請參閱  
 [在 Visual Basic 中的 LINQ 簡介](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)   
 [查詢](../../../visual-basic/language-reference/queries/queries.md)   
 [Select 子句](../../../visual-basic/language-reference/queries/select-clause.md)   
 [From 子句](../../../visual-basic/language-reference/queries/from-clause.md)   
 [Order By 子句](../../../visual-basic/language-reference/queries/order-by-clause.md)   
 [Aggregate 子句](../../../visual-basic/language-reference/queries/aggregate-clause.md)   
 [Group Join 子句](../../../visual-basic/language-reference/queries/group-join-clause.md)