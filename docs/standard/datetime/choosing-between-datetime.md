---
title: "在 DateTime、DateTimeOffset、TimeSpan 與 TimeZoneInfo 之間選擇"
description: "在 DateTime、DateTimeOffset、TimeSpan 與 TimeZoneInfo 之間選擇"
keywords: .NET, .NET Core
author: stevehoag
manager: wpickett
ms.date: 08/11/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: 2dd84ee8-9f0f-4054-9537-155857a460cd
translationtype: Human Translation
ms.sourcegitcommit: c40c28da09e8a122b542463c197196c82c81dd19
ms.openlocfilehash: f8a603bab32afd0b8e7d13c9c5755e3f14a9d2bd

---

# <a name="choosing-between-datetime-datetimeoffset-timespan-and-timezoneinfo"></a>在 DateTime、DateTimeOffset、TimeSpan 與 TimeZoneInfo 之間選擇

使用日期和時間資訊的 .NET 應用程式大不相同，並且可透過數種方式使用該資訊。 日期和時間資訊的較常見用法包含下列一或多項：

* 只反映日期，使時間資訊不重要。

* 只反映時間，使日期資訊不重要。

* 反映抽象的日期和時間，這些並不會和特定時間或位置密切相關 (例如大多數國際連鎖的商店在工作日上午 9 點開始營業)。

* 若要從 .NET 應用程式的外部來源中擷取日期和時間資訊，通常其中的日期和時間資訊會儲存為簡單資料類型。

* 若要唯一且明確地識別單一時間點。 有些應用程式只在主機系統上需要明確的日期和時間；有些則需要在不同系統上都明確 (也就是一個系統上已序列化的日期可以有意義地還原序列化，並且在世界各地的另一個系統上使用)。 

* 若要保留多個相關時間 (例如要求者的當地時間和 Web 要求的回條之伺服器時間)。

* 若要執行日期和時間運算，且該運算可能有會唯一明確地識別單一時間點的結果。 

.NET 包含 [System.DateTime](xref:System.DateTime)、[System.DateTimeOffset](xref:System.DateTimeOffset)、[System.TimeSpan](xref:System.TimeSpan) 和 [System.TimeZoneInfo](xref:System.TimeZoneInfo) 類型，這些所有的類型都能用來建置使用日期和時間的應用程式。 

> [!NOTE]
> 本主題不會討論較舊的 `TimeZone` 類型，因為它的功能幾乎已完全併入 [System.TimeZoneInfo](xref:System.TimeZoneInfo) 類別。 可能的話，開發人員應該使用 [System.TimeZoneInfo](xref:System.TimeZoneInfo) 類別，而非 `TimeZone` 類別。


## <a name="the-datetime-structure"></a>DateTime 結構

[System.DateTime](xref:System.DateTime) 值會定義特定的日期和時間。 它包含 [Kind](xref:System.DateTime.Kind) 屬性，該屬性提供該日期和時間所屬之有限的時區資訊。 [Kind](xref:System.DateTime.Kind) 屬性所傳回的 [DateTimeKind](xref:System.DateTimeKind) 值表示 [DateTime](xref:System.DateTime) 值代表當地時間 [DateTimeKind.Local](xref:System.DateTimeKind.Local))、國際標準時間 (UTC) [DateTimeKind.Utc](xref:System.DateTimeKind.Utc) 還是未指定時間 [DateTimeKind.Unspecified](xref:System.DateTimeKind.Unspecified)。

[DateTime](xref:System.DateTime) 結構適用於執行下列項目的應用程式： 

* 只使用日期。

* 只使用時間。

* 使用抽象的日期和時間。

* 使用遺漏時區資訊的日期和時間。 

* 只使用 UTC 日期和時間。 

* 從 .NET Framework 的外部來源中擷取日期和時間資訊，例如 SQL 資料庫。 一般而言，這些來源會將日期和時間資訊以和 [DateTime](xref:System.DateTime) 結構相容的簡單格式儲存。

* 執行日期和時間運算，但關心其一般結果。 例如，在對特定日期和時間加入六個月的加法運算中，該結果是否對日光節約時間進行調整通常並不重要。

除非特定的 [DateTime](xref:System.DateTime) 值代表 UTC，否則該日期和時間值的可攜性通常是不明確或受限制的。 例如，如果 [DateTime](xref:System.DateTime) 值代表當地時間，則在該當地時區是可攜式的 (也就是說，如果值在相同時區的另一個系統上還原序列化，則該值仍會明確地識別單一時間點)。 在當地時區外，[DateTime](xref:System.DateTime) 值可以有多重解譯。 如果該值的 [Kind](xref:System.DateTime.Kind) 屬性是 [DateTimeKind.Unspecified](xref:System.DateTimeKind.Unspecified)，則它的可攜性更差：現在它於相同的時區中不明確，即使在第一次序列化的同一個系統上也可能如此。 只有當 [DateTime](xref:System.DateTime) 值代表 UTC 時，該值才會明確地識別單一時間點，無論該值所使用的系統或時區為何。

> [!IMPORTANT]
> 當儲存或共用 [DateTime](xref:System.DateTime) 資料時應該使用 UTC，且 [DateTime](xref:System.DateTime) 值的 [Kind](xref:System.DateTime.Kind) 屬性應該設為 [DateTimeKind.Utc](xref:System.DateTimeKind.Utc)。

## <a name="the-datetimeoffset-structure"></a>DateTimeOffset 結構

[System.DateTimeOffset](xref:System.DateTimeOffset) 結構代表日期和時間值，以及表示該值與 UTC 差異大小的位移。 因此，該值一律明確地識別單一時間點。 

[DateTimeOffset](xref:System.DateTimeOffset) 類型包含 [DateTime](xref:System.DateTime) 類型的所有功能並感知時區。 因此適用於執行下列項目的應用程式： 

* 唯一且明確地識別單一時間點。 [DateTimeOffset](xref:System.DateTimeOffset) 類型可用來明確定義「現在」的意義，以記錄交易的時間、記錄系統或應用程式事件的時間以及記錄檔案建立及修改的時間。 

* 執行一般日期和時間運算。

* 只要時間已儲存為兩個不同的值或一個結構中的兩個成員，就可保留多個相關時間。

> [!NOTE]
> [DateTimeOffset](xref:System.DateTimeOffset) 值的用途比 [DateTime](xref:System.DateTime) 值的更為普遍。 因此對於應用程式開發，應該考慮將 [DateTimeOffset](xref:System.DateTimeOffset) 作為預設的日期和時間類型。

[DateTimeOffset](xref:System.DateTimeOffset) 值與特定的時區並沒有密切的關係，但可能來自各種不同的時區。 為了說明這點，下列範例會列出可和一些 [DateTimeOffset](xref:System.DateTimeOffset) 值有關的時區 (包括本機的太平洋標準時間)。

```csharp
using System;
using System.Collections.ObjectModel;

public class TimeOffsets
{
   public static void Main()
   {
      DateTime thisDate = new DateTime(2007, 3, 10, 0, 0, 0);
      DateTime dstDate = new DateTime(2007, 6, 10, 0, 0, 0);
      DateTimeOffset thisTime;

      thisTime = new DateTimeOffset(dstDate, new TimeSpan(-7, 0, 0));
      ShowPossibleTimeZones(thisTime);

      thisTime = new DateTimeOffset(thisDate, new TimeSpan(-6, 0, 0));  
      ShowPossibleTimeZones(thisTime);

      thisTime = new DateTimeOffset(thisDate, new TimeSpan(+1, 0, 0));
      ShowPossibleTimeZones(thisTime);
   }

   private static void ShowPossibleTimeZones(DateTimeOffset offsetTime)
   {
      TimeSpan offset = offsetTime.Offset;
      ReadOnlyCollection<TimeZoneInfo> timeZones;

      Console.WriteLine("{0} could belong to the following time zones:", 
                        offsetTime.ToString());
      // Get all time zones defined on local system
      timeZones = TimeZoneInfo.GetSystemTimeZones();     
      // Iterate time zones 
      foreach (TimeZoneInfo timeZone in timeZones)
      {
         // Compare offset with offset for that date in that time zone
         if (timeZone.GetUtcOffset(offsetTime.DateTime).Equals(offset))
            Console.WriteLine("   {0}", timeZone.DisplayName);
      }
      Console.WriteLine();
   } 
}
// This example displays the following output to the console:
//       6/10/2007 12:00:00 AM -07:00 could belong to the following time zones:
//          (GMT-07:00) Arizona
//          (GMT-08:00) Pacific Time (US & Canada)
//          (GMT-08:00) Tijuana, Baja California
//       
//       3/10/2007 12:00:00 AM -06:00 could belong to the following time zones:
//          (GMT-06:00) Central America
//          (GMT-06:00) Central Time (US & Canada)
//          (GMT-06:00) Guadalajara, Mexico City, Monterrey - New
//          (GMT-06:00) Guadalajara, Mexico City, Monterrey - Old
//          (GMT-06:00) Saskatchewan
//       
//       3/10/2007 12:00:00 AM +01:00 could belong to the following time zones:
//          (GMT+01:00) Amsterdam, Berlin, Bern, Rome, Stockholm, Vienna
//          (GMT+01:00) Belgrade, Bratislava, Budapest, Ljubljana, Prague
//          (GMT+01:00) Brussels, Copenhagen, Madrid, Paris
//          (GMT+01:00) Sarajevo, Skopje, Warsaw, Zagreb
//          (GMT+01:00) West Central Africa
```

```vb
Imports System.Collections.ObjectModel

Module TimeOffsets
   Public Sub Main()
      Dim thisTime As DateTimeOffset 

      thisTime = New DateTimeOffset(#06/10/2007#, New TimeSpan(-7, 0, 0))
      ShowPossibleTimeZones(thisTime) 

      thisTime = New DateTimeOffset(#03/10/2007#, New TimeSpan(-6, 0, 0))  
      ShowPossibleTimeZones(thisTime)

      thisTime = New DateTimeOffset(#03/10/2007#, New TimeSpan(+1, 0, 0))
      ShowPossibleTimeZones(thisTime)
   End Sub

   Private Sub ShowPossibleTimeZones(offsetTime As DateTimeOffset)
      Dim offset As TimeSpan = offsetTime.Offset
      Dim timeZones As ReadOnlyCollection(Of TimeZoneInfo)

      Console.WriteLine("{0} could belong to the following time zones:", _
                        offsetTime.ToString())
      ' Get all time zones defined on local system
      timeZones = TimeZoneInfo.GetSystemTimeZones()     
      ' Iterate time zones
      For Each timeZone As TimeZoneInfo In timeZones
         ' Compare offset with offset for that date in that time zone
         If timeZone.GetUtcOffset(offsetTime.DateTime).Equals(offset) Then
            Console.WriteLine("   {0}", timeZone.DisplayName)
         End If   
      Next
      Console.WriteLine()
   End Sub
End Module
' This example displays the following output to the console:
'       6/10/2007 12:00:00 AM -07:00 could belong to the following time zones:
'          (GMT-07:00) Arizona
'          (GMT-08:00) Pacific Time (US & Canada)
'          (GMT-08:00) Tijuana, Baja California
'       
'       3/10/2007 12:00:00 AM -06:00 could belong to the following time zones:
'          (GMT-06:00) Central America
'          (GMT-06:00) Central Time (US & Canada)
'          (GMT-06:00) Guadalajara, Mexico City, Monterrey - New
'          (GMT-06:00) Guadalajara, Mexico City, Monterrey - Old
'          (GMT-06:00) Saskatchewan
'       
'       3/10/2007 12:00:00 AM +01:00 could belong to the following time zones:
'          (GMT+01:00) Amsterdam, Berlin, Bern, Rome, Stockholm, Vienna
'          (GMT+01:00) Belgrade, Bratislava, Budapest, Ljubljana, Prague
'          (GMT+01:00) Brussels, Copenhagen, Madrid, Paris
'          (GMT+01:00) Sarajevo, Skopje, Warsaw, Zagreb
'          (GMT+01:00) West Central Africa
```

此輸出顯示在本範例中的每個日期和時間值可屬於至少三個不同時區。 2007 年 6 月 10 日的 [DateTimeOffset](xref:System.DateTimeOffset) 值顯示出若日期和時間值代表日光節約時間，則其相對於 UTC 的位移甚至不一定會對應於起始時區的基底 UTC 位移，或對應於從它的顯示名稱中找到的相對於 UTC 的位移。 這表示因為單一 [DateTimeOffset](xref:System.DateTimeOffset) 的值並不會和時區緊密結合，所以它無法反映與日光節約時間相互轉換的時區。 特別是當使用日期和時間運算來管理 [DateTimeOffset](xref:System.DateTimeOffset) 值的時候，這會有問題。 如需在考慮時區調整規則的方式下該如何執行日期和時間運算的討論，請參閱[使用日期和時間執行算術運算](performing-arithmetic-operations.md)。

## <a name="the-timespan-structure"></a>TimeSpan 結構

[System.TimeSpan](xref:System.TimeSpan) 結構表示時間間隔。 其兩個一般用法為： 

* 反映出兩個日期和時間值之間的時間間隔。 例如，從另一個值中減去一個 [DateTime](xref:System.DateTime) 值會傳回 [TimeSpan](xref:System.TimeSpan) 值。 

* 測量已耗用時間。 例如，[Stopwatch.Elapsed](xref:System.Diagnostics.Stopwatch.Elapsed) 屬性會傳回 [TimeSpan](xref:System.TimeSpan) 值，該值反映出在呼叫開始測量已耗用時間的 [System.Diagnostics.Stopwatch](xref:System.Diagnostics.Stopwatch) 方法之其中一種之後已耗用的時間間隔。

若在未參考一天中之特定時間的情況下反映時間，則 [TimeSpan](xref:System.TimeSpan) 值也可用來取代 [DateTime](xref:System.DateTime) 值。 這種用法類似於 [DateTime.TimeOfDay](xref:System.DateTime.TimeOfDay) 和 [DateTimeOffset.TimeOfDay](xref:System.DateTimeOffset.TimeOfDay) 屬性，在不參考日期之情況下，該屬性傳回的 [TimeSpan](xref:System.TimeSpan) 值代表時間。 例如，[TimeSpan](xref:System.TimeSpan) 結構可用來反映商店每日開始營業或打烊的時間，或可用來代表任何有規律事件發生的時間。

下列範例會定義 `StoreInfo` 結構，其中包含用來儲存開始營業和打烊時間的 [TimeSpan](xref:System.TimeSpan) 物件，以及代表商店所在時區的 [TimeZoneInfo](xref:System.TimeZoneInfo) 物件。 該結構也包含兩種方法，`IsOpenNow` 和 `IsOpenAt`，假定使用者處於當地時區，該結構會表示商店是否於使用者指定的時間開始營業。  

```csharp
using System;

public struct StoreInfo
{
   public String store;
   public TimeZoneInfo tz;
   public TimeSpan open;
   public TimeSpan close;

   public bool IsOpenNow()
   {
      return IsOpenAt(DateTime.TimeOfDay);
   }

   public bool IsOpenAt(TimeSpan time)
   {
      TimeZoneInfo local = TimeZoneInfo.Local;
      TimeSpan offset = TimeZoneInfo.BaseUtcOffset;

      // Is the store in the same time zone?
      if (tz.Equals(local)) {
         return time >= open & time <= close;
      }
   }
}
```

```vb
Public Structure StoreInfo
   Dim store As String
   Dim tz As TimeZoneInfo
   Dim open As TimeSpan
   Dim close As TimeSpan

   Public Function IsOpenNow() As Boolean
      Return IsOpenAt(Date.Now.TimeOfDay)
   End Function

   Public Function IsOpenAt(time As TimeSpan) As Boolean
      Dim local As TimeZoneInfo = TimeZoneInfo.Local
      Dim offset As TimeSpan = TimeZoneInfo.Local.BaseUtcOffset

      ' Is the store in the same time zone?
      If tz.Equals(local) Then
         Return time >= open And time <= close
      Else
         Dim delta As TimeSpan = TimeSpan.Zero
         Dim storeDelta As TimeSpan = TimeSpan.Zero

         ' Is it daylight saving time in either time zone?
         If local.IsDaylightSavingTime(Date.Now.Date + time) Then
            delta = local.GetAdjustmentRules(local.GetAdjustmentRules().Length - 1).DaylightDelta
         End If
         If tz.IsDaylightSavingTime(TimeZoneInfo.ConvertTime(Date.Now.Date + time, local, tz))
            storeDelta = tz.GetAdjustmentRules(local.GetAdjustmentRules().Length - 1).DaylightDelta
         End If
         Dim comparisonTime As TimeSpan = time + (offset - tz.BaseUtcOffset).Negate() + (delta - storeDelta).Negate
         Return (comparisonTime >= open And comparisonTime <= close)
      End If
   End Function
End Structure
```

然後 `StoreInfo` 結構可供用戶端程式碼使用，如下所示。 

```csharp
public class Example
{
   public static void Main()
   {
      // Instantiate a StoreInfo object.
      var store103 = new StoreInfo();
      store103.store = "Store #103";
      store103.tz = TimeZoneInfo.FindSystemTimeZoneById("Eastern Standard Time");
      // Store opens at 8:00.
      store103.open = new TimeSpan(8, 0, 0);
      // Store closes at 9:30.
      store103.close = new TimeSpan(21, 30, 0);

      Console.WriteLine("Store is open now at {0}: {1}",
                        DateTime.TimeOfDay, store103.IsOpenNow());
      TimeSpan[] times = { new TimeSpan(8, 0, 0), new TimeSpan(21, 0, 0),
                           new TimeSpan(4, 59, 0), new TimeSpan(18, 31, 0) };
      foreach (var time in times)
         Console.WriteLine("Store is open at {0}: {1}",
                           time, store103.IsOpenAt(time));
   }
}
// The example displays the following output:
//       Store is open now at 15:29:01.6129911: True
//       Store is open at 08:00:00: True
//       Store is open at 21:00:00: False
//       Store is open at 04:59:00: False
//       Store is open at 18:31:00: False
```

```vb
Module Example
   Public Sub Main()
      ' Instantiate a StoreInfo object.
      Dim store103 As New StoreInfo()
      store103.store = "Store #103"
      store103.tz = TimeZoneInfo.FindSystemTimeZoneById("Eastern Standard Time")
      ' Store opens at 8:00.
      store103.open = new TimeSpan(8, 0, 0)
      ' Store closes at 9:30.
      store103.close = new TimeSpan(21, 30, 0)

      Console.WriteLine("Store is open now at {0}: {1}",
                        Date.Now.TimeOfDay, store103.IsOpenNow())
      Dim times() As TimeSpan = { New TimeSpan(8, 0, 0),
                                  New TimeSpan(21, 0, 0),
                                  New TimeSpan(4, 59, 0),
                                  New TimeSpan(18, 31, 0) }
      For Each time In times
         Console.WriteLine("Store is open at {0}: {1}",
                           time, store103.IsOpenAt(time))
      Next
   End Sub
End Module
' The example displays the following output:
'       Store is open now at 15:29:01.6129911: True
'       Store is open at 08:00:00: True
'       Store is open at 21:00:00: False
'       Store is open at 04:59:00: False
'       Store is open at 18:31:00: False
```

## <a name="the-timezoneinfo-class"></a>TimeZoneInfo 類別

[System.TimeZoneInfo](xref:System.TimeZoneInfo) 類別代表地球的任何時區，並可讓一個時區中的任何日期和時間轉換成在另一個時區中對等的日期和時間。 [TimeZoneInfo](xref:System.TimeZoneInfo) 類別讓您能夠處理日期和時間，讓任何日期和時間值能明確地識別單一時間點。

在某些情況下，若要充分利用 [TimeZoneInfo](xref:System.TimeZoneInfo) 類別，可能需要進一步的開發工作。 日期和時間值與其所屬的時區並未緊密結合。 因此，除非您的應用程式提供讓日期和時間與相關聯時區連結的機制，否則很容易就會讓特定日期和時間值與其時區解除關聯。 連結此資訊的一種方法是定義類別或結構，其中包含日期和時間值，以及與其相關聯的時區物件。

當日期和時間物件已具現化後，僅當日期和時間值的所屬時區已知時，才有可能利用 .NET 支援的時區。 情況往往並非如此，特別是在 Web 或網路應用程式的情況下。

## <a name="see-also"></a>另請參閱

[日期、時間及時區](index.md)


<!--HONumber=Nov16_HO3-->


