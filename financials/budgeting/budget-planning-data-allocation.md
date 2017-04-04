---
title: "Úthlutunargögn fjárhagsáætlunargerðar"
description: "Þessi skrá lýsir mismunandi úthlutunaraðferðir sem eru tiltækar í Microsoft Dynamics 365 fyrir Aðgerðirnar og hvernig hægt er að nota þær."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: f717e9de361b5511ac4af360cddb1ea16ad4a1e2
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-data-allocation"></a>Úthlutunargögn fjárhagsáætlunargerðar

Þessi skrá lýsir mismunandi úthlutunaraðferðir sem eru tiltækar í Microsoft Dynamics 365 fyrir Aðgerðirnar og hvernig hægt er að nota þær.  

Hægt er að dreifa gögnum í fjárhagsáætlun á ýmsa vegu til að sýna nákvæmlega áætlaðar upphæðir.

## <a name="allocation-methods"></a>Úthlutunarreglur
Hægt er að nota þrjár úthlutunaraðferðir (Úthlutun yfir mörg tímabil, Úthlutun á víddir og Nota úthlutunarreglur höfuðbókar) til að stofna línur fjárhagsáætlunargerðar sem byggja á línum í sömu fjárhagsáætlunargerð. Þrjár aðrar aðferðir (uppsöfnun, dreifing og afrita úr fjárhagsáætlunargerð) er hægt að nota til að stofna línur fjárhagsáætlunargerðar í öðrum fjárhagsáætlunum. Fyrir allar sex úthlutunaraðferðirnar þarf að tilgreina aðstæður endastaðar. Aðstæður endastaðar geta verið annað hvort sama og upprunaaðstæður eða frábrugðnar upprunaaðstæðum. Þar að auki er hægt að tilgreina hvort nýjum línum er skeytt við fjárhagsáætlunargerðina eða gildandi línum skipt út fyrir nýjar línur í fjárhagsáætlunargerð.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)<ph id="t1">
</ph>**Úthlutun mörg tímabil** – tímabilsúthlutun tegund er notuð til að úthluta fjárhagsáætlunarlínum aðstæður uppruna fjárhagsáætlunargerðarinnar mörg tímabil í aðstæðum áfangastaðar. Upprunaupphæð er úthlutað á margar línur í aðstæðum endastaðar, byggt á prósentu og dagsetningu sem eru skilgreindar í flokknum tímabilsúthlutun.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Úthlutun á víddir** – línum fjárhagsáætlunargerðarinnar er úthlutað úr  upprunalegri fjárhagsáætlunargerð sem ein eða fleiri línur í aðstæðum endastaðar, byggt á prósentu og fjárhagslegum víddum sem eru skilgreind í heiti fjárhagsúthlutunar.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Uppsöfnun** – Línur fjárhagsáætlunar eru lagðar saman úr upprunalegri fjárhagsáætlunargerð í undirfjárhagsáætlun á endastað í yfirfjárhagsáætluninni. Þessi aðferð gerir kleift að sameina á hærra stigi fjárhagsáætlunarupphæðir sem eru teknar saman á neðri stigum í fyrirtækinu.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Dreifing** – Línum fjárhagsáætlunar er dreift úr upprunalegri fjárhagsáætlunargerð í aðalfjárhagsáætluninni yfir í undirfjárhagsáætlunargerðir, byggt á fjárhagsvíddum í skipulagseiningum tengra áætlana. Þessi aðferð gerir kleift að sýna áætlunarupphæðir á lægri stigum í fyrirtækingu sem eru teknar saman á hærri stigum í fyrirtækinu.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Nota úthlutunarreglur fjárhags** – Línum fjárhagsáætlunar er dreift er úr upprunalegri fjárhagsáætlunargerð til endastaðar, byggt á þeirri úthlutunarreglu höfuðbókar sem er valin. úthlutunarreglna höfuðbókar 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Afrita af fjárhagsáætlun** – Eins og í dreifingarúthlutunaraðferð eru línur fjárhagsáætlunargerðar stofnaðar í ákvörðunarstað, byggð á línum í tengdri fjárhagsáætlunargerð. Hins vegar með þessari aðferð, þarf upprunalega fjárhagsáætlunargerðarin ekki að vera aðalfjárhagsáætlun en getur verið á hærra stigi í stigveldi fjárhagsáætlunargerðarinnar. Úthlutunaraðferð þessi er gagnleg ef sameinaðar upphæðir eru upphaflega úr fjárhagsáætlunum á mun efri stigum og þarf að flytja á neðri stig fyrirtækisins til  nákvæmrar yfirferðar og leiðréttingar áður en þær geta fengið samþykki efri stiga.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Að nota úthlutunaraðferðir í fjárhagsáætlunargerð
Til að framkvæma úthlutanir á fjárhagsáætlunarsíðunni skal velja línur til að úthluta og smellið síðan á **Úthlutun fjárhagsáætlunar**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Næst skal velja úthlutun aðferðar. Svæðin sem eftir eru eru síðan stillt samkvæmt aðferðinni sem var valin. Þessi svæði fela meðal annars í sér uppruna og áfangastað fjárhagsáætlunargagna og valkost sem gerir kleift að margfalda uppruna með tilgreindum stuðli þegar upphæðir áfangastaðar eru stofnaðar til að einfalda fjöldaafritunar leiðréttingu. Einnig er hægt að stilla valkostinn **skeyta við áætlun**. Velja **Nei** til að skipta út fyrirliggjandi línum fjárhagsáætlunargerðarinnar, eða veljið **Já** að varðveita fyrirliggjandi línur fjárhagsáætlunargerðar og bæta við nýjum línum fyrir úthlutaðar upphæðir.

## <a name="automating-allocations-during-a-workflow"></a>Að gera sjálfvirkar úthlutanir við verkflæði
Ein öflug aðgerð gerir kleift að framkvæma úthlutanir sjálfkrafa sem hluta af verkflæði fjárhagsáætlunargerðar. Eftir því sem fjárhagsáætlunargerð fer í gegnum sitt verkflæði geta sjálfvirk verk framkallað úthlutun á tilgreindu stigi fjárhagsáætlunargerðar. 

Til að setja upp sjálfvirka úthlutun, verður fyrst að stofna úthlutunaráætlun á síðunni **stillingar fjárhagsáætlunargerðar**. Úthlutunaráætlunin skilgreinir úthlutunaraðferð sem á að nota þegar sjálfvirk úthlutun er keyrð og gildi fyrir mismunandi úthlutunarvalkosti (sjá fyrri hluta varðandi lýsingar). 

Næst er stig úthlutunar stofnað á síðunni **skilgreining fjárhagsáætlunargerðar**. Stig úthlutunar tengir úthlutunaráætlun við verkflæði og stig fjárhagsáætlunargerðar. 

Loks er bætt við sjálfvirku verki fyrir stigsúthlutun fjárhagsáætlunargerðar á æskilegu verkflæðistigi. Í eftirfarandi dæmi hafa tvær stigsúthlutanir fjárhagsáætlunargerðar (rauðmerktar) verið færðar inn í verkflæðið.

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)


