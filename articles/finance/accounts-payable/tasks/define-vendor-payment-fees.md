---
title: Skilgreina greiðsluþóknanir lánardrottna
description: Setja upp greiðsluþóknun lánardrottins
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0705cdae069b687a141b0a85280eaed0fa207a89
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227257"
---
# <a name="define-vendor-payment-fees"></a>Skilgreina greiðsluþóknanir lánardrottna

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]