---
title: Greining á samsvörun áætlunarfínstillingar
description: Þetta efni útskýrir hvernig á að sannreyna núverandi uppsetningu og gögn gagnvart getu virkni fínstillingar skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0382e78942e6cb2047e37b76f1daf5725638d5c3
ms.sourcegitcommit: 915ee7c59ef5fbd4927c10840e5c5e8652f667a9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3277799"
---
# <a name="planning-optimization-fit-analysis"></a>Greining á samsvörun áætlunarfínstillingar

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Til að sjá hversu samhæf núverandi uppsetning og gögn eru við virkni fínstillingar áætlunarinnar ferðu í **Aðaláætlunargerð** \> **Uppsetning** \> **Greining á samsvörun áætlunarfínstillingar** og veldu síðan **Keyra greiningu**. Ef greiningin finnur fyrir ósamræmi eru þau skráð á sömu síðu. (Greiningin getur tekið nokkrar mínútur í keyrslu.)

> [!NOTE]
> Ef ósamræmi finnst, getur þú samt notað fínstillingu skipulagsins. Niðurstöður samsvörunargreiningar sýna bara staði þar sem skipulagsþjónustan mun ekki heiðra núverandi uppsetningu. Með öðrum orðum sýna þær staði þar sem einhver ferli kunna að vera hunsuð eða ekki studd.

## <a name="analysis-results-example-1"></a>Niðurstöður greiningar: Dæmi 1

- **Eiginleiki:** Framleiðsla
- **Mál:** Vörur með uppskriftarstig hærra en núll: 56
- **Útskýring:** Samræmisgreiningin fann 56 vörur sem eru með uppskriftaruppsetningu fyrir framleiðslu. Vegna þess að núverandi útgáfa af fínstillingu áætlunargerðar styður ekki framleiðslu mun fínstilling áætlunarinnar búa til innkaupatillögur í stað framleiðslutillaga. Hún mun einnig sýna viðvörun sem sýnir vörurnar sem varða fyrir áhrifum.

## <a name="analysis-results-example-2"></a>Niðurstöður greiningar: Dæmi 2

- **Eiginleiki:** Aðgerðir
- **Mál:** Þekjuhópar með útreikninga á aðgerðum virkjaða: 6
- **Útskýring:** Samsvörunargreiningin fann sex þekjuhópa þar sem kveikt er á útreikningi á aðgerðum. Þar sem núverandi útgáfa af fínstillingu áætlunarinnar styður ekki aðgerðir verða engar aðgerðir myndaðar við aðalskipulagningu.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Yfirlit yfir mögulegar niðurstöður samræmisgreiningar

Eftirfarandi tafla sýnir hinar ýmsu niðurstöður sem hægt er að sýna eftir samræmisgreiningu. Númeramerkjum (_\#_) verður skipt út fyrir númer sem tilgreinir fjölda færslna sem eru með uppgefið vandamál.

| Eiginleiki | Uppgefið vandamál | Skýring |
| --- | --- | --- |
| Aðgerðir | Þekjuflokkar með virkan útreikning á aðgerðum: _\#_ | Þessi eiginleiki í bið. Sem stendur eru aðgerðir ekki búnar til við aðaláætlanagerð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. Megintilgangur aðgerða er að stinga upp á breytingum á fyrirliggjandi pöntunum. |
| Grunndagatöl | Dagatöl sem nota grunndagatal: _\#_ | Þessi eiginleiki í bið. Sem stendur er grunndagatalið hunsað þegar fínstilling áætlanagerðar er virk. |
| Ráðstöfunarkóðar runu | Aðalrunuráðstafanir sem eru ekki nettó: _\#_ | Þessi eiginleiki í bið. Sem stendur er litið framhjá ráðstöfunarkóðum þegar fínstilling áætlanagerðar er virk. |
| Hægt að lofa (CTP) | Sjálfgefnar pöntunarstillingar með afhendingardagsstjórnun stillta á CTP: _\#_ | Þessi eiginleiki í bið. Sem stendur er litið framhjá CTP þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Afrita fasta áætlun yfir í breytilega áætlun | Afritun á fastri áætlun yfir í breytilega áætlun er gerð virk á færibreytum aðaláætlanagerðarinnar. | Fínstilling áætlanagerðar afritar ekki fasta áætlun í breytilega áætlun, óháð þessari stillingu. Almennt á þessi hugmynd síður við út af hraðanum og fullri endurmyndun sem fínstilling áætlanagerðar veitir. Ef tvær eða fleiri áætlanir eru notaðar ætti að kvikna á aðaláætlanagerð fyrir hvora áætlun. |
| Staðfesting | Þekjuhópar með stillt tímamörk staðfestinga: _\#_ | Í útgáfu 10.0.7 og nýrri er staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn _Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar_ hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. |
| Staðfesting | Vöruþekjufærslur með sjálfvirka staðfestingu stillta: _\#_ | Í útgáfu 10.0.7 og nýrri er sjálfvirk staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn _Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar_ hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. |
| Staðfesting | Aðaláætlanir með sjálfvirka staðfestingu stillta: _\#_ | Í útgáfu 10.0.7 og nýrri er sjálfvirk staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn _Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar_ hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. |
| FitAnalysisPlanningItems | Vörur í áætlun: _\#_ | Þessi eiginleiki í bið. Sem stendur eru vörur í áætlun meðhöndlaðar eins og venjulegar vörur þegar fínstilling áætlanagerðar er virk. |
| Spá | Þekjuflokkar með „Hafa með pantanir innan samstæðu“: _\#_ | Þessi eiginleiki í bið. Eins og er inniheldur aðaláætlanagerð ekki áætlaða seinni tíma eftirspurn þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. Athugið að útgefnar/staðfestar pantanir virka enn með venjulegu samstæðuaðgerðinni og nær utan um flestar atburðarásir. |
| Spá | Þekjuflokkar með „Draga úr spá um“ stillinguna stillta á annað gildi en „Pantanir“: _\#_ | Sjálfgefið er að fínstilling áætlanagerðar noti „Draga úr spá um“ fyrir pantanir, óháð þessari stillingu. |
| Spá | Spárlíkön með undirspárlíkönum: _\#_ | Þessi eiginleiki í bið. Sem stendur eru spár sem nota undirlíkön ekki studdar þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. |
| Spá | Aðaláætlanir með „Hafa með birgðaspá“ virkt: _\#_ | Þessi eiginleiki í bið. Sem stendur eru birgðaspár ekki studdar þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. |
| Tímamörk frystingar | Þekjuhópar með stillt á fryst tímamörk staðfestinga: _\#_ | Tímamörk frystingar eru ekki oft notaðar og sem stendur er ekki áformað að hafa þær með í fínstilling áætlanagerðar. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Tímamörk frystingar | Vöruþekjufærslur með stillt á fryst tímamörk staðfestinga: _\#_ | Tímamörk frystingar eru ekki oft notaðar og sem stendur er ekki áformað að hafa þær með í fínstilling áætlanagerðar. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Tímamörk frystingar | Aðaláætlanir með stillt á fryst tímamörk staðfestinga: _\#_ | Tímamörk frystingar eru ekki oft notaðar og sem stendur er ekki áformað að hafa þær með í fínstilling áætlanagerðar. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Innan samstæðu | Aðaláætlanir þ.m.t. áætluð eftirspurn forstreymis: _\#_ | Þessi eiginleiki í bið. Eins og er inniheldur aðaláætlanagerð ekki áætlaða seinni tíma eftirspurn þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. Athugið að útgefnar/staðfestar pantanir virka enn með hefðbundnu samstæðuaðgerðinni og nær utan um flestar atburðarásir. |
| Kanban | Vöruþekjufærslur með áætlaða kanban-pöntunargerð: _\#_ | Þessi eiginleiki í bið. Sem stendur verður vöruþekja sem stillt er á kanban hunsuð þegar fínstilling áætlanagerðar er virk. Áætluð kanban-pöntunargerð býr til viðvörun við aðaláætlanagerð og áætlaðar innkaupapantanir verða búnar til til að ná yfir viðeigandi eftirspurn. |
| Kanban | Vörur með sjálfgefna kanban-pöntunargerð: _\#_ | Sem stendur verður sjálfgefin pöntunargerð sem stillt er á kanban hunsuð þegar fínstilling áætlanagerðar er virk. Áætluð kanban-pöntunargerð býr til viðvörun við aðaláætlanagerð og áætlaðar innkaupapantanir verða búnar til til að ná yfir viðeigandi eftirspurn. |
| Vinnsla | Uppskriftarlínur með sléttun eða margfeldi í uppsetningu: _\#_ | Þessi eiginleiki í bið. Sem stendur verða uppsetningar með sléttun og margfeldi hunsaðar í uppskriftarlínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Vinnsla | Uppskriftar-/formúlulínur með formúlumælingu: _\#_ | Þessi eiginleiki í bið. Sem stendur er formúlumæling hunsuð í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Vinnsla | Uppskriftar-/formúlulínur með staðgengilsvöru (áætlunarflokka): _\#_ | Þessi eiginleiki í bið. Sem stendur er staðgengilsvara (áætlunarflokkar) hunsaður í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Vinnsla | Uppskriftar-/formúlulínur með neikvæðu magni: _\#_ | Þessi eiginleiki í bið. Uppskriftar- og formúlulínur sem eru með neikvæðu magni fá magnið 0 (núll) og viðvörun verður gefin út þegar fínstilling áætlanagerðar er virkjuð. |
| Vinnsla | Uppskriftar-/formúlulínur með tilfanganotkun: _\#_ | Þessi eiginleiki í bið. Sem stendur eru uppskriftar- og formúlulínur sem eru með tilfanganotkun hunsaðar þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Uppskrifta-/formúlulínur með skrefanotkun: _\#_ | Þessi eiginleiki í bið. Sem stendur er skrefanotkun hunsuð í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Uppskriftir með fastri rýrnun eða breytilegri rýrnun skilgreindar: _\#_ | Þessi eiginleiki í bið. Sem stendur er föst rýrnun og breytileg rýrnun, sem skilgreindar eru í uppskriftum, hunsaðar þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Uppskriftir með úthýsingu: _\#_ | Þessi eiginleiki í bið. Sem stendur er uppsetning úthýsingar í uppskriftum hunsuð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Vinnsla | Uppskriftir án svæðis: _\#_ | Þessi eiginleiki í bið. Sem stendur eru uppskriftir án svæðis hunsaðar þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Senda beiðni með skilgreindum kröfum fyrir tiltekna uppskrift eða leið: _\#_ | Þessi eiginleiki í bið. Sem stendur eru tilteknar kröfur uppskriftar eða leiðar, sem skilgreindar eru í eftirspurninni (t.d. undiruppskrift eða undirleið í sölupöntun), hunsaðar þegar fínstilling áætlanagerðar er virk. Stöðluð uppskrift eða leið verður notuð, óháð þessari stillingu. |
| Vinnsla | Formúluútgáfur með auka-/hliðarafurðir: _\#_ | Þessi eiginleiki í bið. Sem stendur eru aukaafurðir og hliðarafurðir, sem tengjast formúluútgáfunni, hunsaðar þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Formúluútgáfur með arði: _\#_ | Þessi eiginleiki í bið. Sem stendur er arðurinn sem tengist formúluútgáfunni hunsaður þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Áætlanir sem fela í sér röðun: _\#_ | Þessi eiginleiki í bið. Sem stendur er röðun hunsuð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |
| Vinnsla | Útgefnar framleiðslupantanir sem ekki er byrjað á, þar sem áætluð byrjun er á undan deginum í dag: _\#_ | Þessi eiginleiki í bið. |
| Vinnsla | Tímasett tilföng með takmarkaða getu: _\#_ | Þessi eiginleiki í bið. Sem stendur eru tilföng sem áætluð eru með takmarkaðri getu hunsuð þegar fínstilling áætlanagerðar er virk. Áætlanagerð byggist á sjálfgefnum afhendingartíma afurðarinnar. |
| Vinnsla | Leiðir notaðar við áætlanagerð: _\#_ | Þessi eiginleiki í bið. Sem stendur eru leiðir hunsaðar þegar fínstilling áætlanagerðar er virk. Sjálfgefinn afhendingartími afurðarinnar er notaður. |
| Vinnsla | Frátekningaraðferð sölulínu með frátekningu: _\#_ | Frátekning sölulínu sem notar útþenslu er ekki studd þegar fínstilling áætlanagerðar er virk. |
| Vinnsla | Áætlanagerð með frátekningu framleiðslupantana: _\#_ | Áætlanagerð sem notar útþenslu framleiðslupantana er ekki studd þegar fínstilling áætlanagerðar er virk. Hægt er að áætla hverja framleiðslupöntun fyrir sig. |
| Beiðnir um tilboð | Aðaláætlanir með beiðnir um tilboð virkar: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki litið á tilboðsbeiðnir sem eftirspurn þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. |
| Innkaupabeiðnir | Aðaláætlanir með virkar innkaupabeiðnir: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki tekið tillit til beiðna þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. |
| Öryggismörk | Þekjuflokkar með öryggismörk: _\#_ | Þessi eiginleiki í bið. Sem stendur eru öryggismörk hunsuð þegar fínstilling áætlanagerðar er virk. Til að bæta upp fyrir þessa hegðun geturðu aukið afhendingartímann þannig að hann feli í sér öryggismörkin. |
| Öryggismörk | Aðaláætlanir með öryggismörk: _\#_ | Þessi eiginleiki í bið. Sem stendur eru öryggismörk hunsuð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. Til að bæta upp fyrir þessa hegðun geturðu aukið afhendingartímann þannig að hann feli í sér öryggismörkin. |
| Uppfylling öryggisbirgða | Vöruþekjufærslur með „Uppfylla lágmark“ annað en „Dagurinn í dag + öflunartími“: _\#_ | Fínstilling áætlanagerðar notar alltaf *Dagurinn í dag + öflunartími*. Þessi breyting er gerð til að undirbúa einfalda uppsetningu áætlanagerðar í framtíðinni og til að veita niðurstöður sem hægt er að nýta sér. Ef öflunartíminn er ekki hafður með í öryggisbirgðum, verða alltaf tafir á áætluðum pöntunum sem búnar eru til fyrir núverandi lágar lagerbirgðir vegna afhendingartíma. Þessi hegðun getur valdið verulegum truflunum og óæskilegum áætluðum pöntunum. Besta er að breyta stillingunni þannig að *Dagurinn í dag + öflunartími* er notaður. |
| Sölutilboð | Aðaláætlanir með virk sölutilboð: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki tekið tillit til tilboða þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. |
| Endingartími | Aðaláætlanir með virkan endingartíma: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki tekið tillit til endingartíma þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. |

## <a name="related-resources"></a>Tengd tilföng

[Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)

[Hafist handa með fínstillingu áætlanagerðar](get-started.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)
