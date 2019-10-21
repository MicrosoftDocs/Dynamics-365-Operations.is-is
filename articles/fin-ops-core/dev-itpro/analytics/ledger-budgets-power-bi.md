---
title: Raunverulegt samanb. v. fjárhagsáætlun Power BI efni
description: Þetta efnisatriði lýsir raunverulegu á móti fjárhagsáætlun Power BI efni. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184394"
---
# <a name="actual-vs-budget-power-bi-content"></a>Raunverulegt samanb. v. fjárhagsáætlun Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir **Raunverulegt vs. fjárhagsáætlun** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Raunverulegt vs. fjárhagsáætlun** Power BI efni var búið til fyrir einstaklinga sem bera ábyrgð á því að fylgjast með raunverulegum afköstum í samanb. við áætluð afköst í fyrirtæki sínu. **Raunverulegt vs. fjárhagsáætlun** Power BI efni veitir innsýn í afbrigði fjárhagsáætlunar. Hægt er að greina áætlun fyrir gildandi ár eftir tegund lykils, áætlunarkóða, aðallykli, lýsingu aðallykils eða fjárhagstímabili til að öðlast betri skilning á orsökum frávika.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
Skýrslur úr **Raunverulegt samanb. v. áætlun** Power BI efni eru birtar á vinnusvæðunum **Fjárhagsáætlun og spár** og **CFO vinnusvæði**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni
Eftirfarandi tafla veitir upplýsingar um einingarnar sem finna má á hverri síðu skýrslunnar í **aðferðastjórnunar** Power BI-efni .

| Skýrsla                      | Einingar                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Útgjöld - rauntölur bornar saman við áætlun | <ul><li>Heildarkostnaður á þessu ári</li><li>Áætlaður heildarkostnaður á þessu ári</li></ul>  |
| Tekjur - Rauntölur bornar saman við áætlun  | <ul><li>Heildartekjur á þessu ári</li><li>Áætlaðar heildartekjur á þessu ári</li><ul>     |
| Útgjöld                     | <ul><li>Heildarkostnaður á þessu ári</li><li>Kostnaðarmarkmið eftir áætlun</li><ul> |
| Tekjur                     | <ul><li>Heildartekjur á þessu ári</li><li>Tekjumarkmið eftir áætlun</li><ul>   |
| Nettótekjur                  | <ul><li>Nettótekjur á þessu ári</li><li>Nettó tekjumarkmið eftir áætlun</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

| Eining                    | Innihald                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Fjárhagsaðgerðir | Færsluupphæðir fyrir fjárhag                                       |
| Fjárhagsáætlunaraðgerðir         | Færsluupphæðir fyrir áætlunarskrá                                      |
| Aðallyklar             | Aðallyklar til að sía skýrslur eftir                                               |
| Fjárhagsdagatöl          | Fjárhagsdagatöl til að sía skýrslur eftir                                            |
| Fjárhagur                   | Fjárhagur sem hægt er að nota til að sía skýrslu eftir núverandi fjárhag              |
| Fjárhagsáætlunarkóðar              | Fjárhagsáætlunarkóðar til að sía skýrslur eftir                                                |
| Lögaðilar            | Lögaðilar sem hægt er að nota til að sía skýrslur eftir núverandi lögaðila |
