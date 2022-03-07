---
title: Stofna deildir og setja þær inn í deildastigveldið
description: Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis. Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8571b254a3dcdeaf562a97f165b8124f04ae7e6d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068895"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Stofna deildir og setja þær inn í deildastigveldið


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Deild er rekstrareining sem stendur fyrir flokk eða virkt svið fyrirtækis. Deoæd ber ábyrgð á tilteknu sviði innan fyrirtækisins, svo sem sölu, bókhald eða mannauði. Hægt er að nota deildir til að gefa skýrslur um virk svið. Deildir gætu haft ábyrgðarsvið fyrir hagnað og tap.

deild gæti innifalið hóp af kostnaðarstöðum. Hægt er að úthluta stöðum til deilda. Til að stofna Deild er smellt á **Mannauður** &gt; **Deildir** &gt; **Deild**. Eftirfarandi tafla lýsir svæðum sem eru tiltæk.

| Reitur               | Lýsing                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Heiti**                | Færið inn heiti fyrir deildina.                                                                                                                                                                                  |
| **Deildarnúmer**   | Sjálfgefið gildi kann að vera myndað sjálfkrafa ef kóði númeraraðar er úthlutað á **tilvísunarnúmer fyrirtækis** á síðunni **númeraröð**.                                                 |
| **Leita að nafni**         | Færið inn nafn eða skammstöfun sem hægt er að nota til að leita að deildinni.                                                                                                                                            |
| **Athugasemd**                | Færðu inn viðbótarupplýsingar hér.                                                                                                                                                                            |
| **Í stigveldi**        | Valinn gátreitur getur til kynna að deildin er innifalin í stigveldi deildar. Upplýsingar um það hvernig skal bæta við deild við stigveldi deildar, Sjá upplýsingar síðar í þessari grein. |
| **DUNS-númer**         | DUNS stendur fyrir Data Universal Number System. Þetta er níu-stafa númer sem er gefið út af Dun & Bradstreet.                                                                                                     |
| **Yfirmaður**             | Velja einstaklinginn sem hefur umsjón með deildinni                                                                                                                                                                    |
| **Aðsetur**           | Bæta við upplýsingar um aðsetur fyrir deildina. Til dæmis, bæta við póstfangi byggingar sem deild er í.                                                                          |
| **Tengslaupplýsingar** | Bæta við tengslaupplýsingum fyrir deild. Til dæmis er bætt við símanúmer fyrir þjónustuborð í deild.                                                                                           |

Til að bæta deild við stigveldi deildar, skal fylgja þessum skrefum:

1.  Smellt er á **Mannauður** &gt; **Deildir** &gt; **Deildastigveldi**.
2.  Smellið á **Breyta**, og veljið síðan fyrirtæki sem deild ætti að vera undir.
3.  Smellið á **Setja inn**, og veljið **Deild** á listanum.
4.  Í lista yfir deildir sem birtist skal velja deild til að bæta við stigveldið.
5.  Vista breytingarnar. Þú færð Boð um að drög að stigveldi hefur verið stofnuð.
6.  Þegar þú ert tilbúinn, smellið á **Birta** í hönnuði stigveldis. Hægt er að færa inn gildisdagsetningu sem tilgreinir hvenær stigveldi skuli birt. Til dæmis til að bæta við nýjum deild við upphaf næsta almanaksárs, skal stilla gildisdagsetningu til 1. Janúar á nýja almanaksárinu. Breytingar á stigveldinu tekur gildi á þeim degi.

## <a name="steps-for-creating-a-department"></a>Skref til að búa til deild
Sjá greinina [Skilgreina nýjar deildir](./hr-personnel-define-departments.md) fyrir skref fyrir skref aðferð til að búa til nýja deild. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
