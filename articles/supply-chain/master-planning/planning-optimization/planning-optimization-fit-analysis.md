---
title: Samræmisgreining á fínstillingu áætlanagerðar
description: Þessi grein útskýrir hvernig á að sannreyna núverandi uppsetningu og gögn með hliðsjón af getu skipulagsfínstillingaraðgerðarinnar.
author: t-benebo
ms.date: 08/11/2022
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 4459a5d72fafe2596b7fc0cedf060b8f23bb43d2
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750708"
---
# <a name="planning-optimization-fit-analysis"></a>Samræmisgreining á fínstillingu áætlanagerðar

[!include [banner](../../includes/banner.md)]

Þú ættir að greina útkomuna úr samræmisgreiningu á fínstillingu skipulagningar sem hluti af flutningsferlinu. Athugaðu að umfang fínstillingar áætlanagerðar er ekki jafnt og úreltri virkni aðalskipulagsvélar. Við mælum með því að þú vinnir með samstarfsaðilanum og lesir fylgiskjölin til að undirbúa flutninginn.

Fitunargreining áætlanagerðarfínstillingar hjálpar þér að bera kennsl á hvar niðurstaðan gæti verið frábrugðin úreltri aðalskipulagsvél og áætlanagerð fínstillingu. Þessi greining er unnin út frá núverandi uppsetningu og gögnum. 

Til að sjá útkomu samræmisgreiningar á fínstillingu skipulagningar skal farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Samræmisgreining á fínstillingu skipulagningar** og síðan velja **Keyra greiningu**. Ef greiningin finnur fyrir ósamræmi eru þau skráð á sömu síðu. (Greiningin getur tekið nokkrar mínútur í keyrslu.)

> [!NOTE]
>
> - Ekki er hægt að bera kennsl á ósamræmi í samræmisgreiningu fínstillingar áætlanagerðar. Frekari upplýsingar er að finna í [Munur á milli hefðbundinnar aðaláætlanagerðar og fínstillingar áætlanagerðar](planning-optimization-differences-with-built-in.md).
>
> - Ef ósamræmi finnst, getur þú samt notað fínstillingu skipulagsins. Niðurstöður samsvörunargreiningar sýna bara staði þar sem skipulagsþjónustan mun ekki heiðra núverandi uppsetningu. Með öðrum orðum sýna þær staði þar sem einhver ferli kunna að vera hunsuð eða ekki studd.

## <a name="analysis-results-example-1"></a>Niðurstöður greiningar: Dæmi 1

- **Eiginleiki:** Framleiðsla
- **Mál:** Vörur með uppskriftarstig hærra en núll: 56
- **Útskýring:** Samræmisgreiningin fann 56 vörur sem eru með uppskriftaruppsetningu fyrir framleiðslu. Vegna þess að núverandi útgáfa af fínstillingu áætlunargerðar styður ekki framleiðslu mun fínstilling áætlunarinnar búa til innkaupatillögur í stað framleiðslutillaga. Hún mun einnig sýna viðvörun sem sýnir vörurnar sem varða fyrir áhrifum.

## <a name="analysis-results-example-2"></a>Niðurstöður greiningar: Dæmi 2

- **Eiginleiki:** Aðgerðir
- **Mál:** Þekjuhópar með útreikninga á aðgerðum virkjaða: 6
- **Útskýring:** Samsvörunargreiningin fann sex þekjuhópa þar sem kveikt er á útreikningi á aðgerðum. Þar sem núverandi útgáfa af fínstillingu áætlunarinnar styður ekki aðgerðir verða engar aðgerðir myndaðar við aðalskipulagningu.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Yfirlit yfir mögulegar niðurstöður samræmisgreiningar

Eftirfarandi tafla sýnir hinar ýmsu niðurstöður sem hægt er að sýna eftir samræmisgreiningu. Númeramerkjum (*\#*) verður skipt út fyrir númer sem tilgreinir fjölda færslna sem eru með uppgefið vandamál.

> [!IMPORTANT]
> Fyrir eiginleika sem enn eru ekki studdir, gefur eftirfarandi tafla upplýsingar um væntanlegar upplýsingar sem eru áætlaðar út frá núverandi vegakorti okkar. Þessar áætlanir geta breyst án fyrirvara.

| Eiginleiki | Uppgefið vandamál | Skýring | Væntanlegt framboð |
| --- | --- | --- | --- |
| Aðgerðir | Þekjuflokkar með virkan útreikning á aðgerðum: *\#* | Þessi eiginleiki er nú studdur. | Stutt |
| Grunndagatöl | Dagatöl sem nota grunndagatal: *\#* | Þessi eiginleiki er nú studdur. | Stutt | 
| Ráðstöfunarkóðar runu | Aðalrunuráðstafanir sem eru ekki nettó: *\#* | Þessi eiginleiki er nú studdur. Fyrir frekari upplýsingar, sjá [Notaðu lotuúthlutunarkóða til að merkja lotur sem tiltækar eða ekki tiltækar](../../inventory/batch-disposition-codes.md) | Stutt |
| Hægt að lofa (CTP) | Sjálfgefnar pöntunarstillingar með afhendingardagsstjórn stillta á afhendingargetu: *\#* | Í Supply Chain Management 10.0.28 og nýrri, ferli sem kallast *CTP fyrir hagræðingu áætlanagerðar* gerir staðfestar sendingar og móttökudagsetningar aðgengilegar eftir að kraftmikla áætlunin hefur verið keyrð. Fyrir eldri útgáfur af Supply Chain Management er eldri CTP stilling hunsuð þegar áætlanagerð fínstilling er virkjuð. | Stutt |
| Staðfesting | Þekjuhópar með stillt tímamörk staðfestinga: *\#* | Í útgáfu 10.0.7 og nýrri er staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn *Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar* hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. | Stutt |
| Staðfesting | Vöruþekjufærslur með sjálfvirka staðfestingu stillta: *\#* | Í útgáfu 10.0.7 og nýrri er sjálfvirk staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn *Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar* hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. | Stutt |
| Staðfesting | Aðaláætlanir með sjálfvirka staðfestingu stillta: *\#* | Í útgáfu 10.0.7 og nýrri er sjálfvirk staðfesting studd sem aðskilin runuvinnsla staðfestingar þegar aðaláætlanagerð er lokið (að því gefnu að eiginleikinn *Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar* hafi verið gerður virkur í [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Athugið að sjálfvirk staðfesting fínstillingar áætlanagerðar byggir á pöntunardagsetningunni (upphafsdegi), ekki dagsetningu þarfa (lokadegi). Þessi hegðun tryggir að staðfesting áætlaðra pantana gerist á réttum tíma, án þess að þurfa að hafa afhendingartíma tíma í tímamörkum staðfestingar. | Stutt |
| FitAnalysisPlanningItems | Vörur í áætlun: *\#* | Þessi eiginleiki í bið. Sem stendur eru vörur í áætlun meðhöndlaðar eins og venjulegar vörur þegar fínstilling áætlanagerðar er virk. | 2022 útgáfubylgja 2 eða síðar |
| Spá | Þekjuflokkar með „Hafa með pantanir innan samstæðu“: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Áætlanagerð innan samstæðu](Intercompany-planning.md) | Stutt |
| Spá | Þekjuflokkar með „Draga úr spá um“ stillinguna stillta á annað gildi en „Pantanir“: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md) | Stutt |
| Spá | Spárlíkön með undirspárlíkönum: *\#* |  Þessi eiginleiki er nú studdur. Frekari upplýsingar eru í [Aðaláætlanagerð með eftirspurnarspám](demand-forecast.md) | Stutt |
| Spá | Aðaláætlanir með „Hafa með birgðaspá“ virkt: *\#* | Þessi eiginleiki í bið. Sem stendur eru birgðaspár ekki studdar þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. | 2022 útgáfubylgja 2 eða síðar |
| Tímamörk frystingar | Þekjuhópar með stillt tímamörk frystingar: *\#* | Þessi eiginleiki í bið. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Tímamörk frystingar | Vöruþekjufærslur með stillt tímamörk frystingar: *\#* | Þessi eiginleiki í bið. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Tímamörk frystingar | Aðaláætlanir með stillt tímamörk frystingar: *\#* | Þessi eiginleiki í bið. Sem stendur er litið framhjá tímamörkum frystingar þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Innan samstæðu | Aðaláætlanir þ.m.t. áætluð eftirspurn forstreymis: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Áætlanagerð innan samstæðu](Intercompany-planning.md) | Stutt |
| Kanban | Vöruþekjufærslur með áætlaða kanban-pöntunargerð: *\#* | Þessi eiginleiki í bið. Sem stendur verður vöruþekja sem stillt er á kanban hunsuð þegar fínstilling áætlanagerðar er virk. Áætluð kanban-pöntunargerð býr til viðvörun við aðaláætlanagerð og áætlaðar innkaupapantanir verða búnar til til að ná yfir viðeigandi eftirspurn. | Framtíðarbylgja |
| Kanban | Vörur með sjálfgefna kanban-pöntunargerð: *\#* | Sem stendur verður sjálfgefin pöntunargerð sem stillt er á kanban hunsuð þegar fínstilling áætlanagerðar er virk. Áætluð kanban-pöntunargerð býr til viðvörun við aðaláætlanagerð og áætlaðar innkaupapantanir verða búnar til til að ná yfir viðeigandi eftirspurn. | Framtíðarbylgja |
| Lífferilsstaða afurðar | Lífferilsstaða afurðar ekki virk fyrir áætlanagerð: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Útiloka afurðir sem hafa tilteknar lífferilsstöður afurðar](product-lifecycle-state.md) | Stutt |
| Framleiðsla | Uppskriftarlínur með sléttun eða margfeldi í uppsetningu: *\#* | Þessi eiginleiki í bið. Sem stendur verða uppsetningar með sléttun og margfeldi hunsaðar í uppskriftarlínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | Framtíðarbylgja|
| Framleiðsla | Uppskriftar-/formúlulínur með formúlumælingu: *\#* | Þessi eiginleiki í bið. Sem stendur er formúlumæling hunsuð í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Framleiðsla | Uppskriftar-/formúlulínur með staðgengisvörur (áætlunarflokkar): *\#* | Þessi eiginleiki í bið. Sem stendur er staðgengilsvara (áætlunarflokkar) hunsaður í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Framleiðsla | Uppskriftar-/formúlulínur með neikvæðu magni: *\#* | Þessi eiginleiki í bið. Uppskriftar- og formúlulínur sem eru með neikvæðu magni fá magnið 0 (núll) og viðvörun verður gefin út þegar fínstilling áætlanagerðar er virkjuð. Uppfæra aðalgögn til að forðast viðvaranir. | 2022 útgáfubylgja 2 |
| Framleiðsla | Uppskriftar-/formúlulínur með tilfanganotkun: *\#* | Þessi eiginleiki í bið. Sem stendur eru uppskriftar- og formúlulínur sem eru með tilfanganotkun hunsaðar þegar fínstilling áætlanagerðar er virk. Þegar þessi eiginleiki er studdur verður efnisþörfinni stillt á upphafsdagsetningu framleiðslunnar. Þar til þessi eiginleiki er studdur verða kröfur ekki myndaðar fyrir efni sem eru merkt með flaggi tilfanganotkunar. | 2022 útgáfubylgja 2 |
| Framleiðsla | Uppskrifta-/formúlulínur með skrefanotkun: *\#* | Þessi eiginleiki í bið. Sem stendur er skrefanotkun hunsuð í uppskriftar- og formúlulínum þegar fínstilling áætlanagerðar er virk. | 2022 útgáfubylgja 2 |
| Framleiðsla | Uppskriftir með stöðugri rýrnun eða breytilegri rýrnun skilgreindar: *\#* | Þessi eiginleiki í bið. Sem stendur er föst rýrnun og breytileg rýrnun, sem skilgreindar eru í uppskriftum, hunsaðar þegar fínstilling áætlanagerðar er virk. | 2022 útgáfubylgja 2 |
| Framleiðsla | Uppskriftir með úthýsingu: *\#* | Þessi eiginleiki er nú studdur. | Stutt |
| Framleiðsla | Uppskriftir án svæðis: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Framleiðsluáætlun](production-planning.md) | Stutt |
| Framleiðsla | Senda beiðni með skilgreindum kröfum fyrir tiltekna uppskrift eða leið: *\#* | Þessi eiginleiki í bið. Sem stendur eru tilteknar kröfur uppskriftar eða leiðar, sem skilgreindar eru í eftirspurninni (t.d. undiruppskrift eða undirleið í sölupöntun), hunsaðar þegar fínstilling áætlanagerðar er virk. Stöðluð uppskrift eða leið verður notuð, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Framleiðsla | Formúluútgáfur með auka-/hliðarafurðir: *\#* | Þessi eiginleiki í bið. Sem stendur eru aukaafurðir og hliðarafurðir, sem tengjast formúluútgáfunni, hunsaðar þegar fínstilling áætlanagerðar er virk. | 2022 útgáfubylgja 2 |
| Framleiðsla | Formúluútgáfur með arði: *\#* | Þessi eiginleiki í bið. Sem stendur er arðurinn sem tengist formúluútgáfunni hunsaður þegar fínstilling áætlanagerðar er virk. | 2022 útgáfubylgja 2 |
| Framleiðsla | Áætlanir sem fela í sér röðun: *\#* | Þessi eiginleiki í bið. Sem stendur er röðun hunsuð þegar fínstilling áætlanagerðar er virk, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Framleiðsla | Útgefnar framleiðslupantanir sem ekki byrjað á, þar sem áætluð byrjun er á undan deginum í dag: *\#* | Þessi eiginleiki í bið. Eins og er, ef framleiðslupöntun seinkar, mun aðaláætlanagerð gera ráð fyrir því að henni verði lokið í dag. Þetta á við um útgefnar framleiðslupantanir þar sem afhendingardagsetning er í fortíðinni, en hefur ekki verið lokið. | 2022 útgáfubylgja 2 |
| Framleiðsla | Tímasett tilföng með takmarkaða getu: *\#* | Þessi eiginleiki er nú studdur.| Stutt |
| Framleiðsla | Leiðir notaðar við áætlanagerð: *\#* | Þessi eiginleiki er studdur. | Stutt |
| Framleiðsla | Frátekningaraðferð sölulínu með frátekningu: *\#* | Frátekning sölulínu sem notar útþenslu er ekki studd þegar fínstilling áætlanagerðar er virk. | 2022 útgáfubylgja 2 |
| Framleiðsla | Áætlanagerð með frátekningu framleiðslupantana: *\#* | Áætlanagerð sem notar útþenslu framleiðslupantana er ekki studd þegar fínstilling áætlanagerðar er virk. Hægt er að áætla hverja framleiðslupöntun fyrir sig. | 2022 útgáfubylgja 2 |
| Beiðnir um tilboð | Aðaláætlanir með beiðnir um tilboð virkar: *\#* | Þessi eiginleiki í bið. Sem stendur er ekki litið á beiðnir um tilboð sem eftirspurn þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Innkaupabeiðnir | Aðaláætlanir með virkar innkaupabeiðnir: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Innkaupabeiðnir](purchase-requisitions.md) | Stutt |
| Öryggismörk | Þekjuflokkar með öryggismörk: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Öryggismörk](safety-margins.md) | Stutt |
| Öryggismörk | Aðaláætlanir með öryggismörk: *\#* | Þessi eiginleiki er nú studdur. Frekari upplýsingar má finna í [Öryggismörk](safety-margins.md) |  Stutt |
| Sölutilboð | Aðaláætlanir með virk sölutilboð: *\#* | Þessi eiginleiki í bið. Sem stendur er ekki tekið tillit til tilboða þegar fínstilling áætlanagerðar er virk. Þær verða hunsaðar, óháð þessari stillingu. | 2022 útgáfubylgja 2 |
| Endingartími | Aðaláætlanir með virkan endingartíma: *\#* | Þessi eiginleiki er nú studdur. | Stutt |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Aðalskipulagskerfisarkitektúr](../master-planning-architecture.md)
- [Byrjaðu á aðalskipulagi](get-started.md)
- [Munur á milli hefðbundinnar aðaláætlanagerðar og fínstillingar áætlanagerðar](planning-optimization-differences-with-built-in.md)
- [Færibreytur ekki notaðar af fínstillingu áætlanagerðar](not-used-parameters.md)
- [Skoða áætlunarferil og skipulagsannála](plan-history-logs.md)
- [Keyra áætlanagerð fyrir hlutmengi](plan-filters.md)
- [Hætta við áætlunarvinnslu](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
