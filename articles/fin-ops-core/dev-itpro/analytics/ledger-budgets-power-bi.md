---
title: Raunverulegt samanb. v. fjárhagsáætlun Power BI efni
description: Þetta efnisatriði lýsir raunverulegu á móti fjárhagsáætlun Power BI efni. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkanið.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9cc52f4cdab3084c9ac43078b0b0d534119ab514
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744240"
---
# <a name="actual-vs-budget-power-bi-content"></a>Raunverulegt samanb. v. fjárhagsáætlun Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir **Rauntölur bornar saman við fjárhagsáætlun** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]