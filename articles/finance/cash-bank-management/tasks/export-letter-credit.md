---
title: Flytja út kreditbréf
description: Þetta ferli fer í gegnum ferlið fyrir Útflutning kreditbréfs.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779555"
---
# <a name="export-letter-of-credit"></a>Flytja út kreditbréf

[!include [banner](../../includes/banner.md)]

Þetta ferli fer í gegnum ferlið fyrir Útflutning kreditbréfs.

Skjalaupplýsingar um kreditbréf er samning sem er gefið út af banka, sem bankinn samþykkir til að tryggja að greiðslur fyrir hönd kaupanda, ef skilmálum samningsins milli seljanda og kaupanda eru uppfyllt.



Keyra á **Settu upp bankaaðstöðu og færslusnið** málsmeðferð og **Lánabréf_Búa til bankafyrirgreiðslusamning** málsmeðferð fyrir þessa málsmeðferð. Verður að velja fyrirtæki USMF sýnigögn til að keyra þetta ferli til enda.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Stofna sölupöntun fyrir Flytja út kreditbréf
1. Fara til **Viðskiptakröfur > Pantanir > Allar sölupantanir**.
2. Smellt er á **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Stækkaðu eða felldu niður **Almennt** kafla.
7. Í reitnum **Svæði** skal smella á fellilistahnappinn til að opna leitina.
    * Veldu **Síða** þar sem hluturinn sem á að gefa út er á lager.  
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í reitnum **Vöruhús** skal smella á fellilistahnappinn til að opna leitina.
    * Veldu **Vöruhús** þar sem vara sem á að gefa út er á lager.  
10. Í listanum skal smella á tengilinn í valinni línu.
    * Athugið: The **Tegund bankaskjals** reit ætti að vera valið með **Bankaábyrgð**.  
11. Í **Tegund bankaskjals** reit, veldu **Bankaábyrgð**.
12. Stækkaðu eða felldu niður **Afhending** kafla.
    * Veldu **Stýring á afhendingardagsetningu** = **Enginn**.  
13. Í **Umbeðin móttökudagsetning** reit, sláðu inn dagsetningu.
14. Smellt er á **OK**.
15. Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.
    * Veljið vöruna sem þarf að vera Útgefið/Selt.  
16. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum **Einingarverð** skal slá inn tölu.
19. Útvíkkaðu eða dragðu saman hlutann **Línuupplýsingar**.
20. Smelltu á **Afhending** flipa.
21. Í **Umbeðinn sendingardagur** reit, sláðu inn dagsetningu.
22. Í **Staðfest sendingardagsetning** reit, sláðu inn dagsetningu.
23. Smelltu á aðgerðarrúðuna **Stjórna**.
24. Smellur **Bankaábyrgð**.
25. Í **Númer bankaskjals** reit, sláðu inn gildi.
26. Í **Gildistími** reit, sláðu inn dagsetningu og tíma.
27. Stækkaðu eða felldu niður **bankaupplýsingar** kafla.
28. Í **Útgefandi banki** reit, smelltu á fellilistann til að opna leitina.
29. Í listanum skal smella á tengilinn í valinni línu.
30. Í **Ráðgjafarbanki** reit, smelltu á fellilistann til að opna leitina.
31. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
32. Í listanum skal smella á tengilinn í valinni línu.
33. Smellur **Sækja sölupöntunarsendingar**.
34. Smellur **Gefa út bankaskjal**.
35. Lokið síðunni.

## <a name="post-packing-slip"></a>Bóka fylgiseðil
1. Á aðgerðasvæðinu er smellt á **Taka til og pakka**.
2. Smellur **Póstu fylgiseðill**.
3. Útvíkka eða draga saman hlutann **Færibreytur**.
4. Í reitnum **Magn** velurðu **Allt**.
5. Stækkaðu eða felldu niður **Uppsetning** kafla.
6. Í **Dagsetning fylgiseðils** reit, sláðu inn dagsetningu.
7. Veljið númer fyrir Sendingu.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Smellt er á **OK**.
10. Smellt er á **OK**.

## <a name="post-sales-invoice"></a>Bókar sölureikninga.
1. Í aðgerðasvæðinu smellirðu á **Reikningur.**
2. Smelltu á **Reikningur**.
3. Stækkaðu eða felldu niður **Yfirlit** kafla.
4. Veldu **Sendingarnúmer**.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Stækkaðu eða felldu niður **Uppsetning** kafla.
7. Í retinum **Reikningsdagsetning** slærðu inn dagsetningu.
8. Smellt er á **OK**.
9. Smellt er á **OK**.

## <a name="shipment-document-submitted-status"></a>Staða fyrir sent Flutningsskjal
1. Smelltu á aðgerðarrúðuna **Stjórna**.
2. Smellur **Bankaábyrgð**.
3. Stækkaðu eða felldu niður **Línur** kafla.
    * Athugið: The **Skjal lagt fram** reit ætti að vera stillt á **Já**.  

## <a name="verify-export-letter-of-credit"></a>Sannprófa flytja út kreditbréf
1. Fara til **Handbært fé og bankastjórnun > Lánsfjárbréf > Útflutningslán og innheimta innflutnings**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Staðfestu að **Útflutningsbréf** á **Sendingarstaða** af **Reikningsfært**.  

## <a name="customer-payment"></a>Greiðsla viðskiptavinar
1. Fara til **Viðskiptakröfur > Greiðslur > Greiðsludagbók**.
2. Smellt er á **Nýtt**.
3. Í listanum skal merkja valda línu.
4. Í reitnum **Heiti** skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal smella á tengilinn í valinni línu.
6. Smellið á **Línur**.
7. í retinum **Dagsetning** ritarðu dagsetningu.
8. Í reitnum **Lykill** tilgreinirðu þau gildi sem óskað er eftir.
9. Smellur **Uppgjör**.
10. Velja skal gátreitinn í hausnum fyrir samtala.
    * Athugið: Stilltu **Sýna** sviði til **Bankaábyrgð**.  
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Veldu eða hreinsaðu **Mark** gátreit.
13. Smellt er á **OK**.
14. Smelltu á **Greiðsla** flipa.
    * Staðfestu upplýsingar um bankaskjalsnúmer og sendingarnúmer  
15. Smelltu á **Bóka**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Staðfesta flytja út kreditbréf eftir greiðslu
1. Fara til **Handbært fé og bankastjórnun > Lánsfjárbréf > Útflutningslán og innheimta innflutnings**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Staðfestu að **Sendingarstaða** = **Greiðsla móttekin** og **Staða upphæð** = **0,00**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
