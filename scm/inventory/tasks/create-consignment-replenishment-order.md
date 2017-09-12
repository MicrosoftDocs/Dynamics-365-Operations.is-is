---
title: "Stofna áfyllingarpöntun vörusendingar"
description: "Þessi verklýsing sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 5e268f640be11b0905457ff6b7697c90411f53e5
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Stofna áfyllingarpöntun vörusendingar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir. Hún sýnir einnig hvernig á að skrá innhreyfingar afurða þannig að vörusendingabirgðir eru skráðar sem lagerbirgðir í lánardrottins. Þetta ferli myndi er yfirleitt framkvæmt af innkaupaaðila. Hægt er að nota þessar leiðbeiningar í sýnifyrirtækinu USMF. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.




## <a name="create-a-consignment-replenishment-order"></a>Stofna áfyllingarpöntun vörusendingar
1. Fara í Innkaup og uppruni > vörusending > vörusending áfylling Pantanir.
2. Smellið á „Nýtt“.
3. Í svæðinu Lánardrottnalykill skal slá inn 'US-104'.
    * Velja þarf lánardrottinn sem skráður er sem er eigandi á síðunni birgðaeigendur.  
4. Smellið á „Í lagi“.
5. Smellið á „Bæta við línu“.
6. Í svæðið vörunúmer færðu inn 'M9211CI.'.
    * Þú verður að velja vöru sem er uppsett fyrir vörusendingabirgðir.  
7. Færið inn númer í reitnum „Magn“.
8. Dagsetning er rituð í reitinn umbeðin dagsetning afhendingar:.
    * Umbeðnar og staðfestar dagsetningar eru notaðar af MRP-vélinni (vél lánstímaálags) vegna áætlaðrar komu varningsins.  
9. Dagsetning er rituð í reitinn staðfestur afhendingardagur.
10. Víkkið út hlutann „Upplýsingar um línu“.
11. Smellið á flipann Birgðavíddir.
12. Til að sýna eiganda í reitnum eigandi birgðavídda, skal endurnýja síðuna.
    * Lánardrottininn US-104 er nú skráður sem eiganda.  

## <a name="check-the-inventory-transaction-status"></a>Athugaðu staða birgðafærslunnar.
1. Smellið á birgðir.
2. Smella á Færslur.
3. Í listanum skal merkja valda línu.
    * Athugið svæðið móttaka er stillt á Pantað.  
4. Lokið síðunni.

## <a name="receive-items"></a>Taka á móti vörum
1. Smellið á „Innhreyfingarskjal“.
2. Sláið inn gildi í reitinn Ytra innhreyfingarskjal afurða.
3. Í reitinn magn skal slá inn númer sem er lægra en númerið sem er sýnt þar.
4. Smellið á „Í lagi“.

## <a name="check-the-on-hand-inventory"></a>Athuga birgðir á lager.
1. Smellið á birgðir.
2. Smelltu Á lager.
3. Smelltu á Yfirlit.
    * Vörur sem hafa verið mótteknar sem vörusendingabirgðir í eigu lánardrottins eru tiltæk á lager. Eftirstandandi magn á áfyllingarpöntun vörusendingar er birt í reitnum Samtals pantað.  
4. Lokið síðunni.
5. Smellið á „Loka“.

