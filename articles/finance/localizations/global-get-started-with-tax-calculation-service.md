---
title: Hafist handa með skattaútreikning
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp skattaútreikning.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 454608c2c3a86b71cf181129c762c837c5165902
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336657"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Hafist handa með skattaútreikningi (forútgáfa)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Þetta efnisatriði veitir upplýsingar um hvernig hafist er handa við skattaútreikning. Fyrst leiðir það þig í gegnum grunnstillingarskrefin í Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) og Dynamics 365 Finance og Dynamics 365 Supply Chain Management. Það fer síðan yfir almennu leiðina til að nota möguleika skattaútreiknings í færslum Finance og Supply Chain Management.

Þessi uppsetning samanstendur af fjórum meginskrefum:

1. Í LCS skal setja upp skattaútreikning.
2. Í RCS skal setja upp eiginleika skattaútreiknings. Þessi uppsetning á ekki við um neinn sérstakan lögaðila. Hægt er að nota hana í öllum lögaðilum í Finance og Supply Chain Management.
3. Í Finance og Supply Chain Management skal setja upp færibreytur skattaútreiknings eftir lögaðila.
4. Í Finance og Supply Chain Management skal stofna færslur á borð við sölupantanir og nota skattaútreikning til að ákvarða og reikna skatta.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að klára ferlið í þessu efnisatriði þurfa eftirfarandi skilyrði að vera til staðar:

- Þú hefur aðgang að LCS-reikningnum þínum og þú hefur virkjað LCS-verk með umhverfi í lagi 2 (eða ofar) sem keyrir Dynamics 365 útgáfu 10.0.18 með [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) eða nýrri.
- Þú hefur aðgang að RCS-reikningnum þínum.
- Þú hafðir samband við Microsoft til að virkja forútgáfuna í uppsettu umhverfi þínu af Finance eða Supply Chain Management.

## <a name="set-up-tax-calculation-in-lcs"></a>Setja upp skattaútreikning í LCS

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com)
2. Ljúkið uppsetningunni fyrir Microsoft Power Platform-samþættingu. Frekari upplýsingar er að finna í [Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Veljið eitt af uppsettu umhverfunum sem er ekki framleiðsluumhverfi og veljið því næst **Setja upp nýja innbót**.
4. Veljið **Skattaútreikningur (forskoðun)**.
5. Lesið og samþykkið skilmálana og veljið því næst **Setja upp**.

## <a name="set-up-tax-calculation-in-rcs"></a>Setja upp skattaútreikning í RCS

Skrefin í þessum hluta eru ekki tengd við sérstakan lögaðila. Aðeins þarf að ljúka þessu ferli einu sinni og hægt er að ljúka því í hvaða lögaðila sem er í RCS.

1. Skráðu þig inn í [RCS](https://marketing.configure.global.dynamics.com/).
2. Á vinnusvæðinu **Rafræn skýrslugerð**, skal bæta við nýrri skilgreiningarveitu. Notið heiti fyrirtækisins sem heiti veitunnar. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Veljið skilgreiningarveituna sem var stofnuð og veljið síðan **Stilla sem virkt**.
4. Veljið skilgreiningarveituna **Microsoft** og veljið því næst **Geymslur**.
5. Í reitnum **Gerð** skal velja **Altæk**.
6. Veljið **Opna**.
7. Opnið **Gagnalíkan skatts**, stækkið skráartréð, og veljið síðan **Skattaskilgreining**.
8. Veljið nýjustu útgáfuna og svo **Flytja inn**.
9. Farið aftur á vinnusvæðið **Altækir eiginleikar (forskoðun)**, veljið **Eiginleikar**, veljið reitinn **Skattaútreikningur**, og veljið því næst **Bæta við**.
10. Velja eina af eftirfarandi gerðum eiginleika:

    - **Nýr eiginleiki** – Búa til uppsetningu eiginleika sem er með tómt innihald.
    - **Byggt á fyrirliggjandi eiginleika** – Búa til eiginleika úr fyrirliggjandi eiginleika og afrita innihaldið úr fyrirliggjandi eiginleikauppsetningu.

11. Færið inn heiti og lýsingu á eiginleikanum og veljið svo **Stofna eiginleika**.

    Þegar eiginleikinn hefur verið búinn til verða útgáfudrög hans sjálfkrafa búin til.

12. Veldu drög eiginleikans og svo **Breyta**. Fyllt er í síðuna **Uppsetning skattaútreiknings**.
13. Veljið **Útgáfa skilgreiningar**. Þú ættir að sjá grunnstillingarútgáfuna sem þú fluttir inn í skrefi 8.

    Microsoft veitir sjálfgefna skattaskilgreiningu fyrir innbót skattaútreiknings. Þessi skilgreining nær yfir flestar kröfur varðandi hegðun skattaútreikningsins. Hún verður uppfærð út frá ábendingum markaðarins. Ef ætlunin er að stækka skilgreininguna þannig að hún uppfylli tilteknar kröfur skal skoða [Hvernig á að smíða viðbót í skattþjónustu](./tax-service-add-data-fields-tax-integration-by-extension.md) til að fá upplýsingar um hvernig á að búa til og velja sína eigin skattaskilgreiningu.

    Þegar **Útgáfa skilgreiningar** hefur verið valin birtast nokkrir flipar til viðbótar:

    - **Skattkóðar** – Þessi flipi er áskilinn. Hann er notaður til að vinna með aðalgögn fyrir skattkóða. Allir skattkóðar sem eru búnir til í þessum flipa eru sjálfkrafa samstilltir við Finance þegar núverandi útgáfa af uppsetningu skattaeiginleika er virkjuð í lögaðilanum.
    - **Gildissvið skattkóða** – Þessi flipi er áskilinn. Hann er notaður til að skilgreina fylki sem ákvarðar skattkóða, skattflokk og vöruskattflokk. Skattkóðinn sem verður fyrir valinu er notaður til að reikna út skattupphæðina. Gildunum í reitunum **Skattkóði**, **Skattflokkur** og **Vöruskattflokkur** er skilað til Finance.
    - **Gildissvið skattskráningarnúmers viðskiptavinar** – Þessi flipi er valfrjáls. Ef þú ert með mörg skattskráningarnúmer fyrir einn viðskiptavin getur skattaútreikningur sjálfkrafa fundið út rétt skattskráningarnúmer. Í fylki þessa flipa eru reglurnar skilgreindar sem eru notaðar til að taka ákvörðunina. Annars munu Finance og Supply Chain Management halda áfram að nota sjálfgefið skattskráningarnúmerí skattskyldum skjölum fyrir sölufærslur.
    - **Gildissvið skattskráningarnúmers lánardrottins** – Þessi flipi er valfrjáls. Ef þú ert með mörg skattskráningarnúmer fyrir einn lánardrottin getur skattaútreikningur sjálfkrafa fundið út rétt skattskráningarnúmer. Í fylki þessa flipa eru reglurnar skilgreindar sem eru notaðar til að taka ákvörðunina. Annars munu Finance og Supply Chain Management halda áfram að nota sjálfgefið skattskráningarnúmerí skattskyldum skjölum fyrir innkaupafærslur.
    - **Gildissvið listakóða** – Þessi flipi er valfrjáls. Hann getur aðstoðað við að ákveða sjálfkrafa gildið í reitnum **Listakóði** í gegnum sveigjanlegri og stillanlegri reglur. Í fylki þessa flipa er hægt að skilgreina reglurnar sem eru notaðar til að taka ákvörðunina. Annars munu Finance og Supply Chain Management halda áfram að nota sjálfgefinn kóða í skattskyldum skjölum.

14. Í flipanum **Skattkóðar** skal velja **Bæta við** og slá inn skattkóðann og lýsingu.
15. Veljið **Skatthluti**. Skatthlutinn er safn af útreikningsaðferðum sem var skilgreint í fyrri útgáfu valdrar skattaskilgreiningar. Eftirfarandi skatthlutar eru í boði:

    - Eftir nettóupphæð
    - Eftir brúttóupphæð
    - Eftir magni
    - Eftir framlegð
    - Skattur á skatt

16. Veljið **Vista**. Fleiri reitir verða tiltækir samkvæmt skatthlutanum sem var valinn.
17. Notið eftirfarandi valkosti til að gera grein fyrir eðli skattkóðans:

    - Er undanskilið
    - Er notkunarskattur
    - Er bakfært gjald
    - Undanskilja úr útreikningi grunnupphæðar

    Fyrir aðstæður neysluskatts skal setja upp einn skattkóða sem er með jákvætt skatthlutfall og merkja hann sem **Er neysluskattur**.

    Fyrir aðstæður bakfærðs gjalds skal setja upp tvo skattkóða, einn sem er með jákvætt skatthlutfall og annan sem er með neikvætt skatthlutfall en sama hlutfallið. Merkið neikvæða skattkóðann sem **Er bakfært gjald**. Frekari upplýsingar um lausn bakfærðs gjalds í Finance er að finna í [Virkni bakfærðs gjalds fyrir skema VSK/VÞS](emea-reverse-charge.md).
    
    Fyrir sumar skattgerðir sem á að undanskilja frá útreikning á grunnupphæð skatts fyrir færslur með verði, t.d. tollur í sumum löndum, skal velja gátreitinn **Undanskilja frá útreikningi grunnupphæðar**.

    Viðhaldið mörkum skatthlutfalla og skattupphæðar fyrir þennan skattkóða.

18. Endurtakið skref 14 til 17 til að bæta við öllum öðrum nauðsynlegum skattkóðum.
19. Í flipanum **Gildissvið skattkóða** skal velja dálkana sem þarf til að finna út réttan skattkóða og síðan velja **Bæta við**.
20. Sláðu inn eða veldu gildi fyrir hvern dálk. Reitirnir **Skattkóði**, **Skattflokkur** og **Vöruskattflokkur** verða úttak þessa fylkis.
21. Endurtakið skref 19 til 20 til að setja upp gildissvið skattskráningarnúmera viðskiptavinar, skattskráningarnúmer lánardrottins og listakóða.
22. Veljið **Vista** og lokið síðan skjámyndinni.
23. Veljið **Breyta stöðu** \> **Ljúka**. Þegar stöðunni er breytt í **Lokið** verður ekki lengur hægt að breyta útgáfunni.
24. Veljið **Breyta stöðu** \> **Birta**. Þessi útgáfa á uppsetningu skattaeiginleikans verður færð í altæku geymsluna og verður sýnileg hverjum lögaðila í Finance.

## <a name="dynamics-365-setup"></a>Dynamics 365 uppsetning

Þegar uppsetningu RCS er lokið þarf, eins og lýst er í fyrri hlutanum, að vera með útgefna útgáfu af skattaeiginleikanum. Fylgið þessum skrefum til að setja upp skattaútreikning í Finance.

Lögaðili sér um uppsetningu í þessum hluta. Þú verður að skilgreina hana fyrir hvern lögaðila sem á að virkja skattaútreikning fyrir í Finance.

1. Í Finance skal fara í **Skattur** \> **Uppsetning** \> **Skattaskilgreining** \> **Uppsetning skattaútreiknings (forútgáfa)**.
2. Á flipanum **Almennt** skal stilla eftirfarandi reiti:

    - **Virkja skattaútreikning** – Veljið þennan gátreit til að virkja innbót skattaútreiknings fyrir lögaðilann. Ef það er ekki virkjað fyrir núverandi lögaðila mun lögaðilinn halda áfram að nota núverandi skattkerfi til að finna út og reikna skatt.
    - **Uppsetning eiginleika** – Veljið uppsetningu og útgáfu útgefins skattaeiginleika fyrir lögaðilann. Frekari upplýsingar um það hvernig á að setja upp og ljúka við útgefinn skattaeiginleika er að finna í fyrri hluta þessa efnisatriðis.
    - **Viðskiptaferli** – Veljið viðskiptaferlana sem á að virkja.
    - **Virkja leiðréttingu á skattkóða** – Stillið þennan valkost á **Já** til að virkja leiðréttingar á skattkóða á síðum virðisaukaskatts.

3. Í flipanum **Útreikningar** skal skilgreina fyrirhugaða sléttunarreglu fyrir lögaðilann.
4. Í flipanum **Viðbrögð við villum** skal skilgreina fyrirhugaða aðferð við meðhöndlun á villu fyrir lögaðilann. Þrír valkostir eru í boði fyrir hvern niðurstöðukóða:

    - Ekkert
    - Viðvörun
    - Villa

5. Vistið uppsetninguna.
6. Endurtakið skref 1 til 5 fyrir hvern lögaðila til viðbótar.

## <a name="transaction-processing"></a>Úrvinnsla á færslu

Þegar öllum uppsetningarferlum er lokið er hægt að nota skattaútreikning til að ákveða og reikna út skatt í Finance. Skrefin til að vinna úr færslum eru þau sömu. Eftirfarandi færslur eru studdar í Finance útgáfu 10.0.18:

- Söluferli

    - Sölutilboð
    - Sölupöntun
    - Staðfesting
    - Tiltektarlisti
    - Fylgiseðill
    - Sölureikningur
    - Kreditnóta
    - Skila pöntun
    - Gjald hauss
    - Línugjald

- Innkaupaferli

    - Innkaupapöntun
    - Staðfesting
    - Komulisti
    - Innhreyfingarskjal afurða
    - Innkaupareikningur
    - Gjald hauss
    - Línugjald
    - Kreditnóta
    - Skila pöntun
    - Innkaupabeiðni
    - Gjald innkaupabeiðnilínu
    - Beiðni um tilboð
    - Síðuhaus gjald við beiðnum um tilboð
    - Lína gjald í beiðni um tilboð

- Birgðavinnsla

    - Flutningspantanir - senda
    - Móttaka flutningspöntunar
