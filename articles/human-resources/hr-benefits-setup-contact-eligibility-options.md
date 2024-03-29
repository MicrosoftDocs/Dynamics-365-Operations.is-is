---
title: Grunnstilla hæfnisvalkosti persónulegs tengiliðar
description: Þessi grein útskýrir hvernig á að stilla hæfisvalkosti fyrir persónulega tengiliði í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803885"
---
# <a name="configure-personal-contact-eligibility-options"></a>Grunnstilla hæfnisvalkosti persónulegs tengiliðar


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein útskýrir hvernig á að stilla gerðir persónulegra tengiliða sem hægt er að nota í fríðindum í Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir eru einstaklingar sem falla undir áætlanir þínar (tengdir einstaklingar) eða sem njóta góðs af áætlunum þínum (viðtakendur). Tengdir einstaklingar eru yfirleitt makar eða börn. Viðtakendur geta verið makar, börn eða foreldrar.

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfiskostir persónulegs tengliðar**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Hæfnisvalkostur** | Einstakt nafn eða kóða fyrir hæfileika til að bera kennsl á hæfisvalkostinn. |
   | **Lýsing** | Stutt lýsing á hæfisvalkosti. |
   | **Hæfniskóði tengiliðar** | Kerfiskóðinn sem lýsir best hæfnisvalkosti einstaklingsins. Hægt er að velja um: <ul><li>Vensl</li><li>Nemandi</li><li>Skjólstæðingur of gamall</li><li>Hreyfihamlaður skjólstæðingur sem er of gamall</li></ul> |
   | **Staða** | Staða hæfisvalkosts. Ef staða á valkosti hæfis er stillt á óvirk geturðu valið hæfisvalkost persónulegs tengiliðar fyrir persónulega tengiliði. |
   | **Vensl** | Tilgreinir samband persónulegra tengiliða og starfsmanns. Þessi reitur er aðeins virkur ef hæfnisnúmer tengiliðar er stillt á Samband. |
   | **Aldur** |Tilgreinir hámarksaldur viðurkennds persónulegs tengiliðs fyrir bótaáætlunina. Þessi reitur er aðeins virkur ef þú velur samband. Þessi aldur er borinn saman við reiknaðan aldur persónulegra tengiliða. Reiknaður aldur er: (Dagsetning umfjöllunar - fæðingardagur persónulegs tengiliðar / 365). Þessi tala er alltaf heiltala.
Fyrir **Oft háð persónulega** aðgengisvalkosti er aldurinn á þessu sviði lágmarksaldur. Til dæmis: ef aldur er stilltur á 18 á valmöguleikanum **Ofháð** valkostinum, þá myndu þeir á framfæri sem eru merktir sem ofháðir og eru 18 ára eða eldri falla undir hæfisvalkostinn.  |

4. Veldu **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
