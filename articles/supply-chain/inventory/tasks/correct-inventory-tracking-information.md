---
title: Leiðrétta birgðarakningarupplýsingar
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að leiðrétta rakningarupplýsingar birgða.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aae70bf74f3b640167a01d8a5935989d7225695dc5d4f3817ac2ce92d191cb31
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766704"
---
# <a name="correct-inventory-tracking-information"></a>Leiðrétta birgðarakningarupplýsingar

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að leiðrétta rakningarupplýsingar birgða. Í þessu dæmi munum við að uppfæra upplýsingar runu sem stjórnað er af vöru með því að breyta ranglega skráð rununúmer í annarri runu. Hægt er að gilda með þessu ferli í sýnigögn gögn fyrirtækisins USPI eða með því að nota eigin gögn. Ef eigin gögn eru notuð, þarf að hafa vöru sem er runuvirkjaðir og það má ekki vera stjórnað úr staðsetningu. Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir birgðaflutning. Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.


## <a name="create-an-inventory-transfer-journal"></a>Stofna færslubóka fyrir birgðaflutning
1. Fara í Flutningi.
2. Smellið á „Nýtt“.
3. Sláið inn eða veldu gildi í reitnum heiti.
4. Smellið á „Í lagi“.

## <a name="create-journal-lines"></a>Stofna færslubókarlínur
1. Smellið á „Nýtt“.
2. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Ef verið er að nota USPI, veljið M5003 vöru.  
3. Færið inn númer í reitnum „Magn“.
4. Smellið á flipann Birgðavíddir.
5. Sláðu inn eða veldu gildi í reitnum rununúmer.
6. Sláið inn eða veldu gildi í reitnum svæði.
7. Sláðu inn eða veldu gildi í reitnum Vöruhús.
8. Sláðu inn eða veldu gildi í reitnum rununúmer.

## <a name="post-the-journal"></a>Bóka færslubókina
1. Smellið á „Bóka“.
2. Smellið á „Í lagi“.

## <a name="check-tracing-information"></a>Skoða upplýsingar um rakningu
1. Smellið á birgðir.
2. Smellt er á Rakningu.
3. Smellið á „Í lagi“.
    * með því að nota þessar upplýsingar rakningu er hægt rekja sig til baka í runu sem þú leiðréttir birgðir fyrir.  Einnig er hægt að nota síðuna rakningu Vöru til að skoða þessar upplýsingar.  
4. Lokið síðunni.

## <a name="check-inventory-transactions"></a>Athuga Birgðafærslur
1. Smellið á birgðir.
2. Smella á Færslur.
    * Hér er hægt að sjá færslurnar sem voru stofnaðar þegar þitt færslubók var bókuð.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]