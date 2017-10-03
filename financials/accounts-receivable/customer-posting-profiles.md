---
title: "Bókunarreglur viðskiptavina"
description: "Bókunarreglur viðskiptavina stýra bókun á viðskiptavinafærslum í fjárhag."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: b36e75a5f527b41d50cc73e28a0b4e7e5df67e5c
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2017

---

# <a name="customer-posting-profiles"></a>Bókunarreglur viðskiptavina

[!include[banner](../includes/banner.md)]


Bókunarreglur viðskiptavina stýra bókun á viðskiptavinafærslum í fjárhag.

<a name="customer-posting-profiles"></a>Bókunarreglur viðskiptavina
-------------------------

Bókunarreglur viðskiptavina gera það mögulegt að úthluta fjárhagslykla og skjalastillingar fyrir alla viðskiptavini, hóp af viðskiptavinum eða einn viðskiptavin. Þessar stillingar verður notuð þegar stofnaðar eru sölupantanir, reikningur með frjálsum texta, staðgreiðslur, innheimtubréf og vaxtanótur. Fyrir sumar færslur geturðu valið bókunarreglu sem er frábrugðin og sem hefur forgang fram yfir bókunarregluna sem er sett upp fyrir færslur í þessar skjámynd. 

Sjálfgefin bókunarregla er skilgreint í flýtiflipanum Fjárhagur og Virðisaukaskattir á síðunni Færibreytur viðskiptaskulda. Sjálfgefin bókunarregla er síðan tekin með sjálfkrafa í haus nýrra skjala þar sem hægt er að breyta henni í aðra bókunarreglu ef þörf krefur.

Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð í síðu skilgreining færslubókunar. Bókunarskilgreiningar stýra bókun á viðskiptavinafærslum í fjárhag í stað bókunarskilgreininga.

## <a name="creating-a-posting-profile"></a>Stofnun Bókunarregla
Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni. Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu. Við bókunarferli er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi:

| **Lykilkóði** svæðisgildið | **Númer lykils/Flokks** svæðisgildið            | Forgangsröðun leitar |
|------------------------------|-------------------------------------------------|-----------------|
| **Tafla**                    | Tiltekinn viðskiptavinareikningur.                       | 1               |
| **Flokkur**                    | Viðskiptavinarflokkur sem er úthlutað á viðskiptavininn | 2               |
| **Allt**                      | Autt                                           | 3               |

Ef óskað er eftir að allar færsla viðskiptavinar hafi sömu bókunarregluna setjið þá einungis upp eina bókunarreglu með gildinu  Allt í svæðið lykilkóði. Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Reitur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bókunarregla</strong></td>
<td>Færið inn kóða fyrir bókunarreglu. T.d. væri hægt að útbúa tvær bókunarreglur til að fá einn lykil fyrir viðskiptavinastöður í landsgjaldmiðlinum og annan fyrir viðskiptavinastöður í erlendum gjaldmiðli. Hægt væri að kalla annan lykilinn „Lands“ og hinn „Erlendur“.</td>
</tr>
<tr class="even">
<td><strong>Lýsing</strong></td>
<td>Færa skal inn lýsingu á bókunarregla. Þetta er einungis notað til að auðkenna betur bókunarregla þegar það er skoða í þessa síðu.</td>
</tr>
<tr class="odd">
<td><strong>Kóði lykils</strong></td>
<td>Tilgreinið hvort bókunarreglan eigi við um einstakan viðskiptavin, flokk af viðskiptavinum eða alla viðskiptavini:
<ul>
<li><strong>Taflan</strong> – bókunarregla á við einn viðskiptamaður. Veljið viðskiptavinalykil í númerareit lykils/flokks.</li>
<li><strong>Taflan</strong> – bókunarregla á við einn viðskiptavinaflokk. Veljið viðskiptavinaflokk í númerareit lykils/flokks.</li>
<li><strong>Allt</strong> – bókunarregla á við alla viðskiptavini. Látið Númer lykils/Flokks svæðisgildið vera autt.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Númer lykils/flokks</strong></td>
<td>Ef tafla er valin í svæðinu lykilkóði veljið þá lykilnúmer viðskiptavinar sem er tengdur við bókunarregluna. Ef valinn er Flokkur, veljið þá flokk viðskiptavina. Ef allt er valið skal skilja þetta svæði eftir autt.</td>
</tr>
<tr class="odd">
<td><strong>Safnlykill</strong></td>
<td>Veljið fjárhagslykilinn sem nota á sem safnlykil viðskiptavina fyrir viðskiptavini sem bókunarreglan er úthlutuð á.</td>
</tr>
<tr class="even">
<td><strong>Jafna lykil</strong></td>
<td>Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá. Þetta svæði birtast aðeins ef sjóðstreymisspár eru virkjuð.</td>
</tr>
<tr class="odd">
<td><strong>Fyrirframgreiðslur virðisaukaskatts</strong></td>
<td>Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Ábending" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Athugið</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Síðunni færibreytur viðskiptakrafna er notuð til að tilgreina bókunarreglu sem nota á þegar greiðsla er merkt sem fyrirframgreiðsla.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Skuldbindingar vegna afsláttarlykils</strong></td>
<td>Veljið Fjárhagslyklar fyrir afsláttarskuldbindingar.</td>
</tr>
<tr class="odd">
<td><strong>Innheimtubréfaröð</strong></td>
<td>Veljið kennimerki innheimtubréfaraðar fyrir viðskiptavini sem bókunarreglan tengist.</td>
</tr>
<tr class="even">
<td><strong>Vaxtakóði</strong></td>
<td>Veljið vaxtakóði til að nota fyrir útreikninga vaxta fyrir viðskiptavini sem bókunarreglan tengist.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Töfluskorður**

Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út. Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.

Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :

| Reitur                 | Lýsing                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Uppgjör**        | Veljið þessa víxlun til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu. Ef þessi víxlun er tóm þarftu að jafna færslur handvirkt með því að nota Jafna opnar færslur síðuna eða síðuna færa inn greiðsla viðskiptavinar. |
| **Áhugasvið**          | Veldu þessa víxlun eigi að reikna vexti á útistandandi skuldum fyrir viðskiptavinalykill  með þessa forstillingum. Ef víxlunin er hreinsaður, munu vextir ekki vera reiknaðir fyrir þessa viðskiptavini.                                           |
| **Innheimtubréf** | Veldu þessa víxlun eigi innheimtubréf að vera myndað fyrir viðskiptavinalykill  með þessa forstillingum. Ef víxlunin er hreinsaður, munu innheimtubréf ekki vera mynduð fyrir þessa viðskiptavini.                                                 |
| **Loka**             | Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar. Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.                                                                           |



Frekari upplýsingar, sjá [Yfirlit yfir greiðslur viðskiptavinar](../cash-bank-management/tasks/customer-payment-overview.md).


