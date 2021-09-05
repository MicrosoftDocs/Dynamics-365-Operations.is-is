---
title: Greining á samsvörun áætlunarfínstillingar
description: Þetta efni útskýrir hvernig á að sannreyna núverandi uppsetningu og gögn gagnvart getu virkni fínstillingar skipulagningar.
author: ChristianRytt
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd0fdd677824db823f9bc42f0ad1bdd90cf3b16d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344979"
---
# <a name="planning-optimization-fit-analysis"></a>Samræmisgreining á fínstillingu áætlanagerðar

[!include [banner](../../includes/banner.md)]

Þú ættir að greina útkomuna úr samræmisgreiningu á fínstillingu skipulagningar sem hluti af flutningsferlinu. Athugið að umfang fínstillingar skipulagningar jafnast ekki á við núverandi virkni innbyggðrar aðaláætlanagerðar. Við mælum með því að þú vinnir með samstarfsaðilanum og lesir fylgiskjölin til að undirbúa flutninginn. 

Samræmisgreining á fínstillingu skipulagningar hjálpar þér að finna út hvar útkoman kann að vera mismunandi milli innbyggðrar vélar aðaláætlanagerðar og fínstillingar skipulagningar. Þessi greining er unnin út frá núverandi uppsetningu og gögnum. 

Til að sjá útkomu samræmisgreiningar á fínstillingu skipulagningar skal farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Samræmisgreining á fínstillingu skipulagningar** og síðan velja **Keyra greiningu**. Ef greiningin finnur fyrir ósamræmi eru þau skráð á sömu síðu. (Greiningin getur tekið nokkrar mínútur í keyrslu.)

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

Eftirfarandi tafla sýnir hinar ýmsu niðurstöður sem hægt er að sýna eftir samræmisgreiningu. Númeramerkjum (_\#_) verður skipt út fyrir númer sem tilgreinir fjölda færslna sem eru með uppgefið vandamál. Eiginleikar sem eru studdir eða í forútgáfu eru tiltækir með útgáfu 10.0.9 eða nýrri (nema hærra útgáfunúmer sé skráð í dálkinn „Væntanlegt framboð“).

> [!NOTE]
> Ekki er hægt að bera kennsl á ósamræmi í samræmisgreiningu fínstillingar áætlanagerðar. Frekari upplýsingar er að finna í [Munur á milli hefðbundinnar aðaláætlanagerðar og fínstillingar áætlanagerðar](planning-optimization-differences-with-built-in.md).

| Eiginleiki | Uppgefið vandamál | Skýring | Væntanlegt framboð |
| --- | --- | --- | --- |
| Aðgerðir | Þekjuflokkar með virkan útreikning á aðgerðum: _\#_ | Þessi eiginleiki í bið. Sem stendur eru aðgerðir ekki búnar til við aðaláætlanagerð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. Megintilgangur aðgerða er að stinga upp á breytingum á fyrirliggjandi pöntunum. Meta hvort aðgerðir eru nýttar sem hluti af viðskiptaferlum eða ef upplýsingar um seinkun sem tengjast pöntunum eru fullnægjandi. | 2022. apríl |
| Grunndagatöl | Dagatöl sem nota grunndagatal: _\#_ | Þessi eiginleiki í bið. Sem stendur er grunndagatalið hunsað þegar fínstilling áætlanagerðar er virk. Meta hvort þörf sé á grunndagatali fyrir viðskiptaferla eða ef bein uppsetning í dagatölum er nægjanleg. | 2022. apríl | 
| Ráðstöfunarkóðar runu | Aðalrunuráðstafanir sem eru ekki nettó: _\#_ | Þessi eiginleiki í bið. Sem stendur er litið framhjá ráðstöfunarkóðum þegar fínstilling áætlanagerðar er virk. | Server 2022 eða nýrri |
| Hægt að lofa (CTP) | Sjálfgefnar pöntunarstillingar með afhendingardagsstjórnun stillta á CTP: _\#_ | Þessi eiginleiki í bið. Sem stendur er litið framhjá CTP þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022. október |
| Afrita fasta áætlun yfir í breytilega áætlun | Afritun á fastri áætlun yfir í breytilega áætlun er gerð virk á færibreytum aðaláætlanagerðarinnar. | Fínstilling áætlanagerðar afritar ekki fasta áætlun í breytilega áætlun, óháð þessari stillingu. Almennt á þessi hugmynd síður við út af hraðanum og fullri endurmyndun sem fínstilling áætlanagerðar veitir. Ef tvær eða fleiri áætlanir eru notaðar ætti að kvikna á aðaláætlanagerð fyrir hvora áætlun. | 2022. október |
| Staðfesting | Þekjuhópar með stillt tímamörk staðfestinga: _\#_ | Í útgáfu 10.0.7 og nýrri er staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn _Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar_ hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. | Stutt |
| Staðfesting | Vöruþekjufærslur með sjálfvirka staðfestingu stillta: _\#_ | Í útgáfu 10.0.7 og nýrri er sjálfvirk staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn _Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar_ hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. | Stutt |
| Staðfesting | Aðaláætlanir með sjálfvirka staðfestingu stillta: _\#_ | Í útgáfu 10.0.7 og nýrri er sjálfvirk staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn _Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar_ hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. | Stutt |
| FitAnalysisPlanningItems | Vörur í áætlun: _\#_ | Þessi eiginleiki í bið. Sem stendur eru vörur í áætlun meðhöndlaðar eins og venjulegar vörur þegar fínstilling áætlanagerðar er virk. | Server 2022 eða nýrri |
| Spá | Þekjuflokkar með „Hafa með pantanir innan samstæðu“: _\#_ | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Áætlanagerð innan samstæðu](Intercompany-planning.md) | Stutt |
| Spá | Þekjuflokkar með „Draga úr spá um“ stillinguna stillta á annað gildi en „Pantanir“: _\#_ | Þessi eiginleiki er nú studdur. Frekari upplýsingar eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md) | Stutt |
| Spá | Spárlíkön með undirspárlíkönum: _\#_ |  Þessi eiginleiki er nú studdur. Frekari upplýsingar eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md) | Stutt |
| Spá | Aðaláætlanir með „Hafa með birgðaspá“ virkt: _\#_ | Þessi eiginleiki í bið. Sem stendur eru birgðaspár ekki studdar þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. | Server 2022 eða nýrri |
| Tímamörk frystingar | Þekjuhópar með stillt á fryst tímamörk staðfestinga: _\#_ | Tímamörk frystingar eru ekki oft notaðar og sem stendur er ekki áformað að hafa þær með í fínstilling áætlanagerðar. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | Á ekki við |
| Tímamörk frystingar | Vöruþekjufærslur með stillt á fryst tímamörk staðfestinga: _\#_ | Tímamörk frystingar eru ekki oft notaðar og sem stendur er ekki áformað að hafa þær með í fínstilling áætlanagerðar. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | Á ekki við |
| Tímamörk frystingar | Aðaláætlanir með stillt á fryst tímamörk staðfestinga: _\#_ | Tímamörk frystingar eru ekki oft notaðar og sem stendur er ekki áformað að hafa þær með í fínstilling áætlanagerðar. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | Á ekki við |
| Innan samstæðu | Aðaláætlanir þ.m.t. áætluð eftirspurn forstreymis: _\#_ | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Áætlanagerð innan samstæðu](Intercompany-planning.md) | Stutt |
| Kanban | Vöruþekjufærslur með áætlaða kanban-pöntunargerð: _\#_ | Þessi eiginleiki í bið. Sem stendur verður vöruþekja sem stillt er á kanban hunsuð þegar fínstilling áætlanagerðar er virk. Áætluð kanban-pöntunargerð býr til viðvörun við aðaláætlanagerð og áætlaðar innkaupapantanir verða búnar til til að ná yfir viðeigandi eftirspurn. | Server 2022 eða nýrri |
| Kanban | Vörur með sjálfgefna kanban-pöntunargerð: _\#_ | Sem stendur verður sjálfgefin pöntunargerð sem stillt er á kanban hunsuð þegar fínstilling áætlanagerðar er virk. Áætluð kanban-pöntunargerð býr til viðvörun við aðaláætlanagerð og áætlaðar innkaupapantanir verða búnar til til að ná yfir viðeigandi eftirspurn. | Server 2022 eða nýrri |
| Lífferilsstaða afurðar | Lífferilsstaða afurðar ekki virk fyrir áætlanagerð: _\#_ | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Útiloka afurðir sem hafa tilteknar líftímastöður afurðar](product-lifecycle-state.md) | Stutt |
| Framleiðsla | Uppskriftarlínur með sléttun eða margfeldi í uppsetningu: _\#_ | Þessi eiginleiki í bið. Sem stendur verða uppsetningar með sléttun og margfeldi hunsaðar í uppskriftarlínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2021. október |
| Framleiðsla | Uppskriftar-/formúlulínur með formúlumælingu: _\#_ | Þessi eiginleiki í bið. Sem stendur er formúlumæling hunsuð í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022. október |
| Framleiðsla | Uppskriftar-/formúlulínur með staðgengilsvöru (áætlunarflokka): _\#_ | Þessi eiginleiki í bið. Sem stendur er staðgengilsvara (áætlunarflokkar) hunsaður í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022. október |
| Framleiðsla | Uppskriftar-/formúlulínur með neikvæðu magni: _\#_ | Þessi eiginleiki í bið. Uppskriftar- og formúlulínur sem eru með neikvæðu magni fá magnið 0 (núll) og viðvörun verður gefin út þegar fínstilling áætlanagerðar er virkjuð. Uppfæra aðalgögn til að forðast viðvaranir. | 2022. október |
| Framleiðsla | Uppskriftar-/formúlulínur með tilfanganotkun: _\#_ | Þessi eiginleiki í bið. Sem stendur eru uppskriftar- og formúlulínur sem eru með tilfanganotkun hunsaðar þegar fínstilling áætlanagerðar er virk. Þegar þessi eiginleiki er studdur verður efnisþörfinni stillt á upphafsdagsetningu framleiðslunnar. Þar til þessi eiginleiki er studdur verða kröfur ekki myndaðar fyrir efni sem eru merkt með flaggi tilfanganotkunar. | 2022. október |
| Framleiðsla | Uppskrifta-/formúlulínur með skrefanotkun: _\#_ | Þessi eiginleiki í bið. Sem stendur er skrefanotkun hunsuð í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk. | 2022. október |
| Framleiðsla | Uppskriftir með fastri rýrnun eða breytilegri rýrnun skilgreindar: _\#_ | Þessi eiginleiki í bið. Sem stendur er föst rýrnun og breytileg rýrnun, sem skilgreindar eru í uppskriftum, hunsaðar þegar fínstilling áætlanagerðar er virk. | 2022. október |
| Framleiðsla | Uppskriftir með úthýsingu: _\#_ | Þessi eiginleiki í bið. Sem stendur er uppsetning úthýsingar í uppskriftum hunsuð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022. apríl |
| Framleiðsla | Uppskriftir án svæðis: _\#_ | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Framleiðsluáætlun](production-planning.md) | Stutt |
| Framleiðsla | Senda beiðni með skilgreindum kröfum fyrir tiltekna uppskrift eða leið: _\#_ | Þessi eiginleiki í bið. Sem stendur eru tilteknar kröfur uppskriftar eða leiðar, sem skilgreindar eru í eftirspurninni (t.d. undiruppskrift eða undirleið í sölupöntun), hunsaðar þegar fínstilling áætlanagerðar er virk. Stöðluð uppskrift eða leið verður notuð, óháð þessari stillingu. | 2022. október |
| Framleiðsla | Formúluútgáfur með auka-/hliðarafurðir: _\#_ | Þessi eiginleiki í bið. Sem stendur eru aukaafurðir og hliðarafurðir, sem tengjast formúluútgáfunni, hunsaðar þegar fínstilling áætlanagerðar er virk. | 2022. október |
| Framleiðsla | Formúluútgáfur með arði: _\#_ | Þessi eiginleiki í bið. Sem stendur er arðurinn sem tengist formúluútgáfunni hunsaður þegar fínstilling áætlanagerðar er virk. | 2022. október |
| Framleiðsla | Áætlanir sem fela í sér röðun: _\#_ | Þessi eiginleiki í bið. Sem stendur er röðun hunsuð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022. október |
| Framleiðsla | Útgefnar framleiðslupantanir sem ekki er byrjað á, þar sem áætluð byrjun er á undan deginum í dag: _\#_ | Þessi eiginleiki í bið. Eins og er, ef framleiðslupöntun seinkar, mun aðaláætlanagerð gera ráð fyrir því að henni verði lokið í dag. Þetta á við um útgefnar framleiðslupantanir þar sem afhendingardagsetning er í fortíðinni, en hefur ekki verið lokið. | 2022. október |
| Framleiðsla | Tímasett tilföng með takmarkaða getu: _\#_ | Þessi eiginleiki í bið. Sem stendur eru tilföng sem áætluð eru með takmarkaðri getu hunsuð þegar fínstilling áætlanagerðar er virk. Áætlanagerð byggist á sjálfgefnum afhendingartíma afurðarinnar. | 2022. október |
| Framleiðsla | Leiðir notaðar við áætlanagerð: _\#_ | Þessi eiginleiki í bið. Sem stendur eru leiðir hunsaðar þegar fínstilling áætlanagerðar er virk. Sjálfgefinn afhendingartími afurðarinnar er notaður. | Forskoðun: Studd (10.0.20), GA: Október 2021 |
| Framleiðsla | Frátekningaraðferð sölulínu með frátekningu: _\#_ | Frátekning sölulínu sem notar útþenslu er ekki studd þegar fínstilling áætlanagerðar er virk. | 2022. október |
| Framleiðsla | Áætlanagerð með frátekningu framleiðslupantana: _\#_ | Áætlanagerð sem notar útþenslu framleiðslupantana er ekki studd þegar fínstilling áætlanagerðar er virk. Hægt er að áætla hverja framleiðslupöntun fyrir sig. | 2022. október |
| Beiðnir um tilboð | Aðaláætlanir með beiðnir um tilboð virkar: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki litið á tilboðsbeiðnir sem eftirspurn þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. | 2022. október |
| Innkaupabeiðnir | Aðaláætlanir með virkar innkaupabeiðnir: _\#_ | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Innkaupabeiðnir](purchase-requisitions.md) | Stutt |
| Öryggismörk | Þekjuflokkar með öryggismörk: _\#_ | Þessi eiginleiki er nú studdur að hluta. Frekari upplýsingar má finna í [Öryggismörk](safety-margins.md) | Mörk innhreyfinga: Studd. Endurpöntunarmörk og úthreyfingamörk: janúar 2022 |
| Öryggismörk | Aðaláætlanir með öryggismörk: _\#_ | Þessi eiginleiki er nú studdur að hluta. Frekari upplýsingar má finna í [Öryggismörk](safety-margins.md) | Mörk innhreyfinga: Studd. Endurpöntunarmörk og úthreyfingamörk: janúar 2022 |
| Uppfylling öryggisbirgða | Vöruþekjufærslur með „Uppfylla lágmark“ annað en „Dagurinn í dag + öflunartími“: _\#_ | Fínstilling áætlanagerðar notar alltaf *Dagurinn í dag + öflunartími*. Þessi breyting er gerð til að undirbúa einfalda uppsetningu áætlanagerðar í framtíðinni og til að veita niðurstöður sem hægt er að nýta sér. Ef öflunartíminn er ekki hafður með í öryggisbirgðum, verða alltaf tafir á áætluðum pöntunum sem búnar eru til fyrir núverandi lágar lagerbirgðir vegna afhendingartíma. Þessi hegðun getur valdið verulegum truflunum og óæskilegum áætluðum pöntunum. Besta er að breyta stillingunni þannig að *Dagurinn í dag + öflunartími* er notaður. Uppfæra aðalgögn til að forðast viðvaranir. | Á ekki við |
| Sölutilboð | Aðaláætlanir með virk sölutilboð: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki tekið tillit til tilboða þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. | Server 2022 eða nýrri |
| Endingartími | Aðaláætlanir með virkan endingartíma: _\#_ | Þessi eiginleiki í bið. Sem stendur er ekki tekið tillit til endingartíma þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022. apríl |

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir fínstillingu áætlanagerðar](planning-optimization-overview.md)

[Hafist handa með fínstillingu áætlanagerðar](get-started.md)

[Munur á milli hefðbundinnar aðaláætlanagerðar og fínstillingar áætlanagerðar](planning-optimization-differences-with-built-in.md)

[Færibreytur ekki notaðar af fínstillingu áætlanagerðar](not-used-parameters.md)

[Skoða áætlunarferil og skipulagsannála](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
