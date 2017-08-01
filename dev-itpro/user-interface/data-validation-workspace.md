---
title: "Vinnusvæði gagnaprófunar"
description: "Vinnusvæði gátlista gagnavilluleitar gerir kleift að rekja villuleitarferli gagna milli fyrirtækja, svæða og einstaklinga. Hægt er að nota gátlistann við nýja innleiðingu eftir uppfærslu eða eftir yfirfærslu."
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e105c4b171979a03c20718c1fa9d558c921cd704
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="data-validation-workspace"></a>Vinnusvæði gagnaprófunar

[!include[banner](../includes/banner.md)]


Þetta efni veitir yfirlit yfir **vinnusvæðið Gátlisti gagnavilluleitar** og tengdar skilgreiningar.

## <a name="data-validation-checklist-workspace"></a>Vinnusvæði gátlista gagnaprófunar

**Vinnusvæði gátlista gagnavilluleitar** gerir kleift að rekja villuleitarferli gagna milli fyrirtækja, svæða og einstaklinga. Hægt er að nota gátlistann við nýja innleiðingu eftir uppfærslu eða eftir yfirfærslu. Samkvæmt yfirliti í vinnusvæðinu **Gátlisti gagnavilluleitar** muntu sjá annaðhvort öll verk og stöður fyrir gagnaprófunarverk eða aðeins þau verkefni sem þér er úthlutað.

Fyrst verður að velja gagnaprófunarverk efst í vinnusvæðinu. Öll gögn sem birtast á vinnusvæðinu eru síðan síuð með völdu gagnaprófunarverki.

### <a name="summary-tiles"></a>Samantektarreitir

**Samantektarreitir** veita yfirlit yfir ferlið og vísar hjálpa til við að halda gagnaprófunarferlinu á áætlun. Hægt er að sjá öll eftirstandandi verk, lokin verk, verk í vinnslu og verk sem ekki eru hafin fyrir ferlið. Þessar upplýsingar eru fyrir öll fyrirtæki sem eru tekin með í völdu gagnaprófunarferli.

### <a name="tasks-and-status-section"></a>Hlutinn Verkefni og staða

Í hlutanum **Verkefni og staða** er staða gagnaprófunarverks birt á mismunandi vegu: staða eftir lögaðila, eftir svæðum og eftir verkefnalista. Hægt er að velja síu til að skoða stöðu fyrir tiltekið fyrirtæki. Hver stöðuflipi veitir sundurliðun eftir bæði prósentu sem hefur verið lokið og fjölda verka sem eftir eru.

Síðasti flipinn eru fyrir nákvæman verkefnalista. Listinn sýnir fullan verkefnalista.
Hægt er að sía lista yfir verk með nokkrum aðferðum. Smellt er á **Breyta verkefni** til að breyta stöðu verks eða úthluta verkefni. Smellt er á **Tengingar** til að skoða tengingar við verk.

Heiti verksins er tengill síðu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition-vefsíðu sem notandinn verður að fara á til að ljúka vinnu. Hægt er að setja þennan tengil með því að nota reitinn **Heiti valmyndaratriðis** þegar á að breyta eða stofna verk úr skjámyndinni **Skilgreina gögnum villuleit verks**.

Tengja má skrárnar, athugasemdir, myndir og Vefslóðir við verk með aðgerð **fylgiskjöl** Til dæmis er hægt að hengja við skýrsluskrána sem var prentuð fyrir verk. Tákn birtist í dálknum **Viðhengi** fyrir verkefni ef viðhengi eru til staðar.

Valkosturinn **Svarað** er sjálfkrafa fylltur út þegar verkinu er lokið með nafni starfsmanns sem lauk verkinu. Þegar verkefni er merkt sem lokið er reiturinn **Lokadagsetning** sjálfkrafa uppfært á núgildandi dagsetningu og tíma.

### <a name="configure-data-validation-project-page"></a>Skilgreina síðu gagnaprófunarverks

Áður en hægt er að nota vinnusvæðið **Gátlisti gagnaprófunar** þarf að skilgreina ferlið með því að nota síðuns **Skilgreina gögn villuleitarverks**. (Smellt er á **Vinnusvæði** \> **Gátlisti gagnavilluleitar** \> **Skilgreina gögn villuleitarverks**.)

### <a name="task-areas"></a>Verksvæði

Verksvæði eruð notuð til að flokka gagnaprófunarverk í röklegt svæði eignarhalds innan fyrirtækisins. Til dæmis gætu Viðskiptaskuldir, Viðskiptakröfur eða Fjárhagur verið notuð sem verksvæði.

**Heiti valmyndaratriðis** er tengt við verkframlag vinnu og hægt er að nota það til að fara beint á tengda síðu af verktengli í vinnusvæðinu. T.d. er hægt að tengja gagnaprófunarverk sem á að keyra skýrslur **Aldursgreiningarramma Viðskiptaskulda** við síðuna **Aldursgreiningarskýrsla Viðskiptaskulda**.
