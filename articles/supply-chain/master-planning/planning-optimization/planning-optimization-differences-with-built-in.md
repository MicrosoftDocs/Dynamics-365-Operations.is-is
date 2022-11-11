---
title: Munur á hagræðingu áætlanagerðar og úreltu aðalskipulagsvélarinnar
description: Þessi grein listar upp eiginleika sem áætlanagerð fínstilling styður ekki enn og eru ekki skráðir á síðuna áætlanagerð fínstillingu passa greiningu.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745362"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Munur á hagræðingu áætlanagerðar og úreltu aðalskipulagsvélarinnar

[!include [banner](../../includes/banner.md)]

Niðurstöður hagræðingar áætlanagerðar gætu verið frábrugðnar niðurstöðum úr úreltu aðalskipulagsvélinni. Munurinn getur stafað af eiginleikum sem eru í biðstöðu. Þessi grein listar eiginleika sem skipulagsfínstilling styður ekki enn og eru ekki skráðir á **[Áætlun Optimization passa greiningu](planning-optimization-fit-analysis.md)** síðu].

| Eiginleiki | Núverandi hegðun í fínstillingu áætlanagerðar |
|---|---|
| Framleiðsluþyngdarafurðir | Litið er á afurðir með framleiðsluþyngd sem venjulegar afurðir.|
| Stækkanlegar víddir | Stækkanlegar víddir eru ekki studdar af áætlanagerð fínstillingu. Þegar þú notar áætlanagerð fínstillingu, eru stækkanlegar víddir tómar á fyrirhuguðum pöntunum, jafnvel þegar **Þekjuáætlun eftir vídd** gátreiturinn er valinn á **Geymsluvíddarhópar** eða **Rekja víddarhópa** síðu. |
| Keyrslur síaðrar framleiðslu | Nánari upplýsingar er að finna í [Framleiðsluáætlun - Síur](production-planning.md#filters). |
| Spáráætlun | Spáráætlun er ekki studd. Við mælum með því að aðaláætlanagerð sé notuð þar sem spárlíkani er úthlutað á aðaláætlunina. |
| Númeraraðir fyrir áætlaðar pantanir | Númeraraðir fyrir áætlaðar pantanir eru ekki studdar. Númer áætlaðra pantana eru búin til þjónustumegin. Áætlað pöntunarnúmer er yfirleitt sýnt með 10 stöfum, en röðin er í raun byggð á 20 stöfum, með 10 stöfum úthlutuðum fyrir áætlunarkeyrslutalningu og 10 stöfum fyrir talningu á áætluðum pöntunum. |
| Afrit áætlunar, eyða áætlun og hreinsun á útgáfu áætlunar | <p>Eftirfarandi atriði eru gerð óvirk undir **Aðaláætlanagerð \> Aðaláætlanagerð \> Vinna með áætlanir** í yfirlitssvæðinu:</p><ul><li>Afrit áætlunar</li><li>Eyða áætlun</li><li>Tiltekt áætlunarútgáfu</li></ul> |
| Skilapantanir | Skilapantanir eru ekki teknar til greina. |
| Tengdir eiginleikar tímasettir | Frekari upplýsingar er að finna í [Röðun með ótakmarkaða getu](infinite-capacity-planning.md#limitations). |
| Uppfylling öryggisbirgða | Fínstilling áætlanagerðar notar alltaf valkostinn *Dagurinn í dag + öflunartími* fyrir reitinn **Uppfylla lágmark** á síðunni **Vöruþekja**. Þetta hjálpar til við að koma í veg fyrir óæskilegar áætlaðar pantanir og önnur vandamál vegna þess að ef öflunartíminn er ekki hafður með í öryggisbirgðum, verða alltaf tafir á áætluðum pöntunum sem búnar eru til vegna afhendingartíma. |
| Þarfarakning öryggisbirgða og nettóþarfir | Þarfagerð *Öryggisbirgða* er ekki tekin með og er ekki sýnd á síðunni **Nettóþarfir**. Öryggisbirgðir endurspegla ekki eftirspurn og eru ekki með þarfadagsetningu tengda við sig. Þess í stað setja þær takmarkanir á hversu miklar birgðir þurfa að vera til staðar á hverjum tíma. Hins vegar er reitargildið **Lágmark** áfram tekið til greina þegar áætlaðar pantanir eru reiknaðar í aðaláætlanagerð. Við mælum með að þú skoðir dálkinn **Uppsafnað magn** á síðunni **Nettóþarfir** til að sjá að þetta gildi var tekið til greina. Vegna þess að tengingin er öðruvísi, gæti verið stungið upp á mismunandi aðgerðum. |
| Flutningsdagatöl | Gildið í dálknum **Flutningsdagatal** á síðunni **Afhendingarmátar** er hunsað. |
| Lágmarks/hámarksþekjukóði án gilda| Með úreltu aðalskipulagsvélinni, þegar þú notar lágmark/hámark þekjukóða þar sem engin lágmarks- eða hámarksgildi eru stillt, meðhöndlar áætlunarvélin þekjukóðann sem kröfu og býr til eina pöntun fyrir hverja kröfu. Með áætlanagerð hagræðingu mun kerfið búa til eina pöntun á dag til að standa undir fullri upphæð fyrir þann dag.  |
| Nettóþörf og handvirkt búnar skipulagðar pantanir | Með úreltu aðalskipulagsvélinni birtast handvirkt birgðapantanir fyrir vöru sjálfkrafa meðal nettóþörfanna fyrir þá vöru. Til dæmis, þegar innkaupapöntun er stofnuð úr sölupöntun, birtist innkaupapöntunin á **Nettókröfur** síðu án þess að þörf sé á fyrri aðgerðum. Þetta er vegna þess að úrelt aðalskipulagsvél skráir birgðafærslur í`inventLogTTS` töflu og sýnir breytingar á **Nettókröfur** síðu fyrir kraftmiklar áætlanir. Hins vegar, með áætlanagerð fínstillingu, munu handvirkt búnar pantanir ekki birtast meðal netþörf vöru fyrr en áætlanagerð fínstilling er keyrð (með því að nota áætlun sem inniheldur vöruna), eða fyrr en þú velur **Uppfærsla \> Aðalskipulag** á aðgerðarrúðunni á **Nettókröfur** síðu, sem mun keyra aðalskipulag fyrir hlutinn. Fyrir frekari upplýsingar um hvernig á að vinna með **Nettókröfur** síðu, sjá [Nettókröfur og tengingarupplýsingar](net-requirements.md). |
| Auðlindaúthlutun | Þegar unnið er með óendanlega afkastagetu, úthlutar úrelta aðalskipulagsvélin öllum skipulögðum pöntunum á sama tilfang á tilteknum tilfangahópi. Hagræðing áætlanagerðar bætir þetta með því að velja tilföng af handahófi svo mismunandi framleiðslupantanir geti notað mismunandi tilföng. Ef þú vilt nota sama tilfang fyrir allar skipulagðar pantanir, þá verður þú að tilgreina það tilfang í leiðinni. |
| Ítarlegar gagnagerðir (EDTs) | Áætlanagerð fínstilling styður ekki breytingar á nákvæmni EDTs. Þetta þýðir að þetta ferli er ekki opinberlega stutt og það er ekki tryggt að það virki. |
| Uppfylling öryggisbirgða | Áætlanagerð hagræðing notar alltaf a **Uppfylltu lágmark** af *Dagsetning í dag + innkaupatími*. Þetta undirbýr kerfið til að nota einfaldaða skipulagsuppsetningu í framtíðinni og gefur raunhæfa niðurstöðu. Ef innkaupatíminn er ekki innifalinn fyrir öryggisbirgðir, verða áætlaðar pantanir sem eru búnar til fyrir litlar birgðir alltaf seinkaðar vegna afgreiðslutíma. Þessi hegðun getur valdið verulegum truflunum og óæskilegum áætluðum pöntunum. Besta aðferðin er að breyta stillingunni til að nota *Dagsetning dagsins + innkaupatími*. Uppfæra aðalgögn til að forðast viðvaranir. |
| Afrita fasta áætlun yfir í breytilega áætlun | Hagræðing áætlanagerðar afritar ekki kyrrstæðar áætlanir yfir í kraftmiklar áætlanir, óháð stillingu á **Aðalskipulagsbreytur** síðu. Almennt séð skiptir þessi aðgerð minna máli vegna hraðans og fullkominnar endurnýjunar sem áætlanagerð fínstilling veitir. Ef tvær eða fleiri áætlanir eru notaðar ætti að kvikna á aðaláætlanagerð fyrir hvora áætlun. |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)
- [Færibreytur ekki notaðar af fínstillingu áætlanagerðar](not-used-parameters.md)
- [Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
