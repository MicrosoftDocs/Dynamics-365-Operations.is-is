---
title: "Fyrirtæki og stigveldi fyrirtækis"
description: "Fyrirtæki er hópur af fólki sem eru að vinna saman að því að framkvæma viðskiptaferli eða ná markmiði. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 25d3628b0a1d5fd67bbb215e6cde2a08d062f9d2
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="organizations-and-organizational-hierarchies"></a>Fyrirtæki og stigveldi fyrirtækis

[!include[banner](../includes/banner.md)]


Fyrirtæki er hópur af fólki sem eru að vinna saman að því að framkvæma viðskiptaferli eða ná markmiði. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri.

<a name="organizations"></a>Fyrirtæki
-------------

Í Microsoft Dynamics 365 for Operations er hægt að skilgreina eftirfarandi gerðir samstæðufyrirtækja: Lögaðila, rekstrareiningar, og hópa.

Öll innri fyrirtæki eru gerðir af einingunni **Samningsaðil**. Notið þess vegna þessum fyrirtækjum í aðsetursbók til að geyma aðsetur og tengslaupplýsingar. Aðila, sem getur verið annað hvort einstaklingur eða fyrirtæki, geta tilheyrt einni eða fleiri aðsetursbækur.
### <a name="legal-entities"></a>Lögaðilar

Lögaðili er fyrirtæki sem hefur skráð ögfest lagalega uppbyggingu. Lögaðila er hægt að færa inn í samninga og eru þeir krafnir um að útbúa yfirlit sem segir til um frammistöðu þeirra. Fyrirtæki er lögaðila. Í þessari útgáfu af Microsoft Dynamics 365 for Operations eru fyrirtæki eina tegund af lögaðila sem þú getur búið til, og sérhver lögaðili tengist auðkenni fyrirtækisins. Þessi tenging til staðar þar sem fyrirtæki Kenni eða DataAreaId, í gagnalíkön þeirra er að nota sumar rekstrarsvið í forritinu. Í þessum virku svæðum eru fyrirtæki notuð sem mörk fyrir öryggi gagna. Notendur geta nálgast gögn aðeins fyrir fyrirtæki sem eru skráðir inn í.

### <a name="operating-units"></a>Rekstrareiningar

Rekstrareining er fyrirtæki sem er notað til að skipta stýringu verðmæta og rekstrarferlis í viðskiptum. Fólk í rekstrareiningu hefur skyldu til að hámarka notkun takmarkaðra auðlinda, bæta ferli og bera ábyrgð á afköstum sínum. Í Microsoft Dynamics 365 for Operations innihalda tegundir rekstrareininga kostnaðarstaði, viðskiptaeiningar, virðisstrauma, deildir og smásölurásir. Eftirfarandi tafla veitir frekari upplýsingar um hverja tegund rekstrareiningar.
| Gerð rekstrareiningar | Lýsing                                                                                                                                    | Tilgangur                                                                                                                                 |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Kostnaðarstaður         | Rekstrareining þar sem stjórnendur eru ábyrgir fyrir áætluðum útgjöldum og raunútgjöldum.                                                      | Notað fyrir stjórnun og rekstraráætlanagerðar stýringu viðskiptaferli sem ná yfir lögaðila.                                         |
| Viðskiptaeining       | Er hálf-sjálfstæð rekstrareining sem er stofnuð til að uppfylla viðskiptamarkmið áætlunar.                                                        | Notuð við fjárhagsskýrslugerð sem byggir á industries eða línur afurða sem fyrirtækið þjónar óháð lögaðila. |
| Virðisstraumur        | Rekstrareining sem stýrir einn eða fleiri framleiðsluflæði.                                                                                  | Almennt notað í lean manufacturing til að stjórna aðgerðum og flæði sem þarf til að útvega vöru eða þjónustu til neytenda.  |
| Deild          | Rekstrareining sem táknar flokk eða hagnýtan hluta fyrirtækis sem sinnir ákveðnu verki, svo sem sölu eða bókhald. | Notað til að gefa skýrslu um rekstrarsvið. Deild kann að borið ábyrgð á hagnaði og tapi og getur verið samsett úr hóp kostnaðarstaða.   |
| Smásölurás      | Rekstrareining sem táknar verslunarhúsnæði, netverslun eða netmarkaður.                                          | Notað fyrir stjórnun og rekstraráætlanagerðar stýringu á eina eða fleiri verslanir fyrir innan eða í lögaðila.                                  |

### <a name="teams"></a>Teymi

Teymi er fyrirtæki þar sem meðlimir deila  algengar ábyrgð, hagsmuni eða markmið. Liðin má ekki notaður í stigveldi fyrirtækja.
Stigveldi fyrirtækja
--------------------------

Setja upp stigveldi fyrirtækis til að skoða og gefa skýrslu um reksturinn frá ólíkum sjónarhornum. Til dæmis er hægt að setja upp stigveldi lögaðila fyrir skatt, lagalega eða lögbundna skýrslugerð. Setja upp stigveldi sem byggir á aðgerðaeiningum til að gefa skýrslu um fjárhagslegar upplýsingar sem ekki er krafist samkvæmt lögum, en sem er notuð við innri stjórnun. Til dæmis er hægt að stofna innkaupa stigveldi til að stýra innkaup reglur reglur og viðskiptaferli. Hverju stigveldi er úthlutað tilgangi í Microsoft Dynamics 365 for Operations. Tilgangur stigveldis ákvarðar gerðir fyrirtæki sem má hafa með í stigveldi. Tilgangur skilgreinir einnig hvaða forrit aðstæður sem hægt er að nota í stigveldinu. Fyrirtæki í stigveldi geta samnýtt færibreytur reglur og færslur. Fyrirtæki getur erft eða hunsað færibreytur móðurfélags þess. Hins vegar samnýtt aðalgögn, eins og afurðir og aðsetursbækur, gildir fyrir allt fyrirtækið og ekki er hægt að hnekkja verði fyrir einstök fyrirtæki. Stofnun fyrirtæki og stigveldi krefst vandlegrar áætlanagerðar. Sjá frekari upplýsingar í [Skipuleggja stigveldi fyrirtækis](plan-organizational-hierarchy.md).






