---
title: Breyta líkani og vörpun til að búa til skjöl sem eru með forritsgögnum
description: Í þessu efni er útskýrt hvernig á að hanna skilgreiningar skýrslugerðar til að mynda rafrænt skjal og uppfæra forritsgögn. (Hluti 2 - Mynda skjöl).
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
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567093"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Breyta líkani og vörpun til að búa til skjöl sem eru með forritsgögnum

[!include [banner](../../includes/banner.md)]

Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið „ER Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 2: Búa til skjöl)“. 

Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit. Í þessu ferli muntu breyta Rafræna skýrslugerð (ER) grunnstillingar þannig að hægt sé að byrja að nota þær til að búa til rafræn skjöl og uppfæra gögn fyrir forrit. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Skrefin er hægt að klára með því að nota DEMF gagnasafn.


## <a name="modify-data-model"></a>Breyta gagnalíkani
1. Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.
2. Í trénu skal velja „Intrastat (líkan)“.
    * Þú munt útvíkka það hvernig þú notar gagnalíkanið. Fyrir utan að nota það sem gagnaveitu til að búa til Intrastat skýrsluna, verður gagnalíkanið notað til að safna upplýsingum um Instrastat skýrslugerðarferlið. Upplýsingarnar verða síðan notaðar til að uppfæra gögn fyrir forrit.   
3. Smellið á Hönnuður.
4. Smellt er á Nýtt til að opna felligluggann.
5. Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.
6. Í reitnum Heiti skal færa inn „Fyrir gagnauppfærslu fyrir forrit“.
    * Fyrir uppfærsla gagna hugbúnaðarins  
7. Smelltu á Bæta við.
8. Í trénu skal velja „Fyrir gagnauppfærslu fyrir forrit“.
    * Þessu nýja rótaratriði er bætt við til að tilgreina gagnaflæði fyrir gögn á hreyfingu frá Intrastat skýrslunni (notuð sem gagnaveitu) til tafla forrits (áfangastaður uppfærslu). Athugið að mismunandi rótaratriði verður að nota til að sækja gögn sem eru bókuð í skjal á útleið og til að sækja gögn frá skjalinu sem er notað til að uppfæra gögn fyrir forrit.   
9. Smellt er á Nýtt til að opna felligluggann.
10. Í svæðið Heiti, færðu inn „Safn haus“.
    * Safnshaus  
11. Veljið í svæðinu gerð Vöru „Skrárlisti".
12. Smelltu á Bæta við.
    * Þú munt stofna skrá fyrir hverja Intrastat skýrslu sem er búin til, og þess vegna þarftu að búa til nýtt atriði fyrir það.  
13. Smellt er á Nýtt til að opna felligluggann.
14. Í svæðið Heiti, færðu inn 'skrárnafn'.
    * Skrárnafn  
15. Veljið 'Strengur' í svæðinu Vöru.
16. Smelltu á Bæta við.
17. Smellt er á Nýtt til að opna felligluggann.
18. Í svæðið Heiti, færðu inn “Númer lína“.
    * Línufjöldi  
19. Velja „Heiltala“ í svæðinu gerð Vöru.
20. Smelltu á Bæta við.
    * Bættu þessu atriði við til að tákna númer Intrastat færslnanna sem eru skráðar á meðan núverandi skráningarferli stendur.  
21. Smellt er á Nýtt til að opna felligluggann.
22. Í svæðið Heiti, færðu inn „Safn línur“.
    * Safnslínur  
23. Veljið í svæðinu gerð Vöru „Skrárlisti".
24. Smelltu á Bæta við.
    * Bættu þessu atriði við til að tákna lista Intrastat færslnanna sem eru skráðar á meðan núverandi skráningarferli stendur.  
25. Smellt er á Nýtt til að opna felligluggann.
26. Í reitnum Heiti skal færa inn ‚Upphæð'.
    * Upphæð  
27. Veljið 'Raunveruleg' í svæðinu gerð vöru.
28. Smelltu á Bæta við.
29. Smellt er á Nýtt til að opna felligluggann.
30. Í svæðið Heiti, færðu inn „Grunnvara skrá kenni“.
    * Vöru skrá kenni  
31. Velja „Int64“ í svæðinu gerð Vöru.
32. Smelltu á Bæta við.
33. Smellt er á Nýtt til að opna felligluggann.
34. Í reitnum Heiti skal færa inn „Númer afurðar“
    * Vörunúmer  
35. Veljið 'Strengur' í svæðinu Vöru.
36. Smelltu á Bæta við.
37. Smellið á „Vista“.
38. Lokið síðunni.

## <a name="modify-model-mapping"></a>Breyta Vörpun líkans
1. Í trénu skal víkka út „Intrastat (líkan)“.
2. Í trénu skal velja „Intrastat (líkan)\Intrastat (vörpun)“.
    * Breyta fyrirliggjandi vörpun líkans til að hefja notkun þess fyrir uppfærslu gagna fyrir forrit og til að skjala upplýsingar um Intrastat skýrslugerð.  
3. Smellið á Hönnuður.
4. Smellið á „Nýtt“.
5. Í svæðið Heiti, færðu inn „Uppfæra safn“.
    * Uppfæra safn  
6. Í reitnum Stefna skal velja „Til viðtökustaðar".
7. Smellið á „Vista“.
    * Þessu nýja rótaratriði er bætt við til að tilgreina gagnaflæði fyrir gögn á hreyfingu frá Intrastat skýrslunni (notuð sem gagnaveitu) til tafla forrits (áfangastaður uppfærslu). Athugið að mismunandi rótaratriði líkans verður að nota til að sækja gögn frá forritinu fyrir skýrslugerðarferlið og síðan nota gögnin úr gagnalíkaninu fyrir uppfærslu hugbúnaðargagna.   
8. Smellið á Hönnuður.
9. Í trénu skal velja „Gagnalíkan\Gagnalíkan“.
    * Bættu við þeirri gagnaveitu sem er krafist Þetta er gagnalíkanið sem inniheldur upplýsingar um skráðar Intrastat færslur sem verða að vera skjalaðar.  
10. Smella á bæta Við rót.
11. Í reitnum Heiti skal færa inn „líkan“.
    * líkan  
12. Sláið inn eða veldu gildið „Fyrir gagnauppfærslu fyrir forrit“ í reitnum Skilgreining.
    * Fyrir uppfærsla gagna hugbúnaðarins  
13. Smellt er á Í lagi.
14. Í trénu skal víkka út 'model'.
15. Veljið 'Functions\Calculated svæðið', í trénu.
16. Í trénu skal velja „Líkan\Safn haus“.
17. Smelltu á Bæta við.
    * Þar sem þú vilt tölusetja skráðar Intrastat færslur í skjölun, verður að bæta við viðeigandi gagnaveitu.  
18. Í svæðið Heiti, færðu inn „Tölusettar línur“.
    * Tölusettar línur  
19. Smellt er á Breyta formúla.
20. Í trénu skal velja „Listi\TÖLUSETJA“.
21. Smelltu á Bæta við Aðgerð.
22. Í trénu skal víkka út 'model'.
23. Í trénu skal víkka út „Líkan\Safn haus“.
24. Í trénu skal víkka út „Líkan\Safn haus\Safn línur“.
25. Smellt er á Bæta við gagnagjafa.
26. Í svæði Formúla slá inn „SKEYTA SAMAN(líkan.„Safn haus“ „Safn línur“)“.
    * TÖLUSETJA(líkan.„Safn haus“ „Safn línur“)  
27. Smellið á „Vista“.
28. Lokið síðunni.
29. Smellið á „Í lagi“.
30. Smelltu á Bæta við Áfangastað
    * Bæta við forritstöflum sem áskildum viðtökustað sem krefst uppfærslna til að skjala upplýsingar um skráðar Instrastat færslur.  
31. Í svæðið Heiti, færðu inn „Safn“.
    * Safnvista  
32. Í svæðið Heiti töflu skal færa inn „IntrastatArchiveGeneral“.
    * IntrastatArchiveGeneral  
    * Haltu skýrsluaðgerðinni „Setja inn“ svo þú getir bætt skýrslum við á meðan skjölun upplýsinga um hvert Intrastat skýrslugerðarferli fer fram.  
33. Veljið Já í svæðinu Færsla upplskrá.
    * Veldu Já til að fá upplýsingar um vandkvæði varðandi gagnauppfærslu hugbúnaðarins.  
34. Veljið Já í svæðinu Sleppa færsla aðgerð villuleit.
    * Veldu Já til að draga úr villum við villuleit um auða „Intrastat safnkenni“ reitinn. Þetta verður gert eftir að skrám hefur verið bætt við, byggðar á númeraraðastillingum sem eru grunnstilltar fyrir þessa töflu í skjámyndinni Erlend viðskipti færibreytur.  
35. Smellið á „Í lagi“.
    * Binda einingar úr viðbættri gagnaveitu (afmarkað líkan byggt á völdu rótaratriði) við einingar frá viðbættum viðtökustað.  
36. Í trénu skal víkka út „Safn“.
37. Í trénu skal víkka út „Safn\<Tengsl“.
38. Í trénu skal víkka út „Safn\<Tengsl\IntrastatArchiveDetail“.
39. Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Upphæð(UpphæðMST)'.“.
40. Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur“.
41. Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur\Gildi“.
42. Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur\Gildi\Upphæð“.
43. Smelltu á Binda.
44. Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Grunnvara(IntrastatCommodity)“.
45. Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Gildi\Grunnvara skrá kenni“.
46. Smelltu á Binda.
47. Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Afurðanúmer(ItemIdi)“.
48. Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Gildi\Afurðanúmer“.
49. Smelltu á Binda.
50. Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Lína númer(LineNumber)“.
51. Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Númer“.
52. Smelltu á Binda.
53. Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail“.
54. Í trénu skal velja „Líkan\Safn haus\Tölusettar línur“.
55. Smelltu á Binda.
56. Í trénu skal velja „Safn\Heiti skráar (FileName)“.
57. Í trénu skal velja „Líkan\Safn haus\Heiti skráar“.
58. Smelltu á Binda.
59. Í trénu skal velja „Safn\Fjöldi lína(NumberOfLines)“.
60. Í trénu skal velja „Líkan\Safn haus\Fjöldi lína“.
61. Smelltu á Binda.
62. Í trénu skal velja „Safn“.
63. Í trénu skal velja „Líkan\Safn haus“.
64. Smelltu á Binda.
65. Smellið á „Vista“.
66. Lokið síðunni.
67. Lokið síðunni.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]