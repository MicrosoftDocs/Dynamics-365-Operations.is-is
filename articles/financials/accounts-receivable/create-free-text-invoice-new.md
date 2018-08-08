--- 
title: "Stofna reikning með frjálsum texta"
description: "Þessi grein sýnir hvernig skal stofna reikning með frjálsum texta."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: is-is
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Stofna reikning með frjálsum texta

[!include [banner](../includes/banner.md)]

Þessi grein sýnir hvernig skal stofna reikning með frjálsum texta. Fyrir þetta ferli skal nota USMF sýnifyrirtækið.

## <a name="create-a-free-text-invoice"></a>Stofna reikning með frjálsum texta

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

## <a name="copy-lines"></a>Afrita línur
Til að afrita línur á reikningi með frjálsum texta skal velja eina eða fleiri línur og smella síðan á Afrita valdar línur. Þú getur tilgreint fjölda eintaka sem þú vilt gera og þú getur líka afritað athugasemdir og viðhengi. Þú getur afritað dreifingarnar eða heimilað endursköpun þeirra þegar þú bókar. Um leið og þú afritar línurnar geturðu breytt upplýsingum eftir þörfum. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Búa til reikning með frjálsum texta út frá sniðmáti
Þú getur búið til reikning með frjálsum texta út frá sniðmáti. Þegar þú velur Nýtt úr sniðmáti úr flipanum Reikningur getur þú valið sniðmátsnafn og viðskiptavinarlykilinn fyrir nýja reikninginn með frjálsum texta. Þú getur einnig valið að gera gildi sjálfgefin, svo sem greiðsluskilmála og greiðsluaðferð frá viðskiptavininum eða notaðu gildin sem voru vistuð með sniðmátinu. Nýr reikningur með frjálsum texta verður búinn til og þú getur breytt gildunum í þeirri reikningi. 


