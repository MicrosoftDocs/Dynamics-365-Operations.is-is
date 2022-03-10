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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109832"
---
# <a name="define-vendor-payment-fees"></a>Skilgreina greiðsluþóknanir lánardrottna

[!include [banner](../../includes/banner.md)]

Setja upp greiðsluþóknun lánardrottins Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara til **Viðskiptaskuldir > Greiðsluuppsetning > Greiðslugjald**.
2. Smellt er á **Nýtt**.
3. Í **Gjaldskr** reit, sláðu inn gildi.
    * The **Gjaldskr** ætti að lýsa því hvenær þetta gjald verður notað, svo sem "EFT_Fee".  
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í **Gjaldslýsing** reit, sláðu inn gildi.
    * Bæta við lýsingu til að veita frekari upplýsingar um þegar þóknunin er metin.  
6. Í **Hleðsla** reit, veldu annað hvort **Seljandi** eða **Fjárhagsbók**.
    * **Fjárhagsbók** er notað þegar gjaldið verður gjaldfært á fyrirtæki þitt. **Seljandi** er notað þegar gjaldið verður metið til seljanda.  
7. Færið inn aðallykil fyrir þar sem þóknunin verður kostnaðarfært.
    * Þessi valkostur er aðeins í boði þegar þú velur **Fjárhagsbók** sem **Hleðsla** valmöguleika.  
8. Velja færslubók sem nota má þessa þóknun. 
    * Fyrir Greiðsluþóknun lánardrottins, mundirðu velja færslubók 'Lánardrottinsgreiðsluna'.  
9. Smelltu á S **ave**.
10. Smellt er á **Uppsetning greiðsluþóknunar**.
    * Haltu áfram að **Uppsetning greiðslugjalds** til að skilgreina hvenær gjaldið ætti að vera sjálfgefið í dagbókinni sem þú valdir.  
11. Veldu annað hvort **Tafla**, **eða** **Allt**.
    * **Tafla** er notað til að velja einn bankareikning, **Hópur** er notað til að velja bankahóp, og **Allt** er að nota þessa gjaldskrá fyrir alla bankareikninga.  
12. Veljið bankaflokk eða bankareikningi.
    * Uppflettingin mun sýna bankahóp ef þú valdir **Hópur**, og mun sýna bankareikninga ef þú valdir **Tafla**.  
13. Velja Greiðsluhátt sem verður metið þessu gjaldi.
14. Veldu **Greiðslulýsing** fyrir valinn greiðslumáta.
    * The **Greiðslulýsing** er notað með rafrænum millifærslumáta greiðslu.  
15. Velja hvort gjaldið er prósentu, upphæð eða bili.
16. Færa inn prósentu eða upphæð þóknunar.
    * Ef **Gjald** er prósenta, sláðu inn prósentuna. Ef **Gjald** er upphæð skal slá inn upphæð gjaldsins. Ef **Gjald** er bil, notaðu **Tímabil** flipa til að skilgreina þrepaskipt gjöld.  
17. Í **Gjaldmiðill** reit, veldu gjaldmiðilinn sem gjaldið verður metið í.
    * Þessi gjaldmiðill er fyrir þóknun. Greiðslugjaldmiðli er notuð til að skilgreina hvenær þóknun regluna ætti að vera metin á grundvelli gjaldmiðli greiðslu. Til dæmis bankanum gæti gjaldfærð þóknun þegar greiðsla er gerð í EUR, en aðrar greiðslur ekki eru metnar fyrir þóknun.  
18. Smelltu á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
