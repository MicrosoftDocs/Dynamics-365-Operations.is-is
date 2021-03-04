---
title: Skilgreina samstæðureglur sendingar
description: Þetta efnisatriði útskýrir hvernig á að setja upp sjálfgefnar og sérstilltar samstæðureglur sendingar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: adb88bbd29a89a1d18d7fd4781c2541ffb4e721f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430677"
---
# <a name="configure-shipment-consolidation-policies"></a>Skilgreina samstæðureglur sendingar

[!include [banner](../includes/banner.md)]

Samstæðuferli sendingar sem notar samstæðureglur sendingar leyfa sjálfvirka samstæðu sendingar við sjálfvirka og Handvirk losun í vöruhúsið. Eftir að kveikt er á þessum eiginleika verður að skilgreina fyrstu reglurnar. Ef engar reglur eru skilgreindar mun hver sölulína mynda aðskilda sendingu sem er með eina farmlínu.

Aðstæðurnar sem eru sýndar í þessu efnisatriði sýna hvernig setja á upp sjálfgefnar og sérsniðnar samstæðureglur sendingar.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Kveikja á eiginleikanum „Samstæðureglur sendingar“

> [!IMPORTANT]
> Í [fyrstu aðstæðunum](#scenario-1) sem lýst er í þessu efnisatriði er fyrst sett upp vöruhús til að það noti eldri samstæðueiginleika sendingar. Því næst eru samstæðureglur sendingar gerðar tiltækar. Á þennan hátt er hægt að læra á hvernig uppfærsluaðstæðurnar virka. Ef ætlunin er að nota sýnigagnaumhverfi til að fara í gegnum fyrstu aðstæðurnar skal ekki kveikja á eiginleikanum áður en farið er í gegnum aðstæðurnar.

Áður en hægt er að nota eiginleikann *Samstæðureglur sendingar* þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Sameina sendingu*

## <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Allar aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>Aðstæður 1: Skilgreina sjálfgefnar samstæðureglur sendingar

Tvenns konar ástand er til staðar þar sem skilgreina þarf lágmarksfjölda sjálfgefinna reglna eftir að kveikt er á eiginleikanum *Samstæðureglur sendingar*:

- Þú ert að uppfæra umhverfi sem inniheldur þegar gögn.
- Þú ert að setja upp algjörlega nýtt umhverfi.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Uppfæra umhverfi þar sem vöruhús hafa þegar verið skilgreind fyrir millipöntunarsamstæðu

Þegar þetta er ræst ætti að slökkva á eiginleikanum *Samstæðureglur sendingar* til að herma eftir umhverfi þar sem grunneiginleikinn fyrir millipöntunarsamstæðu var þegar notaður. Þá er eiginleikastjórnun notuð til að kveikja á eiginleikanum, svo hægt sé að fá upplýsingar um hvernig setja á upp samstæðureglur sendingar eftir uppfærsluna.

Fylgið eftirfarandi skrefum til að setja upp sjálfgefnar samstæðureglur sendingar í umhverfi þar sem vöruhús hafa þegar verið skilgreind fyrir millipöntunarsamstæðu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Á listanum skal finna og opna viðkomandi vöruhúsafærslu (til dæmis, vöruhús *24* í **USMF**-sýnigögnum).
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á flýtiflipanum **Vöruhús** skal stilla valkostinn **Taka sendingu með í samstæðu við losun í vörugeymslu** á *Já*.
1. Endurtakið skref 2 til 4 fyrir öll önnur vöruhús þar sem sameining er nauðsynleg.
1. Lokið síðunni.
1. Notaðu [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum *Samstæðureglum sendingar*. Á vinnusvæðinu **Eiginleikastjórnun** kallst eiginleikinn *Sameina sendingu*.
1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**. Hugsanlega þarf að uppfæra vafrann til að sjá nýja valmyndaratriðið **Samstæðureglur sendingar** eftir að kveikt er á eiginleikanum.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu** til að stofna eftirfarandi reglur:

    - **CrossOrder**-regla fyrir reglugerðina *Sölupantanir* (að því gefnu að a.m.k. eitt vöruhús sé sett upp til að nota sem eldri samstæðueiginleikann)
    - **Sjálfgefið**-regla fyrir reglugerðina *Sölupantanirnar*
    - **Sjálfgefið**-regla fyrir reglugerðina *Flutningsútgáfa*
    - **CrossOrder**-regla fyrir reglugerðina *Flutningsútgáfa* (að því gefnu að a.m.k. eitt vöruhús sé sett upp til að nota eldri samstæðueiginleikann)

    > [!NOTE]
    > - Báðar **CrossOrder**-reglur nota saman reitahóp sem eldri rök, fyrir utan reitinn fyrir pöntunarnúmerið. (Þessi reitur er notaður til að sameina línur í sendingar, út frá þáttum eins og vöruhúsi, flutningsmáta afhendingar og aðsetri.)
    > - Báðar **Sjálfgefið**-reglur nota saman reitahóp sem eldri rök, einnig reitinn fyrir pöntunarnúmerið. (Þessi reitur er notaður til að sameina línur í sendingar, út frá þáttum eins og pöntunarnúmeri, vöruhúsi, flutningsmáta afhendingar og aðsetri.)

1. Velja skal **CrossOrder**-reglu fyrir reglugerðina *Sölupantanir* og síðan skal velja **Breyta fyrirspurn** á aðgerðasvæðinu.
1. Í svarglugga fyrirspurnaritilsins skal gefa gaum að því að skráð eru vöruhús sem hafa valkostinn **Taka sendingu með í samstæðu við losun í vörugeymslu** stilltan á *Já*. Þess vegna eru þau höfð með í fyrirspurninni.

### <a name="create-default-policies-for-a-new-environment"></a>Stofna sjálfgefnar reglur fyrir nýtt umhverfi

Fylgið eftirfarandi skrefum til að setja upp sjálfgefnar samstæðureglur sendingar í glænýju umhverfi.

1. Notið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum *Samstæðureglur sendingar*, ef ekki er þegar kveikt á honum. Á vinnusvæðinu **Eiginleikastjórnun** kallst eiginleikinn *Sameina sendingu*.
1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu** til að stofna eftirfarandi reglur:

    - **Sjálfgefið**-regla fyrir reglugerðina *Sölupantanirnar*
    - **Sjálfgefið**-regla fyrir reglugerðina *Flutningsútgáfa*

    > [!NOTE]
    > Báðar **Sjálfgefið**-reglur nota saman reitahóp sem eldri rök, einnig reitinn fyrir pöntunarnúmerið. (Þessi reitur er notaður til að sameina línur í sendingar, út frá þáttum eins og pöntunarnúmeri, vöruhúsi, flutningsmáta afhendingar og aðsetri.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>Aðstæður 2: Skilgreina sérsniðna samstæðureglu sendingar

Þessar aðstæður sýna hvernig setja á upp sérsniðna samstæðureglu sendingar. Sérsniðnar reglur geta stutt við flóknar viðskiptaþarfir þar sem sendingasamstæða ræðst af mismunandi skilyrðum. Stutt lýsing á viðskiptum fylgir með fyrir hvert dæmi um reglu síðar í þessum aðstæðum. Þessi dæmi um reglur ætti að setja upp í röð sem tryggir pýramídaskipulag á mati á fyrirspurnum. (Með öðrum orðum, þær reglur sem eru með flest skilyrði ættu að vera metnar með mestan forgang.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Kveikja á eiginleika og undirbúa aðalgögn fyrir þessar aðstæður

Áður en hægt er að fara í gegnum æfingarnar í þessum aðstæðum þarf að kveikja á eiginleikanum og undirbúa aðalgögnin sem eru nauðsynleg fyrir síuna, eins og lýst er í eftirfarandi undirköflum. (Þessi skilyrði eiga einnig við um aðstæður sem taldar eru upp í [Dæmi um hvernig nota á samstæðureglur sendingar](#example-scenarios).)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Kveikja á eiginleikanum og stofna sjálfgefnar reglur

Nota skal eiginleikastjórnun til að virkja eiginleikann, ef ekki hefur þegar verið kveikt á honum, og stofna sjálfgefnar samstæðureglur sem lýst er í [aðstæðum 1](#scenario-1).

#### <a name="create-two-new-product-filter-codes"></a>Búa til tvo nýja afurðasíukóða

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Afurðasíur \> Afurðarsíur** og bætið við tveimur afurðasíum:

    - Afurðasía 1:

        - **Síukóði:** *Eldfimt*
        - **Síuheiti:** *Kóði 4*

    - Afurðasía 2:

        - **Síukóði:** *Sprengifimt*
        - **Síuheiti:** *Kóði 4*

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opnið afurðina með vörunúmerið *M9200*. (Afurðin sem valin er verður að vera virk fyrir ítarlegt ferli \[vöruhúsakerfis\] og þessi afurð er forvirk fyrir vöruhúsakerfisferli í **USMF**-sýnigögnunum.)
1. Á flýtiflipanum **Vöruhús** skal stilla reitinn **Kóði 4** á *Eldfimt*.
1. Lokið síðunni.
1. Opnið afurðina með vörunúmerið *M9201*. (Þessi vara er einnig forvirk fyrir vöruhúsakerfisferla í **USMF**-sýnigögnunum.)
1. Á flýtiflipanum **Vöruhús** skal stilla reitinn **Kóði 4** á *Sprengifimt*.
1. Lokið síðunni.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Stofna nýjan flutningsmáta afhendingar

1. Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Máti**.
1. Stofnið flutningsmáta sem verður notaður í samstæðufyrirspurnum og gefið honum heitið *Flugfélög*.
1. Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Farmflytjendur**.
1. Stofna flutningsaðila sem er með eftirfarandi stillingar:

    - **Farmflytjandi:** *Flugfélög*
    - **Heiti:** *Flugfélög*
    - **Máti:** *Flugfélög*

1. Á flýtiflipanum **Þjónusta** fyrir nýja flutningsaðilann skal bæta við línu sem er með eftirfarandi stillingar:

    - **Flutningsþjónusta:** *flug*
    - **Flutningsaðferð:** *flug*

1. Í aðgerðarúðunni skal velja **Vista**.

    > [!NOTE]
    > Þegar nýr flutningsaðili er vistaður er reiturinn **Flutningsmáti** fyrir nýju línuna í hnitanetinu **Þjónusta** sjálfkrafa stilltur á *Airwa-Air*. Þegar notast er við flutningsmátann *Airwa-Air* fyrir sölupöntun er flutningsmátinn *Flugfélög* notaður fyrir tengdar sendingar.

#### <a name="create-an-order-pool"></a>Búa til pöntunarsett

1. Opnið **Sala og markaðssetning \> Uppsetning \> Sölupantanir \> Pöntunarsett**.
1. Stofnið pöntunarsett sem verður notað fyrir samstæðufyrirspurn. Þetta pöntunarsett ætti að hafa eftirfarandi stillingar:

    - **Hópur:** Færið inn heiltölu sem ekki er þegar í notkun í öðrum hópi.
    - **Heiti:** *ShipCons*

1. Opnið **Sölu og markaðssetning \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Opnið viðskiptavininn sem er með lykilnúmer *US-003*.
1. Á flýtiflipanum **Sjálfgildi sölupantana** skal stilla reitinn **Sölupantanahópur** á nýstofnaða pantanahópinn.
1. Lokið síðunni og endurtakið síðan skref 4 og 5 fyrir viðskiptavininn sem er með lykilnúmer *US-004*.

### <a name="create-example-policy-1"></a>Búa til dæmastefnu 1

Í þessu dæmi er reglan *Viðskiptavinum+Máti* búin til, sem hægt er að nota fyrir eftirfarandi viðskiptatilvik:

- Reglan mun leita að tilteknum viðskiptavinalykli (*US-001*) og tilteknum flutningsmáta (*Airwa-Air*).
- Slökkt er á „Samstæða við opnar sendingar“.
- Samstæða er gerð fyrir hvert pöntunarauðkenni. (Með öðrum orðum eru aðskildar sendingar til staðar fyrir hverja pöntun, vöruhús o.s.frv.)

Fylgið eftirfarandi skrefum til að stofna samstæðureglu sendingar fyrir þetta viðskiptatilvik.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til reglu sem hefur eftirfarandi stillingar:

    - **Heiti reglu:** *CustomerMode*
    - **Lýsing á reglu:** *Viðskiptavinalykill og flutningsmáti*

1. Hafið valkostinn **Samstæða við opnar sendingar** stilltan á *Nei*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á flýtiflipanum **Samstæðureitir**, á listanum **Eftirstandandi reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veljið **Bæta við**-hnappinn ![Hægri ör ](media/forward-button.png) til að færa reitinn á listann **Valdir reitir**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritilsins, á flipanum **Svið** , á hnitanetinu, skal finna línuna þar sem reiturinn **Reitur** er stilltur á *Viðskiptamannalykill* og stilla reitinn **Skilyrði** fyrir þá línu á *US-001*.
1. Veljið **Bæta við** til að bæta við línu sem er með eftirfarandi stillingar í hnitanetinu:

    - **Tafla:** *Pantanalínur*
    - **Afleidd tafla:** *Pöntunarlínur*
    - **Reitur:** *Afhendingarmáti*
    - **Skilyrði:** *Airwa-Air*

1. Veldu **Í lagi** til að loka svarglugganum.

> [!NOTE]
> Fyrir þetta viðskiptatilvik eru pöntunarlínur fyrir viðskiptavin *US-001* sem nota flutningsmátann *Airwa-Air* ekki sameinaðar á milli pantana. Þessari reglu er ætlað að vera notuð fyrst í röð, í þeim tilvikum þar sem sendingar fyrir alla aðra flutningsmáta eru sameinaðar fyrir þennan viðskiptavin.

### <a name="create-example-policy-2"></a>Búa til dæmastefnu 2

Í þessu dæmi er reglan *Hættulegar vörur* búin til, sem hægt er að nota fyrir eftirfarandi viðskiptatilvik:

- Reglan mun leita að tilteknum síukóða (*hættulegt*) og tilteknum flutningsmáta (*Airwa-Air*).
- Kveikt er á „Samstæða við opnar sendingar“.
- Samstæða er þvert á pantanir. (Með öðrum orðum verða aðskildar sendingar fyrir hvern lykil, vöruhús o.s.frv., en aðeins innan vöruflokksins sem tilgreindur er í fyrirspurninni.)

Fylgið eftirfarandi skrefum til að stofna samstæðureglu sendingar fyrir þetta viðskiptatilvik.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til reglu sem hefur eftirfarandi stillingar:

    - **Heiti reglu:** *Vörugerð*
    - **Lýsing á reglu:** *Sameina sömu gerð vöru á milli pantana*

1. Stillið valkostinn **Sameina við opnar sendingar** á *Já*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á flýtiflipanum **Samstæðureitir**, á listanum **Eftirstandandi reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veljið **Bæta við**-hnappinn ![Hægri ör ](media/forward-button.png) til að færa reitinn á listann **Valdir reitir**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritilsins, á flipanum **Samtengingar** , skal stækka og velja **Töflur \> Upplýsingar um hleðslu** á trénu.
1. Velja **Bæta við töflusamtengingu**.
1. Á hnitaneti tengsla sem birtist er hægt að finna og velja línuna þar sem reiturinn **Tengsl** er stilltur á *Vörunúmer í vöruhúsi* og síðan velja **Velja**. 
1. Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Vörunúmer í vöruhúsi*
    - **Afleidd tafla:** *Vörunúmer í vöruhúsi*
    - **Svæði:** *kóði 4*
    - **Skilyrði:** *Eldfimt*

1. Veldu **Í lagi** til að loka svarglugganum.

> [!NOTE]
> Fyrir þetta viðskiptatilvik eru allar pöntunarlínur þar sem vörur hafa tiltekinn síukóða (þ.e. síukóðann þar sem reiturinn **Kóði 4** er stilltur á *Eldfimt*) sameinaður við aðrar vörur af sömu gerð á milli pantana. Ef opin sending er til staðar fyrir sama lykil, vöruhús og vöruflokk verða nýju línurnar hengdar við hana.

### <a name="create-example-policy-3"></a>Búa til dæmareglu 3

Í þessu dæmi er reglan *Kröfur viðskiptavinar* búin til, sem hægt er að nota fyrir eftirfarandi viðskiptatilvik:

- Reglan mun leita að tilteknum viðskiptavinalykli.
- Kveikt er á „Samstæða við opnar sendingar“.
- Samstæða er yfir allar pantanir en byggist á beiðnum viðskiptavinar. (Með öðrum orðum eru margar pantanir flokkaðar í sendingar, byggtá sama beiðninúmeri viðskiptavinar og vöruhúsi.)

Fylgið eftirfarandi skrefum til að stofna samstæðureglu sendingar fyrir þetta viðskiptatilvik.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til reglu sem hefur eftirfarandi stillingar:

    - **Heiti reglu:** *CustomerOrderNo*
    - **Lýsing á reglu:** *Sameina línur út frá innkaupapöntun viðskiptavinar*

1. Stillið valkostinn **Sameina við opnar sendingar** á *Já*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á flýtiflipanum **Samstæðureitir**, á listanum **Eftirstandandi reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Beiðni viðskiptavinar*.
1. Veljið **Bæta við**-hnappinn ![Hægri ör ](media/forward-button.png) til að færa reitinn á listann **Valdir reitir**.
1. Á listanum **Eftirstandandi reitir** skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veljið **Bæta við**-hnappinn ![Hægri ör ](media/forward-button.png) til að færa reitinn á listann **Valdir reitir**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritilsins, á flipanum **Svið** skal finna línuna þar sem reiturinn **Reitur** er stilltur á *Viðskiptamannalykill* og stilla reitinn **Skilyrði** fyrir þá línu á *US-001*.
1. Veldu **Í lagi** til að loka svarglugganum.

> [!NOTE]
> Fyrir þetta viðskiptatilvik eru allar pöntunarlínur þar sem sölupantanir hafa sama beiðninúmer viðskiptavinar sameinaðar í eina sendingu, óháð sölupöntunarnúmerinu. (Beiðninúmer viðskiptavinarins er notað sem númer innkaupapöntun viðskiptavinarins, \[Innkaupapöntun\].) Ef opin sending er til staðar fyrir sama lykil, vöruhús og vöruflokk verða nýju línurnar hengdar við hana. Hægt er að nota þessa reglu ef viðskiptavinurinn sendir fleiri pöntunarlínur sem hafa sama innkaupanúmer nokkrum sinnum sama dag og vill að allar línurnar verðir flokkaðar í eina sendingu. (Með öðrum orðum er eingöngu þörf á einu farmbréfi og einum fylgiseðli.)

### <a name="create-example-policy-4"></a>Búa til dæmastefnu 4

Í þessu dæmi er reglan *Viðskiptavinir sem leyfa samstæðu* búin til, sem hægt er að nota fyrir eftirfarandi viðskiptatilvik:

- Reglan mun leita tilteknu pöntunarsetti til að auðkenna viðskiptavini sem samþykkja sameinaðar sendingar.
- Slökkt er á „Samstæða við opnar sendingar“.
- Samstæða er gerð yfir allar pantanir með því að nota reitina sem valdir eru með sjálfgefnu CrossOrder-reglunni (til að endurtaka fyrri gátreitinn **Sameina sendingar við losun í vöruhús**).

- Hægt er að hnekkja reglunni á sölupöntun með því að velja annan pöntunarsett.

Fylgið eftirfarandi skrefum til að stofna samstæðureglu sendingar fyrir þetta viðskiptatilvik.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til reglu sem hefur eftirfarandi stillingar:

    - **Heiti reglu:** *Pöntunarsett*
    - **Lýsing á reglu:** *Samstæða milli pantana sem byggð er á pöntunarsetti*

1. Hafið valkostinn **Samstæða við opnar sendingar** stilltan á *Nei*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á flýtiflipanum **Samstæðureitir**, á listanum **Eftirstandandi reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veljið **Bæta við**-hnappinn ![Hægri ör ](media/forward-button.png) til að færa reitinn á listann **Valdir reitir**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils á flipanum **Svið** skal velja **Bæta við** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Sölupantanir*
    - **Afleidd tafla:** *Sölupantanir*
    - **Reitur:** *Sett*
    - **Skilyrði:** *ShipCons*

1. Veldu **Í lagi** til að loka svarglugganum.

> [!NOTE]
> Fyrir þetta viðskiptatilvik eru allar pöntunarlínur þar sem sölupantanir tilheyra sömu pöntunarsetti sameinaðar í eina sendingu á milli sölupantana fyrir sama lykil, vöruhús og flutningsmáta afhendingar. Í stað pöntunarsetts er hægt að nota hvaða annan reit sem er til að aðgreina hóp viðskiptavina og nota sölupöntunarhausinn sjálfgefið. Hægt er að nota þessa aðferð ef viðskiptavinurinn, ekki vöruhúsið, er að keyra þörfina fyrir sameiningu. (Í eldri samstæðurökunum keyrði vöruhúsið þörfinni fyrir sameiningu.)

### <a name="create-example-policy-5"></a>Búa til dæmastefnu 5

Í þessu dæmi er reglan *Vöruhús sem leyfa samstæðu* búin til, sem hægt er að nota fyrir eftirfarandi viðskiptatilvik:

- Reglan mun leita tilteknu pöntunarsetti til að auðkenna vöruhús sem geta sameinað sendingar.
- Slökkt er á „Samstæða við opnar sendingar“.
- Samstæða er gerð yfir allar pantanir með því að nota reitina sem valdir eru með sjálfgefnu CrossOrder-reglunni (til að endurtaka fyrri gátreitinn **Sameina sendingar við losun í vöruhús**).

Yfirleitt er hægt að vinna þetta viðskiptatilvik með því að nota sjálfgefnu reglurnar sem voru stofnaðar í [aðstæðum 1](#scenario-1). Hins vegar er einnig hægt að stofna svipaðar reglur handvirkt með því að fylgja þessum skrefum.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til reglu sem hefur eftirfarandi stillingar:

    - **Heiti reglu:** *Milli pantana*
    - **Lýsing á reglu:** *Samstæða á milli pantana fyrir tiltekin vöruhús*

1. Hafið valkostinn **Samstæða við opnar sendingar** stilltan á *Nei*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á flýtiflipanum **Samstæðureitir**, í reitnum **Eftirstandandi reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veljið **Bæta við**-hnappinn ![Hægri ör ](media/forward-button.png) til að færa reitinn á listann **Valdir reitir**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritilsins, á flipanum **Svið** skal finna línuna þar sem reiturinn **Reitur** er stilltur á *Vöruhús* og stilla reitinn **Skilyrði** fyrir þá línu á *61, 63*.
1. Veldu **Í lagi** til að loka svarglugganum.

### <a name="set-the-order"></a>Stilla röð

Nú þegar búið er að stofna allar reglurnar þarf að stofna pöntunina sem þær verða notaðar í. Til að nota pýramídanálgun, þar sem reglur með flest skilyrði hafa mestan forgang, skal fylgja þessum skrefum.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Veljið hverja reglu sem er skráð í vinstri dálknum og notið síðan hnappana **Færa upp** og **Færa niður** á aðgerðasvæðinu til að raða reglunum í eftirfarandi röð:

    1. CustomerMode
    1. Gerð vöru
    1. CustomerOrderNo
    1. Pöntunarsett
    1. Á milli pantana
    1. Sjálfgefinn

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Dæmi um hvernig nota á samstæðureglur sendingar

Eftirfarandi aðstæður sýna hvernig hægt er að nota samstæðureglur sendingar sem voru stofnaðar þegar þetta efnisatriði var lesið. Hverjar aðstæður fyrir sig leiða notanda í gegnum samstæðuferli sendingar sem notar samstæðureglur sendingar við sjálfvirka eða handvirka losun í vöruhúsið:

- Sviðsmynd 1: [sameina sendingar þegar þær eru losaðar í vöruhús með því að nota sjálfvirka losun sölupantana](../warehousing/consolidate-shipments-automatic.md)
- Sviðsmynd 2: [sameina sendingar þegar samstæðureglu sendingar hefur verið hnekkt á síðunni „Losa í vöruhús“](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Sviðsmynd 3: [sameina sendingar með því að nota „Losa í vöruhús“ á vinnusvæði farmáætlunar](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Sviðsmynd 4: [sameina sendingar með því að nota samstæðuvinnusvæði sendinga](../warehousing/consolidate-shipments-manual-workbench.md)
- Sviðsmynd 5: [sameina sendingar handvirkt með því að nota síðuna „Sameina sendingar“](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Frekari upplýsingar

- [Samstæðureglur sendingar](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]