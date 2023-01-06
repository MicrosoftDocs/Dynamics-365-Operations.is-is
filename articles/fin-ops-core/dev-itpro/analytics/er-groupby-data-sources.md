---
title: Flokka færslur og leggja saman útreikninga með því að nota GROUPBY-gagnagjafa
description: Þessi grein útskýrir hvernig hægt er að nota gagnagjafa af GROUPBY-gerð í rafrænni skýrslugerð (ER).
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 0e520705d2441ead5a68ec3284db74999b3d90b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277573"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Flokka færslur og leggja saman útreikninga með því að nota GROUPBY-gagnagjafa

[!include[banner](../includes/banner.md)]

Við stillingu á líkanavörpun eða sniðmáta [rafrænnar skýrslugerðar (ER)](general-electronic-reporting.md) er hægt að [bæta við](#AddMmDataSource2) áskilins gagnagjafa af gerðinni **GroupBy**.

Á hönnunartíma er **GroupBy** gagnagjafi skilgreindur til að bera kennsl á eftirfarandi einingar:

- [Grunngagnagjafi](#BaseDataSource) sem inniheldur færslur sem verða flokkaðar á keyrslutíma
- [Flokkunarreitir](#GroupingFields) grunngagnagjafa verða notaðir fyrir færsluflokkun við keyrslu
- [Samanlagðar aðgerðir](#AggregateFunctions) sem tilgreina samanlagða útreikninga sem gerðir verða fyrir hvern uppgötvaðan hóp við keyrslu

Við keyrslu flokkar skilgreindur **GroupBy** gagnagjafi færslur sem eru með sömu gildi í flokkunarreitum og skilar síðan lista yfir færslur. Hver færsla stendur fyrir einn hóp. Fyrir hvern flokk sýnir gagnagjafinn reitargildin sem upphaflegu færslurnar voru flokkaðar eftir, gildi reiknaðra samanlagðra aðgerða og lista yfir færslur grunngagnagjafa sem tilheyrir flokknum.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Samsteypuaðgerðir

Á keyrslutíma eru allir samanlagðir útreikningar gerðir fyrir hvern hóp færslna. Þessi útreikningur er gerður með því að nota gildi eins reits eða segðar í færslum gagnagjafa sem var valinn fyrir flokkun í breytilegum gagnagjafa af gerðinni **GroupBy**. Eftirfarandi safnaðgerðir eru studdar eins og er:

- **AVG** – Þetta fall skilar meðaltalinu af gildunum í hópi. Aðeins er hægt að nota þetta með tölureitum.
- **COUNT** – Þessi aðgerð skilar fjölda þeirra hluta sem fundust í hóp.
- **Lágm.** – Þetta fall skilar lágmarksgildi meðal gildanna í hópi.
- **Hám.** – Þetta fall skilar hámarksgildi af gildunum í hópi.
- **SUM** – Þetta fall skilar summa allra gilda í hópi. Aðeins er hægt að nota þetta með tölureitum.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Staðsetning keyrslu

Þegar **GroupBy** gagnagjafa er breytt og tilgreindur er grunngagnagjafi sem inniheldur færslurnar sem þarf að flokka finnur kerfið sjálfkrafa skilvirkustu [staðsetninguna](#ExecutionLocation) fyrir framkvæmd á **GroupBy** gagnagjafanum. Ef gagnagrunnsgjafinn er [fyrirspurnarhæfur](er-functions-list-filter.md#usage-notes) (þ.e. ef hægt er að keyra hann á gagnagrunnsstigi) er gagnagrunnur forritsins einnig tilgreindur sem staðsetning keyrslu á breytanlegum **GroupBy** gagnagjafa. Annars er minni forritsþjónsins tilgreint sem staðsetning keyrslu.

Hægt er að breyta handvirkt staðsetningu keyrslu sem finnst sjálfkrafa með því að velja þá staðsetninguna sem á við um skilgreindan gagnagjafa. Ef staðsetning keyrslunnar sem valin var á ekki við kemur upp [staðsetningarvilla](er-components-inspections.md#i5) við hönnun.

> [!TIP]
> Mælt er með að nota staðsetningu gagnagrunnsins til að flokka gagnagjafa með mikinn fjölda af færslum.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Minnisnotkun

Ef **GroupBy** gagnagjafi er keyrður í minni er minni forritsþjónsins sjálfgefið notað til að geyma færslur grunngagnagjafnas sem tilheyrir hverjum uppgötvuðum hópi sem færslur í einum hópi. Til að draga úr minnisnotkun er hægt að bæla niður færslugeymslu fyrir **GroupBy** gagnagjafa ef þeir voru skilgreindir til að reikna aðeins út samanlagðar aðgerðir og færslur í hópi þeirra eru ekki notaðar við keyrslu. Til að draga úr minnisnotkun á þennan hátt skal virkja eiginleikann **Draga úr minnisnotkun í rafrænni skýrslugerð þegar færsluflokkun er aðeins notuð til að reikna út uppsafnanir** á vinnusvæðinu **Eiginleikastjórnun**.

## <a name="alternatives"></a><a name="Alternatives"></a>Aðrir valkostir

Hægt er að reikna út svipaðar uppsafnanir með því að nota [aðrar](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) gerðir af gagnagjöfum eða innbyggðum aðgerðum rafrænnar skýrslugerðar.

Til að læra meira um þennan eiginleika skaltu ljúka við dæmið sem fylgir.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Dæmi: Notaðu GROUPBY gagnagjafa fyrir samanlagða útreikninga og færsluflokkun.

Þetta dæmi sýnir hvernig notandi í hlutverki kerfisstjóra eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint vörpun rafrænnar skýrslugerðar sem er með gagnagjafa **GROUPBY** sem er notaður til að reikna út hlaupandi samtölu og flokka færslur. Þessi líkanavörpun er notað til að prenta eftirlitsskýrsluna þegar Intrastat-skattskýrslan er mynduð. Í þeirri skýrslu getur þú farið yfir skráðar Intrastat færslur.

Hægt er að ljúka ferlunum í þessu dæmi í **DEMF**-fyrirtækinu í Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Undirbúa sýnigögn

Gakktu úr skugga um að þú sért með Intrastat-færslur til að tilkynna á síðunni **Intrastat**. Þú verður að vera með færslur fyrir mismunandi flutningskóða vegna þess að færslur verða flokkaðar eftir reitnum **Flutningur** í þessu dæmi.

![Intrastat-færslur á Intrastat-síðunni undirbúnar.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að hanna líkanavörpun rafrænnar skýrslugerðar.

### <a name="import-the-standard-er-format-configuration"></a>Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs

Fylgdu skrefunum í [Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs](er-quick-start2-customize-report.md#ImportERSolution1) til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi tilvik af Dynamics 365 Finance. Flytja inn útgáfu 1 af skilgreiningunni **Intrastat-líkan** úr geymslunni.

### <a name="create-a-custom-data-model-configuration"></a>Stofna sérstillta skilgreiningu gagnalíkans

Fylgdu skrefunum í [Bæta við sérstilltri skilgreiningu gagnalíkans](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) til að bæta handvirkt við nýrri skilgreiningu **Intrastat-líkans (Litware)** fyrir gagnalíkan rafrænnar skýrslugerðar sem er fengin úr innfluttri skilgreiningu **Intrastat-líkans**.

### <a name="configure-a-custom-data-model-component"></a>Skilgreina sérsniðinn gagnalíkansíhlut

Fylgdu þessum skrefum til að gera nauðsynlegar breytingar á afleiddu gagnalíkani **Intrastat-líkans (Litware)** svo hægt sé að nota það til að sýna flutningskóða sem eru með nauðsynlegar upplýsingar.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningartrénu, skal velja **Intrastat-líkan (Litware)**.
3. Veljið **Hönnuður**.
4. Á síðunni **Hönnuður gagnalíkans**, í líkanstrénu, skal velja **Intrastat**.
5. Veldu **Nýtt** til að bæta við nýjum hnút fyrir valda hnútinn **Intrastat**. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **Flutningur**.
    2. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

6. Veldu **Nýr** til að bæta við nýjum földuðum hnút fyrir hnútinn **Flutningur** sem var bætt við. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **Code**.
    2. Í reitnum **Gerð vöru** velurðu **Strengur**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

7. Veldu **Nýtt** til að bæta við öðrum nýjum földuðum hnút fyrir hnútinn **Flutningur**. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **TotalInvoicedAmount**.
    2. Í reitnum **Gerð vöru** velurðu **Rauntala**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

8. Veldu **Nýtt** til að bæta við öðrum nýjum földuðum hnút fyrir hnútinn **Flutningur**. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **NumberOfTransactions**.
    2. Velja **Heiltala** í svæðinu **gerð Vöru**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

9. Veldu **Nýtt** til að bæta við öðrum nýjum földuðum hnút fyrir hnútinn **Flutningur**. Í fellilistaglugga til að bæta við gagnalíkanshnút skal fylgja þessum skrefum:

    1. Í reitinn **Heiti** skal færa inn **Færsla**.
    2. Í reitnum **Gerð vöru** velurðu **Skráalisti**.
    3. Veljið **Bæta við** til að bæta við nýja hnútnum.

10. Fyrir hnútinn **Flutningur** sem var verið að bæta við skal í flýtiflipanum **Hnútur** velja **Skipta um vörutilvísun**.
11. Í svarglugganum **Skipta um vörutilvísun**, í gagnalíkanatrénu, skal velja **CommodityRecord**. Veljið síðan **Í lagi**.

![Skilgreint gagnalíkan í gagnalíkanahönnuði rafrænnar skýrslugerðar.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Ljúka hönnun sérstillts gagnalíkans

Fylgdu skrefunum í [Ljúka hönnun gagnalíkansins](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) til að ljúka við hönnun á afleiddu gagnalíkani **Intrastat-líkans (Litware)**.

### <a name="create-a-new-model-mapping-configuration"></a>Stofna nýja skilgreiningu líkanavörpunar

Fylgdu skrefunum í [Stofna nýja skilgreiningu líkanavörpunar](er-quick-start1-new-solution.md#CreateModelMapping) til að bæta handvirkt við nýrri skilgreiningu **Intrastat-sýnivörpunar** fyrir vörpun rafræns skýrslugerðarlíkans fyrir afleiddar skilgreiningar **Intrastat-líkans (Litware)**.

### <a name="add-a-new-model-mapping-component"></a>Bæta við nýjum þætti líkanavörpunar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í grunnstillingatrénu, skal stækka skilgreininguna **Intrastat-líkan**.
3. Veljið skilgreiningu **Intrastat sýnivörpun**.
4. Veldu **Hönnuður** til að opna lista yfir varpanir.
5. Veldu **Eyða** til að fjarlægja núverandi vörpunarhluta.
6. Veljið **Nýtt** til að bæta við nýjum vörpuníhlut.
7. Í reitnum **Skilgreining** skal velja **Intrastat**.
8. Í reitinn **Heiti** skal færa inn **Intrastat-vörpun**.
9. Veldu **Hönnuður** til að skilgreina nýju vörpunina.

### <a name="design-the-added-model-mapping-component"></a>Hönnun þáttar sem bætti við líkanavörpun

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Bæta við gagnagjafa til að fá aðgang að forritatöflu

Stilla gagnagjafa til að fá aðgang að forritatöflum sem innihalda upplýsingar um Intrastat-færslur.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Dynamics 365 for Operations\\Töflufærslur**.
2. Á svæðinu **Gagnagjafar** skal velja **Bæta við rót** til að bæta við nýjum gagnagjafa sem verður notaður til að opna töfluna **Intrastat**. Hver færsla **Intrastat** -töflunni táknar eina Intrastat-færslu.
3. Í svargluggann **Eiginleikar gagnagjafa**, í reitinn **Heiti**, skal færa inn **Færsla**.
4. Í reitinn **Tafla** skal slá inn **Intrastat**.
5. Veljið **Í lagi** til að bæta við nýja gagnagjafanum.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Bæta við gagnagjafa til að flokka Intrastat-færslur

Skilgreindu **GroupBy** gagnagjafa til að flokka Intrastat-færslur og reikna út samanlagðar aðgerðir.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gerðir gagnagjafa**, skal velja **Virkni\\Flokka eftir**.
2. Á svæðinu **Gagnagjafar** skal velja **Bæta við rót** til að bæta við nýjum gagnagjafa sem verður notaður til að flokka Intrastat-færslur og reikna út samanlagðar aðgerðir.
3. Í svargluggann **Eiginleikar gagnagjafa**, í reitinn **Heiti**, skal færa inn **TransportRecord**.
4. Veldu **Breyta hópi eftir** til að skilgreina flokkunarskilyrðin.
5. Á síðunni **Breyta færibreytum fyrir „Flokka eftir“** skal í gagnagjafalistanum á hægra svæðinu velja gagnagjafann **Flutningur** og stækka hann.
6. Veldu **Bæta reit við \> Hvað á að flokka** til að gefa til kynna að gagnagjafinn **Flutningur** sé valinn sem <a name="BaseDataSource">grunngagnagjafi</a> fyrir skilgreindan **GroupBy** gagnagjafa. Færslur gagnagjafans **Flutningur** verða flokkaðar og reitargildi þessa gagnagjafa verða notuð fyrir útreikninga í samanlögðum aðgerðum.
7. Veldu reitinn **Færsla/flutningur** og veldu síðan **Bæta reit við \> flokkaður reitur** til að gefa til kynna að reiturinn **Flutningur** fyrir grunngagnagjafann sé valinn sem <a name="GroupingFields">flokkunarskilyrði</a> fyrir skilgreinda gagnagjafann **GroupBy**. Með öðrum orðum verða færslur gagnagjafans **Flutningur** flokkaðar út frá gildinu í reitnum **Flutningur**. Hver færsla skilgreinds **GroupBy** gagnagjafa mun standa fyrir einn flutningskóða sem hefur fundist í færslum grunngagnagjafans.
8. Veldu reitinn **Færsla\AmountMST** og fylgdu svo þessum skrefum:

    1. Veldu **Bæta reit við \> samanlagða reiti** til að gefa til kynna að <a name="AggregateFunctions">samanlögð aðgerð</a> verði reiknuð út fyrir þennan reit.
    2. Á svæðinu **Uppsafnanir**, í færslunni sem hefur verið bætt við fyrir valda reitinn **Færsla/AmountMST**, í reitnum **Aðferð**, skal velja aðgerðina **Summa**.
    3. Í valfrjálsa reitnum **Heiti** er valfrjálst að slá inn **TotalInvoicedAmount**.

    Þessar stillingar tilgreina að fyrir hvern flutningsflokk verður heildarupphæð reitsins **Færsla/AmountMST** reiknuð.

9. Veldu reitinn **Færsla\RecId** og fylgdu svo þessum skrefum:

    1. Veldu **Bæta reit við \> samanlagða reiti** til að gefa til kynna að samanlögð aðgerð verði reiknuð út fyrir þennan reit.
    2. Á svæðinu **Uppsafnanir**, í færslunni sem var bætt við fyrir valda reitinn **Færsla/RecId**, í reitnum **Aðferð**, skal velja aðgerðina **Talning**.
    3. Í valfrjálsa reitnum **Heiti** skal slá inn **NumberOfTransactions**.

    Þessar stillingar tilgreina að fyrir hvern flutningsflokk verður færslufjöldinn í flokknum reiknaður.

10. Veldu **Vista**.
11. Farið yfir færibreyturnar <a name="ExecutionLocation">keyrslu</a> fyrir breytanlegan gagnagjafa. Taktu eftir að **Sjálfvirk leit** hefur verið sjálfkrafa valið í reitnum **Staðsetning keyrslu** og reiturinn **Keyrsla á** inniheldur gildið **SQL**. Þessar stillingar tilgreina að hægt sé að spyrjast fyrir um valda grunngagnagjafann **Færsla** og hægt er að keyra breytanlega **GroupBy** gagnagjafann á gagnagrunnsstigi.
12. Opnaðu uppflettinguna fyrir reitinn **Staðsetning keyrslu** til að fara yfir listann yfir tiltæk gildi. Taktu eftir að hægt er að velja **Fyrirspurn** eða **Í minni** til að þvinga þennan **GroupBy** gagnagjafa til að keyra á gagnagrunnsstigi eða í minni forritsþjóns.
13. Veldu **Vista** og lokaðu síðunni **Breyta færibreytusíðu „Flokka eftir“**.
14. Veldu **Í lagi** til að ljúka gagnagjafanum **GroupBy**.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>Tengja GroupBy-gagnagjafa við reiti gagnalíkans

Bindið skilgreinda gagnagjafa við reiti gagnalíkansins til að tilgreina hvernig fyllt verður út í gagnalíkanið með forritsgögnum við keyrslu.

1. Á síðunni **Hönnuður líkanavörpunar**, í rúðunni **Gagnalíkan**, skal stækka hnútinn **Flutningur**.
2. Í rúðunni **Gagnagjafar** skal stækka gagnagjafann **TransportRecord**.
3. Bæta við bindingu til að birta lista yfir uppgötvaða flutningahópa:

    1. Í rúðunni **Gagnalíkan** skal velja **Flutningur**.
    2. Í rúðunni **Gagnagjafar** skal velja atriðið gagnagjafann **TransportRecord**.
    3. Veldu **Binda**.

4. Bæta við bindingu til að birta flutningskóða fyrir uppgötvaða flutningahópa:

    1. Velja gagnalíkansatriðið **Transport.Code**.
    2. Veljið flokkaða reitinn **TransportRecord.grouped.TransportMode**.
    3. Veldu **Binda**.

5. Bæta við bindingu til að birta gildi útreiknaðra uppsöfnunaraðgerða fyrir hvern uppgötvaðan flutningshóp:

    1. Velja gagnalíkansatriðið **Transport.NumberOfTransactions**.
    2. Veldu samanlagða reitinn **TransportRecord.aggregated.NumberOfTransactions**.
    3. Veldu **Binda**.
    4. Velja gagnalíkansatriðið **Transport.TotalInvoicedAmount**.
    5. Veldu samanlagða reitinn **TransportRecord.aggregated.TotalInvoicedAmount**.
    6. Veldu **Binda**.

6. Bæta við bindingu til að birta færsluskrár sem tilheyra hverjum uppgötvuðum flutningshópi:

    1. Velja gagnalíkansatriðið **Transport.Transaction**.
    2. Veljið **TransportRecord.lines** reitinn.
    3. Veldu **Binda**.

    Hægt er að halda áfram að skilgreina bindingar fyrir földuð atriði fyrir **Transport.Transaction** gagnalíkansatriðið og **TransportRecord.lines** gagnagjafareitinn til að sýna við keyrslu upplýsingar um Intrastat-færslur sem tilheyra hverjum uppgötvuðum flutningsflokki.

![Skilgreind líkanavörpun í hönnuði líkanavörpunar rafrænnar skýrslugerðar.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Kemba þáttinn sem bætti við líkanavörpun

Notið [kembiforrit gagnagjafa rafrænnar skýrslugerðar](er-debug-data-sources.md) til að prófa skilgreinda líkanavörpun.

1. Á síðunni **Hönnuður líkanavörpunar** skal velja **Hefja kembingu**.
2. Í síðunni Kemba **gagnagjafa** vinstra megin skal velja **TransportRecord** gagnagjafa og síðan **Lesa allar færslur**.
3. Stækka **TransportRecord** gagnagjafa, og þá fylgja þessum skrefum:

    1. Veljið gagnagjafann **TransportRecord.grouped.TransportMode**.
    2. Veldu **Sækja gildi**.
    3. Velja gagnagjafann **TransportRecord.grouped.NumberOfTransactions**.
    4. Veldu **Sækja gildi**.
    5. Veljið gagnagjafann **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Veldu **Sækja gildi**.

4. Í glugganum hægra megin skal velja **Víkka allt**.

Gagnagjafinn **TransportRecord** sýnir tvær færslur og tvo flutningskóða. Fyrir hvern flutningskóða er reiknaður út fjöldi færslna og reikningsfærð upphæð.

> [!NOTE]
> Aðferðin „Löt mæling“ er notuð þegar kallað er á **GroupBy** gagnagjafann til að fínstilla gagnagrunnskall. Þar af leiðandi eru sum reitargildin í **GroupBy** gagnagjafa aðeins reiknuð út í kembiforriti fyrir gagnagjafa rafrænnar skýrslugerðar þegar þau eru bundin við gagnalíkansreiti.

![Niðurstöður kembingar gagnagjafa á síðunni Kemba gagnagjafa.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Er hægt að reikna út heildartölur alls þegar heild hóps er reiknaður?

Já. Til að reikna lokasamtölur skal skilgreina annan **GroupBy** gagnagjafa þar sem **GroupBy** gagnagjafinn sem var áður skilgreindur er notaður sem grunngagnagjafi. Eftirfarandi mynd sýnir gagnagjafann **Samtölur** af gerðinni **GroupBy** sem er notaður til að reikna út samanlagt aðgerðina **SUMMA** út frá samlagningu **SUMMU** fyrir **TransportRecord** gagnagjafann af gerðinni **GroupBy**.

![Samtölur gagnagjafa í hönnuði sniðsvörpunar rafrænnar skýrslugerðar.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Eftirfarandi mynd sýnir niðurstöður kembingar gagnagjafans **Samtölur**.

![Niðurstöður kembingar samtölugagnagjafa á síðunni Kemba gagnagjafa.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu](er-debug-data-sources.md)
- [Nota gagnagjafa GAGNASÖFNUNAR í rafrænum skýrslugerðarsniðum](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
