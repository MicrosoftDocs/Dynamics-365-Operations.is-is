---
title: "Kanban-vinnslu röðun fyrir lean manufacturing"
description: "Þessi grein veitir upplýsingar um sjónræna stjórnun á vinnsluröðun kanban-vinnsla og mismunandi leiðir til að raða kanban-vinnslum."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 02 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 062cbbc8a4fd3b4dc738f24ee0606a3741736377
ms.lasthandoff: 03/29/2017


---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban-vinnslu röðun fyrir lean manufacturing

Þessi grein veitir upplýsingar um sjónræna stjórnun á vinnsluröðun kanban-vinnsla og mismunandi leiðir til að raða kanban-vinnslum.  

**kanban-vinnsluröðun** síða gefur sjónrænt eftirlit með vinnuflokkum lean-framleiðslu . Það gefur yfirlit yfir allar kanban-vinnslur og veitir margskonar getu fyrir síun. Úr þessari síðu er hægt að flytja í allar aðrar síður sem tengjast kanban skilgreiningu og framkvæmd.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Sjálfvirk röðun fyrir kanban-vinnslur
Röðun getur ræstar sjálfkrafa ef það **Sjálfvirk áætlun magns** færibreyta í kanban-reglu. Ef sett **Sjálfvirk áætlun magns** að **1**, hver kanban-vinnslan er áætluð strax þegar hún er stofnuð. Niðurstaðan eru nokkrar aðgerðir sem byggja á fyrstur sækir, fyrstur fær. Ef sett þú stillir **Sjálfvirkt áætlunarmagn** á gildi sem er meira en 1, eru kanban-vinnslur flokkaðar áður en þær eru áætlaðar. Þessi hugmynd gerir mögulegt að minnka stærðir kanban niður fyrir stærðir raunverulega efnahagslega runustærð. Til dæmis er efnahagslegt runustærð fyrir tiltekna vöru (eða vörusafn) 30. Í stað þess að stofna kanban sem nota afurðarmagnið, 30, hægt er að stilla kanban-reglu þannig að hann hafi afurðarmagnið 10 og ** Sjálfvirk áætlun magns ** gildi **3**. Þó að sjálfvirk áætlun raði kanban-vinnslum fyrir vinnuflokkinn eingöngu  þegar þrjár óvæntar vinnslur eru til staðar, er það fyllilega gagnsætt fyrir þann sem vinnur áætlanir og yfirmanns í vinnusal að tvær óvæntar vinnslur gætu beðið framkvæmdar. Sá sem vinnur áætlun og yfirmaður í vinnusal taka síðan þessar tvær vinnslur inní framleiðslu með því að áætla þær handvirkt eða stofna aukaleg kanbön.

## <a name="manual-scheduling"></a>Handvirkar raðanir
Microsoft Dynamics AX 2012 kynnti kanban-röðunarspjald fyrir handvirka röðun. Handvirk röðun getur verið samþætt sjálfvirkri röðun. Kanban-röðunarspjald gerir það mögulegt að áætla vinnslur og hætta við áætlanir fyrir vinnslur, flytja þær í röð eða flytja þær frá einu tímabili til annars. Vinnslur sem eru byggð á kanban reglu þar sem gildi **Sjálfvirkrar áætlunar** er meira en **0** má handvirkt hætta við áætlun. Hins vegar verða þessar vinnslur enduráætlaðar  þegar næsta tilvik sjálfvirkrar áætlanagerðar kemur upp (það er, þegar nýtt kanban er stofnað). Eftirfarandi valkostir eru tiltækir fyrir handvirka röðun:

-   **Áætlun** raðar valdar vinnslur eftir gjalddaga þeirra. (Valkosturinn svipar til sjálfvirk áætlun.)
-   **Áætla áfram frá dagsetningu** reynir að raða eftir völdum vinnslum í samræmi við gjalddaga þeirra takmarkar niðurstöðurnar með því að nota tilgreinda fyrstu upphafsdagsetningu.
-   **Aftur á bak** flytur valdar vinnslur aftur í röð innan tímabils.
-   **Áfram ** flytur valdar áætlaðar vinnslur áfram í röð innan tímabils.
-   **Fyrra tímabil** flytur valdar raðaðar vinnslur í upphaf eða lok fyrra tímabils.
-   **Næsta tímabil** flytur valdar raðaðar vinnslur í upphaf eða lok næsta tímabils.
-   **Áætla**&gt;**Afturkalla vinnslustöðu** gerir það mögulegt að unschedule tímasettri vinnslu.

## <a name="lean-scheduling-groups"></a>Lean-röðunarflokkar
Hver Litur stendur fyrir lean röðunarflokk. Lean röðunarflokkum er hægt skilgreina að vild sem almenna flokka eða flokka sem tilheyra einnum vinnuflokkur. Vörur og víddir er hægt úthluta að vild á röðunarflokka. Til dæmis í málningarhólfi, getur áætlunarflokkur staðið fyrir lit vörunnar. Í vinnu sem er knúin af tilteknum kröfum um verkfæri, gætu vörur verið flokkaðar eftir verkfæraþörf og umbúðavinnuflokkur gæti flokkað vörur eftir umbúðasniðmáti. Notkun lita fyrir lean-röðunarflokka er valfrjáls en mælt er með. Það eykur sýnileika inn í stöðu áætlunarinnar. Til dæmis, er mjög erfitt að sjá hvaða liti sem eru framleiddar á hvaða degi og hægt er að sjá í fyrirtækjasamstæðunni hvernig bestuð getur þessari vinnustöð.

## <a name="work-cell-capacity-and-period-capacity"></a>vinnuflokkssgetu og tímabilsgeta
Afkastageta lean-vinnuflokks er alltaf samtíma afkastageta. Með öðrum orðum, margar vinnslur geta verið virk í vinnuflokks á sama tíma. Hægt er að rekja afkastagetu á tvo vegu: gegnumstreymi og tíma.

### <a name="throughput"></a>Afköst

Afköst vinnuflokks ákvarðast af meðalafkastamagni fyrir tilvísunartímabil (staðlaður vinnudagur, viku eða mánuð). Raunveruleg afkastagetu á dag eða viku er síðan reiknaður á grundvelli vinnutíma fyrir dagatal sem er úthlutað á vinnuflokkinn. Afkastageta sem er hlaðin eftir vinnslu er magn vinnslunnar, leiðréttar með afkastahlutfalli vörunnar í vinnuflokki.

### <a name="hours"></a>Vinnustundir

Tiltæk afkastageta eftir degi eða viku ákvarðast af dagatalinu sem er úthlutað á vinnuflokkinn. Afkastageta sem er hlaðin eftir vinnslu er tími ferlis fyrir verkþátt, leiðrétt af magninu (sjálfgefinn verkþáttur miðað við raunverulegt magn vinnslu) og afkastahlutfalli vörunnar í vinnuflokki.

#### <a name="period-capacity-factbox"></a>Upplýsingareitur fyrir Afkastagetu tímabils

**áætlun kanban-vinnslu** listasíðu inniheldur Upplýsingakassa sem sýnir tiltækt og bókað tímabil afkastagetu fyrir valda vinnuflokkinn. Tímabil sýna daga eða vikur, samkvæmt völdum áætlunartímabilum í framleiðsluflæðislíkani.

<a name="see-also"></a>Sjá einnig
--------


