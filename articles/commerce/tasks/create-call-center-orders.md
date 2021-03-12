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
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964846"
---
# <a name="create-call-center-orders"></a> Stofna pantanir fyrir símaver

[!include [banner](../includes/banner.md)]

Þetta ferli fer í gegnum hvernig er flett upp viðskiptavinur, ný pöntun er stofnuð, leita að afurð og innheimta greiðslu frá viðskiptavini. Þessi aðferð notar sýnigögn fyrirtækis USRT og er ætlaður fyrir Afgreiðslumaður sölupöntunar. Frumskilyrði: Notandinn sem klárar ferlið er settur upp sem notandi símavers og Fabrikam hálfsárs Vörulisti er birt með minnst einn frumkóða á honum.

1. Fárið í **Smásala og viðskipti \> Viðskiptavinir \> Þjónusta við viðskiptavini**.
2. Færa inn leitarskilyrði til að fletta upp viðskiptavinar í svæðinu **SearchText.**
    * Til að fá þetta dæmi skal slá inn „Karen“ og velja **Tab**.  
3. Velja Leita.
    * Þar sem það er aðeins einn viðskiptavinur með heitinu Karen í sýnigögn verður hann sjálfvirkt valinn.  
4. Veldu **Ný sölupöntun**.
5. Útvíkka eða draga saman haushlutann **sölupöntun**.
6. Veljið frumkóða fyrir vörulistann.
    * Ef engin virkir frumkóðar eru til staðar er hægt að sleppa þessu þrepi.  
7. Veldu **Bæta við línu**.
8. Færið inn leitarorð í svæðið **Númer vöru**.
    * Fyrir Þetta sýnishorn ferlis að færa inn hluta vörunúmer '8111' og styðjið á flipanum. Þá birtist leitarglugginn.  
9. Velja afurðar til að bæta við sölupöntun.
10. Færið inn sölumagn
11. Velja **Stofna**.
12. Veljið **Ljúka** til að fanga greiðslu viðskiptavinar.
13. Veljið **Bæta við**.
    * Bæta Við tengli er í flipanum Greiðslur. Útvíkka flipanum Greiðslur ef hún er dregin saman.  
14. Veldu greiðslumáti
    * Veljið greiðslumáta reiðufjár fyrir þetta ferli.  
15. Lokið síðunni.
16. Færa skal inn upphæðina.
    * Fyrir þetta ferli skal færa upphæð jafnt og stöðu pöntunar sem hægt er að sjá í samantekt sölupöntunar síðunni vinstra megin við svæðið upphæð. Þessi aðgerð leyfir notandanum að ljúka pöntun sem að fullu greitt.  
17. Veljið **Í lagi**.
18. Veldu **Senda**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Sérstilla tölvupósta vegna færslna eftir afhendingarmáta](../customize-email-delivery-mode.md)

[Breyta afhendingarmáta á sölustað](../pos-change-delivery-mode.md)

