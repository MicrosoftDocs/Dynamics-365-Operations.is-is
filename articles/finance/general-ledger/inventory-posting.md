---
title: Birgðabókun
description: Þetta efni útskýrir flipann Birgðabókun á prófílsíðunni Birgðabókun.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783330"
---
# <a name="inventory-posting"></a>Birgðabókun

The **Birgðir** flipann á **Skráningarsnið** síða er notuð til að stjórna því hvernig birgðafærslur eru bókaðar í fjárhag. Birgðafærslur eru færslur sem eru ekki búnar til úr sölupöntunum, innkaupapantunum eða framleiðslupöntunum. Þeir birta sjálfkrafa líkamlegar og fjárhagslegar uppfærslur á birgðahaldinu samtímis. Ein undantekning eru millifærslupantanir sem aðgreina líkamlegar og fjárhagslegar uppfærslur þegar þú sendir og tekur á móti birgðum.

Eftirfarandi tafla sýnir nokkur dæmi um birgðafærslur.

| Færslugerð | Kvittun eða útgáfa | Líkamleg færslu, fjárhagsfærsla eða hvort tveggja | Lýsing |
|---|---|---|---|
| Hreyfing | Bæði | Bæði | <p>Hreyfingarbók er birgðabók sem þú getur notað til að bæta við eða fjarlægja birgðahald. Það virkar eins og birgðaleiðréttingarbók. Hins vegar er einn lykilmunur sá að aðalreikningurinn sem vegur á móti færslunni er tilgreindur.</p><p>Hreyfibókin færir upphafsstöður og einskiptisleiðréttingar sem þarf að gjaldfæra. Til dæmis er það notað þegar birgðir eru fjarlægðar fyrir sölusýni.</p><p>Þegar færslubókin er bókuð eiga sér stað líkamlegar og fjárhagslegar uppfærslur samtímis.</p><p>Jákvætt magn á færslubókarlínunum táknar innhreyfingar og neikvætt magn táknar útgáfur.</p> |
| Leiðrétting birgða | Bæði | Bæði | Birgðaleiðréttingarbók er notuð til að bæta við eða fjarlægja birgðir. Það leyfir þér ekki að velja mótreikning. Aðeins þeir reikningar sem tilgreindir eru á **Birgðafærslusnið** síðu eru notuð til að uppfæra aðalbókarfærsluna. |
| Flutningur (dagbók) | Bæði | Bæði | <p>Flutningabók er notuð til að flytja birgðir frá einum stað til annars (með því að nota geymsluvíddir). Það uppfærir vöruupplýsingarnar um birgðafærslu með nýrri vöru eða rakningarvíddum.</p><p>Flutningabók býr til eina línu fyrir hreyfingu vöru. Þessi lína hefur "frá" og "til" reiti fyrir birgðavíddir. Hver lína í flutningsbók býr til tvær birgðafærslur. Ein færsla er búin til fyrir "frá" birgðavíddir. Það táknar málið og hefur neikvætt magn. Hin færslan er búin til fyrir "til" birgðavíddir. Það táknar kvittunina og hefur jákvætt magn.</p><p>Flutningabækur gætu ekki búið til fylgiskjöl ef flutningur á birgðum er talin vera ófjárhagsleg millifærsla. Birgðavíddir sem eru mismunandi fyrir gildin „frá“ og „til“ eru ekki merktar með **Fjárhagsskrá** valmöguleika á **Geymsluvíddarhópur** eða **Rekjavíddarhópur** síðu. Til dæmis, ef **Fjárhagsskrá** valkostur er ekki merktur á **Staðsetning** vídd, og þú færir birgðir frá einni staðsetningu til annarrar á sömu síðu og vöruhúsi, er engin fylgiskjöl búin til.</p><p>Flutningsbækur eru frábrugðnar flutningspöntunum að því leyti að engin skjöl eru til fyrir hreyfinguna. Uppfærslan er gerð í einni færslu með því að bóka færslubókina. Aftur á móti getur millifærslupöntun búið til tínslu- og sendingarskjöl og krefst tveggja uppfærslu til að vinna úr færslunni.</p> |
| Flutningspöntunarsending | Gefa út | Bæði | <p>Þegar þú býrð til nýja flutningspöntun hefur hver samsetning af línu og birgðavídd tvær birgðafærslur: eina fyrir flutningspöntunarsendinguna og eina fyrir flutningspöntunarkvittunina. Þegar þú sendir flutningspöntunina eru tvær birgðafærslur uppfærðar og tvær birgðafærslur til viðbótar eru búnar til fyrir flutning á vörum, samtals fjórar birgðafærslur.</p><ol><li>Fyrsta birgðafærslan er notuð til að fjarlægja vöruna úr upprunavöruhúsi og staðsetningu. Útgáfustaða þessarar færslu er **Seldur** til að gefa til kynna að varan sé ekki lengur til í vöruhúsinu.</li><li>Önnur birgðafærslan er notuð til að bæta vörunni við flutningsvöruhúsið sem er valið fyrir vöruhúsið sem verið er að flytja vöruna frá. Kvittunarstaða þessarar færslu er **Keypt**.</li><li>Þriðja birgðafærslan er fyrir flutning frá flutningsvöruhúsi yfir í ákvörðunarvöruhús. Útgáfustaða þessarar færslu er **Frátekið líkamlegt**. Þessi staða tryggir að ekki sé hægt að neyta vörunnar í öðru ferli á meðan hún er enn í flutningi.</li><li>Fjórða birgðafærslan er fyrir móttöku á vörum í áfangavörugeymslunni. Kvittunarstaða þessarar færslu er **Pantaði**.</li></ol> |
| Móttaka flutningspöntunar | Innhreyfing | Bæði | Þegar flutningspöntun er móttekin í áfangageymslunni er birgðastaða birgðafærslunnar sem er í flutningsvöruhúsinu (númer 3 í dæminu á undan) uppfærð í **Seldur**, og birgðastaða birgðafærslunnar fyrir áfangavöruhús er uppfærð í **Keypt**. |
| Uppskriftir | Bæði | Bæði | Hægt er að nota efnisyfirlit (BOM) dagbók til að tilkynna vöru sem fullunna og neyta hráefnis sem var neytt í ferlinu án þess að nota framleiðslupöntun. Uppskriftarbók inniheldur venjulega að minnsta kosti eina jákvæða línu fyrir fullunna vöru og eina eða fleiri neikvæðar línur fyrir hráefnin sem verið er að neyta. Fullunnin vörulínan er kvittun í birgðum en neikvæðu línurnar eru útgáfur úr birgðum fyrir hráefnin. Þegar þú býrð til uppskriftarbók er fyrsta línan uppskriftarhaus og síðari línur sem bætast við eru uppskriftarlínur. |
| Eignarhaldsbreyting birgða | Bæði | Bæði | Breytingabók birgðaeignarhalds er notuð til að breyta eignarhaldi á sendum birgðum frá lánardrottni til fyrirtækis þíns. Birgðabreytingarbækur líkjast birgðaflutningsbókum að því leyti að tvær birgðafærslur eru tengdar hverri samsetningu línu og birgðavídd. Ein birgðafærsla fjarlægir birgðina frá lánardrottni í **Eignarhald** vídd, og hinn bætir hlutnum við lögaðilann í **Eignarhald** vídd. |
| Vörumóttaka | Innhreyfing | Efnislegt | Vörufærslubók er notuð til að uppfæra innhreyfingarstöðu birgða í **Skráður**. Það er venjulega notað fyrir móttöku innkaupapöntunar á vörum og sölupöntunarskilum. |
| Framleiðsluinntak | Innhreyfing | Efnislegt | Framleiðsluinntaksbók líkist komufærslubók vöru. Framleiðsluinntak er notað til að taka á móti fullunnum vörum úr framleiðslupöntun í vöruhúsinu. Þegar færslubókin er bókuð er staða birgðafærslunnar uppfærð í **Skráður**. |
| Talning | Bæði | Bæði | Talningarbók er notuð til að skrá magn vöru sem var talið fyrir tiltekna samsetningu birgðavídda. Birgðafærslur eru stofnaðar þegar lína færslubókarinnar hefur talningarmun. Lína sem hefur hærra talið magn veldur innhreyfingu í birgðum. Lína sem hefur lægra talið magn veldur vandamáli úr birgðum. Línur þar sem talið magn samsvarar væntu magni hafa engar birgðafærslur. |
| Seðlatalning | Á ekki við | Á ekki við | Merkjatalningarbók er notuð til að rekja birgðamerki sem eru úthlutað og notuð í fullri birgðatalningu. Þú getur notað færslubókina til að úthluta merkinúmeri á tiltekna samsetningu af vöru og birgðavídd og til að fylgjast með stöðu þess merkis meðan á fullri birgða stendur. Merkjatalningarbækur búa ekki til birgðafærslur. |
| Gæðapantanir | Gefa út | Efnislegt | <p>Gæðapöntun er notuð til að skrá prófunarniðurstöður fyrir tiltekna lotu í birgðum. Hver gæðapöntun tengist núverandi birgðafærslu eða hluta af birgðafærslu.</p><p>Gæðapöntun mun búa til nýja birgðafærslu við tvær aðstæður:</p><ul><li>Gæðapöntunin er merkt sem **Eyðileggjandi próf** á **Almennt** flipa.</li><li>Gæðapöntunin er merkt sem **Sóttkví við staðfestingarbilun** á **Almennt** flipa, og prófið stenst ekki löggildinguna. Í þessu tilviki eru tvær birgðafærslur búnar til. Ein birgðafærsla fjarlægir vöruna úr upprunalegu birgðavíddarsamsetningu og staðsetningu, og hin bætir vörunni við sóttkví vöruhús.</li></ul> |
| Biðgeymslupantanir | Bæði | Bæði | <p>Birgðafærslur sóttkvíarpantana eru eins og millifærslupöntun. Sóttvarnarhús er notað til að rekja birgðahaldið. Um er að ræða tvær kvittunarfærslur og tvær útgáfufærslur.</p><p>Þegar þú stofnar pöntunina upphaflega eru tvær færslur búnar til. Kvittun færslan hefur stöðuna **Pantaði** fyrir sóttkví vöruhús sem er tengt vöruhúsinu þar sem varan er staðsett. Útgáfuviðskiptin hafa stöðuna **Á pöntun** fyrir vöruhúsið þar sem varan er geymd.</p><p>Þegar þú byrjar sóttkvíarpöntunina eru tvær færslur til viðbótar búnar til og núverandi færslur eru uppfærðar. Staða móttökufærslunnar fyrir sóttkví vöruhús er uppfærð í **Tekið á móti**, og staða útgáfufærslunnar fyrir geymsluvöruhúsið er uppfærð í **Dregið frá**.</p><p>Nýju færslurnar tvær eru notaðar til að gefa til kynna endanlega hreyfingu til baka í vörugeymsluna. Kvittun færslan hefur stöðuna **Pantaði** fyrir vörugeymsluna og sú útgáfufærsla hefur stöðuna **Frátekið líkamlegt** fyrir sóttvarnargeymsluna.</p><p>Þegar þú tilkynnir sóttkvíarpöntun sem lokið, táknar þessi aðgerð líkamlega uppfærslu sóttkvíarpöntunarinnar. Innhreyfingarstaða í geymsluvöruhúsi er uppfærð í **Tekið á móti**.</p><p>Þegar þú lýkur sóttkvíarpöntuninni táknar þessi aðgerð fjárhagsuppfærslu sóttkvíarpöntunarinnar. Staða útgáfuviðskipta er uppfærð í **Seldur**, og staða kvittunarfærslna er uppfærð í **Keypt**.</p><p>Að öðrum kosti geturðu fellt niður sóttkvíarpöntunina. Þessi aðgerð fjarlægir vöruna úr birgðum. Þegar þú fellir niður sóttkvíarpöntun eru aðeins þrjár færslur eftir. Móttökufærslan fyrir vörugeymsluna er fjarlægð og staða kvittunarfærslunnar sem eftir er er uppfærð í **Keypt**. Staða útgáfuviðskiptanna tveggja er uppfærð í **Seldur**. Þessi aðgerð er líkamleg og fjárhagsleg uppfærsla fyrir pöntunina.</p> |

## <a name="fixed-receipt-price-posting"></a>Föst kvittun verðbókun

Fast kvittunarverð gerir þér kleift að nota staðlaðan kostnað fyrir vöru. Það er valkostur við að velja **Staðalkostnaður** valmöguleika á **Vörulíkanahópur** síðu fyrir hlut. Helsti munurinn þegar þú notar fast innhreyfingarverð er að kostnaðarverðið sem nú er stillt verður notað fyrir vöruna þegar innhreyfingin í birgðum er bókuð. Ekkert endurmatsferli er fyrir föstu kvittunarverði. Þegar fjárhagsuppfærsla er bókuð er núverandi kostnaðarverð notað við bókun. Ef kostnaðarverð sem notað er við móttöku og reikningur er ólíkt verður frávikið bókað á fasta innhreyfingarverðs rekstrarreikninga.

Til að nota fast kvittunarverð fyrir vöru, verður þú að ljúka eftirfarandi uppsetningu:

- Veldu **Bókaðu efnislegar birgðir** gátreitinn á **Vörulíkanahópur** síðu fyrir vöruna sem er valin í birgðafærslulínunni.
- Veldu **Fast kvittunarverð** gátreitinn á **Vörulíkanahópur** síðu.
- Tilgreindu aðalreikninga fyrir eftirfarandi bókunargerðir á **Birgðafærslusnið** síða:

    - Hagnaður á föstu verði innhreyfingar
    - Tap á föstu verði innhreyfingar

Fyrir frekari upplýsingar, sjá [Fast kvittunarverð](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Birting aflaþyngdar

Aflaþyngdarvörur eru oft notaðar í iðnaði eins og matvælaiðnaði, þar sem vörur geta verið örlítið mismunandi eftir þyngd, stærð eða hvort tveggja. Aflaþungaafurðir nota tvær mælieiningar: birgðaeiningar og aflaþungaeiningu. Vægi birgða þegar það kemur inn í vöruhús getur verið frábrugðið þyngdinni þegar birgðin er gefin út úr vöruhúsinu. Vöruvinnsla aflaþyngdar stillir birgðahaldið.

Ef frávik er í aflaþyngd er mismunurinn færður á þá reikninga sem tilgreindir eru í **Náðu í þyngdartap** og **Aflaþyngd hagnaður** sviðum á **Birgðafærslusnið** síðu. Venjulega er sami aðalreikningur tilgreindur í báðum reitunum.

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir og inniheldur sýnishorn af aðalreikningum og lýsingum.

- "Debet/kredit?" Dálkurinn gefur til kynna hvort viðskiptin eru venjulega debet eða kredit. Í sumum tilfellum getur færslan bókað annað hvort skuldfærslur eða inneignir.
- Dálkurinn „Jöfnunarreikningur“ gefur til kynna að bókunartegundin sé jöfnunarreikningur. Með öðrum orðum, upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslunnar. "P" táknar líkamlega bókun og "F" táknar fjárhagslega bókun.
- Dálkurinn „Fylgjast með“ gefur til kynna hvort aðalreikningur bókunartegundarinnar sé venjulega sá sami og aðalreikningur annarrar bókunartegundar. Nánar tiltekið gefur það til kynna færslugerðina sem venjulega er notuð fyrir færsluna.

> [!NOTE]
> Aðalreikningar og heiti aðalreikninga í töflunni eru tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Taplykill sökum þyngdar afurðar | 510520 | Leiðrétting birgða | Kostnaður | | Nr. | Bæði | Hagnaðarlykill sökum þyngdar afurðar | Þessi reikningur er notaður þegar þú bókar birgðafærslu þar sem magn aflaþyngdar er lægri. |
| Hagnaðarlykill sökum þyngdar afurðar | 510520 | Leiðrétting birgða | Kostnaður | | Nr. | Bæði | Taplykill sökum þyngdar afurðar | Þessi reikningur er notaður þegar þú bókar birgðafærslu þar sem magn aflaþyngdar er hærri. |

Fyrir frekari upplýsingar um aflaþyngdarvörur, sjá [Um aflaþyngdarhluti](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) og [Vöruvinnsla aflaþyngdar með vöruhúsastjórnun](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Birgðir í eignaflutningsbókun

Birgðir í eignabók (**Fastafjármunir** \> **Tímarit** \> **Birgðir í eignabók**) er notað til að færa vörur úr birgðum og breyta þeim í fastafjármuni. Frekari upplýsingar eru í [Samþætting eigna](/fixed-assets/fixed-asset-integration.md).

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir og inniheldur sýnishorn af aðalreikningum og lýsingum.

- "Debet/kredit?" Dálkurinn gefur til kynna hvort viðskiptin eru venjulega debet eða kredit. Í sumum tilfellum getur færslan bókað annað hvort skuldfærslur eða inneignir.
- Dálkurinn „Jöfnunarreikningur“ gefur til kynna að bókunartegundin sé jöfnunarreikningur. Með öðrum orðum, upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslunnar. "P" táknar líkamlega bókun og "F" táknar fjárhagslega bókun.
- Dálkurinn „Fylgjast með“ gefur til kynna hvort aðalreikningur bókunartegundarinnar sé venjulega sá sami og aðalreikningur annarrar bókunartegundar. Nánar tiltekið gefur það til kynna færslugerðina sem venjulega er notuð fyrir færsluna.

> [!NOTE]
> Aðalreikningar og heiti aðalreikninga í töflunni eru tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Úthreyfing eignar | 180100 | Varanlegir fastafjármunir | Eign | Kredit | Nr. | Bæði | Á ekki við | Þessi reikningur er notaður þegar þú bókar birgðir í eignabók til að fjarlægja vöru úr birgðum og breyta henni í eign. |

## <a name="moving-average-posting"></a>Færð meðaltal færslna

Hreyfanlegt meðaltal er ævarandi kostnaðaraðferð sem byggir á meðaltalsreglunni. Kostnaður vegna birgðaútgáfu breytist ekki þegar innkaupakostnaður breytist. Mismunurinn er eignfærður og byggir á hlutfallsútreikningi. Eftirstandandi upphæð er skráð sem kostnaður.

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðalreikningum og lýsingum.

- "Debet/kredit?" Dálkurinn gefur til kynna hvort viðskiptin eru venjulega debet eða kredit. Í sumum tilfellum getur færslan bókað annað hvort skuldfærslur eða inneignir.
- Dálkurinn „Jöfnunarreikningur“ gefur til kynna að bókunartegundin sé jöfnunarreikningur. Með öðrum orðum, upphæðin sem er bókuð á þessum reikningi er sjálfkrafa bakfærð þegar síðari færsla er bókuð.
- Dálkurinn „P/F“ sýnir tegund færslunnar. "P" táknar líkamlega bókun og "F" táknar fjárhagslega bókun.
- Dálkurinn „Fylgjast með“ gefur til kynna hvort aðalreikningur bókunartegundarinnar sé venjulega sá sami og aðalreikningur annarrar bókunartegundar. Nánar tiltekið gefur það til kynna færslugerðina sem venjulega er notuð fyrir færsluna.

> [!NOTE]
> Aðalreikningar og heiti aðalreikninga í töflunni eru tillögur. Við mælum með því að þú vinnur með endurskoðanda þínum til að ákvarða bestu uppsetninguna fyrir viðskiptaþarfir þínar.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Verðmunur á hlaupandi meðaltali | 510600 | Hreyfanlegur meðalverðsmunur | Kostnaður | Bæði | Nr. | Bæði | Á ekki við | Þessi reikningur er notaður þegar munur er á kostnaði á milli kvittunar og reiknings. |
| Endurmat á hlaupandi meðaltali | 510610 | Færir meðaltal endurmats | Kostnaður | Bæði | Nr. | Bæði | Á ekki við | Þessi reikningur er notaður þegar þú stillir meðaltalskostnað vöru |

## <a name="sample-posting-profile-configuration"></a>Dæmi um stillingar fyrir færslusnið

Eftirfarandi tafla sýnir dæmi um sjálfgefnar bókunargerðir með sýnishorn af aðalreikningum og lýsingum.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | P/F | Fylgja | Lýsing |
|---|---|---|---|---|---|---|---|---|
| Birgðavandamál | 140100 | Efnisskrá | Eign | Kredit | Nr. | Bæði | Innhreyfing birgða | Þessi reikningur er notaður þegar birgðafærsla sem er bókuð er vandamál (neikvætt magn) og tengist ekki sölu, innkaupum eða framleiðslu. Jöfnun á þennan reikning er birgðaútgjöld, tapsreikningur. Þessi reikningur táknar venjulega birgðir í efnahagsreikningi. |
| Birgðaútgjöld, tap | 510100 | Hagnaður og tap birgða | Kostnaður | Debet | Nr. | Bæði | Birgðaútgjöld, hagnaður | Þessi reikningur er notaður þegar birgðafærsla sem er bókuð er vandamál (neikvætt magn) og tengist ekki sölu, innkaupum eða framleiðslu. Jöfnun á þennan reikning er birgðaútgáfureikningur. |
| Innhreyfing birgða | 140100 | Efnisskrá | Eign | Debet | Nr. | Bæði | Birgðavandamál | Þessi reikningur er notaður þegar birgðafærsla sem er bókuð er kvittun (jákvætt magn) og er ekki tengd sölu, innkaupum eða framleiðslu. Jöfnun á þennan reikning er birgðaútgjöld, hagnaðarreikningur. Þessi reikningur táknar venjulega birgðir í efnahagsreikningi. |
| Birgðaútgjöld, hagnaður | 510100 | Hagnaður og tap birgða | Kostnaður | Kredit | Nr. | Bæði | Birgðaútgjöld, tap | Þessi reikningur er notaður þegar birgðafærsla sem er bókuð er kvittun (jákvætt magn) og er ekki tengd sölu, innkaupum eða framleiðslu. Jöfnun á þennan reikning er birgðakvittun. |
| Millieining, lánardrottnar | 231500 | Greiðsla milli eininga | Skuld | Debet | Nr. | Bæði | | Þessi reikningur er notaður þegar birgðir eru fluttar á milli birgðavídda eins og vefsvæða og kostnaður við vöru er mismunandi á milli vefsvæða. |
| Millieining, viðskiptavinir | 131500 | Kröfur milli eininga | Eign | Kredit | Nr. | Bæði | | Þessi reikningur er notaður þegar birgðir eru fluttar á milli birgðavídda eins og vefsvæða og kostnaður við vöru er mismunandi á milli vefsvæða. |
