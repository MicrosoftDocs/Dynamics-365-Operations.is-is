---
title: Afrita svæði fyrir rafræn viðskipti
description: Þessi grein lýsir því hvernig á að afrita núverandi netverslunarsíðu innan eða á milli rafrænna viðskiptaumhverfa í Microsoft Dynamics 365 Commerce vefsmiður.
author: josaw1
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 9b74e0d48be29272b893c855c229e4003f0c161e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276293"
---
# <a name="copy-an-e-commerce-site"></a>Afrita svæði fyrir rafræn viðskipti

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að afrita núverandi netverslunarsíðu innan eða á milli rafrænna viðskiptaumhverfa í Microsoft Dynamics 365 Commerce vefsmiður.

Dynamics 365 Commerce styður afritun eða klónun vefsvæða sem sjálfsafgreiðsluaðgerð í Commerce site builder. Hægt er að afrita síður innan eins rafrænnar viðskiptaumhverfis eða á milli tveggja rafrænna viðskiptaumhverfa. Notandinn sem setur afritunaraðgerðina af stað verður að vera leigjandastjórnandi bæði í uppruna- og áfangastað rafrænna viðskiptaumhverfisins.

Afritunaraðgerð vefsvæðisins afritar allt rafræn verslunarefni upprunasíðunnar. Þetta efni inniheldur síður, brot, sniðmát, vefslóðir og eignir. Áður en hægt er að nota nýja síðu verður að frumstilla hana með fyrstu keyrsluupplifun (FRE) ferli. Hægt er að kortleggja rásir og hafa umsjón með þeim í Site builder, á **Vefstillingar \> Rásir**.

Lengd afritunaraðgerðarinnar fer fyrst og fremst eftir fjölda eigna á upprunasíðunni. Fyrir einstaklega stórar síður mælum við með því að þú íhugir að nota umhverfisafritunaraðgerðina í staðinn. (Þessi aðgerð er einnig þekkt sem gagnaflutningsaðgerðin).

> [!NOTE]
> - Upprunasíðan verður skrifvarinn meðan afritunaraðgerðin stendur yfir.
> - Aðeins birtar útgáfur af skjölum eru afritaðar. Ef engar útgáfur hafa verið birtar eru aðeins nýjustu útgáfurnar afritaðar.
> - Útgáfuferill fyrir efni verður ekki tiltækur á áfangasíðunni.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Afritaðu síðu í rafrænu viðskiptaumhverfi

Til að afrita síðu innan rafræns viðskiptaumhverfis skaltu fylgja þessum skrefum.

1. Skráðu þig inn á vefsvæðisgerðina fyrir umhverfið þar sem þú vilt framkvæma afritunaraðgerðina.
1. Opnaðu lista yfir vefsvæði með því að velja **Vefskiptaskipti** í efra hægra horninu og veldu síðan **Stjórna síðum**.
1. Finndu síðuna sem þú vilt afrita eða klóna og veldu hana með því að velja gátreitinn við hliðina á síðuheitinu.
1. Veldu á skipanastikunni **Afritaðu síðuna**.
1. Í **Afritaðu síðuna** fljúgandi valmynd, í **Nýtt nafn síðunnar** reit, sláðu inn nafn fyrir nýju síðuna. Nýja síðuheitið verður að vera einstakt í rafrænu viðskiptaumhverfinu. The **Heimild leigjandi** og **Heimildasíða** reitir eru sjálfkrafa stilltir á upplýsingarnar fyrir núverandi leigjanda og valda síðu.
1. Veldu **Búðu til afrit**.

Eftir að upplýsingarnar hafa verið staðfestar gefur tilkynning til kynna að nýtt vefafritunarstarf hafi verið búið til. Hægt er að fylgjast með framvindu starfsins í [hægri rúðu á **Störf leigjanda** síðu](#monitor-the-site-copy-operation). Þegar afritunaraðgerðinni hefur verið lokið birtist nýja vefsíðan á listanum yfir vefsvæði í veflistaskjánum.

Eftirfarandi mynd sýnir dæmi um **Afritaðu síðuna** útfallsvalmynd í vefsmiði.

![Afritaðu valmynd síðunnar í síðugerð.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Afritaðu síðu á milli tveggja rafrænna viðskiptaumhverfa

Til að afrita síðu á milli tveggja rafrænna viðskiptaumhverfa skaltu fylgja þessum skrefum.

1. Skráðu þig inn á vefsíðugerð fyrir netviðskiptaumhverfi áfangastaðarins.
1. Veldu á skipanastikunni **Afritaðu síðuna**.
1. Í **Afritaðu síðuna** fljúgandi valmynd, í **Nýtt nafn síðunnar** reit, sláðu inn nafn fyrir nýju síðuna. Nýja síðuheitið verður að vera einstakt í rafrænu viðskiptaumhverfinu.
1. Í **Heimild leigjandi** reit, veldu nafn upprunaleiganda.
1. Í **Heimildasíða** reit, veldu upprunasíðuna.
1. Veldu **Búðu til afrit**.

> [!NOTE]
> Heimildir leigjanda stjórnanda eru nauðsynlegar fyrir bæði uppruna- og áfangastað rafræn viðskipti.

Eftir að upplýsingarnar hafa verið staðfestar gefur tilkynning til kynna að nýtt vefafritunarstarf hafi verið búið til. Hægt er að fylgjast með framvindu starfsins í [hægri rúðu á **Störf leigjanda** síðu](#monitor-the-site-copy-operation). Þegar afritunaraðgerðinni hefur verið lokið birtist nýja vefsíðan á listanum yfir vefsvæði í veflistaskjánum.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Kortarásir meðan á afritunaraðgerð stendur (valfrjálst)

Hægt er að kortleggja upprunarásir og staðsetningar við áfangarásir og staðsetningar sem hluta af afritunaraðgerðinni. Ef kortlagning rásarinnar er gerð sem hluti af afritunaraðgerðinni er ekki krafist að frumstilla síðuna með FRE ferlinu og stilla rásirnar í síðustillingum. 

Fylgdu þessum skrefum til að kortleggja allar rásir og staðsetningar „eins og þær eru“ (1-til-1) í vefsvæðisgerð.

1. Opnaðu lista yfir vefsvæði með því að velja **Vefskiptaskipti** í efra hægra horninu og veldu síðan **Stjórna síðum**.
1. Finndu síðuna sem þú vilt afrita eða klóna og veldu hana með því að velja gátreitinn við hliðina á síðuheitinu.
1. Veldu á skipanastikunni **Afritaðu síðuna**.
1. Í **Afritaðu síðuna** útvalmynd, sláðu inn gildi fyrir **Nýtt nafn síðunnar**, **leigjandi**, og **Heimildasíða** (ef ekki þegar til staðar).
1. Veldu **Bættu við rásakortum**.
1. Í **Stilltu vefrásir og staðsetningar** valmynd, veldu **Upprunarás**, og veldu síðan upprunarásina.  
1. Veldu **Áfangarrás** og veldu síðan sömu rás og upprunarásina. 
1. Veldu **Bæta við staðbundnum stað**.
1. Veldu **Heimildarstaður**, og veldu síðan upprunastaðinn.
1. Veldu **Áfangastaður**, og veldu síðan sama stað og upprunastaðinn. 
1. Fyrir **URL slóð**, sláðu inn einstaka vefslóð sem er ekki notuð í áfangaumhverfinu.
1. Endurtaktu skref 8-11 fyrir hvern stað sem á að kortleggja fyrir rásina.
1. Veljið **Bæta við**.
1. Endurtaktu skref 6-11 fyrir hverja upprunarás.
1. Veljið **Loka**.
1. Skoðaðu uppsetninguna fyrir nákvæmni og veldu síðan **Afritaðu síðuna**.

> [!NOTE]
> Allar upprunarásir og staðsetningar verða að kortleggja og aðeins er hægt að kortleggja þær einu sinni.

## <a name="monitor-the-site-copy-operation"></a>Fylgstu með afritunaraðgerðinni

Til að fylgjast með framvindu afritunaraðgerðarinnar skaltu fylgja þessum skrefum.

1. Skráðu þig inn á vefsíðugerð fyrir netviðskiptaumhverfi áfangastaðarins.
1. Í vinstri glugganum velurðu **Störf leigjanda**.
1. Á **Störf leigjanda** síðu, finndu og veldu síðuafritunarstarfið á listanum. Gluggi birtist hægra megin og sýnir stöðu og upplýsingar um valið starf.

Hægt er að hætta við starf sem hefur stöðuna **Í vinnslu**. Veldu starfið á listanum og veldu síðan **Hætta við** á skipanastikunni.

Þú getur prófað aftur starf sem hefur stöðuna **Mistókst** eða **Lokið með villum**. Veldu starfið á listanum og veldu síðan **Reyndu aftur** á skipanastikunni.

> [!NOTE]
> Vinnsla myndbandaeigna gæti haldið áfram eftir að afritunarvinnu er lokið.

Eftirfarandi mynd sýnir dæmi um hægri gluggann á **Störf leigjanda** síðu í Site builder.

![Upplýsingar um starf í hægra rúðunni á síðunni Leigjandastörf í vefsmiði.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Frumstilla nýja síðu með því að nota FRE ferlið

Áður en hægt er að nota nýja síðuna verður að frumstilla hana með FRE ferlinu.

Til að frumstilla nýja síðu með því að nota FRE ferlið skaltu fylgja þessum skrefum.

1. Skráðu þig inn á síðugerðarmann fyrir nýju síðuna.
1. Opnaðu lista yfir vefsvæði með því að velja **Vefskiptaskipti** í efra hægra horninu og veldu síðan **Stjórna síðum**.
1. Finndu og veldu nýju síðuna sem þú vilt frumstilla.
1. Í **Settu upp síðuna þína** valmynd, í **Veldu lén** reit, veldu lén. Öll lén sem tengdust rafrænu viðskiptaumhverfinu við frumstillingu eru tiltæk fyrir val.
1. Í **Veldu sjálfgefna rás** reit, veldu tengda netverslunarrás. Valin rás mun veita úrval og aðrar upplýsingar sem eru geymdar í höfuðstöðvum Commerce.
1. Í **Veldu sjálfgefið tungumál** reit, veldu sjálfgefið höfundartungumál. Öll tungumál sem voru stillt fyrir valda netverslunarrás er hægt að velja.
1. Í **Leið** reitinn samanstendur gildið af grunnléninu og valfrjálsri vefslóð sem þú getur slegið inn. Þú getur skilið slóðina eftir auða ef rásin verður þjónustað frá lénsrótinni, eða ef þú vilt slá inn þessar upplýsingar síðar í rásarstillingarskjánum í vefsvæðisgerðinni. Slóðin verður að vera einstök í rafrænu viðskiptaumhverfinu.
1. Veldu **Í lagi**. Síðan er frumstillt með þeim upplýsingum sem þú gafst upp og þú sendir aftur á vefstjórnunarskjáinn.

Eftirfarandi mynd sýnir dæmi um **Settu upp síðuna þína** svargluggi í vefsvæðisgerð.

![Settu upp svargluggann fyrir síðuna þína í vefsíðugerðinni.](media/site-copy_3.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

[Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-b2c-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
