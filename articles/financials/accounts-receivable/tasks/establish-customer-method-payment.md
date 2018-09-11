--- 
title: "Setja upp greiðslumáta fyrir viðskiptavin"
description: "Stofna greiðsluhátt fyrir greiðsla viðskiptavinar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabcfe83ac83a8210ce4e0d46a08acdc48f4bf3b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-method-of-payment"></a>Setja upp greiðslumáta fyrir viðskiptavin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Stofna greiðsluhátt fyrir greiðsla viðskiptavinar. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Farðu í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.
2. Smellið á „Nýtt“.
3. Í svæðinu greiðslumáta, færið inn Kenni fyrir greiðsluaðferð.
    * Kenni greiðsluaðferðar er sýnt á reikninga og greiðslur, svo gera skal nægjanlega lýsandi til að skilja hvaða gerð af greiðslu er skráð og fyrir hvaða bankareikning.  
4. Færið inn lýsingu í svæðinu Lýsingu.
5. Veljið hvaða staða greiðslu er nauðsynlegt í til að bóka greiðslur.
    * Þegar greiðsla viðskiptavinar er stofnuð, það er aðeins hægt að bóka þegar greiðslustöðu samræmist greiðslustöðu sem skilgreind hér.  
6. Veljið hvernig á að stofna greiðslur viðskiptavina fyrir reikninga.
    * Þessi valkostur er aðeins notað þegar greiðslutillaga er keyrð. Hægt væri að nota greiðslutillögu fyrir greiðslur viðskiptavinar þegar gerð er beingreiðsla, og fjármagn tekið af  bankareikningar viðskiptavinar.  
7. Veljið greiðslugerð
    * Greiðslugerð hjálpar til við ákvarða hvort einhverjar villuleit á sér stað eða ekki á greiðsluna.  
8. Velja hvað greiðslur gerð lykils verður bókað til.
    * Venjulega yrði Banki valinn fyrir þennan valmöguleika.  
9. Veljið bankareikninginn sem verður að skrá þessa greiðslu.
10. Færa inn bankafærslugerð til að auðkenna gerð greiðslunnar sem er notað af bankanum.
    * Færslugerð banka er notaður við ferlið afstemmingu banka og getur auðvelda afstemmingu.  
11. Velja hvort þessi greiðslu tímabundið bókuð á millilykil.
    * Ef óskað er að reyna fljótandi tíma fyrir greiðslu til að hreinsa banka, nota milliaðgerðir. Greiðslan bókar tímabundið fjárhagslykil þar til hún hreinsar banka, og greiðsla færist á bankareikning sem er skilgreindur hér.  
12. Færið inn aðallykilinn notað fyrir millibókun.
    * Þetta er aðallykill sem greiðslan verður tímabundið bókuð í ef notuð er milliaðgerð.  
13. Notið flipann skráarsnið til að skilgreina stillingar fyrir rafrænar greiðslur.
14. Notið flipann greiðslueftirlit til að skilgreina svæðin sem eru skylda.
    * Til dæmis, ef þess er krafist allar greiðslur með þessari greiðsluaðferð til að vera lagðar inn, hægt er að velja valkostinn á þessum flipa.  
15. Notið flipann greiðslueigindir til að tilgreina greiðslueigindir sem á að nota fyrir þennan greiðslumáta.
16. Smellið á „Vista“.


