---
title: Stýring starfsmannshausa
description: Þessi grein veitir upplýsingar um sérsniðna hausstýringu í sjálfsafgreiðslu starfsmanna, í miðstöð fólks og á starfsmannssíðunni í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2867a952df79161aaee657dbc3df1f3298294dd5
ms.sourcegitcommit: 167f73a834629752c6b79c312d744e52df7f0927
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445989"
---
# <a name="worker-header-control"></a>Stýring starfsmannshausa

Microsoft Dynamics 365 Human Resources veitir sérsniðna hausstýringu í **Sjálfsafgreiðsla starfsmanna**, í **Fólk** miðstöð, og á straumlínulagað **Vinnumaður** síðu. Hausinn inniheldur lykilupplýsingar um starfsmanninn og einnig aðgerðir með einum smelli eins og að senda tölvupóst, hringja eða senda skilaboð. Hægt er að breyta hausnum með því að fjarlægja reiti eða bæta við reitum, þar á meðal sérsniðnum reitum, til að sýna viðbótarupplýsingar. Til að nota nýju hausstýringuna skaltu fara á **Eiginleikastjórnun**, og virkjaðu **Stýring starfsmannshausa** eiginleiki.

## <a name="personalization"></a>Sérstilling

Einn af helstu kostum hausstýringar starfsmanna er hæfileikinn til að sérsníða upplýsingar sem birtast á hausnum.

Efst til hægri í hausnum er hópur þriggja reita sem sýna mismunandi gögn, allt eftir stöðu starfsmanns. Þessi hópur reita er nefndur Kastljóshluti haussins. Þú getur sérsniðið Kastljóshluta haussins með því að fjarlægja núverandi reiti eða bæta við reitum. Reitirnir sem hægt er að bæta við Kastljóshlutann í hausstýringunni eru mismunandi fyrir **Sjálfsafgreiðsla starfsmanna**, **miðstöð**, og **Vinnumaður** síðu.

## <a name="employee-self-service"></a>Sjálfsafgreiðsla starfsmanns

Verkmannshausinn á **Sjálfsafgreiðsla starfsmanna** síða inniheldur eftirfarandi upplýsingar:

- Heiti starfsmanns
- Númer starfsmanns
- Stöðutitill
- Deildir
- Gerð starfskrafts
- Lögaðili ráðningar
- Starfsaldur
- Tilkynnir til (stjórnanda)
- Gerð stöðu

Hausinn inniheldur einnig aðgerð með einum smelli til að breyta persónuupplýsingum einstaklingsins. Veldu **Breyttu persónulegum upplýsingum** að opna **Persónuupplýsingar** síðu inn **Sjálfsafgreiðsla starfsmanna**.

## <a name="people-hub"></a>Yfirlit yfir fólk

Starfsmaðurinn hausar inn **Fólk** miðstöð (það **Vinnurými fólks** síðu) inniheldur eftirfarandi upplýsingar:

- Heiti starfsmanns
- Númer starfsmanns
- Stöðutitill
- Deildir
- Gerð starfskrafts
- Lögaðili ráðningar
- Starfsaldur
- Tilkynnir til (stjórnanda)
- Gerð stöðu

Hausinn inniheldur einnig aðgerðir með einum smelli eins og tölvupósti, símtölum eða skilaboðum. Ef notandi er að skoða eigin upplýsingar á **Vinnurými fólks** síðu, aðgerðarhlutinn með einum smelli inniheldur **Breyttu persónulegum upplýsingum** takki. Notandinn getur valið þennan hnapp til að opna **Persónuupplýsingar** síðu inn **Sjálfsafgreiðsla starfsmanna**.

## <a name="streamlined-worker-page"></a>Straumlínulagað verkamannasíða

Starfsmannshausinn á straumlínulagað **Vinnumaður** síða inniheldur eftirfarandi upplýsingar:

- Heiti starfsmanns
- Númer starfsmanns
- Stöðutitill
- Deildir
- Gerð starfskrafts
- Lögaðili ráðningar

Það fer eftir stöðu starfsmanns, gögnin á hausnum gætu breyst. Til dæmis, ef starfsmaðurinn hefur yfirgefið fyrirtækið, inniheldur hausstýringin **Farið út** merki, lokadagsetningu ráðningar og ástæðu uppsagnar.

Taflan hér að neðan sýnir gögnin sem birtast á hausnum fyrir mismunandi stöður starfsmanna.

| Staða starfsmanns | Gögn sem eru sýnd | Athugasemd |
|-----------------|--------------------|------|
| Í bið | <ul><li>Nafn</li><li>Númer starfsmanns</li><li>Stöðutitill</li><li>Deild</li><li>Gerð starfskrafts</li><li>Lögaðili</li><li>Skilti í bið</li><li>Upphafsdagsetning</li><li>Gefur skýrslu</li><li>Gerð stöðu</li></ul> | |
| Nýlegar ráðningar | <ul><li>Nafn</li><li>Númer starfsmanns</li><li>Stöðutitill</li><li>Deild</li><li>Gerð starfskrafts</li><li>Lögaðili</li><li>Nýlegt leigumerki</li><li>Starfsaldur</li><li>Gefur skýrslu</li><li>Gerð stöðu</li></ul> | Sjálfgefið er **Nýleg ráðning** merki er sýnt fyrir starfsmenn sem hafa verið ráðnir á síðustu sjö dögum. Til að breyta þessari stillingu, á **Stærðir mannauðs** síðu, á **Almennt** flipa, í **Tímabil nýlegra ráðninga** kafla, sláðu inn tímaramma. Til dæmis til að skoða **Nýleg ráðning** merki fyrir starfsmenn sem voru ráðnir á síðustu 14 dögum, stilla **Tímabil** sviði til **14** og **Eining** sviði til **Dagar**. |
| Virkur starfsmaður | <ul><li>Nafn</li><li>Númer starfsmanns</li><li>Stöðutitill</li><li>Deild</li><li>Gerð starfskrafts</li><li>Lögaðili</li><li>Upphafsdagsetning</li><li>Gefur skýrslu</li><li>Gerð stöðu</li></ul> | |
| Hætti | <ul><li>Nafn</li><li>Númer starfsmanns</li><li>Stöðutitill</li><li>Deild</li><li>Gerð starfskrafts</li><li>Lögaðili</li><li>Útgöngumerki</li><li>Starfsaldur</li><li>Gefur skýrslu</li><li>Gerð stöðu</li></ul> | Sjálfgefið er **Hætta** merki er sýnt fyrir starfsmenn sem fara á næstu sjö dögum. Til að breyta þessari stillingu, á **Stærðir mannauðs** síðu, á **Almennt** flipa, í **Lokar dagsetningarbili starfsmanns** kafla, sláðu inn tímaramma. Til dæmis til að skoða **Hætta** merki fyrir starfsmenn sem eru að fara á næstu 14 dögum, stilltu **Tímabil** sviði til **14** og **Eining** sviði til **Dagar**. |
| Hættir | <ul><li>Farið út merki</li><li>Númer starfsmanns</li><li>Dagsetning starfsloka</li><li>Ástæðukóði</li></ul> | Sjálfgefið, **the Exited** merki er sýnt fyrir starfsmenn sem hafa hætt á síðustu sjö dögum. Til að breyta þessari stillingu, á **Stærðir mannauðs** síðu, á **Almennt** flipa, í **Lokið dagsetningarbili starfsmanna** kafla, sláðu inn tímaramma. Til dæmis til að skoða **Farið út** merki fyrir starfsmenn sem hafa hætt á síðustu 14 dögum, stilltu **Tímabil** sviði til **14** og **Eining** sviði til **Dagar**. |
