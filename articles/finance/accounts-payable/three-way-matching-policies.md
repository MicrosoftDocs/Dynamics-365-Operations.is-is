---
title: Stefnur þríhliða jöfnunarregla
description: Þetta efnisatriði gefur dæmi um þríhliða jöfnun.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d337abc899ec668a52d9ba931599dc51d91a296c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971804"
---
# <a name="three-way-matching-policies"></a>Stefnur þríhliða jöfnunarregla

[!include [banner](../includes/banner.md)]

Þetta efnisatriði gefur dæmi um þríhliða jöfnun.

<a name="example-three-way-matching-for-items"></a>Dæmi: Þríhliða jöfnun fyrir vörur
-------------------------------------

**Samantekt:** Ken er stjórnandi við höfuðstöðvar fyrirtækis lögaðila sem heitir Fabrikam. Ken ákveður að allir reikningar lánardrottins sem eru byggðir á innkaupapöntunum skuli jafnaðir við innkaupapöntunarlínur (tvíhliða jöfnun). Fyrir innkaup á vörum sem verða notaðar sem eignir, skulu reikningar jafnaðir við innkaupapöntunarlínur og línur innhreyfingarskjals afurða (þríhliða jöfnun).

Fabrikam starfar með marga lögaðila og starfsmenn á öllum stöðum í heiminum. Þar sem magn færslna eykst, eykst misræmi á milli innhreyfinga og reikninga einnig. Þetta leiðir til þess að eignir eru afskrfaðar. Reikningar frá lánardrottnum eru greiddir en ferlið inniheldur ekki auðkenningu misræmis þegar mótteknar eru færri vörur en pantað var, eða þegar vörur eru alls ekki mótteknar. Eyðsla eykst einnig þar sem starfsmenn þurfa samt sem áður verkfæri og annað efni við störf sín. Ken vill tryggja að lánardrottnar séu að senda afurðir sem eru pantaðar og að vörurnar séu mótteknar af starfsmönnum Fabrikam. Þess vegna Ken krefst tvíhliða og þríhliða jöfnunar fyrir alla lögaðila í fyrirtækinu. Reikningsjöfnun hjálpar til við að tryggja að hægt sé að rekja og leysa vandamál sem koma upp varðandi vörur sem hafa horfið eða ekki verið mótteknar. 

Reikningsjöfnunarreglur í þessu dæmi hjálpa fólki í eftirfarandi hlutverkum að uppfylla þessi markmið:

-   Ken er eftirlitsmaður fyrir fyrirtækið Fabrikam. Hann getur hjálpað fólki í fyrirtækinu að greina og laga vandamál við pöntun, móttöku og greiðslu á vörum (vörur og þjónusta) frá lánardrottnum.
-   Phyllis og Apríl eru aðalbókarar í deild lánadrottna fyrir bandarískt útibú Fabrikam. Þær geta framfylgt stefnu fyrirtækisins og gengið úr skugga um að reikningar séu aðeins greiddir eftir jöfnun þeirra við innkaupapöntun og innhreyfingar á vörum og þjónustu, þar sem við á.
-   Tony er framleiðslustjóri fyrir bandarískt útibú Fabrikam. Hann og annað starfsfólk framleiðslu geta tryggt að vörur séu mótteknar eins og þær voru pantaðar frá lánardrottnum og eru teknir með þannig að við starfsfólks hafa hvað þeir verða að hafa til að sinna starfi sínu.

### <a name="prerequisites"></a>Forkröfur

-   Ken stillir jöfnunarreglu sem á við lögaðila stigs í þríhliða jöfnun.
-   Ken setur er Sjálfkrafa uppfærslu haus jöfnun víxla stöðu í lögaðila á Já.
-   Ken stillir reitinn Samtölur verðsamræmis fyrir lögaðilann á Prósentu og færir inn 15% sem prósentu vikmarka.
-   Ken stillir jöfnunarreglu á atriðastigi vöru 1500 – CNC Milicron Vél á þríhliða jöfnun. Þessi vara er eignaliður sem er notaður fyrir framleiðslu hjá Fabrikam. Reikningar fyrir þessa vöru eru jafnaðir við innkaupapöntunarlínur fyrir verð og við innhreyfingarskjöl afurða fyrir magn.
-   Tony færir innkaupabeiðni fyrir fimm CNC Milicron Vélar. Alicia, afgreiðslumaður pantana hjá Fabrikam, gefur út innkaupapöntun til lögaðila sem heitir Contoso til að afhenda vörurnar.

    | Vörunúmer                 | Magn | Einingarverð | Nettóupphæð | Gjaldakóði        | Gildi gjalds |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicron vél | 5        | 8.000,00   | 40.000,00  | Sending og afgreiðsla | 3.000,00      |

-   Arnie, starfsmaður viðskiptakrafa hjá Contoso, fer yfir sendingar vikunnar. Arnie velur sendingarfærslur til að reikningsfæra Fabrikam fyrir afhendingu CNC Milicron Vélar. Arnie setur með gjöld fyrir sending og afgreiðslu. Fabrikam mun telja að gjöldin séu hluti af kostnaði eignarinnar.

### <a name="scenario"></a>Aðstæður

1.  Sammy, starfsmaður í móttökudeild Fabrikam, fær heildarmagn af vélum sem eru sendar frá Contoso. Hann færir inn magn upp á 5 í innhreyfingarskjal afurða. Vegna þess að innkaupapöntunin hefur verið móttekin að fullu, breytist staða innkaupapöntunar í Móttekið.
2.  Apríl, samræmingaraðili lánardrottna á Fabrikam, færir inn og staðfestir reikninginn sem er sendur af Contoso. Hún staðfestir eftirfarandi upplýsingar:
    -   Fyrir vörur sem krefjast þríhliða jöfnunar jafnast magnið í reikningslínunni við magnið sem var móttekið. Magn á reikningi er sýnt á innhreyfingarskjali afurða sem er jafnað við reikninginn.
    -   Fyrir vörur sem krefjast tvíhliða eða þríhliða jöfnunar eru verð á reikningslínunni innan vikmarka sem eru skilgreind í Microsoft Dynamics 365 Finance. Þar á meðal eru eftirfarandi gerðir af samsvörun verðs:
        -   Samsvörun nettóeiningaverðs – Nettóeiningaverð í reikningslínunni samsvarar nettóeiningarverði í innkaupapöntunarlínunni, innan prósentu vikmarka. Í þessu dæmi eru vikmörk nettóeiningaverðs +8%.
        -   Jöfnun samtalna verðs – Nettóupphæð í reikningslínunni er jöfnuð við nettóupphæð innkaupapöntunarlínu, innan vikmarka prósentu, upphæðar eða prósentu og upphæðar. Í þessu dæmi eru vikmörk jöfnunar samtalna verðs +15%.

Pappírsreikningur frá Contoso inniheldur eftirfarandi upplýsingar.

| Vara                        | Magn | Einingarverð | Nettóupphæð |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicron vél | 5        | 8.100,00   | 40,500.00  |
| Sending og afgreiðsla       |          |            | 4,000.00   |
| Skattur                         |          |            | 0,00       |
| Alls                       |          |            | 44,500.00  |

Reikningalínan inniheldur eftirfarandi upplýsingar.

| Vörunúmer                 | Magn | Einingarverð | Nettóupphæð línu | Jöfnunarregla    | Magn á innhreyfingarskjali afurða sem á að para | Verðsamsvörun | Samtala verðs jöfnuð |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicron vél | 5        | 8.100,00   | 40.500,00       | Þríhliða jöfnun | Stóðst                         | Stóðst      | Stóðst            |

Þar sem þessi lína stenst reikningsjöfnunarferlið er hægt að bóka reikninginn.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a>Dæmi: Samsetningar þríhliða jöfnunar fyrir vöru og lánardrottinn
Samantekt: Ken er eftirlitsmaður við höfuðstöðvar fyrirtækis lögaðila sem heitir Fabrikam. Ken ákveður að allir reikningar sem eru byggðir á innkaupapöntunum skuli jafnaðir við innkaupapöntunarlínur (tvíhliða jöfnun). Cassie er bókari í malasísku útibúi Fabrikam. Hún tilgreinir að valdar vörur sem eru pantaðar frá tilteknum lánardrottnum í Malasíu skuli jafnaðar við innkaupapöntunarlínur og línur innhreyfingarskjals afurða (þríhliða). Hún getur einnig hnekkt jöfnunarreglu á hærra stigi yfir jöfnun fyrir tilgrendar innkaupapantanir. 

Rúmmál og upphæðir eru litlar og vandræði hafa verið með afhendingardagsetningu frá sumum lánardrottnum í Malasíu. Þess vegna stillir Cassie stýringar fyrir samsetningar á tiltekinni vöru og lánardrottni sem keyptar eru í Malasíu á þríhliða jöfnun. 

Reikningsjöfnunarreglur í þessu dæmi hjálpa fólki í eftirfarandi hlutverkum að uppfylla þessi markmið:
-   Ken er eftirlitsmaður fyrir fyrirtækið Fabrikam. Hann getur hjálpað fólki í fyrirtækinu að greina og laga vandamál við pöntun, móttöku og greiðslu á vörum (vörur og þjónusta) frá lánardrottnum.
-   Cassie er bókari fyrir útibú Fabrikam í Malasíu. Hún getur framfylgt stefnu fyrirtækisins og gengið úr skugga um að reikningar séu aðeins greiddir eftir jöfnun þeirra við línur innkaupapöntunar og innhreyfingarskjöl sem sýna vörur og þjónustu. Hún getur einnig hækkað stig stýringar í þríhliða jöfnun fyrir tilteknar vörur til að stýra rekstrarkostnaði.

### <a name="prerequisites"></a>Forkröfur

-   Ken stillir jöfnunarreglu sem á við lögaðila stigs í tvíhliða.
-   Ken stillir reitinn Samtölur verðsamræmis fyrir lögaðilann á Prósentu og færir inn 10% sem prósentu vikmarka.
-   Ken stillir vikmörk einingarverðs fyrir allar vörur á 2%.
-   Cassie stillir jöfnunarregluna á samsetningarstig vöru og lánardrottins fyrir vöru PH2500 – Tölvu og lánardrottinn Contoso á þríhliða jöfnun.
-   Alicia, afgreiðslumaður pantana í útibúi Fabrikam í Malasíu, gefur út innkaupapantanir til Contoso til að afhenda vörurnar þrjár, eins og sýnt er í eftirfarandi töflu. Þegar hún stofnar innkaupapöntun, hnekkir hún jöfnunarreglu fyrir þráðlausa mús í þríhliða jöfnun í stað tvíhliða jöfnunar.

    | Vörunúmer           | Magn | Einingarverð | Nettóupphæð | Jöfnunarregla (sjálfgefin) | Jöfnunarregla (á innkaupapöntunarlínu) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 - Tölva     | 2        | 2.500,00   | 5.000,00   | Þríhliða jöfnun              | Þríhliða jöfnun                           |
    | MM01 – Þráðlaus mús | 2        | 40,00      | 80,00      | Tvíhliða jöfnun                | Þríhliða jöfnun                           |
    | USB drif             | 200      | 10,00      | 2.000,00   | Tvíhliða jöfnun                | Tvíhliða jöfnun                             |

### <a name="scenario"></a>Aðstæður

1.  Vörurnar berast. Sammy, starfsmaður í móttökudeild útibús Fabrikam í Malasíu, er truflaður og bókar ekki innhreyfingarskjal afurða strax.
2.  Apríl, samræmingaraðili lánardrottna á Fabrikam, færir inn og staðfestir reikninginn sem er sendur af Contoso. Hún staðfestir eftirfarandi upplýsingar:
    -   Fyrir vörur sem krefjast þríhliða jöfnunar jafnast magnið í reikningslínunni við magnið sem var móttekið. Magn á reikningi er sýnt á innhreyfingarskjali afurða sem er jafnað við reikninginn.
    -   Fyrir vörur sem krefjast tvíhliða eða þríhliða jöfnunar eru verð á reikningslínunni innan vikmarka sem eru skilgreind í forritinu. Þar á meðal eru eftirfarandi gerðir af samsvörun verðs:
        -   Samsvörun nettóeiningaverðs – Nettóeiningaverð í reikningslínunni samsvarar nettóeiningarverði í innkaupapöntunarlínunni, innan prósentu vikmarka. Í þessu dæmi eru vikmörk nettóeiningaverðs +2%.
        -   Jöfnun samtalna verðs – Nettóupphæð í reikningslínunni er jöfnuð við nettóupphæð innkaupapöntunarlínu, innan vikmarka prósentu, upphæðar eða prósentu og upphæðar. Í þessu dæmi eru vikmörk jöfnunar samtalna verðs +10%.

Pappírsreikningur frá Contoso inniheldur eftirfarandi upplýsingar.

| Vara                  | Magn | Einingarverð | Nettóupphæð |
|-----------------------|----------|------------|------------|
| PH2500 - Tölva     | 2        | 2.500,00   | 5.000,00   |
| MM01 – Þráðlaus mús | 2        | 41.00      | 82.00      |
| USB drif             | 200      | 10.05      | 2,010.00   |
| Samtals reikningsupphæð         |          |            | 7,092.00   |

Reikningalínan inniheldur eftirfarandi upplýsingar.

| Vörunúmer           | Magn | Einingarverð | Nettóupphæð línu | Jöfnunarregla    | Magn á innhreyfingarskjali afurða sem á að para | Verðsamsvörun | Samtala verðs jöfnuð |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 - Tölva     | 2        | 2.500,00   | 5.000,00        | Þríhliða jöfnun | Stóðst ekki                         | Stóðst      | Stóðst            |
| MM01 – Þráðlaus mús | 2        | 41,00      | 82,00           | Þríhliða jöfnun | Stóðst ekki                         | Stóðst ekki      | Stóðst            |
| USB drif             | 200      | 10,05      | 2010,00         | Tvíhliða jöfnun   |                                | Stóðst      | Stóðst            |

Athugið eftirfarandi vörur:
-   Fyrir PH2500 – Tölvulína, dálkurinn Magnjöfnun innhreyfingarskjals afurða hefur viðvörunartákn þar sem reikningslínan er ekki jöfnuð við innhreyfingarskjal afurða.
-   Fyrir MM01 – Þráðlaus mús, dálkurinn Magnjöfnun innhreyfingarskjals afurða hefur viðvörunartákn þar sem reikningslínan er ekki jöfnuð við innhreyfingarskjal afurða. Dálkurinn Jöfnun einingarverðs hefur viðvörunartákn þar sem farið er fram úr 2% verðvikmörkum nettóeiningaverðs.
-   Fyrir línu USB-drifs er dálkurinn Magnjöfnun innhreyfingarskjals afurða auður þar sem tvíhliða jöfnun jafnast ekki við magn reikningslínu og magn línu innhreyfingarskjals afurða.

Ef samþykkis er krafist fyrir reikninga sem á að bóka með jöfnunarmisræmi verður að velja Samþykkja bókun með misræmi víxla á Reikningnum samsvarandi upplýsingasíða áður en hægt er að bóka reikning með jöfnunarvillu verðs og jöfnunarvillur magns. Ef samþykkis er krafist, úrvinnslu reikninga getur haldið áfram ef engar aðrar bókunarvillur eru til staðar.


Nánari upplýsingar er að finna í [Yfirlit yfir reikningsjöfnun viðskiptaskulda](accounts-payable-invoice-matching.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]