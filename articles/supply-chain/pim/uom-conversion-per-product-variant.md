---
title: Mælieiningarumreikningur á afurðarafbrigði
description: Í þessu efnisatriði er fjallað um hvernig hægt er að setja upp mælieiningarumreikninga fyrir afurðarafbrigði.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: a47f705976b7a5b34492294e28aa8cd47ea38825
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/22/2019
ms.locfileid: "345928"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mælieiningarumreikningur á afurðarafbrigði

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

Í þessu efnisatriði er fjallað um hvernig hægt er að setja upp mælieiningarumreikninga fyrir afurðarafbrigði. Dæmi um uppsetninguna fylgir með.

Þessi eiginleiki gerir fyrirtækjum kleift að skilgreina mismunandi umreikninga eininga milli afbrigða sömu afurðarinnar. Eftirfarandi dæmi er notað í þessu efnisatriði. Fyrirtæki selur stuttermaboli í eftirfarandi stærðum: litlir, miðlungs, stórir og mjög stórir. Stuttermabolur er skilgreindur sem afurð og mismunandi stærðir eru skilgreindar sem afbrigði af vörunni. Stuttermabolunum er pakkað í kassa og það geta verið fimm bolir í kassa, fyrir utan þá mjög stóru þar sem aðeins er pláss fyrir fjóra boli. Fyrirtækið vill rekja ólík afbrigði af stuttermabolunum í einingunni **Stykki** en selur bolina í einingunni **Kassar**. Umreikningur milli birgðaeiningar og sölueiningar er 1 kassi = 5 stykki, fyrir utan afbrigðið Mjög stór þar sem umreikningurinn er 1 kassi = 4 stykki.

## <a name="setup"></a>Uppsetning

Hægt er að skilgreina færibreyturnar til að nota eiginleikann fyrir afurðir sem **Öll ferli** eða eingöngu fyrir afurð sem er virkjuð fyrir **Vöruhúsaferli** með því að nota valkostinn **Kveikja á mælieiningarumreikningum** á síðunni **Færibreytur afurðarupplýsinga**.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Setja upp afurð fyrir umreikning einingar fyrir hvert afbrigði

Aðeins er hægt að búa til afurðarafbrigði fyrir afurðir af **Undirgerð afurðar**: **Afurðarsniðmát**. Nánari upplýsingar er að finna í [Stofna afurðarsniðmát](tasks/create-product-master.md).

Eiginleikinn er ekki virkjaður fyrir afurðir sem eru settar upp fyrir ferli framleiðsluþyngdar. 

Við stofnun afurðarsniðmáts skal virkja mælieiningarumreikning með því að nota valkostinn **Virkja umreikninga mælieiningar** á síðunni **Upplýsingar um afurð**.

Þegar afurðarsniðmát með útgefnum afurðarafbrigðum er búið til, er hægt að setja upp umreikninga eininga fyrir hvert afbrigði. Hægt er að finna valmyndaratriðið til að opna síðu fyrir umreikning eininga í samhengi við afurð eða afurðarafbrigði á eftirfarandi síðum.

-   Síðan **Upplýsingar um afurð**
-   Síðan **Upplýsingar um útgefnar afurðar**
-   Síðan **Útgefin afurðarafbrigði**

Þegar þú opnar síðuna **Umreikningur eininga** í samhengi við afurðarsniðmát eða útgefið afurðarafbrigði getur þú valið hvort þú vilt setja upp umreikning eininga fyrir afurðina eða fyrir afurðarafbrigðið. Þú gerir það með því að velja annaðhvort **Afurðarafbrigði** eða **Afurð** í reitnum **Búa til umreikning fyrir**.

### <a name="product-variant"></a>Afurðarafbrigði

Ef þú velur **Afurðarafbrigði** getur þú valið fyrir hvaða afbrigði þú vilt setja upp umreikning eininga í reitnum **Afurðarafbrigði**.

### <a name="product"></a>Afurð

Ef þú velur **Afurð** getur þú sett upp umreikning eininga fyrir afurðarsniðmát. Þessi umreikningur eininga á við um öll afurðarafbrigði með engan skilgreindan umreikning eininga.

### <a name="example"></a>Dæmi

Afurðarsniðmát, **Stuttermabolur**, er með fjögur útgefin afurðarafbrigði: Lítill, Miðlungs, Stór og Mjög stór. Stuttermabolunum er pakkað í kassa og það geta verið fimm bolir í kassa, fyrir utan þá Mjög stóru þar sem aðeins er pláss fyrir fjóra boli.

Fyrst skaltu opna síðuna **Umreikningur eininga** á upplýsingasíðu útgefinna afurða fyrir **Stuttermabolir.**

Á síðunni **Umreikningur eininga** skal setja upp umreikning eininga fyrir útgefna afurðarafbrigðið Mjög stór.

| **Svæði**             | **Stilling**             |
|-----------------------|-------------------------|
| Búa til umskráningu fyrir | Afurðarafbrigði         |
| Afurðarafbrigði       | Stuttermabolur : : Mjög stór : : |
| Frá einingu             | Kassar                   |
| Stuðull                | 4                       |
| Til einingar               | Stykki                  |

Útgefnu afurðarafbrigðin Lítill, Miðlungs og Stór eru með sama umreikning eininga milli eininganna Kassi og Stykki, sem þýðir að hægt er að skilgreina umreikning eininga fyrir þessi afurðarafbrigði í afurðarsniðmátinu.

| **Svæði**             | **Stilling** |
|-----------------------|-------------|
| Búa til umskráningu fyrir | Afurð     |
| Afurð               | Stuttermabolur     |
| Frá einingu             | Kassar       |
| Stuðull                | 5           |
| Til einingar               | Stykki      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Nota Excel til að uppfæra umreikning eininga

Ef afurð er með mörg afurðarafbrigði með mismunandi umreikningum eininga, er góð hugmynd að flytja út umreikninga eininga úr síðunni **Umreikningur eininga** í Excel-töflureikni, uppfæra umreikningana, og síðan senda þá til baka til Finance and Operations.

Valmöguleikinn að flytja út í Excel og senda breytingarnar aftur til Finance and Operations er virkjuð í valmyndaratriðinu **Opna í Microsoft Office** í aðgerðarúðunni á síðunni **Umreikningur eininga**.
