---
title: Birgðabókun
description: Í þessari grein útskýring á birgðabókunarflipa á síðu birgðabókunarreglu.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 7fd507dd171b0d49673bdd0d0900b3f02dbcb65b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891552"
---
# <a name="inventory-posting"></a>Birgðabókun

Flipinn **Birgðir** á síðunni **Birgðabókunarreglur** er notaður til að stjórna því hvernig birgðafærslur eru bókaðar í fjárhagnum. Birgðafærslur eru færslur sem eru ekki stofnaðar úr sölupöntunum, innkaupapöntunum eða framleiðslupöntunum. Þær bóka sjálfkrafa efnislegar og fjárhagslegar uppfærslur í birgðirnar á sama tíma. Ein undantekning er flutningspantanir sem aðskilja efnislegar og fjárhagslegar uppfærslur þegar birgðir eru afhentar og mótteknar.

Eftirfarandi tafla sýnir dæmi um birgðafærslur.

| Færslugerð | Innhreyfing eða úthreyfing | Efnisleg færsla, fjárhagsleg færsla eða hvort tveggja | Lýsing |
|---|---|---|---|
| Hreyfing | Bæði | Bæði | <p>Hreyfingabók er birgðabók sem hægt er að nota til að bæta við eða fjarlægja birgðir. Þetta virkar eins og færslubók fyrir birgðaleiðréttingu Einn mikilvægur munur er sá að aðallykillinn sem jafnar færsluna er tilgreindur.</p><p>Hreyfibókin færir inn upphafsstöður og einkvæmar leiðréttingar sem þarf að kostnaðarfæra. Til dæmis er hún notuð þegar birgðir eru fjarlægðar fyrir sölusýnishorn.</p><p>Þegar færslubókin er bókuð gerast efnislegar og fjárhagslegar uppfærslur á sama tíma.</p><p>Jákvætt magn í færslubókarlínum táknar innhreyfingar og neikvætt magn táknar úthreyfingar.</p> |
| Leiðrétting birgða | Bæði | Bæði | Birgðaleiðréttingabók er notuð til að bæta við eða fjarlægja birgðir. Það leyfir þér ekki að velja mótlykil. Aðeins lyklar sem eru tilgreindir á síðunni **Birgðabókunarregla** eru notaðir til að uppfæra fjárhagsfærsluna. |
| Flutningur (færslubók) | Bæði | Bæði | <p>Flutningsbók er notuð til að flytja birgðir frá einni staðsetningu yfir á aðra (með því að nota geymsluvíddir). Hún uppfærir afurðarupplýsingar á birgðafærslu með nýjum afurðar- eða rakningarvíddum.</p><p>Flutningsbók stofnar eina línu fyrir hreyfingu á vöru. Þessi lína er með reitina „frá“ og „til“ fyrir birgðavíddirnar. Hver lína í flutningsbókinni stofnar tvær birgðafærslur. Ein færsla er stofnuð fyrir „frá“ birgðavíddirnar. Það táknar vandamálið og er með neikvætt magn. Hin færslan er stofnuð fyrir „til“ birgðavíddirnar. Það táknar innhreyfinguna og hefur jákvætt magn.</p><p>Ekki er víst að flutningsbækur búi til fylgiskjal ef flutningur birgða er álitinn ófjárhagslegur flutningur. Birgðavíddir sem eru frábrugðin „frá“ og „til“ gildunum eru ekki merktar með valkostinum **Fjárhagslegar birgðir** á síðunni **Birgðavíddarflokkur** eða **Rakningarvíddarflokkur**. Ef valkosturinn **Fjárhagslegar birgðir** er til dæmis ekki merktur í víddinni **Staðsetning** og birgðir eru færðar frá einni staðsetningu til annarrar á sama svæði og í sama vöruhúsi er ekkert fylgiskjal búið til.</p><p>Flutningsbækur er frábrugðnar flutningspöntunum að því leyti að það eru engin skjöl fyrir flutninginn. Uppfærslan er gerð í einni færslu með því að bóka færslubókina. Aftur á móti getur flutningspöntun búið til tínslu- og afhendingarskjöl og þarf tvær uppfærslur til að vinna úr færslunni.</p> |
| Flutningspöntunarsending | Gefa út | Bæði | <p>Þegar ný flutningspöntun er stofnuð er hver samsetning af línu- og birgðavídd með tvær birgðafærslur: eina fyrir afhendingu flutningspöntunar og aðra fyrir móttöku flutningspöntunar. Þegar flutningspöntunin er afhend eru tvær birgðafærslur uppfærðar og tvær birgðafærslur til viðbótar eru búanar til fyrir flutning á vörum, samanlagt fjórar birgðafærslur.</p><ol><li>Fyrsta birgðafærslan er notuð til að fjarlægja vöruna úr upprunalegu vöruhúsi og staðsetningu. Úthreyfingarstaða þessarar færslu er **Seld** til að gefa til kynna að varan sé ekki lengur tiltæk í vöruhúsinu.</li><li>Önnur birgðafærslan er notuð til að bæta vörunni við flutningsvöruhúsið sem er valið fyrir vöruhúsið sem varan er flutt úr. Innhreyfingarstaða þessarar færslu er **Keypt**.</li><li>Þriðja birgðafærslan er fyrir flutning úr flutningsvöruhúsinu í áfangavöruhúsið. Útgáfustaða færslunnar er **Frátekið efnislegt magn**. Þessi staða tryggir að ekki er hægt að nota vöruna í öðru ferli á meðan hún er enn í flutningi.</li><li>Fjórða birgðafærslan er fyrir móttöku vöru í áfangavöruhúsi. Innhreyfingarstaða þessarar færslu er **Pantað**.</li></ol> |
| Móttaka flutningspöntunar | Innhreyfing | Bæði | Þegar flutningspöntun er móttekin í áfangavöruhúsi er birgðastaða birgðafærslunnar sem er í flutningsvöruhúsinu (númer 3 í fyrrgreindu dæmi) uppfærð í **Selt** og birgðastaða birgðafærslunnar fyrir áfangavöruhúsið er uppfærð í **Keypt**. |
| Uppskriftir | Bæði | Bæði | Hægt er að nota uppskriftabók til að skrá afurð sem lokið og nota hráefnin sem voru notuð í ferlinu án þess að nota framleiðslupöntun. Uppskriftabók inniheldur yfirleitt a.m.k. eina jákvæða línu fyrir fullunna vöru og eina eða fleiri neikvæðar línur fyrir hráefni sem verið er að nota. Lína fullunninnar vöru er innhreyfing í birgðir, en neikvæðar línur eru úthreyfingar úr birgðum fyrir hráefnin. Þegar uppskriftabók er búin til er fyrsta línan uppskriftarhausinn og næstu línur sem bætt er við eru uppskriftarlínur. |
| Eignarhaldsbreyting birgða | Bæði | Bæði | Birgðafærslubók fyrir breytingu á eignarhaldi er notuð til að breyta eignarhaldi sendra birgð frá lánardrottni í fyrirtæki notanda. Birgðabækur eignarhaldsbreytinga líkjast birgðaflutningsbókum þar sem tvær birgðafærslur tengjast hverri samsetningu af línu og birgðavídd. Ein birgðafærsla fjarlægir birgðirnar úr lánardrottni í víddinni **Eignarhald** og hin bætir vörunni við lögaðilann í víddinni **Eignarhald**. |
| Vörumóttaka | Innhreyfing | Efnislegt | Vörukomubók er notuð til að uppfæra stöðu innhreyfingar á birgðum í **Skráð**. Hún er yfirleitt notuð fyrir móttöku innkaupapöntunar á vörum og skilum á sölupöntunum. |
| Framleiðsluinntak | Innhreyfing | Efnislegt | Framleiðsluinntaksbók líkist vörukomubók. Framleiðsluinntak er notað til að taka á móti fullunnum vörum frá framleiðslupöntun í vöruhúsinu. Þegar færslubókin er bókuð er staða birgðafærslunnar uppfærð í **Skráð**. |
| Talning | Bæði | Bæði | Talningabók er notuð til að skrá magn vörunnar sem var talið fyrir tiltekna samsetningu af birgðavíddum. Birgðafærslur eru stofnaðar þegar lína færslubókarinnar er með mismun í talningu. Lína sem er með hærra talið magn veldur innhreyfingu í birgðir. Lína sem er með lægra talið magn veldur úthreyfingu úr birgðum. Línur þar sem talið magn samsvarar væntu magni eru ekki með neinar birgðafærslur. |
| Seðlatalning | Á ekki við | Á ekki við | Merkjatalningabók er notuð til að rekja birgðamerki sem er úthlutað og notuð í fullri birgðatalningu. Hægt er að nota færslubókina til að úthluta merkjanúmeri á tiltekna samsetningu af vöru og birgðavídd og til að rekja stöðu merkisins við fullar birgðir. Merkjatalningabækur stofna ekki birgðafærslur. |
| Gæðapantanir | Gefa út | Efnislegt | <p>Gæðapöntun er notuð til að skrá niðurstöður prófunar fyrir tiltekna lotu í birgðum. Hver gæðapöntun tengist fyrirliggjandi birgðafærslu eða hluta af birgðafærslu.</p><p>Gæðapöntun mun búa til nýja birgðafærslu í tveimur aðstæðum:</p><ul><li>Gæðapöntunin er merkt sem **Eyðileggingarpróf** í flipanum **Almennt**.</li><li>Gæðapöntunin er merkt sem **Biðgeymsla þegar fellur á prófi** í flipanum **Almennt** og prófið getur ekki staðfest. Í þessu tilfelli eru tvær birgðafærslur stofnaðar. Ein birgðafærsla fjarlægir vöruna úr upprunalegri birgðavíddarsamsetningu og staðsetningu og hin bætir vörunni við biðgeymsluvöruhúsið</li></ul> |
| Biðgeymslupantanir | Bæði | Bæði | <p>Birgðafærslur biðgeymslupöntunar eru eins og flutningspöntun. Biðgeymsluvöruhús er notað til að rekja birgðirnar. Um er að ræða tvær innhreyfingarfærslur og tvær úthreyfingarfærslur.</p><p>Þegar þú stofnar pöntunina í upphafi eru tvær færslur stofnaðar. Innhreyfingarfærslan er með stöðuna **Pantað** fyrir biðgeymsluvöruhúsið sem er tengt vöruhúsinu þar sem varan er staðsett. Úthreyfingarfærslan er með stöðuna **Í pöntun** fyrir vöruhúsið þar sem varan er geymd.</p><p>Þegar biðgeymslupöntunin er sett af stað eru tvær frekari færslur stofnaðar og fyrirliggjandi færslur uppfærðar. Staða innhreyfingarfærslunnar fyrir biðgeymsluvöruhúsið er uppfærð í **Móttekið** og staða úthreyfingarfærslunnar fyrir biðgeymsluvöruhúsið er uppfærð í **Frádregið**.</p><p>Nýju færslurnar tvær eru notaðar til að gefa til kynna flutning til baka í geymsluvöruhúsið. Innhreyfingarfærslan er með stöðuna **Pantað** fyrir geymsluvöruhúsið og úthreyfingarfærslan er með stöðuna **Frátekið efnislegt** fyrir biðgeymsluvöruhúsið.</p><p>Þegar biðgeymslupöntun er skráð sem lokið stendur þessi aðgerð fyrir efnislega uppfærslu á biðgeymslupöntuninni. Staða innhreyfingar í geymsluvöruhúsinu er uppfærð í **Móttekið**.</p><p>Þegar biðgeymslupöntuninni lýkur stendur þessi aðgerð fyrir fjárhagslega uppfærslu biðgeymslupöntunarinnar. Staða úthreyfingarfærslunnar er uppfærð í **Selt** og staða innhreyfingarfærslunnar er uppfærð í **Keypt**.</p><p>Einnig er hægt að sleppa biðgeymslupöntuninni. Þessi aðgerð fjarlægir vöruna úr birgðum. Þegar biðgeymslupöntun er rýrnuð eru aðeins þrjár færslur eftir. Innhreyfingarfærslan fyrir geymsluvöruhúsið er fjarlægð og staða eftirstandandi innhreyfingarfærslu er uppfærð í **Keypt**. Staða völdu úthreyfingarfærslnanna tveggja er uppfærð í **Selt**. Þessi aðgerð er efnisleg og fjárhagsleg uppfærsla fyrir pöntunina.</p> |

## <a name="fixed-receipt-price-posting"></a>Bókun á föstu verði innhreyfingar

Fast innhreyfingarverð gerir þér kleift að nota staðalkostnað fyrir afurð. Önnur leið er að velja valkostinn **Staðalkostnaður** á síðunni **Vörulíkanaflokkur** fyrir vöru. Helsti munurinn þegar notað er fast innhreyfingarverð er að kostnaðarverðið sem er nú þegar skilgreint verður notað fyrir vöruna þegar innhreyfing í birgðir er bókuð. Ekkert endurmatsferli kostnaðar er til fyrir fast verð innhreyfingar. Þegar fjárhagsleg uppfærsla er bókuð er núverandi kostnaðarverð notað við bókun. Ef kostnaðarverð sem notað er við innhreyfingu og reikningurinn er annar verður frávikið bókað á fastan rekstrarreikning.

Til að eiga möguleikann á því að nota fast verð innhreyfingar fyrir afurð þarf að ljúka eftirfarandi grunnstillingu:

- Veldu gátreitinn **Bóka efnislegar birgðir** á síðunni **Vörulíkanaflokkur** fyrir vöruna sem er valin í birgðafærslulínunni.
- Veldu gátreitinn **Fast innhreyfingarverð** á síðunni **Vörulíkanaflokkur**.
- Tilgreindu aðallyklana fyrir eftirfarandi bókunargerðir á síðunni **Birgðabókunarregla**:

    - Hagnaður á föstu verði innhreyfingar
    - Tap á föstu verði innhreyfingar

Frekari upplýsingar eru í [Fast kostnaðarverð](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Bókun þyngdar afurðar

Afurðir í framleiðsluþyngd eru oft notaðar í atvinnugreinum þar sem þyngd og/eða stærð afurða er mismunandi, t.d. í matvælaiðnaði. Afurðir í framleiðsluþyngd nota tvær mælieiningar: birgðaeiningu og framleiðsluþyngdareiningu. Þyngd birgða þegar þær koma inn í vöruhús getur verið frábrugðin þyngdinni þegar birgðir eru losaðar út úr vöruhúsinu. Þyngd afurðar við vinnslu afurðar leiðréttir birgðir.

Ef frávik er á framleiðsluþyngd er munurinn bókaður á lyklana sem eru tilgreindir í reitunum **Tap framleiðsluþyngdar** og **Hagnaður framleiðsluþyngdar** á síðunni **Birgðabókunarregla**. Yfirleitt er sami aðallykill tilgreindur í báðum reitum.

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir og inniheldur sýnidæmi aðallykla og lýsingar.

- „Debet/kredit?“ dálkur segir til um hvort færslan er yfirleitt debet eða kredit. Í sumum tilvikum getur færslan bókað annaðhvort debet eða kredit.
- Dálkurinn „Millireikningur“ gefur til kynna að bókunargerðin sé millireikningur. Þ.e. upphæðin sem er bókuð á þennan lykil er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslu. „P“ stendur fyrir bókun og „F“ stendur fyrir fjárhagslega bókun.
- Dálkurinn „Fylgja“ gefur til kynna hvort aðallykillinn fyrir bókunargerðina sé yfirleitt sá sami og aðallykillinn fyrir aðra bókunargerð. Nánar tiltekið gefur hann til kynna bókunargerðina sem er yfirleitt notuð við bókun.

> [!NOTE]
> Aðallyklarnir og heiti aðallykla í töflunni eru tillögur. Mælt er með að þú vinnir með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Taplykill sökum þyngdar afurðar | 510520 | Leiðrétting birgða | Kostnaður | | Nr. | Bæði | Hagnaðarlykill sökum þyngdar afurðar | Þessi lykill er notaður þegar birgðafærsla er bókuð þar sem magn framleiðsluþyngdar er lægra. |
| Hagnaðarlykill sökum þyngdar afurðar | 510520 | Leiðrétting birgða | Kostnaður | | Nr. | Bæði | Taplykill sökum þyngdar afurðar | Þessi lykill er notaður þegar birgðafærsla er bókuð þar sem magn framleiðsluþyngdar er hærra. |

Frekari upplýsingar um afurðir framleiðsluþyngdar er að finna í [Um vörur með framleiðsluþyngd](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) og [Úrvinnsla á afurð með framleiðsluþyngd](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Bókun birgðafærslu í eignir

Birgðirnar í eignabók (**Eignir** \> **Færslubækur** \> **Birgðir í eignabók**) eru notaðar til að flytja vörur úr birgðum og breyta þeim í eignir. Frekari upplýsingar eru í [Samþætting eigna](/fixed-assets/fixed-asset-integration.md).

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir og inniheldur sýnidæmi aðallykla og lýsingar.

- „Debet/kredit?“ dálkur segir til um hvort færslan er yfirleitt debet eða kredit. Í sumum tilvikum getur færslan bókað annaðhvort debet eða kredit.
- Dálkurinn „Millireikningur“ gefur til kynna að bókunargerðin sé millireikningur. Þ.e. upphæðin sem er bókuð á þennan lykil er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslu. „P“ stendur fyrir bókun og „F“ stendur fyrir fjárhagslega bókun.
- Dálkurinn „Fylgja“ gefur til kynna hvort aðallykillinn fyrir bókunargerðina sé yfirleitt sá sami og aðallykillinn fyrir aðra bókunargerð. Nánar tiltekið gefur hann til kynna bókunargerðina sem er yfirleitt notuð við bókun.

> [!NOTE]
> Aðallyklarnir og heiti aðallykla í töflunni eru tillögur. Mælt er með að þú vinnir með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Úthreyfing eignar | 180100 | Efnislegar eignir | Eign | Kredit | Nr. | Bæði | Á ekki við | Þessi lykill er notaður þegar birgðir eru bókaðar í eignabók til að fjarlægja vöru úr birgðum og breyta þeim í eign. |

## <a name="moving-average-posting"></a>Bókun hlaupandi meðaltals

Hlaupandi meðaltal er varanlegur kostnaðarútreikningur sem byggir á hugmyndinni um meðaltal. Kostnaður vegna úthreyfinga birgða breytist ekki þegar innkaupakostnaður breytist. Mismunurinn er eignfærður og byggir á hlutfallsútreikningi. Eftirstandandi upphæð er skráð sem kostnaður.

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðallyklum og lýsingum.

- „Debet/kredit?“ dálkur segir til um hvort færslan er yfirleitt debet eða kredit. Í sumum tilvikum getur færslan bókað annaðhvort debet eða kredit.
- Dálkurinn „Millireikningur“ gefur til kynna að bókunargerðin sé millireikningur. Þ.e. upphæðin sem er bókuð á þennan lykil er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslu. „P“ stendur fyrir bókun og „F“ stendur fyrir fjárhagslega bókun.
- Dálkurinn „Fylgja“ gefur til kynna hvort aðallykillinn fyrir bókunargerðina sé yfirleitt sá sami og aðallykillinn fyrir aðra bókunargerð. Nánar tiltekið gefur hann til kynna bókunargerðina sem er yfirleitt notuð við bókun.

> [!NOTE]
> Aðallyklarnir og heiti aðallykla í töflunni eru tillögur. Mælt er með að þú vinnir með endurskoðanda þínum til að finna út bestu stillingarnar fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Verðmunur á hlaupandi meðaltali | 510600 | Hlaupandi meðaltal verðmunar | Kostnaður | Bæði | Nr. | Bæði | Á ekki við | Þessi lykill er notaður þegar það er munur á kostnaði milli innhreyfingar og reiknings. |
| Endurmat á hlaupandi meðaltali | 510610 | Færir meðaltal endurmats | Kostnaður | Bæði | Nr. | Bæði | Á ekki við | Þessi lykill er notaður þegar kostnaður hlaupandi meðaltals fyrir afurð er leiðréttur |

## <a name="sample-posting-profile-configuration"></a>Skilgreining prófunarbókunarreglu

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðallyklum og lýsingum.

| Bókunargerð | Dæmi um aðallykil | Dæmi um heiti aðallykils | Lykilgerð | Debet/Kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Birgðavandamál | 140100 | Efnisbirgðir | Eign | Kredit | Nr. | Bæði | Innhreyfing birgða | Þessi lykill er notaður þegar birgðafærsla sem er bókuð er úthreyfing (neikvætt magn) og tengist ekki sölu, innkaupum eða framleiðslu. Mótlykill við þennan lykil er birgðaútgjöldin, taplykill. Þessi lykill sýnir yfirleitt birgðir á efnahagsreikningi. |
| Birgðaútgjöld, tap | 510100 | Birgðahagnaður og tap | Kostnaður | Debet | Nr. | Bæði | Birgðaútgjöld, hagnaður | Þessi lykill er notaður þegar birgðafærsla sem er bókuð er úthreyfing (neikvætt magn) og tengist ekki sölu, innkaupum eða framleiðslu. Mótlykill við þennan lykil er birgðaúthreyfingarlykillinn. |
| Innhreyfing birgða | 140100 | Efnisbirgðir | Eign | Debet | Nr. | Bæði | Birgðavandamál | Þessi lykill er notaður þegar birgðafærsla sem er bókuð sem innhreyfing (jákvætt magn) og tengist ekki sölu, innkaupum eða framleiðslu. Mótlykill við þennan lykil er birgðaútgjöld, hagnaðarlykill. Þessi lykill sýnir yfirleitt birgðir á efnahagsreikningi. |
| Birgðaútgjöld, hagnaður | 510100 | Birgðahagnaður og tap | Kostnaður | Kredit | Nr. | Bæði | Birgðaútgjöld, tap | Þessi lykill er notaður þegar birgðafærsla sem er bókuð sem innhreyfing (jákvætt magn) og tengist ekki sölu, innkaupum eða framleiðslu. Mótlykill við þennan lykil er birgðainnhreyfingarlykillinn. |
| Millieining, lánardrottnar | 231500 | Interunit viðskiptaskuld | Bótaábyrgð | Debet | Nr. | Bæði | | Þessi lykill er notaður þegar birgðir eru fluttar á milli birgðavídda eins og svæða og kostnaður vöru er mismunandi á milli svæða. |
| Millieining, viðskiptavinir | 131500 | Interunit viðskiptakröfur | Eign | Kredit | Nr. | Bæði | | Þessi lykill er notaður þegar birgðir eru fluttar á milli birgðavídda eins og svæða og kostnaður vöru er mismunandi á milli svæða. |
