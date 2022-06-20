---
title: Flokkaðu færslur og uppsafnaða útreikninga með því að nota GROUPBY gagnaveitur
description: Þessi grein útskýrir hvernig þú getur notað GROUPBY gerð gagnagjafa í rafrænni skýrslugerð (ER).
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b20b5db0794157560f27f15594a84083966642f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861788"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Flokkaðu færslur og uppsafnaða útreikninga með því að nota GROUPBY gagnaveitur

[!include[banner](../includes/banner.md)]

Þegar þú stillir [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) líkanakortanir eða snið, þú getur [Bæta við](#AddMmDataSource2) nauðsynlegar gagnaheimildir **GroupBy** tegund.

Á hönnunartíma, a **GroupBy** gagnagjafi er stilltur til að bera kennsl á eftirfarandi þætti:

- A [grunnuppspretta gagna](#BaseDataSource) sem inniheldur færslur sem verða flokkaðar á keyrslutíma
- [Flokkun reita](#GroupingFields) af grunngagnagjafanum, sem verður notaður til að flokka skrár á keyrslutíma
- [Samanlögð aðgerðir](#AggregateFunctions) sem tilgreina heildarútreikninga sem verða gerðir fyrir hvern fundinn hóp á keyrslutíma

Á keyrslutíma, stillt **GroupBy** gagnaveita flokkar færslur sem hafa sömu gildi í flokkunarreitunum og skilar síðan lista yfir færslur. Hver skrá táknar einn hóp. Fyrir hvern hóp afhjúpar gagnagjafinn svæðisgildin sem upphafsfærslurnar voru flokkaðar eftir, gildi útreiknuðu uppsafnaða fallanna og lista yfir færslur grunngagnagjafans sem tilheyrir hópnum.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Samanlögð aðgerðir

Á keyrslutíma eru allir samanlagðir útreikningar gerðir fyrir hvern hóp skráa. Þessi útreikningur er gerður með því að nota gildi eins reits eða tjáningar í skrám gagnagjafa sem var valinn til að flokka í breytanlega gagnagjafa **GroupBy** tegund. Eftirfarandi heildaraðgerðir eru studdar eins og er:

- **AVG** – Þessi aðgerð skilar meðaltali gilda í hópi. Það er aðeins hægt að nota með tölulegum sviðum.
- **COUNT** – Þessi aðgerð skilar fjölda hluta sem fundust í hópi.
- **Min** – Þessi aðgerð skilar lágmarksgildi meðal gilda í hópi.
- **Hámark** – Þessi aðgerð skilar hámarksgildi meðal gilda í hópi.
- **SUMMA** – Þessi aðgerð skilar summu allra gilda í hópi. Það er aðeins hægt að nota með tölulegum sviðum.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Staðsetning keyrslu

Þegar þú breytir a **GroupBy** gagnagjafa og tilgreindu grunngagnagjafann sem inniheldur færslurnar sem þarf að flokka, kerfið finnur sjálfkrafa skilvirkustu [staðsetningu](#ExecutionLocation) fyrir framkvæmd þess **GroupBy** gagnagjafa. Ef grunngagnagjafinn er [fyrirspurnahæft](er-functions-list-filter.md#usage-notes) (þ.e. ef hægt er að keyra hann á gagnagrunnsstigi), er forritagagnagrunnurinn einnig tilgreindur sem framkvæmdarstaður breytanlegs **GroupBy** gagnagjafa. Annars er minni forritaþjónsins tilgreint sem framkvæmdarstaður.

Þú getur handvirkt breytt sjálfvirkri framkvæmdarstaðsetningu með því að velja staðsetningu sem á við um stillta gagnagjafann. Ef framkvæmdarstaðurinn sem er valinn á ekki við, a [staðfestingarvilla](er-components-inspections.md#i5) er hent á hönnunartíma.

> [!TIP]
> Við mælum með því að þú notir gagnagrunnsstaðsetninguna til að flokka gagnagjafa sem afhjúpa mikinn fjölda gagna.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Minnisnotkun

Sjálfgefið, ef a **GroupBy** gagnagjafi er keyrður í minni, er minni forritaþjónsins notað til að geyma færslur um grunngagnagjafa sem tilheyrir hverjum fundinum hópi sem færslur á einum hópi. Til að draga úr minnisnotkun er hægt að bæla niður geymslupláss fyrir **GroupBy** gagnagjafar ef þeir voru stilltir til að reikna aðeins samanlagðar aðgerðir og færslur hóps þeirra eru ekki notaðar á keyrslutíma. Til að draga úr minnisnotkun á þennan hátt, virkjaðu **Draga úr minnisnotkun í ER þegar færsluflokkun er aðeins notuð til að reikna samansafn** eiginleiki í **Eiginleikastjórnun** vinnurými.

## <a name="alternatives"></a><a name="Alternatives"></a> Valkostir

Hægt er að reikna svipaðar samanlagnir með því að nota [öðruvísi](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) tegundir gagnagjafa eða ER innbyggðar aðgerðir.

Til að læra meira um þennan eiginleika skaltu ljúka við dæmið sem fylgir.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Dæmi: Notaðu GROUPBY gagnagjafa fyrir uppsafnaða útreikninga og skráningarflokkun

Þetta dæmi sýnir hvernig notandi í hlutverki kerfisstjóra eða rafrænnar skýrslugerðar ráðgjafa getur stillt ER líkanavörpun sem hefur **HÓPBYGGING** gagnagjafi sem er notaður til að reikna út samanlagðar aðgerðir og hópskrár. Þessi líkanvörpun er notuð til að prenta eftirlitsskýrsluna þegar Intrastat yfirlýsingin er mynduð. Sú skýrsla gerir þér kleift að skoða tilkynntar Intrastat færslur.

Hægt er að ljúka verklagsreglunum í þessu dæmi í **DEMF** fyrirtæki í Microsoft Dynamics 365 Fjármál. 

### <a name="prepare-sample-data"></a>Undirbúa sýnishornsgögn

Gakktu úr skugga um að þú hafir Intrastat færslur til að tilkynna um **Intrastat** síðu. Þú verður að hafa færslur fyrir mismunandi flutningskóða, því þú flokkar færslur eftir **Flutningur** reit í þessu dæmi.

![Undirbúningur Intrastat færslur á Intrastat síðunni.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ER ramma til að hanna ER líkanakortlagningu.

### <a name="import-the-standard-er-format-configuration"></a>Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs

Fylgdu skrefunum í [Flytja inn staðlaða ER sniðstillingu](er-quick-start2-customize-report.md#ImportERSolution1) til að bæta stöðluðum ER stillingum við núverandi tilvik þitt af Dynamics 365 Finance. Flytja inn útgáfu 1 af **Intrastat líkan** stillingar úr geymslunni.

### <a name="create-a-custom-data-model-configuration"></a>Búðu til sérsniðna gagnalíkanstillingu

Fylgdu skrefunum í [Bættu við sérsniðinni gagnalíkönstillingu](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) til að bæta við nýju handvirkt **Intrastat líkan (Litware)** Uppsetning ER gagnalíkans sem þú færð úr innfluttu **Intrastat líkan** stillingar.

### <a name="configure-a-custom-data-model-component"></a>Stilltu sérsniðna gagnalíkan íhlut

Fylgdu þessum skrefum til að gera nauðsynlegar breytingar á afleiddu **Intrastat líkan (Litware)** gagnalíkan, þannig að hægt sé að nota það til að afhjúpa flutningskóða sem hafa nauðsynlegar upplýsingar.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, í stillingartrénu, veldu **Intrastat líkan (Litware)**.
3. Veljið **Hönnuður**.
4. Á **Hönnuður gagnalíkana** síðu, í líkanatrénu, veldu **Intrastat**.
5. Veldu **Nýtt** til að bæta við nýjum hreiðri hnút fyrir valinn **Intrastat** hnút. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **Flutningur**.
    2. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

6. Veldu **Nýtt** til að bæta við nýjum hreiðri hnút fyrir **Flutningur** hnút sem þú varst að bæta við. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **Kóði**.
    2. Í reitnum **Gerð vöru** velurðu **Strengur**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

7. Veldu **Nýtt** til að bæta við öðrum nýjum hreiðri hnút fyrir **Flutningur** hnút. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **TotalInvoicedAmount**.
    2. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

8. Veldu **Nýtt** til að bæta við öðrum nýjum hreiðri hnút fyrir **Flutningur** hnút. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **NumberOfTransactions**.
    2. Velja **Heiltala** í svæðinu **gerð Vöru**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

9. Veldu **Nýtt** til að bæta við öðrum nýjum hreiðri hnút fyrir **Flutningur** hnút. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í **Nafn** reit, slá inn **Viðskipti**.
    2. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

10. Fyrir **Viðskipti** hnút sem þú varst að bæta við, á **Hnútur** Flýtiflipi, veldu **Skipta um vörutilvísun**.
11. Í **Skipta um vörutilvísun** valmynd, í gagnalíkantrénu, veldu **Vöruskrá**. Veljið síðan **Í lagi**.

![Skilgreint gagnalíkan í gagnalíkanahönnuði rafrænnar skýrslugerðar.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Ljúktu við hönnun sérsniðins gagnalíkans

Fylgdu skrefunum í [Ljúktu við hönnun gagnalíkans](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) til að ljúka hönnun hins afleidda **Intrastat líkan (Litware)** gagnalíkan.

### <a name="create-a-new-model-mapping-configuration"></a>Stofna nýja skilgreiningu líkanavörpunar

Fylgdu skrefunum í [Búðu til nýja gerð kortlagningarstillingar](er-quick-start1-new-solution.md#CreateModelMapping) til að bæta við nýju handvirkt **Intrastat sýniskortlagning** ER líkan kortlagningarstillingar fyrir afleidda **Intrastat líkan (Litware)** stillingar.

### <a name="add-a-new-model-mapping-component"></a>Bættu við nýjum líkanakortlagningarhluta

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á **Stillingar** síðu, í stillingartrénu, stækkaðu **Intrastat líkan** stillingar.
3. Veldu **Intrastat sýniskortlagning** stillingar.
4. Veldu **Hönnuður** til að opna lista yfir varpanir.
5. Veldu **Eyða** til að fjarlægja núverandi kortlagningarhluta.
6. Veldu **Nýtt** til að bæta við nýjum kortlagningarhluta.
7. Í **Skilgreining** reit, veldu **Intrastat**.
8. Í **Nafn** reit, slá inn **Intrastat kortlagning**.
9. Veldu **Hönnuður** til að stilla nýju kortlagninguna.

### <a name="design-the-added-model-mapping-component"></a>Hannaðu viðbætta líkankortahlutann

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Bættu við gagnagjafa til að fá aðgang að forritatöflu

Stilltu gagnagjafa til að fá aðgang að forritatöflunum sem innihalda upplýsingar um Intrastat færslur.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Töflufærslur**.
2. Í **Uppsprettur gagna** rúðu, veldu **Bæta við rót** til að bæta við nýjum gagnagjafa sem verður notaður til að fá aðgang að **Intrastat** borð. Hvert met í **Intrastat** taflan táknar eina Intrastat færslu.
3. Í **Eiginleikar gagnagjafa** valmynd, í **Nafn** reit, slá inn **Viðskipti**.
4. Í **Tafla** reit, slá inn **Intrastat**.
5. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Bættu við gagnagjafa til að flokka Intrastat-færslur

Stilla a **GroupBy** gagnagjafi til að flokka Intrastat færslur og reikna samanlagðar aðgerðir.

1. Á **Módelkortahönnuður** síðu, í **Tegundir gagnagjafa** rúðu, veldu **Aðgerðir\\ Hópur eftir**.
2. Í **Uppsprettur gagna** rúðu, veldu **Bæta við rót** til að bæta við nýjum gagnagjafa sem verður notaður til að flokka Intrastat færslur og reikna samanlagðar aðgerðir.
3. Í **Eiginleikar gagnagjafa** valmynd, í **Nafn** reit, slá inn **Flutningaskrá**.
4. Veldu **Breyta hópi eftir** til að stilla flokkunarskilyrði.
5. Á **Breyta 'Group By' færibreytum** síðu, í gagnaheimildalistanum í hægri glugganum, veldu **Viðskipti** gagnagjafa og stækka hana.
6. Veldu **Bæta reit við \> Hvað á að hópa** til að gefa til kynna að **Viðskipti** gagnagjafi er valinn sem <a name="BaseDataSource">grunnuppspretta gagna</a> fyrir stillta **GroupBy** gagnagjafa. Skrár yfir **Viðskipti** gagnagjafi verður flokkaður og svæðisgildi þessa gagnagjafa verða notuð fyrir útreikninga í samanlagðri föllum.
7. Veldu **Færsla\flutningur** reit og veldu síðan **Bæta reit við \> Hópað svið** til að gefa til kynna að **Flutningur** reit grunngagnagjafans er valið sem <a name="GroupingFields">flokkunarviðmiðun</a> fyrir stillta **GroupBy** gagnagjafa. Með öðrum orðum, skrár yfir **Viðskipti** gagnagjafi verður flokkaður út frá verðmæti **Flutningur** sviði. Sérhver skrá yfir stillt **GroupBy** gagnagjafi mun tákna einn flutningskóða sem hefur fundist í skrám grunngagnagjafans.
8. Veldu **Færsla\Upphæð MST** reit og fylgdu síðan þessum skrefum:

    1. Veldu **Bæta reit við \> Samanlagt reitir** að gefa til kynna að an<a name="AggregateFunctions">samanlagt fall</a> verður reiknað fyrir þennan reit.
    2. Í **Söfnun** glugganum, í færslunni sem hefur verið bætt við fyrir valið **Færsla\Upphæð MST** sviði, í **Aðferð** reit, veldu **Summa** virka.
    3. Í **Nafn** valfrjáls reit, slá inn **TotalInvoicedAmount**.

    Þessar stillingar tilgreina að fyrir hvern flutningshóp, heildarupphæð **Færsla\Upphæð MST** reit verður reiknað út.

9. Veldu **Færsla\RecId** reit og fylgdu síðan þessum skrefum:

    1. Veldu **Bæta reit við \> Samanlagt reitir** til að gefa til kynna að uppsafnað fall verði reiknað fyrir þennan reit.
    2. Í **Söfnun** glugganum, í færslunni sem hefur verið bætt við fyrir valið **Færsla\RecId** sviði, í **Aðferð** reit, veldu **Telja** virka.
    3. Í **Nafn** valfrjáls reit, slá inn **NumberOfTransactions**.

    Þessar stillingar tilgreina að fyrir hvern flutningshóp verði fjöldi færslur í hópnum reiknaður út.

10. Veldu **Vista**.
11. Skoðaðu<a name="ExecutionLocation">framkvæmd</a> færibreytur gagnagjafans sem hægt er að breyta. Taktu eftir því **Sjálfvirk skynjun** hefur verið valið sjálfkrafa í **Framkvæmdarstaður** sviði, og **Framkvæmd kl** reiturinn inniheldur gildið **SQL**. Þessar stillingar tilgreina að valið **Viðskipti** grunngagnauppspretta er nú hægt að spyrja, og þú getur keyrt breytanlegt **GroupBy** gagnagjafa á gagnagrunnsstigi.
12. Opnaðu leitina fyrir **Framkvæmdarstaður** reit til að skoða lista yfir tiltæk gildi. Taktu eftir að þú getur valið **Fyrirspurn** eða **Í minningu** að þvinga þetta fram **GroupBy** gagnagjafa sem á að keyra á gagnagrunnsstigi eða í minni forritaþjónsins.
13. Veldu **Vista**, og lokaðu **Breyta 'Group By' færibreytum** síðu.
14. Veldu **Allt í lagi** til að klára stillingar á **GroupBy** gagnagjafa.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> Bindið GroupBy gagnagjafa við reiti gagnalíkana

Binddu stillta gagnagjafann við reiti gagnalíkans til að tilgreina hvernig gagnalíkanið verður fyllt út með forritsgögnum á keyrslutíma.

1. Á **Módelkortahönnuður** síðu, í **Gagnalíkan** rúðu, stækkaðu **Flutningur** hnút.
2. Í **Uppsprettur gagna** rúðu, stækkaðu **Flutningaskrá** gagnagjafa.
3. Bættu við bindingu til að afhjúpa lista yfir uppgötvaða flutningshópa:

    1. Í **Gagnalíkan** glugga, veldu **Flutningur** atriði.
    2. Í **Uppsprettur gagna** glugga, veldu **Flutningaskrá** gagnagjafa.
    3. Veldu **Binda**.

4. Bættu við bindingu til að afhjúpa flutningskóða hvers uppgötvaðrar flutningshóps:

    1. Veldu **Flutningskóði** gagnalíkan hlut.
    2. Veldu **TransportRecord.grouped.TransportMode** flokkað svæði.
    3. Veldu **Binda**.

5. Bættu við bindingu til að afhjúpa gildi reiknaðra heildarfalla fyrir hvern uppgötvaðan flutningshóp:

    1. Veldu **Transport.NumberOfTransactions** gagnalíkan hlut.
    2. Veldu **TransportRecord.aggregated.NumberOfTransactions** samanlagður reitur.
    3. Veldu **Binda**.
    4. Veldu **Transport.TotalInvoicedAmount** gagnalíkan hlut.
    5. Veldu **TransportRecord.aggregated.TotalInvoicedAmount** samanlagður reitur.
    6. Veldu **Binda**.

6. Bættu við bindingu til að afhjúpa færsluskrár sem tilheyra hverjum uppgötvaðum flutningshópi:

    1. Veldu **Flutningur.Viðskipti** gagnalíkan hlut.
    2. Veldu **TransportRecord.lines** sviði.
    3. Veldu **Binda**.

    Þú getur haldið áfram að stilla bindingar fyrir hreiður atriði í **Flutningur.Viðskipti** gagnalíkan atriði og **TransportRecord.lines** reit gagnagjafa til að afhjúpa, á keyrslutíma, upplýsingar um Intrastat-færslurnar sem tilheyra hverjum uppgötvaðum flutningshópi.

![Skilgreind líkanavörpun í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Kembiforritið sem bætt var við líkanakortlagningarhlutann

Nota [Villuleitari fyrir ER gagnagjafa](er-debug-data-sources.md) til að prófa uppsetta líkanavörpunina.

1. Á **Módelkortahönnuður** síðu, veldu **Byrjaðu að kemba**.
2. Á **Villuleit gagnaveitur** síðu, í vinstri glugganum, veldu **Flutningaskrá** gagnagjafi og veldu síðan **Lestu allar skrár**.
3. Stækkaðu **Flutningaskrá** gagnagjafa og fylgdu síðan þessum skrefum:

    1. Veldu **TransportRecord.grouped.TransportMode** gagnagjafa.
    2. Veldu **Sækja gildi**.
    3. Veldu **TransportRecord.grouped.NumberOfTransactions** gagnagjafa.
    4. Veldu **Sækja gildi**.
    5. Veldu **TransportRecord.grouped.TotalInvoicedAmount** gagnagjafa.
    6. Veldu **Sækja gildi**.

4. Í hægri glugganum velurðu **Auka allt**.

The **Flutningaskrá** gagnagjafi afhjúpar tvær skrár og sýnir tvo flutningskóða. Fyrir hvern flutningskóða er reiknaður fjöldi færslna og heildarupphæð reikninga.

> [!NOTE]
> „Latur lestur“ nálgunin er notuð þegar a **GroupBy** gagnagjafi er kallaður til að hámarka gagnagrunnssímtöl. Þess vegna eru sum svæðisgildanna í a **GroupBy** gagnagjafar eru aðeins reiknaðir í villuleitarforriti ER gagnagjafar þegar þeir eru bundnir við gagnalíkanareit.

![Niðurstöður villuleitar gagnauppsprettu á síðunni Villuleit gagnaheimildir.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Er einhver leið til að reikna út heildartölur þegar heildarsamtölur eru reiknaðar?

Já. Til að reikna heildartölur skaltu stilla aðra **GroupBy** gagnaveita þar sem **GroupBy** gagnagjafi sem þú áður stilltir er notaður sem grunngagnagjafi. Eftirfarandi mynd sýnir **Samtals** gagnauppspretta **GroupBy** tegund sem er notuð til að reikna samanlagðann **SUMMA** fall, byggt á **SUMMA** samansafn af **Flutningaskrá** gagnauppspretta **GroupBy** tegund.

![Heildaruppspretta gagna í ER líkanskortahönnuðinum.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Eftirfarandi mynd sýnir niðurstöður **Samtals** villuleit gagnagjafa.

![Niðurstöður kembiforrita fyrir heildargagnauppsprettu á síðunni Villuleita gagnaveitur.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu](er-debug-data-sources.md)
- [Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
