---
title: Grunnstilla hæfnisvalkosti persónulegs tengiliðar
description: Grunnstilla hæfnisvalkosti fyrir persónulega tengiliði í Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 071523e2a1e9de6f0ed2b77e4ad6802efb0073f7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558250"
---
# <a name="configure-personal-contact-eligibility-options"></a>Grunnstilla hæfnisvalkosti persónulegs tengiliðar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði útskýrir hvernig á að skilgreina gerðir persónulegra tengiliða sem hægt er að nota í fríðindum í Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir eru einstaklingar sem falla undir áætlanir þínar (tengdir einstaklingar) eða sem njóta góðs af áætlunum þínum (viðtakendur). Tengdir einstaklingar eru yfirleitt makar eða börn. Viðtakendur geta verið makar, börn eða foreldrar.

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
   | **Aldur** | Hámarksaldur gjaldgengs persónulegs tengiliðar vegna bótakerfisins. Þessi reitur er aðeins virkur ef þú velur samband. Þessi aldur er borinn saman við reiknaðan aldur persónulegra tengiliða. Reiknaður aldur er: (Dagsetning umfjöllunar - fæðingardagur persónulegs tengiliðar / 365). Þessi tala er alltaf heiltala. |

4. Veljið **Vista**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
