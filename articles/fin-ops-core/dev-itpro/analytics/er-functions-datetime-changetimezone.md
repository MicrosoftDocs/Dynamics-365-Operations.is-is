---
title: CHANGETIMEZONE - Aðgerð rafrænnar skýrslugerðar
description: Þessi grein veitir upplýsingar um hvernig CHANGETIMEZONE rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: be94f57cfcb6115ea386a279c379662f7d401d11
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903586"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE - Aðgerð rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Aðgerðin `CHANGETIMEZONE` skilar *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* gildi á samræmdum heimstíma (\[GMT\]) sem er umreiknaður úr uppgefnu gildi dagsetningar/tíma í einu tímabelti í gildi dagsetningar/tíma í öðru tímabelti.

## <a name="syntax"></a>Málskipun

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Frumbreytur

`datetime`: *DateTime*

Gildi dagsetningar/tíma í tímabelti samræmds heimstíma sem stendur fyrir gildi dagsetningar/tíma sem á að umreikna.

`base time zone`: *[Strengur](er-formula-supported-data-types-primitive.md#string)*

Heiti tímabeltisins sem uppgefið gildi dagsetningar/tíma er breytt í fyrir umreikning.

`target time zone`: *Strengur*

Heiti tímabeltisins sem umreiknað gildi dagsetningar/tíma er breytt í við umreikning.

## <a name="return-values"></a>Skilagildi

*DateTime-gildi*

Gildi dagsetningar/tíma sem kemur út í tímabelti samræmds heimstíma.

## <a name="usage-notes"></a>Notkunarbréf

Til að tilgreina uppruna- og marktímabelta er hægt að nota heiti tímabelta sem [boðið er upp](https://data.iana.org/time-zones/releases/) á af hálfu [Internet Assigned Numbers Authority (IANA)](https://www.iana.org/) eða sem eru [studd](/windows-hardware/manufacture/desktop/default-time-zones) af Microsoft Windows.

Á keyrslutíma er undantekningin „Tímabelti „\<time zone name\>“ er ekki til staðar“ notuð ef uppgefið heiti finnst ekki í IANA-listanum eða í Windows-stýriskránni.

Fyrir tímabelti þar sem sumartími er notaður samanstendur umreikningurinn af hliðrun sumartíma samræmds heimstíma. Nýjustu tiltækar upplýsingar um þessa hliðrun eru notaðar við umreikning.

## <a name="example-1"></a>Dæmi 1

Í þessu dæmi eru notuð tímabeltisheitin fyrir Windows.

Þú skilgreinir gagnagjafann **DSX** af gerðinni **Reiknaður reitur**. Hann inniheldur eftirfarandi segð.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Ef þú stillir segð gagnagjafans **DSY** af gerðinni **Reiknaður reitur** sem `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` skilar gagnagjafinn **DSX** textanum **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Þessi texti sýnir að tímamismunurinn á milli tveggja uppgefinna tímabelta 1. júní er meira en sólarhringur. Þar af leiðandi er umreiknað gildi dagsetningar/tíma einu degi á undan uppgefins gildis dagsetningar/tíma vegna þess að grunntímabeltið er á undan tímabelti markmiðs.

Ef þú stillir segð gagnagjafans **DSY** af gerðinni **Reiknaður reitur** sem `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` skilar gagnagjafinn **DSX** textanum **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Þessi texti sýnir að tímamismunurinn á milli tveggja uppgefinna tímabelta 1. desember er minni en sólarhringur. Þar af leiðandi jafngildir gildi dagsetningar/tíma uppgefnu gildi dagsetningar/tíma.

> [!NOTE]
> Sama segðin skilar öðru fráviki á milli uppgefinna og umreiknaðra dagsetninga/tímagilda fyrir sömu pörun tímabelta vegna þess að mismunandi hliðrun sumartíma samræmds heimstíma kemur fram fyrir uppgefin tímabelti á tiltekinni dagsetningu/tíma.

## <a name="example-2"></a>Dæmi 2

Í þessu dæmi eru heiti IANA-tímabeltis notuð.

Þú skilgreinir gagnagjafann **DSX** af gerðinni **Reiknaður reitur**. Hann inniheldur eftirfarandi segð.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Ef þú stillir segð gagnagjafans **DSY** af gerðinni **Reiknaður reitur** sem `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` skilar gagnagjafinn **DSX** textanum **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Þessi texti sýnir að tímamismunurinn á milli tveggja uppgefinna tímabelta 1. júní er meira en sólarhringur. Þar af leiðandi er umreiknað gildi dagsetningar/tíma einu degi á undan uppgefins gildis dagsetningar/tíma vegna þess að grunntímabeltið er á undan tímabelti markmiðs.

Ef þú stillir segð gagnagjafans **DSY** af gerðinni **Reiknaður reitur** sem `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` skilar gagnagjafinn **DSX** textanum **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Þessi texti sýnir að tímamismunurinn á milli tveggja uppgefinna tímabelta 1. desember er minni en sólarhringur. Þar af leiðandi jafngildir gildi dagsetningar/tíma uppgefnu gildi dagsetningar/tíma.

## <a name="example-3"></a>Dæmi 3

Þú skilgreinir gagnagjafann **DSX** af gerðinni **Reiknaður reitur**. Hann inniheldur eftirfarandi segð.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Ef þú stillir segð gagnagjafans **DSY** af gerðinni **Reiknaður reitur** sem `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` skilar gagnagjafinn **DSX** textanum **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Þessi texti sýnir að tímamismunurinn á milli tveggja uppgefinna tímabelta 1. júní er meira en sólarhringur. Þar af leiðandi er umreiknað gildi dagsetningar/tíma einu degi á eftir uppgefnu gildi dagsetningar/tíma vegna þess að tímabelti markmiðs er á undan grunntímabelti.

## <a name="example-4"></a>Dæmi 4

Þú gætir fengið dagsetningar-/tímastimpil frá ytri uppruna sem texta sem inniheldur engar upplýsingar um tímabelti. Hins vegar gætirðu þekkt tímabeltið þar sem upprunastaðurinn er. Til dæmis færðu dagsetningu-/tímastimpilinn **01/12/2021 12:55:00** frá þjónustu sem er starfrækt á Spáni. Til að vista rétt þetta gildi dagsetningar/tíma í gagnagrunninn skal ljúka eftirfarandi umreikningi:

- Skilgreindu gagnagjafann **DSY** af gerðinni **Reiknaður reitur** til að umreikna dagsetningar-/tímastimpil úr texta í dagsetningar-/tímagildi samræmds heimstíma.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Skilgreindu gagnagjafann **DSX** af gerðinni **Reiknaður reitur** til að hliðra dagsetningar-/tímagildi samræmds heimstíma sem dagsetningar-/tímagildi fyrir tímabelti ytri upprunastaðar.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Þegar þú notar `CHANGETIMEZONE` aðgerðina fyrir umreikning dagsetningar/tíma skal hafa í huga að öll gildi dagsetningar/tíma vistuð í gagnagrunninum sem gildi í tímabelti samræmds heimstíma. Áður en hægt er að sýna þetta gildi á síðum forrits er því umbreytt. Umbreytingin tekur mið af tímabeltinu sem er [stillt](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) sem kjörsvæði fyrir innskráðan notanda forritsins.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar- og tímaaðgerðir](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
