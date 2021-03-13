---
title: Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)
description: Í þessu efnisatriði er útskýrt hvernig á að stofna nýja skilgreiningu rafrænnar skýrslugerðar sem inniheldur sniðmát til að mynda rafræn skjöl á OPENXML-sniði.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b832961061d05e3f1ae046f820bc7a37baaf90c
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092667"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði. Þessi skilgreining verður notuð til að vinna greiðslur lánardrottna.

Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í GBSI fyrirtæki.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”. Einnig verður að hafa Excel-skráin sem verður flutt inn þegar sniðmátið er stofnuð. Hægt er að fá aðgang að þessari skrá í [Sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>Hlaða upp skilgreiningu greiðslugagnalíkans.
1. Farðu í **Einingar > Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.
2. Í listanum merkirðu skilgreiningarveitu fyrir dæmi um fyrirtæki, veljið Litware, Inc. Ef þessi skilgreiningarveita sést ekki verður fyrst að ljúka við skrefin í [Stofna skilgreiningarveitur og merkja þær sem virkar](er-configuration-provider-mark-it-active-2016-11.md).
3. Veldu **Stilla sem virkt**.
4. Veldu **Geymslur**. Velja gagnasafn fyrir gerðina Rekstrartilföng, ef tiltækur. Ef hennar er tiltæk, sleppa eftirfarandi skref um stofnun nýja gagnasafns.  
5. Veldu **Bæta við** til að opna felligluggann.
6. Í reitnum **Gerð geymslu fyrir grunnstillingar**, færirðu inn `Operations resourcesdd`.
7. Veljið **Stofna geymslu**.
8. Veljið **Í lagi**.
9. Veljið **Opna**.
10. Í trénu skal velja **Greiðslulíkan**.
11. Velja **Innflutningur**. Flytja inn þetta gagnalíkan. Það verður notað sem gagnagjafi í nýja skilgreiningu sniðs. Sleppa þessu þrepi ef skilgreiningin hefur þegar verið flutt.  
12. Velja skal **Já**.
13. Lokaðu síðunum þar til þú kemur aftur á rafrænu skýrslusíðuna.

## <a name="create-a-new-format-configuration"></a>Stofna nýja skilgreiningu á sniði
1. Veldu **Skilgreiningar skýrslugerðar**.
2. Í trénu skal velja **Greiðslulíkan**.
3. Veldu **Stofna skilgreiningu** til að opna felligluggann.
4. Í reitinn **Nýtt** skal slá inn `Format based on data model PaymentModel`. Stofna snið sem byggir á gagnalíkani PaymentModel.
5. Í reitinn **Heiti** skaltu færa inn `Sample worksheet report`. Dæmi um vinnublaðsskýrslu  
6. Á svæðinu **Lýsing** skal færa inn `Sample worksheet report for vendors' payments`. Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna.  
7. Í svæðinu **Skilgreining gagnalíkans** skal færa inn eða velja gildi. Veljið skilgreininguna **CustomerCreditTransferInitiation**.  
8. Veljið **Stofna skilgreiningu**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Hanna nýtt skjal í sniði OPENXML vinnublaði
1. Í trénu skal velja **greiðslulíkan\dæmi um vinnublaðsskýrslu**.
2. Veljið **Hönnuður**.
3. Á Aðgerðasvæðinu skal velja **Flytja inn**.
4. Veldu **Flytja inn úr Excel**.
5. Veldu **Viðhengi**. Tengja fyrirliggjandi Excel-skjalið sem sniðmát.  
6. Veljið **Nýtt**.
7. Veldu **Skrá**. Benda á fyrirliggjandi Excel-skrá.  
8. Lokið síðunni.
9. Sláið inn eða veldu gildi í reitnum **sniðmát**. Veljið viðhengda Excel-skráin sem nota á sem sniðmát.  
10. Veljið **Í lagi**. Athugið að sniðshlutar Rafræn skýrslugerð hafa verið stofnað í hönnunarsniði sem byggir á uppbygging MS Excel-skjals sem vísað er úr (nefnd svið).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Stofna nýja gagnagjafa til að reikna samtölur eftir gjaldmiðilskóða
1. Veldu flipann **Vörpun**.
2. Veldu **Bæta við rót** til að opna felligluggann.
3. Í trénu skal velja **virkni\Flokka eftir**.
4. Í reitinn **Heiti** skaltu færa inn `PaymentByCurrency`.
5. Veldu **Breyta hópi eftir**.
6. Stækkaðu í trénu **tegund**, veldu síðan **líkan\Greiðslur**.
7. Veldu **Bæta reit við**.
8. Veldu **Hvað skal flokka**.
9. Stækkaðu í trénu **líkan\Greiðslur**, veldu síðan **líkan\Greiðslur\Gjaldmiðill**.
10. Veldu **Bæta reit við**.
11. Veldu **Flokkaðir reitir**.
12. Í trénu veljið **model\Payments\Instructed Amount(InstructedAmount)**.
13. Veldu **Bæta reit við**, veldu síðan **Uppsöfnunarsvið**.
14. Veljið valkost í retinum **aðferð**. Velja aðgerðina **Uppsöfnuð SAMTALA**.  
15. Í reitinn **Heiti** skaltu færa inn `TotalInstructuredAmount`.
16. Veljið **Vista**.
17. Lokið síðunni.
18. Veljið **Í lagi**.

## <a name="map-format-components-to-data-sources"></a>Varpa sniðsíhlutum í gagnagjafa
1. Í trénu skal útvíkka **model\Payments\Initiating Party(InitiatingParty)\Name** og **Excel\ReportHeader\CompanyName**.
2. Veldu **Binda**.
3. Í trénu skal velja **model\Payments\Creditor\Identification\Source ID(SourceID)** og **Excel\PaymLines\VendAccountName**.
4. Veldu **Binda**.
5. Veldu í trénu **model\Payments\Creditor\Name** og **Excel\PaymLines\VendName**.
6. Veldu **Binda**.
7. Veldu í trénu **model\Payments\Creditor Agent(CreditorAgent)\Name** og **Excel\PaymLines\Bank**.
8. Veldu **Binda**.
9. Veldu í trénu **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** og **Excel\PaymLines\RoutingNumber**.
10. Veldu **Binda**.
11. Veldu í trénu **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** og **Excel\PaymLines\AccountNumber**.
12. Veldu **Binda**.
13. Veldu í trénu **model\Payments\Instructed Amount(InstructedAmount)** og **Excel\PaymLines\Debit**.
14. Veldu **Binda**.
15. Veldu í trénu **model\Payments\Currency** og **Excel\PaymLines\Currency**.
16. Veldu **Binda**.
17. Veldu í trénu **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency**.
18. Veldu **Binda**.
19. Veldu í trénu **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount**.
20. Veldu **Binda**.
21. Í trénu velurðu **PaymentByCurrency** og **Excel\SummaryLines**.
22. Veldu **Binda**.
23. Í trénu velurðu **model\Payments** og **Excel\PaymLines**.
24. Veldu **Binda**.
25. Veljið **Vista** og lokið síðan síðunni.

## <a name="use-the-created-configuration-for-payments-processing"></a>Nota stofnaða grunnstillingu fyrir greiðsluvinnslu
1. Veljið **Breyta stöðu**.
2. Velja **Lokið**.
3. Veljið **Í lagi**.
4. Í skoðunarrúðunni ferðu í **Kerfi > Viðskiptaskuldir > Greiðsluuppsetning > Greiðsluhættir**.
5. Nota flýtiafmörkun til að sía í svæði **Greiðsluháttur** með gildinu **Rafrænt**.
6. Veljið **Breyta**.
7. Útvíkkaðu hlutann **Skráarsnið**.
8. Velja skal **Já** í reitnum **Almenn rafræn skýrslugerð**.
9. Færa inn eða velja gildi í reitnum **Skilgreining útflutningssniðs**. Veljið skilgreininguna **Dæmi um vinnublaðsskýrslu**.  
10. Veljið **Vista**.
11. Lokið síðunni.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Nota stofnaða skilgreiningu fyrir prófun á vinnslu greiðslubóka
1. Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Greiðslur > Greiðslubók**.
2. Veldu **Nýr** til að stofna nýja greiðslubók.
3. Í svæðið **Heiti** skal slá inn **VendPay**.
4. Veldu **Línur**.
5. Í reitnum **Lykill** skal færa inn gildin `GB_SI_000001`.
6. Stilltu **Debet** á `1000`.
7. Veljið **Nýtt**.
8. Í reitnum **Lykill** skal færa inn gildin `GB_SI_000005`.
9. Stilltu **Debet** á `2000`.
10. Í reitinn **Gjaldmiðill** skal slá inn `EUR`.
11. Í reitinn **Mótlykill** skal tilgreina gildin `GBSI OPER`.
12. Í reitnum **Greiðsluháttur** skal slá inn `Electronic`.
13. Veljið **Vista**.
14. Veldu **Búa til greiðslur**.
15. Í reitnum **Greiðsluháttur** skal slá inn `Electronic`.
16. Í reitnum **Heiti skrár** færðu inn `Payments`.
17. Í reitinn **Bankareikningar** skal slá inn `GBSI OPER`.
18. Veldu **Í lagi** og síðan aftur **Í lagi**. Fara yfir stofnaðar vinnublað, þar á meðal upplýsingar um greiðslulínur ásamt samtölur fyrir hvern gjaldmiðilskóði sem notaður er í þessum greiðsluskilaboðum.  

