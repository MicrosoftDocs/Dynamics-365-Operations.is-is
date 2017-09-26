---
title: "Rökstuðningsskjöl fjárhagsáætlunargerðar"
description: "Rökstuðningsskjöl veita sögu fyrir þá sem biðja fjárhagsáætlun að útskýra hvers vegna tilgreind fjárhagsáætlun er nauðsynleg."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1d23c0e1725a39d25d2be8971f541b2c31bbe859
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="budget-planning-justification-documents"></a>Rökstuðningsskjöl fjárhagsáætlunargerðar

[!include[banner](../includes/banner.md)]


Rökstuðningsskjöl veita sögu fyrir þá sem biðja fjárhagsáætlun að útskýra hvers vegna tilgreind fjárhagsáætlun er nauðsynleg. 

Sniðmát fjárhagsáætlunargerðar er stofnað af fjárhagsáætlunarstjóra í Microsoft Word og úthlutað til núverandi ferli fjárhagsáætlunargerðar. Eigendur fjárhagsáætlunar getur svo opnað sniðmát og haft gögn sjálfvirkt útfyllt í Word á grunni beiðnar um fjárhagsáætlun. Þeir geta svo bætt við viðbótartexti eða gögn áður en það er vistað og fest sérsniðið jöfnunarfylgiskjal við fjárhagsáætlun.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Setja upp Microsoft Dynamics Office-innbót

1.  Opnaðu nýtt skjal í Microsoft Word.
2.  Smellt er á **Setja inn** á borða, og smellt er á **Verslun**.
3.  Leita fyrir Microsoft Dynamics Office-innbót og Smelltu á **Bæta við**.
4.  Í Word í hægri rúðunni skal smella á **Bæta við upplýsingum um þjón**.
5.  Rita eða líma vefslóð þjóns og Smellt er á **Í lagi**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Skilgreina jöfnunarsniðmát í Microsoft Word

1.  Smellið á **Hönnun** í Microsoft Dynamics Office-innbót eftir að þú hefur skráð þig inn.
2.  Fyrir upplýsingar úr haus Smellið á hnappinn **Bæta við reitum**.
3.  Velurðu eining gagnaveita BudgetPlanJustification, og Smellið á **Áfram**. **athugasemd:** Þessi eining er áskilið fyrir jöfnunarfylgiskjal. Hægt er að nota aðrar einingar en upphleðsla aftur í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition gengur ekki ef þessi eining er ekki notuð.
4.  Bæta við merkjunum og gildunum BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, og DocumentNumber og í Word-skjalið. **athugasemd:** Hægt er að nota sín eigin sérsniðnu merki, frekar en stöðluð merki, ef þess er þörf.
5.  Smelltu á **Lokið** til að ljúka haushlutanum.
6.  Fyrir upplýsingar línustigs um upphæðir fjárhagsáætlunar Smelltu á **Bæta við tafla**.
7.  Aftur velurðu eining gagnaveita BudgetPlanJustification, og Smellið á **Áfram**.
8.  Bæta við reitum fyrir EffectiveDate, ScenarioName, AccountDisplayValue, og AccountingCurrencyExpenseAmount. **athugasemd:** Ef athugasemdir eru í boði til innan stakra fjárhagsáætlunarlína er hægt að bæta þeim við töfluna hér.
9.  Bæta við Auka leiðbeiningar til að veita notanda og framkvæma öll nauðsynleg snið eða stíl á fylgiskjali.
10. Vistaðu skjalið á staðbundinni tölvu og lokaðu skránni áður en haldið er áfram.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Setja upp Ferli fjárhagsáætlunargerðar sem nota á jöfnunarsniðmát

1.  Í Finance and Operations er farið í **Fjárhagsáætlun** &gt; **Uppsetning** &gt; **Fjárhagsáætlunargerð** &gt; **Sniðmát jöfnunarskjala**.
2.  Smellt er á **Nýtt** og flett að nýstofnuðu skjali í Microsoft Word.
3.  Færa skal inn sniðmátsheiti til birtingar og lýsingu. Smellt er á **OK**.
4.  Farðu í **Fjárhagsáætlun** &gt; **Setja upp** &gt; **Fjárhagsáætlunar** **gerð** &gt; **Ferli fjárhagsáætlunargerðar**.
5.  Veldu ferlið þar sem nota á jöfnunarsniðmátið og smelltu á **Breyta**.
6.  Í reitnum **Sniðmát rökstuðningsskjals** velurðu viðeigandi sniðmát og vistar.

##### <a name="edit-and-save-personalized-justification-documents"></a>Breyta og vista sérsniðnum rökstuðningsskjölum

1.  Í Finance and Operations er stofnuð ný fjárhagsáætlun eða fyrirliggjandi fjárhagsáætlun opnuð.
2.  Í fellilistavalmynd **Jöfnun** Velja **Stofna nýjan rökstuðning**.
3.  Eftir útfyllingu upplýsinga, velja að hlaða upp sérsniðnu fylgiskjali æyr fellilistavalmyndinni **Rökstuðningur**.




