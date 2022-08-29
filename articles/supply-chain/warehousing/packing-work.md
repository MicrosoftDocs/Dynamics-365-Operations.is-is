---
title: Pökkunarvinna við pökkun á útgámum og vinnslu sendinga
description: Þessi grein lýsir tegundinni „Pökkun“ verkbeiðni, sem stýrir vinnu við pökkun gáma og styður hlutasendingar á pökkuðum gámum sem tengjast farmi þar sem birgðavörur eru ópakkaðar.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220745"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>Pökkunarvinna við pökkun á útgámum og vinnslu sendinga

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir *Pökkun* tegund verkbeiðni, sem stjórnar vinnu við pökkun gáma og styður hlutasendingar á pökkuðum gámum sem tengjast farmi þar sem birgðavörur eru eftir ópakkaðar. Pökkunarvinna gerir þér kleift að nota [staðfesta og flytja](confirm-and-transfer.md) virkni til að staðfesta sendingar á útleið sem eru tengdar gámum.

Pökkunarvinna er sjálfkrafa búin til þegar birgðahald sem tengist frumskjalavinnu er sett á staði í *Pökkunarstaður* tegund. Verkið samanstendur af tveimur línum, annarri fyrir *Velja* og einn fyrir *Settu*, og er sjálfkrafa viðhaldið sem hluti af ferli fyrir lokun/opnun gáma.

Fyrir frekari upplýsingar um hvernig á að setja upp og nota gámapökkunarferlið, sjá [Pakkaðu ílát til sendingar](packing-containers.md).

## <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Ef kerfið þitt inniheldur ekki þá eiginleika sem lýst er í þessari grein, farðu á [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), og kveiktu á eftirfarandi eiginleikum í eftirfarandi röð. Báðir eiginleikar eru hluti af **Vöruhússtjórnun** mát.

1. *Staðfesta og flytja*
1. *Pökkunarvinna fyrir pökkunarstöðvar*

## <a name="set-up-a-location-for-packing-work"></a>Settu upp stað fyrir pökkunarvinnu

Notaðu eftirfarandi aðferð til að setja upp pökkunarstaði. Fyrir hvern stað er hægt að velja hvort kerfið býr sjálfkrafa til pökkunarvinnu.

1. Fara til **Vöruhússtjórnun \> Uppsetning \> Pökkun \> Uppsetning pökkunarstöðvar**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við uppsetningarskrá pökkunarstöðvar.
1. Í nýju skránni skaltu stilla eftirfarandi reiti:

    - **Vöruhús** – Veldu eða sláðu inn vöruhúsið þar sem pökkunarstaðurinn er staðsettur.
    - **Staðsetning** – Veldu eða sláðu inn pökkunarstaðinn. Þessari staðsetningu verður að úthluta staðsetningarsniði sem notar staðsetningargerðina sem er stillt sem gerð pökkunarstaðsetningar fyrir fyrirtæki þitt á **Vöruhússtjórnunarfæribreytur** síðu. Fyrir frekari upplýsingar, sjá [Pakkaðu ílát til sendingar](packing-containers.md).
    - **Búðu til pökkunarvinnu** – Veljið þennan gátreit til að búa til pökkunarvinnu í hvert sinn sem hlutir eru afhentir á pökkunarstaðinn. Verkið mun innihalda tengla á tengdar hleðslulínur, þannig að hægt sé að pakka og senda hluta farms.

## <a name="example-scenario"></a>Dæmi

Þetta dæmi sýnir hvernig á að vinna úr sölupöntunarflæði á útleið með því að pakka gámi og senda hlutahleðslu.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Þú getur líka notað þessa atburðarás sem leiðbeiningar til að nota eiginleikann á framleiðslukerfi. Hins vegar, í því tilfelli, verður að skipta út eigin gildi fyrir hverja stillingu sem er lýst hér.

### <a name="configure-packing-work-for-warehouse-packing-location"></a>Stilltu pökkunarvinnu fyrir pökkunarstað vöruhúss

Til að byrja verður þú að stilla *Pökkun* vinnuferli fyrir tiltekið vöruhús og staðsetningu.

1. Fara til **Vöruhússtjórnun \> Uppsetning \> Pökkun \> Uppsetning pökkunarstöðvar**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við uppsetningarskrá.
1. Í nýju skránni skaltu stilla eftirfarandi gildi:

    - **Vöruhús:** *62*
    - **Staðsetning:** *Pakka*
    - **Búðu til pökkunarvinnu:** *Já*

1. Lokaðu **Uppsetning pökkunarstöðvar** síðu.

### <a name="create-a-load-template-that-allows-partial-shipping"></a>Búðu til hleðslusniðmát sem leyfir sendingu að hluta

Til að hægt sé að afhenda farm yfir margar sendingar, verður þú að tengja það við hleðslusniðmát sem gerir ráð fyrir sendingu að hluta. Fylgdu þessum skrefum til að búa til nauðsynlegt sniðmát.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Farmur \> Hleðslusniðmát**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við uppsetningarskrá.
1. Í nýju skránni skaltu stilla eftirfarandi gildi:

    - **Auðkenni hlaða sniðmáts:** *Hluti*
    - **Leyfa skiptingu álags meðan á skipi stendur staðfest:** *Já*

1. Lokaðu **Hlaða sniðmát** síðu.

Fyrir frekari upplýsingar, sjá [Staðfesta og flytja](Confirm-and-transfer.md).

### <a name="process-a-sales-order"></a>Afgreiða sölupöntun

Fylgdu þessum skrefum til að vinna úr sölupöntun og senda hana að hluta.

1. Ljúktu við [dæmi atburðarás](packing-containers.md#scenario) sem er veitt í [Pakkaðu ílát til sendingar](packing-containers.md). Í þeirri atburðarás muntu búa til sölupöntun fyrir tvö stykki af einni vöru. Þú munt þá pakka aðeins einum af hlutunum í ílát og loka ílátinu. Þú ættir að skrifa niður sendingarauðkennið sem þú býrð til, eins og sagt er um í atburðarásinni.
1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna**.
1. Í síusvæðinu skaltu velja **Sýna lokuð verk** gátreit. Sláðu síðan inn sendingarauðkenni í **Sía** reit og veldu til að sía eftir **Sendingarauðkenni** gildi. Þú ættir nú að sjá þrjá verkhausa. Einn er fyrir sölupöntunartínsluvinnuna og hefur stöðuna *Lokað*. Tveir eru fyrir pökkunarferlið: einn er tengdur lokaða ílátinu og hefur stöðuna *Lokað*, og hitt tengist ópakkaðri vöru sem eftir er og hefur stöðuna *Opið*.
1. Veldu **Hlaða auðkenni** gildi fyrir hvaða verkhaus sem er að opna **Hlaða upplýsingar** síðu fyrir hleðsluna.
1. Skiptið yfir í **Hausa** yfirlitið.
1. Á **Almennt** flýtiflipann, veldu **Breyta** hnappinn fyrir **Hlaða auðkenni sniðmáts** sviði. Veldu síðan hleðslusniðmátið að hluta sem þú bjóst til fyrir þessa atburðarás (*Hluti*).
1. Á aðgerðarrúðunni, á **Senda og taka á móti** flipa, í **Staðfesta** hópur, veldu **Sending á útleið**.
1. Í **Skip staðfest** valmynd, veldu **Skiptu magni í nýtt hleðslu** valmöguleika.
1. Veldu **Í lagi**.

Þú hefur nú sent einn gám sem tengist upprunalegu hleðslunni og kerfið hefur búið til nýja hleðslu fyrir þær vörur sem eftir eru sem enn þarf að pakka í gáma.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
