---
title: "My.Settings 物件 | Microsoft Docs"
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
  - "My.MySettingsProperty.Settings"
  - "My.Settings"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Settings 物件"
ms.assetid: 41f30dc1-202a-4273-b9b7-5728941f996c
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
translationtype: Human Translation
---
# My.Settings 物件
[!INCLUDE[vs2017banner](../../../csharp/includes/vs2017banner.md)]

提供屬性和方法來存取應用程式的設定。  
  
## <a name="remarks"></a>備註  
  `My.Settings` 物件提供應用程式的設定存取權，並可讓您動態儲存和擷取屬性設定和應用程式的其他資訊。 如需詳細資訊，請參閱 [管理應用程式設定 (.NET)](/visual-studio/ide/managing-application-settings-dotnet)。  
  
## <a name="properties"></a>屬性  
 屬性的 `My.Settings` 物件提供存取您的應用程式設定。 若要新增或移除設定，使用 **設定設計工具**。  
  
 每個設定 **名稱**, ，**類型**, ，**範圍**, ，和 **值**, ，以及這些設定會決定要存取的每個設定的屬性會出現在 `My.Settings` 物件︰  
  
-   **名稱** 判斷屬性的名稱。  
  
-   **型別** 判斷屬性的型別。  
  
-   **範圍** 指出屬性是否為唯讀。 如果值為 **應用程式**, ，屬性是唯讀; 如果值為 **使用者**, ，屬性是讀寫。  
  
-   **值** 是屬性的預設值。  
  
## <a name="methods"></a>方法  
  
|||  
|-|-|  
|方法|說明|  
|`Reload`|重新載入使用者設定從上次儲存的值。|  
|`Save`|儲存目前的使用者設定。|  
  
  `My.Settings` 物件也會提供進階的屬性和方法，繼承自 <xref:System.Configuration.ApplicationSettingsBase> 類別。  
  
## <a name="tasks"></a>工作  
 下表列出包含工作的範例 `My.Settings` 物件。  
  
|||  
|-|-|  
|以|請參閱|  
|讀取應用程式設定|[如何︰ 讀取 Visual Basic 中的應用程式設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)|  
|變更使用者設定|[如何︰ 變更 Visual Basic 中的使用者設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)|  
|保存使用者設定|[如何︰ 保存 Visual Basic 中的使用者設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)|  
|建立使用者設定的屬性方格|[如何︰ 建立 Visual Basic 中的使用者設定的屬性方格](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)|  
  
## <a name="example"></a>範例  
 此範例中顯示的值 `Nickname` 設定。  
  
 [!CODE [VbVbalrMyResources#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#14)]  
  
 為了讓範例能夠運作，您的應用程式必須 `Nickname` 類型設定 `String`。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Configuration.ApplicationSettingsBase>   
 [如何︰ 讀取 Visual Basic 中的應用程式設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)   
 [如何︰ 變更 Visual Basic 中的使用者設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)   
 [如何︰ 保存 Visual Basic 中的使用者設定](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)   
 [如何︰ 建立 Visual Basic 中的使用者設定的屬性方格](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)   
 [管理應用程式設定 (.NET)](/visual-studio/ide/managing-application-settings-dotnet)