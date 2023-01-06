---
title: REPEAT ER-fall
description: Þessi grein inniheldur upplýsingar um hvernig á að nota REPEAT í rafrænni skýrslugerð (ER).
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220724"
---
# <a name="repeat-er-function"></a>REPEAT ER-fall

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Aðgerðin `REPEAT` býr til færslu sem inniheldur reitinn sem er með gildi sem stemmir við tiltekið inntak. Hún skilar síðan nýjum *Færslulista* fyrir færslu sem er endurtekin ákveðið oft.

## <a name="syntax"></a>Málskipun

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Frumbreytur

`item`: Allar studdar [frum](er-formula-supported-data-types-primitive.md)- eða [samsettar](er-formula-supported-data-types-composite.md) gagnagerðir

Gildið sem á að endurtaka.

`number`: *Heiltala*

Fjöldi endurtekninga.

## <a name="return-values"></a>Skilagildi

*Færslulisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Listi yfir endurteknar færslur sem skilað er afhjúpar eftirfarandi reiti:

- Tilgreinda gildið (`Item` reitur)
- Gildandi færsluvísir (`Number` reitur)

> [!NOTE]
> Þar sem einhliða númerun er notuð fyrir þessa aðgerð skal er reiturinn `Number` með gildið **1** fyrir fyrstu færslu afleidds lista.

Hægt er að nota þessa aðgerð til að fjölga fyrirliggjandi gögnum þannig að hægt sé prófun á afköstum og magni á lausnum [Rafrænnar skýrslugerðar](general-electronic-reporting.md) með því að nota [Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Dæmi

Þú vilt búa til skjal á XML-sniði sem verður að innihalda eins margar `Party` XML-einingar og þú tilgreinir í gagnaskráningarreit í svarglugganum við keyrslu áður en keyrsla á rafrænu skýrslugerðarsniði hefst.

Eftirfarandi mynd sýnir [snið](er-overview-components.md#format-component) rafrænnar skýrslugerðar. Í þessu sniði er einni `Party` XML-einingu bætt við til að sýna eiginleika eins aðila.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

Næsta mynd sýnir eftirfarandi skilgreinda gagnagjafa:

- Gagnagjafinn `Party` sem stendur fyrir einn aðila. Reiturinn `Party.Value` er notaður til að birta eitt textagildi.
- `NumberOfRepeats` [Gagnagjafinn](er-user-input-parameter-data-sources.md) sem er notaður til að bjóða upp á gagnaskráningarreit í svarglugganum við keyrslu þannig að þú getir tilgreint fjölda aðila sem færa á inn í myndað skjal.
- `Party2` gagnagjafinn sem endurtekur `Party` færsluna eins oft og þú tilgreindir í `NumberOfRepeats` gagnagjafanum.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Næsta mynd sýnir gagnabindingar á breytanlegu sniði rafrænnar skýrslugerðar sem eru stofnaðar til að mynda úttak á XML-sniði. Þetta úttak kynnir einstaka aðila sem upptalda hnúta.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt og gildi gagnagjafans `NumberOfRepeats` er tilgreint sem **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
