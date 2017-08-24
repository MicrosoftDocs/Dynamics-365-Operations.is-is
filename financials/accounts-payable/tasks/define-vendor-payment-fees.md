--- 
title: "Skilgreina greiðsluþóknanir lánardrottna"
description: "Setja upp greiðsluþóknun lánardrottins"
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 844badb3b3037df8c4f22be558f01ea3dbf37f9d
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-fees"></a>Skilgreina greiðsluþóknanir lánardrottna

[!include[task guide banner](../../includes/task-guide-banner.md)]

Setja upp greiðsluþóknun lánardrottins Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluþóknun.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum Kenni greiðsla .
    * Kenni Þóknunar ætti að lýsa hvenær gjaldi verður notað eins og "EFT_Fee".  
4. Í reitinn Heiti skal slá inn gildi.
5. Færa inn gildi í lýsingarsvæðinu Þóknunar.
    * Bæta við lýsingu til að veita frekari upplýsingar um þegar þóknunin er metin.  
6. Velja Lánardrottna eða Fjárhagslykla í svæðinu Gjalda.
    * Fjárhagur er notaður þegar þóknunar gjaldfærðar í þínu fyrirtæki.  Lánardrottinn er notaður þegar þóknunin verður metin til lánardrottins.  
7. Færið inn aðallykil fyrir þar sem þóknunin verður kostnaðarfært.
    * Þessi valkostur er aðeins tiltækur þegar valinn er Fjárhag sem valkostur Gjalda.  
8. Velja færslubók sem nota má þessa þóknun. 
    * Fyrir Greiðsluþóknun lánardrottins, mundirðu velja færslubók 'Lánardrottinsgreiðsluna'.  
9. Smellið á „Vista“.
10. Smellt er á uppsetning Greiðsluþóknunar.
    * Halda áfram greiðsluþóknunaruppsetning til að skilgreina hvenær þóknun verði sjálfgefið á færslubókar sem er valin.  
11. Veljið annað hvort Töflu, Flokk eða Allt.
    * Tafla er notuð til að velja einn bankareikning Flokkurinn er notaður til að velja bankaflokk og Allt er til að nota þessa uppsetningu þóknunar fyrir alla bankareikninga  
12. Veljið bankaflokk eða bankareikningi.
    * Uppfletting sýna bankaflokk ef valinn var Flokkur, og sýna bankareikninga ef Tafla var valin.  
13. Velja Greiðsluhátt sem verður metið þessu gjaldi.
14. Velja greiðsluupplýsingar til að nota fyrir valinn greiðsluháttinn.
    * Greiðsluupplýsingar er notaður við rafræna sjóður greiðsluhættir flutning.  
15. Velja hvort gjaldið er prósentu, upphæð eða bili.
16. Færa inn prósentu eða upphæð þóknunar.
    * Færa inn prósentu ef Þóknunin er prósenta. Ef Gjaldið er upphæð, færið inn upphæð þóknunar. Notið flipann Bil til að skilgreina lagskipt gjöld ef Þóknunin er millibili.  
17. Í gjaldmiðill Þóknunar, veljið þann gjaldmiðil sem þóknunin verður metin.
    * Þessi gjaldmiðill er fyrir þóknun. Greiðslugjaldmiðli er notuð til að skilgreina hvenær þóknun regluna ætti að vera metin á grundvelli gjaldmiðli greiðslu. Til dæmis bankanum gæti gjaldfærð þóknun þegar greiðsla er gerð í EUR, en aðrar greiðslur ekki eru metnar fyrir þóknun.  
18. Smellið á „Vista“.


