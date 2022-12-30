---
title: Endurreikna nettóupphæðir línu þegar sölupantanir og tilboð eru flutt inn
description: Í þessari grein er því lýst hvort og hvernig kerfið endurreiknar nettóupphæð línu þegar sölupantanir og tilboð eru flutt inn. Þar er einnig útskýrt hvernig hægt er að stjórna hegðuninni í mismunandi útgáfum af Microsoft Dynamics 365 Supply Chain Management.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719335"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Endurreikna nettóupphæðir línu þegar sölupantanir og tilboð eru flutt inn

[!include [banner](../includes/banner.md)]

Í þessari grein er því lýst hvort og hvernig kerfið endurreiknar nettóupphæð línu þegar sölupantanir og tilboð eru flutt inn. Þar er einnig útskýrt hvernig hægt er að stjórna hegðuninni í mismunandi útgáfum af Microsoft Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Hvernig uppfærslur á nettó línuupphæðum eru reiknaðar við innflutning

Supply Chain Management útgáfa 10.0.23 innihélt fyrst [villuleiðréttingu 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Þessi villuleiðrétting breytti skilyrðum þess að reiturinn **Nettóupphæð** á línu er hægt að uppfæra eða endurreikna þegar uppfærslur á fyrirliggjandi sölupöntunum og verðtilboðum eru flutt inn. Í útgáfu 10.0.29 er hægt að skipta um þessa villuleiðréttingu með því að kveikja á eiginleikanum *Reikna nettóupphæð línu við innflutning*. Þessi eiginleiki hefur svipuð áhrif en veitir altæka stillingu sem gerir þér kleift að snúa aftur til gömlu hegðunarinnar ef þörf krefur. Þrátt fyrir að nýja hegðunin geri kerfið skilvirkara getur hún leitt til ófyrirsjáanlegra niðurstaðna í tilteknum aðstæðum þar sem öll eftirfarandi skilyrði eru uppfyllt:

- Gögn sem uppfæra fyrirliggjandi skrár eru flutt inn í gegnum *Sölupöntunarlínur V2*, *Söluverðtilboðslínur V2* eða *Skilapantanalínur* með því að notaa Open Data Protocol (OData), þar á meðal aðstæður þar sem þú notar tvöföld skráning, inn-/útflutning í gegnum Excel og tilteknar samþættingar þriðja aðila.
- Gildandi [Mat á stefnum viðskiptasamnings](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) innihalda breytingareglu sem takmarkar uppfærslur á reitknum **Nettóupphæð** á sölupöntunarlínum, sölutilboðslínum og/eða skilapöntunarlínum. Athugaðu að fyrir skilapantanalínur reiknast alltaf reiturinn **Nettóupphæð** og ekki er hægt að stilla hana handvirkt.
- Innfluttu gögnin fela í sér breytingar á reitnum **Nettóupphæð** á línum eða breytingar (svo sem vöruverð, magn eða afsláttur) sem valda því að gildi reitsins **Nettóupphæð** á línum er endurreiknað fyrir eina eða fleiri fyrirliggjandi línufærslur.

Í þessum sérstöku aðstæðum eru áhrif mats á reglu verðsamnings að setja takmarkanir á uppfærslur í reitnum **Nettóupphæð** í línunni. Þessi takmörkun kallast *breytingaregla*. Vegna þessarar reglu biður kerfið þig um að staðfesta hvort þú viljir gera breytinguna þegar þú notar notendaviðmótið til að breyta eða endurreikna reitinn. Hins vegar, þegar þú flytur inn færslu, verður kerfið að velja fyrir þig. Áður en útgáfa 10.0.23 er gefin út hefur kerfið alltaf látið nettóupphæð línunnar vera óbreytta, nema nettóupphæð línu á innleið sé 0 (núll). Í nýrri útgáfum uppfærir kerfið hins vegar alltaf eða endurreiknar nettóupphæðina eftir þörfum, nema það fái sérstaka skipun um að gera það ekki. Þrátt fyrir að nýja hegðunin sé rökréttari gæti hún valdið vandræðum hjá þér ef þú ert þegar að keyra ferli eða samþættingar sem gera ráð fyrir eldri hegðun. Þessi grein lýsir því hvernig á að breyta aftur í gamla hegðun ef þörf krefur.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Stjórna útreikningum nettóupphæða línu í útgáfum 10.0.29 og nýrri

Supply Chain Management útgáfa 10.0.29 kynnti eiginleika sem er nefndur *Reikna nettóupphæð línu við innflutning*. Þessi eiginleiki bætir við valkosti sem er nefndur **Reikna nettóupphæð línu** á síðunni **Færibreytur viðskiptakrafna**. Þessi valkostur gerir þér kleift að velja milli nýrrar og eldri hegðunar til að reikna nettóupphæðir línu við innflutning.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Kveikja eða slökkva á eiginleikanum reikna nettóupphæð línu við innflutning

Þegar þú uppfærir í útgáfu 10.0.29 er sjálfgefið kveikt á eiginleikanum *Reikna nettóupphæð línu við innflutning* og nýi valkosturinn **Reikna nettóupphæð línu** er upphaflega stilltur á *Já*. Stillingin *Já* samsvarar nýju stöðluðu hegðuninni. Það passar við hegðun kerfisins þegar slökkt er á eiginleikanum, nema þegar um er að eiginleika [CalculateLineAmount-færibreytunnar](#CalculateLineAmount), eins og lýst er síðar í þessari grein. Stillingin *Engin* passar við hegðun kerfisins fyrir útgáfu 10.0.23 og er aðallega veitt til að styðja við eldri samþættingaraðstæður.

Stjórnendur geta kveikt eða slökkt á eiginleikanum *Reikna nettóupphæð línu við innflutning* með því að nota [Vinnusvæði eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Stilla valkostinn Reikna nettóupphæð línu

Þegar kveikt er á eiginleikanum *Reikna nettóupphæð línu við innflutning*, getur þú stillt valkostinn **Reikna nettóupphæð línu** með því að fylgja þessum skrefum.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á flipanum **Verð**, á flýtiflipanum **Útreikningur á nettóupphæð línu með samþættingu**, stillið valkostinn **Reikna nettóupphæð línu** á eitt af eftirfarandi gildum:

    - *Já* – Kerfið mun alltaf endurreikna og uppfæra línuupphæðir þegar þörf krefur. (Þess vegna mun það hunsa stefnu um mat á verðsamningi).
    - *0* – Ef fyrirliggjandi eða innkomin nettóupphæð fyrir einhverja línu er 0 (núll) er gildið fyrir þá línu endurreiknað miðað við önnur gildi (svo sem einingarverð, magn og afslátt). Ef fyrirliggjandi eða innkomin nettóupphæð er frábrugðin 0 (núll) og breytingastefna er stillt í reitinn **Nettóupphæð** í línunni er reiturinn ekki endurreiknaður eða uppfærður, jafnvel þótt innkomnar breytingar á línuverði, magni og/eða afslætti leiði til þess að endurreikna eigi upphæð línunnar. Þessi hegðun passar við hegðun í útgáfu 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>Hvernig eiginleikanum Reikna nettóupphæð línu hefur áhrif á færibreytuna CalculateLineAmount

Þegar kveikt er á eiginleikanum *Reikna nettóupphæð línu við innflutning* er gildi `CalculateLineAmount` færibreytunnar fyrir töflur `SalesLine` og `SalesQuotationLine` engin áhrif. Þess í stað er hegðuninni stjórnað altækt með valkostinum **Reikna nettóupphæð línu** sem er lýst í fyrri hlutanum. Þegar kveikt er á eiginleikanum má því ekki taka tengsli við `CalculateLineAmount` gildinu.

Þegar slökkt er á eiginleikanum *Reikna nettóupphæð línu við innflutning*, virkar `CalculateLineAmount` færibreytan fyrir töflu `SalesLine` og `SalesQuotationLine` eins og í Supply Chain Management 10.0.23 til og með 10.0.28, eins og lýst er í næsta hluta.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Stjórna útreikningum á nettóupphæðum línu í útgáfum 10.0.28 og fyrr

Þegar [villuleiðrétting 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) var sett inn í útgáfu 10.0.23 var hægt að velja hvernig hver viðeigandi gagnaeining ætti að haga sér þegar nettóupphæð línunnar var breytt eða þurfti að endurreikna hana vegna annarra breytinga (svo sem uppfærðs vöruverðs). Þú gætir stjórnað þessari hegðun með því að stilla nýju `CalculateLineAmount` færibreytuna fyrir hverja línu á eitt af eftirfarandi gildum í innfluttu skránni:

- **`CalculateLineAmount` = *1*** – Reiturinn **Nettóupphæð** á línunni er alltaf endurreiknaður og uppfærður, óháð því hvort breytingaregla er sett fyrir reitinn, og óháð verðmæti nettóupphæðar línu á innleið eða fyrirliggjandi.
- **`CalculateLineAmount` = *0*** – Ef fyrirliggjandi eða innkomin nettóupphæð fyrir einhverja línu er 0 (núll) er gildið fyrir þá línu endurreiknað miðað við önnur gildi (svo sem einingarverð, magn og afslátt). Ef fyrirliggjandi eða innkomin nettóupphæð er frábrugðin 0 (núll) og breytingastefna er stillt í reitinn **Nettóupphæð** í línunni er reiturinn ekki endurreiknaður eða uppfærður.  

Hegðun kerfisins fer eftir þinni útgáfu af Supply Chain Management:

- Í útgáfu 10.0.22 og fyrr hegðar kerfið sér alltaf eins og það `CalculateLineAmount` sé stillt á *0*, og engin leið er að láta það hegða sér eins og það `CalculateLineAmount` sé stillt á *1*.
- Í útgáfum 10.0.23 til og með 10.0.28 hagar kerfið sér eins og það `CalculateLineAmount` sé stillt á *1* fyrir allar línur þar sem það er ekki sérstaklega stillt á *0* í innfluttu skránni.
