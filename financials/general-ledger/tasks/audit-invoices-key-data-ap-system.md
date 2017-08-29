--- 
title: "Endurskoða reikninga og lykilgögn í viðskiptaskuldum"
description: "Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 38cc5587d970d05492638ed349484e6c002d5363
ms.contentlocale: is-is
ms.lasthandoff: 07/28/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Endurskoða reikninga og lykilgögn í viðskiptaskuldum

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þegar reikningur er móttekinn frá lánardrottni fyrir vörur eða þjónustu á innkaupapöntun gætu viðskiptaferlin krafist þess að vörurnar eða þjónustan séu mótteknar áður en hægt er að samþykkja reikninginn til greiðslu. Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn. 

Á síðunni færibreytum viðskiptaskulda, skal tryggja að valkosturinn Virkja sannprófun á reikningsjöfnun sé valinn, svæðið Bóka reikning með misræmi er stillt til að Krefjast samþykkis, og svæðið Línujöfnunarregla er stillt á þríhliða jöfnun.

Þessi aðferð notar sýnigögn USMF fyrirtækisins. hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum.


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Fara í Allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
4. Í svæðinu Lánardrottnalykill skal slá inn gildi.
5. Smellið á „Í lagi“.
6. Smellið á „Bæta við línu“.
7. Í reitnum Vörunúmer skal slá inn gildi.
8. Smellið á „Innkaup“ á aðgerðarúðunni.
9. Smellið á „Staðfesta“.

## <a name="post-a-product-receipt"></a>Bóka innhreyfingarskjal afurða
1. Smellið á „Móttaka“ á aðgerðarúðunni.
2. Smellið á „Innhreyfingarskjal“.
3. Í listanum skal merkja valda línu.
4. Í reitinn innhreyfingarskjal afurða skal slá inn gildi.
5. Smellið á „Í lagi“.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Skráðu og jafnaðu reikningu lánardrottins við innhreyfingarskjal afurða
1. Smellið á „Reikningur“ á aðgerðarúðunni.
2. Smellið á „Reikningur“.
3. Í reitnum Númer skal slá inn gildi.
4. Smellt er á Sjálfgefið úr: Pantað magn til að opna felligluggann.
5. Í reitnum sjálfgefið magn fyrir línur skal velja valkost.
6. Smellið á „Í lagi“.
7. Smella á Já.
8. Smellt er á Jafna innhreyfingarskjöl afurða.
9. Smellið á „Í lagi“.
10. Smellið á „Yfirfara“ á aðgerðarúðunni.
11. Smellið á „Samsvörunarupplýsingar“.


