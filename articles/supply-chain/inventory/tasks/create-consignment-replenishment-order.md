---
title: Stofna áfyllingarpöntun vörusendingar
description: Þessi verklýsing sýnir hvernig skal stofna áfyllingarpöntun vörusendingar þar sem hægt er að rekja áætlaða afhendingu frá lánardrottni inn í vörusendingabirgðir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3e33008d04ea8bb7d145c7b63cec23a4a45dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "315499"
---
# <a name="create-a-consignment-replenishment-order"></a>Stofna áfyllingarpöntun vörusendingar

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

