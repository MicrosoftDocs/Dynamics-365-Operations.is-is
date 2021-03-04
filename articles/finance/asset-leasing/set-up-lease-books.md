---
title: Setja upp leigubækur
description: Þetta efnisatriði lýsir upplýsingum sem unnið er með í leigubókum. Leigubækur innihalda bókhaldsreglur sem ákvarða hvernig leigan er gjaldfærð í kerfinu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444579"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]