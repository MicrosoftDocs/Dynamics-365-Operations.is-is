---
title: "Rauntölur bornar saman við fjárhagsáætlun - Power BI-efni"
description: "Þetta efnisatriði lýsir Power BI-efninu Rauntölur bornar saman við fjárhagsáætlun. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: fa0c56f4773b9062d616772e2bca9a576ad37ce2
ms.contentlocale: is-is
ms.lasthandoff: 12/18/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Rauntölur bornar saman við fjárhagsáætlun - Power BI-efni

[!INCLUDE [banner](../includes/banner.md)]

Þetta efnisatriði lýsir Microsoft Power BI-efninu **Rauntölur bornar saman við fjárhagsáætlun**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið. 

## <a name="overview"></a>Yfirlit

Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** var stofnað fyrir einstaklinga sem bera ábyrgð á því að fylgjast með rauntölum bornum saman við áætluð afköst í fyrirtækinu. Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** gefur sýnileika í frávik í fjárhagsáætlun. Hægt er að greina áætlun fyrir gildandi ár eftir tegund lykils, áætlunarkóða, aðallykli, lýsingu aðallykils eða fjárhagstímabili til að öðlast betri skilning á orsökum frávika. 

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Skýrslur úr **Raunverulegt samanb. v. áætlun** Power BI efni eru birtar á vinnusvæðunum **Fjárhagsáætlun og spár** og **CFO vinnusvæði**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni
Eftirfarandi tafla veitir upplýsingar um mælikvarða sem eru á hverri skýrslusíðu í Power BI-efninu **Rauntölur bornar saman við fjárhagsáætlun**.


|           Skýrsla            |                                       Einingar                                        |
|-----------------------------|--------------------------------------------------------------------------------------|
| Útgjöld - rauntölur bornar saman við áætlun |  <ul><li>Heildarkostnaður á þessu ári</li><li>Áætlaður heildarkostnaður á þessu ári</li></ul>  |
| Tekjur - Rauntölur bornar saman við áætlun  |   <ul><li>Heildartekjur á þessu ári</li><li>Áætlaðar heildartekjur á þessu ári</li><ul>    |
|           Útgjöld           | <ul><li>Heildarkostnaður á þessu ári</li><li>Kostnaðarmarkmið eftir áætlun </li><ul> |
|           Tekjur           |  <ul><li>Heildartekjur á þessu ári</li><li>Tekjumarkmið eftir áætlun </li><ul>  |
|         Nettótekjur          |  <ul><li>Nettótekjur á þessu ári</li><li>Nettó tekjumarkmið eftir áætlun </li><ul>  |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

|          Eining           |                                     Innihald                                     |
|---------------------------|----------------------------------------------------------------------------------|
| Fjárhagsaðgerðir |                    Færsluupphæðir fyrir fjárhag                    |
|     Fjárhagsáætlunaraðgerðir     |                   Færsluupphæðir fyrir áætlunarskrá                    |
|       Aðallyklar       |                        Aðallyklar til að sía skýrslur eftir                        |
|     Fjárhagsdagatöl      |                      Fjárhagsdagatöl til að sía skýrslur eftir                       |
|          Fjárhagur          |       Fjárhagur sem hægt er að nota til að sía skýrslu eftir núverandi fjárhag        |
|       Fjárhagsáætlunarkóðar        |                        Fjárhagsáætlunarkóðar til að sía skýrslur eftir                         |
|      Lögaðilar       | Lögaðilar sem hægt er að nota til að sía skýrslur eftir núverandi lögaðila |


