---
title: Skilgreina flokka í markvissri áætlanagerð
description: flokkur í markvissri áætlanagerð eru skilgreind til að flokka og greina afurðir í áætlun kanban.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0cb17c68abbc4979a65e33c50450be575df3d93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836265"
---
# <a name="define-lean-schedule-groups"></a>Skilgreina flokka í markvissri áætlanagerð

[!include [task guide banner](../../includes/task-guide-banner.md)]

flokkur í markvissri áætlanagerð eru skilgreind til að flokka og greina afurðir í áætlun kanban. Hægt er að gera flokkunina sem almennan tengingu fyrir hvert fyrirtæki eða við vinnuflokkur. Hver flokkur hefur litakóði sem úthlutað er fyrir sjónræn lýsing á lístasíðum kanban-röðunar. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="define-lean-scheduling-group"></a>Skilgreina flokkur í markvissri áætlanagerð
1. Fara í Afurðaupplýsingastjórnun > Lean-framleiðsla > Lean-áætlunarflokkar.
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðinu áætlunarflokkur.
    * Áætlunarflokkur getur verið skilgreind sem altæka flokka eða við vinnuflokks. Í þessu dæmi skilgreina altæka flokka og vinnuflokkurinn er haldið eftir autt. Stillingar fyrir þennan flokk eiga við allar vinnuflokkana sem ekki hafa flokka tiltekna áætlunarflokk.  
4. Veljið lit úr valinu lit.
    * Litir eru notaðir til að auðkenna störf á listasíðu áætlunar fyrir kanban eða spjald kanban ferlis.  
5. Í listanum skal merkja valda línu.
6. Í listanum skal smella á tengilinn í valinni línu.

## <a name="associate-product"></a>Tengja afurð
1. Tengja tiltekna afurð
    * Til eru tvær leiðir til að tengja afurðir við flokkur í markvissri áætlanagerð, annaðhvort sem tiltekinni vöru (venslagerð Vöru = Vöru) eða sem hluta af úthlutunarlykil vöru (venslagerð vöru= flokk).    
2. velja Vöru í Venslagerðarsvæði Vöru
3. Í reitnum Vörunúmer skal slá inn gildi.
4. Í reitinn afkastageta skal slá inn númer.
    * Sjálfgefin afkastahlutfall er 1, sem þýðir að tengdar afurðir nota nákvæmlega afköst tilgreind í vinnsluaðgerðum framleiðsluflæðis. Afkastahlutfall > 1 tilgreinir hærri tilfanganotkun, afkastahlutfall < 1 tilgreinir lægri notkun tilfanga. Hlutfallið er notað í útreikningi kanban-vinnslunotkun og í útreikningi kostnaðar.  

## <a name="associate-item-allocation-key"></a>Úthluta úthlutunarlykil vöru
1. Tengja úthlutunarlykil vöru
    * Bæta tengingu við úthlutunarlykil vöru með því að nota hópagerð vöruvensla.   Athugið að fyrir þetta ferli þarf að spár úthlutunarlykli vöru skilgreindum í gögnin þín.  
2. Velja flokk í Venslagerðarsvæði Vöru
3. Í reitnum úthlutunarlykill vöru skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.

