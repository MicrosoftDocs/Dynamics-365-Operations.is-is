--- 
title: "Setja upp greiðslumáta fyrir viðskiptavin"
description: "Stofna greiðsluhátt fyrir greiðsla viðskiptavinar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: bfafcccb12112ca7cceefb65be3f942bfc307751
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-method-of-payment"></a>Setja upp greiðslumáta fyrir viðskiptavin

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


