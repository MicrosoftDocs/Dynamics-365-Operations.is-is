---
title: Settu upp Regulatory Configuration Service (RCS).
description: Í þessari grein er útskýrt hvernig á að setja upp Regulatory Configuration Service (RCS).
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710782"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Settu upp Regulatory Configuration Service (RCS).

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp Regulatory Configuration Service (RCS).

## <a name="turn-on-globalization-features"></a>Kveikja á altækum eiginleikum

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Veldu reitinn **Stjórnun eiginleika**.
3. Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Altækir eiginleikar** í listanum og síðan velja **Virkja núna**.

Reitur fyrir vinnusvæði **Altækir eiginleikar** ætti nú að birtast á aðalstjórnborði RCS.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Setja upp færibreytur fyrir RCS-samþættingu við rafræna reikningsfærslu

1. Á vinnusvæðinu **Altækir eiginleikar**, í hlutanum **Viðeigandi stillingar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.
2. Eftir fyrstu uppsetningu breytanna verður þú beðin(n) að tengjast Life Cycle Services (LCS). Veljið **Smella hér til að tengjast við Lifecycle Services**, og eftir að tengingu hefur verið komið á veljið **Í lagi**.

    > [!IMPORTANT]
    > Í löndum eða svæðum þar sem gagnavistun er framfylgt, og ef RCS-vistfang þitt var útvegað á öðru svæði þar sem LCS-vistfang er útvegað, gætir þú fengið eftirfarandi villuboð í RCS: „Ekkert HTTP-vistfang fannst sem passar við URI-vistfang beiðninnar“. Veldu **Í lagi**. Þú gætir fengið villuboð í RCS: "Ekki tókst að mynda notandamerki fyrir Dynamics Lifecycle Services fyrir hönd notanda. Hafa skal samband við kerfisstjóra.
    >  
    > Þetta gerist vegna þess að LCS er alþjóðleg þjónusta sem er veitt á bandarísku svæði. RCS frá núverandi svæði getur ekki tengst LCS vegna stefnu um gagnageymslu. Við þessu eru tvær mögulegar lausnir:
    > - Eyddu RCS frá núverandi svæði og endurskapaðu það á bandarísku svæði.
    > - Hunsaðu villurnar og haltu áfram með uppsetningu rafrænna reikninga. Þessar villur hafa engin áhrif á virkni rafrænna reikninga.

3. Í flipanum **Rafræn reikningsfærsla**, í reitinn **URI fyrir endastöð þjónustu** skal slá inn viðeigandi endastöð þjónustu fyrir Microsoft Azure staðfestninguna þína eins og sýnt er í eftirfarandi töflu.

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

3. Farðu yfir og sláðu inn í **Forritsauðkenni** reitinn fasta gildið **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Gakktu úr skugga um að aðeins sé slegið inn alþjóðlegt einkvæmt kennimerki (GUID) og að gildið innihaldi ekki önnur tákn, svo sem bil, kommur, punkta eða tilvitnunarmerki.
4. Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni Microsoft Dynamics Lifecycle Services (LCS) umhverfis. Þetta gildi er tilvísun í Finance eða Supply Chain Management-umhverfi sem þú munt nota með rafrænu reikningsfærsluþjónustunni. Til að fá auðkennið þitt skráir þú þig inn á [LCS](https://lcs.dynamics.com/), opnar verkefnið þitt og svo á flipann **Stjórna umhverfinu**, í hlutanum **Umhverfisupplýsingar**, skoðar í reitinn **Umhverfisauðkenni**.

    > [!IMPORTANT]
    > Ef viðbótin fyrir rafræna reikningsfærslu er sett upp í mörgum Finance eða Supply Chain Management-umhverfum í LCS skal ávallt nota umhverfisauðkenni þess umhverfis sem síðast var sett upp. Ef þú ákveður að setja viðbótina upp í nýju umhverfi eftir að þú hefur sett upp og unnið með rafræna reikningsfærslu skaltu uppfæra **LCS-umhverfisauðkenni** í RCS til að fá nýjasta gildið.

5. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="configuration-providers"></a>Skilgreiningarveitur

Þú getur notað þjónustuaðila til að greina á milli eigenda rafrænna skýrslna sem eru notaðar í rafrænum reikningaferlum og eigenda hnattrænna eiginleika. Fyrir alla hnattræna eiginleika sem eru gefnir upp af Microsoft og birtir í hnattrænu gagnasafni er stillingin stillt á **Microsoft** (`http://microsoft.com`).

Þú getur aðeins breytt ER stillingum og hnattrænum eiginleikum sem tilheyra virkri skilgreiningarveitu. Þú getur notað þessar stillingar og eiginleika sem sniðmát til að búa til stillingar og eiginleika sem tilheyra virkri skilgreiningarveitu, svo að þú getir breytt þeim.

Fyrst skaltu búa til skilgreiningarveiturnar. Stillið svo eitt sem virkt. Ekki er hægt að stilla skilgreiningarveituna **Microsoft** sem virka.

### <a name="create-a-configuration-provider"></a>Kveikja á skilgreiningarveitu

1. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Viðeigandi tenglar**, skal velja **Skilgreiningarveitur**.
2. Veljið **Nýtt**.
3. Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir skilgreiningarveituna.
4. Færið inn einkvæmt veffang skilgreiningarveitu í **Veffang** reitinn.
5. Veljið **Vista** og lokið síðan skjámyndinni.

### <a name="select-a-configuration-provider-as-active"></a>Velja skilgreiningarveitu sem virka

1. Í listanum yfir skilgreiningarveitur skaltu velja skilgreiningarveituna sem þú vilt að sé virk.
2. Veldu **Stilla sem virkt**.

## <a name="import-er-configurations-from-the-global-repository"></a>Flytja inn skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu

1. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Viðeigandi tenglar**, skal velja **Skilgreiningarveitur**.
2. Í lista yfir skilgreiningarveitur skal velja **Microsoft** og svo **Gagnageymslur**.
3. Veljið **Altækt** og síðan **Opna** á aðgerðasvæðinu.
4. Flytja inn eftirfarandi gerðir rafrænnar skýrslugerðar:

    - **Samhengislíkan viðskiptavinareiknings**
    - **Reikningslíkan**
    - **Fjárhagsskjöl** (fyrir brasilískar aðstæður, ef með þarf)
    - **Skilaboðalíkan svars**

5. Ef **Vörpun líkans** var ekki sjálfkrafa flutt inn skaltu flytja það inn.
6. Lokið síðunni.
