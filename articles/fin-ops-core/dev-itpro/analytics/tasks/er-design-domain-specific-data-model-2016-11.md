---
title: Rafræn skýrslugerð Hanna lénasértæk gagnalíkön
description: Í þessu efnisatriði er útskýrt hvernig á að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur gagnalíkan fyrir skjöl rafrænna greiðslna.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351c5a6624f7ee912c507a9f74324f4c8f61166b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755035"
---
# <a name="er-design-domain-specific-data-model"></a>Rafræn skýrslugerð Hanna lénasértæk gagnalíkön

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur gagnalíkan fyrir rafræn greiðsluskjöl. Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin eru stofnuð.

Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í hvaða fyrirtæki sem er þar sem ER skilgreiningar eru samnýttar á milli fyrirtækja. Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.

1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.

    Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, „Litware, Inc”. Ef ekki sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.  
    
2. Smelltu á Grunnstillingar skýrslugerðar

    Stofna verður skilgreiningu sem inniheldur gagnalíkan fyrir rafræna greiðsluskjöl. Þessi gagnalíkan verður notaður síðar sem gagnaveita þegar snið fyrir greiðsluskjölin.  

## <a name="create-a-new-data-model-configuration"></a>Stofna nýjan skilgreiningu gagnalíkans
1. Smellt er á stofna skilgreiningu til að opna fellilistanum.
2. Í svæðið Heiti, færðu inn "Greiðslur (einfaldaður líkan)".
3. Færðu inn 'Skilgreining greiðslulíkans' í svæðinu Lýsingu.

    Virkt skilgreiningarveitu er sjálfkrafa færð inn hér. Þessa veitu mun geta unnið með þessa skilgreiningu. Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.  

4. Smellið á hnappinn "Stofna skilgreiningu" að ljúka verkinu fyrir stofnun skilgreiningar

## <a name="create-a-data-model"></a>Stofna gagnalíkan
Verið er að búa til nýtt gagnalíkan fyrir valda grunnstillingu. Þessi útgáfa skilgreiningarinnar mun hafa stöðuna drög.  
1. Smellið á Hönnuður.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>Skilgreina uppbygging aðila sem er í greiðsluferli
1. Smellt er á Nýtt til að opna felligluggann.
2. Í svæði Nafn færirðu inn „Aðili“.
3. Smelltu á Bæta við.
4. Smellt er á Nýtt til að opna felligluggann.
5. Í svæðið Heiti, færðu inn ‚Heiti'.
6. Veljið 'Strengur' í svæðinu Vöru.
7. Smelltu á Bæta við.
8. Í svæði Finna færirðu inn „Aðili“.
9. Smelltu á Finna fyrri.

## <a name="define-the-bank-structure-for-this-model"></a>Skilgreina skipulag banka fyrir þetta líkan
1. Smellt er á Nýtt til að opna felligluggann.
2. Í svæðið Heiti, færðu inn ‚umboðsmaður'.
3. Veljið 'Færslan' í svæðinu Vöru.
4. Smelltu á Bæta við.
5. Í svæði Lýsing, færðu inn „Fjárhagsstofnun“ (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldari/lánardrottinn).

    Fjárhagsstofnun (til dæmis, banki) sem þjónustar lykil fyrir aðila (skuldara/lánardrottin).  

6. Smellt er á Nýtt til að opna felligluggann.
7. Í svæðið Heiti, færðu inn ‚Heiti'. 
8. Veljið 'Strengur' í svæðinu Vöru.
9. Smelltu á Bæta við.
10. Smellt er á Nýtt til að opna felligluggann.
11. Í svæðið Heiti, færðu inn ‚SWIFT'.
12. Smelltu á Bæta við.
13. Í svæði Lýsing slá inn „Auðkenniskóði banka“. 
14. Smellt er á Nýtt til að opna felligluggann.
15. Í svæðið Heiti, færðu inn 'RoutingNumber'.
16. Smelltu á Bæta við.
17. Í svæði Lýsing slá inn „Leiðarnúmer“.
18. Smelltu á Finna fyrri.

## <a name="define-the-bank-account-structure-for-this-model"></a>Skilgreina skipulag bankareikning fyrir þetta líkan
1. Smellt er á Nýtt til að opna felligluggann.
2. Í reitnum Heiti skal færa inn 'Bankareikningur'. 
3. Veljið 'Færslan' í svæðinu Vöru.
4. Smelltu á Bæta við.
5. Í svæði Lýsing slá inn „Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka)“.

    Auðkenning lykils hjá aðila í fjármálastofnun (t.d. banka).  

6. Smellt er á Nýtt til að opna felligluggann.
7. Í svæðið Heiti, færðu inn 'Gjaldmiðils'. 
8. Veljið 'Strengur' í svæðinu Vöru.
9. Smelltu á Bæta við.
10. Í svæði Lýsing slá inn „Gjaldmiðilskóði“.
11. Smellt er á Nýtt til að opna felligluggann.
12. Í svæðið Heiti, færðu inn ‚númer'. 
13. Smelltu á Bæta við.
14. Smellt er á Nýtt til að opna felligluggann.
15. Í svæðið Heiti, færðu inn ‚IBAN-númer'. 
16. Smelltu á Bæta við.
17. Í svæði Lýsing slá inn „Alþjóðlegt bankareikningsnúmer“.

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>Skilgreina uppbygging greiðsluskilaboða fyrir greiðslugerð kreditfærslu
1. Smellt er á Nýtt til að opna felligluggann.
2. Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.
3. Í svæðið Heiti, Færðu inn 'CustomerCreditTransferInitiation'.
4. Smelltu á Bæta við.
5. Í svæði Finna, slá inn „CustomerCreditTransferInitiation“. 
6. Smelltu á Finna fyrri.
7. Smellt er á Nýtt til að opna felligluggann.
8. Í svæðið Heiti, færðu inn 'MessageIdentification'. 
9. Smelltu á Bæta við.
10. Í svæði Lýsing, færið inn Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.

    Tilvísun frá einum stað til annars, eins og úthlutað er af hálfu leiðbeinandi aðila, (og send til næsta aðila í röðinni) til að auðkenna skilaboðin.  

11. Smellt er á Nýtt til að opna felligluggann.
12. Í svæðið Heiti, færðu in 'ProcessingDateTime'.
13. Velja 'DateTime' í svæðinu gerð Vöru.
14. Smelltu á Bæta við.
15. Í svæðinu Lýsing færa inn „Dagsetningu og tíma sem greiðsluskilaboðin var stofnuð“. 
16. Smellt er á Nýtt til að opna felligluggann.

    Skilgreina skipulag greiðslufærsla fyrir þetta líkan.  

17. Í svæðið Heiti, færðu inn 'Greiðslur'.
18. Veljið í svæðinu gerð Vöru „Skrárlisti".
19. Smelltu á Bæta við.
20. Færið inn 'Greiðslulínur fyrir gildandi skilaboð' í svæðinu Lýsingu.
21. Smellt er á Nýtt til að opna felligluggann.
22. Í svæðið Heiti, færðu inn 'Lánardrottins'. 
23. Veljið 'Færslan' í svæðinu Vöru.
24. Smelltu á Bæta við.
25. Færið inn „Aðili sem á að taka á móti fjárhæð“ í svæðinu Lýsingu. 
26. Smellt er á Skipta um vörutilvísun.
27. Í svæði Finna færirðu inn „Aðili“.
28. Smellt er á Finna næsta.
29. Smellt er á Í lagi.
30. Í svæði Finna færirðu inn „Greiðslur“.
31. Smellt er á Finna næsta.
32. Smellt er á Nýtt til að opna felligluggann.
33. Í svæðið Heiti, færðu inn ‚skuldari'. 
34. Smelltu á Bæta við.
35. Í svæðinu Lýsing, færðu inn „Aðili sem skuldar lánveitanda (til þrautavara) tiltekna fjárhæð“.
36. Smellt er á Skipta um vörutilvísun.
37. Í svæði Finna færirðu inn „Aðili“.
38. Smellt er á Finna næsta.
39. Smellt er á Í lagi.
40. Smellt er á Finna næsta.
41. Smellt er á Nýtt til að opna felligluggann.
42. Í reitnum Heiti skal færa inn ‚Lýsing'.
43. Veljið 'Strengur' í svæðinu Vöru.
44. Smelltu á Bæta við.
45. Smellt er á Nýtt til að opna felligluggann.
46. Í svæðið Heiti, færðu inn 'Gjaldmiðils'.
47. Smelltu á Bæta við.
48. Í svæði Lýsing slá inn „Gjaldmiðilskóði“.
49. Smellt er á Nýtt til að opna felligluggann.
50. Í reitnum Heiti skal færa inn ‚TransactionDate'. 
51. Velja 'Dagsetning' í svæðinu gerð vöru.
52. Smelltu á Bæta við.
53. Í svæði Lýsing slá inn „Færsludagsetning“. 
54. Smellt er á Nýtt til að opna felligluggann.
55. Í reitnum Heiti skal færa inn ‚InstructedAmount'.  
56. Veljið 'Raunveruleg' í svæðinu gerð vöru.
57. Smelltu á Bæta við.
58. Í svæðinu Lýsing, færðu inn „Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað“. Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um.

    Peningafjárhæð sem á að færa á milli skuldara og lánardrottins, áður en frádráttur gjalda á sér stað. Upphæð skal sett fram í þeim gjaldmiðli sem upphafsaðili segir til um  

59. Smellt er á Nýtt til að opna felligluggann.
60. Í svæðið Heiti, færðu inn 'End2EndID'. 
61. Veljið 'Strengur' í svæðinu Vöru.
62. Smelltu á Bæta við.
63. Í svæði Lýsing, slá inn „Einkvæmt kenni sem úthlutað er af upphafsaðila“. Þessi auðkenning er færð áfram, óbreytt, í gegnum alla keðjuna, enda á milli 
64. Í svæðið Heiti, færðu inn 'PaymentModel'.

    Heiti PaymentModel stemmir sig af við með fyrirfram skilgreindum viðmót greiðsluskjámyndir.  

65. Smellið á „Vista“.
66. Lokið síðunni.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]