---
title: Listi yfir ER-aðgerðir í lénssértæka flokknum fyrir viðskipti
description: Þessi grein veitir upplýsingar um aðgerðir fyrir lénsértæka virkni fyrir viðskipti sem eru studdar í rafrænni skýrslugerð (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b1ac46cf10d57b40af1fa99021156ad97a17ba20
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272683"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>Listi yfir ER-aðgerðir í lénssértæka flokknum fyrir viðskipti

[!include [banner](../includes/banner.md)]

Hægt er að nota aðgerðir tiltekins léns í rafrænni skýrslugerð til að framkvæma útreikninga og beiðnir um gagnaaðgang sem eiga sérstaklega við um innleiðingu á Microsoft Dynamics 365 Finance. Þessi grein gefur yfirlit yfir þessar aðgerðir.

## <a name="list-of-supported-functions"></a>Listi yfir studdar aðgerðir

| Aðgerð| Lýsing |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Þessi aðgerð skilar *Streng*-gildi sem táknar tilvísun kröfuhafa sem MOD10 segð, byggða á tölustöfum tilgreinds reikningsnúmers. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Þessi aðgerð skilar *Streng*-gildi sem táknar stakt fjárhagsvíddarkenni sem er tekið úr tilgreindum streng. Tilgreindur strengur sýnir allar víddir sem kommuaðskilinn lista yfir kenni. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Þessi aðgerð skilar *raungildi* sem sýnir niðurstöður umreiknings á tilgreindri peningaupphæð frá tilgreindum upprunagjaldmiðli til tilgreinds markgjaldmiðils með því að nota stillingar tilgreinds fyrirtækis á tilteknum degi. |
| [CurCredRef](er-functions-other-curcredref.md) | Þessi aðgerð skilar *Streng*-gildi sem táknar tilvísun kröfuhafa, byggða á tölustöfum tilgreinds reikningsnúmers. |
| [FA_Balance](er-functions-other-fabalance.md) | Þessi aðgerð skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um varanleika fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan, skýrsluár og skýrsludag. |
| [FA_Sum](er-functions-other-fasum.md) | Þessi aðgerð skilar *Ílát (skrá)*-gildi sem samanstendur af gögnum um upphæðir fastafjármuna fyrir tiltekinn hlut í varanlegum rekstrarfjármunum, kóða fyrir virðislíkan og dagsetningatímabil. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Þessi aðgerð skilar *strengja*-gildi sem sýnir kóðann fyrir lögaðilann (fyrirtæki) sem notandi er skráður inn á. |
| [ISOCredRef](er-functions-other-isocredref.md) | Þessi aðgerð skilar *strengja*-gildi sem sýnir tilvísun Alþjóðlegu staðlastofnunarinnar (ISO), byggt á tölustöfum og stafrófstáknum í tilgreindu númeri vörureiknings. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Þessi aðgerð skilar *Boolean*-gildinu **TRUE** ef tilgreindur strengur táknar gildan alþjóðlegan bankareikning (IBAN). Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**. |
| [Mod_97](er-functions-other-mod97.md) | Þessi aðgerð skilar *Streng*-gildi sem táknar tilvísun kröfuhafa sem MOD97 segð, byggða á tölustöfum tilgreinds reikningsnúmers. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Þessi aðgerð skilar *strengja*-gildi sem táknar nýtt myndað gildi númeraraðar, byggt á tilgreindri númeraröð, umfangi og umfangskenni. Umfangskennið jafngildir fyrirtækjakóðanum sem er til staðar í því samhengi sem ER sniðið er keyrt undir. |
| [RoundAmount](er-functions-other-roundamount.md) | Þessi aðgerð skilar *raungildi* sem táknar niðurstöðuna af námundun tilgreindrar upphæðar að tilgreindum fjölda aukastafa í samræmi við tilgreinda ávölunarreglu. |
| [TableName2ID](er-functions-other-tablename2id.md) | Þessi aðgerð skilar tölulegri framsetningu töfluauðkennis fyrir tilgreint töfluheiti sem *heiltölu*-gildi. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Formúlutungumál í rafrænni skýrslugerð](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
