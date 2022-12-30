---
title: Aðstæður fyrir vélarstöðu
description: Þessi grein lýsir aðstæðum fyrir stöðu vélar, sem gerir þér kleift að nota skynjaragögn til að fylgjast með stöðu búnaðarins.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689640"
---
# <a name="the-machine-status-scenario"></a>Aðstæður fyrir vélarstöðu

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Aðstæður fyrir *vélarstöðu* gerir þér kleift að nota skynjaragögn til að fylgjast með stöðu búnaðarins. Ef þú setur upp skynjara sem sendir merki þegar framleiðsluverk á tilfangi vélar framleiðir úttak, en ekkert skynjaramerki er móttekið innan tiltekins tímabils, er tilkynning sýnd á stjórnborði umsjónarmanns.

## <a name="scenario-dependencies"></a>Aðstæður tengsl

Aðstæður fyrir *vélarstöðu* er með eftirfarandi tengsl:

- Aðeins er hægt að ræsa tilkynningu ef framleiðsluverk er í gangi á tengdri vél.
- Senda verður merki sem stendur fyrir merkið *hluti-út* til IoT-miðstöðvar.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Útbúa sýnigögn fyrir aðstæður vélarstöðu

Ef þú vilt nota sýnikerfi til að prófa aðstæður fyrir *stöðu vélar* skaltu nota kerfi þar sem [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) eru sett upp, velja lögaðilann (fyrirtæki) *USMF* og útbúa frekari sýnigögn eins og lýst er í þessum hluta. Ef þú notar eigin skynjara og gögn geturðu sleppt þessum hluta.

### <a name="set-up-a-sensor-simulator"></a>Setja upp skynjarahermi

Ef þú vilt prófa þessar aðstæður án þess að nota efnislegan skynjara getur þú sett upp hermi til að búa til nauðsynleg merki. Frekari upplýsingar eru í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Staðfestu að tilfang 3118 sé notað fyrir vöruna P0111

Framleiðslupöntun verður tímasett og losuð. Framleiðsluverk er þar af leiðandi losað til tilfangs *3118* (*Svampskurðarvél*). Fylgdu þessum skrefum til að staðfesta að tilfang *3118* sé notað fyrir framleiðslu *P0111* í sýnigögnunum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finnið og veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *P0111*.
1. Á aðgerðasvæðinu, í flipanum **Hönnuður**, í flokknum **Yfirlit**, skal velja **Leið**.
1. Á síðunni **Leið**, á flipanum **Yfirlit** neðst á síðunni, skaltu velja línuna þar sem **Aðg.nr.** reitur er stilltur á *30*.
1. Á flipanum **Tilfangaþarfir** neðst á síðunni skaltu ganga úr skugga um að tilfang *3118* (*Svampskurðarvél*) sé tengd aðgerðinni.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Stofna og gefa út framleiðslupöntun fyrir vöru P0111

Fylgdu eftirfarandi skrefum til að stofna og losa framleiðslupöntun fyrir vöru *P0111*.

1. Fara í **Framleiðslustýringar \> Framleiðslupantanir \> Allar framleiðslupantanir**.
1. Á síðunni **Allar framleiðslupantanir**, á aðgerðasvæðinu, skal velja **Ný runupöntun**.
1. Í svarglugganum **Stofna runu** skal stilla eftirfarandi gildi:

    - **Vörunúmer:** *P0111*
    - **Magn:** *10*

1. Veldu **Stofna** til að stofna pöntunina og fara aftur á síðuna **Allar framleiðslupantanir**.
1. Notið reitinn **Sía** til að leita að framleiðslupöntunum þar sem reiturinn **Vörunúmer** er stilltur á *P0111*. Leitaðu síðan að og veljið framleiðslupöntun sem var verið að stofna.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Áætla**.
1. Í svarglugganum **Mat** skal velja Í **lagi** til að keyra matið.
1. Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, í flokknum **Uppsetning**, skal velja **Losa**.
1. Í svarglugganum **Losa** skaltu skrá niður númer runupöntunar sem var verið að stofna.
1. Veldu **Í lagi** til að losa pöntunina.

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

Þú notar vinnsluviðmót framleiðslugólfs til að hefja verk sem var tímasett og gefið út fyrir vörunúmer *P0111* í hlutanum hér á undan. Fylgdu þessum skrefum til að skilgreina vinnslumiðmót framleiðslugólfsins.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Ef þú hefur ekki sett upp viðmótið áður birtist innskráningarsíða. Færðu inn skilríki
1. Veldu **Stilla** til að opna **Stilla tæki** leiðsagnarforritið.
1. Á síðunni **Grunnstilla tæki - Skref 1 - Velja skilgreiningu** skal velja *Sjálfgefnu* skilgreininguna.
1. Veljið **Næst**.
1. Á síðunni **Grunnstilla tæki - Skref 2 - Skilgreina svæði framleiðslugólfs** skal stilla reitinn **Tilfang** á *3118*.
1. Veldu **Í lagi**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a>Virkja leitarvalkostinn í vinnsluviðmóti framleiðslugólfsins

Til að auðvelda leit að framleiðslugólfinu fyrir framleiðslupöntunina sem var gefin út hér á undan skal fylgja þessum skrefum til að virkja leitarvalkostinn í vinnsluviðmóti framleiðslugólfsins.

1. Farið í **Framleiðslustýring \> Uppsetning \> Framkvæmd framleiðslu \> Grunnstilla framkvæmd á framleiðslugólfi**.
1. Veldu *Sjálfgefna* stillingu.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Í flýtiflipanum **Almennt** skal stilla valkostinn **Virkja leit** á *Já*.
1. Lokið síðunni.

### <a name="start-the-first-job-in-the-batch-order"></a>Ræsið fyrsta verk runupöntunina

Fylgið eftirfarandi skrefum til að hefja verkið á tilfangi *3118*.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Í reitnum **Kortkenni** slærðu inn *123*. Veljið síðan **Innskráning**.
1. Þegar beðið er um ástæðu fjarveru skaltu velja eitt af spjöldunum fyrir fjarveru og velja svo **Í lagi**.
1. Í reitnum **Leita** er slegið inn lotunúmer pöntunar sem þú skrifaðir áður niður hjá þér. Veldu síðan **færslulykilinn**.
1. Smelltu á pöntunar og veldu síðan **Hefja vinnslu**.
1. Í svarglugganum **Hefja vinnslu** velurðu **Ræsa**.

## <a name="set-up-the-machine-status-scenario"></a>Setja upp aðstæður vélarstöðu

Fylgdu þessum skrefum til að setja upp aðstæður fyrir *vélarstöðu* í Supply Chain Management.

1. Farðu í **Framleiðslustýring \> Uppsetning \> Gervigreind skynjaragagna \> Aðstæður**.
1. Í aðstæðureitnum **Staða vélar** skal velja **Skilgreina** til að opna uppsetningarleiðsögnina fyrir þessar aðstæður.
1. Á síðunni **Skynjarar** skal velja **Nýtt** til að bæta skynjara við hnitanetið. Stillið svo eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn kenni skynjarans sem þú ert að nota. (Ef þú notar Raspberry PI Azure IoT Online Simulator og hefur sett það upp eins og lýst er í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md), sláðu inn *MachineStatus*.)
    - **Lýsing á skynjara** – Færið inn lýsingu á skynjari.

1. Endurtaka á fyrra skref fyrir hvern skynjara sem þú vilt bæta við. Hægt er að koma aftur og bæta við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á síðunni **Vörpun viðskiptafærslu**, í hlutanum **Skynjarar**, skaltu velja færslu fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í hlutanum **Vörpun viðskiptafærslu** skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni, stilltu reitinn **Viðskiptafærsla** á tilfangið sem þú notar valinn skynjara til að fylgjast með. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla reitinn á *á 3118, svampskurðarvél*.)
1. Veljið **Næst**.
1. Á síðunni **Þröskuldur vélarstöðu** skal skilgreina hversu langt á eftir síðasta *hluti-út* merkið kerfið á senda tilkynningu um vélarstöðu. Tvær leiðir eru til að skilgreina þröskuldinn:

    - **Sjálfgefinn þröskuldur (mínútur)** – Stilltu þennan reit til að skilgreina sjálfgefinn þröskuld. Gildið mun síðan eiga við um öll tilföng þar sem reiturinn **Þröskuldur til að ákvarða að vél bregðist ekki við (mínútur)** er stilltur á tvær mínútur eða skemur. Lágmarksgildi er *2* (mínútur).
    - **Þröskuldur til að ákvarða að vél bregðist ekki við (mínútur)** – Fyrir hvert tilfang í hnitanetinu þar sem ekki á að nota sjálfgefinn þröskuld fyrir skal færa inn hnekkingargildi í þennan reit. Tilföng sem eru stillt á að nota þröskuld sem er tvær mínútur eða styttri munu nota stillinguna **Sjálfgefinn þröskuldur (mínútur)** í staðinn.

    > [!NOTE]
    > Yfirleitt er *hluti-út* merkið notað til að fylgjast með vélarstöðu. Því ættir þú að staðfesta að þröskuldurinn fyrir hvert tilfang vélar sé lengri en vélin þarf til að framleiða einn hluta.

1. Veljið **Næst**.
1. Á síðunni **Virkja skynjara**, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkja**. Fyrir hvern virkan skynjara í hnitanetinu birtist gátmerki í dálkinum **Virkur**.
1. Veljið **Ljúka**.

## <a name="work-with-the-machine-status-scenario"></a>Vinna með aðstæður fyrir vélarstöðu

Eftir að þú hefur sett upp skynjara og stillt aðstæður, getur þú skoðað viðburði vélarstöðu í Supply Chain Management. Þessi kafli lýsir því hvar og hvernig eigi að skoða þessar upplýsingar.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Skoða gögn vélarstöðu á síðu tilfangastöðu

Á síðunni **Staða tilfanga** geta eftirlitsaðilar fylgst með *hlutur-úti*-merkis sem tekið er við frá skynjurunum sem er varpað á hvert tilfang vélarinnar. Fylgja skal þessum skrefum til að skilgreina tímalínu.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Staða tilfanga**.
1. Í svarglugganum **Skilgreina** skal stilla eftirfarandi reiti:

    - **Tilfang** – Veldu tilföngin sem á að fylgjast með. (Ef þú ert að vinna með sýnigögnin skaltu velja *3118*).
    - **Tímaröð 1** – Veldu færslu (mælieiningarlykil) sem hefur eftirfarandi snið fyrir heiti sitt: *MachineReportingStatus:&lt;Sensor&gt;*
    - **Birtingarheiti** – Færðu inn *Merki um hluti út*.

Eftirfarandi mynd sýnir dæmi um gögn vélarstöðu á síðunni **Staða tilfanga** við hefðbundna vinnslu.

![Upplýsingar um stöðu vélar á síðu tilfangastöðu við hefðbundna vinnslu](media/sdi-resource-status-downtime-up.png "Gögn um vélarstöðu á síðu tilfangastöðu við hefðbundna vinnslu")

Eftirfarandi mynd sýnir dæmi um gögn um stöðu vélar þegar niðurtími er greindur.

![Upplýsingar um stöðu vélarinnar á síðunni Staða tilfanga þegar niðurtími greinist](media/sdi-resource-status-downtime-down.png "Upplýsingar um stöðu vélarinnar á síðunni Staða tilfanga þegar niðurtími greinist")

### <a name="view-machine-status-on-the-notifications-page"></a>Skoða stöðu vélar á tilkynningarsíðunni

Á síðunni **Tilkynningar** getur umsjónarmenn skoðað tilkynningar sem eru búnar til þegar of langur tími hefur liðið frá skynjarinn gaf síðast frá sér *hluti-út* merkið. Hver tilkynning veitir yfirlit yfir það framleiðsluverk sem verður fyrir áhrifum af stöðvun og gefur kost á að endurúthluta viðkomandi verki í annað tilfang.

Til að opna síðuna **Tilkynningar** ferðu í **Framleiðslustýring \> Fyrirspurnir og skýrslur \> Gervigreind skynjaragagna \> Tilkynningar**.

Eftirfarandi mynd sýnir dæmi um tilkynningu um vélarstöðu.

![Dæmi um stöðutilkynningu vélar](media/sdi-resource-status-downtime-notification.png "Dæmi um stöðutilkynningu vélar")
