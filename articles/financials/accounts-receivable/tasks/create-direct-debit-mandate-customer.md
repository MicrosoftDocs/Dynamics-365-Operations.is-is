---
title: Stofna beingreiðsluumboð fyrir viðskiptavin
description: Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916370"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Stofna beingreiðsluumboð fyrir viðskiptavin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk sýnir stofnun umboð fyrir beingreiðsla -og nota hana á reikningi.


## <a name="create-a-bank-account"></a>Stofna skal bankareikning.
1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.
2. Í listanum velurðu skrá. Veljið til dæmis U.S. 001
3. Í aðgerðasvæðinu er smellt á **Viðskiptavinur**.
4. Smelltu á **Bankareikninga**.
5. Smellt er á **Nýtt**.
6. Í reitinn **Bankareikningar** skal slá inn gildi.
7. Í reitinn **Heiti** skal slá inn gildi.
8. Í reitinn **IBAN** skal slá inn gildi.
9. Í reitinn **Gjaldmiðill** skal slá inn gildi.
10. Smellt er á **Vista**.
11. Lokið síðunni.
12. Í **skoðunarrúðunni** ferðu í **Kerfiseiningar > Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar**.
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Í listanum skal smella á tengilinn í valinni línu.
15. Smellið á **Breyta**.
16. Útvíkkaðu flýtiflipann **Aukakenni**.
17. Í reitinn **Beingreiðslukenni** skal slá inn gildi.
18. Í reitinn **IBAN** skal slá inn gildi.
19. Lokið síðunni.
20. Lokið síðunni.

## <a name="define-the-electronic-payment-method"></a>Skilgreina rafrænu greiðsluaðferðina
1. Í **skoðunarrúðunni** ferðu í **Kerfi > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Greiðsluháttur** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitinn **Greiðslugerð** skal velja „Rafræna greiðslu“. Greiðslugerð fyrir aðferð umboð fyrir beingreiðsla verður að vera Rafrænar greiðslur.
6. Veldu já í reitnum **Krefjast umboðs**.
7. Lokið síðunni.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Bæta umboð fyrir beingreiðsla við viðskiptavin
1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.
2. Í listanum velurðu skrá. Veljið til dæmis U.S. 001
3. Smellið á **Breyta**.
4. Útvíkkaðu flýtiflipann **Sjálfgildi greiðslu**.
5. Færa inn eða velja gildi í reitnum **Greiðsluaðferð**.
6. Útvíkkaðu flýtiflipann **Sjálfgildi greiðslu**.
7. Útvíkkaðu flýtiflipann **Umboð fyrir beingreiðslu**.
8. Smelltu á **Bæta við**.
9. Færa inn eða veljið gildi í svæðinu **Bankareikningur**.
10. Í reitinn **Bankareikningur lánardrottins** skal rita eða velja gildi.
11. Í reitinn **Greiðslutíðni** skal færa inn fjölda greiðslna sem búist er við fyrir þetta umboð.
12. Smellt er á **OK**.
13. Smelltu á **Prenta**.
14. Smellt er á **Umboðsskýrsla**.
15. Lokið síðunni.
16. Smellið á **Breyta**.
17. Í reitinn **Dagsetning undirskriftar** skal færa inn dagsetningu.
18. Smellið á **Já**.
19. Færðu inn Staðurinn þar sem umboðið var undirritað
20. Smellt er á **OK**.
21. Lokið síðunni.

## <a name="create-a-free-text-invoice-with-mandate"></a>Stofna reikningur með frjálsum texta með umboði
1. Í **skoðunarrúðunni** ferðu í **Einingar > Viðskiptakröfur > Reikningar > Allir frjálsir textareikningar**.
2. Smellt er á **Nýtt**.
3. Veljið þann viðskiptavin sem umboðið var bætt við.
4. Í reitinn **Kenni beingreiðsluumboðs** skal færa inn eða velja gildi.

