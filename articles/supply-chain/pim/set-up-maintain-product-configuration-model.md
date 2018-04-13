---
title: "Setja upp afbrigðalíkan afurðar"
description: "Þessi grein lýsir því hvernig afbrigðalíkan afurðar er sett upp og stofnað."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 8504eb789b0d449cf2e29d4314d189dc0b8a6b43
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---

# <a name="set-up-a-product-configuration-model"></a>Setja upp afbrigðalíkan afurðar

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig afbrigðalíkan afurðar er sett upp og stofnað.

| Verkefni                                                        | lýsing                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stofna afurðarsniðmát                                    | Stofna afurðarsniðmát úr **afurðarsniðmát** listanum. Losaðu afurðarsniðmátið í öll viðeigandi fyrirtæki. Fyrir afurðarsniðmát sem er notað sem útgáfu fyrir afbrigðalíkan afurðar eða sem undirþáttagerð, verður **skorðuskilgreiningu** að vera valinn sem afbrigðistækni, og skilgreiningarvíddin verður að vera valin aðeins fyrir afurðarvíddarflokknum. |
| Stofna íhluti                                          | Stofna íhluti á **Íhluti** síðu. Íhlutir eru grunneiningar afbrigðalíkans afurðar geta verið endurnýttir í mörgum afbrigðalíkan afurðar.                                                                                                                                                                                                                      |
| Stofna gerð eiginda.                                     | Stofna gerðir eiginda í á **gerðir Eiginda** síðu. Gerðir eiginda tilgreina safn gagnagerða fyrir eigindir sem eru notaðar í afbrigðalíkani afurðar. Eigindir af geðinni **Boole**, **Texta** með föstum lista og **Heiltala** með ýmsum gerðum lista sett af gildum sem eru tiltæk þegar þú skilgreinir afurðarafbrigði byggt á afbrigðalíkan afurðar.       |
| Stofna afbrigðalíkan afurðar                       | Skoða afbrigðalíkan afurðar á **nýtt afbrigðalíkan afurðar** síðu                                                                                                                                                                                                                                                                                                              |
| Bæta eigindum við afbrigðalíkan afurðar.            | Stofna eigind á **eigindir** flýtiflipa á **afbrigðalíkans afurðar sem byggir á Skorðum**síðunni Eigindir lýsa eiginleikum afbrigðalíkans afurðar.                                                                                                                                                                                                       |
| Bæta skorðum við afbrigðalíkan afurðar.           | Stofna skorður á **skorður** flýtiflipa á **afbrigðalíkans afurðar sem byggir á Skorðum**síðunni Skorður eru takmarkanir sem afurðarafbrigði verður að uppfylla. Skorður eru annað hvort segð eða töfluskorðum.                                                                                                                                 |
| Bæta undiríhlutum við afbrigðalíkan afurðar.         | Stofna undiríhluti á **undiríhlutir** flýtiflipa á **afbrigðalíkans afurðar sem byggir á Skorðum**síðunni Undiríhlutir tengjast íhluti og eru tengdar við vörur sem tákna á undiríhlutinn.                                                                                                                                                                       |
| Bæta notendaskilyrðum við afbrigðalíkan afurðar.     | Notendakröfur eru svipaðar undiríhlutir en þeir ekki vísa til vöru. Hægt er að líta á notendakröfur sem Skuggauppskrift. Allar uppskriftalínur eða leiðaraðgerðir sem eru settar beint undir notendakröfur verður að vera dregin saman í yfirhlutinn.                                                                                                                       |
| Bæta uppskriftarlínum við afbrigðalíkan afurðar.             | Stofna uppskriftarlína á **uppskriftarlína** flýtiflipa á **afbrigðalíkans afurðar sem byggir á Skorðum**síðunni Uppskriftarlínur standa fyrir hluti sem þarf til að búa til afbrigði afurðarinnar.                                                                                                                                                                                                 |
| Bæta leiðaraðgerð við afbrigðalíkan afurðar.      | Stofna leiðaraðgerðir á **leiðaraðgerðir** flýtiflipa á **afbrigðalíkans afurðar sem byggir á Skorðum**síðunni Leiðaraðgerðir tákna skref í röð skrefa sem eru framkvæmd til að gera afbrigði afurðarinnar.                                                                                                                                                    |
| Stofna virk útgáfa fyrir afbrigðalíkan afurðar | Stofna virk útgáfa fyrir afbrigðalíkan afurðar á síðunni **útgáfur** Útgáfa er sambandið milli afbrigðalíkans afurðar og afurðarsniðmát. Hægt er að skilgreina afbrigðalíkan afurðar virkrar útgáfu úr sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun.                                                               |
| Prófa afbrigðalíkan afurðar                         | Prófa afbrigðalíkan afurðar úr annað hvort **upplýsingum afbrigðalíkans afurðar sem byggir á Skorðum** síðu eða **listi yfir afbrigðalíkan afurðar** síðu Prófun á  afbrigðalíkan afurðar gerir hermingu á skilgreiningarferli vörulíkans skilgreiningarferlið sem kemur upp við meðhöndlun pantana.                                                                                                |
| Skoða sniðmát afbrigðalíkans afurðar                | Stofna afbrigðalíkan afurðar á **grunnstillingarsniðmát**síðu grunnstillingarsniðmát inniheldur gildi fyrir eiginleika í afbrigðalíkani afurðar. Veljið eigindargildi á í **skilgreiningarlína** síðu. Hægt er að velja að hlaða grunnstillingarsniðmáti vörulíkansvið skilgreiningu vörulíkans.                                                   |
| Skilgreina vöru                                          | Hægt er að skilgreina afbrigðalíkan afurðar úr sölupöntun, sölutilboði, innkaupapöntun eða framleiðslupöntun.                                                                                                                                                                                                                                                                           |






