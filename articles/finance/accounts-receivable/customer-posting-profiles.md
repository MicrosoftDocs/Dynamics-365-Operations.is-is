---
title: Bókunarreglur viðskiptavina
description: Þessi grein lýsir bókunarsniðum viðskiptavina, sem stjórna bókun viðskiptavinafærslur í fjárhag.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0563040590eefab57706b183281c47a82e46076
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891696"
---
# <a name="customer-posting-profiles"></a>Bókunarreglur viðskiptavina

[!include [banner](../includes/banner.md)]

Þessi grein lýsir bókunarsniðum viðskiptavina, sem stjórna bókun viðskiptavinafærslur í fjárhag.

## <a name="customer-posting-profiles"></a>Bókunarreglur viðskiptavina

Bókunarsnið viðskiptavina gerir þér kleift að úthluta aðalbókareikningum og skjalastillingum til allra viðskiptavina, hóps viðskiptavina eða eins viðskiptamanns. Þessar stillingar verða notaðar þegar þú býrð til sölupöntunarreikninga, frítextareikninga, verkreikninga, greiðslubækur, innheimtubréf og vaxtanótur. 

Sjálfgefið póstsnið er skilgreint á **Fjárhagsbók og söluskattur** flipi á **Færibreytur viðskiptakrafna** síðu. Það er síðan sjálfkrafa innifalið í haus nýrra skjala. Þú getur breytt því þar ef annað póstsnið er krafist. 

Fyrirtæki sem samþykkja fyrirframgreiðslur frá viðskiptavinum stilla oft annað bókunarsnið fyrir fyrirframgreiðslur og tengja það í færibreytunum sem sjálfgefið bókunarsnið fyrir fyrirframgreiðslur. Fyrir frekari upplýsingar, sjá [Fyrirframgreiðslur viðskiptavina](customer-prepayments.md).

Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð á síðunni **Skilgreiningar færslubókana**. Bókunarskilgreiningar eru notaðar í stað bókunarsniða til að stjórna bókun viðskiptavinafærslur í fjárhag. Frekari upplýsingar eru í [Bókunarskilgreiningar](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Stofnun Bókunarregla
Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni. Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu. Við bókunarferli er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi:

| Lykilkóði svæðisgildið | Númer lykils/Flokks svæðisgildið                | Forgangsröðun leitar |
|--------------------------|-------------------------------------------------|-----------------|
| Tafla                    | Tiltekinn viðskiptavinareikningur.                       | 1               |
| Hópur                    | Viðskiptavinarflokkur sem er úthlutað á viðskiptavininn | 2               |
| Allir                      | Autt                                           | 3               |

Ef þú vilt að allar færslur viðskiptavina hafi sama bókunarsnið skaltu setja upp aðeins eitt bókunarsnið, þar sem **Allt** er fært inn í **Reikningskóði** sviði. Tilgreindu eftirfarandi gildi til að setja upp bókunarregluna.

<table>
<thead>
<tr>
<th>Svæði</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr>
<td>Bókunarregla</td>
<td>Færið inn kóða fyrir bókunarreglu. T.d. væri hægt að útbúa tvær bókunarreglur til að fá einn lykil fyrir viðskiptavinastöður í landsgjaldmiðlinum og annan fyrir viðskiptavinastöður í erlendum gjaldmiðli. Hægt væri að kalla annan lykilinn „Lands“ og hinn „Erlendur“.</td>
</tr>
<tr>
<td>Lýsing</td>
<td>Færa skal inn lýsingu á bókunarregla. Þetta er einungis notað til að auðkenna betur bókunarregla þegar það er skoða í þessa síðu.</td>
</tr>
<tr>
<td>Kóði lykils</td>
<td>Tilgreinið hvort bókunarreglan eigi við um einstakan viðskiptavin, flokk af viðskiptavinum eða alla viðskiptavini:
<ul>
<li><b>Taflan</b> – bókunarregla á við einn viðskiptamaður. Veldu viðskiptamannareikninginn í<b>Reikningur/hópnúmer</b> sviði.</li>
<li><b>Taflan</b> – bókunarregla á við einn viðskiptavinaflokk. Veldu viðskiptavinahópinn í<b>Reikningur/hópnúmer</b> sviði.</li>
<li><b>Allt</b> – bókunarregla á við alla viðskiptavini. Látið reitinn <b>Númer lykils/flokks</b> vera autt.</li>
</ul>
</td>
</tr>
<tr>
<td>Númer lykils/flokks</td>
<td>Ef<b>Tafla</b> er valið í<b>Reikningskóði</b> reit, veldu reikningsnúmer viðskiptavinarins sem er tengdur við bókunarsniðið. Ef<b>Hópur</b> er valinn skaltu velja viðskiptavinahópinn. Ef <b>Allt</b> er valið skal skilja þenan reit eftir auðan.</td>
</tr>
<tr>
<td>Safnlykill</td>
<td>Veldu aðalreikninginn sem verður notaður sem viðskiptareikningur viðskiptakrafna fyrir viðskiptavinina sem eru tengdir við bókunarsniðið. Þessi reikningur er reikningurinn fyrir<b>Jafnvægi viðskiptavina</b> tegund færslu.</td>
</tr>
<tr>
<td>Greiðslugeta lykils fyrir greiðslur</td>
<td>Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá. Þessi reitur mun aðeins birtast ef sjóðstreymisspár eru virkjaðar.</td>
</tr>
<tr>
<td>Fyrirframgreiðslur virðisauka</td>
<td><p>Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.</p>
<p><strong>Athugið:</strong> Nota<b>Færibreytur viðskiptakrafna</b> síðu til að tilgreina færslusniðið sem er notað þegar greiðsla er merkt sem fyrirframgreiðsla.</p>
</td>
</tr>
<tr>
<td>Skuldbindingar vegna afsláttarlykils</td>
<td>Veljið Fjárhagslyklar fyrir afsláttarskuldbindingar.</td>
</tr>
<tr>
<td>Innheimtubréfaröð</td>
<td>Veljið kennimerki innheimtubréfaraðar fyrir viðskiptavini sem bókunarreglan tengist.</td>
</tr>
<tr>
<td>Vaxtakóði</td>
<td>Veljið vaxtakóði til að nota fyrir útreikninga vaxta fyrir viðskiptavini sem bókunarreglan tengist.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Setja inn dæmi

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðalreikningum og lýsingum. The **Debet/kredit** dálkurinn gefur til kynna hvort færslan er venjulega debet eða kredit eða í sumum tilfellum getur bókað annað hvort. The **Hreinsunarreikningur** dálkurinn gefur til kynna að bókunartegundin sé jöfnunarreikningur. Þetta þýðir að upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð. 

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Staða viðskiptavinar | 130100 | Viðskiptakröfur | Eign | Bæði | Nr. | Tilgreindu reikninginn í **Yfirlitsreikningur** sviði.|
| Ekkert | 110110 | Bankareikningur | Eign | Bæði | Nr. | Tilgreindu aðalreikninginn í **Lausafjárreikningur fyrir greiðslur** sviði. Þessi reikningur er ekki notaður til að birta. Það er aðeins notað til að spá fyrir um sjóðstreymi. |
| Fyrirframgreiðslur virðisauka | 202900 | Afgreiðsla söluskatts | Bótaábyrgð | Bæði | Já | Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur. |
| Skuldbindingar vegna afsláttarlykils | 250600 | Frestað tekjur og afslættir | Bótaábyrgð | Bæði | Já | Veljið fjárhagsreikning fyrir skuldir afslætti.|     

### <a name="table-restrictions"></a>Töflutakmarkanir

Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út. Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.

Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :

| Reitur                 | Lýsing                                           |
|-----------------------|-------------------------------------------------------|
| Jöfnun        | Veljið þessa víxlun til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu. Ef þessi rofi er hreinsaður verður þú að jafna færslur handvirkt með því að nota **Gerðu upp opin viðskipti** síðu eða **Sláðu inn greiðslur viðskiptavina** síðu. |
| Áhugasvið          | Veldu þessa víxlun eigi að reikna vexti á útistandandi skuldum fyrir viðskiptavinalykill með þessum forstillingum. Ef víxlunin er hreinsaður, munu vextir ekki vera reiknaðir fyrir þessa viðskiptavini.                                           |
| Innheimtubréf | Veldu þessa víxlun eigi innheimtubréf að vera myndað fyrir viðskiptavinalykill með þessum forstillingum. Ef víxlunin er hreinsaður, munu innheimtubréf ekki vera mynduð fyrir þessa viðskiptavini.                                                 |
| Loka             | Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar. Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.             |



Frekari upplýsingar, sjá [Yfirlit yfir greiðslur viðskiptavinar](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
