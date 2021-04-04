---
title: Breyta sniðum til að búa til skjöl sem eru með forritsgögnum
description: Í þessu efni er útskýrt hvernig á að hanna skilgreiningar skýrslugerðar til að mynda rafrænt skjal og uppfæra forritsgögn.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad75adb22efbd90d3fb4a71a2d592950a66bafd8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565442"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Breyta sniðum til að búa til skjöl sem eru með forritsgögnum

[!include [banner](../../includes/banner.md)]

Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 3: Breyta líkani og vörpun)“.

Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit. Í þessu ferli muntu breyta Rafræna skýrslugerð (ER) grunnstillingar þannig að þú notar þær ekki bara til að búa til rafræn skjöl, heldur líka uppfæra gögn fyrir forrit. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota DEMF gagnasafn.


## <a name="modify-format-to-collect-details-of-reporting"></a>Breyta sniði til að safna upplýsingum um skýrslugerð
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal víkka út „Intrastat (líkan)“.
3. Í trénu skal velja „Intrastat (líkan)\Intrastat (Snið)“.
4. Smellið á Hönnuður.
5. Stækkið „Skrá“ í trénu.
6. Í trénu skal víkka út „Skrá\Framtal“.
7. Í trénu skal velja „Skrá\Framtal\Gögn“.
8. Veljið „Einn margir“ í svæðinu Margfeldi.
    * Skilgreina þessa sniðeiningu til að skjala upplýsingar um Intrastat skýrsulgerðarferlið. Þetta atriði táknar skrá safnhauss.  
9. Í trénu skal víkka út „Skrá\Framtal\Gögn“.
10. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð“.
11. Veljið „Núll margir“ í svæðinu Margfeldi.
    * Skilgreina þessa sniðeiningu til að skjala upplýsingar um Intrastat skýrsulgerðarferlið. Þetta atriði mun tákna lista yfir skjalaðar línur.  
12. Í trénu skal víkka út „Skrá\Framtal\Gögn\Afurð“.
13. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim1“.
14. Veljið Já í svæðinu undanskildar
    * Þú munt ekki skjala þessi gögn, svo þú getur útilokað þessa sniðeiningu frá gagnaveitu Intrastat skýrslugerðarupplýsinga.  
15. Stækkið „Skrá\Framtal\Gögn\Afurð\Dim1“ í trénu.
16. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim1\eign“.
17. Veljið Já í svæðinu undanskildar
18. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim1\dagsetning“.
19. Veljið Já í svæðinu undanskildar
20. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim2“.
21. Veljið Já í svæðinu undanskildar
22. Í trénu skal stækka „Skrá\Framtal\Gögn\Afurð\Dim2“.
23. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim2\eign“.
24. Veljið Já í svæðinu undanskildar
25. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim2\kóði“.
26. Veljið Já í svæðinu undanskildar
27. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim3“.
    * Nokkrar sniðeiningar geta borið sama heiti. Til dæmis Dim. Þú getur ekki borið greinileg kennsl á þær þegar þú notar þetta snið sem gagnaveitu fyrir skjölun Intrastat skýrslugerðarupplýsinga, þannig að þú þarft að skilgreina önnur nöfn fyrir þessar sniðeiningar.   
28. Í reitnum Heiti skal færa inn ‚Upphæð'.
    * Upphæð  
29. Veljið „Akkúrat einn“ í svæðinu Margfeldi.
30. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð\Dim4“.
31. Í reitnum Heiti skal færa inn ‚Atriði.
    * vara  
32. Veljið „Akkúrat einn“ í svæðinu Margfeldi.
    * Fyrir utan hönnunarsniðeiningarnar, verður að skjala eftirfarandi Intrastat skýrslugerðarupplýsingar: einkvæm skrá auðkenna fyrir hverja skráða grunnvöru og heiti skjals sem er myndað. Þar sem þessi gögn verða ekki fyllt út í Intrastat skýrslunni, verður að bæta við sniðinu sem tengist þessum upplýsingaeiningum sem gagnaveituatriði.  
33. Í trénu skal velja „Skrá\Framtal\Gögn“.
34. Smelltu á Bæta við til að opna felligluggann.
35. Í trénu skal velja „Gagnaveita/Afurð“.
36. Í svæðið Heiti, færðu inn 'skrárnafn'.
    * Skrárnafn  
37. Veljið „Strengur“ í reitnum Gagnagerð.
38. Smellið á „Í lagi“.
39. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð“.
40. Smellið á Bæta við atriðum.
41. Í svæðið Heiti, færðu inn „Grunnvara skrá kenni“.
    * Vöru skrá kenni  
42. Veljið „Int64“ í reitnum Gagnagerð.
43. Smellt er á Í lagi.
44. Smelltu á flipann Vörpun.
45. Í trénu skal velja „Skrá\Framtal\Gögn\Heiti skráar“.
46. Smelltu á Binda.
47. Í trénu skal víkka út 'model'.
48. Í trénu skal víkka út „líkan\Færslur“.
49. Í trénu skal velja „Skrá\Framtal\Gögn\Afurð =  líkan.Færslur\Grunnvara skrá kenni“.
50. Í trénu skal velja „líkan\Færslur\Grunnvara skrá kenni“.
51. Smelltu á Binda.
52. Smelltu á Vista.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Breyta sniði til að geyma í minni upplýsingar um skýrslugerð

1. Smellt er á Varpa sniði á líkan.
2. Smellið á Nýtt.
3. Sláið inn eða veldu rótaratriðið „Fyrir gagnauppfærslu fyrir forrit“ í reitnum Skilgreining.
    * Fyrir uppfærsla gagna hugbúnaðarins.
4. Í reitnum Heiti skal færa inn „Vörpun til að uppfæra gögn“.
    * Vörpun fyrir uppfærslu gagna  
5. Smellið á „Vista“.
    * Þessi vörpun skilgreinir hvernig upplýsingum um Intrastat skýrsluna er safnað saman í gagnalíkaninu, skipaninni sem er tilgreind af völdu rótaratriði „Fyrir gagnauppfærslu fyrir forrit“. Þessar upplýsingar, vörpun líkans með sama rótaratriði „Fyrir gagnauppfærslu fyrir forrit“, og stefnuna „Til viðtökustaðar“ verða notaðar fyrir gagnauppfærsluna fyrir forrit. Gagnauppfærslan fyrir forrit hefst strax eftir að Intrastat skýrslan á útleið er búin til. Hægt er að sleppa gagnauppfærslan fyrir forrit við keyrslu, en gagnalíkanið verður að vera tómt (innihalda tóma skráningarlista).
6. Smellið á Hönnuður.
    * Intrastat skýrsla á útleið er bætt við sjálfvirkt sem gagnaveitu fyrir þessa vörpun líkans.  
    * Binda einingar skýrslunnar sem hönnuð hefur verið (sett fram sem gagnaveita) við einingar gagnalíkansins, sem er afmarkað út frá völdu rótaratriði líkansins.  
7. Í trénu skal víkka út „Safn haus“.
8. Í trénu skal víkka út „Safn haus\Safn línur“.
9. Í trénu skal víkka út „snið“.
10. Í trénu skal víkka út „snið\Framtal: XML Eining(Framtal)“.
11. Í trénu skal víkka út „snið\Framtal: XML Eining(Framtal)\Gögn: XML Eining 1..* (Gögn)“.
12. Í trénu skal víkka út „snið\Framtal: XML Eining(Framtal)\Gögn: XML Eining 1..* (Gögn)\Afurð: XML Eining 0..* (Afurð)“.
13. Í trénu skal víkka út „snið\Framtal: XML Eining(Framtal)\Gögn: XML Eining 1..* (Gögn)\Afurð: XML Eining 0..* (Afurð)\Dim3: XML Eining 1..1 (Upphæð)“.
14. Í trénu skal víkka út „snið\Framtal: XML Eining(Framtal)\Gögn: XML Eining 1..* (Gögn)\Afurð: XML Eining 0..* (Afurð)\Dim4: XML Eining 1..1 (Afurð)“.
15. Í trénu skal velja „Safn haus\Fjöldi lína“.
16. Smellið á „Breyta“.
17. Í trénu skal velja „Listi\TELJA“.
18. Smelltu á Bæta við Aðgerð.
19. Í trénu skal víkka út „snið“.
20. Í trénu skal víkka út „snið\Framtal: XML Eining(Framtal)“.
21. Í trénu skal víkka út „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`“.
22. Í trénu skal velja „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`“.
23. Smellt er á Bæta við gagnagjafa.
24. Í svæði Formúla slá inn „TELJA(snið.Yfirlýsing.Gögn.Atriði)“.
    * TALNING(snið.yfirlýsing.gögn.afurð)  
25. Smellið á „Vista“.
26. Lokið síðunni.
27. Í trénu skal velja „Safn haus\Heiti skráar“.
28. Í trénu skal velja „snið\Framtal: XML Eining(Framtal)\Gögn: XML Eining 1..* (Gögn)\Heiti skráar: Afurð Strengur(Heiti skráar)“.
29. Smelltu á Binda.
30. Í trénu skal velja „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)`“.
31. Í trénu skal velja „Safn haus\Safn línur\Afurðanúmer“.
32. Smelltu á Binda.
33. Í trénu skal velja „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)`“.
34. Í trénu skal velja „Safn haus\Safn línur\Upphæð“.
35. Smelltu á Binda.
36. Í trénu skal velja „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)`“.
37. Í trénu skal velja „Safn haus\Safn línur\Grunnvara skrá kenni“.
38. Smelltu á Binda.
39. Í trénu skal velja „Safn haus\Safn línur“.
40. Í trénu skal velja „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`“.
41. Smelltu á Binda.
42. Í trénu skal velja „Safn haus“.
43. Í trénu skal velja „`format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`“.
44. Smelltu á Binda.
45. Smelltu á Vista.
46. Lokið síðunni.
47. Lokið síðunni.
48. Lokið síðunni.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]