---
title: Ekki er hægt að uppfæra hleðslulínu vegna þess að magn sem losnar yrði neikvætt
description: Þetta vandamál kemur upp við uppfærslu eða eyðingu á hleðslulínu sem myndi valda neikvæðu losuðu magni.
author: GalynaFedorova
ms.date: 6/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSLoadLineUnShipQty,WHSLoadTable_WHSLoadLineUnShipQty,WHSLoadPlanningWorkbench_WHSLoadLineUnShipQty,WHSShipmentDetails_WHSLoadLineUnShipQty,WHSLoadPlanningListPage_DeleteButtonLoadLine,WHSLoadTable_DeleteButtonLoadLine,WHSLoadPlanningWorkbench_DeleteButtonLoadLine,WHSShipmentDetails_DeleteButtonShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a6325a632e1f68a0a3a9cb6b6091c48da014a405e8ce9ad69ea841f5cceb216f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728460"
---
# <a name="cant-update-a-load-line-because-the-released-quantity-would-be-negative"></a>Ekki er hægt að uppfæra hleðslulínu vegna þess að magn sem losnar yrði neikvætt

Villukóði: @WAX:ReleasedQtyCannotBeNegative

## <a name="symptoms"></a>Einkenni

Þetta vandamál kemur upp við uppfærslu eða eyðingu á hleðslulínu sem myndi valda neikvæðu losuðu magni. Í þessu tilviki, þegar reynt er að uppfæra eða eyða hleðslulínunni, sýnir kerfið eftirfarandi villuboð:

> Losað magn má ekki vera neikvætt fyrir afurð %1, lota %2.

Þú getur því ekki uppfært eða eytt farmlínunni.

## <a name="cause"></a>Orsök

Eftir að þú uppfærir eða eyðir hleðslulínu uppfærir kerfið losað magn tengdrar sölulínu (*whsSalesLine.ReleaseQty*). Kerfið metur losað magn og ef það kemst að því að losað magn línunnar væri neikvætt eftir uppfærsluna leyfir það þér ekki að uppfæra eða eyða línunni. Þessi villuleit á sér stað í hvert sinn sem reynt er að uppfæra annaðhvort magn hleðslulínu eða mælieiningu með ýmsum aðgerðum eins og að eyða hleðslulínu, eyða sendingu, breyta magni hleðslulínu, minnka tiltektarmagn og velja of litla tiltekt.

Algengasta ástæðan fyrir þessu vandamáli er breyting á umreikningi einingar sem er notuð fyrir opnar hleðslulínur. Til dæmis var umreikningur einingar þegar sölupöntun var gefin út *50 Ea = 1 PL*. Áður en viðkomandi sendingu hleðslu var lokið var umreikningi einingar hinsvegar breytt í *100 Ea = 1 PL*.

## <a name="resolution"></a>Lausn

Lausnin er að snúa við breytingum á umreikningi einingar eða eyða hleðslulínunni og síðan innleiða umreikninginn aftur. Þú verður að koma í veg fyrir að aðrar hleðslur sem fela í sér vöruna sem leiddi til vandamálsins frá því að vera afgreidd þangað til vandamálið er lagað. Annars gætu nýju breytingarnar verið notaðar fyrir aðrar hleðslur sem eru þegar opnar.

Til að leysa þetta vandamál skal ljúka eftirfarandi verkum:

1. Fara yfir umbreytingu einingar sem var notuð fyrir hleðslulínuna.
2. Farðu yfir núverandi umbreytingu einingar fyrir vöruna og gerðu leiðréttingar sem gera kleift að uppfæra eða eyða hleðslulínunni.
3. Uppfærðu eða eyddu hleðslulínunni og snúðu við leiðréttingum á umbreytingu einingar.

### <a name="review-the-unit-conversion-that-was-used-for-the-load-line"></a>Fara yfir umbreytingu einingar sem var notuð fyrir hleðslulínuna

Notaðu eftirfarandi ferli til að yfirfara hleðslulínurnar þínar og skrifaðu hjá þér umreikning einingarinnar sem var notaður fyrir hleðslulínuna.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veldu hleðsluna sem inniheldur hleðslulínuna sem ekki er hægt að eyða eða uppfæra.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Í efra hnitanetinu skal velja viðeigandi vinnukenni.
1. Í flipanum **Almennt** neðst á síðunni skal reikna út umreikningsstuðulinn á milli gildisins fyrir **Vinnumagn birgða** og gildisins **Vinnumagn**. Skráið niður taxtann.
1. Endurtaktu þetta ferli fyrir öll viðeigandi vinnukenni til að ganga úr skugga um að sami umreikningurinn hafi verið notaður.

### <a name="review-the-current-unit-conversion-for-the-item-and-make-adjustments"></a>Yfirfara núverandi umreikning einingar fyrir vöruna og gera leiðréttingar

Notið eftirfarandi aðferð til að fara yfir umreikning einingar fyrir afurð og gera leiðréttingar til að tryggja að umreikningur einingar sé í takt við hleðslulínuna.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opnaðu viðeigandi afurð til að fara síðuna **Upplýsingar um losaðar afurðir**.
1. Á aðgerðarúðunni á flipanum **Afurð** í flokknum **Uppsetning** skal velja **Umreikningur eininga**.
1. Veldu umreikning milli eininganna og gerðu leiðréttingar með því að nota umreikninginn sem þú fannst í fyrri hlutanum.

### <a name="update-or-delete-the-load-line-and-revert-the-unit-conversion-adjustments"></a>Uppfæra eða eyða hleðslulínunni og snúa við leiðréttingum á umbreytingu einingar

Notið eftirfarandi aðferð til að vinna úr hleðslulínunni eins og þörf er á og snúið við umreikningum eininga.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Opnaðu hleðsluna sem inniheldur hleðslulínuna sem ekki er hægt að eyða eða uppfæra.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.
1. Halda áfram með nauðsynlegar aðgerðir eftir þörfum. (Til dæmis, eyða hleðslulínunni, eða breyta magni hennar.)
1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opnaðu viðeigandi afurð til að fara síðuna **Upplýsingar um losaðar afurðir**.
1. Á aðgerðarúðunni á flipanum **Afurð** í flokknum **Uppsetning** skal velja **Umreikningur eininga**.
1. Veldu umreikninginn milli eininganna og snúðu við leiðréttingunum sem voru gerðar í fyrri hlutanum.
