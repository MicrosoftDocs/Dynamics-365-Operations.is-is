---
title: Setja upp greiðslumáta fyrir viðskiptavin
description: Þetta efni útskýrir hvernig á að stofna greiðslumáta fyrir greiðslur viðskiptavina.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22680a3033c1518735eb9edb4c6f22f310509aba
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867632"
---
# <a name="establish-customer-method-of-payment"></a>Setja upp greiðslumáta fyrir viðskiptavin

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efni útskýrir hvernig á að stofna greiðslumáta fyrir greiðslur viðskiptavina. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Í skoðunarrúðunni ferðu í **Kerfi > Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir**.
2. Veljið **Nýtt**.
3. Í svæðinu **Greiðslumáti** skal færa inn kenni fyrir greiðsluaðferð. Kenni greiðsluaðferðar er sýnt á reikninga og greiðslur, svo gera skal nægjanlega lýsandi til að skilja hvaða gerð af greiðslu er skráð og fyrir hvaða bankareikning.  
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Veljið hvaða staða greiðslu er nauðsynlegt í til að bóka greiðslur. Þegar greiðsla viðskiptavinar er stofnuð, það er aðeins hægt að bóka þegar greiðslustöðu samræmist greiðslustöðu sem skilgreind hér.  
6. Veljið hvernig á að stofna greiðslur viðskiptavina fyrir reikninga. Þessi valkostur er aðeins notað þegar greiðslutillaga er keyrð. Hægt væri að nota greiðslutillögu fyrir greiðslur viðskiptavinar þegar gerð er beingreiðsla, og fjármagn tekið af bankareikningum viðskiptavinar.  
7. Veljið greiðslugerð Greiðslugerð hjálpar til við ákvarða hvort einhverjar villuleit á sér stað eða ekki á greiðsluna.  
8. Velja hvað greiðslur gerð lykils verður bókað til. Venjulega yrði Banki valinn fyrir þennan valmöguleika.  
9. Veljið bankareikninginn sem verður að skrá þessa greiðslu.
10. Færa inn bankafærslugerð til að auðkenna gerð greiðslunnar sem er notað af bankanum. Færslugerð banka er notaður við ferlið afstemmingu banka og getur auðvelda afstemmingu.  
11. Velja hvort þessi greiðslu tímabundið bókuð á millilykil. Ef óskað er að reyna fljótandi tíma fyrir greiðslu til að hreinsa banka, nota milliaðgerðir. Greiðslan bókar tímabundið fjárhagslykil þar til hún hreinsar banka, og greiðsla færist á bankareikning sem er skilgreindur hér.  
12. Færið inn aðallykilinn notað fyrir millibókun. Þetta er aðallykill sem greiðslan verður tímabundið bókuð í ef notuð er milliaðgerð.  
13. Notið flipann **Skráarsnið** til að skilgreina stillingar fyrir rafrænar greiðslur.
14. Notið flipann **Greiðslueftirlit** til að skilgreina svæðin sem eru skylda. Til dæmis, ef þess er krafist allar greiðslur með þessari greiðsluaðferð til að vera lagðar inn, hægt er að velja valkostinn á þessum flipa.  
15. Notið flipann **Greiðslueigindir** til að tilgreina greiðslueigindir sem á að nota fyrir þennan greiðslumáta.
16. Veljið **Vista**.

