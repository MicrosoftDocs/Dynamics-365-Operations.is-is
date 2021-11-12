---
title: Listi yfir ER-aðgerðir í flokknum Dagsetning og tími
description: Þetta efni veitir upplýsingar um aðgerðir dagsetningar og tíma sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 706331eaadf602aba46463fdcfc0d38f1fc94e08
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647264"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Listi yfir ER-aðgerðir í flokknum Dagsetning og tími

[!include [banner](../includes/banner.md)]

Hægt er að nota dagsetningar- og tímaaðgerðir rafrænnar skýrslugerðar (ER) til að ná upplýsingum úr dagsetningar- og tímagildum og framkvæma aðgerðir á þeim. Þetta efni gefur yfirlit yfir þessar aðgerðir.

## <a name="list-of-supported-functions"></a>Listi yfir studdar aðgerðir

| Aðgerð | Lýsing |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Þessi aðgerð skilar *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* gildi sem er tilgreindur fjöldi daga fyrir eða eftir tiltekna upphafsdagsetningu. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Þessi aðgerð skilar *DateTime* gildi sem er umreiknað úr uppgefnu gildi dagsetningar/tíma í einu tímabelti í gildi dagsetningar/tíma í öðru tímabelti. |
| [DateFormat](er-functions-datetime-dateformat.md) | Aðgerðin skilar *[String](er-formula-supported-data-types-primitive.md#string)*-gildi sem setur fram tiltekið dagsetningargildi sem texta á tilteknu sniði og í valinni tiltekinni menningu. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Þessi aðgerð skilar *String*-gildi sem setur fram tiltekið dagsetningar-/tímagildi sem texta á tilteknu sniði og í valinni tiltekinni menningu. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningar-/tímagildi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu dagsetningargildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md) | Þessi aðgerð skilar *Date*-gildi sem er umreiknað úr gefnu textagildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningargildi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Þessi aðgerð skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar. |
| [Dagar](er-functions-datetime-days.md) | Þessi aðgerð skilar *heiltölu*-gildi sem sýnir fjölda daga milli einnar tilgreindrar dagsetningar og annarrar tilgreindrar dagsetningar. |
| [Now](er-functions-datetime-now.md) | Þessi aðgerð skilar *DateTime*-gildi sem táknar dagsetningu og tíma núverandi netþjóns hugbúnaðar. |
| [NullDate](er-functions-datetime-nulldate.md) | Þessi aðgerð skilar *Dagsetningar*-gildi sem táknar **núll** dagsetningu (1. janúar, 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Þessi aðgerð skilar *DateTime*-gildi sem táknar **núll** dagsetningar-/tímagildi (1. janúar, 1900) í samræmdum alþjóðlegum tíma. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Þessi aðgerð skilar *DateTime*-gildi sem táknar setudagsetningu og -tíma núverandi hugbúnaðar. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Þessi aðgerð skilar *Date*-gildi sem táknar setudagsetningu núverandi hugbúnaðar. |
| [Í dag](er-functions-datetime-today.md) | Þessi aðgerð skilar *Date*-gildi sem táknar netþjónsdagsetningu núverandi hugbúnaðar. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
