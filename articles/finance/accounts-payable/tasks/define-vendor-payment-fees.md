---
title: Skilgreina greiðsluþóknanir lánardrottna
description: Setja upp greiðsluþóknun lánardrottins
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109832"
---
# <a name="define-vendor-payment-fees"></a>Skilgreina greiðsluþóknanir lánardrottna

[!include [banner](../../includes/banner.md)]

Setja upp greiðsluþóknun lánardrottins Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara í **Viðskiptakröfur > Greiðsluuppsetning > Greiðsluþóknun**.
2. Smellt er á **Nýtt**.
3. Færa inn gildi í reitnum **Kenni gjalds**.
    * **Kenni þóknunar** ætti að lýsa hvenær gjaldi verður notað eins og "EFT_Fee".  
4. Í reitinn **Heiti** skal slá inn gildi.
5. Færa inn gildi í reitnum **Þóknunarlýsing**.
    * Bæta við lýsingu til að veita frekari upplýsingar um þegar þóknunin er metin.  
6. Velja **Lánardrottna** eða **Fjárhagslykla** í svæðinu **Gjald**.
    * **Fjárhagur** er notaður þegar þóknunar gjaldfærðar í þínu fyrirtæki. **Lánardrottinn** er notaður þegar þóknunin verður metin til lánardrottins.  
7. Færið inn aðallykil fyrir þar sem þóknunin verður kostnaðarfært.
    * Þessi valkostur er aðeins tiltækur þegar valinn er **Fjárhagur** sem valkostur **Gjalda**.  
8. Velja færslubók sem nota má þessa þóknun. 
    * Fyrir Greiðsluþóknun lánardrottins, mundirðu velja færslubók 'Lánardrottinsgreiðsluna'.  
9. Smellið á **Vista**.
10. Smellt er á **Uppsetning greiðsluþóknunar**.
    * Halda áfram **Greiðsluþóknunaruppsetning** til að skilgreina hvenær þóknun verði sjálfgefið á færslubókar sem er valin.  
11. Veljið annað hvort **Töflu**, **Flokk** eða **Allt**.
    * **Tafla** er notuð til að velja einn bankareikning **Flokkur** er notaður til að velja bankaflokk og **Allt** er til að nota þessa uppsetningu þóknunar fyrir alla bankareikninga  
12. Veljið bankaflokk eða bankareikningi.
    * Uppfletting sýna bankaflokk ef valinn var **Flokkur**, og sýna bankareikninga ef **Tafla** var valin.  
13. Velja Greiðsluhátt sem verður metið þessu gjaldi.
14. Velja **Greiðsluupplýsingar** til að nota fyrir valda greiðsluháttinn.
    * **Greiðsluupplýsingar** er notað við greiðsluhátt rafrænnar millifærslu.  
15. Velja hvort gjaldið er prósentu, upphæð eða bili.
16. Færa inn prósentu eða upphæð þóknunar.
    * Færa inn prósentu ef **Þóknun** er prósenta. Ef **Þóknun** er upphæð, færið inn upphæð þóknunar. Ef **Þóknun** er tímabil skal nota flipann **Tímabil** til að skilgreina lagskipt gjöld.  
17. Í **Gjaldmiðill þóknunar** reitnum, veljið þann gjaldmiðil sem þóknunin verður metin.
    * Þessi gjaldmiðill er fyrir þóknun. Greiðslugjaldmiðli er notuð til að skilgreina hvenær þóknun regluna ætti að vera metin á grundvelli gjaldmiðli greiðslu. Til dæmis bankanum gæti gjaldfærð þóknun þegar greiðsla er gerð í EUR, en aðrar greiðslur ekki eru metnar fyrir þóknun.  
18. Smelltu á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
