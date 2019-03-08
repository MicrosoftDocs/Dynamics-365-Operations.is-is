---
title: Setja upp greiðsluþóknanir viðskiptavina
description: Stofna greiðsluþóknanir fyrir greiðsluar viðskiptavinar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "354829"
---
# <a name="establish-customer-payment-fees"></a>Setja upp greiðsluþóknanir viðskiptavina

[!include [task guide banner](../../includes/task-guide-banner.md)]

Stofna greiðsluþóknanir fyrir greiðsluar viðskiptavinar.

Þetta verkefni notar USMF-sýnifyrirtækið.

1. Fara í Viðskiptakröfur > Uppsetningar greiðslu > Greiðsluþóknun.
2. Smellið á „Nýtt“.
3. Í svæðið Kenni Þóknunar að færa inn kenni Þóknunar.
    * Kenni Þóknunar Birtist í greiðslubókum, þannig að hafðu það lýsandi til að skilja er hvaða þóknun er metin.  
4. Færa skal inn heiti þóknunar í reitinn Heiti.
5. Færið inn lýsingu fyrir þóknun í lýsingarsvæði Þóknunar.
6. Velja hvort gjaldið verður skuldfærð á Viðskiptavin eða fjárhagslykil.
    * Ef viðskiptavinur er metin þóknun, veljið Viðskiptavinar. Ef þóknunin verður meta sem útgjöld á fyrirtækið , velja Fjárhag. Veljið Viðskiptavin fyrir þetta verk.  
7. Veljið gerð færslubókar sem getur notað þessa greiðsluþóknun.
    * Ef þessi gjöld eru notaðar fyrir greiðslur viðskiptavina, færslubókargerð líklega verður greiðslu Viðskiptavinar.  
8. Smellið á „Vista“.
9. Smellt er á uppsetning Greiðsluþóknunar.
    * Uppsetning greiðsluþóknunar er notuð til að skilgreina skilyrði fyrir það hvenær greiðsluþóknun verður metin.  Til dæmis er hægt að skilgreina þóknunin verður reiknuð ef bankareikningurinn er USMF OPER og greiðsluháttur er ávísun.  
10. Veljið annað hvort Töflu, Flokk eða Allt til að skilgreina hvaða bankareikninga verða metnar þessu gjaldi.
    * Ef Allt er valið, gæti allar bankareikningar verið metnar fyrir þessu gjaldi.  Ef Tafla er valinn er aðeins bankareikningur sem þú valdir verið metnar gjaldi. Ef þú velur Flokk, einungis bankareikningur í valda bankaflokkinn gæti verið metnar þessu gjaldi.  
11. Veljið bankaflokk eða bankareikningi.
    * Ef Tafla er valin, birtir leitin bankareikninga. Ef flokkur er valin, birtir leitin bankaflokka.  
12. Í listanum skal smella á tengilinn í valinni línu.
13. Velja Greiðsluhátt sem verður metið þessu gjaldi.
    * Til dæmis er hægt að meta þóknun viðskiptavinum ef þeir senda greiðslur sem ávísun, frekar en sem rafræna greiðslu.  
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Ef við á, færið inn gjaldmiðil greiðslunnar.
    * Greiðslugjaldmiðli er notað sem aukaleg skilyrði fyrir hvort þóknunin verður metin.  Til dæmis bankanum gæti gjaldfærð aukalegar þóknun fyrir greiðslur mótteknar í USD-gjaldmiðli, þar sem þær vanalega aðeins færðar í gjaldmiðli EUR.  
16. Velja hvort gjaldið verður prósentu, upphæð eða bil.
17. Færa inn prósentu eða upphæð þóknunar.
    * Sé svæðið Prósenta/Upphæð Prósenta, þá mun gildi fært inn hér verða prósenta. Ef svæðið Prósenta/Upphæð er Upphæð, þá er gildi sem færð er inn hér vera upphæð. Sé svæðið Prósenta/Upphæð er tímabil, nota tímabils flipann til að skilgreina lög.  
18. Veljið gjaldmiðil fyrir gjöldin í svæðinu gjaldmiðill Þóknunar.
    * Þetta er gjaldmiðill sem þóknunin verður stofnuð í.  
19. Smellið á „Vista“.

