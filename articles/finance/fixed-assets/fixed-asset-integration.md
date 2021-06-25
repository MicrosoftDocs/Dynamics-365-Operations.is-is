---
title: Samþætting eigna
description: Eignir má samþætta við fjárhag, birgðastjórnun, viðskiptakröfur og viðskiptaskuldir. Einnig er hægt að setja upp eignir þannig að þær séu samþættar með innkaupapöntunum.
author: ShylaThompson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e6be2aeb263c339f4e733b98ea4e01194973a9f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189785"
---
# <a name="fixed-assets-integration"></a>Samþætting eigna

[!include [banner](../includes/banner.md)]

Eignir má samþætta við fjárhag, birgðastjórnun, viðskiptakröfur og viðskiptaskuldir. Einnig er hægt að setja upp eignir þannig að þær séu samþættar með innkaupapöntunum.

## <a name="general-ledger"></a>Fjárhagur

Í fjárhag, gildi allra eigna er yfirleitt tekið saman í mörgum aðallyklum sem er krafist fyrir fjárhagsskýrsla. Hins vegar er hægt að stofna margar eignafærslur á siðunni **Eignir**. Þessar færslur geta verið upplýsingar um verð kaup, afskriftir og mat. Hvert skipti sem færsla er bókuð fyrir eign eru viðeigandi aðallyklar uppfærðir. Aðallyklar fyrir eignir sýna alltaf uppfært virði eignanna

Á síðunni **Bókunarreglur eigna** eru skilgreindir aðallyklar sem færslur eignabókar eru bókaðar í. Einnig tilgreinirðu þær gerðir eignafærslna sem bókaðar eru í hvern aðallykil. Hægt er að stofna ýmsar samsetningar af aðallyklum fyrir eignir, allt eftir upplýsingastigi sem þú vilt fyrir eignir í fjárhag. Aðallyklar geta verið byggðir á færslugerðum, bókum og öðrum aðallyklum.

## <a name="inventory-management"></a>Birgðir
Í birgðafærslubók fyrir eignir getur þú slegið inn kaup á eignum sem lögaðili hefur framleitt eða smíðað fyrir sig. Síðan er hægt að flytja vörur í birgðum til eigna sem kaup eða sem hluta af kaupum. 

Einnig er hægt að fá eignir með því að nota innkaupapantanir Þegar innkaupapantanir innihalda birgðavörur sem eru merktar sem eignir ákvarðar stillingin í gátreitnum **Leyfa eignakaup úr innkaupum** á síðunni **Færibreytur eigna** hvort kaupin séu bókuð fyrir eignina þegar reikningurinn er bókaður. Ein innkaupalína býr til eina eign, óháð magninu. Gildi sem hefur kaup eigna á birgðir fer eftir uppsetningu lögaðila. 

Þegar birgðavara breytist í eignakaup, annað hvort í gegnum birgðabók, innkaupapöntun, eða kauptillögu, stofnast kaupfærsla bókar eignarinnar. Ef kaupvirðisfærsla fela í sér afleidda bók, stofnast einnig kaupvirðisfærsla afskriftarbókar. 

Minnkun birgða þegar kaup eru bókuð er stjórnað af þeim bókunarreglum sem eru skilgreindar á síðunni **Bókun** í Birgðastjórnun. Hins vegar þarf ekki alltaf að minnka birgðir þegar reikningar sem tengjast eignum eru bókaðir. Í sumum tilfellum gæti verið að kaupa eignir til innri notkunar. Sem dæmi má nefna fartölvu sem er keypt fyrir söludeild. Þegar unnið er með innkaupapantanir, er hægt að nota vörur sem eru settar upp fyrir bæði endursölu og notkun innan fyrirtækisins. 

Ef þú notar sérstaka innhreyfingar- og úthreyfingarlykla fyrir vöruflokka fyrir eignir, geturðu notað sama birgðavara fyrir bæði innri innkaup og sem birgðir til endursölu. 

Eignir sem eru til innri notkunar eru settar upp þannig að þær hafi lykilgerðina **Eignainnhreyfing**. Þessi gerð er notuð til að rekja móttöku eignarinnar. Þegar reikningur lánardrottins er bókaður, skaltu nota innhreyfingarlykil eignar ef eitthvað af eftirfarandi skilyrðum er uppfyllt:

-   Reikningslínan inniheldur eign vegna innri málefna.
-   Gátreiturinn **Ný eign?** er valinn fyrir línu innhreyfingarskjal afurða sem er bókað.
-   Gátreiturinn **Stofna nýja eign** er valinn fyrir reikningslínu lánardrottins.

Þessi lykill er yfirleitt kostnaðarlykill. Þú getur sett upp lykilgerðina **Innhreyfing eigna** fyrir annaðhvort vöruflokk eða staka vöru með því að nota flipann **Innkaupapöntun** í skjámyndunum **Vöruflokkur** eða **Bókun**.

Á svipaðan hátt er hægt að setja upp eignir sem eru til innanhússnota þannig að þær hafi lykilgerðina **Úthreyfing eignar**. Þessi gerð lykils er að nota í úthlutun eignar til móttakanda. Þegar eign er keypt með því að nota innkaupapöntun mótreiknar eignaúthreyfingareikningurinn debetreikning eigna. Hægt er að bókfæra kaup eigna annaðhvort um leið og lánardrottnareikningur er bókaður eða þegar eignakaup eru bókuð í eignabókina, mögulega með því að nota kauptillögu. Þú getur sett upp lykilgerðina **Úthreyfing eigna** fyrir annaðhvort vöruflokk eða staka vöru með því að nota flipann **Birgðir** í skjámyndunum **Vöruflokkur** eða **Vörubókun**. 

Að lokum, eru aðallyklar sem eru notaðir í bókun ákvarðaðir af valkostum fyrir samþættingu fjárhags sem eru tilgreindar fyrir vörulíkanaflokk. Þar að auki eru aðallykla sem notaðar eru mismunandi, eftir því hvort að eign er tengd við innkaupapöntunarlínuna. Lyklarnir eru afleiddir frá bókunarforstillingunni fyrir hvern vöruflokk. 
**Athugið:** Ef frátekning birgða er til staðar þegar innhreyfingarskjal afurða er bókað, er ekki hægt að tengja eign eða stofna eign út frá línunni. 

Lyklar sem eignafærslur eru bókaðar í fara eftir tveimur þáttum: hvort eignir séu keyptar eða unnar af lögaðili, og á færslugerð eignarinnar. 

Færslugerðin tengir birgðafærsluna við bókunarforstillingu í Eignum. Þar sem bókunarregla í Eignum skilgreinir hvaða lykill er uppfærður er val á færslugerð fyrir eign einnig óbeint val á þeim aðallykli sem færslan er bókuð í. Fyrir bæði uppbyggðar og keyptar eignir er færslugerðin yfirleitt **Kaup** eða **Leiðrétting kaupa**.

## <a name="accounts-receivable"></a>Viðskiptakröfur
Bókunarreglur eru settir upp í eignum notar samþætting eigna við viðskiptavini. Þessar bókunarreglur eru gerð virk þegar eign og tegund eignafærslu er valin fyrir reikning viðskiptavinar áður en reikningur viðskiptavinar er bókaður. Þar sem eignir eru ekki hluti af birgðastjórnun, verður að nota síðuna **Textareikningur** þegar eign er seld. 

Ef bók inniheldur afleidda bók er afskriftarbókafærsla stofnuð þegar reikningur viðskiptavinar er bókaður.

## <a name="accounts-payable"></a>Viðskiptaskuldir
Eignir eru yfirleitt keyptar af ytri lánardrottnum. Hægt er að nota skjámyndina **Færibreytur eigna** til að tilgreina hvort eignakaup eru alltaf bókuð um leið og reikningar lánardrottins eru bókaðir, eða hvort einungis er hægt að bóka eignakaup úr Eignum. Ef bókun eignakaup eru leyfð út frá viðskiptaskuldum, uppfærast eignalyklar í hvert sinn sem bókaður er reikningur lánardrottins fyrir eignakaup. 

Ef kerfið er sett upp þannig að bókuð séu eignakaup um leið og reikningur er bókaður, bókast færslan samkvæmt bókunarforstillingum sem eru settar upp í Eignir fyrir mismunandi tegundir eignafærslna. Bókuninni er stjórnað af eigninni og þeirri tegund eignafærslu sem hefur verið valin á síðunni **Innkaupapöntun** áður en reikningur lánardrottins var bókaður. 

Ef bók inniheldur afleidda bók er afskriftarbókafærsla stofnuð þegar reikningur lánardrottins er bókaður.

Samþætting fyrir hverja pöntunarlínu er virkjuð á flipanum **Eignir** á flýtiflipanum **Línuupplýsingar** á síðunni **Innkaupapöntun**. Hægt er að senda innkaupapöntun fyrir eign til seljanda. Hins vegar, eignir og aðallykla uppfærast einungis þegar reikningur lánardrottins er bókaður eftir að eignin er móttekin. Vegna þess að innkaupapantanir geta einungis innihaldið birgðavöru, áhrifin sem hefur kaup eigna á birgðir fer eftir uppsetningu lögaðila.

## <a name="project-management-and-accounting"></a>Verkefnastjórnun og bókhald
Hægt er að tengja verkefni við eign sem verður fyrir áhrifum af verkefninu. Einnig er hægt að tengja hvern áfanga, verkefni eða undirverk við mismunandi eignir. Hægt er að tengja eina eign við hverja verkfærslu. Tenging er mynduð þegar fært er inn númer eignar í reitinn **Eign** á síðunni **Verkefni**. Gerð verks verður að vera annaðhvort **Innri** eða **Kostnað verks**. 

Einnig er hægt að nota síðuna **Verkefni** til að skoða upplýsingar um eignir sem eru tengdar verkum. Á flýtiflipanum **Uppsetning** er smellt á eignatengilinn til að opna síðuna **Eignir**. Smellið síðan á **Verkefni** &gt; **Öll verkefni** til að skoða verkefni sem eru tengd við eign. 

Yfirleitt eru eignir tengdar verkefnum þegar verkefnin tengjast vinnu, viðhaldi eða endurbótum á eigninni sjálfri. Þegar verkinu er lokið, uppfærsluleiðréttingu eignarinnar er ekki stofnuð sjálfkrafa. Þess vegna verður að stofna í uppfærsluleiðréttingu handvirkt, ef þörf er á uppfærsluleiðréttingu. 

Til að eyða tengingu milli verks og eignar, skal hreinsa reitinn **Númer eignar** á síðunni **Verkefni**. 

Einnig er hægt að ákvarða eign sem þú stofnar eða framleiðir sem hluta af áætluðu verki. Við lok matsverks, er hægt að bóka eignakaupfærslu sjálfkrafa.

Frekari upplýsingar eru í [Kaupa eignir með innkaupum](acquire-assets-procurement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]