---
title: Áætla kanban-vinnslu
description: Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cab3af0802ae6fa942460cfdd9c0819e1d31d4b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579089"
---
# <a name="schedule-kanban-jobs"></a>Áætla kanban-vinnslu

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur. Ferli "Undirbúa ferli kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta verk er ætluð fyrir yfirmaður vinnusals og framleiðslustjóri sem vinnur með kanban.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Velja kanban-vinnslur fyrir vinnuflokks
1. Fara í Framleiðslustýringar > Kanban > Áætlun kanban-vinnslu.
2. Útvíkka upplýsingakassa Afkastageta Tímabilsins
    * Útvíkka kanban-upplýsingakassa.  
3. Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal merkja valda línu.
    * Velja vinnuflokkur 1250. Þetta sía yfirlitið til að birta aðeins vinnslur fyrir vinnuflokk 1250.  
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á Velja.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Áætlun kanban-vinnslu í fyrsta tímabilinu tiltæk
1. Í listanum skal merkja valda línu.
    * Veljið fyrstu línunni á listanum sem hefur stöðuna Ekki áætlað. Brotinni línu í reitnum staða Vinnslu gefur til kynna Ekki áætluð.  
2. Smellt er á Áætlun.
    * Þetta mun áætla kanban-vinnslu á fyrsta tiltæka tímabili.  
    * Athugið að kanban-vinnslu er fluttur í lok lista þar sem hún hefur verið bætt við tímabil sem hefjast frá dagsetningunni í dag.  
    * Ef tímabil sem hefjast frá dagsetningunni í dag er bókað til fulls mun vinnslu færð á fyrsta tiltæka tímabils.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Raða tvær kanban-vinnslur fyrir tiltekinn dag
1. Í listanum skal velja línu 1.
    * Þú ættir að sjá í fyrstu línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.  
2. Í listanum skal velja línu 2.
    * Þú ættir að sjá í annarri línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu. Nú ertu með fyrstu tveimur vinnslum sem valin.  
3. Smellt er á Áætlun frá dagsetningu til að opna svargluggann fellilistanum.
4. Merkja eða afmerkja Hnekkja viðbrögðum við skorti á afkastagetu reitnum.
    * Þessi valkostur gerir kleift að hnekkja sjálfgefin viðbrögð við skorti á afköstum.  
5. Í reitnum viðbrögð við skorti á afkastagetu Velja 'Bæta við umbeðið tímabil'.
    * Þessi valkostur munu tryggja að vinnslunni er bætt við umbeðið tímabil, óháð því ef vinnuflokkur gæti verið ofhlaðinn.  
6. Smellt er á Áætlun.
    * Athugið að báðir vinnslur er bætt við umbeðið tímabil.  
    * Hægt er að sjá álag fyrir hvert tímabil í hlutanum afkastageta Tímabilsins. Reiturinn Notkun sýnir áætlaða notkun á þessu tímabili. Ef áætluð notkun er hærri en tiltæk afkastageta í þetta tímabil er valið ofhlaðin notkun.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]