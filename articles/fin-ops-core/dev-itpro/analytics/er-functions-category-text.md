---
title: Listi yfir ER-aðgerðir í textaflokknum
description: Þetta efni veitir upplýsingar um textaaðgerðir sem eru studdar í rafrænni skýrslugerð (ER).
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916615"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Listi yfir ER-aðgerðir í textaflokknum

[!include [banner](../includes/banner.md)]

Hægt er að nota textaaðgerðir rafrænnar skýrslugerðar (ER) til að framkvæma aðgerðir á gagnagjöfum af gagnagerðinni *Strengur*. Þetta efni gefur yfirlit yfir þessar aðgerðir.

## <a name="list-of-supported-functions"></a>Listi yfir studdar aðgerðir

| Aðgerð | Lýsing |
|----------|-------------|
| [Char](er-functions-text-char.md) | Þessi aðgerð skilar *Strengja*-gildi sem sýnir stakt staftákn sem vísað er til af tilgreindu Unicode númerinu. |
| [Samtengja](er-functions-text-concatenate.md) | Þessi aðgerð skilar öllum tilgreindum textastrengjum sem *Strengja*-gildi eftir að þeir hafa verið sameinaðir í einn streng. |
| [Snið](er-functions-text-format.md) | Þessi aðgerð skilar *strengja*-gildi fyrir tilgreinan streng eftir að hann hefur verið sniðinn með því að skipta út öllum tilvikum af **%N** með *ntu* frumbreytunni. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Þessi aðgerð leitar að tilteknu *Enum*-gildi í tilgreindum tölusetningargagnagjafa með því að nota tölusetningarheitið sem er tilgreint sem *Strengja*-gildi. Ef *Enum*-gildi finnst skilar aðgerðin því. |
| [GuidValue](er-functions-text-guidvalue.md) | Þessi aðgerð umreiknar tilgreint inntak af gerðinni *Strengur* í gagnaatriði af gerðinni *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Þessi aðgerð þáttar gögn í JavaScript Object Notation (JSON) sniði sem er aðgengilegt á tilgreindri slóð og dregur út tölugildi sem byggist á tilgreindu auðkenni. Hún skilar síðan útdregnu tölugildinu sem *Strengja*-gildi. |
| [Vinstri](er-functions-text-left.md) | Þessi aðgerð skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá upphafi tiltekins strengs. |
| [Len](er-functions-text-len.md) | Þessi aðgerð skilar *heiltölugildi* sem sýnir fjölda staftákna í tilteknum streng. |
| [Lower](er-functions-text-lower.md) | Þessi aðgerð skilar tilgreindum textastreng sem *Strengja*-gildi eftir að því hefur verið breytt í lágstafi. |
| [Mid](er-functions-text-mid.md) | Þessi aðgerð skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá tilteknum streng, með upphafi í tilgreindri stöðu. |
| [NumberFormat](er-functions-text-numberformat.md) | Þessi aðgerð skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni menningu. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Þessi aðgerð skilar tilteknu tölu sem *Strengja*-gildi eftir að það hefur verið stafsett (það er, breytt í textastrengi) á tilgreindu tungumáli. |
| [PadLeft](er-functions-text-padleft.md) | Þessi aðgerð skilar *strengjagildi* af tilgreindri lengd, þar sem upphaf tilgreinds strengs er fyllt með einu eða fleiri tilvikum af tilgreindum stöfum. |
| [QrCode](er-functions-text-qrcode.md) | Þessi aðgerð skilar *Íláts*-gildi sem sýnir Quick Response Code (QR-kóða) myndar fyrir tiltekinn streng á tvíundarsniði. |
| [Skipta um](er-functions-text-replace.md) | Þessi aðgerð skilar tilgreindum textastreng sem *Strengja*-gildi eftir að öllu því eða öllu leyti hefur verið skipt út fyrir annan streng. |
| [Hægri](er-functions-text-right.md) | Þessi aðgerð skilar *strengjagildi* sem sýnir tilgreindan fjölda staftákna frá lokum tiltekins strengs. |
| [Texti](er-functions-text-text.md) | Þessi aðgerð skilar tilgreindri tölu sem *strengjagildi* eftir að því hefur verið breytt í textastreng sem er sniðið í samræmi við stillingar á þjónsstaðsetningu á núverandi tilviki forrits. |
| [Þýða](er-functions-text-translate.md) | Þessi aðgerð skilar tilgreindum textastreng sem *Strengja*-gildi eftir að öllu því eða öllu leyti hefur verið skipt út fyrir annan streng. |
| [Trim](er-functions-text-trim.md) | Þessi aðgerð skilar tilgreindum textastreng sem *strengjagildi* eftir að bilum fyrir framan og aftan hefur verið eytt, og eftir að samfelld bil milli orðanna hafa verið fjarlægð. |
| [Upper](er-functions-text-upper.md) | Þessi aðgerð skilar tilgreindum textastreng sem *Strengja*-gildi eftir að því hefur verið breytt í hástafi. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)