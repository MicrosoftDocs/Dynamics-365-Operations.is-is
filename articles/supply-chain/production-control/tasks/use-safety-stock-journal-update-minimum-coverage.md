---
title: Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu
description: Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum.
author: ChristianRytt
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 478dd85abebf76dd264e93bcbe3f218a0ff0a5a8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916807"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Nota færslubók öryggisbyrgða til að uppfæra lágmarkstryggingu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að reikna lágmarks þekju tillögur byggðar á sögulegum færslum og uppfæra svo vöruþekju ásamt tillögum. Þetta er gert með því að nota öryggisbirgðabók. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verk er ætluð fyrir framleiðslustjóra, sem hjálpar við að viðhalda lágmarks þekju.


## <a name="create-a-new-safety-stock-journal-name"></a>Stofnið nýja heiti öryggisbirgðabókar.
1. Í **skoðunarrúðunni** ferðu í **Aðaláætlanagerð > Uppsetning > Heiti færslubókar öryggisbirgða**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Heiti** skal slá inn "efni".
4. Í reitinn **Lýsing** skal slá inn "Efni".
5. Lokið síðunni.

## <a name="create-a-safety-stock-journal"></a>Stofna öryggisbirgðabók
1. Í **skoðunarrúðunni** ferðu í **Aðaláætlanagerð > Aðaláætlanagerð > Keyra > Útreikningur öryggisbirgða**.
2. Smellt er á **Nýtt**.
3. Sláið inn eða veldu gildi í reitnum **Heiti**. Velja skal nafn öryggisbirgðabókar sem þú stofnaðir, til dæmis, Efni.  
4. Smelltu á **Stofna línur**.
5. Í reitnum **Frá dags.** færirði inn dagsetningu.  
6. Í reitnum **Til dags.** færirðu inn dagsetningu.
7. Smellt er á **OK**. Þetta stofnar línur fyrir víddir sem hafa birgðafærslur.  

## <a name="calculate-proposal"></a>Reikna tillögu
1. Smelltu á **Reikna tillögu**.
2. Veldu valkostinn **Nota meðaltal úthreyfinga á afhendingartíma**.
3. Stilltu **Margfeldisstuðullinn** á "10". Margföldunarstuðullinn er notaður til að leiðrétta tillöguna. Þar sem sýnigögn hefur aðeins nokkrar færslur, þarf að stilla stuðulinn til að fá raunhæfa tillögu.  
4. Smellt er á **OK**. Skruna niður til að finna M0002 og M0003. Skoða dálkinn **Reiknað lágmarksmagn**.   

## <a name="update-minimum-quantity"></a>Uppfæra lágmarksmagn
1. Í reitinn **Nýtt lágmarksmagn** skal slá inn tölu. Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu. Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi. T.d. er hægt að færa inn Reiknuð lágmarksmagn á þessu svæði fyrir M0002 sem er með vöruhús 12 .  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Til dæmis, er hægt að velja M0002 sem er með vöruhús 12 .  
3. Í reitinn **Nýtt lágmarksmagn** skal slá inn tölu. Uppfæra nýja lágmarksmagn til að samsvara gildinu í útreiknaða lágmarksmagninu. Ef Reiknuð lágmarkið er núll er hægt að færa inn viðkomandi framvirk gildi.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Bóka nýtt lágmarksmagn og villuleita niðurstöður
1. Smelltu á **bóka.**
2. Smellt er á **OK**.
3. Smellið til að fylgja tenglinum í reitnum **Vörunúmer**.
4. Smellið til að fylgja tenglinum í reitnum **Vörunúmer**.
5. Í **Aðgerðarrúðunni** er smellt á Áætlun.
6. Smelltu á **Vöruþekju**. Athugaðu að **Lágmarksmagn** hefur verið uppfært með nýju lágmarksmagni úr öryggisbirgðabók.  

