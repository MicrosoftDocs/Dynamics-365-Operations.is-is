---
title: Skrá reikning lánardrottins í reikningabók
description: Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "348941"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Skrá reikning lánardrottins í reikningabók

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

