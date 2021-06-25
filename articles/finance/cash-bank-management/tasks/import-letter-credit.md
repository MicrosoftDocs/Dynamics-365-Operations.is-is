---
title: Flytja inn kreditbréf
description: Þetta ferli fer í gegnum ferlið fyrir innflutning á kreditbréfs.
author: kweekley
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 841b4b4bb3c2f98ac65491a21bb991945c9f4bc9
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193930"
---
# <a name="import-letter-of-credit"></a>Flytja inn kreditbréf

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir innflutning á kreditbréfs. Setja verður upp eftirfarandi áður en þessi ferli er klárað: banka aðstöðu, forstillingar bókunar , bankaaðstöðusamningnum og upplýsingar um banka lánardrottins.

Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Stofna innkaupapöntun með kreditbréfi
1. Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu lánardrottnalykill.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Útvíkka eða draga saman hlutann Almennt.
7. Sláið inn eða veldu gildi í reitnum svæði.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Sláðu inn eða veldu gildi í reitnum Vöruhús.
10. Í listanum skal smella á tengilinn í valinni línu.
11. Dagsetning er rituð í reitinn dagsetning reikningsskila.
12. Dagsetning er rituð í reitinn afhendingardagur.
    * Athugasemd: Svæðið 'Gerð bankaskjals' ætti að velja með gildinu "Kreditbréfs".  
13. Smellið á „Í lagi“.
14. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
15. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
16. Í listanum skal smella á tengilinn í valinni línu.
17. Útvíkka hlutann upplýsingar Línu.
18. Smellið á flipann Afhendingar.
19. Dagsetning er rituð í reitinn afhendingardagur.
20. Dagsetning er rituð í reitinn staðfestur afhendingardagur.
21. Færið inn númer í reitnum „Einingarverð“.
    * Skilgreina upplýsingar kreditbréfs.  
22. Í Aðgerðarrúðunni er smellt á Stjórna.
23. Smellt er á kreditbréf/innflutningssafn
24. Í svæðinu dagsetningu beitingar, færið inn dagsetningu og tíma.
    * Staðfesta að svæðið ' bankareikningur' hefur sjálfgefin virkan bankareikninginn, sem er byggð á dagsetningu forrits.  
25. Færa inn gildi í reitnum númer bankaskjals.
26. Í svæðið móttökudagsetning, færa inn dagsetningu og tíma.
27. Útvíkka hlutann Bankaskjal.
28. Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.
29. Útvíkka hlutann bankaupplýsingar.
30. Sláið inn eða veldu gildi í reitnum banki sem veitir ráðgjöf.
31. Í listanum skal smella á tengilinn í valinni línu.
32. Smellið á „Vista“.
33. Smellt er á Sækja sending innkaupapöntunar.
34. Lokið síðunni.
35. Smellið á „Innkaup“ á aðgerðarúðunni.
36. Smellið á „Staðfesta“.
37. Í Aðgerðarrúðunni er smellt á Stjórna.
38. Smellt er á kreditbréf/innflutningssafn
39. Smellið á Vinnslu.
40. Smellið á „Staðfesta“.
    * Staðfesta aðstöðustaða minnkar upphæð innkaupapöntunar.  Í þessu dæmi Innkaupaupphæð = 500,00, aðstöðuhámark = 10000.00, því aðstöðustaða = 9500.00.  
41. Lokið síðunni.
42. Færið inn númer í reitnum „Einingarverð“.
43. Smellið á „Vista“.
44. Smellið á „Innkaup“ á aðgerðarúðunni.
45. Smellið á „Staðfesta“.
    * Lagfæra kreditbréf, vegna breytinga í einingaverði.  
46. Í Aðgerðarrúðunni er smellt á Stjórna.
47. Smellt er á kreditbréf/innflutningssafn
    * Lagfæra kreditbréf, vegna breytinga á einingarverð Innkaupapöntunar.  
48. Smellið á Vinnslu.
49. Smellt er á Lagfæra.
50. Smella á Fjarlægja.
51. Smella á Já.
52. Smellt er á Sækja sending innkaupapöntunar.
53. Smellið á Vinnslu.
54. Smellið á „Staðfesta“.
    * Staðfesta aðstöðustaða minnkar upphæð innkaupapöntunar.  Í þessu dæmi er hægt að breyta upphæð Innkaupa = 600,00, aðstöðuhámark = 10000.00, því aðstöðustaða = 9400.00.  
55. Lokið síðunni.

## <a name="post-packing-slip"></a>Bóka fylgiseðil
1. Smellið á „Móttaka“ á aðgerðarúðunni.
2. Smellið á „Innhreyfingarskjal“.
3. Í reitinn PurchParmTable_Num skal slá inn gildi.
    * Veljið númer Sendingar stofnaðar með tilvísan í kreditbréfi.  
4. Í listanum skal smella á tengilinn í valinni línu.
5. Færa inn dagsetningu í reitnum móttökudagsetning afurðar.
6. Smellið á „Í lagi“.
7. Lokið síðunni.
8. Lokið síðunni.

## <a name="verify-import-letter-of-credit-status"></a>Staðfesta skal stöðu Innflutnings kreditbréfs
1. Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja inn kreditbréf og innflutningssafn.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Sannprófa innflutt bréf stöðu lánsfés     
4. Lokið síðunni.
5. Lokið síðunni.

## <a name="post-purchase-invoice"></a>Bóka innkaupareikninga
1. Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.
    * Velja innkaupapöntun sem var stofnuð með kreditbréfs.  
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smellið á „Reikningur“ á aðgerðarúðunni.
5. Smellt er á Reikningnum.
6. Í reitnum Númer skal slá inn gildi.
7. Í reitinn sendingarnúmer skal slá inn eða velja gildi.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Færið inn dagsetningu á svæðinu „Reikningsdagsetning“.
10. Smellið á „Uppfæra samsvörunarstöðu“.
11. Smellið á „Bóka“.
12. Lokið síðunni.
13. Lokið síðunni.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>Staðfesta stöðu og prentun á innfluttri bankaábyrgð

1. Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja inn kreditbréf og innflutningssafn.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Staðfesta Innflutning kreditbréfs credit2.  
    * Villuleita: Sendingarstaða = Reikningsfært upplýsingar um bankaaðstaða  
4. Smellið á Skoða.
5. Smellt er á Prenta umsókn.
6. Smellið á „Í lagi“.
    * Staðfesta jöfnun kreditbréf er prentuð.  
7. Lokið síðunni.
8. Lokið síðunni.
9. Lokið síðunni.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Bóka greiðslubók Lánardrottins fyrir reikninga innkaupapantana sem stofnaðar með kreditbréfs
1. Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
3. Sláið inn eða veldu gildi í reitnum heiti.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á Línur.
6. Dagsetning er rituð í reitinn Dagetning.
7. Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.
8. Smellt er á Gera upp færslur.
9. Stækka Samtals hluti.
10. Í reitnum Sýna skal velja valkost.
    * Staðfesta að númer bankaskjals og svæði sendingarnúmers hafa verið uppfærðar.  
11. Veldu gátreitinn Merkja.
12. Smellið á „Í lagi“.
13. Smellið á flipann Greiðslu.
    * Staðfesta að númer bankaskjals og svæði sendingarnúmers hafa verið uppfærðar.  
14. Smellið á „Bóka“.
15. Lokið síðunni.
16. Lokið síðunni.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Staðfesta skal stöðu Innflutnings kreditbréfs eftir að Reikningur greiddur
1. Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja inn kreditbréf og innflutningssafn.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Sannprófa innflutt bréf stöðu lánsfés   
4. Lokið síðunni.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Staðfesta aðstöðumörk banka og nýtingarskýrslu
1. Fara í Reiðufé og bankakerfi > Fyrirspurnir og skýrslur > Kreditbréf eða ábyrgðarbréf > Bankaaðgerðir og skýrsla um nýtingu.
2. Útvíkka Færslur til að taka hluta.
3. Smellt er á Síu.
    * Skilgreina svæðið Skilyrði með bankareikning sem þarf.  
4. Í reitinn Skilyrði skal slá inn eða veldu gildi.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á „Í lagi“.
7. Smellið á „Í lagi“.
    * Staðfesta skýrsluna sem sýnir færslur.  
    * Staðfesta skýrslunni inniheldur færslur með númer bankaskjals, aðstöðuhámark, nýttar upphæð og stöðuupphæð aðstöðu.  
8. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]