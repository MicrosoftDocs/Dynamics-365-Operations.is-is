---
title: REPEAT ER aðgerð
description: Þessi grein veitir upplýsingar um hvernig á að nota REPEAT Electronic Reporting (ER) aðgerðina.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220724"
---
# <a name="repeat-er-function"></a>REPEAT ER aðgerð

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

The`REPEAT` fall byggir færslu sem inniheldur reitinn sem hefur gildi sem passar við tilgreint inntak. Það skilar svo nýju *Met listi* af skrá sem er endurtekin ákveðinn fjölda sinnum.

## <a name="syntax"></a>Málskipun

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Frumbreytur

`item`: Allir studdir [frumstætt](er-formula-supported-data-types-primitive.md) eða [samsettur](er-formula-supported-data-types-composite.md) gagnategund

Gildi til að endurtaka.

`number`: *Heiltala*

Fjöldi endurtekningar.

## <a name="return-values"></a>Skilagildi

*Færslulisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Listinn yfir endurteknar færslur sem er skilað afhjúpar eftirfarandi reiti:

- Tilgreint gildi (`Item` reit)
- Núverandi metvísitala (`Number` reit)

> [!NOTE]
> Vegna þess að einbyggð númerun er notuð fyrir þessa aðgerð, er`Number` reiturinn hefur gildið **1** fyrir fyrstu skráningu listans sem fékkst.

Þú getur notað þessa aðgerð til að margfalda núverandi gögn svo þú getir gert árangurs- og magnprófun á [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) lausnir með því að nota [Aðhvarfssvíta sjálfvirkniverkfæri (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Dæmi

Þú vilt búa til skjal á XML sniði sem verður að innihalda jafn mörg`Party` XML þættir eins og þú tilgreinir í gagnafærslureit í svarglugganum á keyrslutíma, áður en keyrsla á ER sniði hefst.

Eftirfarandi mynd sýnir bráðamóttökuna [sniði](er-overview-components.md#format-component). Í þessu sniði, smáskífan`Party` XML frumefni er bætt við til að afhjúpa eiginleika eins aðila.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Næsta mynd sýnir eftirfarandi stilltu gagnagjafa:

- The`Party` gagnaveita sem táknar einn aðila. The`Party.Value` reiturinn er notaður til að birta eitt textagildi.
- The`NumberOfRepeats`[gagnagjafa](er-user-input-parameter-data-sources.md) sem er notað til að bjóða upp á gagnafærslureit í svarglugganum á keyrslutíma, svo að þú getir tilgreint fjölda aðila sem ætti að færa inn í myndað skjal.
- The`Party2` gagnagjafi sem endurtekur`Party` Skráðu fjölda skipta sem þú tilgreindir í`NumberOfRepeats` gagnagjafa.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Næsta mynd sýnir gagnabindingar á breytanlegu ER-sniði sem eru búnar til til að búa til úttak á XML-sniði. Þessi framleiðsla sýnir einstaka aðila sem upptalda hnúta.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Eftirfarandi mynd sýnir niðurstöðuna þegar hönnuð snið er keyrt og gildið á`NumberOfRepeats` gagnagjafi er tilgreindur sem **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
