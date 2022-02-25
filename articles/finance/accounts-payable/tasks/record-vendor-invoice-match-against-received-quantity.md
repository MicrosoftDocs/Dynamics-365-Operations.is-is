---
title: Skrá reikning lánardrottins og samsvara við móttekið magn
description: Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a3f1463821a43af0d8d5f15225944b080414e4c
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109919"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Skrá reikning lánardrottins og samsvara við móttekið magn

[!include [banner](../../includes/banner.md)]

Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu. Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn. 

Í **Færibreytur viðskiptaskulda** síðu, tryggja að **Virkja reikningssamsvörun** valkostur er valinn, the **Bókaðu reikning með misræmi** reiturinn er stilltur á **Krefjast samþykkis**, og **Línusamsvörun stefna** reiturinn er stilltur á **Þríhliða samsvörun**.

Þessi aðferð notar sýnigögn USMF fyrirtækisins. hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Fara í Allar innkaupapantanir.
2. Smellt er á **Nýtt**.
3. Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina.
4. Í svæðinu **Lánardrottnalykill** skal slá inn gildi.
5. Smellt er á **OK**.
6. Smella á **Bæta við línu**.
7. Í reitnum **Vörunúmer** skal slá inn gildi.
8. Í aðgerðasvæðinu skal smella á **Innkaup**.
9. Smellið á **Staðfesta**.

## <a name="post-a-product-receipt"></a>Bóka innhreyfingarskjal afurða
1. Í aðgerðasvæðinu skal smella á **Móttaka**.
2. Smellið á **Innhreyfingarskjal afurða**.
3. Í listanum skal merkja valda línu.
4. Í reitinn **Innhreyfingarskjal afurða** skal slá inn gildi.
5. Smellt er á **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Skráðu og jafnaðu reikningu lánardrottins við innhreyfingarskjal afurða
1. Í aðgerðasvæðinu smellirðu á **Reikningur.**
2. Smelltu á **Reikningur**.
3. Í reitinn **Númer** skal slá inn gildi.
4. Smellið á **Sjálfgefið úr: Pantað magn** til að opna felligluggann.
5. Í reitnum **Sjálfgefið magn fyrir línur** skal velja valkost.
6. Smellið á **Í lagi**.
7. Smellið á **Já**.
8. Smellið á **Jafna innhreyfingarskjöl afurða**.
9. Smellið á **Í lagi**.
10. Í aðgerðasvæðinu skal smella á **Yfirfara**.
11. Smellið á **Samsvörunarupplýsingar**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
