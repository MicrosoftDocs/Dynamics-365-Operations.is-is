---
title: Skilgreina samstæðureglur sendingar
description: Þessi grein útskýrir hvernig á að setja upp sjálfgefna og sérsniðnar sameiningarstefnur fyrir sendingar.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427983"
---
# <a name="configure-shipment-consolidation-policies"></a>Skilgreina samstæðureglur sendingar

[!include [banner](../includes/banner.md)]

Samstæðuferli sendingar sem notar samstæðureglur sendingar leyfa sjálfvirka samstæðu sendingar við sjálfvirka og Handvirk losun í vöruhúsið. Eftir að kveikt er á þessum eiginleika verður að skilgreina fyrstu reglurnar. Ef engar reglur eru skilgreindar mun hver sölulína mynda aðskilda sendingu sem er með eina farmlínu.

Atburðarásirnar sem eru kynntar í þessari grein sýna hvernig á að setja upp sjálfgefna og sérsniðna samstæðustefnu fyrir sendingar.

> [!WARNING]
> Ef þú uppfærir Microsoft Dynamics 365 Supply Chain Management kerfi þar sem þú hefur notað eldri sendingarsamstæðueiginleikann, gæti sameining hætt að virka eins og þú býst við nema þú fylgir ráðleggingunum sem eru gefin hér.
>
> Um birgðakeðjustjórnunaruppsetningar þar sem *Samþjöppunarreglur sendingar* Slökkt er á eiginleikanum, þú virkjar sendingarsamstæðu með því að nota **Sameinaðu sendingu við losun á vöruhús** stilling fyrir hvert einstakt vöruhús. Þessi eiginleiki er nauðsynlegur frá og með útgáfu 10.0.29. Þegar kveikt er á henni mun **Sameinaðu sendingu við losun á vöruhús** stillingin verður falin og virkninni er skipt út fyrir *stefnur um samþjöppun sendinga* sem lýst er í þessari grein. Hver stefna setur samstæðureglur og inniheldur fyrirspurn til að stjórna hvar stefnan á við. Þegar þú kveikir á eiginleikanum fyrst verða engar stefnur um samþjöppun sendingar skilgreindar á **Samþjöppunarreglur sendingar** síðu. Þegar engar reglur eru skilgreindar notar kerfið arfgenga hegðun. Þess vegna heldur hvert núverandi vöruhús áfram að virða sína **Sameinaðu sendingu við losun á vöruhús** stilling, jafnvel þó að sú stilling sé nú falin. Hins vegar, eftir að þú hefur búið til að minnsta kosti eina stefnu fyrir samþjöppun sendingar, **Sameinaðu sendingu við losun á vöruhús** stillingar hafa ekki lengur nein áhrif og samstæðuvirkni er algjörlega stjórnað af reglunum.
>
> Eftir að þú hefur skilgreint að minnsta kosti eina sameiningarstefnu fyrir sendingar mun kerfið athuga sameiningarreglurnar í hvert sinn sem pöntun er losuð í vöruhúsið. Kerfið vinnur úr stefnum með því að nota röðun sem er skilgreind af hverri stefnu **Stefna röð** gildi. Það beitir fyrstu stefnu þar sem fyrirspurnin passar við nýju röðina. Ef engar fyrirspurnir passa við pöntunina myndar hver pöntunarlína sérstaka sendingu sem hefur eina hleðslulínu. Þess vegna mælum við með því að þú búir til sjálfgefna stefnu sem gildir fyrir öll vöruhús og hópa eftir pöntunarnúmeri. Gefðu þessari varastefnu hæstv **Stefna röð** gildi, þannig að það sé afgreitt síðast.
>
> Til að endurskapa eldri hegðun verður þú að búa til stefnu sem flokkar ekki eftir pöntunarnúmeri og hefur fyrirspurnarskilyrði sem innihalda öll viðeigandi vöruhús.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Kveikja á eiginleikanum „Samstæðureglur sendingar“

Til að nota *Samþjöppunarreglur sendingar* eiginleika, verður að vera kveikt á honum fyrir kerfið þitt. Frá og með Supply Chain Management útgáfu 10.0.29 er aðgerðin skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu sem er eldri en 10.0.29 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Samþjöppunarreglur sendingar* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a> Settu upp fyrstu sameiningarstefnurnar þínar

Ef þú ert að vinna með nýtt kerfi eða kerfi þar sem þú ert nýbúinn að kveikja á *Samþjöppunarreglur sendingar* eiginleiki í fyrsta skipti, fylgdu þessum skrefum til að setja upp upphafsreglur um samþjöppun sendingar.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu** til að stofna eftirfarandi reglur:

    - Stefna sem er nefnd *Sjálfgefið* fyrir *Sölupantanir* tegund stefnu.
    - Stefna sem er nefnd *Sjálfgefið* fyrir *Flutningamál* tegund stefnu.
    - Stefna sem er nefnd *CrossOrder* fyrir *Flutningamál* tegund stefnu. (Þessi regla er aðeins búin til ef þú varst með að minnsta kosti eitt vöruhús þar sem arfleifð **Sameinaðu sendingu við losun á vöruhús** stillingin var virkjuð.)
    - Stefna sem er nefnd *CrossOrder* fyrir *Sölupantanir* tegund stefnu. (Þessi regla er aðeins búin til ef þú varst með að minnsta kosti eitt vöruhús þar sem arfleifð **Sameinaðu sendingu við losun á vöruhús** stillingin var virkjuð.)

    > [!NOTE]
    > - Bæði *CrossOrder* stefnur líta á sama mengi sviða og fyrri rökfræði. Hins vegar taka þeir einnig tillit til pöntunarnúmerareitsins. (Þessi reitur er notaður til að sameina línur í sendingar, út frá þáttum eins og vöruhúsi, flutningsmáta afhendingar og aðsetri.)
    > - Bæði *Sjálfgefið* stefnur líta á sama mengi sviða og fyrri rökfræði. Hins vegar taka þeir einnig tillit til pöntunarnúmerareitsins. (Þessi reitur er notaður til að sameina línur í sendingar, út frá þáttum eins og pöntunarnúmeri, vöruhúsi, flutningsmáta afhendingar og aðsetri.)

1. Ef kerfið myndaði a *CrossOrder* stefnu fyrir *Sölupantanir* gerð stefnu, veldu hana og veldu síðan á aðgerðarrúðunni **Breyta fyrirspurn**. Í fyrirspurnaritlinum geturðu séð hvaða vöruhús þín eru **Sameinaðu sendingu við losun á vöruhús** stilling var áður virkjuð fyrir. Þess vegna endurskapar þessi regla fyrri stillingar þínar fyrir þessi vöruhús.
1. Sérsníddu nýju sjálfgefna reglurnar eftir þörfum með því að bæta við eða fjarlægja reiti og/eða breyta fyrirspurnum. Þú getur líka bætt við eins mörgum nýjum reglum og þú þarft. Fyrir dæmi sem sýna hvernig á að sérsníða og stilla reglur þínar, sjá dæmi atburðarás síðar í þessari grein.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Atburðarás: Stilltu sérsniðnar stefnur um samþjöppun sendingar

Þessi atburðarás gefur dæmi sem sýnir hvernig á að setja upp sérsniðnar sendingarsamstæðureglur og prófa þær síðan með því að nota kynningargögn. Sérsniðnar reglur geta stutt við flóknar viðskiptaþarfir þar sem sendingasamstæða ræðst af mismunandi skilyrðum. Stutt lýsing á viðskiptum fylgir með fyrir hvert dæmi um reglu síðar í þessum aðstæðum. Þessi dæmi um reglur ætti að setja upp í röð sem tryggir pýramídaskipulag á mati á fyrirspurnum. (Með öðrum orðum, þær reglur sem eru með flest skilyrði ættu að vera metnar með mestan forgang.)

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Þessi atburðarás vísar til gilda og skráa sem eru innifalin í staðlinum [kynningargögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) sem er veitt fyrir birgðakeðjustjórnun. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á *USMF* áður en hafist er handa.

### <a name="prepare-master-data-for-this-scenario"></a>Undirbúa aðalgögn fyrir þessa atburðarás

Áður en þú getur farið í gegnum æfingarnar í þessari atburðarás verður þú að undirbúa aðalgögnin sem þarf til að framkvæma síunina, eins og lýst er í eftirfarandi undirköflum. (Þessar forsendur eiga einnig við um aðstæðurnar sem eru skráðar í [Dæmi um hvernig á að nota samþjöppunarreglur fyrir sendingar](#example-scenarios) kafla.)

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
1. Lokaðu síðunni og endurtaktu síðan skref 4 og 5 fyrir viðskiptavininn sem hefur reikningsnúmerið *US-004*.

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
1. Veldu hnappinn **Bæta við** ![Hægri ör.](media/forward-button.png) til að færa reitinn í listann **Valdir reitir**.
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
1. Veldu hnappinn **Bæta við** ![Hægri ör.](media/forward-button.png) til að færa reitinn í listann **Valdir reitir**.
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
1. Veldu hnappinn **Bæta við** ![Hægri ör.](media/forward-button.png) til að færa reitinn í listann **Valdir reitir**.
1. Á listanum **Eftirstandandi reitir** skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veldu hnappinn **Bæta við** ![Hægri ör.](media/forward-button.png) til að færa reitinn í listann **Valdir reitir**.
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
1. Veldu hnappinn **Bæta við** ![Hægri ör.](media/forward-button.png) til að færa reitinn í listann **Valdir reitir**.
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

Venjulega er hægt að taka á þessu viðskiptatilviki með því að nota sjálfgefnar reglur sem þú bjóst til í [Settu upp fyrstu sameiningarstefnurnar þínar](#initial-policies). Hins vegar er einnig hægt að stofna svipaðar reglur handvirkt með því að fylgja þessum skrefum.

1. Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.
1. Stillið reitinn **Gerð stefnu** á *Sölupantanir*.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til reglu sem hefur eftirfarandi stillingar:

    - **Heiti reglu:** *Milli pantana*
    - **Lýsing á reglu:** *Samstæða á milli pantana fyrir tiltekin vöruhús*

1. Hafið valkostinn **Samstæða við opnar sendingar** stilltan á *Nei*.
1. Í aðgerðarúðunni skal velja **Vista**.
1. Á flýtiflipanum **Samstæðureitir**, í reitnum **Eftirstandandi reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stillt á *Flutningsmáti*.
1. Veldu hnappinn **Bæta við** ![Hægri ör.](media/forward-button.png) til að færa reitinn í listann **Valdir reitir**.
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

Eftirfarandi aðstæður sýna hvernig þú gætir notað samþjöppunarreglur sendingar sem þú bjóst til þegar þú lest þessa grein. Hverjar aðstæður fyrir sig leiða notanda í gegnum samstæðuferli sendingar sem notar samstæðureglur sendingar við sjálfvirka eða handvirka losun í vöruhúsið:

- Sviðsmynd 1: [sameina sendingar þegar þær eru losaðar í vöruhús með því að nota sjálfvirka losun sölupantana](../warehousing/consolidate-shipments-automatic.md)
- Sviðsmynd 2: [sameina sendingar þegar samstæðureglu sendingar hefur verið hnekkt á síðunni „Losa í vöruhús“](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- Sviðsmynd 3: [sameina sendingar með því að nota „Losa í vöruhús“ á vinnusvæði farmáætlunar](../warehousing/consolidate-shipments-load-planning-workbench.md)
- Sviðsmynd 4: [sameina sendingar með því að nota samstæðuvinnusvæði sendinga](../warehousing/consolidate-shipments-manual-workbench.md)
- Sviðsmynd 5: [sameina sendingar handvirkt með því að nota síðuna „Sameina sendingar“](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir stefnur um samþjöppun sendingar](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
