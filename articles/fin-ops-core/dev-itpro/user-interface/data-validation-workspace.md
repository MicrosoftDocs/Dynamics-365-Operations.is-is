---
title: Vinnusvæði gátlista gagnaprófunar
description: Vinnusvæði gátlista gagnavilluleitar gerir kleift að rekja villuleitarferli gagna milli fyrirtækja, svæða og einstaklinga.
author: bking
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DataValidationWorkspace
audience: Application User
ms.reviewer: rhaertle
ms.assetid: ''
ms.search.region: Global
ms.author: bking
ms.openlocfilehash: 4e50d4c94c0b8468a80ad214a21c8f5e0dedae71
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092332"
---
# <a name="data-validation-checklist-workspace"></a>Vinnusvæði gagnaprófunargátlista

[!include [banner](../includes/banner.md)]

Þetta efni veitir yfirlit yfir **vinnusvæðið Gátlisti gagnavilluleitar** og tengdar skilgreiningar.

**Vinnusvæði gátlista gagnavilluleitar** gerir kleift að rekja villuleitarferli gagna milli fyrirtækja, svæða og einstaklinga. Hægt er að nota gátlistann við nýja innleiðingu eftir uppfærslu eða eftir yfirfærslu. Samkvæmt yfirliti í vinnusvæðinu **Gátlisti gagnavilluleitar** muntu sjá annaðhvort öll verk og stöður fyrir gagnaprófunarverk eða aðeins þau verkefni sem þér er úthlutað.

Fyrst verður að velja gagnaprófunarverk efst í vinnusvæðinu. Öll gögn sem birtast á vinnusvæðinu eru síðan síuð með völdu gagnaprófunarverki.

## <a name="summary-tiles"></a>Samantektarreitir

**Samantektarreitir** veita yfirlit yfir ferlið og vísar hjálpa til við að halda gagnavilluleit á áætlun. Hægt er að sjá öll útistandandi verkefni, lokin verk, verk í vinnslu og verk sem ekki hefur verið byrjað á fyrir ferlið. Þessar upplýsingar eru fyrir öll fyrirtæki sem eru tekin með í völdu gagnaprófunarferli.

## <a name="tasks-and-status-section"></a>Hlutinn Verkefni og staða

Í hlutanum **Verkefni og staða** er staða gagnaprófunarverks birt á mismunandi vegu: staða eftir lögaðila, eftir svæðum og eftir verkefnalista. Hægt er að velja síu til að skoða stöðu fyrir tiltekið fyrirtæki. Hver stöðuflipi veitir sundurliðun eftir bæði prósentu sem hefur verið lokið og fjölda verka sem eftir eru.

Síðasti flipinn eru fyrir nákvæman verkefnalista. Listinn sýnir fullan verkefnalista. Hægt er að sía lista yfir verk með nokkrum aðferðum. Smellt er á **Breyta verkefni** til að breyta stöðu verks eða úthluta verkefni. Smellt er á **Tengingar** til að skoða tengingar við verk.

Verkefnið er tengill á síðu sem notandinn verður að fara á til að ljúka vinnunni. Hægt er að setja þennan tengil með því að nota reitinn **Heiti valmyndaratriðis** þegar á að breyta eða stofna verk úr skjámyndinni **Skilgreina gögnum villuleit verks**.

Tengja má skrárnar, athugasemdir, myndir og Vefslóðir við verk með aðgerð **fylgiskjöl** Til dæmis er hægt að hengja við skýrsluskrána sem var prentuð fyrir verk. Tákn birtist í dálknum **Viðhengi** fyrir verkefni ef viðhengi eru til staðar.

Valkosturinn **Svarað** er sjálfkrafa fylltur út þegar verkinu er lokið með nafni starfsmanns sem lauk verkinu. Þegar verkefni er merkt sem lokið er reiturinn **Lokadagsetning** sjálfkrafa uppfært á núgildandi dagsetningu og tíma.

## <a name="configure-data-validation-project-page"></a>Skilgreina síðu gagnaprófunarverks

Áður en hægt er að nota vinnusvæðið **Gátlisti gagnaprófunar** þarf að skilgreina ferlið með því að nota síðuns **Skilgreina gögn villuleitarverks**. (Smellt er á **Vinnusvæði** \> **Gátlisti gagnavilluleitar** \> **Skilgreina gögn villuleitarverks**.)

## <a name="task-areas"></a>Verksvæði

Verksvæði eruð notuð til að flokka gagnaprófunarverk í röklegt svæði eignarhalds innan fyrirtækisins. Til dæmis gætu Viðskiptaskuldir, Viðskiptakröfur eða Fjárhagur verið notuð sem verksvæði.

**Heiti valmyndaratriðis** er tengt við verkframlag vinnu og hægt er að nota það til að fara beint á tengda síðu af verktengli í vinnusvæðinu. T.d. er hægt að tengja gagnaprófunarverk sem á að keyra skýrslur **Aldursgreiningarramma Viðskiptaskulda** við síðuna **Aldursgreiningarskýrsla Viðskiptaskulda**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]