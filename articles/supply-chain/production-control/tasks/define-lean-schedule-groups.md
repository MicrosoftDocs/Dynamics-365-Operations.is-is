---
title: Skilgreina flokka í markvissri áætlanagerð
description: flokkur í markvissri áætlanagerð eru skilgreind til að flokka og greina afurðir í áætlun kanban.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4187381b838825b21a354eeecdf48693d919975b07a881ba32d234135694ad06
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754585"
---
# <a name="define-lean-schedule-groups"></a>Skilgreina flokka í markvissri áætlanagerð

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]