---
title: Bókunarreglur viðskiptavina
description: Þessi grein útskýrir bókunarreglur viðskiptavina sem stjórna bókun á færslum viðskiptavina í fjárhaginn.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891696"
---
# <a name="customer-posting-profiles"></a>Bókunarreglur viðskiptavina

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir bókunarreglur viðskiptavina sem stjórna bókun á færslum viðskiptavina í fjárhaginn.

## <a name="customer-posting-profiles"></a>Bókunarreglur viðskiptavina

Bókunarreglur viðskiptavina gera þér kleift að úthluta fjárhagslyklum og skjalastillingum á alla viðskiptavini, hóp af viðskiptavinum eða einn viðskiptavin. Þessar stillingar verða notaðar þegar reikningar sölupöntunar eru búnir til, reikningar með frjálsum texta, verkreikningar, greiðslubækur, innheimtubréf og vaxtanótur. 

Sjálfgefin bókunarregla er skilgreind í flipanum **Fjárhagur og virðisaukaskattur** á síðunni **Færibreytur viðskiptakrafna**. Hún er síðan sjálfkrafa höfð með í hausnum og nýjum skjölum. Þú getur breytt þessu þar ef þú þarft að setja inn aðra notandalýsingu. 

Fyrirtæki sem samþykkja fyrirframgreiðslur frá viðskiptavinum skilgreina oft aðra bókunarreglu fyrir fyrirframgreiðslur og tengja hana í færibreytunum sem sjálfgefna bókunarreglu fyrir fyrirframgreiðslur. Frekari upplýsingar er að finna í [Fyrirframgreiðslur viðskiptavinar](customer-prepayments.md).

Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð á síðunni **Skilgreiningar færslubókana**. Bókunarskilgreiningar eru notaðar í staðinn fyrir bókunarreglur til að stjórna bókun viðskiptavinafærslna í fjárhaginn. Frekari upplýsingar eru í [Bókunarskilgreiningar](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Stofnun Bókunarregla
Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni. Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu. Við bókunarferli er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi:

| Lykilkóði svæðisgildið | Númer lykils/Flokks svæðisgildið                | Forgangsröðun leitar |
|--------------------------|-------------------------------------------------|-----------------|
| Tafla                    | Tiltekinn viðskiptavinareikningur.                       | 1               |
| Flokkur                    | Viðskiptavinarflokkur sem er úthlutað á viðskiptavininn | 2               |
| Allir                      | Autt                                           | 3               |

Ef allar viðskiptavinafærslur eiga að vera með sömu bókunarregluna skal aðeins setja upp eina bókunarreglu þar sem **Allt** er fært inn í reitinn **Kóði lykils**. Tilgreindu eftirfarandi gildi til að setja upp bókunarregluna.

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
<li><b>Taflan</b> – bókunarregla á við einn viðskiptamaður. Veljið viðskiptavinalykil í reitnum <b>Númer lykils/flokks</b>.</li>
<li><b>Taflan</b> – bókunarregla á við einn viðskiptavinaflokk. Veljið viðskiptavinaflokk í reitinn <b>Númerareit lykils/flokks</b>.</li>
<li><b>Allt</b> – bókunarregla á við alla viðskiptavini. Látið reitinn <b>Númer lykils/flokks</b> vera autt.</li>
</ul>
</td>
</tr>
<tr>
<td>Númer lykils/flokks</td>
<td>Ef <b>Tafla</b> er valin í svæðinu <b>Lykilkóði</b> veljið þá lykilnúmer viðskiptavinar sem er tengdur við bókunarregluna. Ef <b>Flokkur</b> er valinn skal velja flokk viðskiptavina. Ef <b>Allt</b> er valið skal skilja þenan reit eftir auðan.</td>
</tr>
<tr>
<td>Safnlykill</td>
<td>Veldu aðallykilinn sem verður notaður sem viðskiptalykill viðskiptakrafna fyrir viðskiptavini sem tengjast bókunarreglunni. Þessi reikningur er reikningurinn fyrir <b>Staða viðskiptamanns</b> bókunargerð.</td>
</tr>
<tr>
<td>Greiðslugeta lykils fyrir greiðslur</td>
<td>Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá. Þessi reitur birtist aðeins ef sjóðsstreymisspár eru virkjaðar.</td>
</tr>
<tr>
<td>Fyrirframgreiðslur virðisauka</td>
<td><p>Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.</p>
<p><strong>Athugaðu:</strong> Notaðu síðuna <b>Færibreytur viðskiptakrafna</b> til að tilgreina bókunarregluna sem verður notuð þegar greiðsla er merkt sem fyrirframgreiðsla.</p>
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

## <a name="posting-examples"></a>Dæmi um bókanir

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðallyklum og lýsingum. Dálkurinn **Debet/kredit** gefur til kynna hvort færslan sé yfirleitt debet eða kredit eða í sumum tilfellum er hægt að bóka annað hvort. Dálkurinn **Millireikningur** gefur til kynna hvort bókunargerðin sé millireikningur. Þetta þýðir að upphæðin sem er birt á þessum reikningi er sjálfkrafa afturkölluð þegar seinni færsla er bókuð. 

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/kredit | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Staða viðskiptavinar | 130100 | Viðskipti viðskiptakrafna | Eign | Bæði | Nr. | Tilgreindu lykilinn í reitnum **Safnlykill**.|
| Ekkert | 110110 | Bankareikningur | Eign | Bæði | Nr. | Tilgreindu aðallykilinn í reitnum **Greiðslugetulykill fyrir greiðslur**. Þessi reikningur er ekki notaður fyrir bókanir. Það er aðeins notað fyrir sjóðstreymisspá. |
| Fyrirframgreiðslur virðisauka | 202900 | Jöfnun virðisaukaskatts | Bótaábyrgð | Bæði | Já | Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur. |
| Skuldbindingar vegna afsláttarlykils | 250600 | Frestaðar tekjur og afslættir | Bótaábyrgð | Bæði | Já | Veljið Fjárhagslyklar fyrir afsláttarskuldbindingar.|     

### <a name="table-restrictions"></a>Töflutakmarkanir

Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út. Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.

Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :

| Reitur                 | Lýsing                                           |
|-----------------------|-------------------------------------------------------|
| Jöfnun        | Veljið þessa víxlun til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu. Ef þessi víxlun er tóm þarftu að jafna færslur handvirkt með því að nota síðuna **Jafna opnar færslur** eða síðuna **Færa inn greiðslur viðskiptavina**. |
| Áhugasvið          | Veldu þessa víxlun eigi að reikna vexti á útistandandi skuldum fyrir viðskiptavinalykill með þessum forstillingum. Ef víxlunin er hreinsaður, munu vextir ekki vera reiknaðir fyrir þessa viðskiptavini.                                           |
| Innheimtubréf | Veldu þessa víxlun eigi innheimtubréf að vera myndað fyrir viðskiptavinalykill með þessum forstillingum. Ef víxlunin er hreinsaður, munu innheimtubréf ekki vera mynduð fyrir þessa viðskiptavini.                                                 |
| Loka             | Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar. Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.             |



Frekari upplýsingar, sjá [Yfirlit yfir greiðslur viðskiptavinar](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
