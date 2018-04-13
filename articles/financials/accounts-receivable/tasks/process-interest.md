--- 
title: Reikna vexti
description: "Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="process-interest"></a>Reikna vexti

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur. Þetta verkefni notar USMF-sýnifyrirtækið.


## <a name="set-up-interest-on-the-posting-profile"></a>Setja upp vexti fyrir bókunarregluna
1. Farið í Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina.
2. Smellið á „Breyta“.
    * Veldu vaxtakóða úr fellilistanum. Ef ekki á að reikna vexti fyrir færslur með þessari bókunarreglu, skilið eftir autt.  
    * Takmarkanaflipi fyrir Taflan leyfir þér að breyta hvernig vextir eru unnir. Ef þetta svæði er stillt á Já eru vextir reiknast fyrir þessa bókunarreglu.  

## <a name="calculate-interest"></a>Reikna út vexti
1. Fara í Skuldir og innheimta > Vextir > Stofna vaxtanótur.
    * Velja færslugerðir sem verður að reikna út vexti fyrir. Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.  
    * Ef Vaxta er valið, muntu reikna vaxtavexti. Hægt er að athuga lög um útreikningi á vaxtavöxtum áður en þessar færslur eru hafðar með.  
    * Vextir reiknast úr þessari dagsetning sem „Til dagsetningar". Ef ekki er tiltekin á "Frá dagsetningu', þá allir óbókaðir vaxtanóta verður hætt við og vextir verða endurreiknuð frá færsludagsetning.  
2. Færið inn dagsetningu vaxtanótunnar.
    * Það eru þrír möguleikar fyrir bókunarreglu: Reikningur - Nota bókunareglu sem er úthlutað til reikning viðskiptavinar fyrir hverja vaxtanótu.   Velja – Notið bókunarregluna sem valin var á svæðinu .   Færsla – Notið einstaka bókunarreglu úr færslum þar sem vextir eru reiknaðir fyrir hverja vaxtanótu. Færslur sem hafa ekki úthlutaða bókunarreglu nota bókunarreglu sem er tilgreind á svæðinu Fjárhagur og virðisaukaskattur í skjámyndinni Færibreytur viðskiptakrafna.  
    * Veljið bókunarreglu hér ef "Nota bókunarreglu úr" er breytt í "Velja".  
3. Útvíkka eða draga saman Færslur sem á að taka með hluta.
4. Smellt er á Síu.
5. Í forsendusvæðinu, færið inn kenni viðskiptavinar. Til dæmis færið inn ‚US-001‘..
6. Smellið á „Í lagi“.
7. Smellið á „Í lagi“.

## <a name="print-interest-notes"></a>Prenta vaxtanótur
1. Fara í Skuldir og innheimta > Vextir > Endurskoða og vinna vaxtanótur.
2. Í reitnum Staða er ‚Stofnað' valin.
3. Veljið í svæðinu Prentað 'Ekki prentað'.
4. Smelltu á Prenta.
5. Útvíkka eða draga saman Færslur sem á að taka með hluta.
6. Smellið á „Í lagi“.
7. Lokið síðunni.

## <a name="post-the-interest-note"></a>Bóka vaxtanótu
1. Velja vaxtanótu sem er að tilbúin til bókunar (staða er stofnuð).
2. Smellið á „Bóka“.
3. Færð er inn bókunardagsetning fyrir vaxtanóta.
    * Skal velja Já í stofna fjárhagsfærsla fyrir hverja vaxtanóta.     Ef þú velur ekki já, safnast upp allir vextir á vaxtanóta til viðskiptavinarins og eru bókaðar á fjárhag í einni færslu.  
4. Útvíkka eða draga saman Færslur sem á að taka með hluta.
5. Smellið á „Í lagi“.
6. Í reitnum Staða er ‚bókað' valin.


