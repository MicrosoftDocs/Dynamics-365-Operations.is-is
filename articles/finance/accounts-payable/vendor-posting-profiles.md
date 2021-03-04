---
title: Bókunarreglur lánardrottna
description: Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43450c5f7ab8295b896b591880da9d0bddd955cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444213"
---
# <a name="vendor-posting-profiles"></a>Bókunarreglur lánardrottna

[!include [banner](../includes/banner.md)]

Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag.

<a name="vendor-posting-profiles"></a>Bókunarreglur lánardrottna
-----------------------

Bókunarreglur lánardrottina gera þér kleift að úthluta fjárhagslyklum og skjalastillingum á alla lánardrottna, hóp af lánardrottnum eða einn lánardrottinn. Þessar stillingar verður notaðar þegar þú stofnar innkaupapantanir, lánardrottnalykla og staðgreiðslur. Fyrir sumar færslur geturðu valið bókunarreglu sem er frábrugðin og sem hefur forgang fram yfir bókunarregluna sem er sett upp fyrir færslur í þessar skjámynd. Sjálfgefin bókunarregla er skilgreind á flýtiflipanum **Fjárhagur og Virðisaukaskattur** á síðunni **Færibreytur viðskiptaskulda**. Sjálfgefin bókunarregla er síðan sjálfvirkt tekin með í haus nýrra skjala þar sem hægt er að breyta henni í aðra bókunarreglu ef þörf krefur.

Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð á síðunni **Skilgreiningar færslubókana**. Bókunarskilgreining stýra bókun á lánardrottnafærslum í fjárhag í stað bókunarskilgreininga.

## <a name="creating-a-posting-profile"></a>Stofnun Bókunarregla
### <a name="setup"></a>**Uppsetning**

Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni. Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu. Í bókunarferlinu er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi.

| **Lykilkóði** svæðisgildið | **Númer lykils/Flokks** svæðisgildið        | Forgangsröðun leitar |
|------------------------------|---------------------------------------------|-----------------|
| **Tafla**                    | Tilgreindur lánardrottnareikningur                     | 1               |
| **Hópur**                    | Lánardrottnahópur sem er úthlutað á lánardrottinn | 2               |
| **Öll**                      | Autt                                       | 3               |

Ef þú vilt að allar lánardrottnafærslur hafi sömu bókunarregluna skaltu aðeins setja upp eina bókunarreglu með **Allt** í reitinn **Reikningskóði**. Tilgreindu eftirfarandi gildi til að setja upp bókunarregluna.

<table>
<thead>
<tr class="header">
<th>Svæði</th>
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
<li><strong>Taflan</strong> – bókunarregla við einn lánardrottinn. Veldu lánardrottnalykil í reitnum <strong>Númer lykils/flokks</strong>.</li>
<li><strong>Taflan</strong> – bókunarregla á við einn lánardrottnaflokk. Veljið lánardrottnaflokkur í reitnum <strong>Númer lykils/flokks</strong>.</li>
<li><strong>Allt</strong> – bókunarregla á við alla lánardrottna. Látið reitinn <strong>Númer lykils/flokks</strong> vera autt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Númer lykils/flokks</strong></td>
<td>Ef <strong>Tafla</strong> er valin í reitnum <strong>Lykilkóði</strong> veljið þá lykilnúmer lánardrottins sem er tengdur við bókunarregluna. Ef valinn er <strong>Flokkur</strong> skaltu velja flokk lánardrottins. Ef <strong>Allt</strong> er valið skal skilja þenan reit eftir auðan.</td>
</tr>
<tr class="odd">
<td><strong>Safnlykill</strong></td>
<td>Veljið fjárhagslykilinn sem nota á sem safnlykil fyrir lánardrottna sem bókunarreglan er tengd. Færibreytan <strong>Ekki leyfa handvirka færslu</strong> fyrir þennan aðalreikning verður merkt. Ef þú fjarlægir síðan þennan reikning úr pósti skaltu staðfesta stillinguna <strong>Ekki leyfa handvirka færslu</strong> á síðunni <strong>Aðalreikningar</strong>. 
<p><strong>Ath.:</strong> Ef valkosturinn <strong>Nota bókunarskilgreiningar</strong> er valinn á síðunni <strong>Færibreytur fjárhags</strong> er færslubókunarskilgreining fyrir reikningur lánardrottins notað í stað samantektarlykils.</p>
</td>
</tr>
<tr class="even">
<td><strong>Jafna lykil</strong></td>
<td>Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá. Þetta svæði er aðeins tiltækur þegar sjóðstreymisspá er virkjaður.</td>
</tr>
<tr class="odd">
<td><strong>Fyrirframgreiðslur virðisaukaskatts</strong></td>
<td>Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.
<p><strong>Ath.:</strong> Bókunarreglan sem er notuð þegar greiðslan er merkt sem fyrirframgreiðsla er valin í reitnum <strong>Bókun</strong> með reitnum <strong>Fylgiskjal fyrirframgreiðslubókar</strong> á svæðinu <strong>Fjárhags og söluskattur</strong> á síðunni <strong>Færibreytur viðskiptaskulda</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Koma</strong></td>
<td>Veldu fjárhagslykilsins sem upplýsingar um ósamþykkta reikningur lánardrottins er bókað í. Upplýsingarnar eru færðar inn í komubók Reikninga. Til dæmis, færir notandi grunnupplýsingar um lánardrottnareikninga þegar þær eru mótteknar í komubók. Þegar komubókin er bókuð eru færslurnar bókaðar á lykil sem færður er inn hér og í reitnum <strong>Mótlykill</strong>. Þegar reikningarnir eru samþykktir er skuldin flutt úr komulykillinn í safnlykil lánardrottna.</td>
</tr>
<tr class="odd">
<td><strong>Mótlykill</strong></td>
<td>Veljið fjárhagslykilsins sem er notaður fyrir mótfærslu ósamþykktra lánardrottnareikninga sem eru uppfærðir í gegnum komubókina. Mótfærslulykillinn virkar sem mótlykill fyrir færslur sem eru bókaðar í vörukomubók. Þess vegna er inniheldur lykillinn innkaup lánardrottins sem hafa ekki verið samþykkt enn.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Töflutakmarkanir**

Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út. Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.

Tilgreindu eftirfarandi gildi til að setja upp bókunarregluna

| Svæði          | Lýsing                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Jöfnun** | Veljið þennan valkost til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu. Ef þessi valkostur er tómur þarftu að jafna færslur handvirkt með því að nota síðuna **Jafna opnar færslur**. |
| **Hætta við**     | Veljið þennan valkost ef þú vilt geta hætt við færslur sem eru með þessari bókunarreglu.                                                                                                               |
| **Loka**      | Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar. Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]