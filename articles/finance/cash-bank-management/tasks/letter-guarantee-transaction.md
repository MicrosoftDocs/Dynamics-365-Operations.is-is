---
title: Færsla ábyrgðarbréfs
description: Þetta ferli fer í gegnum Fyrir ferli ábyrgðarbréfs.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30e21c11b067f6def127f3eab026d7255ab1ca29
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779935"
---
# <a name="letter-of-guarantee-transaction"></a>Færsla ábyrgðarbréfs

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum Fyrir ferli ábyrgðarbréfs.



Ljúka þarf eftirfarandi verkum áður en þessu ferli er lokið:

- Setja upp bankaaðstöðu og bókunarreglur fyrir ábyrgðaryfirlýsingu.

- Stofna bankaaðstöðusamningn fyrir kreditbréf.



Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Stofna Sölupöntun með Ábyrgðarbréf
1. Fara til **Viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** skal færa inn eða velja gildi.
4. Útvíkka eða draga saman hlutann Almennt.
5. Í reitnum **Svæði** slærðu inn eða velur gildi.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitnum **Vöruhús** slærðu inn eða velur gildi.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í **Tegund bankaskjals** reit, veldu **Ábyrgðarbréf**.
10. Smellt er á **OK**.
11. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
12. Í reitnum **Einingarverð** skal slá inn tölu.
13. Víkkið út hlutann „Upplýsingar um línu“.
14. Smellið á flipann „Afhending“.
    * Athugasemd: Velja stýringu Afhendingardagsetningar = Ekkert  
15. Í **Umbeðinn sendingardagur** reit, sláðu inn dagsetningu.
16. Í **Staðfest sendingardagsetning** reit, sláðu inn dagsetningu.

## <a name="process-letter-of-guarantee_request"></a>Ferli ábyrgðaryfirlýsing_beiðni
1. Smelltu á aðgerðarrúðuna **Stjórna**.
2. Smellur **Ábyrgðarbréf**.
3. Smelltu á aðgerðarrúðuna **Ábyrgðarbréf**.
4. Smellur **Beiðni** til að opna fallgluggann.
5. Í **Tegund** reit, sláðu inn eða veldu gildi.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitnum **Gildi** skal slá inn númer.
8. Í **Gildistími** reit, sláðu inn dagsetningu og tíma.
9. Smellt er á **OK**.
10. Lokið síðunni.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Ferli ábyrgðaryfirlýsing_senda í banka
1. Fara til **Handbært fé og bankastjórnun > Ábyrgðarbréf > Ábyrgðarbréf**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Smellur **Sendu í banka** til að opna fallgluggann.
4. Færa inn eða veljið gildi í svæðinu **Bankareikningur**.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellt er á **OK**.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Ferli ábyrgðaryfirlýsing_móttekið frá banka
1. Smellur **Tekið á móti frá banka** til að opna fallgluggann.
2. Í **Bankanúmer** reit, sláðu inn gildi.
    * Staðfestu gildin í útreiknuðu **Framlegð** og **Kostnaður** sviðum.  
3. Smellt er á **OK**.
4. Stækka aðgerðasvæðið.
    * Staðfesta færslu 'Móttekið frá banka'.  
5. Smelltu til að fylgja hlekknum í **Lotunúmer dagbókar** sviði.
6. Smellið á **Línur**.
    * Staðfestið bókun á færslum færslubókar.  
7. Lokið síðunni.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Ferli Ábyrgðaryfirlýsingar_veita til rétthafi
1. Fara til **Viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Smelltu á aðgerðarrúðuna **Stjórna**.
4. Smellur **Ábyrgðarbréf**.
5. Smelltu á aðgerðarrúðuna **Ábyrgðarbréf**.
6. Smellur **Gefðu styrkþega** til að opna fallgluggann.
7. Smellt er á **OK**.
8. Fara til **Handbært fé og bankastjórnun > Ábyrgðarbréf > Ábyrgðarbréf**.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellur **Gefðu styrkþega** til að opna fallgluggann.
11. Smellt er á **OK**.
12. Stækka aðgerðasvæðið.
    * Villuleita "Gefa rétthafa" færslu.  

## <a name="process-letter-of-guarantee_increase-value"></a>Ferli ábyrgðaryfirlýsing_auka gildi
1. Fara til **Viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Smelltu á aðgerðarrúðuna **Stjórna**.
4. Smellur **Ábyrgðarbréf**.
5. Smelltu á aðgerðarrúðuna **Ábyrgðarbréf**.
6. Smellur **Auka verðmæti** til að opna fallgluggann.
7. Í **Gildi til að auka** reit, sláðu inn númer.
8. Smellt er á **OK**.
9. Fara til **Handbært fé og bankastjórnun > Ábyrgðarbréf > Ábyrgðarbréf**.
10. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
11. Smellur **Auka verðmæti** til að opna fallgluggann.
12. Smellt er á **OK**.
13. Stækka aðgerðasvæðið.
    * Staðfesta færslu 'Auka gildi'.  
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Smelltu til að fylgja hlekknum í **Lotunúmer dagbókar** sviði.
16. Smellið á **Línur**.
    * Staðfesta bókaðar færslur færslubókar.  

## <a name="process-letter-of-guarantee_liquidate"></a>Ferli ábyrgðaryfirlýsing_eyða
1. Fara til **Viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Smelltu á aðgerðarrúðuna **Stjórna**.
4. Smellur **Ábyrgðarbréf**.
5. Smelltu á aðgerðarrúðuna **Ábyrgðarbréf**.
6. Smellur **Gjaldtaka** til að opna fallgluggann.
7. Smellt er á **OK**.
8. Fara til **Handbært fé og bankastjórnun > Ábyrgðarbréf > Ábyrgðarbréf**.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellur **Gjaldtaka** til að opna fallgluggann.
11. Smellt er á **OK**.
12. Stækka aðgerðasvæðið.
    * Staðfesta „eyða" færslu.  
13. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
14. Smelltu til að fylgja hlekknum í **Lotunúmer dagbókar** sviði.
15. Smellið á **Línur**.
    * Staðfesta bókaðar færslur færslubókar.  
16. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
