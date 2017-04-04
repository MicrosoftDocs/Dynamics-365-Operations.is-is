---
title: "Sniðmát fjárhagsáætlunargerðar fyrir Excel"
description: "Þetta efnisatriði lýsir hvernig á að stofna Microsoft Excel sniðmát sem hægt er að nota fjárhagsáætlanir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Sniðmát fjárhagsáætlunargerðar fyrir Excel

Þetta efnisatriði lýsir hvernig á að stofna Microsoft Excel sniðmát sem hægt er að nota fjárhagsáætlanir.

Þetta efnisatriði sýnir hvernig á að stofna sniðmát Excel sem notuð verður við með því að nota staðlaða sýnigögn gagnasafninu og innskráningu notanda Stjórnun fjárhagsáætlunargerðum. Sjá frekari upplýsingar um fjárhagsáætlunargerð [yfirlit Fjárhagsáætlunargerðar.](budget-planning-overview-configuration.md) Einnig er hægt að fylgja í [101 á Fjárhagsáætlunargerð](budget-plan.md) kennsluefni til að fræðast um skilgreiningu og notkun reglum kerfiseiningunni grunnur.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Búa til vinnublað með skjal fjárhagsáætlunarútlit
Skjöl fjárhagsáætlunargerðar geta skoðað og breytt með því að nota eina eða fleiri útlit. Hver útlit getur haft á tengt skjal sniðmáts fjárhagsáætlunargerðar til að skoða og breyta fjárhagsáætlunargögn áætlun í excel-vinnublað. Í þessu efnisatriði skjal sniðmáti fjárhagsáætlunargerðar mynduð með því að nota afbrigði útlit. Opna skal **lista yfir fjárhagsáætlunargerðir** (**Fjárhagsáætlun**&gt;**fjárhagsáætlunargerðir**). Smellið á **Nýtt** til að stofna nýtt skjal fjárhagsáætlunargerðar. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Nota skal **Bæta** línu valkost til að bæta við línum. Smellið á **Útlit** til að skoða skilgreiningu útlit fyrir skjalið í áætlun. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Hægt er að yfirfara skilgreiningu útlit og leiðrétta hana eftir þörfum. Fara í **Sniðmát**&gt;**Mynda** til að stofna excel-skráin fyrir þetta útlit. Eftir að sniðmát er mynduð fara **Sniðmát**&gt;**Skoða** til að opna og fara yfir sniðmát skjals áætlunarinnar. Hægt er að vista excel-skrá á staðbundnu drifið. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Ekki hægt að breyta skjalinu fjárhagsáætlunarútlit eftir Excel sniðmát er tengd við hana. Til að breyta útliti, eyða skrá tengda Excel sniðmát og endurgera hana. Þetta er nauðsynlegt til að halda svæði í útliti og vinnublaðið samstillt. 

Excel-sniðmát innihalda allar einingar úr skjal fjárhagsáætlunarútlit, þar sem er **Tiltækt í Vinnublaðinu** dálkurinn er stillt á Satt. Einingar sem skarast leyfast ekki í Excel-sniðmát. Til dæmis ef útlit inniheldur Beiðni Q1 Beiðni 2. árfsjórðungi, Beiðni 3. árfsjórðungi, og 4. árfsjórðungi Beiðni dálka og heildarupphæð beiðni dálkinn sem stendur samtölu allra 4 ársfjórðungslega dálka er aðeins ársfjórðungslega dálka eða samtöludálk er tiltæk á að nota í Excel-sniðmát. Excel-skráin hægt að uppfæra dálka skarast við uppfærslu þar sem gögn í töflunni gæti orðið útrunnin og rangar.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Til að koma í veg fyrir hugsanlega vandamál við að skoða og breyta með því að nota Excel gögn fjárhagsáætlunar, sami notandi skuli vera skráður inn í bæði Dynamics 365 Aðgerða og Gagnatengi Microsoft Dynamics Office-viðbótar.

## <a name="add-a-header-to-budget-plan-document-template"></a>Bæta haus skjals sniðmáts fjárhagsáætlunargerðar
Bæta upplýsingum í haus, veljið efstu línu í Excel-skrár og setja auðar línur. Smellið á **Hönnun** í í **Gagnatengi** til að bæta fyrirsagnasvæði excel-skrá.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Í í **Hönnun** flipann ** ** smellið **Bæta** svæði og velja svo **BudgetPlanHeader** sem einingin gagnagjafi.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Punktur bendilinn í æskilega staðsetningu í excel-skrá. Smellið á **Bæta merki** til að bæta svæða merki valda staðsetningu. Velja **Bæta Gildi** til að bæta gildissvæðið á völdum stað. Smellið á **Gert** til að loka hönnuðurinn.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Bæta reiknaður dálkur fjárhagsáætlunar tafla sniðmáts fjárhagsáætlunargerðar
--------------------------------------------------------------

Næsta, reiknað dálkum bætt við myndaða skjalinu sniðmáts fjárhagsáætlunargerðar. A **Heildarupphæð beiðni** dálk sem sýnir Q1 Beiðni: Beiðni 4. árfsjórðungi dálka, og **Leiðrétting** dálk sem endurreiknar á **Heildarupphæð Beiðni** dálkinn með stuðli fyrirfram.

Smellið á **Hönnun** í á **gagnatengi** til að bæta dálkum í töflunni. Smellið á **Breyta** hliðina á **BudgetPlanWorksheet** gagnagjafa til að byrja að bæta dálkum.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valda svæðaflokkur birtir dálka sem eru tiltækar í sniðmátinu. Smellið á **Formúlu** til að bæta nýjum dálki. Heiti nýjum dálki og líma niðurstöðurnar inn formúluna sem **Formúlu** svæði. Smellið á **Uppfærslu** til að setja inn í dálkinn.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Stofna formúluna í excel-töflunni til að skilgreina formúla, og afritið hana svo á **Hönnun** glugga. Dynamics 365 fyrir bundna töflu Aðgerðir verður yfirleitt að vera með heitið "AXTable1". Til dæmis til að biðja Um Q1 draga saman: beiðni Um á 4. árfsjórðungi dálka í töflureikni formúlunnar = AxTable1\[Beiðni Q1\]+ AxTable1\[Krefjast á 2. árfsjórðungi\]+ AxTable1\[Krefjast á 3. árfsjórðungi\]+ AxTable1\[Krefjast á 4. árfsjórðungi\].

Endurtakið þessi skref til að setja í **Leiðrétting** dálk. Nota formúluna = AxTable1\[Heildarupphæð beiðni\]\*$I$ 1 fyrir þennan dálk. Þetta mun taka gildi í hólfi I1 og margfalda gildin í á **Heildarupphæð beiðni** dálk til að reikna leiðréttingarupphæðir.

Vista og loka excel-skrá. Snúa aftur í Dynamics 365 Aðgerðum og í **Útlit**, smellið á **Sniðmát &gt;Senda** til að hlaða upp vistaða Excel sniðmátið sem nota á fyrir fjárhagsáætlunargerð. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Loka skal **Útlit** sleði. Í **fjárhagsáætlunargerð** skjals er smellt á **Vinnublað** til að skoða og breyta skjali í Excel. Athugið að leiðrétt Excel sniðmátið sem var notað til að stofna þessi vinnublaði fjárhagsáætlunargerðar og reiknaðra dálka eru uppfærðar með því að nota formúlur sem skilgreindar voru í fyrra þrep. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Ábendingar & tricks til að stofna sniðmát fjárhagsáætlunargerðar
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Hægt I bæta og aðrir gagnagjafar sniðmáts fjárhagsáætlunargerðar til að nota?

Já, er hægt að nota í **Hönnun** valmynd til að bæta fleiri einingar sama eða öðrum svarblöð í Excel-sniðmát. Til dæmis er hægt að bæta við **BudgetPlanProposedProject** gagnagjafa til að stofna og viðhalda lista yfir tillagt verk á sama tíma þegar vinna með áætlun áætlun gögn í Excel. Athugið að meðtöldum há rúmmál gagnagjafa gætu áhrif á afköst excel-vinnubók. 

Hægt er að nota í **Síu** í í **Gagnatengi** til að bæta viðeigandi síur viðbótar gagnagjafa.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Hægt I fela valkostinn Hönnun í connector Gögn fyrir aðra notendur?

Opna já, er **Gagnatengi** valkosti til að fela í **Hönnun** kost af öðrum notendum.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Útvíkka **Gögn connector valkosti** og hreinsa í **Virkja hönnun** gátreitinn. Þetta verður að fela í **Hönnun** valkosturinn úr á **gagnatengi**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Hægt I veg fyrir að notendur accidently lokun gagnatengi á meðan unnið með gögn?

Mælt er með læsingu sniðmát til að koma í veg fyrir að notendur úr henni er lokað. Smellið til að kveikja læsingu á **gagnatengi**, í hægra horninu efst ör birtist. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Smella á örina til viðbótar valmynd. Velja **Læsa**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Hægt ég nota aðra Excel aðgerðir, eins og hólf snið, litum, skilyrtar snið og gröf með mínar sniðmát fjárhagsáætlunargerðar?

Já, flestum staðlaða Excel getu virkar í sniðmát fjárhagsáætlunargerðar. Mælt er með því að nota color-coding fyrir notendur til að aðgreina á milli dálka skrifvarin og hægt að breyta. Skilyrt snið má nota til að auðkenna koma auga svæðum áætlunarinnar. Dálkur samtölur geta auðveldlega fram með því að nota staðlaða Excel formúlur yfir í töflu.

Einnig er hægt að stofna og nota veltitöfluskýrslum og gröf á frekari flokkun og sjóngervingum fjárhagsáætlunargögn. Á við **Gögn** flipanum, á **Tengingar** flokk er smellt á **Endurnýja Alla**, og smellið síðan á **Tengingu Eiginleika**. Smellið á **Notkun** flipa. Undir **Endurnýja**, veljið þá **Endurnýja gögn við opnun skráar** gátreitinn. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


