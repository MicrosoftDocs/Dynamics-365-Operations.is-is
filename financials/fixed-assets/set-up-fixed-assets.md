---
title: Uppsetning eigna
description: "Þetta efnisatriði veitir yfirlit yfir Uppsetningu eignaeiningar."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: c239fd31e8ea865b0378cf0d6feb1dd920e396d0
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-fixed-assets"></a>Uppsetning eigna

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir yfirlit yfir Uppsetningu eignaeiningar.

<a name="overview"></a>Yfirlit
--------
Færibreytur stjórna almennri hegðun innan eignar.

Eignaflokkar leyfa þér að flokka eignunum og tilgreina sjálfgefnar eigindir fyrir hverja eign sem er úthlutað á flokk. Bókum er úthlutað á eignaflokka. Bækur rekja fjárhagslegu virði eignar yfir tíma með því að nota skilgreiningu afskriftir sem tilgreind er í afskriftareglu.

Eignir eru úthlutaðar flokki þar sem þær eru stofnaðar. Að sjálfgefnu eru bækur úthlutað eignaflokki sem er svo úthlutað á eign. Bækur sem eru skilgreind til að bóka í fjárhaginn tengjast bókunarreglu. Fjárhagslykla eru skilgreindar eftir bók í bókunarreglu og eru notaðar þegar færslur eigna eru bókuð. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Afskriftarreglur
Afskriftareglur ætti að setja upp fyrst. Í Afskriftaregla er skilgreint hvernig virði eignar er afskrifað með tímanum. Þú þarft að skilgreina aðferð við afskrift, afskriftarár (almanaksár eða fjárhagsár) og tíðni afskrifta.

## <a name="books"></a>Bækur
Eftir að setja upp afskriftareglur, verður að stofna nauðsynleg bækur fyrir eignunum. Hver bók rekur óháð fjárhagslegan lífsferil eigna. Hægt er að skilgreina bækur til að bóka tengdar færslur í fjárhag. Þessi skilgreining er sjálfgefna stillingin, þar sem hún er yfirleitt notuð við fjárhagsskýrslugerð fyrirtækis. Bækur sem bóka ekki í fjárhag bóka aðeins í undirbókar Eigna og eru yfirleitt notaðar fyrir skattskýrslugerð.

Aðalafskriftaregla er úthlutað á hvert bók. Bækur hafa einnig afskriftareglu umskipta, ef þessa gerð forstillingar á við. Til að láta hafa eignabók sjálfkrafa með í keyrslum afskrifta, þarf að virkja á Reikna afskrift valkostur. Ef þessi valkostur var ekki valinn fyrir eign sleppir afskriftatillaga eigninni.

Einnig hægt að setja upp afleiddar bækur. Tilgreindu afleiddu færslurnarer bókaðar sem nákvæmt afrit af aðalfærslunni gagnvart afleiddu bókunum. Þar af leiðandi eru afleiddra færslna yfirleitt settir upp fyrir kaup og losanir, en ekki fyrir afskriftarfærslur.

## <a name="fixed-asset-posting-profiles"></a>Bókunarreglur eigna
Eftir að þú setur upp bækur, geturðu stofnað bókunarreglur. Bókunarreglu verður að skilgreina með bók, en einnig er hægt að skilgreina það á ítarlegri stigi. Til dæmis er hægt að skilgreina bókunarreglu fyrir samsetningu bókar og eignaflokks eða jafnvel fyrir einstaka eignabók. Að sjálfgefnu eru fjárhagslykla sem eru skilgreindar notaðir fyrir eignafærslur.

Skilgreina verður fjárhagslykla sem notaðar eru við losunarferli, bæði sölulosun og rýrnunarlosun. Á losunartíma eigna eru áður bókaðar færslur bakfærðar úr upprunalegum lyklum og nettóupphæð eru færðar í viðeigandi lykil fyrir hagnað og tap fyrir eignalosun. Til að hjálpa til við að tryggja að fræslur séu bakfærðar á réttan hátt, verður að setja upp lyklana fyrir hverri gerð færslunnar sem notað er í fyrirtækinu. Aðallykilinn ætti að vera upprunalegi lykillinn sem stilltur var í bókunarreglu fyrir viðkomandi gerð færslu og mótlykill ætti að vera þinn hagnaður og tap fyrir losunarreikninginn. Undantekningin er bókað nettóvirði. Í þessu tilfelli ætti að stilla bæði aðallykilinn og mótlykil á hagnað og tap fyrir losunarreikninginn.

## <a name="fixed-asset-groups"></a>Eignaflokkar
Eignaflokkur er eini áskildi reiturinn þegar eign er stofnuð. Gildið í þessu svæði ákveður sjálfgildi nokkurra upplýsingasvæða fyrir eignina. Bækur eru settar upp þannig að sjálfgefna bókin er úthlutað á hverja eign í flokki. Hægt er síðan að stilla eiginleika fyrir bækur sem eiga við tiltekna eignaflokka, eins og Líftími og afskriftarreglu.

Einnig er hægt að skilgreina sérstakar heimildir til afskrifta eða viðbótarafskriftir, fyrir tiltekna samsetningu eignaflokks og bókar. Úthluta verður forgangur á sérstök heimild til afskriftar til að tilgreina röðina sem heimildir eru reiknaðar í þegar margar heimildir eru úthlutaðar á bók.

## <a name="fixed-asset-parameters"></a>Eignafæribreyta
Síðasta skrefið er að uppfæra færibreytur eigna.

Fjármögnunarþröskuldi svæði ákvarðar eignir sem eru afskrifaðar. Ef innkaupalína er valin sem föst eign, en hún uppfyllir ekki tilgreindan fjármögnunarþröskuld, er eign enn stofnuð eða uppfærð, en valkostur Reikna afskrift er stilltur á Nei. Þess vegna verður eignin ekki afskrifuð sjálfkrafa sem hluti af afskriftartillögunum.

Einn mikilvægur valkostur er að Stofna sjálfvirkt afskriftaleiðréttingaupphæðir með losun Þegar þessi valkostur er stilltur á Já, er afskrift eignar sjálfvirkt leiðrétt, byggt á stillingum afskriftar við losun eignar. Annar valkostur gerir þér kleift að draga frá staðgreiðsluafslættir frá kaupupphæð þegar um er að ræða kaup eignar með því að nota reikning lánardrottins.

Í flýtiflipi Innkaupapantanir  er hægt er skilgreina hvernig eignir eigi að vera stofnaðar sem hluti af innkaupaferli. Fyrsta valkostur er Leyfa eignakaup úr innkaupum. Ef þessu valkostur er stilltur á Já, eiga eignakaup á sér stað þegar reikningur er bókaður. Ef þessi valkostur er stilltur á Nei er enn hægt að setja eign á innkaupapöntunina (IP) og reikning, en kaupin verða ekki bókuð. Bókun verður að framkvæma sem sérstakt skref úr eignabók. Í valkostinum Stofna eign við bókun innhreyfingarskjals afurða eða reiknings er hægt að stofna nýja eign "fyrirvaralaust" við bókun, þannig að það þarf ekki að setja upp sem eign fyrir færsluna. Síðasta valkostinum Gá að stofnun eigna við innfærslu lína, á einungis við innkaupabeiðnir.

Hægt er að skilgreina ástæðukóða svo þeirra sé krafist fyrir breytingar á eign eða fyrir tiltekna eignafærslur.

Loks á Númeraraðir flipa skilgreina númeraraðir fyrir eignir. Hægt er að hnekkja númeraröð eigna eftir númeraröð eigna ef hún hefur verið tilgreind.




