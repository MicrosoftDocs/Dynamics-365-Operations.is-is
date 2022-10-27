---
title: Endurreikna línu nettóupphæðir þegar þú flytur inn sölupantanir og tilboð
description: Þessi grein lýsir því hvort og hvernig kerfið endurreikur línu nettóupphæðir þegar sölupantanir og tilboð eru fluttar inn. Það útskýrir einnig hvernig þú getur stjórnað hegðun í mismunandi útgáfum af Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719335"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Endurreikna línu nettóupphæðir þegar þú flytur inn sölupantanir og tilboð

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvort og hvernig kerfið endurreikur línu nettóupphæðir þegar sölupantanir og tilboð eru fluttar inn. Það útskýrir einnig hvernig þú getur stjórnað hegðun í mismunandi útgáfum af Microsoft Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Hvernig uppfærslur á nettólínuupphæðum eru reiknaðar við innflutning

Supply Chain Management útgáfa 10.0.23 kynnt [villuleiðrétting 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Þessi villuleiðrétting breytti skilyrðunum þar sem **Virði** reitinn á línu er hægt að uppfæra eða endurreikna þegar uppfærslur á núverandi sölupöntunum og tilboðum eru fluttar inn. Í útgáfu 10.0.29 geturðu skipt út þessari villuleiðréttingu með því að kveikja á *Reiknaðu nettóupphæð línu við innflutning* eiginleiki. Þessi eiginleiki hefur svipuð áhrif, en hann veitir alþjóðlega stillingu sem gerir þér kleift að fara aftur í gamla hegðun ef þú þarft. Þrátt fyrir að nýja hegðunin geri kerfið til að virka á innsæi hátt getur það valdið óvæntum niðurstöðum í sérstökum atburðarásum þar sem öll eftirfarandi skilyrði eru uppfyllt:

- Gögn sem uppfæra núverandi færslur eru flutt inn í gegnum *Sölupöntunarlínur V2*, *V2*, eða *Skilapöntunarlínur* eining með því að nota Open Data Protocol (OData), þar með talið aðstæður þar sem þú notar tvískrifað, inn-/útflutning í gegnum Excel, og sumar samþættingar þriðja aðila.
- [Stefna um mat á viðskiptasamningum](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) sem eru til staðar koma á breytingastefnu sem takmarkar uppfærslur á **Virði** reit á sölupöntunarlínum, sölutilboðslínum og/eða skilapöntunarlínum. Athugaðu að fyrir skilapöntunarlínur, **Virði** reiturinn er alltaf reiknaður út og ekki hægt að stilla hann handvirkt.
- Innfluttu gögnin innihalda breytingar á **Virði** reit á línum, eða breytingar (svo sem einingaverð, magn eða afslátt) sem valda því að verðmæti **Virði** reit á línur sem á að endurreikna fyrir eina eða fleiri fyrirliggjandi línufærslur.

Í þessum tilteknu atburðarásum eru áhrif matsstefnu viðskiptasamninga að setja takmörkun á uppfærslur á **Virði** sviði á línunni. Þessi takmörkun er þekkt sem a *breyta stefnu*. Vegna þessarar stefnu, þegar þú notar notendaviðmótið til að breyta eða endurreikna reitinn, biður kerfið þig um að staðfesta hvort þú viljir gera breytinguna. Hins vegar, þegar þú flytur inn skrá, verður kerfið að velja fyrir þig. Fyrir útgáfu 10.0.23 skildi kerfið alltaf nettóupphæð línunnar óbreytta, nema nettóupphæð línunnar sem kom inn sé 0 (núll). Hins vegar, í nýrri útgáfum, uppfærir kerfið alltaf eða endurreiknar nettóupphæðina eftir þörfum, nema það sé beinlínis fyrirskipað að gera það ekki. Þó að nýja hegðunin sé rökréttari gæti hún valdið þér vandamálum ef þú ert nú þegar að keyra ferli eða samþættingu sem gera ráð fyrir eldri hegðun. Þessi grein lýsir því hvernig á að fara aftur í gamla hegðun ef þú þarft.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Stjórna útreikningum á nettóupphæðum línu í útgáfum 10.0.29 og síðar

Supply Chain Management útgáfa 10.0.29 kynnti eiginleika sem heitir *Reiknaðu nettóupphæð línu við innflutning*. Þessi eiginleiki bætir við valkosti sem er nefndur **Reiknaðu nettóupphæð línu** til **Færibreytur viðskiptakrafna** síðu. Þessi valkostur gerir þér kleift að velja á milli nýju og eldri hegðunar til að reikna út nettóupphæðir við innflutning.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Kveiktu eða slökktu á eiginleikanum Reikna línu nettóupphæð við innflutning

Þegar þú uppfærir í útgáfu 10.0.29, *Reiknaðu nettóupphæð línu við innflutning* sjálfgefið er kveikt á eiginleikum og nýja **Reiknaðu nettóupphæð línu** valkostur er upphaflega stilltur á *Já*. The *Já* stilling samsvarar nýju staðlaða hegðuninni. Það passar við kerfishegðun þegar slökkt er á eiginleikanum, nema ef um er að ræða virkni [CalculateLineAmount færibreyta](#CalculateLineAmount), eins og lýst er síðar í þessari grein. The *Nei* stilling passar við kerfishegðun fyrir útgáfu 10.0.23 og er aðallega veitt til að styðja við eldri samþættingarsviðsmyndir.

Stjórnendur geta snúið við *Reiknaðu nettóupphæð línu við innflutning* kveikt eða slökkt á eiginleikanum með því að nota [Eiginleikastjórnun vinnusvæði](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Stilltu valkostinn Reikna línu nettóupphæð

Þegar *Reiknaðu nettóupphæð línu við innflutning* kveikt er á eiginleikanum geturðu stillt **Reiknaðu nettóupphæð línu** valmöguleika með því að fylgja þessum skrefum.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á **Verð** flipa, á **Útreikningur á nettóupphæð línu með samþættingu** flýtiflipann, stilltu **Reiknaðu nettóupphæð línu** valmöguleika á eitt af eftirfarandi gildum:

    - *Já* – Kerfið mun alltaf endurreikna og uppfæra línuupphæðir þegar þörf krefur. (Þess vegna mun það hunsa matsstefnu viðskiptasamninga.)
    - *Nei* – Ef fyrirliggjandi eða komandi nettóupphæð fyrir einhverja línu er 0 (núll), er gildi þeirrar línu endurreiknað út frá öðrum gildum (svo sem einingaverði, magni og afslætti). Ef fyrirliggjandi eða komandi nettóupphæð er frábrugðin 0 (núll), og breytingastefna er sett á **Virði** reitinn á línunni er reiturinn ekki endurreiknaður eða uppfærður, jafnvel þó að komandi breytingar á línuverði, magni og/eða afslætti þýði að endurreikna ætti heildarlínuna. Þessi hegðun passar við útgáfu 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a> Hvernig eiginleikinn Reikna línu nettóupphæð við innflutning hefur áhrif á færibreytuna CalculateLineAmount

Þegar *Reiknaðu nettóupphæð línu við innflutning* kveikt er á eiginleikanum, gildið á`CalculateLineAmount` breytu fyrir`SalesLine` og`SalesQuotationLine` töflur hafa engin áhrif. Þess í stað er hegðuninni stjórnað á heimsvísu af **Reikna línu nettó upphæð** valmöguleika sem lýst er í fyrri hlutanum. Þess vegna, þegar kveikt er á eiginleikanum, máttu ekki vera háður`CalculateLineAmount` gildi.

Þegar *Reiknaðu nettóupphæð línu við innflutning* slökkt er á eiginleikum, the`CalculateLineAmount` breytu fyrir`SalesLine` og`SalesQuotationLine` töflur virka eins og þær gera í Supply Chain Management útgáfum 10.0.23 til 10.0.28, eins og lýst er í næsta kafla.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Útreikningar á nettóupphæð stjórnlínu í útgáfum 10.0.28 og eldri

Hvenær [villuleiðrétting 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) var kynnt í útgáfu 10.0.23, varð mögulegt að velja hvernig hver viðkomandi gagnaeining ætti að haga sér þegar nettóupphæð línu var breytt eða þurfti að endurreikna vegna annarra breytinga (svo sem uppfærts vöruverðs). Þú gætir stjórnað þessari hegðun með því að stilla nýja`CalculateLineAmount` færibreytu fyrir hverja línu í eitt af eftirfarandi gildum í innfluttu skránni:

- **`CalculateLineAmount` = *1*** — Hið **Virði** reiturinn á línunni er alltaf endurreiknaður og uppfærður, óháð því hvort breytingastefna er sett á reitinn, og óháð verðmæti nettóupphæðar sem er á innleið eða núverandi línu.
- **`CalculateLineAmount` = *0*** – Ef fyrirliggjandi eða komandi nettóupphæð fyrir einhverja línu er 0 (núll), er gildi þeirrar línu endurreiknað út frá öðrum gildum (svo sem einingaverði, magni og afslætti). Ef fyrirliggjandi eða komandi nettóupphæð er frábrugðin 0 (núll), og breytingastefna er sett á **Virði** reitinn á línunni er reiturinn ekki endurreiknaður eða uppfærður.  

Kerfið fer eftir útgáfunni þinni af Supply Chain Management:

- Í útgáfu 10.0.22 og eldri hegðar kerfið sér alltaf eins og það sé`CalculateLineAmount` er stillt á *0*, og það er engin leið að láta það hegða sér eins og það sé`CalculateLineAmount` er stillt á *1*.
- Í útgáfum 10.0.23 til 10.0.28 hegðar kerfið sér eins og`CalculateLineAmount` er stillt á *1* fyrir allar línur þar sem það er ekki sérstaklega stillt á *0* í innflutningsskránni.
