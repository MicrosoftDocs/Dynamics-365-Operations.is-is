---
title: "Yfirlit yfir gæðastjórnun"
description: "Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Microsoft Dynamics 365 for Finance and Operations til að bæta gæði afurða innan aðfangakeðju þinnar."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 28ef47e2dc1f9c7e1c0b262c58332dcfea1f7495
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="quality-management-overview"></a>Yfirlit yfir gæðastjórnun

[!include[banner](../includes/banner.md)]


Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Microsoft Dynamics 365 for Finance and Operations til að bæta gæði afurða innan aðfangakeðju þinnar.

Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra. Þar sem greiningargerðir eru tengdar leiðréttingaskýrslum getur Microsoft Dynamics 365 for Finance and Operations raðað verk til að leiðrétta vandamál og komið í veg fyrir þau verði endurtekin.

Auk virkni fyrir stjórnun ósamkvæmni inniheldur gæðastjórnun virkni til að rekja úthreyfingar eftir gerð vanda (jafnvel innri vandamál) og til að auðkenna lausnir sem skammtíma- eða langtímalausnir. Upplýsingar um afkastavísi (KPI) veita innsýn í sögulegan feril fyrri vandamála með ósamkvæmi og þeirra lausna sem voru notuð til að leiðrétta þau. Hægt er að nota söguleg gögn til að fara yfir skilvirkni fyrri gæðaráðstafana og ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.

Þegar gæðatenging er sett upp getur Finance and Operations myndað gæðapantanir fyrir ýmis viðskiptaferli, tilvik og skilyrði. Gæðatengingin getur náð yfir ákveðna vöru, einstökan vöruflokk eða allar vörur.

## <a name="examples-of-the-use-of-quality-management"></a>Dæmi um notkun á gæðastjórnun
Gæðastjórnun er sveigjanleg og hægt er að innleiða hana á mismunandi vegu til að uppfylla kröfur um tiltekið stig í aðgerðum framboðskeðju. Eftirfarandi dæmi sýna hugsanlega notkun á þessum eiginleikum:

-   Hefja ferli gæðaeftirlits sjálfvirkt, byggt á fyrirfram skilgreindum skilyrðum (við vöruhússkráningu innkaupapöntunar frá tilteknum lánardrottni).
-   Læsa birgðum við skoðun til að koma í veg fyrir að ósamþykktar birgðir séu notaðar (alger stöðvun á pöntunarmagni innkaup).
-   Vörusýnishorn eru notuð sem hluti af gæðatengingu til að skilgreina magn gildandi efnislegra birgða sem verður að skoða. Sýnishorn geta verið byggð á föstu magni eða hlutfalli.
-   Stofna gæðapantanir fyrir hluta móttöku. Til að stofna gæðapöntun sem byggir á magni sem tekið er við efnislega með pöntun verður að velja gátreitinn **Eftir uppfærðu magni** á skjámyndinni **Vörusýnishorn**.
-   Stofna prófunargerðir sem innihalda lágmark, hámark og markprófunargildi og framkvæma eigindlega-samanborið við-eigindlega prófun sem hefur fyrirfram skilgreindar niðurstöður villuleitar.
-   Tilgreina viðunandi gæðastig (AQL) til að stjórna vikmörkum gæðaráðstafana.
-   Tilgreina tilföng sem skoðunaraðgerð krefst, eins og prófunarsvæði og prófunartæki.

## <a name="working-with-quality-associations"></a>Vinna með gæðatengingar
Viðskiptaferli sem notar gæðatengingu getur verið tengt mismunandi upprunaskjölum, eins og innkaupapöntunum, sölupöntunum eða framleiðslupöntunum.

Hver gæðatengingafærsla skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir. Skilgreina verður gæðatengingafærslu fyrir hvert afbrigði viðskiptaferlis. Til dæmis er hægt að setja upp gæðatengingu sem myndar gæðapöntun þegar innhreyfingarskjal afurða innkaupapöntun er uppfært. Það fer eftir uppsetningu á keyrsluáætlun hvort hægt sé að stöðva kveikjuferlið sjálft á meðan gæðapöntun er opin eða hvort hægt sé að stöðva næstu ferli, eins og reikningsfærslu á innkaupapöntun.

**Ábending:** Meðan gæðapantanir eru opnar er birgðamagn sjálfkrafa stöðvað til útgáfu. Það fer eftir **Alger stöðvun** stillingunni á síðunni **Vörusýnishorn** hvort magn sé annaðhvort magn í gæðapöntun eða magn í upprunaskjalslínu.

Fyrir tiltekið viðskiptaferli auðkennir gæðatengingarfærslan tilvik og skilyrði sem mynda skal gæðapöntun fyrir. Skilyrðin geta átt sérstaklega við svæði eða lögaðila. Aðeins er hægt að mynda gæðapöntun sem felur í sér eyðileggingarprófun þegar lagerbirgðir eru til staðar fyrir tilvikið.

Eftirfarandi dæmi sýna hvernig gæðatengingafærsla er skilgreind fyrir afbrigði hvers viðskiptaferlis. Í eftirfarandi töflu eru dæmin tekin saman eftir tilviki og skilyrðum sem skilgreind eru af gæðatengingarfærslu.

<table>
<tbody>
<tr>
<th>Gerð tilvísunar</th>
<th>Gerð tilviks</th>
<th>Framkvæmd</th>
<th>Lokun tilviks</th>
<th>Tilvísun skjals</th>
</tr>
<tr>
<td>Birgðir</td>
<td>Ekki tiltækt</td>
<td>Ekki tiltækt</td>
<td>Ekkert</td>
<td>Allt</td>
</tr>
<tr>
<td rowspan="7">Sala</td>
<td rowspan="4">Tiltektarferli er áætlað</td>
<td rowspan="4">Fyrir</td>
<td>Ekkert</td>
<td rowspan="22">Tilgreint kenni, Flokkur eða Allir aðeins</td>
</tr>
<tr>
<td>Tiltektarferli</td>
</tr>
<tr>
<td>Fylgiseðill</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="3">Fylgiseðill</td>
<td rowspan="3">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Fylgiseðill</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="15">Innkaup</td>
<td rowspan="7">Innhreyfingaskjal</td>
<td rowspan="4">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingaskjal</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="3">Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="3">Skráning</td>
<td rowspan="3">Ekki tiltækt</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="5">Innhreyfingarskjal afurðar</td>
<td rowspan="3">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Innhreyfingarskjal afurðar</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="2">Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Reikningur</td>
</tr>
<tr>
<td rowspan="8">Framleiðsla</td>
<td rowspan="3">Skráning</td>
<td rowspan="3">Ekki tiltækt</td>
<td>Ekkert</td>
<td rowspan="12">Allt</td>
</tr>
<tr>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="5">Bóka tilbúið</td>
<td rowspan="3">Fyrir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="2">Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="4">Biðgeymsla</td>
<td rowspan="3">Bóka tilbúið</td>
<td rowspan="2">Fyrir</td>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Við skil</td>
</tr>
<tr>
<td>Eftir</td>
<td>Við skil</td>
</tr>
<tr>
<td>Við skil</td>
<td>Fyrir</td>
<td>Við skil</td>
</tr>
<tr>
<td rowspan="3">Leiðaraðgerð</td>
<td rowspan="3">Bóka tilbúið</td>
<td rowspan="2">Fyrir</td>
<td>Ekkert</td>
<td rowspan="3">Tilgreitn kenni, Flokkur eða Allt, og Tilfangasértækt, Flokkur eða Allt</td>
</tr>
<tr>
<td>Bóka tilbúið</td>
</tr>
<tr>
<td>Eftir</td>
<td>Ekkert</td>
</tr>
<tr>
<td rowspan="3">Framleiðsla aukaafurðar</td>
<td>Skráning</td>
<td>Ekki tiltækt</td>
<td rowspan="3">Ekkert</td>
<td rowspan="3">Allt</td>
</tr>
<tr>
<td rowspan="2">Bóka tilbúið</td>
<td>Fyrir</td>
</tr>
<tr>
<td>Eftir</td>
</tr>
</tbody>
</table>

Eftirfarandi tafla veitir frekari upplýsingar um hvernig hægt er að mynda gæðapantanir fyrir tilgreindar gerðir ferla.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Gerð ferlis</th>
<th>Þegar hægt er að mynda gæðapantanir sjálfvirkt</th>
<th>Þegar hægt er að mynda gæðapantanir ef eyðileggingarprófun er áskilin</th>
<th>Upplýsingar um skilyrði</th>
<th>Upplýsingar um handvirka myndun</th>
</tr>
<tr>
<td>Innkaupapöntun</td>
<td>Á undan eða eftir komulista eða innhreyfingarskjal afurða fyrir efni sem er móttekið er bókuð</td>
<td>Eftir innhreyfingarskjal afurða fyrir efni sem er móttekið er bókað, þar sem efnið verður að vera tiltækt fyrir eyðileggingarprófun</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í innkaupapöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Biðgeymslupöntun</td>
<td>Á undan eða eftir biðgeymslupöntunin er skráð sem lokið eða lokið</td>
<td>Ekki er hægt að mynda gæðapantanir sem krefjast eyðileggingarprófana. Gert er ráð fyrir að virkni biðgeymslupöntunar annist ráðstöfun á efni sem er eyðilagt.</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í biðgeymslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Sölupöntun</td>
<td>Á undan á áætluðu tiltektarferli eða fylgiseðilsuppfærslu fyrir vörur sem verið er að senda</td>
<td>Á hvaða þrepi sem er</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða viðskiptavinar eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í sölupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Framleiðslupöntun</td>
<td>Á undan eða eftir að tilbúið magn fyrir framleiðslupöntun er skráð</td>
<td>Eftir að tilbúið magn fyrir framleiðslupöntun er skráð</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis eða vöru eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í framleiðslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Framleiðslupöntun sem er með leiðaraðgerð</td>
<td>Á undan eða eftir að skýrslu er lokið fyrir aðgerð</td>
<td>Á undan eða eftir að skýrsluframleiðslu er lokið fyrir síðustu aðgerð</td>
<td>Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða rekstrartilfanga eða samsetningu þessara skilyrða.</td>
<td>Gæðapöntun sem er stofnuð handvirkt og vísar í leiðaraðgerð getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</td>
</tr>
<tr>
<td>Birgðir</td>
<td>Ekki er hægt að mynda gæðapöntun sjálfkrafa fyrir færslu í birgðabók eða fyrir flutningspantanafærslur.</td>
<td></td>
<td></td>
<td>Gæðapöntun verður að vera stofnuð handvirkt fyrir birgðamagn vöru. Efnislegra lagerbirgða er krafist.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Gæðastjórnunarsíður
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Síða</th>
<th>Lýsing</th>
<th>Dæmi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gæðatengingar</td>
<td>Sjá fyrri hluta í þessari grein.</td>
<td>Gæðatenging skilgreinir allar eftirfarandi upplýsingar fyrir gæðapöntun sem er mynduð:
<ul>
<li>Færslutilvikið</li>
<li>Safn prófana sem þarf að framkvæma á vörum</li>
<li>Viðunandi gæðastig</li>
<li>Úrtaksáætlunin</li>
</ul>
Gæðatengingu verður að skilgreina fyrir hvert afbrigði viðskiptaferlis sem krefst sjálfvirkrar myndunar gæðapöntunar. Til dæmis er hægt að mynda gæðapöntun í viðskiptaferlum fyrir innkaupapantanir, biðgeymslupantanir, sölupantanir eða framleiðslupantanir.</td>
</tr>
<tr class="even">
<td>Prófanir</td>
<td>Notið þessa skjámynd til að skilgreina og skoða einstök próf sem ákvarða hvort framleiðsluvara fyrirtækisins uppfylli gæðakröfur. Hægt er að úthluta einu eða fleiri einstökum prófum á prófunarflokk. Í þessu tilviki þarf einnig að tilgreina prófunarsértækar upplýsingar, eins og viðunandi mælingargildi. Mælingargildi eru notuð fyrir magnbundnar prófanir og prófunarbreytur eru notaðar fyrir eðlisbundin próf.
<ul>
<li>Magnbundið próf hefur prófunargerð fyrir <strong>Heiltala</strong> eða <strong>Brot</strong> og er einnig með skilgreinda mælieiningu. Gæðaskilyrði og prófunarniðurstöður sem eru sýnd sem tölur.</li>
<li>Eðlisbundið próf hefur prófunargerðina <strong>Valkostir</strong>. Eigindlegar prófanir krefjast viðbótarupplýsingar um prófunarbreytuna sem verið er að mæla og tölusetta valkosti hennar. Gæðaforskriftir og prófunarniðurstöður sem eru sýnd eftir útkomu.</li>
</ul></td>
<td>Framleiðslufyrirtæki framkvæmir tvær prófanir á innkeypt efni: magnbundið prófun á gæðum efnis og eigindlega prófun á umbúðaskemmdum. Fyrirtækið skilgreinir viðbótarupplýsingar um eðlisbundið próf til að auðkenna prófunarbreytu (skemmdar umbúðir) og niðurstöður hennar. Fyrirtæki notar síðuna <strong>Prófunarflokkar</strong> til að úthluta tveimur prófunum á prófunarflokk og tilgreina prófunarsértækar upplýsingar. Prófunarflokknum er úthlutað á gæðapöntun svo að fyrirtækið getur tilkynnt niðurstöður prófana fyrir bæði prófin.</td>
</tr>
<tr class="odd">
<td>Prófunarflokkar</td>
<td>Notaðu þessa síðu til að setja upp, breyta og skoða prófunarflokka og einstakar prófanir sem er úthlutað á prófunarflokk. Efri rúðan birtir prófunarflokka og neðri rúðan birtir prófanir sem er úthlutað á valinn prófunarflokk. Nokkrum reglum er úthlutað á prófunarflokk, eins og úrtaksáætlun, viðunandi gæðastigi og þörf fyrir eyðileggingarprófun. Þegar þú úthlutar stöku prófi á prófunarflokk, skilgreinirðu viðbótarupplýsingar, eins og röðina, skjölin og gildisdagsetningarnar. Fyrir magnbundna prófun innihalda upplýsingar sem eru skilgreindar einnig viðunandi mælingargildi. Upplýsingarnar eru prófunarfæribreytur og sjálfgefin útkoma fyrir eigindlega prófun. Prófunarflokkur sem er úthlutað á gæðapöntun skilgreinir sjálfgefið safn prófana sem verður að framkvæma á tiltekinni vöru. Hins vegar er hægt að bæta við, breyta, eða eyða prófunum innan gæðapöntunar. Niðurstöður prófana eru tilkynntar fyrir hvert próf á gæðapöntun.</td>
<td>Framleiðslufyrirtæki skilgreinir prófunarflokk fyrir hvert afbrigði af gæðareglum sínum. Mismunandi prófunarflokkar endurspegla mismun á úrtaksáætlunum, safn prófana sem þarf að framkvæma samtímis, viðunandi gæðastigi og öðrum stuðlum. Fyrir magnbundnar prófanir er einnig mismunur í viðunandi mælingargildum. Til að framfylgja gæðareglum úthlutar fyrirtækið prófunarflokki á hverja reglu fyrir sjálfvirka myndun gæðapantana á síðunni <strong>Gæðatengingar</strong> og einnig prófunarflokki á gæðapantanir sem eru stofnaðar handvirkt.</td>
</tr>
<tr class="even">
<td>Vörugæðaflokkar</td>
<td>Notaðu þessa síðu til að setja upp, breyta og skoða vörur sem er úthlutað á gæðaflokk eða gæðaflokka sem eru tengdir vöru. Gæðaflokkur stendur fyrir sameiginlegar prófunarkröfur fyrir vörur. Þegar búið er að skilgreina kröfur fyrir prófun á síðunni <strong>Prófunarflokkar</strong> er hægt að skilgreina reglur fyrir sjálfvirka myndun gæðapantana. Til að einfalda ferlið eru ekki skilgreindar reglur fyrir stakar vörur. Þess í stað eru skilgreindar reglur fyrir gæðaflokk, með því að nota síðuna <strong>Gæðatengingar</strong>. Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valinn gæðaflokk til að úthluta viðeigandi vörum á þeim flokki. Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valda vöru til að úthluta viðeigandi gæðaflokkum á vöruna.</td>
<td>Framleiðslufyrirtæki kaupir ýmislegt hráefni sem eru með sömu prófunarkröfur fyrir væntanlegt eftirlit. Fyrirtækið skilgreinir gæðaflokk og úthlutar síðan vörunúmerum sem eru tengd hráefnum á þann flokk. Síðar kaupir fyrirtækið nýja gerð hráefnis sem er með sömu prófunarkröfur. Í stað þess að setja upp ný skilyrði um prófanir fyrir nýtt efni bætir við fyrirtækið vörunúmeri fyrir nýtt efni fyrirliggjandi gæðaflokk. Sama framleiðslufyrirtæki framleiðir einnig vörur sem eru með sömu prófunarkröfur í framleiðslu og sendir vörur með sömu kröfur fyrir framkvæmd prófana fyrir sendingu. Fyrirtækið skilgreinir tvo viðbótargæðaflokka og úthlutar síðan viðeigandi vörunúmerum í hvern gæðaflokk.</td>
</tr>
<tr class="odd">
<td>Prófunarbreytur</td>
<td>Notaðu síðuna til þess að skilgreina og skoða breyturnar sem eru tengdar við eigindlega prófun. Fyrir hverja færibreytu eru skilgreindar númeraðar niðurstöður sem sýna mögulega valkosti. Skilgreina prófanir á <strong>Prófanir</strong> síðu. Fyrir eðlisbundið próf verður að stilla prófunargerðina á <strong>Valkost</strong>. Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta breytu á prófun.</td>
<td>Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru. Þessi prófun hefur nokkur breytur. Ein færibreyta er bragð, með valkostunum gott eða vont. Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</td>
</tr>
<tr class="even">
<td>Útkomur úr prófunarbreytum</td>
<td>Notið þessa síðu til að setja upp, breyta og skoða mögulegar niðurstöður prófana fyrir prófunarbreytu sem tengist gæðaprófi. Hægt er að gefa hverri niðurstöðu einkunnina <strong>staðist</strong> eða <strong>fallið</strong>. Skilgreina verður breytuna og niðurstöður hennar fyrir hverja eigindlega prófun sem er skilgreind á síðunni <strong>Prófanir</strong>. (Fyrir gæðaprófanir er prófunargerðin stillt á <strong>Valkostur</strong> á síðunni <strong>Prófanir</strong>.) Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta prófunarbreytu og sjálfgefinni niðurstöðu á staka gæðaprófun.</td>
<td>Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru. Þessi eftirlitsprófun hefur nokkur breytur. Ein færibreyta er bragð, með valkostum gott eða vont. Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi. Hver einasta niðurstaða hefur stöðuna <strong>staðist</strong> eða <strong>fallið</strong>. Á meðan á gæðaprófi stendur fyrir hverja færibreytu, skráir prófunaraðili niðurstöður prófsins með því að velja eina af mögulegu niðurstöðunum.</td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Sjá einnig
--------

[Ferli gæðastjórnunar](quality-management-processes.md)

[Virkja stjórnun ósamkvæmni](enable-nonconformance-management.md)

