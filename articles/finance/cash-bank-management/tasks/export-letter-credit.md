---
title: Flytja út kreditbréf
description: Þetta ferli fer í gegnum ferlið fyrir Útflutning kreditbréfs.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cd18320ca8505b1357ce505dfb4c94e81aaae91
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444342"
---
# <a name="export-letter-of-credit"></a>Flytja út kreditbréf

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir Útflutning kreditbréfs.

Skjalaupplýsingar um kreditbréf er samning sem er gefið út af banka, sem bankinn samþykkir til að tryggja að greiðslur fyrir hönd kaupanda, ef skilmálum samningsins milli seljanda og kaupanda eru uppfyllt.



Keyra ferli 'Setja upp bankaaðgerðir og bókunarreglur' og ‚kreditbréf_Stofna bankaaðstöðusamningur' aðferð fyrir þetta ferli. Verður að velja fyrirtæki USMF sýnigögn til að keyra þetta ferli til enda.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Stofna sölupöntun fyrir Flytja út kreditbréf
1. Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.
2. Smellið á „Nýtt“.
3. Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Útvíkka eða draga saman hlutann Almennt.
7. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
    * Velja Svæðið þar sem varan á að gefa út er í birgðum.  
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
    * Veljið Vöruhús þar sem varan á að gefa út er í birgðum.  
10. Í listanum skal smella á tengilinn í valinni línu.
    * Athugasemd: Svæðið "Gerð bankaskjals" ætti að velja með gildinu "Kreditbréfs".  
11. Í gerð bankaskjals svæðinu, veljið "Kreditbréfs".
12. Stækka eða fella saman hlutann Afhending.
    * Veljið stýringu Afhendingardagsetningar = Ekkert.  
13. Færa inn dagsetningu í reitnum umbeðin móttökudagsetning
14. Smellið á „Í lagi“.
15. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
    * Veljið vöruna sem þarf að vera Útgefið/Selt.  
16. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum Einingarverð skal slá inn tölu.
19. Útvíkka eða draga saman hluta upplýsingar Línu.
20. Smellið á flipann Afhendingar.
21. Færa inn dagsetningu í reitnum Umbeðinni sendingardagsetningu .
22. Færa inn dagsetningu í reitnum staðfest sendingardagsetning
23. Í Aðgerðarrúðunni er smellt á Stjórna.
24. Smellt er á kreditbréf
25. Færa inn gildi í reitnum númer bankaskjals.
26. Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.
27. Útvíkka eða draga saman hlutanum bankaupplýsingar.
28. Í reitnum Útgáfubanki skal smella á fellilistahnappinn til að opna leitina.
29. Í listanum skal smella á tengilinn í valinni línu.
30. Í reitnum banki sem veitir ráðgjöf skal smella á fellilistahnappinn til að opna leitina.
31. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
32. Í listanum skal smella á tengilinn í valinni línu.
33. Smellt er á Sækja sending sölupöntunar.
34. Smelltu á gefa út bankaskjal
35. Lokið síðunni.

## <a name="post-packing-slip"></a>Bóka fylgiseðil
1. Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.
2. Smellið á „Bóka fylgiseðil“.
3. Útvíkka eða draga saman hlutann Færibreytur.
4. Í svæðinu magn, veljið 'Allt'.
5. Útvíkka eða draga saman hlutann Setja upp.
6. Færa inn dagsetningu í reitnum dagsetning fylgiseðils.
7. Veljið númer fyrir Sendingu.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Smellið á „Í lagi“.
10. Smellið á „Í lagi“.

## <a name="post-sales-invoice"></a>Bókar sölureikninga.
1. Smellið á „Reikningur“ á aðgerðarúðunni.
2. Smellið á „Reikningur“.
3. Útvíkka eða draga saman hlutann yfirlit.
4. Veljið númer fyrir Sendingu.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Útvíkka eða draga saman hlutann Setja upp.
7. Færið inn dagsetningu á svæðinu „Reikningsdagsetning“.
8. Smellið á „Í lagi“.
9. Smellið á „Í lagi“.

## <a name="shipment-document-submitted-status"></a>Staða fyrir sent Flutningsskjal
1. Í Aðgerðarrúðunni er smellt á Stjórna.
2. Smellt er á kreditbréf
3. Útvíkka eða draga saman hlutann línur.
    * Athugasemd: Svæðið 'Skjal er sent' ætti að stilla 'Já'.  

## <a name="verify-export-letter-of-credit"></a>Sannprófa flytja út kreditbréf
1. Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja út kreditbréf og innflutningssafn.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Staðfestið að ábyrgðarbréf útflutnings hefur sendingarstaða 'Reikningsfært'.  

## <a name="customer-payment"></a>Greiðsla viðskiptavinar
1. Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.
2. Smellið á „Nýtt“.
3. Í listanum skal merkja valda línu.
4. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á Línur.
7. Dagsetning er rituð í reitinn Dagetning.
8. Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.
9. Smellt er á Jöfnun.
10. Velja skal gátreitinn í hausnum fyrir samtala.
    * Athugasemd: Stilla svæðið Sýna á "Kreditbréfs" .  
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Veldu eða hreinsaðu gátreitinn Merkið við.
13. Smellið á „Í lagi“.
14. Smellið á flipann Greiðslu.
    * Staðfesta númer bankaskjals og upplýsingar sendingarnúmers  
15. Smellið á „Bóka“.

## <a name="verify-export-letter-of-credit-after-payment"></a>Staðfesta flytja út kreditbréf eftir greiðslu
1. Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja út kreditbréf og innflutningssafn.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Staðfesta sendingarstaða = Greiðsla móttekin og staða upphæð = 0,00.  

