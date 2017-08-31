--- 
title: "Hanna skilgreiningu fyrir myndun skýrslna á OpenXML-sniði fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d552dbcf932813de4d060b4f2190cf388eddb1bf
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Hanna skilgreiningu fyrir myndun skýrslna á OpenXML-sniði fyrir rafræna skýrslugerð (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði. Þessi skilgreining verður notuð til að vinna greiðslur lánardrottna.



Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í GBSI fyrirtæki.



Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka". Einnig verður að hafa Excel-skráin sem verður flutt inn þegar sniðmátið er stofnuð. Þessi skrá er hægt að fá aðgang að í: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx


## <a name="upload-the-payments-data-model-configuration"></a>Hlaða upp skilgreiningu greiðslugagnalíkans.
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
2. Í listanum skal merkja valda línu.
    * Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, veljið 'Litware, Inc.' Ef sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".  
3. Smellt á Stilla sem virkt.
4. Smella á Geymslur.
    * Velja gagnasafn fyrir gerðina Rekstrartilföng, ef tiltækur. Ef hennar er tiltæk, sleppa eftirfarandi skref um stofnun nýja gagnasafns.  
5. Smelltu á Bæta við til að opna felligluggann.
6. Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".
7. Smellið á Stofna gagnasafn.
8. Smellið á „Í lagi“.
9. Smellt er á Opin.
10. Í trénu skal velja „Greiðslulíkan“.
11. Smelltu á Flytja inn.
    * Flytja inn þetta gagnalíkan. Það verður notað sem gagnagjafi í nýja skilgreiningu sniðs. Sleppa þessu þrepi ef skilgreiningin hefur þegar verið flutt.  
12. Smella á Já.
13. Lokið síðunni.
14. Lokið síðunni.

## <a name="create-a-new-format-configuration"></a>Stofna nýja skilgreiningu á sniði
1. Smelltu á Grunnstillingar skýrslugerðar
2. Í trénu skal velja „Greiðslulíkan“.
3. Smellt er á stofna skilgreiningu til að opna fellilistanum.
4. Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.
    * Stofna snið sem byggir á gagnalíkani PaymentModel.  
5. Í svæðið Heiti, Færðu inn 'dæmi um vinnublaðsskýrslu '.
    * Dæmi um vinnublaðsskýrslu  
6. ÆU reitnum Lýsing, færðu inn "Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna".
    * Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna.  
7. Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.
    * Veljið skilgreininguna 'CustomerCreditTransferInitiation'.  
8. Smelltu á Stofna skilgreiningu.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Hanna nýtt skjal í sniði OPENXML vinnublaði
1. Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.
2. Smellið á Hönnuður.
3. Í aðgerðasvæðinu er smellt á innflutningur.
4. Smella á Flytja inn úr Excel
5. Smellt er á viðhengi
    * Tengja fyrirliggjandi Excel-skjalið sem sniðmát.  
6. Smellið á „Nýtt“.
7. Smella á Skrá
    * Benda á fyrirliggjandi Excel-skrá.  
8. Lokið síðunni.
9. Sláið inn eða veldu gildi í reitnum sniðmát.
    * Veljið viðhengda Excel-skráin sem nota á sem sniðmát.  
10. Smellið á „Í lagi“.
    * Athugið að sniðshlutar Rafræn skýrslugerð hafa verið stofnað í hönnunarsniði sem byggir á uppbygging MS Excel-skjals sem vísað er úr (nefnd svið).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Stofna nýja gagnagjafa til að reikna samtölur eftir gjaldmiðilskóða
1. Smelltu á flipann Vörpun.
2. Smelltu á Bæta við rót til að opna felligluggann.
3. Í trénu skal velja „virkni\Flokka eftir“.
4. Í reitnum Heiti skal færa inn 'PaymentByCurrency'.
    * PaymentByCurrency  
5. Smella á Breyta hópi eftir
6. Í trénu skal víkka út 'model'.
7. Veljið 'model\Payments', í trénu.
8. Smellt er á Bæta reit við
9. Veldu hvað skal flokka
10. Í trénu skal víkka út 'model\Payments'.
11. Veljið 'líkan\greiðslur', í trénu.
12. Smellt er á Bæta reit við
13. Smellt er á Flokkaðir reitir
14. Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.
15. Smellt er á Bæta reit við
16. Smellt er á Uppsöfnunarreitir
17. Veljið valkost í svæðinu aðferð.
    * Velja samsteypuaðgerðina SAMTÖLU.  
18. Í reitnum Heiti skal færa inn 'TotalInstructuredAmount'
    * TotalInstructuredAmount  
19. Smellið á „Vista“.
20. Lokið síðunni.
21. Smellið á „Í lagi“.

## <a name="map-format-components-to-data-sources"></a>Varpa sniðsíhlutum í gagnagjafa
1. Í trénu skal víkka út 'model'.
2. Í trénu skal víkka út 'model\Payments'.
3. Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)'.
4. Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)\Name'.
5. Í tré skal víkka 'Excel\ReportHeader'.
6. Í tré skal velja 'Excel\ReportHeader\CompanyName'.
7. Smelltu á Binda.
8. Útvíkka 'model\Payments\Creditor', í trénu.
9. Í trénu skal útvíkka 'model\Payments\Creditor\Identification'.
10. Í trénu skal velja 'model\Payments\Creditor\Identification\Source ID(SourceID)'.
11. Í tré skal víkka 'Excel\PaymLines'.
12. Í tré skal velja 'Excel\PaymLines\VendAccountName'.
13. Smelltu á Binda.
14. Veljið 'model\Payments\Creditor\Name', í trénu.
15. Í tré skal velja 'Excel\PaymLines\VendName'.
16. Smelltu á Binda.
17. Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.
18. Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Name'.
19. Í tré skal velja 'Excel\PaymLines\Bank'.
20. Smelltu á Binda.
21. Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.
22. Í tré skal velja 'Excel\PaymLines\RoutingNumber'.
23. Smelltu á Binda.
24. Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.
25. Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)\Identification'.
26. Í trénu skal velja 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.
27. Í tré skal velja 'Excel\PaymLines\AccountNumber'.
28. Smelltu á Binda.
29. Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.
30. Í tré skal velja 'Excel\PaymLines\Debit'.
31. Smelltu á Binda.
32. Útvíkka 'model\Payments\Creditor', í trénu.
33. Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.
34. Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.
35. Veljið 'líkan\greiðslur', í trénu.
36. Í tré skal velja 'Excel\PaymLines\Currency'.
37. Smelltu á Binda.
38. Í trénu skal víkka út 'PaymentByCurrency'.
39. Í trénu skal víkka út 'PaymentByCurrency\grouped'.
40. Í trénu skal velja 'PaymentByCurrency\grouped\Currency'.
41. Í tré skal víkka 'Excel\SummaryLines'.
42. Í tré skal velja 'Excel\SummaryLines\SummaryCurrency'.
43. Smelltu á Binda.
44. Í trénu skal víkka út 'PaymentByCurrency\aggregated'.
45. Í trénu skal velja 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.
46. Í tré skal velja 'Excel\SummaryLines\SummaryAmount'.
47. Smelltu á Binda.
48. Í trénu skal velja 'PaymentByCurrency'.
49. Í tré skal velja 'Excel\SummaryLines'.
50. Smelltu á Binda.
51. Veljið 'model\Payments', í trénu.
52. Í tré skal velja 'Excel\PaymLines'.
53. Smelltu á Binda.
54. Smellið á „Vista“.
55. Lokið síðunni.

## <a name="use-the-created-configuration-for-payments-processing"></a>Nota stofnaða grunnstillingu fyrir greiðsluvinnslu
1. Smellið á „Breyta stöðu“.
2. Smelltu á Ljúka.
3. Smellið á „Í lagi“.
4. Lokið síðunni.
5. Lokið síðunni.
6. Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
7. Nota flýtiafmörkun til að sía í svæði Greiðsluháttur með gildinu „Rafrænt“.
    * Rafrænt  
8. Smellið á „Breyta“.
9. Útvíkka hlutann Skráarsnið.
10. Velja skal Já í Almennan rafræna skýrslugerð svæði.
11. Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.
    * Veljið skilgreininguna 'Dæmi um vinnublaðsskýrslu'.  
12. Smellið á „Vista“.
13. Lokið síðunni.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Nota stofnaða skilgreiningu fyrir prófun á vinnslu greiðslubóka
1. Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
    * Stofna nýja greiðslubók.  
3. Í svæðið Heiti skal slá inn ‚VendPay'.
    * VendPay  
4. Smellið á „Línur“.
5. Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000001'.
    * GB_SI_000001  
6. Stilla debet á '1000'.
7. Smellið á „Nýtt“.
8. Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000005'.
    * GB_SI_000005  
9. Stilla debet á '2000'.
10. Í reitinn gjaldmiðill skal slá inn EUR.
    * EUR  
11. Í reitinn Mótlykill skal tilgreina gildin ''GBSI OPER'.
    * GBSI OPER  
12. Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.
    * Rafrænt  
13. Smellið á „Vista“.
14. Smelltu á Mynda greiðslur.
15. Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.
    * Rafrænt  
16. Í svæði Skráarheiti skal slá inn „Greiðslur“.
    * Til dæmis, skráið greiðslur.  
17. Í reitinn Bankareikningar skal slá inn 'GBSI OPER'.
    * GBSI OPER  
18. Smellið á „Í lagi“.
19. Smellið á „Í lagi“.
    * Fara yfir stofnaðar vinnublað, þar á meðal upplýsingar um greiðslulínur ásamt samtölur fyrir hvern gjaldmiðilskóði sem notaður er í þessum greiðsluskilaboðum.  


