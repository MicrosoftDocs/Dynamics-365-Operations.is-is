---
title: " Stofna pantanir fyrir símaver"
description: Þetta ferli fer í gegnum hvernig er flett upp viðskiptavinur, ný pöntun er stofnuð, leita að afurð og innheimta greiðslu frá viðskiptavini.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ec10e0f79e4eca7f51ba48c679dcf6fe745eb29
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141431"
---
# <a name="create-call-center-orders"></a> Stofna pantanir fyrir símaver

[!include [banner](../includes/banner.md)]

Þetta ferli fer í gegnum hvernig er flett upp viðskiptavinur, ný pöntun er stofnuð, leita að afurð og innheimta greiðslu frá viðskiptavini. Þessi aðferð notar sýnigögn fyrirtækis USRT og er ætlaður fyrir Afgreiðslumaður sölupöntunar. Frumskilyrði: Notandinn sem klárar ferlið er settur upp sem notandi símavers og Fabrikam hálfsárs Vörulisti er birt með minnst einn frumkóða á honum.

1. Fara í Retail og Commerce > viðskiptavinur > viðskiptavinur þjónusta.
2. Færa inn leitarskilyrði til að fletta upp viðskiptavinar í svæðinu SearchText.
    * Fyrir þetta dæmi í ferlinu 'karen' og stutt er á flipann.  
3. Smellið á leita.
    * Þar sem það er aðeins einn viðskiptavin með heitinu Karen í sýnigögn þær verða sjálfvirkt valinn.  
4. Smelltu á Ný sölupöntun
5. Útvíkka eða draga saman hlutann sölupöntunarhaus.
6. Veljið frumkóða fyrir vörulistann.
    * Ef engin virk frumkóðar eru hægt að loka á upprunareit og sleppa þessu þrepi.  
7. Smellið á „Bæta við línu“.
8. Færið inn leitarorð í svæðið númer vöru.
    * Fyrir Þetta sýnishorn ferlis að færa inn hluta vörunúmer '8111' og styðjið á flipanum. Þetta mun birtast glugganum leit að vöru.  
9. Velja afurðar til að bæta við sölupöntun
10. Færið inn sölumagn
11. Smellið á Stofna.
12. Smellið á Ljúka til að fanga greiðslu viðskiptavinar.
13. Smelltu á Bæta við.
    * Bæta Við tengli er í flipanum Greiðslur. Útvíkka flipanum Greiðslur ef hún er dregin saman.  
14. Veldu greiðslumáti
    * Veljið greiðslumáta reiðufjár fyrir þetta ferli.  
15. Lokið síðunni.
16. Færa skal inn upphæðina.
    * Fyrir Þetta ferli skal færa upphæð jafnt og stöðu pöntunar sem hægt er að sjá í samantekt sölupöntunar síðunni vinstra megin við svæðið upphæð. Þetta leyfir notandanum að ljúka sem að fullu greitt.  
17. Smellið á „Í lagi“.
18. Smelltu á Senda.

