--- 
title: "Vinna úr innheimtubréfum"
description: "Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka innheimtubréf."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Vinna úr innheimtubréfum

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka innheimtubréf. Þetta verkefni notar USMF-sýnifyrirtækið.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Setja upp röð innheimtubréfa á bókunarreglu
1. Farið í Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina.
2. Smellið á „Breyta“.
    * Veljið innheimtubréfaröð úr í fellilistanum. Ef ekki á að mynda innheimtubréf fyrir færslur með þessari bókunarreglu, skilið eftir autt.  
    * Flipanum takmarkanir fyrir Taflan gerir kleift að breyta hvernig innheimtubréf eru unnin. Ef þetta svæði er stillt á Já, þá mun það verða að stofna innheimtubréf fyrir þessa bókunarreglu.  
3. Lokið síðunni.

## <a name="create-collection-letters"></a>Búa til innheimtubréf
1. Fara í Skuldir og innheimta > Innheimtubréf > Stofna innheimtubréf.
    * Velja verður færslugerðir sem innheimta á bréf fyrir. Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.  
2. Í reitnum innheimtubréf skal velja valkost.
3. Færðu inn dagsetningu innheimtubréfs.
    * Það eru tveir valkostir bókunarreglu: Reiknings – Notið bókunarreglu sem er úthlutað á reikning viðskiptavina fyrir hverja vaxtanótu.   Velja – Notið bókunarregluna sem valin var á svæðinu .  
    * Veljið bókunarreglu hafi verið breytt "Nota bókunarreglu úr" á "Velja".  
4. Útvíkka Færslur til að taka hluta.
5. Smellt er á Síu.
6. Í svæðið Skilyrði, í svæðið Skilyrði er fært inn kenni Viðskiptavinar. Til dæmis færið inn ‚US-001‘..
7. Smellið á „Í lagi“.
8. Smellið á „Í lagi“.

## <a name="print-collection-letters"></a>Prenta innheimtubréf
1. Fara í Skuldir og innheimta > Innheimtubréf > Fara yfir og vinna innheimtubréf.
2. Í reitnum Staða er ‚Stofnað' valin.
3. Veljið í svæðinu Prentað 'Ekki prentað'.
4. Smelltu á Prenta.
5. Smellt er á athugasemd innheimtubréfs
6. Útvíkka Færslur til að taka hluta.
7. Færa inn lokadagsetningu fyrir bókanir
8. Smellt er á í lagi til að prenta innheimtubréfið.

## <a name="post-the-collection-letter"></a>Bóka innheimtubréf
1. Smellið á „Bóka“.
2. Færð er inn bókunardagsetning fyrir innheimtubréf.
3. Útvíkka Færslur til að taka hluta.
4. Smellið á „Í lagi“.
5. Í reitnum Staða er ‚bókað' valin.
6. Prenta svæði, velja valkostur.


