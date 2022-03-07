---
title: GETENUMVALUEBYNAME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin GETNUMVALUEBYNAME í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 09/23/2020
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
ms.openlocfilehash: 03759852e5ceb13b79b0df4592bdcef76eb0a82865725c00df40b9cc5f786240
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774438"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `GETENUMVALUEBYNAME` leitar að tilteknu *Enum*-gildi í tilgreindum tölusetningargagnagjafa með því að nota tölusetningarheitið sem er tilgreint sem *Strengja*-gildi. Ef *Enum*-gildi finnst skilar aðgerðin því. Að öðrum kosti skilar aðgerðin upptalningargildinu **núll**.

## <a name="syntax"></a>Málskipun

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Frumbreytur

`enumeration data source path`: *Upptalning*

Gild slóð gagnagjafa af einni af eftirfarandi upptalningargerðum:

- Líkanaupptalning rafrænnar skýrslugerðar (ER)
- Upptalning ER-sniðs
- Upptalning Microsoft Dynamics 365 Finance

`enumeration value text`: *Strengur*

Strengagildi sem táknar heiti staks upptalningargildis.

## <a name="return-values"></a>Skilagildi

Má vera núll *Enum*

Upptalningargildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Engin undantekning er gerð ef gildið *Enum* er ekki að finna með því að nota heiti upptalningargildisins sem er tilgreint sem gildið *Strengur*.

## <a name="example-1"></a>Dæmi 1

Í eftirfarandi mynd er **ReportDirection** upptalningin kynnt í gagnalíkani. Athugaðu að merki eru skilgreind fyrir tölusetningargildin.

![Tiltæk gildi fyrir tölusetningu gagnalíkans.](./media/ER-data-model-enumeration-values.PNG)

Eftirfarandi mynd sýnir þessar upplýsingar:

- Gagnagjafinn **$Direction** er stilltur í ER-skýrslu. Þessi gagnagjafi er stilltur út frá líkanaupptalningunni **ReportDirection**.
- Segðin `$IsArrivals` er hönnuð til að nota líkanatölusetningarbyggðan gagnagjafa **$Direction** sem færibreytu þessarar aðgerðar.
- Gildi þessarar samanburðarsegðar er **TRUE**.

![Dæmi um tölusetningu gagnalíkans.](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Dæmi 2

Aðgerðirnar `GETENUMVALUEBYNAME` og [`LISTOFFIELDS`](er-functions-list-listoffields.md) gerir þér kleift að sækja gildi og merki yfir studdar tölusetningar sem textagildi. (Studdar tölusetningar eru tölusetningar forrits, tölusetningar gagnalíkans og tölusetningar sniðs.)

Á eftirfarandi mynd er gagnagjafinn **TransType** kynntur í líkanavörpun. Þessi gagnagjafi vísar í forritstölusetningu **LedgerTransType**.

![Gagnagjafi líkanavörpunar sem vísar í tölusetningu forrits.](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Eftirfarandi mynd sýnir gagnagjafann **TransTypeList** sem er skilgreindur í líkanavörpun. Þessi gagnagjafi er skilgreindur út frá **TransType** tölusetningu forrits. `LISTOFFIELDS`-aðgerðin er notuð til að skila öllum gildum tölusetningar sem lista yfir færslur sem innihalda reiti. Á þennan hátt verða upplýsingar um sérhvert gildi tölusetningar sýndar.

> [!NOTE]
> **EnumValue** gildið er skilgreint fyrir **TransTypeList** gagnagjafann með því að nota `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)`-segðina. Þessi reitur skilar gildi tölusetningar fyrir hverja færslu í þessum lista.

![Gagnagjafi líkanavörpunar sem skilar öllum tölusetningargildum af valinni tölusetningu sem lista yfir færslur.](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Eftirfarandi mynd sýnir gagnagjafann **VendTrans** sem er skilgreindur í líkanavörpun. Þessi gagnagjafi skilar lánardrottnafærslum úr forritstöflu **VendTrans**. Fjárhagsgerð hverrar færslu er skilgreind eftir gildinu á reitnum **TransType**.

> [!NOTE]
> **TransTypeTitle** gildið er skilgreint fyrir **VendTrans** gagnagjafann með því að nota `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label`-segðina. Þessi reitur skilar merki tölusetningargildis af núverandi færslu sem texta, ef þetta tölusetningargildi er í boði. Annars skilar hann auðum streng.
>
> Reiturinn **TransTypeTitle** er bundinn við **LedgerType** reit gagnalíkans sem gerir kleift að nota þessar upplýsingar í öllum sniðum rafrænnar skýrslugerðar sem notar gagnalíkanið sem upprunastað gagna.

![Gagnagjafi líkanavörpunar sem skilar lánardrottnafærslum.](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Eftirfarandi mynd sýnir hvernig hægt er að nota [kembiforrit gagnagjafans](er-debug-data-sources.md) til að prófa skilgreinda líkanavörpun.

![Nota kembiforrit gagnagjafa til að prófa skilgreinda líkanavörpun.](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

**LedgerType** reitur gagnalíkans sýnir merki af færslugerðum eins og búist var við.

Ef ætlunin er að nota þessa nálgun fyrir mikið magn af færslugögnum verður að íhuga afköst keyrslunnar. Frekari upplýsingar er að finna í [Rekja framkvæmd á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[Rekja keyrslu á sniðum rafrænnar skýrslugerðar til að úrræðaleita vandamál sem tengjast afköstum](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER-aðgerð](er-functions-list-listoffields.md)

[FIRSTORNULL ER-aðgerð](er-functions-list-firstornull.md)

[WHERE ER-aðgerð](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]