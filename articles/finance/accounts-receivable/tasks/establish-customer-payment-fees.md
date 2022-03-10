---
title: Setja upp greiðsluþóknanir viðskiptavina
description: Stofna greiðsluþóknanir fyrir greiðsluar viðskiptavinar.
author: ShivamPandey-msft
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15151987bb398de404994cdd416916c00a8dd1773bbf6d654f6a40160a2f4a49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768364"
---
# <a name="establish-customer-payment-fees"></a>Setja upp greiðsluþóknanir viðskiptavina

[!include [banner](../../includes/banner.md)]

Stofna greiðsluþóknanir fyrir greiðsluar viðskiptavinar.

Þetta verkefni notar USMF-sýnifyrirtækið.

1. Í **skoðunarrúðunni** ferðu í **Kerfi > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluþóknun**.
2. Smellt er á **Nýtt**.
3. Í reitinn **Kenni þóknunar** skal færa inn kenni þóknunar. Kenni Þóknunar Birtist í greiðslubókum, þannig að hafðu það lýsandi til að skilja er hvaða þóknun er metin.  
4. Færa skal inn heiti þóknunar í reitinn **Heiti**.
5. Færið inn lýsingu fyrir þóknun í reitinn **Lýsing þóknunar**.
6. Í reitnum **Gjald** skal velja hvort gjaldið verður skuldfært á viðskiptavin eða fjárhagslykil. Ef viðskiptavinur er metin þóknun, veljið Viðskiptavinar. Ef þóknunin verður meta sem útgjöld á fyrirtækið , velja Fjárhag. Veljið Viðskiptavin fyrir þetta verk.  
7. Í reitnum **Gerð færslubókar** skal velja þá tegund færslubókar sem getur notað þetta greiðslugjald. Ef þessi gjöld eru notaðar fyrir greiðslur viðskiptavina, færslubókargerð líklega verður greiðslu Viðskiptavinar.  
8. Smellt er á **Vista**.
9. Smellt er á **Uppsetning greiðsluþóknunar**. Uppsetning greiðsluþóknunar er notuð til að skilgreina skilyrði fyrir það hvenær greiðsluþóknun verður metin.  Til dæmis er hægt að skilgreina þóknunin verður reiknuð ef bankareikningurinn er USMF OPER og greiðsluháttur er ávísun.  
10. Í reitnum **Flokkanir** skal velja annaðhvort Töflu, Flokk eða Allt til að skilgreina hvaða bankareikningar þetta gjald verður skuldfært á. Ef Allt er valið, gæti allar bankareikningar verið metnar fyrir þessu gjaldi.  Ef Tafla er valinn er aðeins bankareikningur sem þú valdir verið metnar gjaldi. Ef þú velur Flokk, einungis bankareikningur í valda bankaflokkinn gæti verið metnar þessu gjaldi.  
11. Í reitnum **Bankavensl** skal velja annaðhvort bankaflokk eða bankareikning. Ef Tafla er valin, birtir leitin bankareikninga. Ef flokkur er valin, birtir leitin bankaflokka.  
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í reitnum **Greiðslumáti** skal velja þann greiðslumáta sem þetta gjald verður metið fyrir. Til dæmis er hægt að meta þóknun viðskiptavinum ef þeir senda greiðslur sem ávísun, frekar en sem rafræna greiðslu.  
14. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
15. Ef það á við skal í reitnum **Greiðslugjaldmiðill** slá inn greiðslugjaldmiðil. Greiðslugjaldmiðli er notað sem aukaleg skilyrði fyrir hvort þóknunin verður metin.  Til dæmis bankanum gæti gjaldfærð aukalegar þóknun fyrir greiðslur mótteknar í USD-gjaldmiðli, þar sem þær vanalega aðeins færðar í gjaldmiðli EUR.  
16. Velja hvort gjaldið verður prósentu, upphæð eða bil.
17. Í **reitinn Hlutfall/upphæð** skal slá inn annaðhvort prósentu eða fjárhæð gjaldsins. Sé svæðið Prósenta/Upphæð Prósenta, þá mun gildi fært inn hér verða prósenta. Ef svæðið Prósenta/Upphæð er Upphæð, þá er gildi sem færð er inn hér vera upphæð. Sé svæðið Prósenta/Upphæð er tímabil, nota tímabils flipann til að skilgreina lög.  
18. Veljið gjaldmiðil fyrir þóknunina í reitnum **Gjaldmiðill þóknunar**. Þetta er gjaldmiðill sem þóknunin verður stofnuð í.  
19. Smellt er á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]