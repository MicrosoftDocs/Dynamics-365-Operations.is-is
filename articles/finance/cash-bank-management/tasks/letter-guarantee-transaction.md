---
title: Færsla ábyrgðarbréfs
description: Þetta ferli fer í gegnum Fyrir ferli ábyrgðarbréfs.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e025f0d0a89eb6c6ab024236400a7c65b108e6d5
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722747"
---
# <a name="letter-of-guarantee-transaction"></a>Færsla ábyrgðarbréfs

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum Fyrir ferli ábyrgðarbréfs.



Ljúka þarf eftirfarandi verkum áður en þessu ferli er lokið:

- Setja upp bankaaðstöðu og bókunarreglur fyrir ábyrgðaryfirlýsingu.

- Stofna bankaaðstöðusamningn fyrir kreditbréf.



Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Stofna Sölupöntun með Ábyrgðarbréf
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
4. Útvíkka eða draga saman hlutann Almennt.
5. Sláið inn eða veldu gildi í reitnum svæði.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Sláðu inn eða veldu gildi í reitnum Vöruhús.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í gerð bankaskjals svæðinu, veljið 'Ábyrgðarbréf'.
10. Smellt er á Í lagi.
11. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
12. Færið inn númer í reitnum „Einingarverð“.
13. Víkkið út hlutann „Upplýsingar um línu“.
14. Smellið á flipann „Afhending“.
    * Athugasemd: Velja stýringu Afhendingardagsetningar = Ekkert  
15. Færa inn dagsetningu í reitnum Umbeðinni sendingardagsetningu .
16. Færa inn dagsetningu í reitnum staðfest sendingardagsetning

## <a name="process-letter-of-guarantee_request"></a>Ferli ábyrgðaryfirlýsing_beiðni
1. Í Aðgerðarrúðunni er smellt á Stjórna.
2. Smellt er á Ábyrgðaryfirlýsingar.
3. Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.
4. Smelltu á Beiðni til að opna felligluggann.
5. Færa inn eða veljið gildi í svæðinu gerð.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitinn Gildi skal slá inn númer.
8. Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.
9. Smellið á „Í lagi“.
10. Lokið síðunni.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Ferli ábyrgðaryfirlýsing_senda í banka
1. Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Smellt er á Senda til banka til að opna felligluggi.
4. Færa inn eða veljið gildi í svæðinu bankareikning.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á „Í lagi“.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Ferli ábyrgðaryfirlýsing_móttekið frá banka
1. Smellt er á Móttekið frá banka til að opna felligluggi
2. Færa inn gildi í reitnum númer banka.
    * Staðfestið gildin í reiknuðum svæðum Framlegð og Kostnað.  
3. Smellið á „Í lagi“.
4. Stækka aðgerðasvæðið.
    * Staðfesta færslu 'Móttekið frá banka'.  
5. Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.
6. Smellið á „Línur“.
    * Staðfestið bókun á færslum færslubókar.  
7. Lokið síðunni.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Ferli Ábyrgðaryfirlýsingar_veita til rétthafi
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Í Aðgerðarrúðunni er smellt á Stjórna.
4. Smellt er á Ábyrgðaryfirlýsingar.
5. Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.
6. Smellt er á Veita rétthafa til að opna felligluggi.
7. Smellið á „Í lagi“.
8. Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellt er á Veita rétthafa til að opna felligluggi.
11. Smellið á „Í lagi“.
12. Stækka aðgerðasvæðið.
    * Villuleita "Gefa rétthafa" færslu.  

## <a name="process-letter-of-guarantee_increase-value"></a>Ferli ábyrgðaryfirlýsing_auka gildi
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Í Aðgerðarrúðunni er smellt á Stjórna.
4. Smellt er á Ábyrgðaryfirlýsingar.
5. Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.
6. Smellt er á auka gildi til að opna felligluggann.
7. Færið inn númer í Gildi til að bæta við svæði.
8. Smellið á „Í lagi“.
9. Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.
10. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
11. Smellt er á auka gildi til að opna felligluggann.
12. Smellið á „Í lagi“.
13. Stækka aðgerðasvæðið.
    * Staðfesta færslu 'Auka gildi'.  
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.
16. Smellið á „Línur“.
    * Staðfesta bókaðar færslur færslubókar.  

## <a name="process-letter-of-guarantee_liquidate"></a>Ferli ábyrgðaryfirlýsing_eyða
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Í Aðgerðarrúðunni er smellt á Stjórna.
4. Smellt er á Ábyrgðaryfirlýsingar.
5. Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.
6. Smellt er á eyða til að opna felligluggann.
7. Smellið á „Í lagi“.
8. Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellt er á eyða til að opna felligluggann.
11. Smellið á „Í lagi“.
12. Stækka aðgerðasvæðið.
    * Staðfesta „eyða" færslu.  
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.
15. Smellið á „Línur“.
    * Staðfesta bókaðar færslur færslubókar.  
16. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
