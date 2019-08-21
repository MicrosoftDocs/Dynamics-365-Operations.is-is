---
title: Flytja efnislegar birgðir innan vöruhúss
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7344bfa3be0d7345d3ac68202c7bc26bcac8ebb9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845258"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Flytja efnislegar birgðir innan vöruhúss

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað. Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir birgðaflutning áður en byrjað er að þetta. Hægt er að fara í gegnum þessu ferli í sýnigögn fyrirtækisins USMF með notkun dæmagilda sem eru sýndar eða með því að nota eigin gögn ef afurðir og staðsetningar eru uppsettar. Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.


## <a name="create-an-inventory-transfer-journal"></a>Stofna færslubóka fyrir birgðaflutning
1. Fara í Flutningi.
2. Smellið á „Nýtt“.
3. Sláið inn eða veldu gildi í reitnum heiti.
4. Smellið á „Í lagi“.
    * Það er að valkostur um að tilgreina 'Frá' og ''til“ vídda fyrir hverja færslubókarlínu. Þetta eru mikilvægar fyrir gerð færslubókar. Hægt er að flytja vörur á staði með mismunandi reglur. Í þessu dæmi munum við flytja vöru innan sama vöruhús, frá númeraplötustýrð staðsetningu á staðsetningu sem ekki er númeraplötustýrð.   

## <a name="create-journal-lines"></a>Stofna færslubókarlínur
1. Smellið á „Nýtt“.
2. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Ef verið er að nota USMF er hægt að velja 'A0001'.  
3. Sláið inn eða veldu gildi í reitnum Frá svæði.
    * Ef verið er að nota USMF er hægt að velja '2'.  
4. Sláið inn eða veldu gildi í reitnum í Til svæðis.
    * Ef verið er að nota USMF er hægt að velja '2'.  
5. Sláðu inn eða veldu gildi í reitnum Úr vöruhúsi.
    * Ef verið er að nota USMF er hægt að velja '24'.  
6. Sláðu inn eða veldu gildi í reitnum Í vöruhús.
    * Ef verið er að nota USMF er hægt að velja '24'.  
7. Færa inn eða veljið gildi í svæðinu Frá staðsetningu.
    * Ef verið er að nota USMF er hægt að velja 'FL-001'.  
8. Sláðu inn eða veldu gildi í reitnum Í staðsetning.
    * Ef verið er að nota USMF er hægt að velja ‚BULK-001'.  
9. Færið inn númer í reitnum „Magn“.
10. Smellið á flipann Birgðavíddir.
11. Færa inn eða veljið gildi í svæðinu númeraplata.
    * Ef verið er að nota USMF er hægt að velja '24'.  
12. Smellið á „Vista“.

## <a name="post-the-inventory-transfer-journal"></a>Bóka færslubóka fyrir birgðaflutning
1. Smellið á „Bóka“.
2. Smellið á „Í lagi“.

## <a name="view-inventory-transactions"></a>Skoða birgðafærslur
1. Smellið á birgðir.
2. Smella á Færslur.
    * Hér er hægt að sjá færslurnar sem voru stofnaðar þegar þitt færslubók var bókuð.  

