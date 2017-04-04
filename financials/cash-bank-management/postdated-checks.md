---
title: "Fyrirframdagsettar ávísanir"
description: "Þessi skrá upplýsingar um stuðning fyrir fyrirframdagsettar ávísanir í Microsoft Dynamics 365 fyrir Aðgerðir. Fyrirframdagsettar ávísanir eru ávísanir sem eru gefnar út til að greiða og taka á móti greiðslum í framtíðinni. Þess vegna er ekki hægt að leysa út ávísun fram að tilgreindri dagsetningu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Fyrirframdagsettar ávísanir

Þessi skrá upplýsingar um stuðning fyrir fyrirframdagsettar ávísanir í Microsoft Dynamics 365 fyrir Aðgerðir. Fyrirframdagsettar ávísanir eru ávísanir sem eru gefnar út til að greiða og taka á móti greiðslum í framtíðinni. Þess vegna er ekki hægt að leysa út ávísun fram að tilgreindri dagsetningu.

Microsoft Dynamics 365 aðgerða styður ferli fulla stjórnun fyrir fyrirframdagsettar ávísanir viðskiptavina og lánardrottna, eins og sýnt er í eftirfarandi töflu.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Aðstæður</th>
<th>Upplýsingar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Uppsetning fyrirframdagsettra ávísana</td>
<td>Þarf að setja upp nýju greiðsluaðferðina og tilgreina greiðsluaðferðina fyrir millireikninga fyrir útgefnar ávísanir, mótteknar ávísanir og staðgreiðsluskatt.</td>
</tr>
<tr class="even">
<td>Skráning og bókun fyrirframdagsettrar ávísunar fyrir lánardrottin</td>
<td>Skrá upplýsingar um fyrirframdagsettar ávísanir sem er gefin út til lánardrottins. Þegar greiðslan er bókuð viðurkenndur skuld lánardrottins, en bankareikningurinn er ekki enn kredit. Í stað þess er millireikningur notað fyrir þennan tilgang.</td>
</tr>
<tr class="odd">
<td>Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottin</td>
<td>Skrá upplýsingar um fyrirframdagsettar ávísanir sem er tekið er við frá viðskiptavini. Þegar greiðslan er bókuð, viðskiptakröfur viðskiptavinar er kredit en bankareikningurinn er ekki enn debet. Í stað þess er millireikningur notað fyrir þennan tilgang.</td>
</tr>
<tr class="even">
<td>Skrá og bóka fyrirframdagsettar endurnýjunarverð ávísun fyrir viðskiptavin eða lánardrottinn</td>
<td>
Ef upprunaleg ávísun til lánardrottins eða frá viðskiptavini tapast eða skemmist er hægt að gefa út endurnýjaða fyrirframdagsetta ávísun. Þegar upplýsingar um ávísunina eru skráðar skal tilvísun í upprunalegu ávísunina fylgja með og gefa til kynna að nýja ávísunin komi í stað þeirra upprunalegu. Einnig er hægt að bóka endurnýjaða ávísun.</td>
</tr>
<tr class="odd">
<td>Flytja fyrirframdagsettar ávísanir viðskiptavinar til lánardrottins</td>
<td>Þegar tekið er á móti fyrirframdagsettri ávísun frá viðskiptavini er hægt að flytja þá ávísun til lánardrottins sem greiðsla.</td>
</tr>
<tr class="even">
<td>Jöfnun fyrirframdagsettar ávísunar viðskiptamanns eða lánardrottins</td>
<td>Gera upp fyrirframdagsetta ávísun sem er bókuð á millilykil fyrir viðskiptamann eða lánardrottin þegar ávísunin gjaldfellur loks. Þegar ávísun er jafnaður, er bankans að lokum debet- eða kreditfærður gagnvart millireikning sem notuð var áður.</td>
</tr>
<tr class="odd">
<td>Afturkalla fyrirframdagsetta ávísun fyrir lánardrottin</td>
<td>Hægt er að hætta við bókaða fyrirframdagsettar ávísanir í þessum aðstæðum:-ávísuninni var skilað af bankanum.
-Athugun er beitt á rangur reikningur.
-Staðgreiðsla er gerð með ávísun.
</td>
</tr>
<tr class="even">
<td>Stöðva greiðslu fyrir fyrirframdagsettar ávísanir</td>
<td>Hægt er að stöðva greiðslu á fyrirframdagsettu ávísuninni sem gefin var út á lánardrottinn vegna ástæðna svo sem ónógrar innistæðu á bankareikningnum, breytingum á skilmálum lánardrottins, sendingu á gölluðum vörum frá lánardrottni eða vöruskilum til lánardrottins. Hægt er að stöðva greiðslu á ávísanir sem hefur ekki verið autt.</td>
</tr>
</tbody>
</table>





