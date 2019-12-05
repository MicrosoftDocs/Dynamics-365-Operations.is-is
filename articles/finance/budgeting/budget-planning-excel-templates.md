---
title: Sniðmát fjárhagsáætlunargerðar fyrir Excel
description: Þetta efnisatriði lýsir hvernig stofna á sniðmát í Microsoft Excel sem hægt er að nota með fjárhagsáætlununum.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 471c719a8e6de0ebe6fcdad0ae222453db841c87
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772100"
---
# <a name="budget-planning-templates-for-excel"></a>Sniðmát fjárhagsáætlunargerðar fyrir Excel

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig stofna á sniðmát í Microsoft Excel sem hægt er að nota með fjárhagsáætlununum.

Þetta efnisatriði sýnir hvernig stofna á sniðmát í Excel sem verða notuð með fjárhagsáætlununum sem nota stöðluð sýnigögn og innskráningu kerfisstjóranotanda. Nánari upplýsingar um fjárhagsáætlunargerð eru í [Yfirlit fjárhagsáætlunargerðar](budget-planning-overview-configuration.md). Einnig er hægt að fylgja sýnidæminu [Fjárhagsáætlunargerð](budget-plan.md) til að læra skilgreiningu og notkunarreglur grunneininda.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Mynda vinnublað með útliti fjárhagsáætlunarskjals

Fjárhagsáætlunarskjal má skoða og breyta með einu eða fleiri útlitum. Hvert útlit getur haft an tengdar fjárhagsáætlunarskjal sniðmát til að skoða og breyta fjárhagsáætlungögnum í Excel vinnublað. Í þessu efnisatriði verður sniðmát fjárhagsáætlunarskjals myndað með fyrirliggjandi útlitsskilgreiningu. 

1. Opnaðu **Fjárhagsáætlunarlista** (**Fjárhagsáætlun** &gt; **Fjárhagsáætlunargerðir**). 
2. Smellt er á **Ný** til að búa til nýtt fjárhagsáætlunarskjal. 

   [![Fjárhagsáætlanalisti](./media/bpt11-1024x552.png)](./media/bpt11.png) 

3. Notaðu **Bæta við** línuaðgerðina til að bæta við línum. Smellt er á **Útlit** til að skoða útlitsskilgreiningu fjárhagsáætlunarskjals. 

   [![Fjárhagsáætlanir bæta við](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Hægt er að yfirfara grunnstillingu útlits og leiðrétta hana eftir þörfum. 
1. Farðu í **Sniðmát** &gt; **Mynda** til að stofna Excel-skrá fyrir þetta útlit. 
2. Eftir að sniðmát er myndað, skal fara í **Sniðmát** &gt; **Skoða** til að opna og yfirfara sniðmát fjárhagsáætlunarskjals. Hægt er að vista Excel-skrána á staðbundnu drifi. 

[![Vista sem](./media/bpt3-1024x545.png)](./media/bpt3.png)

> [!NOTE] 
> Útlit fjárhagsáætlunarskjals getur ekki verið breytt eftir að Excel-sniðmát er tengt því. Til að breyta útlitinu þarf að eyða tengdri skrá Excel-sniðmáts og endurgera það. Þetta er áskilið til að halda svæðum í útliti og vinnublaði samstilltum. 

Excel-sniðmátið mun innihalda allar einingar úr útliti fjárhagsáætlunarskjals, þar sem dálkurinn **Tiltækt í Vinnublað** dálkur er stilltur á rétt. Einingar sem skarast eru ekki leyfðar í Excel-sniðmáti. Til dæmis, ef útlitið inniheldur dálkana Request Q1, Request Q2, Request Q3, og Request Q4, og samtölubeiðnadálk sem sýnir samtölu allra 4 ársfjórðungslegra dálka, er aðeins ársfjórðungslegur dálkur eða samtöludálkur tiltækur til notkunar í Excel-sniðmáti. Excel-skráin getur ekki uppfært dálka sem skarast á meðan uppfærslu stendur, þar sem gögn í töflunni gætu úrelst og orðið ónákvæm.

> [!NOTE] 
> Til að forðast möguleg vandamál við skoðun og breytingar á fjárhagsáætlunargögnum með Excel ætti sami notandi að vera skráður bæði inn í gagnatenglana Microsoft Dynamics 365 Finance og Microsoft Dynamics Office-innbóta.

## <a name="add-a-header-to-budget-plan-document-template"></a>Bæta haus við sniðmát fjárhagsáætlunarskjals.
Til að bæta við upplýsingum úr haus velurðu efstu línuna í Excel-skránni og setur inn auðar línur. Smellið á **Hönnun** í **Gagnatengli** til að bæta við haussvæðum í Excel-skrá.

Í flipanum **Hönnun** er smellt á svæðið **Bæta við** og svo valið **BudgetPlanHeader** sem gagnaveita einingar.

Settu bendilinn á óskaða staðsetningu í Excel-skránni. Smellt er á **Bæta við merki** til að bæta við svæðidmerki á valda staðsetningu. Veldu **Bæta við gildi** til bæta gildissvæði í valinn svæði. Smellið síðan á **Gert** til að loka hönnuði.

## <a name="select-add-valuemediabpt7pngmediabpt7png"></a>[![Velja Bæta við gildi](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Bæta reiknuðum dálki við sniðmátstöflu fjárhagsáætlunarskjals
--------------------------------------------------------------

Næst verður reiknuðum dálki bætt við myndað sniðmát fjárhagsáætlunarskjals. Dálkur með **samtala beiðni**, sem tekur saman dálkana Beiðni Q1: Beiðni Q4 og dálkur **Leiðrétting**, sem endurreiknar dálk **Samtals Beiðni** með fyrirframskilgreindum þætti.

Smellið á **Hönnun** í **Gagnatengli** til að bæta dálkum við í töfluna. Smellt er á **Breyta** við hliðina á **BudgetPlanWorksheet** gagnaveita til að byrja að bæta við dálkur.

[![Byrja að bæta við dálkum](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valinn svæðaflokkur sýnir þá dálka sem eru í boði í sniðmátinu. Smellt er á **Formúla** til að bæta við nýjum dálki við. Nefndu nýja dálkinn og límdu formúluna síðan inn í svæðið **Formúla**. Smellt er á **Uppfæra** til setja dálkinn inn.

[![Bæta við og setja inn dálk](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Til að skilgreina formúluna þarf að stofna formúluna í vinnublaðinu og afrita hana síðan í gluggann **Hönnun**. Bundin tafla í Finance and Operations fær yfirleitt heitið „AXTable1“. Til dæmis, til að draga saman dálkana Request Q1 : Request Q4 í vinnubókinni er formúlan = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].

Endurtaktu þessi skref til að setja inn dálkinn **leiðrétting**. Notaðu formúla = AxTable1\[Samtals beiðni\]\*$I$1 fyrir þennan dálkur. Þetta mun taka gildið í hólfi I1 og margfalda gildin í dálknum **Samtals beiðni** til að reikna út leiðréttingarupphæðir.

Vistaðu og lokaðu Excel-skránni. Í **Útlit** skaltu smella á **Sniðmát &gt; Hlaða upp** til að hlaða upp vistuðu Excel-sniðmáti til að nota fyrir fjárhagsáætlun. 

[![Hlaða upp Excel-sniðmáti](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Lokaðu sleðanum **Útlit**. Í skjalinu **Fjárhagsáætlun** er smellt á **Vinnublað** til að skoða og breyta fylgiskjali í Excel. Athugaðu að leiðrétta Excel-sniðmát var notað til að stofna þetta vinnublað fjárhagsáætlunar og reiknaðir dálkar eru uppfærðir með formúlunum sem voru skilgreindar í fyrra skrefi. 

[![Skoða og breyta skjali í Excel](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Ábendingar og ráð fyrir stofnun sniðmáta fjárhagsáætlunargerðar
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Get ég bætt viðbótargagnaveitum við sniðmát fjárhagsáætlunar?

Já, þú getur notað valmyndina **Hönnun** til að bæta við viðbótareiningum við sama eða önnur vinnublöð í Excel-sniðmáti. Til dæmis er hægt að bæta við gagnaveitunni **BudgetPlanProposedProject** til að stofna og viðhalda lista yfir fyrirhuguð verk um leið og unnið er með gögn fjárhagsáætlunar í Excel. Athugaðu að ef gagnaveita með miklu magni er notuð getur það haft áhrif á afköst Excel-vinnubókar. 

Hægt er að nota valkostinn **Sía** í **Gagnatengi** til að bæta við óskuðum síum í viðbættar gagnaveitur.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Get ég falið valkostinn Hönnun í Gagnatengi fyrir öðrum notendum?

Já, opnaðu valkosti **Gagnatengis** til að fela valkostinn **Hönnun** fyrir öðrum notendum.

[![Opna valkosti gagnatengisins](./media/bpt13-1024x565.png)](./media/bpt13.png)

Stækka **Valkosti gagnatengis** og hreinsa gátreitinn **Kveikja á hönnun**. Þetta mun fela valkostinn **Hönnun** úr **Gagnatengi**.

[![Fela hönnunarvalkost fyrir gagnatengið](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Get ég hindrað notendur í því að loka gagnatenglinum óvart á meðan unnið er með gögn?

Við mælum með því að læsa sniðmátinu til að hindra notendur í að loka því. Til að kveikja á læsingu er smellt á **Gagnatengi**, efst í hægra horninu birtist ör. 

[![Kveikja á læsingunni](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Smellt er á örina fyrir auka valmynd. Veldu **Læsa**.

### <a name="select-lockmediabpt16-1024x614pngmediabpt16png"></a>[![Velja læsingu](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Get ég notað aðra Excel-eiginleika, eins og hólfasnið, liti, skilyrðisbundin snið, og gröf með sniðmátum fjárhagsáætlunar?

Já, flestir hefðbundir Excel-eiginleikar munu virka í sniðmátum fjárhagsáætlunar. Við mælum með því að nota litakóðun fyrir notendur til að gera greinarmun á milli skrifvarinna og breytanlegra dálka. Skilyrðisbundin snið má nota til að auðkenna vandamálasvæði í áætluninni. Dálkasamtölur er auðveldlega hægt að sýna með því að nota hefðbundnar Excel-formúlur fyrir ofan töfluna.

Einnig er hægt að stofna og nota snúningstöflur og myndrit fyrir viðbótarflokkaa og myndbirtingar á fjárhagsáætlunargögnum. Á flipanum **Gögn**, í flokknum **Tengingar**, er smellt á **Endurnýja allt**, og síðan er smellt á **Eiginleikar tengingar**. Smelltu á flipann **Notkun**. Undir **Endurhlaða** velurðu gátreitinn **Endurhlaða gögnum þegar skráin er opnuð**. 



