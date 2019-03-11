---
title: Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu
description: Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "341098"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum. Þetta er gert með því að nota öryggisbirgðabók. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verk er ætluð fyrir framleiðslustjóra, sem hjálpar við að viðhalda lágmarks þekju.


## <a name="create-a-new-safety-stock-journal-name"></a>Stofnið nýja heiti öryggisbirgðabókar.
1. Fara í Heiti öryggisbirgðabóka
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn "efni".
4. Í reitinn Lýsing skal slá inn "Efni".
5. Lokið síðunni.

## <a name="create-a-safety-stock-journal"></a>Stofna öryggisbirgðabók
1. Fara í Útreikningur öryggisbirgða
2. Smellið á „Nýtt“.
3. Sláið inn eða veldu gildi í reitnum heiti.
    * Velja skal nafn öryggisbirgðabókar sem þú stofnaðir, til dæmis, Efni.  
4. Smellið á Stofna línur .
5. Dagsetning er rituð í reitinn Frá dags.
    * Stilla dagsetningu á „02-01-2015“.  
6. Í reitinn Til dagsetningar skal slá inn dagsetningu.
    * Stilla dagsetningu á 2015-12-30  
7. Smellið á „Í lagi“.
    * Þetta stofnar línur fyrir víddir sem hafa birgðafærslur.  

## <a name="calculate-proposal"></a>Reikna tillögu
1. Smella á Reikna tillögu
2. Veldu valkostinn Nota meðaltal úthreyfinga á afhendingartíma.
3. Stilla Margfeldisstuðullinn á "10"
    * Margföldunarstuðullinn er notaður til að leiðrétta tillöguna. Þar sem sýnigögn hefur aðeins nokkrar færslur, þarf að stilla stuðulinn til að fá raunhæfa tillögu.  
4. Smellið á „Í lagi“.
    * Skruna niður til að finna M0002 og M0003. Skoða dálkinn reiknað lágmarksmagn.   

## <a name="update-minimum-quantity"></a>Uppfæra lágmarksmagn
1. Í reitinn nýtt lágmarksmagn skal slá inn númer.
    * Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu. Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi. T.d. er hægt að færa inn Reiknuð lágmarksmagn á þessu svæði fyrir M0002 sem er með vöruhús 12 .  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Til dæmis, er hægt að velja M0002 sem er með vöruhús 12 .  
3. Í reitinn nýtt lágmarksmagn skal slá inn númer.
    * Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu. Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Bóka nýtt lágmarksmagn og villuleita niðurstöður
1. Smellið á „Bóka“.
2. Smellið á „Í lagi“.
3. Smellið til að elta tengilinn í reitnum vörunúmer.
4. Smellið til að elta tengilinn í reitnum vörunúmer.
5. Smellið á „Áætlun“ á aðgerðarúðunni.
6. Smellt er á vöruþekju.
    * Athugaðu að Lágmarksmagn hefur verið uppfærður með nýtt lágmarksmagn úr öryggisbirgðabók.  

