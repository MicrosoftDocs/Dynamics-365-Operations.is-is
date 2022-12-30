---
title: Aðstæður fyrir vörugæði
description: Í þessari grein er að finna upplýsingar um aðstæður vörugæða. Þessar aðstæður notar skynjara til að mæla gæði vörurunu og býr til viðvörun ef mæling fer út fyrir skilgreind mörk.
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
ms.openlocfilehash: c0f1c57251234921779f67faf61d47cdde119e64
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690049"
---
# <a name="the-product-quality-scenario"></a>Aðstæður fyrir vörugæði

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Í aðstæðunum *vörugæði* er skynjari settur upp til að mæla gæði vörurunu í vinnusal. Ef mæling fer út fyrir skilgreind mörk fyrir vöruna er birtist tilkynning á stjórnborði umsjónarmanns. Til dæmis er skynjari að mæla raka matvöru sem kemur út úr framleiðslulínunni. Ef mælingin er utan leyfilegs lágmarks- eða hámarksgildis fyrir raka fyrir vöruna myndast tilkynning.

## <a name="scenario-dependencies"></a>Aðstæður tengsl

Aðstæðurnar *Gæði afurðar* eru háðar eftirfarandi:

- Viðvörun getur aðeins verið ræst ef framleiðslupöntun er keyrð á varpaðri vél og ef vélin framleiðir afurð sem er með varpaða runueigind.
- Merki sem stendur fyrir runueigindina verður að vera send til IoT-miðstöðvar og einkvæmt heiti eiginleika verður að fylgja.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Útbúa sýnigögn fyrir aðstæður vörugæða

Ef þú vilt nota sýnikerfi til að prófa aðstæður *vörugæði* skaltu nota kerfi þar sem [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) eru sett upp, velja lögaðilann (fyrirtæki) *USMF* og útbúa frekari sýnigögn eins og lýst er í þessum hluta. Ef þú notar eigin skynjara og gögn geturðu sleppt þessum hluta.

Í þessum hluta setur þú upp sýnigögnin þannig að þú getir notað losaða vöru *P0111* (*Samsett ver*) í aðstæðunum *vörugæði*. Í þessu aðstæðum rekur kerfið hvort gildi runueigindar sem er mældur af skynjara sé utan skilgreindra marka fyrir runueiginleika sem tengist vörunni.

### <a name="set-up-a-sensor-simulator"></a>Setja upp skynjarahermi

Ef þú vilt prófa þessar aðstæður án þess að nota efnislegan skynjara getur þú sett upp hermi til að búa til nauðsynleg merki. Frekari upplýsingar eru í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Tengja runueigind og tilfang við vöru P0111

Fylgdu þessum skrefum til að tengja eiginleika runu við vöru *P0111* (*Samsett koddaver*) og staðfesta að tilfang *3118* (*Svampskurðarvél*) sé notuð fyrir hana.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finnið og veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *P0111*.
1. Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Runueigindir**, velurðu **Tilgreint fyrir afurð**.
1. Á síðunni **Vörutengt** skal velja **Nýtt** til að búa til vörusértæka runueigind.
1. Stillið eftirfarandi reiti í hausnum:

    - **Eiginleikakóði** – Veldu umfang þeirra eiginleika sem þú munt fylgjast með (*Tafla*, *Hópur* eða *Allt*). Í þessum aðstæðum skaltu velja *Tafla*, því þú munt alltaf fylgjast með einum eiginleika.
    - **Tengsl eiginleika** – Veldu eiginleika sem þú notar við aðstæður *vörugæði* til að fylgjast með gildi vörugæða. Í þessu dæmi skaltu velja *Styrkur*, sem er eiginleiki sem er innifalinn í stöðluðum sýnigögnum.

1. Á flýtiflipa **Gildi** í reitunum **Lágmark** og **Hámark** skilgreinið svið ásættanlegra gilda sem eigindim verður að tilkynna til að standast gæðaeftirlit. Ef skynjarinn tilkynnir gildi utan þessa bils mun kerfið auðkenna það sem brot á gæðum. Aðrir reitir á þessum flýtiflipa eiga ekki við um aðstæðurnar *Vörugæði*. Sjálfgefin gildi sem þú sérð núna koma frá sýnigögnum. Því skaltu skilja þær eftir eins og þær eru, og loka síðunni **Vörutengt** til að fara aftur á síðuna **Upplýsingar um losaða afurð** fyrir vöru *P0111*.
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

### <a name="configure-the-production-floor-execution-interface"></a>Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi

Ef þú hefur ekki þegar gert það, stilltu þá viðmót fyrir framkvæmd á framleiðslugólfi til að sýna verk sem eru úthlutuð tilfangi *3118* (*Svampskurðarvél*). Frekari leiðbeiningar er að finna í eftirfarandi köflum:

- [Grunnstilla viðmót fyrir framkvæmd á framleiðslugólfi](sdi-scenario-equipment-downtime.md#config-pfe)
- [Virkja leitarvalkost á viðmót fyrir framkvæmd á framleiðslugólfi](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Ræsið fyrsta verk runupöntunina

Fylgið eftirfarandi skrefum til að hefja fyrsta verkið í runupöntuninni.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Framkvæmd á framleiðslugólfi**.
1. Í reitnum **Kortkenni** slærðu inn *123*. Veljið síðan **Innskráning**.
1. Þegar beðið er um ástæðu fjarveru skaltu velja eitt af spjöldunum fyrir fjarveru og velja svo **Í lagi**.
1. Í reitnum **Leita** er slegið inn lotunúmer pöntunar sem þú skrifaðir áður niður hjá þér. Veldu síðan **færslulykilinn**.
1. Smelltu á pöntunar og veldu síðan **Hefja vinnslu**.
1. Í svarglugganum **Hefja vinnslu** velurðu **Ræsa**.

## <a name="set-up-the-product-quality-scenario"></a>Setja upp aðstæður fyrir vörugæði

Fylgdu þessum skrefum til að setja *vörugæði* aðstæður í Supply Chain Management.

1. Farðu í **Framleiðslustýring \> Uppsetning \> Gervigreind skynjaragagna \> Aðstæður**.
1. Í aðstæðureitnum **Gæði vöru** skaltu velja **Stilla** til að opna lei fyrir þessar aðstæður.
1. Á síðunni **Skynjarar** skal velja **Nýtt** til að bæta skynjara við hnitanetið. Stillið svo eftirfarandi reiti fyrir það:

    - **Auðkenni skynjara** – Sláðu inn kenni skynjarans sem þú ert að nota. (Ef þú notar Raspberry PI Azure IoT Online Simulator og hefur sett það upp eins og lýst er í [Setja upp eftirlíkingarskynjara til prófunar](sdi-set-up-simulated-sensor.md), sláðu inn *Gæði*.)
    - **Lýsing á skynjara** – Færið inn lýsingu á skynjari.

1. Endurtaka á fyrra skref fyrir hvern skynjara sem þú vilt bæta við. Hægt er að koma aftur og bæta við fleiri skynjurum hvenær sem er.
1. Veljið **Næst**.
1. Á síðunni **Vörpun viðskiptafærslu**, í hlutanum **Skynjarar**, skaltu velja færslu fyrir einn af skynjurunum sem þú varst að bæta við.
1. Í hlutanum **Vörpun viðskiptafærslu** skal velja **Ný** til að bæta línu við hnitanetið.
1. Á nýju línunni ætti reiturinn **Gerð viðskiptafærslu** að vera sjálfkrafa að vera stilltur á *Tilföng(WrkCtrTable)*. Stilltu reitinn **Viðskiptafærsla** á tilfangið sem þú notar valinn skynjara til að fylgjast með. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla þau *á 3118, svampskurðarvél*.)
1. Strax og þú hefur valið gerð viðskiptafærslu fyrir línuna sem þú bættir við í fyrra þrepi er annarri línu sjálfkrafa bætt við hnitanetið. Á þessari línu ætti að stilla reitinn **Gerð viðskiptafærslu** á *Lotueiginleika(PdsBatchAttrib)*. Stilltu reitinn **Viðskiptafærsla** á runueigind sem þú notar valinn skynjara til að fylgjast með. (Ef þú notar sýnigögnin sem þú bjóst til fyrr í þessari grein skaltu stilla þau *Styrkur, prósentuhlutfall styrks*.)
1. Veljið **Næst**.
1. Á síðunni **Virkja skynjara**, í hnitanetinu, veldu skynjarann sem þú bættir við og veldu síðan **Virkja**. Fyrir hvern virkan skynjara í hnitanetinu birtist gátmerki í dálkinum **Virkur**.
1. Veljið **Ljúka**.

## <a name="work-with-the-product-quality-scenario"></a>Vinna með aðstæður fyrir vörugæði

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Skoða gögn um vörugæði á síðunni Staða tilfanga

Á síðunni **Staða tilfanga** geta eftirlitsaðilar fylgst með tímalínu merkis vörugæð sem tekið er við frá skynjurunum sem er varpað á hvert tilfang vélarinnar. Fylgja skal þessum skrefum til að skilgreina tímalínu.

1. Farið í **Framleiðslustýring \> Framkvæmd framleiðslu \> Staða tilfanga**.
1. Í svarglugganum **Skilgreina** skal stilla eftirfarandi reiti:

    - **Tilfang** – Veldu tilföngin sem á að fylgjast með. (Ef þú ert að vinna með sýnigögnin skaltu velja *3118*).
    - **Tímaröð 1** – Veldu færslu (mælieiningarlykil) sem hefur eftirfarandi snið fyrir heiti sitt: *ProductQuality:&lt;JobId&gt;:&lt;AttributeName&gt;*
    - **Birta nafn** – Sláðu inn *Gildi runueiginda*.

Eftirfarandi skýringarmynd sýnir dæmi um gögn um vörugæði á síðunni **Staða tilfanga** þegar gildið er á sviði ásættanleg gildi.

![Upplýsingar um gæði vöru á síðunni Tilfang þegar gildið er innan marka.](media/sdi-product-quality-in-range.png "Upplýsingar um gæði vöru á síðunni Tilfang þegar gildið er innan marka")

Eftirfarandi skýringarmynd sýnir dæmi um gögn um vörugæði þegar gildi utan sviðs er greint.

![Upplýsingar um gæði vöru á síðunni Staða tilfanga þegar utan sviðs gildi greinist.](media/sdi-product-quality-out-of-range.png "Upplýsingar um gæði vöru á síðunni Staða tilfanga þegar utan sviðs gildi greinist")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Skoða gögn um gæði vöru á Tilkynningarsíðunni

Á síðunni **Tilkynningar** geta umsjónarmenn skoðað tilkynninguna sem er búin til þegar skynjarinn mælir gildi runueigindar sem fellur utan skilgreindra þröskulda fyrir runueigindina. Hver tilkynning veitir yfirlit yfir það framleiðsluverk sem verður fyrir áhrifum af stöðvun og gefur kost á að endurúthluta viðkomandi verki í annað tilfang.

Til að opna síðuna **Tilkynningar** ferðu í **Framleiðslustýring \> Fyrirspurnir og skýrslur \> Gervigreind skynjaragagna \> Tilkynningar**.

Eftirfarandi skýringarmynd sýnir dæmi um tilkynning um gæði vöru.

![Dæmi um tilkynning um gæði vöru.](media/sdi-product-quality-notification.png "Dæmi um tilkynning um gæði vöru")
