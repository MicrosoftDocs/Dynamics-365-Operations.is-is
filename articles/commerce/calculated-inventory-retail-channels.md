---
title: Reiknið birgðir til ráðstöfunar fyrir smásölurásir
description: Þetta efni lýsir þeim valkostum sem eru í boði til að sýna lagerbirgðir fyrir verslunina og netrásirnar.
author: hhainesms
manager: annbe
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: de4ee98198f441b8f42a8a55aa5ff1015f485234
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413146"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Reiknið birgðir til ráðstöfunar fyrir smásölurásir

[!include [banner](../includes/banner.md)]

Þetta efni lýsir því hvernig fyrirtæki getur notað Microsoft Dynamics 365 Commerce til að skoða áætlað framboð á vörum á netinu og verslunarrásum.

## <a name="accuracy-of-calculation"></a>Nákvæmni útreikninga

Commerce notar marga netþjóna og gagnagrunna til að tryggja sveigjanleika og afköst. Þess vegna er mikilvægt að þú skiljir að fyrirliggjandi birgðagildi sem eru gefin í gegnum sölustaðarforritið (POS), forritsviðmót forritaskila fyrir rafræn viðskipti eru (API) og birgðasíðurnar á staðnum í höfuðstöðvum viðskiptaráðs eru hugsanlega ekki 100 prósent nákvæm í rauntíma. Ef færslur sem eru stofnaðar fyrir afurðir í net- eða verslunarásinni hafa ekki enn verið samstilltar við miðlara og gagnagrunn Commerce Headquarters, þá geta lagerbirgðasíðurnar í Commerce Headquarters ekki sýnt nákvæmt raunverulegt birgðagildi í rauntíma fyrir þessar afurðir. Hins vegar, ef þú stillir fyrirtæki þitt þannig að notendur í Commerce Headquarters eða önnur samþætt forrit geti selt, tekið á móti, skilað eða á annan hátt stillt birgðir út úr verslun eða vöruhúsi á netinu, þá gæti POS eða netrás ekki haft allar upplýsingar sem þarf til að sýna nákvæmt rauntímalagerbirgðagildi fyrir vörur.

Þetta efni útskýrir samstillingarferla gagna sem hægt er að keyra oft til að hjálpa til við að takmarka biðtíma gagna milli forrita eða rása. Hins vegar er mikilvægt að þú hafir skilning á því að öll gögn um framboð á lager, sem eru afhent á rekstrardeginum, eru talin áætlað gildi. Þess vegna, ef þú reynir að bera lagerbirgðaupplýsingarnar sem forritið veitir saman við raunverulegar efnislegar birgðir í hillunum, eða ef þú reynir að bera lagergildin sem eru sýnd í POS saman við gögnin sem þú finnur fyrir sama vöruhús í Commerce Headquarters gætu gildin verið mismunandi. Þess er vænst að þessi munur verði á rekstrardeginum og ætti ekki að líta á hann sem vandamál. Ef þú vilt gera úttekt á gögnum og ganga úr skugga um að gildin sem eru gefin í API fyrir birgðaframboð og Commerce Headquarters passi við raunverulegar efnislega einingar sem eru í hillum verslana þinna eða vöruhúsa, er besti tíminn til að gera það eftir að rásaraðgerðum er lokið fyrir daginn og allar færslur hafa verið samstilltar rétt milli Commerce Headquarters og rásarinnar.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Notaðu API birgðauppflettingar til að fá beiðnir um birgðahald vegna rafrænna viðskipta

Þú getur notað eftirfarandi API til að sýna framboð birgða fyrir afurð þegar viðskiptavinir þínir eru að versla á e-verslunarsíðu.

- **GetEstimatedAvailability** – Notið þetta API til að sækja birgðaframboð fyrir vöruna í rafrænni viðskiptarás vöruhúss eða í öllum vöruhúsum sem eru tengd við skilgreiningu uppfyllingarflokksins fyrir rafrænar viðskiptarásir. Einnig er hægt að nota þetta API fyrir vöruhús á tilteknu leitarsvæði eða radíus, byggt á lengdar- og breiddargráðum.
- **GetEstimatedProductWarehouseAvailability** – Notaðu þetta API til að biðja birgðir um vöru úr tilteknu vöruhúsi. Til dæmis er hægt að nota það til að sýna framboð birgða í atburðarásum sem fela í sér pöntunarupptöku.

> [!NOTE]
> Þessi API skipta út **GetProductAvailabilities** og **GetAvailableInventoryNearby** API í Dynamics 365 Retail útgáfu 10.0.7 og yngri.

Bæði API sækja gögn frá Commerce-miðlaranum og veita mat á lagerbirgðum fyrir tiltekna samsetningu vöru eða vöruafbrigða og vörugeymslu. Þrátt fyrir að önnur API sem eru fáanleg á Commerce-miðlinum geti farið beint í Commerce Headquarters til að sækja lagermagn af afurðum, mælum við ekki með að þau séu notuð í rafrænu viðskiptaumhverfi vegna hugsanlegra afkomuvandamála og tengdra áhrifa sem þessar tíðar beiðnir geta haft á netþjónum Commerce Headquarters. Að auki, ef lagerbirgðir eru reiknaðar út með Commerce-miðlaranum, er líklegra að útreikningurinn innihaldi birgðir sem seldar voru í nýlegum færslum e-Commerce sem hafa ekki enn verið samstilltar við Commerce Headquarters. Þó að Commerce Headquarters hafi hugsanlega ekki upplýsingar um þessar færslur, þá eru Commerce-miðlarinn og gagnagrunnur rásanna með gögnin. Þess vegna verða gögnin tekin með og geta hjálpað til við að fá nákvæmara mat á tiltækum birgðum afurðar.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Byrjaðu með reiknuðum birgðum til ráðstöfunar í e-Commerce

Áður en hægt er að nota þau tvö API sem minnst var á áður verður að virkja eiginleikann **Fínstilltur útreikningur á framboði afurðar** í gegnum vinnusvæðið **Eiginleikastjórnun** í Commerce Headquarters.

Áður en API geta reiknað besta mat á birgðum til ráðstöfunar fyrir vöru, verður að vinna reglulega skyndimynd af birgðaframboði frá Commerce Headquarters og senda í rásagagnagrunninn sem Commerce Scale Unit fyrir e-Commerce notar. Skyndimyndin táknar upplýsingarnar sem aðalstöðvar Commerce hafa um framboð birgða fyrir ákveðna samsetningu afurðar eða afurðaafbrigða og vörugeymsla. Það getur falið í sér birgðaleiðréttingar eða -hreyfingar sem orsakast af innhreyfingum birgða eða af sendingum eða öðrum ferlum sem eru framkvæmdir í Commerce Headquarters og að rás e-Commerce hafi aðeins upplýsingar um vegna samstillingarferilsins.

Skyndimynd gagnagrunnsins sem vinnslan **Tiltækar afurðir** skapar reiknar aðeins út birgðafærslurnar sem voru unnar og bókaðar í Commerce Headquarters á þeim tíma þegar skyndinmyndin var gerð. Ef birgðir voru seldar fyrir afurð í vöruhúsi með staðgreiðslu og ósamhæfri pöntunarsölu viðskiptavina í POS-forritinu, munu Commerce Headquarters ekki strax hafa upplýsingar um tengda birgðaútgáfufærslu fyrir söluna. Það mun hafa upplýsingar um birgðirnar sem eru seldar fyrir þessar gerðir af sölu verslana aðeins eftir að P-vinnslan hefur hlaðið upp tengdum færslum úr rásagagnagrunni verslunarinnar í Commerce Headquarters og tengd sölupöntun er búin til með yfirlýsingu eða með því að senda bókun með hlutastraum. Ferlið við að búa til pöntunina í Commerce Headquarters skapar tengdar birgðafærslur. Fyrir pantanir með rafræn viðskipti, hefur Commerce Headquarters upplýsingar um birgðafærslur aðeins eftir að viðskiptin eru send til Commerce Headquarters í gegnum P-starfið og samstillingarferli pöntunarinnar er lokið. Þess vegna er mikilvægt að þú skiljir að skyndimynd birgða sem er að finna í vinnslunni **Tiltækar afurðir** gæti ekki verið 100 prósent nákvæmt í rauntíma vegna stöðugrar söluvinnslu sem á sér stað á dreifðum netþjónum.

Fylgdu þessum skrefum til að taka mynd af birgðum í Commerce Headquarters.

1. Farðu í **Retail og Commerce \> Upplýsingatækni smásölu og viðskipta \> Afurðir og birgðir \> Tiltækar afurðir**.
1. Veldu **Í lagi** til að keyra vinnsluna **Tiltækar afurðir**. Þú getur líka tímasett þessa vinnslu þannig að það sé keyrt í runu.

Þegar vinnsla **Tiltækar afurðir** hefur lokið keyrslu verður að ýta gögnunum sem var náð í gagnagrunna rása e-Commerce svo að hægt sé að taka nýjustu skyndimynd birgða Commerce Headquarters með í útreikning á áætlaðar lagerbirgðir.

1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Keyrðu vinnsluna **1130** (**Tiltækar afurðir**) til að samstilla skyndimyndargögnin sem vinnslan **Tiltækar afurðir** stofnaði úr Commerce Headquarters í rásagagnagrunna þína.

Þegar beðið er um birgðaframboð úr API **GetEstimatedAvailability** eða **GetEstimatedProductWarehouseAvailability**, er útreikningur keyrður til að reyna að fá besta mögulega mat á birgðum afurðarinnar. Við útreikninginn er vísað til allra pantana viðskiptavina í e-Commerce sem eru í gagnagrunni rásarinnar en voru ekki með í skyndimyndargögnum sem 1130 vinnslan gaf upp. Þessi rök eru framkvæmd með því að rekja síðustu afgreiddu birgðafærslur úr Commerce Headquarters og bera þær saman við færslur í gagnagrunni rásarinnar. Það veitir grunnlínu fyrir útreikningsrökum á rásarhliðinni, svo að aukalegar birgðahreyfingar sem áttu sér stað vegna sölufærslna pantana viðskiptavina í gagnagrunni um rafræn viðskipti geta verið færðar inn í áætlað birgðagildi sem API veitir.

Útreikningsrök rásarinnar skilar áætluðu efnislegu gildi og heildar tiltæku gildi fyrir umbeðna vöru og vöruhús. Hægt er að sýna gildin á e-Commerce vefsvæðinu þínu ef þú vilt, eða þau geta verið notuð til að kalla fram önnur viðskiptarök á e-Commerce vefsíðunni þinni. Til dæmis er hægt að sýna skilaboð um „ekki til á lager“ í stað raunverulegs lagermagns sem API stóðst.

Útreikningsrökin sem rásarhlið á e-Commerce API notar fyrir áætlað birgðaverðmæti geta metið birgðir byggðar eingöngu á pöntunum viðskiptavina sem hafa verið búnar til í gagnagrunni rásarinnar, en sem hefur ekki enn verið samstillt og sent í Commerce Headquarters. Ef rásagagnagrunnurinn þinn inniheldur einnig færslugögn fyrir staðgreidda sölu fyrir verslunarsértæk vöruhús, er staðgreidd sala ekki tekin með í útreikning á rásarhlið e-Commerce fyrir þau vöruhús.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Stilla aðgerð birgðaleitar í POS rásinni

Í smásöluútgáfu 10.0.9 og eldri, notaði aðgerðin **Birgðauppfletting** úr POS notaði rauntíma þjónustuksll í Commerce Headquarters til að fá birgðaupplýsingar fyrir valda afurð, bæði fyrir núverandi verslun notandans og allar aðrar verslanir sem eru stilltar fyrir uppfyllingarhópinn sem hluta af rásarstillingu fyrir verslunina. Í Commerce-útgáfu 10.0.10 og nýrri er hægt að slökkva á rauntíma þjónustuköllum í Commerce Headquarters. Í staðinn getur þú notað útreikninga á hliðarás á Commerce-miðlaranum til að ákvarða lagerbirgðir sem eru efnislega tiltækar fyrir verslunina og alla aðra staði sem eru skilgreindur í uppfyllingarhópnum. Þessi rásarútreiknaða birgðastilling er einnig gagnleg fyrir staði þar sem internettengingin er óáreiðanleg, vegna þess að þú þarft ekki að vera á netinu til að fá úttekt á birgðum í Commerce Headquarters.

Þegar útreikningur rásarhliða er rétt stilltur og stjórnað á réttan hátt getur það gefið áreiðanlegra mat á núverandi birgðum verslunar, vegna þess að hann notar viðskiptagögnin sem eru í gagnagrunni Commerce-rásar, en Commerce Headquarters hafa ef til vill ekki ennþá upplýsingar um það. Til dæmis, ef þú notar núverandi rauntíma þjónustukall til að leita að birgðum í POS, munu Commerce Headquarters líklega ekki enn hafa upplýsingar um reiðufé og sölu sem bara átti sér stað fyrir vöru. Þess vegna mun verðmæti lagerbirgða sem Commerce Headquarters skilar fyrir þá afurð líklega fara yfir raunverulegar lagerbirgðir verslunarinnar um eina einingu. Hins vegar, ef þú notar útreikninga í rásinni er hægt að færa sölu í reiðufé inn í útreikninginn og draga frá því lagervirði sem er sýnt. Þrátt fyrir að gildin sem bæði útreikningur í rásinni og rauntíma þjónustukall veitir séu aðeins mat á lagerbirgðum er mun líklegra að gildið sem útreikningur í rásinni veitir sé rétt fyrir núverandi verslun.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Byrjaðu með reiknuðum birgðum til ráðstöfunar í sölustaðarrás

Til að nota útreikningsrökin fyrir rásarhlið og slökkva á símtölum rauntímaþjónustu fyrir uppflettingu birgða úr sölustaðarforritinu verður fyrst að virkja eiginleikann **Fínstilltur útreikningur á framboði afurðar** á vinnusvæðinu **Eiginleikastjórnun** í Commerce Headquarters. Til viðbótar við að virkja eiginleikann verður að gera breytingar á **Virkniregla**.

Til að breyta **Virknireglu** skal fylgja þessum skrefum:

1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**.
1. Veldu virkniforstillingu.
1. Á flýtiflipanum **Aðgerðir**, í hlutanum **Útreikningur á birgðaframboði**, breytirðu gildi í reitnum **Útreikningsaðferð birgðaframboðs** úr **Rauntímaþjónusta** í **Rás**. Sjálfgefið er að allar virkniforstillingar nota rauntíma þjónustuköll. Þess vegna verður þú að breyta gildi þessa reits ef þú vilt nota útreikningarök í rásinni. Þessi breyting hefur áhrif á sérhverja smásöluverslun sem er tengd við valdar virkniforstillingar.

Þá þarf að samstilla breytingarnar við rásina í gegnum vinnslu áætlanadreifingar með því að framkvæma eftirfarandi skref:

1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Keyrðu vinnsluna **1070** (**Stilling rásar**).

Þegar uppsetningunni er lokið nota upplýsingarnar sem eru veittar um efnislega tiltækar birgðir ekki lengur rauntíma þjónustukall þegar notandi í POS forritinu notar aðgerðina **Birgðauppfletting** (venjuleg og fylkissýn). Þess í stað eru gögn um efnislega tiltækar birgðir fyrir núverandi verslun og allar verslanir í uppfyllingarhópnum reiknuð út frá síðast þekktu skyndimynd sem var afhent í gagnagrunni rásarinnar úr Commerce Headquarters. Skyndimyndargildið er frekar betrumbætt með útreikningi á hliðarásinni til að aðlaga líkamlega tiltækt gildi, byggt á viðbótar sölu- eða skilafærslum sem eru fyrir hendi fyrir valda vöru í gagnagrunni rásarinnar sem voru ekki með í síðustu samstilltu skyndimynda úr 1130 starfinu. Ef rásagagnagrunnurinn hefur ekki að geyma færslugögn fyrir nein vöruhús eða verslanir í uppfyllingarhópnum inniheldur hann engar viðbótarfærslur sem hægt er að taka með í endurútreikning á gildi. Þess vegna er besta matið á lagerbirgðum sem hægt er að sýna fyrir þessi vöruhús eða verslanir eru gögnin úr síðustu þekktu skyndimynd Commerce Headquarters.

Skjáirnir **Uppfylling pöntunar** í POS nýta einnig útreikning í rás til að sýna lagerbirgðir fyrir vörur þegar uppfyllingarlína pöntunar er valin og notandi skoðar spjaldið **Upplýsingar** fyrir lagerbirgðir fyrir valda vöru.

## <a name="optimize-your-inventory-data"></a>Fínstilltu birgðir þínar

Til að tryggja besta mögulega mat á birgðum er mikilvægt að þú notir eftirfarandi runuvinnslur Commerce og keyrir þær oft:

- **P-starf** - P-starfið er að finna á síðunni **Dreifingaráætlanir** og ætti að keyra oft. Þessi vinnsla færir pantanir, ósamstilltar pantanir viðskiptavina sem POS bjó til og staðgreiddar pantanir í e-Commerce sem POS stofnaði úr rásagagnagrunnunum í Commerce Headquarters, svo hægt sé að vinna úr þeim frekar. Þar til þessi gögn eru samstillt úr rásinni í Commerce Headquarters, hafa Commerce Headquarters engar upplýsingar um birgðaleiðréttingar á afurðum í vöruhúsunum sem leiða af þeim færslum.
- **Samstilla pantanir** - Þessi vinnsla keyrir hrá færslugögn í Commerce Headquarters sem P-vinnslan veitir og breytir færslum e-Commerce og ósamstilltum pöntunarfærslum viðskiptavina í sölupantanir í Commerce Headquarters. Þar til þessi vinnsla hefur keyrt og sölupantanir eru búnar til eru engar birgðafærslur stofnaðar. Þess vegna munu lagerbirgðir í Commerce Headquarters ekki taka tillit til færslanna.
- **Reikna færsluuppgjör í runu** - Fyrir staðgreiddar færslur sem eru stofnaðar í versluninni tryggir bókunarferli með hlutastraum að birgðir sem eru tengdar sölu eru uppfærðar á skilvirkan hátt. Til að fá sem skilvirkasta vinnslu á birgðafærslum fyrir staðgreiddar pantanir skaltu gæta þess að stilla kerfið til að nota [bókun með hlutastraum](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Bóka færsluuppgjör í runu** - Þessi vinnsla er einnig nauðsynleg fyrir bókun með hlutastraum. Hún fylgir vinnslunni **Reikna færsluuppgjör í runu**. Þessi vinnsla bókar kerfisbundið reiknuð yfirlit, svo að sölupantanir vegna staðgreiddrar sölu eru stofnaðar í Commerce Headquarters og Commerce Headquarters endurspeglar birgðir verslunarinnar á nákvæmari hátt.
- **Tiltækar afurðir** - Þessi vinnsla skapar mynd af birgðum úr Commerce Headquarters.
- **1130 (Tiltækar afurðir)** - Þessa vinnslu er að finna á síðunni **Dreifingaráætlanir** og ætti að keyra strax á eftir vinnslunni **Tiltækar afurðir**. Þessi vinnsla flytur skyndimynd birgða úr Commerce Headquarters yfir í gagnagrunna rásarinnar.

Mælt er með því að keyra ekki þessar runuvinnslur of oft (á nokkurra mínútna fresti). Tíðar keyrslur valda of miklu álagi á Commerce Headquarters og geta hugsanlega haft áhrif á afköst. Almennt er það góð venja að keyra verk afurðaframboðs og 1130 á klukkutíma fresti og tímasetja P-verk, samstilla pantanir og verk sem tengjast bókun með hlutastraumi með sömu eða hærri tíðni.

> [!NOTE]
> Af frammistöðuástæðum, þegar útreikningar á birgðahlið framboðs eru notaðir til að leggja fram beiðni um birgðaaðstoð með því að nota API fyrir e-Commerce eða nýju POS birgðastöðvar við hlið rásar, notar útreikningurinn skyndiminni til að ákvarða hvort nægur tími hafi liðið til að réttlæta að keyra útreikninga rökfræðinnar aftur. Sjálfgefið skyndiminni er stillt á 60 sekúndur. Til dæmis kveiktir þú á útreikningi á rásarhlið fyrir verslunina þína og skoðaðir lagerbirgðir fyrir vöru á síðunni **Birgðauppfletting**. Ef ein eining vörunnar er síðan seld, mun síðan **Birgðauppfletting** ekki sýna minnkaðan lager fyrr en skyndiminni hefur verið hreinsað. Eftir að notendur bókað færslur í POS ættu þeir að bíða í 60 sekúndur áður en þeir staðfesta að lagerbirgðir hafi verið skertar.

Ef viðskiptasvið þitt þarfnast minni skyndiminnistíma skaltu hafa samband við stuðningsfulltrúa þinn til að fá hjálp.
