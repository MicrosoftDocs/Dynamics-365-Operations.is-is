--- 
title: "Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu"
description: "Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d278b20724006ec3b3aa557738e8b130ca2bba15
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum. Þetta er gert með því að nota öryggisbirgðabók. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verk er ætluð fyrir framleiðslustjóra, sem hjálpar við að viðhalda lágmarks þekju.


## Stofnið nýja heiti öryggisbirgðabókar.
1. Fara í Heiti öryggisbirgðabóka
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn "efni".
4. Í reitinn Lýsing skal slá inn "Efni".
5. Lokið síðunni.

## Stofna öryggisbirgðabók
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

## Reikna tillögu
1. Smella á Reikna tillögu
2. Veldu valkostinn Nota meðaltal úthreyfinga á afhendingartíma.
3. Stilla Margfeldisstuðullinn á "10"
    * Margföldunarstuðullinn er notaður til að leiðrétta tillöguna. Þar sem sýnigögn hefur aðeins nokkrar færslur, þarf að stilla stuðulinn til að fá raunhæfa tillögu.  
4. Smellið á „Í lagi“.
    * Skruna niður til að finna M0002 og M0003. Skoða dálkinn reiknað lágmarksmagn.   

## Uppfæra lágmarksmagn
1. Í reitinn nýtt lágmarksmagn skal slá inn númer.
    * Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu. Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi. T.d. er hægt að færa inn Reiknuð lágmarksmagn á þessu svæði fyrir M0002 sem er með vöruhús 12 .  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Til dæmis, er hægt að velja M0002 sem er með vöruhús 12 .  
3. Í reitinn nýtt lágmarksmagn skal slá inn númer.
    * Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu. Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.  

## Bóka nýtt lágmarksmagn og villuleita niðurstöður
1. Smellið á „Bóka“.
2. Smellið á „Í lagi“.
3. Smellið til að elta tengilinn í reitnum vörunúmer.
4. Smellið til að elta tengilinn í reitnum vörunúmer.
5. Smellið á „Áætlun“ á aðgerðarúðunni.
6. Smellt er á vöruþekju.
    * Athugaðu að Lágmarksmagn hefur verið uppfærður með nýtt lágmarksmagn úr öryggisbirgðabók.  


