---
title: Grunnstilla hæfnisvalkosti persónulegs tengiliðar
description: Grunnstilla hæfnisvalkosti fyrir persónulega tengiliði í Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009433"
---
# <a name="configure-personal-contact-eligibility-options"></a>Grunnstilla hæfnisvalkosti persónulegs tengiliðar

[!include [banner](includes/preview-feature.md)]

Þessi grein sýnir þér hvernig á að stilla gerðir af persónulegum tengiliðum til að nota í ávinningi hjá Microsoft Dynamics 365 Human Resources. Persónulegir tengiliðir geta verið rétthafar eða skjólstæðingar. 

1. Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **Hæfiskostir persónulegs tengliðar**.

2. Veljið **Nýtt**.

3. Tilgreina gildi fyrir eftirfarandi reiti:

   | Svæði | Lýsing |
   | --- | --- |
   | **Hæfnisvalkostur** | Einstakt nafn eða kóða fyrir hæfileika til að bera kennsl á hæfisvalkostinn. |
   | **Lýsing** | Stutt lýsing á hæfisvalkosti. |
   | **Hæfniskóði tengiliðar** | Kerfiskóðinn sem lýsir best hæfnisvalkosti einstaklingsins. Hægt er að velja um: <ul><li>Vensl</li><li>Nemandi</li><li>Skjólstæðingur of gamall</li><li>Hreyfihamlaður skjólstæðingur sem er of gamall</li></ul> |
   | **Staða** | Staða hæfisvalkosts. Ef staða fyrir hæfisvalkost er stillt á óvirk geturðu ekki valið þann valkost fyrir persónulegan tengilið fyrir persónulega tengiliði. |
   | **Vensl** | Tilgreinir samband persónulegra tengiliða og starfsmanns. Þessi reitur er aðeins virkur ef hæfnisnúmer tengiliðar er stillt á Samband. |
   | **Aldur** | Hámarksaldur gjaldgengs persónulegs tengiliðar vegna bótakerfisins. Þessi reitur er aðeins virkur ef þú velur samband. Þessi aldur er borinn saman við reiknaðan aldur persónulegra tengiliða. Reiknaður aldur er: (Dagsetning umfjöllunar - fæðingardagur persónulegs tengiliðar / 365). Þessi tala er alltaf heiltala. |

4. Veljið **Vista**. 
