---
title: Listi yfir ER-aðgerðir í gerðaumbreytingaflokknum
description: Þetta efni veitir upplýsingar um umreikningsaðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686076"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Listi yfir ER-aðgerðir í gerðaumbreytingaflokknum

[!include [banner](../includes/banner.md)]

Hægt er að nota umbreytingaraðgerðir fyrir rafræna skýrslugerð (ER) til að umbreyta gildi milli gerða. Þetta efni gefur yfirlit yfir þessar aðgerðir.

## <a name="type-conversion-functions"></a>Aðgerðir fyrir umbreytingu á gerð

| Aðgerð | Lýsing |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Þessi aðgerð skilar *Int64*-gildi sem táknar tilgreindan streng. |
| [IntValue](er-functions-conversion-intvalue.md)       | Þessi aðgerð skilar *Int*-gildi sem táknar tilgreindan streng. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Þessi aðgerð skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi. Við umreikning er tekið tillit til tilgreindra flokkunarskiltákna aukastafa og tölustafa. |
| [Virði](er-functions-conversion-value.md)             | Þessi aðgerð skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Umreikningsaðgerðir gerðar í flokknum Dagsetning og tími

Eftirfarandi tafla lýsir umreikningsaðgerðum gerða í [dagsetningar- og tímaflokknum](er-functions-category-datetime.md).

| Aðgerð | Lýsing |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu *strengja*-gildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningar-/tímagildi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Þessi aðgerð skilar *DateTime*-gildi sem er umreiknað úr gefnu *dagsetningar*-gildi í dagsetningar-/tímagildi í samræmdan alþjóðlegan tíma (meðaltími Greenwich \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Þessi aðgerð skilar *Date*-gildi sem er umreiknað úr gefnu *strengja*-gildi á tilteknu sniði og í valinni tiltekinni menningu í dagsetningargildi. |

## <a name="type-conversion-functions-in-the-list-category"></a>Umreikningsaðgerðir gerðar í listaflokknum

Eftirfarandi tafla lýsir umreikningsaðgerðum gerða í [listaflokknum](er-functions-category-list.md).

| Aðgerð | Lýsing |
|----------|-------------|
| [Listi](er-functions-list-list.md)                 | Þessi aðgerð skilar *Skráalista*-gildi sem nýjum lista sem er stofnaður úr tilgreindum frumbreytum af gerðinni *Ílát (skrá)*. |
| [ListOfFields](er-functions-list-listoffields.md) | Þessi aðgerð skilar *Skráalista*-gildi sem er stofnað byggt á skipulagi gefinnar frumbreytu af gerðinni *Upptalning* eða *Ílát (skrá)*. |
| [Skipta](er-functions-list-split.md)               | Þessi aðgerð skiptir upp tilteknu *strengjagildi* í undirstrengi og skilar niðurstöðunni sem nýju *Skráalista*-gildi. |
| [StringJoin](er-functions-list-stringjoin.md)     | Þessi aðgerð skilar *strengjagildi* sem samanstendur af samsettum gildum tiltekins svæðis úr tilgreindu gildi *skráalista*. Hægt er að aðskilja gildin með tilgreindri afmörkun. |

## <a name="type-conversion-functions-in-the-text-category"></a>Umreikningsaðgerðir gerðar í textaflokknum

Eftirfarandi tafla lýsir umreikningsaðgerðum gerða í [textaflokknum](er-functions-category-text.md).

| Aðgerð | Lýsing |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Þessi aðgerð skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu. |
| [GuidValue](er-functions-text-guidvalue.md)       | Þessi aðgerð umreiknar tilgreint inntak af gerðinni *Strengur* í gagnaatriði af gerðinni *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Þessi aðgerð skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni menningu. |
| [QrCode](er-functions-text-qrcode.md)             | Þessi aðgerð skilar *Íláts*-gildi sem sýnir Quick Response Code (QR-kóða) myndar fyrir tiltekinn streng á tvíundarsniði. |
| [Texti](er-functions-text-text.md)                 | Þessi aðgerð skilar tilgreindri tölu sem *strengjagildi* sem sýnir tilgreinda tölu eftir að hún hefur verið umreiknuð í textastreng sem er sniðinn í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki forrits. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]