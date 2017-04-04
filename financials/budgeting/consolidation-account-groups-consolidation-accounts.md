---
title: "Fleiri samstæðulyklar og flokka samstæðulykla"
description: "Þetta efni veitir upplýsingar um flokka samstæðulykla og viðbótarsamstæðulykla og útskýrir hvernig þær eru notaðar í Microsoft Dynamics 365 aðgerða."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Fleiri samstæðulyklar og flokka samstæðulykla

Þetta efni veitir upplýsingar um flokka samstæðulykla og viðbótarsamstæðulykla og útskýrir hvernig þær eru notaðar í Microsoft Dynamics 365 aðgerða.

<a name="consolidation-account-groups"></a>Flokkar samstæðulykla
----------------------------

Flokka samstæðulykla gera kleift að búa til flokka yfir lykla sem á að nota til að sameina gögn. Oftast er flokk samstæðulykla táknar stjórnvalda krefjast bókhaldslykla eða varpanir á lykla til flokks sem er skilgreindur eftir headquarters fyrirtækisins. Hægt er að finna sameiningu í flokka á **Uppsetningu** svæði í **Sameiningar** kerfiseiningu. Þegar nýr flokkur er bætt við að færa inn einkvæmt kenni fyrir flokk lykil og nafn.

## <a name="additional-consolidation-accounts"></a>Fleiri samstæðulyklar
Fleiri samstæðulyklar hægt er að tengja lykil úr fyrirliggjandi bókhaldslykla í flokk samstæðulykla. Síðan er hægt að tilgreina gildi sameiningu lykli og heiti. 

Hægt er að finna viðbótarsamstæðulykla í á **Uppsetningu** svæði í **Sameiningar** kerfiseiningu. Þegar ný samstæðulykill er stofnað, verður að tilgreina eftirfarandi upplýsingar:

-   **Aðallykill** -Þetta svæði er uppfletting sem sýnir allar aðallykla sem byggja á bókhaldslykli sem valin var á síðunni. Þegar lykill er valinn er nafn fært sjálfvirkt í á **lykilheiti Aðal** svæði.
-   **Flokkur samstæðulykla** -þetta svæði er Notað til að tilgreina lykilinn sem á að úthluta. Ef að sameina á tvo vegu, verður að bæta sama lykil alla flokka samstæðulykla fjórum.
-   **Samstæðulykill** – færa Inn virði á samstæðulyklinum. Þetta gildi er ekki með verður lykil af við bókhaldslykilinn. Það getur verið hvaða gildi sem þarf.
-   **Heiti samstæðulykils** – færið Inn nafn lykils sem óskað er eftir að það birtist á skýrslum og fyrirspurnum.
-   **Stig SAT** – Þetta svæði er notað til að tilkynna skattayfirvöldum Mexíkósk reikningsyfirlit. 

Þegar lokið hefur verið við flokka samstæðulykla og viðbótarsamstæðulykla er hægt að velja flokk í Sameina online.



