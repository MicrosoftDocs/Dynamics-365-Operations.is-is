---
title: Setja upp leigubækur
description: Þessi grein lýsir þeim upplýsingum sem geymdar eru í leigubókum. Leigubækur innihalda bókhaldsreglur sem ákvarða hvernig leigan er gjaldfærð í kerfinu.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ee8cb3c827d590a5eb91121fe4510fbc56c13d9a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903219"
---
# <a name="set-up-lease-books"></a>Setja upp leigubækur

[!include [banner](../includes/banner.md)]

Leigubækur innihalda bókhaldsreglur sem ákvarða hvernig leigan er gjaldfærð í kerfinu. Til viðbótar við bókhald á grundvelli reiðufjár styður eignarleiga eftirfarandi staðla:

- Almennt viðurkenndar reikningsskilareglur í Bandaríkjunum (US GAAP)
- Efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842)
- ASC 840
- Alþjóðlegum reikningsskilastaðli 16 (IFRS 16)
- Alþjóðlegum reikningsskilastaðli 17 (IAS 17)

Fylgdu þessum skrefum til að búa til leigubók.

1. Opnið **Eignarleiga \> Uppsetning \> Leigubækur**.
2. Veljið **Nýtt** til að bæta við bók.
3. Stilltu eftirfarandi reiti.

    | Nafn                                     | lýsing |
    |------------------------------------------|-------------|
    | Bókunarlag                            | Veljið bókunarlagið sem á að nota. Sérver bók sem tengd er leigu er uppsett fyrir ákveðið bókunarlag. Hvert bókunarlag er með mismunandi bókunartilgang. |
    | Gerð leigu                               | Veljið hvort gerð leigusamningsins verði flokkuð sjálfkrafa eða skilgreind fyrirfram sem fjármögnunar- eða rekstrarleigusamningur. |
    | Bókhaldsrammi                     | Velja rammann sem tengist bókinni. |
    | Leigutími/Uppsetning nýtingartíma          | Forritið flokkar leigusamninginn sem fjármögnunarleigusamning ef gerð leigusamnings er stillt á **Sjálfvirka stillingu** og ef leigutíminn á nýtingartíma eignar er lengri en eða jafnt og prósentuhlutfallið sem fært er inn í þetta svæði.  |
    | Uppsetning á núvirði / gangvirði eignar   | Færið inn heiltölu til að skilgreina þröskuldinn sem mun ákvarða gerð leigunnar. Ef núvirði lágmarks leigugreiðslna í framtíðinni er hærra en skilgreint virði notanda í uppsetningu bókarinnar og ef flokkun leigusamnings bókarinnar er stillt á sjálfvirka stillingu flokkar kerfið leigusamninginn sem fjármögnunarleigusamning. |
    | Skammtímaþröskuldur                     | Sláið inn fjölda mánaða sem á að nota sem mörk fyrir skammtímaleigur. Ef leigutíminn er styttri en eða jafnt og mánaðarfjöldinn sem færður er inn hér, flokkar kerfið leigusamninginn sem skammtímaleigusamning og aðferðin frestaðar leigugreiðslur verður notuð. |
    | Mörk verðlítillar eignar                      | Færa skal inn upphæð sem á að nota sem þröskuld fyrir leigu verðlítillar eignar. Ef gangvirði eignar er jafnt og eða minna en gildi sem er slegið inn hér mun kerfið flokka leigusamninginn sem verðlítinn og frestaðar leigugreiðslur verða notaðar. |
    | Greiða lánardrottni                            | Stillið þennan valkost á **Yes** til að leyfa bókun leigugreiðslna sem reiknings á lánardrottnalykil sem tilgreindur er í hverjum leigusamningi. Þegar leigugreiðsla er bókuð verður lánardrottnalykill kreditfærður. Ef þessi valkostur er stilltur á **Nei**, verður lykillinn sem er tilgreindur fyrir bókunargerðina **Leigugreiðsla** á síðunni **Færibreytur bókunargerðar** kreditfærður þess í stað. |
    | Reglur leigusamnings                       | Velja hefð samninginn fyrir upphafstíma leigu:<ul><li><b>Ekkert</b> – nota upphafsdagsetningu leigu sem upphafsdagsetningu.</li><li><b>Heill mánuður</b> - Notið fyrsta dag mánaðarins sem upphafsdag sem leigusamningingur fellur undir.</li></ul><p>Ef <b>Ekkert</b> er valið er hætta á að skuldfærðar afskriftir og afskriftaráætlanir eigna muni safnast upp og bóka útgjöld í miðjum mánuðinum í stað mánaðarloka. Með því að velja <b>Heill mánuður</b> er tryggt að kerfið byrji að gera grein fyrir leigunni á fyrsta degi mánaðarins og að kostnaður fyrir heilan mánuð verði uppsafnaður og bókaður á síðasta degi mánaðarins.</p><p><strong>Athugið:</strong> Það verður að kveikja á eiginleikanum fyrir viðteknar reglur leigusamninga í gegnum eiginleikastjórnun. Á vinnusvæðinu <b>Eiginleikastjórnun</b> skal finna og velja eiginleikann sem heitir <b>Viðtekin regla leigusamnings fyrir eignarleigu</b> og velja því næst <b>Virkja núna</b>.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
