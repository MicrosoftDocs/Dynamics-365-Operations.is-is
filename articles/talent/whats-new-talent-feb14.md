---
title: Hvað er nýtt eða breytt í Dynamics 365 for Talent (14. febrúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5f96dd60652705de820e0661d417dcaee8143561
ms.sourcegitcommit: 5384200c3e33510c5b3ac31f2b22443e1076251f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2019
ms.locfileid: "390666"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Hvað er nýtt eða breytt í Dynamics 365 for Talent (14. febrúar 2019)

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Talent.

## <a name="changes-in-attract"></a>Breytingar í Attract
Það eru minniháttar villuleiðréttingar með í þessari útgáfu.

## <a name="changes-in-onboarding"></a>Breytingar á nýliðun
Það eru minniháttar villuleiðréttingar með í þessari útgáfu.
 
## <a name="changes-in-core-hr"></a>Breytingar í Core HR 
**Smíði 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>Einingin fyrir föst laun starfsmanns flytur ekki út allar færslur
Með þessari breytingu mun einingin **Föst laun starfsmanns** núna flytja út allar færslur. Eininguna er hægt að nota til að búa til og uppfæra núverandi færslur fyrir föst laun starfsmanna. 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>Lokadagur ráðningar tekur ekki tillit til æskilegrar stillingar á tímabelti starfsmanns
Lokadagar ráðningar taka nú tillit til tímabeltis sem notandi kýs þegar ráðning er búin til eða kláruð hjá fyrirtæki.
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Bresk aðsetur birtast í Analytics sem austur-svissnesk aðsetur
Í þessari útgáfu hefur breyting verið gerð til að leiðrétta skekkju í aðsetrum í **Starfsmannastjórnun**, skýrslunni „Starfsmannafjöldi eftir staðsetningu“.
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>Starfslokakóði er ekki fylltur út í stöðuverkefnaskrám starfsmanns þegar stöðunni er lokað
Breyting hefur verið gerð svo ástæðukóði starfsloka verði sjálfgefinn þegar stöðuverkefni starfsmanns er lokað.

### <a name="new-entity-created-for-job-compensation-levels"></a>Ný eining búin til fyrir launastig starfs
Ný eining fyrir gagnastjórnunarramma (DMF) var búin til. Einingin gerir kleift að búa til og uppfæra launastig, markaðsvirði og upplýsingar könnunar fyrir hvert starf sem er skilgreint í kerfinu.
