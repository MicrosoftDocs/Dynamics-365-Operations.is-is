---
title: "Rauntölur bornar saman við fjárhagsáætlun - Power BI-efni"
description: "Þetta efnisatriði lýsir Power BI-efninu Rauntölur bornar saman við fjárhagsáætlun. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem voru notaðar til að búa til efnið."
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: is-is
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Rauntölur bornar saman við fjárhagsáætlun - Power BI-efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir Microsoft Power BI-efninu **Rauntölur bornar saman við fjárhagsáætlun**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið. 

# <a name="overview"></a>Yfirlit

Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** var stofnað fyrir einstaklinga sem bera ábyrgð á því að fylgjast með rauntölum bornum saman við áætluð afköst í fyrirtækinu. Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** gefur sýnileika í frávik í fjárhagsáætlun. Hægt er að greina áætlun fyrir gildandi ár eftir tegund lykils, áætlunarkóða, aðallykli, lýsingu aðallykils eða fjárhagstímabili til að öðlast betri skilning á orsökum frávika. 

# <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Skýrslur úr **Raunverulegt samanb. v. áætlun** Power BI efni eru birtar á vinnusvæðunum **Fjárhagsáætlun og spár** og **CFO vinnusvæði**.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðir með í Power BI-efni
Eftirfarandi tafla veitir upplýsingar um mælikvarða sem eru á hverri skýrslusíðu í Power BI-efninu **Rauntölur bornar saman við fjárhagsáætlun**.

| Skýrsla                      | Einingar |
|-----------------------------|---------|
| Útgjöld - rauntölur bornar saman við áætlun | <ul><li>Heildarkostnaður á þessu ári</li><li>Áætlaður heildarkostnaður á þessu ári</li></ul> |
| Tekjur - Rauntölur bornar saman við áætlun  | <ul><li>Heildartekjur á þessu ári</li><li>Áætlaðar heildartekjur á þessu ári</li><ul> |
| Útgjöld                     | <ul><li>Heildarkostnaður á þessu ári</li><li>Kostnaðarmarkmið eftir áætlun </li><ul> |
| Tekjur                     | <ul><li>Heildartekjur á þessu ári</li><li>Tekjumarkmið eftir áætlun </li><ul> |
| Nettótekjur                  | <ul><li>Nettótekjur á þessu ári</li><li>Nettó tekjumarkmið eftir áætlun </li><ul> |

## <a name="extending-the-power-bi-content"></a>Stækkun efnis Power BI
Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Microsoft Dynamics 365 öflugri greiningu. Hægt er að breyta þessum þjónustupökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com þjónustupakkana. 

Hægt er að finna Power BI-efnið **Rauntölur bornar saman við fjárhagsáætlun** í safninu Samnýttar eignir í LCS. Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

# <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar

| Eining                    | Innihald |
|---------------------------|----------|
| Fjárhagsaðgerðir | Færsluupphæðir fyrir fjárhag |
| Fjárhagsáætlunaraðgerðir         | Færsluupphæðir fyrir áætlunarskrá |
| Aðallyklar             | Aðallyklar til að sía skýrslur eftir |
| Fjárhagsdagatöl          | Fjárhagsdagatöl til að sía skýrslur eftir |
| Fjárhagur                   | Fjárhagur sem hægt er að nota til að sía skýrslu eftir núverandi fjárhag |
| Fjárhagsáætlunarkóðar              | Fjárhagsáætlunarkóðar til að sía skýrslur eftir |
| Lögaðilar            | Lögaðilar sem hægt er að nota til að sía skýrslur eftir núverandi lögaðila |

