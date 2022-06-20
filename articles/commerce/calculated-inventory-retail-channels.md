---
title: Reikna tiltækar birgðir fyrir smásölurásir
description: Þessi grein lýsir því hvernig fyrirtæki getur notað Microsoft Dynamics 365 Commerce til að skoða áætlað framboð á vörum á netinu og í verslunum.
author: hhainesms
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 952acf4cc26815822436bb7a5117775a5f12200c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884112"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Reikna tiltækar birgðir fyrir smásölurásir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig fyrirtæki getur notað Microsoft Dynamics 365 Commerce til að skoða áætlað framboð á vörum á netinu og í verslunum.

## <a name="accuracy-of-inventory-availability"></a>Nákvæmni birgða til ráðstöfunar

Commerce notar marga netþjóna og gagnagrunna til að tryggja sveigjanleika og afköst. Þess vegna er mikilvægt að þú skiljir að fyrirliggjandi birgðagildi sem eru gefin í gegnum sölustaðarforritið (POS), forritsviðmót forritaskila fyrir rafræn viðskipti eru (API) og birgðasíðurnar á staðnum í Commerce Headquarters eru hugsanlega ekki 100 prósent nákvæm í rauntíma. Ef færslur sem eru stofnaðar fyrir afurðir í net- eða verslunarásinni hafa ekki enn verið samstilltar við höfuðstöðvar, þá geta lagerbirgðasíðurnar í höfuðstöðvum ekki sýnt nákvæmt raunverulegt birgðagildi í rauntíma fyrir þessar afurðir. Hins vegar, ef þú stillir fyrirtæki þitt þannig að notendur í Headquarters eða önnur samþætt forrit geti selt, tekið á móti, skilað eða á annan hátt stillt birgðir út úr verslun eða vöruhúsi á netinu, þá gæti POS eða netrás ekki haft allar upplýsingar sem þarf til að sýna nákvæm raungildi fyrir vörur.

Mikilvægt er að skilja að öll gögn um framboð á lager, sem eru afhent á rekstrardeginum, eru talin áætlað gildi. Þess vegna, ef þú reynir að bera lagerbirgðaupplýsingarnar sem forritið veitir saman við raunverulegar efnislegar birgðir í hillunum, eða ef þú reynir að bera lagergildin sem eru sýnd í POS saman við gögnin sem þú finnur fyrir sama vöruhús í Headquarters gætu gildin verið mismunandi. Þess er vænst að þessi munur verði á rekstrardeginum og ætti ekki að líta á hann sem vandamál. Ef þú vilt gera úttekt á gögnum og ganga úr skugga um að gildin sem eru gefin á sölustöðum, API og höfuðstöðvum passi við raunverulegar efnislega einingar sem eru í hillum verslana þinna eða vöruhúsa, er besti tíminn til að gera það eftir að rásaraðgerðum er lokið fyrir daginn og allar færslur hafa verið samstilltar rétt milli höfuðstöðva og rásanna.

## <a name="channel-side-inventory-calculation"></a>Birgðaútreikningur rásarmegin

Birgðabirgðaútreikningur rásarmegin er aðferð sem tekur síðustu þekktu birgðagögn rásar í Commerce Headquarters sem grunnlínu og tekur síðan til greina frekari birgðabreytingar sem gerðust rásarmegin sem eru ekki í þeirri grunnlínu til að reikna út áætlaðar lagerbirgðir nálægt rauntíma. 

Eftirfarandi birgðabreytingar eru sem stendur teknar til greina í reiknireglu birgða rásarmegin:

- Birgðir seldar í gegnum staðgreiðslupantanir í verslun
- Birgðir seldar í gegnum pantanir viðskiptavina í verslun eða netrás
- Birgðum skilað í verslun
- Birgðir uppfylltar (sækja, pakka, senda) hjá vöruhúsi verslunar

Til að nota birgðaútreikning rásar þarftu að virkja eiginleikann **Útreikningur á ákjósanlegu vöruframboði**.

Ef Commerce-umhverfið þitt er í útgáfu **10.0.8 til 10.0.11** skaltu fylgja þessum skrefum.

1. Í Commerce Headquarters skal fara í **Smásala og viðskipti** \> **Samnýttar viðskiptafæribreytur**.
1. Í flipanum **Birgðir**, í reitnum **Vinnsla vöruframboðs**, skal velja **Nota fínstillt ferli fyrir vinnslu vöruframboðs**.

Ef Commerce-umhverfið þitt er í útgáfu **10.0.12 eða nýrri** skaltu fylgja þessum skrefum.

1. Í Commerce Headquarters skal fara í **Vinnusvæði \> Eiginleikastjórnun** og virkja eiginleikann **Útreikningur á ákjósanlegu vöruframboði**.
1. Ef net- og verslunarrásir nota sömu vöruhús vegna uppfyllingar þarf einnig að virkja eiginleikann **Bætt regla birgðaútreiknings í rás rafrænna viðskipta**. Þannig mun regla rásar varðandi útreikningar taka tillit til óbókaðra færslna sem eru stofnaðar í rás verslunar. (Þessar færslur geta verið staðgreiðslufærslur, viðskiptavinafærslur og skil.)
1. Keyrðu vinnsluna **1070** (**Stilling rásar**).

Ef Commerce-umhverfið þitt var uppfært úr útgáfu sem er eldri en útgáfa 10.0.8 af Commerce, þarftu eftir að hafa virkjað eiginleikann **Útreikningur á ákjósanlegu vöruframboði** einnig að keyra **Frumstilla verkraðara viðskipta** svo eiginleikinn taki gildi. Til að keyra frumstillinguna skal fara í **Smásala og viðskipti** \> **Uppsetning höfuðstöðva** \> **Commerce-verkraðari**.

Til að nota birgðaútreikning rásarmegin er sett skilyrði um að það þurfi að senda reglubundna skyndimynd af birgðagögnum úr höfuðstöðvum, sem vinnslan **Afurðaframboð** stofnar, til gagnagrunna rása. Skyndimyndin táknar upplýsingarnar sem Headquarters hafa um framboð birgða fyrir ákveðna samsetningu afurðar eða afurðaafbrigða og vörugeymsla. Hún inniheldur aðeins birgðafærslur sem voru unnar og birtar í höfuðstöðvum á þeim tíma þegar skyndimyndin var tekin og hún er hugsanlega ekki 100 prósent nákvæm í rauntíma vegna stöðugrar úrvinnslu á sölu sem gerist á dreifðum þjónum.

- Ef birgðir voru seldar fyrir afurð í verslun með staðgreiðslu og ósamhæfri pöntunarsölu viðskiptavina í POS-forritinu, munu Headquarters ekki strax hafa upplýsingar um tengda birgðaútgáfufærslu fyrir söluna. Headquarters mun hafa upplýsingar um birgðirnar sem eru seldar fyrir þessar gerðir af sölu verslana aðeins eftir að P-vinnslan hefur hlaðið upp tengdum færslum úr rásagagnagrunni verslunarinnar í Headquarters og tengdar sölupantanir eru búnar til með yfirlýsingu eða með því að senda bókun með hlutastraum. Ferlið við að búa til pantanir í Headquarters skapar tengdar birgðafærslur. 
- Fyrir pantanir með rafræn viðskipti, hefur Headquarters upplýsingar um birgðafærslur aðeins eftir að viðskiptin eru send til Headquarters í gegnum P-starfið og samstillingarferli pöntunarinnar er lokið.

Fylgdu þessum skrefum til að taka mynd af birgðum í Commerce Headquarters.

1. Farðu í **Retail og Commerce \> Upplýsingatækni smásölu og viðskipta \> Afurðir og birgðir \> Tiltækar afurðir**.
1. Veldu **Í lagi** til að keyra vinnsluna **Tiltækar afurðir**. Einnig er hægt að setja þetta verk í runukeyrslu.

Þegar vinnslan **Afurðaframboð** hefur lokið keyrslu verður að ýta gögnunum sem voru sótt í gagnagrunna rása e-Commerce svo að hægt sé að taka nýjustu skyndimynd af birgðum höfuðstöðva með í reikninginn í útrekningi á áætluðum lagerbirgðum.

Fylgið eftirfarandi skrefum til að samstilla skjámyndagögn frá höfuðstöðvum við rásgagnasafn.

1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Keyrðu vinnsluna **1130** (**Afurðaframboð**) til að samstilla skyndimyndargögnin sem vinnslan **Afurðaframbið** stofnaði úr höfuðstöðvum í rásagagnagrunna þína.

## <a name="inventory-availability-apis-for-e-commerce"></a>API fyrir birgðaframboð rafrænna viðskipta

Commerce veitir eftirfarandi API fyrir aðstæður rafrænna viðskipta til að spyrjast fyrir um birgðaframboð afurðar:

- **GetEstimatedAvailability** – Notaðu þetta API til að spyrjast fyrir um afurð eða afurðarafbrigði í vöruhúsi eða vöruhúsum netrásar sem eru tengd við uppfyllingarflokk netrásar.
- **GetEstimatedProductWarehouseAvailability** – Notaðu þetta API til að spyrjast fyrir um afurð eða afurðarafbrigði úr tilteknu vöruhúsi.

> [!NOTE]
> Þessi API koma í staðinn fyrir **GetProductAvailabilities** og **GetAvailableInventoryNearby** API í Commerce-útgáfu 10.0.7 og eldri.

Bæði API nota útreikningsreglu rásarmegin og skila áætluðu **tiltæku raunmagni**, **tiltæku heildarmagni**, **mælieiningu** og **birgðastöðu** fyrir umbeðna afurð og vöruhús. Hægt er að sýna gildin á e-Commerce vefsvæðinu þínu ef þú vilt, eða þau geta verið notuð til að kalla fram önnur viðskiptarök á e-Commerce vefsíðunni þinni. Til dæmis er hægt að koma í veg fyrir kaup á vörum með birgðastigi sem er „ekki til á lager“.

Þrátt fyrir að önnur API sem eru fáanleg Commerce geti farið beint í höfuðstöðvar til að sækja lagermagn af afurðum, mælum við ekki með að þau séu notuð í rafrænu viðskiptaumhverfi vegna hugsanlegra vandamál með afköst og áhrifa sem þessar tíðu beiðnir geta haft á netþjóna höfuðstöðva. Auk þess, með útreikning rásarmegin, geta bæði API hér að ofan gefið upp nákvæmara mat á afurðaframboði með því að taka til greina færslurnar sem eru búnar til í rásunum sem höfuðstöðvarnar vita ekki af.

Til að skilgreina hvernig skila á afurðarmagni í úttaki API skal fylgja þessum skrefum.

1. Opnið **Smásala og viðskipti \> Uppsetning höfuðstöðva \> færibreytur \> Viðskiptafæribreytur**.
1. Veljið flipann **Birgðir** og stillið síðan í flýtiflipanum **API fyrir birgðaframboð rafrænna viðskipta** skal skilgreina gildið fyrir stillinguna **Magn í úttaki API**.
1. Keyrið vinnsluna **1070** (**Skilgreining rásar**) til að samstilla síðustu stillingu við rásir.

Stillingin **Magn í úttaki API** býður upp á þrjá valmöguleika:

- **Birgðamagn skilavöru** - Efnislegt magn til ráðstöfunar og heildarmagn til ráðstöfunar af umbeðinni afurð er skilað í úttaki API.
- **Birgðamagn skilavöru að frádregnu birgðabiðminni** - Skilað magn í úttaki API er lagað með því að draga frá gildi birgðabiðminnis. Frekari upplýsingar um birgðabiðminnið má finna í [Stilla birgðabiðminni og birgðastöðu](inventory-buffers-levels.md).
- **Ekki birgðamagn skilavöru** - Aðeins birgðastöðu skilað í úttaki API. Frekari upplýsingar um birgðastöður má finna í [Stilla birgðabiðminni og birgðastöður](inventory-buffers-levels.md).

Hægt er að nota `QuantityUnitTypeValue` API-færibreytuna til að tilgreina gerð einingar sem API á að skila magni í. Þessi færibreyta styður valkostina **birgðaeining** (sjálfgefið), **innkaupaeining** og **sölueining**. Skilað magn er sléttað að skilgreindri nákvæmni tilheyrandi mælieiningar í höfuðstöðvum.

**GetEstimatedAvailability** API býður upp á eftirfarandi inntaksfæribreytur til að styðja mismunandi aðstæður fyrirspurna:

- `DefaultWarehouseOnly` - Notaðu þessa færibreytu til að spyrja birgðir um afurð í sjálfgefnu vöruhúsi netrásar. 
- `FilterByChannelFulfillmentGroup` og `SearchArea` - Notaðu þessar tvær færibreytur til að spyrjast fyrir í birgðum um afurð á öllum afhendingarstöðum innan tiltekins leitarsvæðis samkvæmt `longitude`, `latitude` og `radius`. 
- `FilterByChannelFulfillmentGroup` og `DeliveryModeTypeFilterValue` - Notaðu þessar tvær færibreytur til að spyrjast fyrir í birgðum um afurð frá tilteknum vöruhúsum sem eru tend við uppfyllingarflokk netrásar og eru stillt til að styðja ákveðna afhendingarmáta. Færibreytan `DeliveryModeTypeFilterValue` styður valkostina **allt** (sjálfgefið), **sending** og **sótt**. Í aðstæðum þar sem t.d. er hægt að uppfylla netpöntun frá mörgum vöruvöruhúsum er hægt að nota þessar tvær breytur til að spyrja um birgðir vörunnar í öllum þessum vöruhúsum. API skilar í þessu tilviki lagerbirgðum og birgðastöðu afurðar í hverju afhendingarvöruhúsi fyrir sig, ásamt samanlögðu magni og samanlagðri birgðastöðu frá öllum sendingarvöruhúsum í umfangi fyrirspurnar.
 
Einingarnar kaupgluggi, verslunarval, óskalisti, karfa og körfutákn í Commerce nota API og færibreytur sem minnst er á að ofan til að sýna skilaboð um birgðastöðu yfir allt svæði rafrænna viðskipta. Vefsmiður Commerce býður upp á ýmsar birgðastillingar til að stýra markaðssetningu og innkaupahegðun. Nánari upplýsingar er að finna í [Nota birgðastillingar](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Birgðauppfletting sölustaðar með útreikning rásar

Í Commerce útgáfu 10.0.9 og eldri, notaði aðgerðin **Birgðauppfletting** úr POS notaði rauntíma þjónustuksll í Headquarters til að fá birgðaupplýsingar fyrir valda afurð, bæði fyrir núverandi verslun notandans og allar aðrar verslanir sem eru stilltar fyrir uppfyllingarhópinn sem hluta af rásarstillingu fyrir verslunina. Í Commerce-útgáfu 10.0.10 og nýrri er hægt að slökkva á þjónustuköllum til höfuðstöðvar í rauntíma og í staðinn nota útreikning rásar í netþjóni Commerce til að ákvarða lagerbirgðir sem eru efnislega tiltækar fyrir verslunina og alla aðra staði sem eru skilgreindur í uppfyllingarflokknum. Þessi rásarútreiknaða birgðastilling er einnig gagnleg fyrir staði þar sem internettengingin er óáreiðanleg, vegna þess að þú þarft ekki að vera á netinu til að fá úttekt á birgðum í Headquarters.

Þegar útreikningur rásarhliða er rétt stilltur og stjórnað á réttan hátt getur það gefið áreiðanlegra mat á núverandi birgðum verslunar, vegna þess að hann notar viðskiptagögnin sem eru í gagnagrunni Commerce-rásar, en Headquarters hafa ef til vill ekki ennþá upplýsingar um það. Til dæmis, ef þú notar núverandi rauntíma þjónustukall til að leita að birgðum í POS, mun Headquarters líklega ekki enn hafa upplýsingar um reiðufé og sölu sem bara átti sér stað fyrir vöru. Þess vegna mun verðmæti lagerbirgða sem Headquarters skilar fyrir þá afurð líklega fara yfir raunverulegar lagerbirgðir verslunarinnar um eina einingu. Hins vegar, ef þú notar útreikninga í rásinni er hægt að færa sölu í reiðufé inn í útreikninginn og draga frá því lagervirði sem er sýnt. Þrátt fyrir að gildin sem bæði útreikningur í rásinni og rauntíma þjónustukall veitir séu aðeins mat á lagerbirgðum er mun líklegra að gildið sem útreikningur í rásinni veitir sé rétt fyrir núverandi verslun.

Til að skilgreina aðgerðina **Birgðauppfletting** á sölustað í Commerce Headquarters til að nota útreikningsreglu rásar og slökkva á símtölum í rauntímaþjónustu þarf fyrst að virkja eiginleikann **Fínstilltur útreikningur á framboði afurðar** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters og síðan fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**.
1. Veldu virkniforstillingu.
1. Í flýtiflipanum **Aðgerðir**, í hlutanum **Útreikningur á birgðaframboði**, skal breyta gildinu fyrir **Útreikningsaðferð birgðaframboðs** úr **Rauntímaþjónusta** í **Rás**. Sjálfgefið er að allar virkniforstillingar nota rauntíma þjónustuköll. Þú verður að breyta gildi þessa reits ef þú vilt nota útreikningarök í rásinni. Þessi breyting hefur áhrif á sérhverja smásöluverslun sem er tengd við valdar virkniforstillingar.

Þá þarf að samstilla breytingarnar við rásirnar í gegnum vinnslu áætlanadreifingar í höfuðstöðvum með því að framkvæma eftirfarandi skref.

1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Keyrðu vinnsluna **1070** (**Stilling rásar**).

Þegar uppsetningunni er lokið nota upplýsingarnar sem eru veittar um efnislega tiltækar birgðir ekki lengur rauntíma þjónustukall þegar notandi í POS forritinu notar aðgerðina **Birgðauppfletting** (venjuleg og fylkissýn). Þess í stað eru gögn um efnislega tiltækar birgðir fyrir núverandi verslun og allar verslanir í uppfyllingarhópnum reiknuð út frá síðast þekktu skyndimynd sem var afhent í gagnagrunni rásarinnar úr Commerce Headquarters. Skyndimyndargildið er frekar betrumbætt með útreikningi á hliðarásinni til að aðlaga líkamlega tiltækt gildi, byggt á viðbótar sölu- eða skilafærslum sem eru fyrir hendi fyrir valda vöru í gagnagrunni rásarinnar sem voru ekki með í síðustu samstilltu skyndimynda úr 1130 starfinu. Ef rásagagnagrunnurinn hefur ekki að geyma færslugögn fyrir nein vöruhús eða verslanir í uppfyllingarhópnum inniheldur hann engar viðbótarfærslur sem hægt er að taka með í endurútreikning á gildi. Þess vegna er besta matið á lagerbirgðum sem hægt er að sýna fyrir þessi vöruhús eða verslanir eru gögnin úr síðustu þekktu skyndimynd Commerce Headquarters.

Skjáirnir **Uppfylling pöntunar** í POS nýta einnig útreikning í rás til að sýna lagerbirgðir fyrir vörur þegar uppfyllingarlína pöntunar er valin og notandi skoðar spjaldið **Upplýsingar** fyrir lagerbirgðir fyrir valda vöru.

## <a name="optimize-your-inventory-data"></a>Fínstilltu birgðir þínar

Til að tryggja besta mögulega mat á birgðum er mikilvægt að þú notir eftirfarandi runuvinnslur Commerce og keyrir þær oft:

- **P-starf** - P-starfið er að finna á síðunni **Dreifingaráætlanir** og ætti að keyra oft. Þessi vinnsla færir pantanir, ósamstilltar pantanir viðskiptavina sem POS bjó til og staðgreiddar pantanir í e-Commerce sem POS stofnaði úr rásagagnagrunnunum í Commerce Headquarters, svo hægt sé að vinna úr þeim frekar. Þar til þessi gögn eru samstillt úr rásinni í Commerce Headquarters, hafa Commerce Headquarters engar upplýsingar um birgðaleiðréttingar á afurðum í vöruhúsunum sem leiða af þeim færslum.
- **Samstilla pantanir** - Þessi vinnsla keyrir hrá færslugögn í Commerce Headquarters sem P-vinnslan veitir og breytir færslum e-Commerce og ósamstilltum pöntunarfærslum viðskiptavina í sölupantanir í Commerce Headquarters. Þar til þessi vinnsla hefur keyrt og sölupantanir eru búnar til eru engar birgðafærslur stofnaðar. Þess vegna munu lagerbirgðir í Commerce Headquarters ekki taka tillit til færslanna.
- **Reikna færsluuppgjör í runu** - Fyrir staðgreiddar færslur sem eru stofnaðar í versluninni tryggir bókunarferli með hlutastraum að birgðir sem eru tengdar sölu eru uppfærðar á skilvirkan hátt. Til að fá sem skilvirkasta vinnslu á birgðafærslum fyrir staðgreiddar pantanir skaltu gæta þess að stilla kerfið til að nota [bókun með hlutastraum](./trickle-feed.md).
- **Bóka færsluuppgjör í runu** - Þessi vinnsla er einnig nauðsynleg fyrir bókun með hlutastraum. Hún fylgir vinnslunni **Reikna færsluuppgjör í runu**. Þessi vinnsla bókar kerfisbundið reiknuð yfirlit, svo að sölupantanir vegna staðgreiddrar sölu eru stofnaðar í Commerce Headquarters og Commerce Headquarters endurspeglar birgðir verslunarinnar á nákvæmari hátt.
- **Tiltækar afurðir** - Þessi vinnsla skapar mynd af birgðum úr Commerce Headquarters.
- **1130 (Tiltækar afurðir)** - Þessa vinnslu er að finna á síðunni **Dreifingaráætlanir** og ætti að keyra strax á eftir vinnslunni **Tiltækar afurðir**. Þessi vinnsla flytur skyndimynd birgða úr Commerce Headquarters yfir í gagnagrunna rásarinnar.

> [!NOTE]
> - Það er góð venja að keyra verkin **Afurðaframboð** og **1130** á klukkutímafresti og tímasetja P-verk, samstilla pantanir og verk sem tengjast bókun með hlutastraumi með sömu eða hærri tíðni.
> - Af frammistöðuástæðum, þegar útreikningar á birgðahlið framboðs eru notaðir til að leggja fram beiðni um birgðaaðstoð með því að nota API fyrir e-Commerce eða POS birgðastöðvar við hlið rásar, notar útreikningurinn skyndiminni til að ákvarða hvort nægur tími hafi liðið til að réttlæta að keyra útreikninga rökfræðinnar aftur. Sjálfgefið skyndiminni er stillt á 60 sekúndur. Til dæmis kveiktir þú á útreikningi á rásarhlið fyrir verslunina þína og skoðaðir lagerbirgðir fyrir vöru á síðunni **Birgðauppfletting**. Ef ein eining vörunnar er síðan seld, mun síðan **Birgðauppfletting** ekki sýna minnkaðan lager fyrr en skyndiminni hefur verið hreinsað. Eftir að notendur bókað færslur í POS ættu þeir að bíða í 60 sekúndur áður en þeir staðfesta að lagerbirgðir hafi verið skertar.

Ef viðskiptasvið þitt þarfnast minni skyndiminnistíma skaltu hafa samband við stuðningsfulltrúa þinn til að fá hjálp.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
