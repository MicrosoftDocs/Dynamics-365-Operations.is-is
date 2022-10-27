---
title: Settu upp reglustillingarþjónustu (RCS)
description: Þessi grein útskýrir hvernig á að setja upp Regulatory Configuration Service (RCS).
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710782"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Settu upp reglustillingarþjónustu (RCS)

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>Kveiktu á hnattvæðingareiginleikum

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Veldu reitinn **Stjórnun eiginleika**.
3. Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækir eiginleikar** í listanum og síðan velja **Virkja núna**.

A flísar fyrir **Hnattvæðingareiginleikar** vinnusvæði ætti nú að birtast á aðal RCS mælaborðinu.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Setja upp færibreytur fyrir RCS-samþættingu við rafræna reikningsfærslu

1. Á vinnusvæðinu **Altækir eiginleikar**, í hlutanum **Viðeigandi stillingar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.
2. Í fyrsta skipti sem þú setur upp færibreyturnar verðurðu beðinn um að tengjast Life Cycle Services (LCS). Veldu **Smelltu hér til að tengjast Lifecycle Services**, og eftir að tengingunni er komið á skaltu velja **Allt í lagi**.

    > [!IMPORTANT]
    > Í löndum eða svæðum þar sem gagnabúseta er framfylgt, og ef RCS var útvegað á öðru svæði þar sem LCS er útvegað, gætirðu fengið eftirfarandi tengingarvilluboð í RCS: "Engin HTTP tilföng fannst sem samsvarar beiðni URI". Veldu **Í lagi**. Þú gætir fengið önnur villuboð í RCS: „Tókst ekki að búa til notandatákn fyrir Dynamics Lifecycle þjónustu fyrir hönd notanda (). Vinsamlegast hafðu samband við kerfisstjórann þinn."
    >  
    > Þetta gerist vegna þess að LCS er alþjóðleg þjónusta og er veitt á bandarísku svæði. Vegna búsetustefnunnar getur RCS frá núverandi svæði ekki tengst LCS. Við þessar aðstæður eru 2 mögulegar lausnir:
    > - Eyddu RCS af núverandi svæði og endurskapaðu það á Bandaríkjunum.
    > - Hunsa villurnar og haltu áfram með uppsetningu rafrænna reikninga. Þessar villur hafa engin áhrif á virkni rafrænna reikninga.

3. Á **Rafræn reikningagerð** flipa, í **Þjónustuendapunktur URI** reit skaltu slá inn viðeigandi þjónustuendapunkt fyrir þinn Microsoft Azure landafræði, eins og sýnt er í eftirfarandi töflu.

    | Gagnamiðstöð Azure-staðsetningar | URI fyrir endastöð þjónustu |
    |----------------------------|----------------------|
    | Bandaríkin              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Evrópa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Bretland             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Asía                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japan                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sviss                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasilía                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Sameinuðu arabísku furstadæmin       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ástralía                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Frakkland                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Indland                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Noregur                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Suður-Afríka               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Skoðaðu og sláðu inn í **Auðkenni umsóknar** reit fasta gildið **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Gakktu úr skugga um að aðeins alþjóðlegt einkvæmt auðkenni (GUID) sé slegið inn og að gildið innihaldi ekki önnur tákn, eins og bil, kommur, punkta eða gæsalappir.
4. Í **LCS Umhverfiskenni** reit, sláðu inn auðkenni þitt Microsoft Dynamics Lifecycle Services (LCS) umhverfi. Þetta gildi er tilvísun í fjármála- eða framboðskeðjuumhverfið sem þú munt nota með rafrænni reikningsþjónustu. Til að fá auðkenni þitt skaltu skrá þig inn á [LCS](https://lcs.dynamics.com/), opnaðu verkefnið þitt og síðan á **Stjórna umhverfi** flipa, í **Umhverfisupplýsingar** kafla, skoðaðu í **Umhverfiskenni** sviði.

    > [!IMPORTANT]
    > Ef rafræn innheimtuviðbót er sett upp í mörgum fjármála- eða framboðskeðjuumhverfi í LCS, skal alltaf nota umhverfisauðkenni síðasta uppsetta umhverfisins. Ef þú ákveður að setja viðbótina upp í nýju umhverfi Eftir að þú hefur sett upp og unnið með rafræna reikningavirkni skaltu uppfæra **LCS Umhverfiskenni** reit í RCS í nýjasta gildið.

5. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="configuration-providers"></a>Skilgreiningarveitur

Þú getur notað stillingarveitur til að greina á milli eigenda rafrænna skýrslugerðar (ER) stillinga sem eru notaðar í rafrænum reikningsferlum og hnattvæðingareiginleika eigenda. Fyrir alla hnattvæðingareiginleika sem eru útvegaðir af Microsoft og birtir í alþjóðlegu geymslunni, er stillingaveitan stillt á **Microsoft** (`http://microsoft.com`).

Þú getur aðeins breytt ER stillingum og hnattvæðingareiginleikum sem tilheyra virku stillingarveitunni. Þú getur notað þessar stillingar og eiginleika sem sniðmát til að búa til stillingar og eiginleika sem tilheyra virku stillingaveitunni, svo að þú getir stillt þær.

Fyrst skaltu búa til stillingarveiturnar. Stilltu síðan einn þeirra sem virkan. Þú getur ekki stillt **Microsoft** stillingaveitan sem virk.

### <a name="create-a-configuration-provider"></a>Búðu til stillingarveitu

1. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Viðeigandi tenglar**, skal velja **Skilgreiningarveitur**.
2. Veljið **Nýtt**.
3. Í **Nafn** reit, sláðu inn einstakt heiti fyrir stillingarveituna.
4. Í **Netfang** reit, sláðu inn einstaka vefslóð stillingaveitunnar.
5. Veljið **Vista** og lokið síðan skjámyndinni.

### <a name="select-a-configuration-provider-as-active"></a>Veldu stillingarveitu sem virkan

1. Á listanum yfir stillingaveitur, veldu stillingarveituna sem þú vilt stilla sem virkan.
2. Veldu **Stilla sem virkt**.

## <a name="import-er-configurations-from-the-global-repository"></a>Flytja inn ER stillingar úr alþjóðlegu geymslunni

1. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Viðeigandi tenglar**, skal velja **Skilgreiningarveitur**.
2. Í listanum yfir stillingarveitur velurðu **Microsoft**, og veldu síðan **Geymslur**.
3. Veldu **Alþjóðlegt**, og veldu síðan á aðgerðarrúðunni **Opið**.
4. Flyttu inn eftirfarandi ER gerðir:

    - **Samhengislíkan viðskiptavinareiknings**
    - **Reikningslíkan**
    - **Fjárhagsskjöl** (fyrir brasilískar aðstæður, ef þess er krafist)
    - **Skilaboðalíkan svars**

5. Ef **Kortlagning reikningslíkana** var ekki sjálfkrafa flutt inn, flyttu það inn.
6. Lokið síðunni.
