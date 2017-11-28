---
title: "Bókunarskilgreiningar"
description: "Þessi grein veitir upplýsingar um bókunarskilgreiningar og hvernig skuli skilgreina þær og búa til tengla í. Fyrir studdar bókunargerðir og skjöl, er hægt að nota bókunarskilgreiningar í stað bókunarreglur til að flokka aðallykla og fjárhagsvíddir í bókhaldsfærslur."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 513d3e20e0c89eb0064e3c1bc11a3a8dea43cfe4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="posting-definitions"></a>Bókunarskilgreiningar

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um bókunarskilgreiningar og hvernig skuli skilgreina þær og búa til tengla í. Fyrir studdar bókunargerðir og skjöl, er hægt að nota bókunarskilgreiningar í stað bókunarreglur til að flokka aðallykla og fjárhagsvíddir í bókhaldsfærslur.

Fyrir studdar bókunargerðir og skjöl, er hægt að nota bókunarskilgreiningar í stað bókunarreglur til að flokka aðallykla og fjárhagsvíddir í bókhaldsfærslur. Hægt er að skoða skjöl og gerðir bókana á í **bókunarskilgreiningar Færslna** síðu. 

Til að byrja að nota bókunarskilgreiningar, í**Nota bókunarskilgreiningar** valkostinn á í **fjárhagsfæribreytur** síðu. Jafnvel þegar nota bókunarskilgreiningar, enn þarf að skilgreina bókunarreglur fyrir upphaflegar færslur og ekki studdar bókunargerðir og skjöl. 

Þú verður að nota Bókunarskilgreiningar til að styðja bókhald fjárúthlutunar innkaupapantana og áætlaða fjárúthlutun fyrir innkaupabeiðnir.

## <a name="defining-posting-definitions"></a>Skilgreina Bókunarskilgreining
Nota skal**Bókunarskilgreiningar** síðu til að tilgreina skilyrði jöfnunar og færslur sem á að mynda þegar samsvörun verður. Samsvörunarskilyrði eru metnar fyrir upphaflegar færslur og dreifingar á fjárhagsupphæð. 

Á **Bókunarskilgreiningar** síðu má einnig tengja forgangstölur á línur til að stýra röðinni sem línurnar eru metnar í. Línur sem hafa lægsta forgangsnúmer eru metnar fyrst. Til dæmis allar línur sem hafa forgang 1 eru metin og síðan línur sem hafa forgang yfir 2 o.s.frv. Þegar samsvörun finnst eru önnur skilyrði fyrir samsvörun hunsuð. Þar að auki, Einnig geta aðeins skilyrði í flokknum sem samsvara upprunalegu færslunni stofna myndaðrar færslur. 

Hægt er að villuleita bókunarskilgreiningar með í **Prófa bókunarskilgreining** leiðsagnarforritið. Þegar búið er að skilgreina  dæmi um upprunafærslu bókunarskilgreiningar , sérðu myndaðar færslur. 

Hægt er að nota útgáfur bókunarskilgreiningar með gildisdagsetningum. Til dæmis er hægt að stofna síðari útgáfum af bókunarskilgreiningu til að bóka í annan fjárhagslykil í nýtt fjárhagsár. 

Nota skal **bókunarskilgreiningar Færslna** síðu til að tengja bókunarskilgreiningar við færslugerðir.

## <a name="linking-posting-definitions"></a>Tenging Bókunarskilgreininga
Hægt er að tengja úr einni bókunarskilgreiningu til annarar þegar bókunarskilgreiningar eru stofnaðar. Skilyrði fyrir skilgreiningu sem er tengd eru tekin til greina auk skilyrði fyrir núverandi bókunarskilgreiningu. Þessi eiginleiki auðveldar að spara tíma, því ekki þarf að færa aftur inn skilyrði á **Færslur** flýtiflipi á í **Bókunarskilgreiningar** síðunni fyrir núverandi bókunarskilgreiningu ef þegar er færður inn þessar línur fyrir aðra skilgreiningu. 

Taka með alla tengla í skýringarmyndu eða töflum sem væri að nota. Til að forðast árekstra með núverandi bókunarskilgreiningu, ganga úr skugga um að línurnar í hverri bókunarskilgreiningar sem tengt er í séu einkvæmir. 

Eftirfarandi takmarkanir eiga við þegar stofnaðir eru tengla í bókunarskilgreiningar:

-   Tiltekið bókunarskilgreiningu getur annað hvort tengja aðra bókunarskilgreiningu eða tengja úr aðra bókunarskilgreiningu, en ekki bæði. Hins vegar getur bókunarskilgreiningu tengja margar bókunarskilgreiningar.
-   Hægt er að setja upp tengla aðeins milli bókunarskilgreiningar sem eru í sömu einingunni.
-   Hægt er að úthluta bókunarskilgreiningu á hvaða færslugerð sem er, en færslugerð verður að vera í sömu einingunni og bókunarskilgreiningin. Nota skal **bókunarskilgreiningar Færslna** síðu til að sjá af hvaða tegund færsla er í kerfinu.


Frekari upplýsingar eru í [Dæmi um bókunarskilgreiningar](example-posting-definitions.md). 



