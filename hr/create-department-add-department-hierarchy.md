---
title: "Stofna deild og tengja hana við stigveldi deildar"
description: "Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis. Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði. Hægt er að nota deildir til að gefa skýrslur um virk svið. Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ee51abe108b3bc0aabc764b991222db6d185e532
ms.lasthandoff: 03/31/2017


---

# <a name="create-a-department-and-associate-it-with-the-department-hierarchy"></a>Stofna deild og tengja hana við stigveldi deildar

Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis. Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði. Hægt er að nota deildir til að gefa skýrslur um virk svið. Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.

deild gæti innifalið hóp af kostnaðarstöðum. Hægt er að úthluta stöðum til deilda. Deild er smellt á **Mannauður**&gt;**Deildir**&gt;**Deild**. Eftirfarandi tafla lýsir svæðum sem eru tiltækir.

| Reitur               | Lýsing                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Heiti                | Færið inn heiti fyrir deildina.                                                                                                                                                                                  |
| Deildarnúmer   | Sjálfgefið gildi kann að vera myndað sjálfkrafa ef kóði númeraraðar er úthlutað á  **tilvísunarnúmer fyrirtækis ** á síðunni **númeraröð**.                                                 |
| Leita að nafni         | Færið inn nafn eða skammstöfun sem hægt er að nota til að leita að deildinni.                                                                                                                                            |
| Athugasemd                | Færðu inn viðbótarupplýsingar hér.                                                                                                                                                                            |
| Í stigveldi        | Valinn gátreitur getur til kynna að deildin er innifalin í stigveldi deildar. Upplýsingar um það hvernig skal bæta við deild við stigveldi deildar, Sjá upplýsingar síðar í þessari grein. |
| DUNS-númer         | DUNS stendur fyrir Data Universal Number System. Þetta er níu-stafa númer sem er gefið út af Dun & Bradstreet.                                                                                                     |
| Yfirmaður             | Velja einstaklinginn sem hefur umsjón með deildinni                                                                                                                                                                    |
| Aðsetur           | Bæta við upplýsingar um aðsetur fyrir deildina. Til dæmis, bæta við póstfangi byggingar sem deild er í.                                                                          |
| Tengslaupplýsingar | Bæta við tengslaupplýsingum fyrir deild. Til dæmis er bætt við símanúmer fyrir þjónustuborð í deild.                                                                                           |

Til að bæta deild við stigveldi deildar, skal fylgja þessum skrefum:

1.  Smellið á **Mannauður**&gt;**Deildir**&gt;**stigveldi Deildar**.
2.  Smellið á **Breyta**, og veljið síðan fyrirtæki sem deild ætti að vera undir.
3.  Smellið á **Setja inn**, og veljið **Deild** á listanum.
4.  Í lista yfir deildir sem birtist skal velja deild til að bæta við stigveldið.
5.  Vista breytingarnar. Boð sem drög stigveldi hefur verið stofnuð.
6.  Þegar þú afskriftareglur eru tilbúnar, smellið á **Birta** í hönnuði stigveldis. Hægt er að færa inn gildisdagsetningu sem tilgreinir hvenær birt stigveldi. Til dæmis til að bæta við nýjum deild við upphaf næsta almanaksárs, skal stilla gildisdagsetningu til 1. Janúar á nýja almanaksárinu. Breytingar á stigveldinu tekur gildi á þeim degi.



