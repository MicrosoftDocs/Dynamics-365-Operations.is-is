---
title: Áætlun kanban-vinnslu fyrir lean-framleiðslu
description: Þessi grein veitir upplýsingar um sjónræna stjórnun á vinnsluröðun kanban-vinnsla og mismunandi leiðir til að raða kanban-vinnslum.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27a82ebb87c76a2c028d02da5389d195614aaa6ab84887ebd1cb4e443b5bda49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778626"
---
# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Áætlun kanban-vinnslu fyrir lean-framleiðslu

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um sjónræna stjórnun á vinnsluröðun kanban-vinnsla og mismunandi leiðir til að raða kanban-vinnslum.  

**kanban-vinnsluröðun** síða gefur sjónrænt eftirlit með vinnuflokkum lean-framleiðslu . Það gefur yfirlit yfir allar kanban-vinnslur og veitir margskonar getu fyrir síun. Úr þessari síðu er hægt að flytja í allar aðrar síður sem tengjast kanban skilgreiningu og framkvæmd.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Sjálfvirk röðun fyrir kanban-vinnslur
Röðun getur verið ræst sjálfkrafa ef þú stillir **Sjálfvirk áætlunarmagn** færibreytu í kanban-reglu. Ef þú stillir **Sjálfvirkt áætlunarmagn** á **1**, er hver kanban-vinnsla áætluð strax og hún er stofnuð. Niðurstaðan eru nokkrar aðgerðir sem byggja á fyrstur sækir, fyrstur fær. Ef sett þú stillir **Sjálfvirkt áætlunarmagn** á gildi sem er meira en 1, eru kanban-vinnslur flokkaðar áður en þær eru áætlaðar. 

Þessi hugmynd gerir mögulegt að minnka stærðir kanban niður fyrir stærðir raunverulega efnahagslega runustærð. Til dæmis, efnahagsleg runustærð fyrir tiltekna vöru (eða vörusafn) er 30. Í stað þess að stofna kanban sem nota afurðarmagnið, 30, er hægt er að stilla kanban-reglu þannig að hann hafi afurðarmagnið 10 og **Sjálfvirkt áætlunarmagn** með gildið **3**. Þó að sjálfvirk áætlun raði kanban-vinnslum fyrir vinnuflokkinn eingöngu  þegar þrjár óvæntar vinnslur eru til staðar, er það fyllilega gagnsætt fyrir þann sem vinnur áætlanir og yfirmanns í vinnusal að tvær óvæntar vinnslur gætu beðið framkvæmdar. Sá sem vinnur áætlun og yfirmaður í vinnusal taka síðan þessar tvær vinnslur inní framleiðslu með því að áætla þær handvirkt eða stofna aukaleg kanbön.

## <a name="manual-scheduling"></a>Handvirkar raðanir
Microsoft Dynamics AX 2012 kynnti kanban-röðunarspjald fyrir handvirka röðun. Handvirk röðun getur verið samþætt sjálfvirkri röðun. Kanban-röðunarspjald gerir það mögulegt að áætla vinnslur og hætta við áætlanir fyrir vinnslur, flytja þær í röð eða flytja þær frá einu tímabili til annars. Vinnslur sem eru byggð á kanban reglu þar sem gildi **Sjálfvirkrar áætlunar** er meira en **0** má handvirkt hætta við áætlun. Hins vegar verða þessar vinnslur enduráætlaðar  þegar næsta tilvik sjálfvirkrar áætlanagerðar kemur upp (það er, þegar nýtt kanban er stofnað). Eftirfarandi valkostir eru tiltækir fyrir handvirka röðun:

-   **Áætlun** raðar valdar vinnslur eftir gjalddaga þeirra. (Valkosturinn svipar til sjálfvirk áætlun.)
-   **Áætla áfram frá dagsetningu** reynir að raða eftir völdum vinnslum í samræmi við gjalddaga þeirra takmarkar niðurstöðurnar með því að nota tilgreinda fyrstu upphafsdagsetningu.
-   **Aftur á bak** flytur valdar vinnslur aftur í röð innan tímabils.
-   **Áfram** flytur valdar áætlaðar vinnslur áfram í röð innan tímabils.
-   **Fyrra tímabil** flytur valdar raðaðar vinnslur í upphaf eða lok fyrra tímabils.
-   **Næsta tímabil** flytur valdar raðaðar vinnslur í upphaf eða lok næsta tímabils.
-   **Áætla** &gt; **Afturkalla vinnslustöðu** gerir það mögulegt að taka úr áætlun raðaða vinnslu.

## <a name="lean-scheduling-groups"></a>Lean-röðunarflokkar
Hver Litur stendur fyrir lean röðunarflokk. Lean röðunarflokkum er hægt skilgreina að vild sem almenna flokka eða flokka sem tilheyra einnum vinnuflokkur. Vörur og víddir er hægt úthluta að vild á röðunarflokka. Til dæmis í málningarhólfi, getur áætlunarflokkur staðið fyrir lit vörunnar. Í vinnu sem er knúin af tilteknum kröfum um verkfæri, gætu vörur verið flokkaðar eftir verkfæraþörf og umbúðavinnuflokkur gæti flokkað vörur eftir umbúðasniðmáti. Notkun lita fyrir lean-röðunarflokka er valfrjáls en mælt er með. Það eykur sýnileika inn í stöðu áætlunarinnar. Til dæmis, er mjög erfitt að sjá hvaða litir eru framleiddir á hvaða degi, og hægt er að sjá í einu vetfangi hvernig er hægt að hagræða þessari vinnu sem best.

## <a name="work-cell-capacity-and-period-capacity"></a>vinnuflokkssgetu og tímabilsgeta
Afkastageta lean-vinnuflokks er alltaf samtíma afkastageta. Með öðrum orðum, margar vinnslur geta verið virk í vinnuflokks á sama tíma. Hægt er að rekja afkastagetu á tvo vegu: gegnumstreymi og tíma.

### <a name="throughput"></a>Afköst

Afköst vinnuflokks ákvarðast af meðalafkastamagni fyrir tilvísunartímabil (staðlaður vinnudagur, viku eða mánuð). Raunveruleg afkastagetu á dag eða viku er síðan reiknaður á grundvelli vinnutíma fyrir dagatal sem er úthlutað á vinnuflokkinn. Afkastageta sem er hlaðin eftir vinnslu er magn vinnslunnar, leiðréttar með afkastahlutfalli vörunnar í vinnuflokki.

### <a name="hours"></a>Vinnustundir

Tiltæk afkastageta eftir degi eða viku ákvarðast af dagatalinu sem er úthlutað á vinnuflokkinn. Afkastageta sem er hlaðin eftir vinnslu er tími ferlis fyrir verkþátt, leiðrétt af magninu (sjálfgefinn verkþáttur miðað við raunverulegt magn vinnslu) og afkastahlutfalli vörunnar í vinnuflokki.

#### <a name="period-capacity-factbox"></a>Upplýsingareitur fyrir Afkastagetu tímabils

**áætlun kanban-vinnslu** listasíðu inniheldur Upplýsingakassa sem sýnir tiltækt og bókað tímabil afkastagetu fyrir valda vinnuflokkinn. Tímabil sýna daga eða vikur, samkvæmt völdum áætlunartímabilum í framleiðsluflæðislíkani.

## <a name="additional-resources"></a>Frekari upplýsingar





[!INCLUDE[footer-include](../../includes/footer-banner.md)]