---
title: Munur á fínstillingu skipuluagningar og úreltri aðaláætlunarvél
description: Í þessari grein eru sýndir eiginleikar sem fínstilling áætlanagerðar styður ekki enn sem komið er og sem eru ekki sýndir á síðunni Samræmisgreining fyrir fínstillingu áætlanagerðar.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745362"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Munur á fínstillingu skipuluagningar og úreltri aðaláætlunarvél

[!include [banner](../../includes/banner.md)]

Niðurstöður fínstillingar skipulagningar gætu verið frábrugðnar niðurstöðum úr úreltu aðaláætlunarvélinni. Munurinn getur stafað af eiginleikum sem eru í biðstöðu. Í þessari grein eru sýndir eiginleikar sem fínstilling áætlanagerðar styður ekki enn sem komið er og sem eru ekki sýndir á síðunni **[Samræmisgreining fyrir fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)**].

| Eiginleiki | Núverandi hegðun í fínstillingu áætlanagerðar |
|---|---|
| Framleiðsluþyngdarafurðir | Litið er á afurðir með framleiðsluþyngd sem venjulegar afurðir.|
| Stækkanlegar víddir | Fínstilling áætlanagerðar styður ekki stækkanlegar víddir. Þegar fínstilling skipulagningar eru notuð eru stækkanlegar víddir í áætluðum pöntunum, jafnvel þegar gátreiturinn **Þekjuáætlun eftir vídd** er valinn á síðunni **Geymsluvíddarflokkar** eða **Rakningarvíddarflokkar**. |
| Keyrslur síaðrar framleiðslu | Nánari upplýsingar er að finna í [Framleiðsluáætlun - Síur](production-planning.md#filters). |
| Spáráætlun | Spáráætlun er ekki studd. Við mælum með því að aðaláætlanagerð sé notuð þar sem spárlíkani er úthlutað á aðaláætlunina. |
| Númeraraðir fyrir áætlaðar pantanir | Númeraraðir fyrir áætlaðar pantanir eru ekki studdar. Númer áætlaðra pantana eru búin til þjónustumegin. Áætlað pöntunarnúmer er yfirleitt sýnt með 10 stöfum, en röðin er í raun byggð á 20 stöfum, með 10 stöfum úthlutuðum fyrir áætlunarkeyrslutalningu og 10 stöfum fyrir talningu á áætluðum pöntunum. |
| Afrit áætlunar, eyða áætlun og hreinsun á útgáfu áætlunar | <p>Eftirfarandi atriði eru gerð óvirk undir **Aðaláætlanagerð \> Aðaláætlanagerð \> Vinna með áætlanir** í yfirlitssvæðinu:</p><ul><li>Afrit áætlunar</li><li>Eyða áætlun</li><li>Tiltekt áætlunarútgáfu</li></ul> |
| Skilapantanir | Skilapantanir eru ekki teknar til greina. |
| Tengdir eiginleikar tímasettir | Frekari upplýsingar er að finna í [Röðun með ótakmarkaða getu](infinite-capacity-planning.md#limitations). |
| Uppfylling öryggisbirgða | Fínstilling áætlanagerðar notar alltaf valkostinn *Dagurinn í dag + öflunartími* fyrir reitinn **Uppfylla lágmark** á síðunni **Vöruþekja**. Þetta hjálpar til við að koma í veg fyrir óæskilegar áætlaðar pantanir og önnur vandamál vegna þess að ef öflunartíminn er ekki hafður með í öryggisbirgðum, verða alltaf tafir á áætluðum pöntunum sem búnar eru til vegna afhendingartíma. |
| Þarfarakning öryggisbirgða og nettóþarfir | Þarfagerð *Öryggisbirgða* er ekki tekin með og er ekki sýnd á síðunni **Nettóþarfir**. Öryggisbirgðir endurspegla ekki eftirspurn og eru ekki með þarfadagsetningu tengda við sig. Þess í stað setja þær takmarkanir á hversu miklar birgðir þurfa að vera til staðar á hverjum tíma. Hins vegar er reitargildið **Lágmark** áfram tekið til greina þegar áætlaðar pantanir eru reiknaðar í aðaláætlanagerð. Við mælum með að þú skoðir dálkinn **Uppsafnað magn** á síðunni **Nettóþarfir** til að sjá að þetta gildi var tekið til greina. Vegna þess að þarfarakningin er öðruvísi verður hugsanlega stungið upp á öðrum aðgerðum. |
| Flutningsdagatöl | Gildið í dálknum **Flutningsdagatal** á síðunni **Afhendingarmátar** er hunsað. |
| Lágm./hám. þekjukóði án gildis| Með úreltri aðaláætlunarvél, þegar þú notar lágm/hám þekjukóða þar sem engin lágmarks- eða hámarksgildi eru stillt, lítur áætlunarvélin á þekjukóðann sem þörf og stofnar eina pöntun fyrir hverja þörf. Með fínstillingu áætlanagerðar mun kerfið stofna eina pöntun á dag til að ná yfir alla upphæðina fyrir þann dag.  |
| Nettó kröfur og áætlaðar pantanir búnar til handvirkt | Með úreltri aðaláætlunarvél birtast handvirkt stofnaðar birgðapantanir fyrir vöru sjálfkrafa á meðal nettóþarfa fyrir þá vöru. Til dæmis, þegar innkaupapöntun er stofnuð úr sölupöntun, birtist innkaupapöntunin á **Nettóþarfir** án þess að þörf sé á neinum aðgerðum. Þetta er vegna þess að úrelta aðaláætlunarvélin skráir birgðafærslur í töfluna `inventLogTTS` og sýnir breytingar á síðunni **Nettóþarfir** fyrir kvikar áætlanir. Með fínstillingu áætlanagerðar munu handvirkt stofnaðar pantanir hins vegar ekki birtast á meðal nettóþarfa vöru fyrr en fínstilling áætlanagerðar er keyrð (með áætlun sem inniheldur vöruna) eða fyrr en þú velur **Uppfæra \> Aðaláætlanagerð** á aðgerðasvæðinu á síðunni **Nettóþarfir** sem mun keyra aðaláætlanagerð fyrir vöruna. Frekari upplýsingar um hvernig á að vinna með síðu [Nettóþarfir](net-requirements.md) sjá **Nettóþarfir og upplýsingar um þarfarakningu**. |
| Úthlutanir tilfanga | Þegar unnið er með takmarkaða afkastagetu úthlutar úrelt aðaláætlanagerð öllum áætluðum pöntunum á sama tilfangið í tilteknum tilfangaflokki. Fínstilling áætlanagerðar bætir þetta með því að velja tilföng af handahófi þannig að mismunandi framleiðslufyrirmæli geti notað mismunandi tilföng. Ef nota á sömu tilföng fyrir allar áætlaðar pantanir þarf að tilgreina þau tilföng í leiðinni. |
| Auknar gagnagerðir (EDT) | Fínstilling áætlanagerðar styður ekki breytingar á nákvæmni EDT. Þetta þýðir að ferlið er ekki stutt opinberlega og ekki er tryggt að það virki. |
| Uppfylling öryggisbirgða | Fínstilling áætlanagerðar notar alltaf *Uppfylla lágmark* af **Dagurinn í dag + öflunartími**. Þetta býr kerfið undir einfaldaða uppsetningu áætlanagerðar í framtíðinni og býður upp á niðurstöður sem hægt er að bregðast við. Ef öflunartíminn er ekki hafður með í öryggisbirgðum, verða alltaf tafir á áætluðum pöntunum sem búnar eru til fyrir núverandi lágar lagerbirgðir vegna afhendingartíma. Þessi hegðun getur valdið verulegum truflunum og óæskilegum áætluðum pöntunum. Best er að breyta stillingunni til að nota *Dagurinn í dag + öflunartími*. Uppfæra aðalgögn til að forðast viðvaranir. |
| Afrita fasta áætlun yfir í breytilega áætlun | Fínstilling áætlanagerðar afritar ekki fastar áætlanir í kvikar áætlanir, alveg sama hver stillingin er á síðunni **Færibreytur aðaláætlanagerðar**. Almennt á þessi aðgerð síður við út af hraðanum og fullri endurmyndun sem fínstilling skipulagningar veitir. Ef tvær eða fleiri áætlanir eru notaðar ætti að kvikna á aðaláætlanagerð fyrir hvora áætlun. |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)
- [Færibreytur ekki notaðar af fínstillingu áætlanagerðar](not-used-parameters.md)
- [Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
