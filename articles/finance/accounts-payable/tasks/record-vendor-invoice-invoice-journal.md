---
title: Skrá reikning lánardrottins í reikningabók
description: Þessi leiðarvísi mun sýna hvernig á að skrá reikninga lánardrottins sem eru ekki tengdar við innkaupapantanir.
author: abruer
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27d0e81ca37c9a59adc3acce3610fd17fd954a8b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716665"
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
12. Ef verkflæði fyrir reikningsfærslu lánardrottins hefur verið virkjað er smellt á **Verkflæði > Senda**.
    * Þegar sendingin er samþykkt verður dagsetningin færð á fyrsta dag næsta opna tímabils, ef bókunardagsetning færslunna fellur innan tímabils sem er Í bið eða Lokað fyrir fjárhagsbókun.
12. Smelltu á **Bóka**.
13. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
