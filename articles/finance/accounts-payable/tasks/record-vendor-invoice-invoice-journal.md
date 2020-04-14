---
title: Skrá reikning lánardrottins í reikningabók
description: Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140376"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Skrá reikning lánardrottins í reikningabók

[!include [banner](../../includes/banner.md)]

Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir. Dæmi um þessa gerð reiknings innihalda kostnað fyrir vörur eða þjónustu.  Þessi skráning notar sýnigögn USMF fyrirtækis

1. Farðu Í **Skoðunarrúðu > Einingar > Viðskiptaskuldir > Vinnusvæði > Reikningsfærsla lánardrottins**.
2. Í **aðgerðasvæðinu** er smellt á **Ný reikningsbók**.
3. Smellt er á **Nýtt**.
4. Í reitinn **Heiti** færirðu inn heiti færslubókar eða smellir á fellilistahnappinn til að opna leitina.
5. Í reitinn **Lýsing** skal slá inn gildi.
6. Í **Aðgerðasvæðinu**, smellirðu á **Línur**. Færa inn bókunardagsetningu sem mun uppfæra Fjárhag, í svæði **Dagsetning**.  
7. Í reitnum **Lykill** skal færa inn **Lánardrottnalykil**.
8. Í reitnum **Reikningur** færirðu inn númer reiknings.
9. Í reitinn **Lýsing** skal slá inn gildi.
10. Í reitnum **Kredit** skal slá inn tölu.
11. Í svæðinu **Mótlykill**, færið inn lykilnúmer eða smella á fellilistahnappinn til að opna leitina.
    * **Vsk-flokkinn** verður sjálfgefnar úr lykli lánardrottins.  
    * **Vsk-flokkur Vöru** eru sjálfgefnar úr aðallykillinn sem tilgreindur er í svæðinu **Mótlykil**.  
    * **Gjalddagi** er reiknuð út á grundvelli Greiðsluskilmála.  
    * **Staðgreiðsluafsláttur** mun vera sjálfgefið úr lykli Lánardrottins.  
12. Smelltu á **Bóka**.
13. Lokið síðunni.

