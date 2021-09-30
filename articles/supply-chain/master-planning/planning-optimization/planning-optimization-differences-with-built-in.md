---
title: Munur á innbyggðu aðalskipulagi og fínstillingu skipulagningar
description: Í þessu efnisatriði eru sýndir eiginleikar sem fínstilling áætlanagerðar styður ekki enn sem komið er og sem eru ekki sýndir á síðu samræmisgreiningar fyrir fínstillingu áætlanagerðar.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 63f3bc6cb7563ee6ff719272a0795efffcb40bc8
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500197"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Munur á innbyggðu aðalskipulagi og fínstillingu skipulagningar

[!include [banner](../../includes/banner.md)]

Niðurstöður fínstillingar skipulagningar gætu verið frábrugðnar niðurstöðum úr innbyggðu aðaláætlunarvélinni. Munurinn getur stafað af eiginleikum sem eru í biðstöðu. Í þessu efnisatriði eru sýndir eiginleikar sem fínstilling áætlanagerðar styður ekki enn sem komið er og sem eru ekki sýndir á síðunni **[Samræmisgreining fyrir fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)**].

| Eiginleiki | Núverandi hegðun í fínstillingu áætlanagerðar |
|---|---|
| Framleiðsluþyngdarafurðir | Litið er á afurðir með framleiðsluþyngd sem venjulegar afurðir.|
| Stækkanlegar víddir | Stækkanlegar víddir eru auðar í áætluðum pöntunum, jafnvel þegar gátreiturinn **Þekjuáætlun eftir vídd** er valinn á síðunni **Geymsluvíddarflokkar** eða **Rakningarvíddarflokkar**. |
| Keyrslur síaðrar framleiðslu | Nánari upplýsingar er að finna í [Framleiðsluáætlun - Síur](production-planning.md#filters). |
| Spáráætlun | Spáráætlun er ekki studd. Við mælum með því að aðaláætlanagerð sé notuð þar sem spárlíkani er úthlutað á aðaláætlunina. |
| Númeraraðir fyrir áætlaðar pantanir | Númeraraðir fyrir áætlaðar pantanir eru ekki studdar. Númer áætlaðra pantana eru búin til þjónustumegin. |
| Afrit áætlunar, eyða áætlun og hreinsun á útgáfu áætlunar | <p>Eftirfarandi atriði eru gerð óvirk undir **Aðaláætlanagerð \> Aðaláætlanagerð \> Vinna með áætlanir** í yfirlitssvæðinu:</p><ul><li>Afrit áætlunar</li><li>Eyða áætlun</li><li>Tiltekt áætlunarútgáfu</li></ul> |
| Skilapantanir | Skilapantanir eru ekki teknar til greina. |
| Tengdir eiginleikar tímasettir | Frekari upplýsingar er að finna í [Röðun með ótakmarkaða getu](infinite-capacity-planning.md#limitations). |
| Uppfylling öryggisbirgða | Fínstilling áætlanagerðar notar alltaf valkostinn *Dagurinn í dag + öflunartími* fyrir reitinn **Uppfylla lágmark** á síðunni **Vöruþekja**. Þetta hjálpar til við að koma í veg fyrir óæskilegar áætlaðar pantanir og önnur vandamál vegna þess að ef öflunartíminn er ekki hafður með í öryggisbirgðum, verða alltaf tafir á áætluðum pöntunum sem búnar eru til vegna afhendingartíma. |
| Þarfarakning öryggisbirgða og nettóþarfir | Þarfagerð *Öryggisbirgða* er ekki tekin með og er ekki sýnd á síðunni **Nettóþarfir**. Öryggisbirgðir endurspegla ekki eftirspurn og eru ekki með þarfadagsetningu tengda við sig. Þess í stað setja þær takmarkanir á hversu miklar birgðir þurfa að vera til staðar á hverjum tíma. Hins vegar er reitargildið **Lágmark** áfram tekið til greina þegar áætlaðar pantanir eru reiknaðar í aðaláætlanagerð. Við mælum með að þú skoðir dálkinn **Uppsafnað magn** á síðunni **Nettóþarfir** til að sjá að þetta gildi var tekið til greina. |
| Flutningsdagatöl | Gildið í dálknum **Flutningsdagatal** á síðunni **Afhendingarmátar** er hunsað. |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)
- [Færibreytur ekki notaðar af fínstillingu áætlanagerðar](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]