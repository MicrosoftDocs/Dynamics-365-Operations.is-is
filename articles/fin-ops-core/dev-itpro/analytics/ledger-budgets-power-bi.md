---
title: Raunverulegt samanb. v. fjárhagsáætlun Power BI efni
description: Þessi grein lýsir Raunverulegri vs fjárhagsáætlun Power BI efni. Það lýsir einnig hvernig eigi að fara í skýrslur og veitir upplýsingar um gagnalíkanið.
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
ms.openlocfilehash: ff57d052b66103ad716ad8d55afb4fcb095d2c02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847283"
---
# <a name="actual-vs-budget-power-bi-content"></a>Raunverulegt samanb. v. fjárhagsáætlun Power BI efni

[!include [banner](../includes/banner.md)]

Þessi grein lýsir **Raunveruleg vs fjárhagsáætlun** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

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