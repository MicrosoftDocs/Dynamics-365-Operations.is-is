--- 
title: "Skrá reikning lánardrottins í reikningabók"
description: "Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 127875443da1d43783440083b11afd423f2a12fe
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Skrá reikning lánardrottins í reikningabók

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir. Dæmi um þessa gerð reiknings innihalda kostnað fyrir vörur eða þjónustu.  Þessi skráning notar sýnigögn USMF fyrirtækis

1. Fara í Viðskiptaskuldir > Vinnusvæði > Færsla fyrir reikning lánardrottins.
2. Smellt er á Ný reikningabók.
3. Smellið á „Nýtt“.
4. Færið inn heiti færslubókar eða smellið á fellilistahnappinn til að opna leitina, í svæðið Heiti.
5. Sláið inn gildi í reitnum „Lýsing“.
6. Smellið á „Línur“.
    * Færa inn bókunardagsetningu sem mun uppfæra Fjárhag, í svæði Dagsetning.  
7. Í reitnum Lykill skal færa inn Lánardrottnalykil.
8. Í reitnum Reikningur færirðu inn númer reiknings.
9. Í reitinn Lýsing skal slá inn gildi.
10. Í reitnum Kredit skal slá inn tölu.
11. Í svæðinu Mótlykill, færið inn lykilnúmer eða smella á fellilistahnappinn til að opna leitina.
    * Vsk-flokkinn eru sjálfgefnar úr lykli lánardrottins.  
    * Vsk-flokkur Vöru eru sjálfgefnar úr aðallykillinn sem tilgreindur er í svæðinu Mótlykil.  
    * Gjalddagi er reiknuð út á grundvelli Greiðsluskilmála.  
    * Staðgreiðsluafsláttur mun vera sjálfgefið úr lykli Lánardrottins.  
12. Smellið á „Bóka“.
13. Lokið síðunni.


