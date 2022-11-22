---
title: Flytja inn kreditbréf
description: Þetta ferli fer í gegnum ferlið fyrir innflutning á kreditbréfs.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f07748c2dc41f6411add1d54589652baa7fc3fbb
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779439"
---
# <a name="import-letter-of-credit"></a>Flytja inn kreditbréf

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir innflutning á kreditbréfs. Setja verður upp eftirfarandi áður en þessi ferli er klárað: banka aðstöðu, forstillingar bókunar , bankaaðstöðusamningnum og upplýsingar um banka lánardrottins.

Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Stofna innkaupapöntun með kreditbréfi
1. Fara til **Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Lánardrottnalykill** skal færa inn eða velja gildi.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Víkkaðu út hlutann **Almennt**.
7. Í reitnum **Svæði** slærðu inn eða velur gildi.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í reitnum **Vöruhús** slærðu inn eða velur gildi.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Í reitinn **Dagsetning reikningsskila** slærðu inn dagsetningu.
12. Í reitinn **Afhendingardagur** færirðu inn dagsetningu.
    * Athugið: The **Tegund bankaskjals** sviði ætti að vera **Bankaábyrgð**.  
13. Smellt er á **OK**.
14. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
16. Í listanum skal smella á tengilinn í valinni línu.
17. Útvíkkaðu hlutann **upplýsingar Línu**.
18. Smelltu á **Afhending** flipa.
19. Í reitinn **Afhendingardagur** færirðu inn dagsetningu.
20. Í reitnum **Staðfestur afhendingardagur** skal rita dagsetningu.
21. Í reitnum **Einingarverð** skal slá inn tölu.
    * Skilgreina upplýsingar kreditbréfs.  
22. Smelltu á aðgerðarrúðuna **Stjórna**.
23. Smellur **Innheimtubréf/innflutnings**.
24. Í **Umsóknardagur** reit, sláðu inn dagsetningu og tíma.
    * Staðfestu að **bankareikning** reiturinn hefur sjálfgefinn virkan bankareikning, sem er byggður á umsóknardegi.  
25. Í **Númer bankaskjals** reit, sláðu inn gildi.
26. Í **Dagsetning móttöku** reit, sláðu inn dagsetningu og tíma.
27. Stækkaðu **Bankaskjal** kafla.
28. Í **Gildistími** reit, sláðu inn dagsetningu og tíma.
29. Stækkaðu **bankaupplýsingar** kafla.
30. Í **Ráðgjafarbanki** reit, sláðu inn eða veldu gildi.
31. Í listanum skal smella á tengilinn í valinni línu.
32. Smelltu á **Vista**.
33. Smellur **Sæktu innkaupapöntunarsendingar**.
34. Lokið síðunni.
35. Í aðgerðasvæðinu skal smella á **Innkaup**.
36. Smellið á **Staðfesta**.
37. Smelltu á aðgerðarrúðuna **Stjórna**.
38. Smellur **Greiðslubréf / innflutningsheimta**.
39. Smelltu á **Vinnslu**.
40. Smellið á **Staðfesta**.
    * Staðfesta aðstöðustaða minnkar upphæð innkaupapöntunar. Í þessu dæmi Innkaupaupphæð = 500,00, aðstöðuhámark = 10000.00, því aðstöðustaða = 9500.00.  
41. Lokið síðunni.
42. Í reitnum **Einingarverð** skal slá inn tölu.
43. Smelltu á **Vista**.
44. Í aðgerðasvæðinu skal smella á **Innkaup**.
45. Smellið á **Staðfesta**.
    * Lagfæra kreditbréf, vegna breytinga í einingaverði.  
46. Smelltu á aðgerðarrúðuna **Stjórna**.
47. Smellur **Greiðslubréf / innflutningsheimta**.
    * Lagfæra kreditbréf, vegna breytinga á einingarverð Innkaupapöntunar.  
48. Smelltu á **Vinnslu**.
49. Smellur **Breyta**.
50. Smellur **Fjarlægja**.
51. Smellið á **Já**.
52. Smellur **Sæktu innkaupapöntunarsendingar**.
53. Smelltu á **Vinnslu**.
54. Smellið á **Staðfesta**.
    * Staðfesta aðstöðustaða minnkar upphæð innkaupapöntunar. Í þessu dæmi er hægt að breyta upphæð Innkaupa = 600,00, aðstöðuhámark = 10000.00, því aðstöðustaða = 9400.00.  
55. Lokið síðunni.

## <a name="post-packing-slip"></a>Bóka fylgiseðil
1. Í aðgerðasvæðinu skal smella á **Móttaka**.
2. Smellið á **Innhreyfingarskjal afurða**.
3. Í **PurchParmTable_Num** reit, sláðu inn gildi.
    * Veljið númer Sendingar stofnaðar með tilvísan í kreditbréfi.  
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í **Dagsetning móttöku vöru** reit, sláðu inn dagsetningu.
6. Smellt er á **OK**.
7. Lokið síðunni.
8. Lokið síðunni.

## <a name="verify-import-letter-of-credit-status"></a>Staðfesta skal stöðu Innflutnings kreditbréfs
1. Fara til **Handbært fé og bankastjórnun > Lánsfjárbréf > Innflutningsbréf og innheimta innflutnings**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Sannprófa innflutt bréf stöðu lánsfés     
4. Lokið síðunni.
5. Lokið síðunni.

## <a name="post-purchase-invoice"></a>Bóka innkaupareikninga
1. Fara til **Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir**.
    * Velja innkaupapöntun sem var stofnuð með kreditbréfs.  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í aðgerðasvæðinu smellirðu á **Reikningur.**
5. Smelltu á **Reikningur**.
6. Í reitinn **Númer** skal slá inn gildi.
7. Í **Sendingarnúmer** reit, sláðu inn eða veldu gildi.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í retinum **Reikningsdagsetning** slærðu inn dagsetningu.
10. Smelltu á **Uppfæra samsvörunarstöðu**.
11. Smelltu á **Bóka**.
12. Lokið síðunni.
13. Lokið síðunni.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>Staðfesta stöðu og prentun á innfluttri bankaábyrgð

1. Fara til **Handbært fé og bankastjórnun > Lánsfjárbréf > Innflutningsbréf og innheimta innflutnings**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Staðfesta Innflutning kreditbréfs credit2.  
    * Staðfesta: **Sendingarstaða** = **Reikningsfært** Upplýsingar um bankaaðstöðu  
4. Smellur **Útsýni**.
5. Smellur **Prenta forrit**.
6. Smellt er á **OK**.
    * Staðfesta jöfnun kreditbréf er prentuð.  
7. Lokið síðunni.
8. Lokið síðunni.
9. Lokið síðunni.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Bóka greiðslubók Lánardrottins fyrir reikninga innkaupapantana sem stofnaðar með kreditbréfs
1. Fara í **Viðskiptaskuldir > Greiðslur > Greiðslubók**.
2. Smellt er á **Nýtt**.
3. Sláið inn eða veldu gildi í reitnum **Heiti**.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á **Línur**.
6. í retinum **Dagsetning** ritarðu dagsetningu.
7. Í reitnum **Lykill** tilgreinirðu þau gildi sem óskað er eftir.
8. Smellur **Gera upp viðskipti**.
9. Stækka Samtals hluti.
10. Í **Sýna** reit, veldu valkost.
    * Staðfestu að **Númer bankaskjals** og **Sendingarnúmer** reitirnir hafa verið uppfærðir.  
11. Veldu gátreitinn **Merkja**.
12. Smellt er á **OK**.
13. Smellið á flipann Greiðslu.
    * Staðfestu að **Númer bankaskjals** og **Sendingarnúmer** reitirnir hafa verið uppfærðir.  
14. Smelltu á **Bóka**.
15. Lokið síðunni.
16. Lokið síðunni.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Staðfesta skal stöðu Innflutnings kreditbréfs eftir að Reikningur greiddur
1. Fara til **Handbært fé og bankastjórnun > Lánsfjárbréf > Innflutningsbréf og innheimta innflutnings**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Sannprófa innflutt bréf stöðu lánsfés   
4. Lokið síðunni.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Staðfesta aðstöðumörk banka og nýtingarskýrslu
1. Fara til **Handbært fé og bankastjórnun > Fyrirspurnir og skýrslur > Greiðslubréf eða ábyrgðarskýrsla > Skýrsla bankafyrirgreiðslu og nýtingar**.
2. Útvíkka Færslur til að taka hluta.
3. Smella á **Sía**.
    * Skilgreindu **Viðmið** reit með tilskildum bankareikningi.  
4. Í reitinn **Skilyrði** skal slá inn eða velja gildi.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellt er á **OK**.
7. Smellt er á **OK**.
    * Staðfesta skýrsluna sem sýnir færslur.  
    * Staðfesta skýrslunni inniheldur færslur með númer bankaskjals, aðstöðuhámark, nýttar upphæð og stöðuupphæð aðstöðu.  
8. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
