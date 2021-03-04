---
title: Skrá söluþóknun
description: Þetta efni útskýrir hvernig söluumboð eru reiknuð og skráð.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57e3b95cb1f4a13b49ddcd336efaeabb12e5defc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430160"
---
# <a name="register-sales-commissions"></a>Skrá söluþóknun

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig söluumboð eru reiknuð og skráð. Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum. Áður en þessari handbók er ræst þarf að keyra leiðbeiningar sem kallast "Setja upp reglur um söluþóknun" til að tryggja að allar nauðsynlegar uppsetningar á útreikningi sölulauna séu til staðar.

Athugið þær tölur viðskiptavina og vara sem voru valdar fyrir sölulaunaferlið og notið þær þegar beðið er um að stofna sölupöntun í þessari handbók.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Reikningsfæra sölupöntun sem uppfyllir skilyrði sölumanns fyrir þóknun
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.
2. Veljið **Nýtt**.
3. Í reitnum **Viðskiptavinalykill** velurðu skrána sem óskað er eftir af fellivalmyndinni.
4. Veljið **Í lagi**.
5. Í aðgerðasvæðinu velurðu **Valkostir**.
6. Veldu **Breyta skjámynd**.
7. Veldu **Hausyfirlit**.
8. Útvíkkaðu kaflann **Uppsetning**.

    - Gildið í reitnum **Söluflokkur** stendur fyrir flokk sem hefur fengið einum eða fleiri sölumönnum úthlutað. Fólk innan flokksins eru þau sem fá sölulaun þegar pöntunin er reikningsfærð, samkvæmt fyrirframskilgreindum taxta og dreifingu.   
    - Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.  
    - Söluflokkurinn er einnig afritaður í sölupöntunarlínu. Hægt er að breyta þannig að hún sé önnur en sú sem er í haus og/eða á milli lína.  
    - Gildið í svæðinu **Sölulaunaflokkur** stendur fyrir flokk sem var stofnaður fyrir einn eða fleiri viðskiptavini vegna rakningar á sölulaunum.   
    - Gildi er afritað af viðskiptavinakortinu en hægt er að breyta því ef óskað er.   

9. Í aðgerðasvæðinu velurðu **Valkostir**.
10. Veldu **Breyta skjámynd**.
11. Veldu **Línusýn**.
12. Í fellivalmyndinni í reitnum **Vörunúmer** skaltu velja vöruna sem þú hefur sett upp fyrir þóknun. 
13. Í reitnum **Magn** slærðu inn tölu. Athugið nettóupphæð línunnar. Hún stendur fyrir sölutekjur sem í þessu dæmi eru grunnurinn fyrir útreikning þóknunar.  
14. Veljið **Vista**.
15. Í aðgerðasvæðinu velurðu **Reikning**.
16. Veldu **Reikning**.
17. Útvíkkaðu hlutann **Færibreytur**.
18. Í reitnum **Magn** velurðu **Allt**.
19. Veldu **Já** í reitnum **Bókun**.
20. Veldu **Í lagi**, veldu síðan **Í lagi** í næsta glugga. Það gæti tekið um það bil mínútu að bóka færsluna. Heimila vinnslu að ljúka og ekki loka síðunni.  

## <a name="review-the-registered-sales-commissions"></a>Fara yfir skráðar söluþóknanir
1. Á aðgerðarúðunni skal velja **Reikning** og svo **Reikning** aftur.
2. Á aðgerðarúðunni skal velja **Reikning** og svo **Þóknunarfærslur**.

    - Flipinn **Yfirlit** birtir línur sem sýna upphæðir sölulauna sem greiða á sölufulltrúum sem eru tengdir reikningsfærðu sölupöntuninni. Endurskoðum nú upplýsingarnar.  
    - Ef handbókin "Setja upp reglur söluþóknunar" var notuð til að setja upp flokk **Sölulauna** eru tveir sölumenn til að móttaka sölulaun og sölulaununum er skipt jafnt á milli þeirra.  
    - Í þessu dæmi er heildarupphæð þóknun reiknuð sem hlutfall sölutekna (nettóupphæð pöntunarlínu).  
3. Lokið síðunni.
4. Veldu **Fylgiskjal**. Hægt er að skoða færslur fylgiskjala fyrir upphæðir sölulauna sem hafa verið bókaðar í forskilgreindu þóknunarkostnaður og þóknun lykla lánardrottna.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]