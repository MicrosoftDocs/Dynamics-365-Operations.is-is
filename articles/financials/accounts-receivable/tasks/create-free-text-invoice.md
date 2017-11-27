--- 
title: Stofna textareikning
description: "Þessi leiðarvísir fyrir verk sýnir stofnun textareiknings."
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 87e293008fd748aa0dcc6b3caa94a4889bed35de
ms.contentlocale: is-is
ms.lasthandoff: 10/26/2017

---
# <a name="create-a-free-text-invoice"></a>Stofna textareikning

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísir fyrir verk sýnir stofnun textareiknings. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.
2. Smellið á „Nýtt“.
3. Í reitnum Viðskiptavinalykill skal velja gildi.
    * Reikningslykillinn verður sjálfgefið að sama lykli og notaður var fyrir viðskiptavinalykilinn.   
    * Lykilstaðan byrjar á Í vinnslu ef reikningurinn hefur ekki verið bókaður.   
    * Númeri reikningsins verður úthlutað þegar reikningurinn er bókaður.  
    * Ef SEPA-umboð er notað verður umboð fyrir beingreiðslu sjálfkrafa fyllt út með umboði þegar viðskiptavinalykillinn er valinn.  
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í svæðinu aðallykill, skal tilgreina lykilnúmer án víddir.
    * Einnig er hægt að slá inn einn eða fleiri stafi fyrir aðallykilinn og nota uppflettingu til að finna lykilinn. Þú munt færa inn víddirnar síðar í þessari handbók.  
6. Stækkið flýtiflipann fyrir línuupplýsingar til að geta bætt víddum við aðallykilinn.
7. Smellið á flipann fyrir línu „Fjárhagsvíddar“.
    * Víddirnar eru aðeins ætlaðar fyrir valda línu.    
    * Vsk-flokkur er fylltur út frá viðskiptavini. Vsk-flokk frá aðallykli er notað ef viðskiptavinur hefur ekki vsk-flokk.  
    * VSK-flokkur varanna er fylltur út sjálfgefið úr aðallykli. Ef aðallykillinn hefur ekki VSK-flokk vöru verður VSK-flokkur vöru úr virðisaukaskattsfæribreytum fjárhags notaður.    
8. Færið inn númer í reitnum „Magn“.
    * Magnið er valfrjálst.  
9. Færið inn númer í reitnum „Einingarverð“.
    * Einingarverðið er valfrjálst.  
    * Upphæðin er reiknuð út sem magnið margfaldað með einingarverðinu. Þó er hægt að hnekkja útreikningnum og slá inn aðra upphæð.  
10. Smellið á „Virðisaukaskatt“ til að skoða útreiknaðan virðisaukaskatt fyrir reikninginn.
    * Á þessari síðu er hægt að skoða upphæðir virðisaukaskattsins eða hnekkja þeim á leiðréttingarflipanum.  
11. Smellið á „Í lagi“.
12. Smellt er á Gjöld til að bæta gjaldi við reikning. 
13. Í reitnum Gjaldakóði skal slá inn gildi.
14. Í reitinn Gjöld skal slá inn númer.
15. Lokið síðunni.
16. Smellið á „Samtölur“ til að skoða samantekt yfir reikninga og samtölur.
17. Smellið á „Loka“.
18. Smellið á „Bóka“ til að bóka reikninginn. Hægt er að hætta við áður en bókun er framkvæmd.
    * Til að breyta tímasetningu prentunar reiknings: Velja Gildandi til að prenta hvern reikning þegar hann er uppfærður eða Velja Eftir að prenta eftir að allir reikningar hafa verið uppfærðar.  
    * Ef óskað er að breyta hvernig gerð lánamarks viðskiptavinarins er athuguð fyrir bókun, þarf að breyta gerð lánamarks.  
    * Ef það á að prenta reikninginn skal velja Já.  
    * Ef það á að bóka reikninginn skal velja Já. Hægt er að prenta reikninga án bókunar.  
19. Smellið á „Í lagi“.


