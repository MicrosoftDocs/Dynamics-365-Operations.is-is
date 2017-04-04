---
title: "Skjöl réttlætingu fjárhagsáætlunargerðar"
description: "Réttlæting skjöl veita narrative á fyrir þær beðið fjárhagsáætlunar til að útskýra hvers vegna tiltekna áætlun er nauðsynlegt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Skjöl réttlætingu fjárhagsáætlunargerðar

Réttlæting skjöl veita narrative á fyrir þær beðið fjárhagsáætlunar til að útskýra hvers vegna tiltekna áætlun er nauðsynlegt. 

Sniðmát fjárhagsáætlunargerðar er stofnuð af áætlun stjórnanda í Microsoft Word og úthlutað gildandi ferli fjárhagsáætlunargerðar. Fjárhagsáætlun eigendum síðan hægt að opna sniðmátið og hafa fyllt út sjálfkrafa í Word gögn á grundvelli þeirra beiðni um fjárhagsáætlun. Þeir hægt að bæta viðbótartexti eða gögn fyrir vistun og tengja þeirra sérsniðinn réttlætingarskjalið þeirra fjárhagsáætlunargerð.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Setja upp Microsoft Dynamics Office innbótinni fyrir Microsoft Word

1.  Opna nýtt Microsoft Word skjal.
2.  Smellið á **Setja** á gerð og á **Verslun**.
3.  Leita að Microsoft Dynamics Office-viðbótar og smella á **Bæta**.
4.  Í Word, í hægri rúðunni er smellt á **Bæta þjónsupplýsingar**.
5.  Gerð eða líma Vefslóð skýrsluþjóns og smelltu á **í lagi**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Skilgreina skal jöfnunarsniðmát í Microsoft Word

1.  Smellið á **Hönnun** í í Microsoft Dynamics Office-viðbótar eftir að þú hefur verið innskráður.
2.  Haus upplýsingar er að nota í **bæta Við svæðum** hnappinn.
3.  Velja gagnagjafa einingar af BudgetPlanJustification, og smella á **Næsta**. **Athugasemd:** Þessi eining er áskilið fyrir allar réttlætingarskjalið. Hægt er að nota aðrar einingar en upphleðslu aftur í Microsoft Dynamics 365 aðgerða gengur ef þessi eining er ekki tekin með.
4.  Bæta BudgetPlanName BudgetPlanPreparer, ResponsibilityCenter og DocumentNumber merki og gildin í Word-skjal. **Athugasemd:** Er hægt að nota eigin sérsniðinnar merki, frekar en stöðluðu merki ef þörf krefur.
5.  Smellið á **Gert** til að ljúka haus hluta.
6.  Stig línuupplýsingar um upphæðir fjárhagsáætlunargerðar, smellið **töfluna Bæta**.
7.  Aftur, veljið gagnagjafa einingar af BudgetPlanJustification og smella á **Næsta**.
8.  Bæta við svæðum fyrir EffectiveDate ScenarioName, AccountDisplayValue og AccountingCurrencyExpenseAmount. **Athugasemd:** Ef athugasemdir eru til staðar til að bæta innan einstakar línur fjárhagsáætlunargerðar þær er hægt að bæta við töflu hér.
9.  Bæta öllum viðbótarleiðbeiningar til að veita notandanum með forskoðunaraðgerðinni og framkvæma nauðsynlegar snið eða styling á skjalinu.
10. Vista þarf skjalið í staðbundnu tölvunni og loka skrána áður en haldið er áfram.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Setja upp ferli Fjárhagsáætlunargerðar sem nota á jöfnunarsniðmát

1.  Í Microsoft Dynamics 365 aðgerða, farið **Fjárhagsáætlun**&gt;**Uppsetningu**&gt;**fjárhagsáætlunargerð**&gt;**skjalasniðmát Réttlætingu**.
2.  Smellið á **Nýtt** og flettið að nýstofnuðu Microsoft Word skjalið.
3.  Færið inn sniðmát birta heiti og lýsingu. Click **OK**.
4.  Fara í **Fjárhagsáætlun**&gt;**Uppsetningu**&gt;**Fjárhagsáætlunar****áætlanagerð**&gt;**Fjárhagsáætlunargerð ferli**.
5.  Veljið ferli þar sem jöfnunarsniðmát sem á að nota og smella á **Breyta**.
6.  Í því **skjal jöfnunarsniðmát**, veljið viðeigandi sniðmát og vista.

##### <a name="edit-and-save-personalized-justification-documents"></a>Breyta og vista sérsniðinn réttlætingu skjöl

1.  Í Dynamics 365 fyrir Aðgerðir, stofna nýja fjárhagsáætlun eða opna fyrirliggjandi fjárhagsáætlunargerð.
2.  Í því **Réttlætingu** fellilista, veljið **Stofna skal nýja jöfnun**.
3.  Eftir að fylla inn í upplýsingar valið til að senda skjalið sérsniðinn úr á **Réttlætingu** fellilista.



