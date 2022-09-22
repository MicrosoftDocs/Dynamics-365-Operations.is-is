---
title: Munur á innbyggðu aðalskipulagi og fínstillingu skipulagningar
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
ms.openlocfilehash: dd9493e85a90c00b2dd50abb6530661c0fbb77dc
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520838"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Munur á innbyggðu aðalskipulagi og fínstillingu skipulagningar

[!include [banner](../../includes/banner.md)]

Niðurstöður fínstillingar skipulagningar gætu verið frábrugðnar niðurstöðum úr innbyggðu aðaláætlunarvélinni. Munurinn getur stafað af eiginleikum sem eru í biðstöðu. Þessi grein listar eiginleika sem skipulagsfínstilling styður ekki enn og eru ekki skráðir á **[Áætlun Optimization passa greiningu](planning-optimization-fit-analysis.md)** síðu].

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
| Þarfarakning öryggisbirgða og nettóþarfir | Þarfagerð *Öryggisbirgða* er ekki tekin með og er ekki sýnd á síðunni **Nettóþarfir**. Öryggisbirgðir endurspegla ekki eftirspurn og eru ekki með þarfadagsetningu tengda við sig. Þess í stað setja þær takmarkanir á hversu miklar birgðir þurfa að vera til staðar á hverjum tíma. Hins vegar er reitargildið **Lágmark** áfram tekið til greina þegar áætlaðar pantanir eru reiknaðar í aðaláætlanagerð. Við mælum með að þú skoðir dálkinn **Uppsafnað magn** á síðunni **Nettóþarfir** til að sjá að þetta gildi var tekið til greina. |
| Flutningsdagatöl | Gildið í dálknum **Flutningsdagatal** á síðunni **Afhendingarmátar** er hunsað. |
| Lágmarks/hámarksþekjukóði án gilda| Með innbyggðu áætlunarvélinni, þegar þú notar lágmark/hámark þekjukóða þar sem engin lágmarks- eða hámarksgildi eru stillt, meðhöndlar áætlunarvélin þekjukóðann sem kröfu og býr til eina pöntun fyrir hverja kröfu. Með áætlanagerð hagræðingu mun kerfið búa til eina pöntun á dag til að standa undir fullri upphæð fyrir þann dag.  |
| Nettóþörf og handvirkt búnar skipulagðar pantanir | Með innbyggðu áætlunarvélinni birtast handvirkt birgðapantanir fyrir vöru sjálfkrafa meðal netþörfanna fyrir þá vöru. Til dæmis, þegar innkaupapöntun er stofnuð úr sölupöntun, birtist innkaupapöntunin á **Nettókröfur** síðu án þess að þörf sé á fyrri aðgerðum. Þetta er vegna þess að innbyggða áætlunarvélin skráir birgðafærslur í`inventLogTTS` töflu og sýnir breytingar á **Nettókröfur** síðu fyrir kraftmiklar áætlanir. Hins vegar, með áætlanagerð fínstillingu, munu handvirkt búnar pantanir ekki birtast meðal netþörf vöru fyrr en áætlanagerð fínstilling er keyrð (með því að nota áætlun sem inniheldur vöruna), eða fyrr en þú velur **Uppfærsla \> Aðalskipulag** á aðgerðarrúðunni á **Nettókröfur** síðu, sem mun keyra aðalskipulag fyrir hlutinn. Fyrir frekari upplýsingar um hvernig á að vinna með **Nettókröfur** síðu, sjá [Nettókröfur og tengingarupplýsingar með áætlanagerð fínstillingu](net-requirements.md). |
| Auðlindaúthlutun | Þegar unnið er með óendanlega afkastagetu úthlutar innbyggða aðalskipulagsvélin öllum skipulögðum pöntunum á sama tilfang á tilteknum tilfangahópi. Hagræðing áætlanagerðar bætir þetta með því að velja tilföng af handahófi svo mismunandi framleiðslupantanir geti notað mismunandi tilföng. Ef þú vilt nota sama tilfang fyrir allar skipulagðar pantanir, þá verður þú að tilgreina það tilfang í leiðinni. |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)
- [Færibreytur ekki notaðar af fínstillingu áætlanagerðar](not-used-parameters.md)
- [Færibreytur dagsetningar og tíma sem fínstilling áætlanagerðar notar](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
