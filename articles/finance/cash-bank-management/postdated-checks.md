---
title: Fyrirframdagsettar ávísanir
description: Þessi grein veitir upplýsingar um stuðning fyrir fyrirframdagsettar ávísanir. Fyrirframdagsettar ávísanir eru gefnar út til að greiða og taka á móti greiðslum í framtíðinni.
author: angelad116
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: kfend
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d32ed9de66bc92e17c5515a4266f41aaeb9f2c1
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151362"
---
# <a name="postdated-checks"></a>Fyrirframdagsettar ávísanir

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um stuðning fyrir fyrirframdagsettar ávísanir. Fyrirframdagsettar ávísanir eru ávísanir sem eru gefnar út til að greiða og taka á móti greiðslum í framtíðinni. Þess vegna er ekki hægt að leysa út ávísun fram að tilgreindri dagsetningu.

Dynamics 365 Finance styður ferli fullrar stjórnunar fyrir fyrirframdagsettar ávísanir bæði í Viðskiptakröfum og Viðskiptaskuldum, eins og sýnt er í eftirfarandi töflu.
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
<td>Skrá upplýsingar um fyrirframdagsettar ávísanir sem er gefin út til lánardrottins. Þegar greiðslan er bókuð er skuld lánardrottins viðurkennd , en bankareikningurinn er ekki enn kreditfærður. Í stað þess er millireikningur notað fyrir þennan tilgang. </td>
</tr>
<tr class="odd">
<td>Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottin</td>
<td>Skrá upplýsingar um fyrirframdagsettar ávísanir sem er tekið er við frá viðskiptavini. Þegar greiðslan er bókuð er viðskiptakrafa viðskiptavinar kreditfærð, en bankareikningurinn er ekki enn debetfærður. Í stað þess er millireikningur notað fyrir þennan tilgang.</td>
</tr>
<tr class="even">
<td>Skráning og bókun fyrirframdagsettrar ávísunar skiptivöru fyrir viðskiptavin eða lánardrottin</td>
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
<td>Hægt er að hætta við bókaða fyrirframdagsetta ávísun í eftirfarandi aðstæðum: - Ávísuninni var skilað af bankanum.
- Ávísunin er notuð fyrir rangan reikning.
- Staðgreiðsla er framkvæmd í stað ávísunarinnar.
  </td>
  </tr>
  <tr class="even">
  <td>Stöðva greiðslu fyrir fyrirframdagsettri ávísun</td>
  <td>Hægt er að stöðva greiðslu á fyrirframdagsettu ávísuninni sem gefin var út á lánardrottinn vegna ástæðna svo sem ónógrar innistæðu á bankareikningnum, breytingum á skilmálum lánardrottins, sendingu á gölluðum vörum frá lánardrottni eða vöruskilum til lánardrottins. Aðeins er hægt er að stöðva greiðslu vegna ávísana sem ekki er búið að innleysa.</td>
  </tr>
  </tbody>
  </table>



Frekari upplýsingar er hægt að finna í eftirfarandi efni:

[Setja upp fyrirframdagsettar ávísanir](tasks/set-up-postdated-checks.md)

[Skrá og bóka fyrirframdagsetta ávísun fyrir viðskiptavin](tasks/register-post-postdated-check-customer.md)

[Gera upp fyrirframdagsetta ávísun frá viðskiptavini](tasks/settle-postdated-check-customer.md)

[Skrá og bóka fyrirframdagsetta ávísun fyrir lánardrottinn](tasks/register-post-postdated-check-vendor.md) 

[Gera upp fyrirframdagsetta ávísun fyrir lánardrottin](tasks/settle-postdated-check-vendor.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
