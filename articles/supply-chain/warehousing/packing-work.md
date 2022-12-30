---
title: Pökkunarvinna fyrir pökkunargáma og vinnslusendingar á útleið
description: Þessi grein útskýrir verkbeiðnigerðinni „Pökkun“ sem stjórnar vinnu fyrir pökkun gáma og styður hlutaafhendingar á pökkuðum gámum sem tengjast hleðslum þar sem birgðavörur haldast ópakkaðar.
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220745"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Pökkunarvinna fyrir pökkunargáma og vinnslusendingar á útleið

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir verkbeiðnigerðina *Pökkun* sem stjórnar vinnu fyrir pökkun gáma og styður hlutaafhendingar á pökkuðum gámum sem tengjast hleðslum þar sem birgðavörur haldast ópakkaðar. Pökkunarvinna gerir þér kleift að nota virknina [staðfesta og flytja](confirm-and-transfer.md) til að staðfesta sendingu á útleið sem tengist gámum.

Pökkunarvinna er búin til sjálfkrafa þegar birgðir sem tengjast vinnu upprunaskjals eru settar á staðsetningar af gerðinni *Pökkunarstaðsetning*. Verkið samanstendur af tveimur línum, eina fyrir *Tínslu* og aðra fyrir *Frágang* og er sjálfkrafa viðhaldið sem hluti af lokunar-/enduropnunarferli gáms.

Frekari upplýsingar um hvernig setja á upp og nota gámapökkunarferlið er að finna í [Pakka gámum fyrir sendingu](packing-containers.md).

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessari grein skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum í eftirfarandi röð: Báðir eiginleikarnir eru hluti af einingunni **Vöruhúsakerfi**.

1. *Staðfesta og flytja*
1. *Pökkunarvinna fyrir pökkunarstöðvar*

## <a name="set-up-a-location-for-packing-work"></a>Setja upp staðsetningu fyrir pökkunarvinnu

Notaðu eftirfarandi ferli til að setja upp pökkunarstaðsetningar. Fyrir hverja staðsetningu er hægt að velja hvort kerfið býr sjálfkrafa til pökkunarvinnu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Uppsetning pökkunarstöðvar**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta við uppsetningarfærslu pökkunarstöðvar.
1. Í nýju færslunni skal stilla eftirfarandi reiti:

    - **Vöruhús** – Veldu eða farðu í vöruhúsið þar sem pökkunarstaðsetningin er.
    - **Staðsetning** – Velja eða færa inn pökkunarstaðsetningu. Þessari staðsetningu verður að vera úthlutað á staðsetningarforstillingu sem notar staðsetningargerðina sem er skilgreind sem gerð pökkunarstaðsetningar á síðunni **Færibreytur vöruhúsakerfis**. Frekari upplýsingar er að finna í [Pakka gámum fyrir sendingu](packing-containers.md).
    - **Stofna pökkunarvinnu** – Veldu þennan gátreit til að stofna pökkunarvinnu í hvert skipti sem vörur eru afhentar á pökkunarstaðsetningu. Verkið mun innihalda tengla á tengdar hleðslulínur svo hægt sé að pakka og senda hlutahleðslur.

## <a name="example-scenario"></a>Dæmi

Í þessum sýniaðstæðum er sýnt hvernig á að vinna úr sölupöntunarflæði á útleið með því að pakka gámi og afhenda hlutahleðslu.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessa atburðarás sem leiðsögn fyrir notkun eiginleikans í framleiðslukerfi. Hins vegar, í því tilfelli, verður að skipta út eigin gildi fyrir hverja stillingu sem er lýst hér.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Stilla pökkunarvinnu fyrir pökkunarstað vöruhúss

Til að hefjast handa þarftu að skilgreina vinnuferlið *Pökkun* fyrir tiltekið vöruhús og staðsetningu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Uppsetning pökkunarstöðvar**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að bæta við uppsetningarfærslu.
1. Í nýju skránni skal setja inn eftirfarandi gildi:

    - **Vöruhús:** *62*
    - **Staðsetning:** *Pakka*
    - **Stofna pökkunarvinnu:** *Já*

1. Lokið síðunni **Uppsetning pökkunarstöðvar**.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Stofna hleðslusniðmát sem leyfir hlutasendingu

Til að hægt sé að afhenda hleðslu yfir margar sendingar þarf að tengja hana við hleðslusniðmát sem leyfir hlutasendingu. Fylgið eftirfarandi leiðbeiningum til að búa til sniðmátið sem þarf.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Farmur \> Hleðslusniðmát**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að bæta við uppsetningarfærslu.
1. Í nýju skránni skal setja inn eftirfarandi gildi:

    - **Auðkenni hleðslusniðmáts:** *Hluta*
    - **Leyfa skiptingu farmlínu við staðf. afgr.:** *Já*

1. Loka síðunni **Hlaða sniðmátum**.

Frekari upplýsingar er að finna í [Staðfesta og flytja](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Sölupöntun meðhöndluð

Fylgið eftirfarandi skrefum til að vinna sölupöntun og senda hana að hluta.

1. Kláraðu [sýniaðstæðurnar](packing-containers.md#scenario) sem eru gefnar upp í [Pakka gámum fyrir sendingu](packing-containers.md). Á meðan á þeirri sviðsmynd stendur muntu búa til sölupöntun fyrir tvær einingar af einum hlut. Þú pakkar síðan aðeins einu stykki í gáminn og lokar honum. Þú ættir að skrifa hjá þér auðkenni sendingarinnar sem þú býrð til eins og er sagt í aðstæðunum.
1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna**.
1. Í síusvæðinu skal velja gátreitinn **Sýna lokað verk**. Sláðu síðan inn auðkenni sendingar í reitinn **Sía** og veldu að sía eftir gildinu **Auðkenni sendingar**. Þú ættir að sjá þrjá vinnuhausa. Ein er fyrir tiltekt sölupöntunar og hefur stöðuna *Lokað*. Tvö eru fyrir pökkunarferlið: eitt tengist lokaða gámnum og er með stöðuna *Lokað* og hitt tengist ópakkaðri eftirstandandi vöru og er með stöðuna *Opið*.
1. Veldu gildið **Auðkenni hleðslu** fyrir einhvern af vinnuhausunum til að opna síðuna **Upplýsingar um hleðslu** fyrir hleðsluna.
1. Skiptið yfir í **Hausa** yfirlitið.
1. Í flýtiflipanum **Almennt** skal velja hnappinn **Breyta** fyrir reitinn **Auðkenni hleðslusniðmáts**. Veldu síðan hleðslusniðmát hlutasendingar sem var búið til fyrir þessar aðstæður (*Hluta*).
1. Í aðgerðasvæðinu, í flipanum **Afhenda og móttaka** í flokknum **Staðfesta** skal velja **Sending á útleið**.
1. Í svarglugganum **Staðfesta sendingu** skal velja valkostinn **Skipta magni á nýja hleðslu**.
1. Veldu **Í lagi**.

Nú hefurðu sent einn gám sem tengist upprunalegri hleðslu og kerfið hefur búið til nýja hleðslu fyrir eftirstandandi vörur sem á ennþá að pakka í gáma.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
