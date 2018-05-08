---
title: "Bókunarreglur lánardrottna"
description: "Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3571726fd3603371b8e1daec7d6ebe85d72d280d
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-posting-profiles"></a>Bókunarreglur lánardrottna

[!include [banner](../includes/banner.md)]

Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag.

<a name="vendor-posting-profiles"></a>Bókunarreglur lánardrottna
-----------------------

Bókunarreglur lánardrottina gera það mögulegt að úthluta fjárhagslykla og skjalastillingar fyrir alla lánardrottna, hóp af lánardrottna eða einn lánardrottinn. Þessar stillingar verður notuð þegar stofna innkaupapöntun, reikningur lánardrottins og  staðgreiðsla. Fyrir sumar færslur geturðu vaæo‘ bókunarreglu sem er frábrugðin og sem hefur forgang fram yfir bókunarregluna sem er sett upp fyrir færslur í þessar skjámynd. Sjálfgefin bókunarregla er skilgreint í flýtiflipanum Fjárhagur og Virðisaukaskattur á síðunni Færibreytur viðskiptaskulda. Sjálfgefin bókunarregla er síðan tekin með sjálfkrafa í haus ný skjöl þar sem hægt er að breyta henni í aðra bókunarreglu ef þörf krefur.

Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð í síðu skilgreining færslubókunar. Bókunarskilgreining stýra bókun á lánardrottnafærslum í fjárhag í stað bókunarskilgreininga.

## <a name="creating-a-posting-profile"></a>Stofnun Bókunarregla
### <a name="setup"></a>**Uppsetning**

Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni. Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu. Við bókunarferli er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi:

| **Lykilkóði** svæðisgildið | **Númer lykils/Flokks** svæðisgildið        | Forgangsröðun leitar |
|------------------------------|---------------------------------------------|-----------------|
| **Tafla**                    | Tilgreindur lánardrottnareikningur                     | 1               |
| **Flokkur**                    | Lánardrottnahópur sem lánardrottinn tengist | 2               |
| **Allt**                      | Autt                                       | 3               |

Ef óskað er eftir að allar lánardrottnafærslur hafi sömu bókunarregluna, setjið þá einungis upp eina bókunarreglu með gildinu Allt í svæðið lykilkóði. Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :

<table>
<thead>
<tr class="header">
<th>Reitur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bókunarregla</strong></td>
<td>Færið inn kóða fyrir bókunarreglu. T.d. væri hægt að útbúa tvær bókunarreglur til að fá einn lykil fyrir lánardrottnastöður í landsgjaldmiðlinum og annan fyrir lánardrottnastöður í erlendum gjaldmiðli. Hægt væri að kalla annan lykilinn „Lands“ og hinn „Erlendur“.</td>
</tr>
<tr class="even">
<td><strong>Lýsing</strong></td>
<td>Færa skal inn lýsingu á bókunarregla.</td>
</tr>
<tr class="odd">
<td><strong>Kóði lykils</strong></td>
<td>Tilgreinið hvort bókunarreglan eigi við um einstakan lánardrottinn, flokk af lánardrottnum eða alla lánardrottna:
<ul>
<li><strong>Taflan</strong> – bókunarregla við einn lánardrottinn. Veljið lánardrottnalykill í númerareit lykils/flokks.</li>
<li><strong>Taflan</strong> – bókunarregla á við einn lánardrottnaflokk. Veljið lánardrottnaflokkur í númerareit lykils/flokks.</li>
<li><strong>Allt</strong> – bókunarregla á við alla lánardrottna. Látið Númer lykils/Flokks svæðisgildið vera autt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Númer lykils/flokks</strong></td>
<td>Ef tafla er valin í svæðinu lykilkóði veljið þá lykilnúmer lánardrottins sem er tengdur við bókunarregluna. Ef valinn er Flokkur, veljið þá flokk lánardrottins. Ef allt er valið skal skilja þetta svæði eftir autt.</td>
</tr>
<tr class="odd">
<td><strong>Safnlykill</strong></td>
<td>Veljið fjárhagslykilinn sem nota á sem safnlykil fyrir lánardrottna sem bókunarreglan er tengd.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Athugið" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Athugaðu</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ef víxlunin Nota bókunarskilgreiningar er valinn á síðunni Færibreytur fjárhags er færslubókunarskilgreining fyrir reikningur lánardrottins notað í stað samantektarlykils.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Jafna lykil</strong></td>
<td>Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá. Þetta svæði er aðeins tiltækur þegar sjóðstreymisspá er virkjaður.</td>
</tr>
<tr class="odd">
<td><strong>Fyrirframgreiðslur virðisaukaskatts</strong></td>
<td>Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Athugið" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Athugaðu</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bókunarreglan sem er notað þegar greiðslan er merkt sem fyrirframgreiðsla er valinn í reitnum fylgiskjal fyrirframgreiðslubókar í svæðinu Fjárhags og söluskattur á síðunni færibreytum viðskiptaskulda.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Koma</strong></td>
<td>Veldu fjárhagslykilsins sem upplýsingar um ósamþykkta reikningur lánardrottins er bókað í. Upplýsingarnar eru færðar inn í komubók Reikninga. Til dæmis, færir notandi grunnupplýsingar um lánardrottnareikninga þegar þær eru mótteknar í komubók. Þegar komubókin er bókuð eru færslurnar bókaðar á lykil sem færður er inn hér og í svæðinu Mótlykill. Þegar reikningarnir eru samþykktir er skuldin flutt úr komulykillinn í safnlykil lánardrottna.</td>
</tr>
<tr class="odd">
<td><strong>Mótlykill</strong></td>
<td>Veljið fjárhagslykilsins sem er notaður fyrir mótfærslu ósamþykktra lánardrottnareikninga sem eru uppfærðir í gegnum komubókina. Mótfærslulykillinn virkar sem mótlykill fyrir færslur sem eru bókaðar í vörukomubók. Þess vegna er inniheldur lykillinn innkaup lánardrottins sem hafa ekki verið samþykkt enn.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Töflutakmarkanir**

Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út. Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.

Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :

| Reitur          | Lýsing                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Uppgjör** | Veljið þennan valkost til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu. Ef þessi valkostur er tóm þarftu að jafna færslur handvirkt með því að nota Jafna opnar færslur síðuna. |
| **Hætta við**     | Veljið þennan valkost ef þú vilt geta hætt við færslur sem eru með þessari bókunarreglu.                                                                                                               |
| **Loka**      | Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar. Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.                                       |






