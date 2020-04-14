---
title: Fjarlægja kanban-vinnslu úr áætlun
description: Þetta ferli leggur áherslu á fjarlægir í áætluðu kanban-vinnslu úr áætlun með bakfæra staða vinnslu aftur yfir í Ekki áætluð.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b2137268301beb85906bf7fb26c41f6eb09534c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148922"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Fjarlægja kanban-vinnslu úr áætlun

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á fjarlægir í áætluðu kanban-vinnslu úr áætlun með bakfæra staða vinnslu aftur yfir í Ekki áætluð. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir yfirmaður vinnusals eða framleiðslustjóri.


## <a name="find-a-planned-kanban-job"></a>Leita í áætluðu kanban-vinnslu
1. Fara í Framleiðslustýringar > Kanban > Áætlun kanban-vinnslu.
2. Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Velja vinnuflokkur 1250.  
4. Smellið á Velja.
5. Í svæði Birta staða vinnslu, velja "Áætlað".

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Fjarlægja áætlaðar kanban-vinnslu úr áætlun
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið vinnslu sem er með stöðuna Áætluð vinnsla, t.d. með vinnsla frá 19 Desember 2012  
2. Smellið á „Áætlun“ á aðgerðarúðunni.
3. Smellt er á snúa aftur staða vinnslu.
4. Smellið á „Í lagi“.
    * Þetta er bakfæra stöðu vinnslunnar úr "Áætlað" í 'Ekki áætluð' og fjarlægja hana úr spjald ferli.   

