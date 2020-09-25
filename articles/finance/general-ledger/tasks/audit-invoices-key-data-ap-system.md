---
title: Endurskoða reikninga og lykilgögn í viðskiptaskuldum
description: Þetta efnisatriði sýnir hvernig á að endurskoða reikninga og lykilgögn í viðskiptaskuldum.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bb89f0adce41b045b1f573c4c0e841f78b2248c
ms.sourcegitcommit: 95d06006142e6bf83351fb075b413fdc2074d5ee
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761550"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Endurskoða reikninga og lykilgögn í viðskiptaskuldum

[!include [banner](../../includes/banner.md)]

Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu. Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn. 

Á síðunni **færibreytum viðskiptaskulda**, skal tryggja að valkosturinn Virkja sannprófun á reikningsjöfnun sé valinn, svæðið **Bóka reikning með misræmi** er stillt til að **Krefjast samþykkis**, og svæðið **Línujöfnunarregla** er stillt á **þríhliða jöfnun**.

Þessi aðferð notar sýnigögn USMF fyrirtækisins. hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Opnið **Allar innkaupapantanir**.
2. Smellt er á **Nýtt**.
3. Í svæðinu **Lánardrottnalykill** skal slá inn gildi.
4. Smellið á **Í lagi**.
5. Smella á **Bæta við línu**.
6. Í reitnum **Vörunúmer** skal slá inn gildi.
7. Í aðgerðasvæðinu skal smella á **Innkaup**.
8. Smellið á **Staðfesta**.

## <a name="post-a-product-receipt"></a>Bóka innhreyfingarskjal afurða
1. Í aðgerðasvæðinu skal smella á **Móttaka**.
2. Smellið á **Innhreyfingarskjal afurða**.
3. Í reitinn **Innhreyfingarskjal afurða** skal slá inn gildi.
4. Smellið á **Í lagi**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Skráðu og jafnaðu reikningu lánardrottins við innhreyfingarskjal afurða
1. Í aðgerðasvæðinu er smellt á **Reikningur > Reikningur**.
2. Í reitinn **Númer** skal slá inn gildi.
3. Smellið á **Sjálfgefið úr: Pantað magn** til að opna felligluggann.
4. Í reitnum **Sjálfgefið magn fyrir línur** skal velja valkost.
5. Smellið á **Í lagi**.
6. Smellið á **Já**.
7. Smellið á **Jafna innhreyfingarskjöl afurða**.
8. Smellið á **Í lagi**.
9. Í aðgerðasvæðinu skal smella á **Yfirfara**.
10. Smellið á **Samsvörunarupplýsingar**.

