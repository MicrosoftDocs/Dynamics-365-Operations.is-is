---
title: Reikna út uppskrift með notkun uppbyggingar með mörgum stigum (febrúar 2016)
description: Þetta ferli sýnir hvernig reikna skal út kostnað fullunninnar vöru með því að nota niðurbrot á mörgum stigum sem er í kostnaðarskjali.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f0ec28a20d32fc38cd6e77a76a02fc9544db3ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430412"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Reikna út uppskrift með notkun uppbyggingar með mörgum stigum (febrúar 2016)

[!include [banner](../../includes/banner.md)]

Þetta ferli sýnir hvernig reikna skal út kostnað fullunninnar vöru með því að nota niðurbrot á mörgum stigum sem er í kostnaðarskjali. Þetta er sjöunda verkið í línunni Útreikningur uppskrifta. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.

1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja vöru BOM_1.  
3. Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.
4. Smellt er á Verð vöru.
5. Smellt er á Reikna vörukostnað.
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.  
6. Í svæði Kostnaðarútgáfa, slá inn eða velja gildi.
    * Velja kostnaðarútgáfa 20, því að áætlaður kostnaður og niðurbrot eru með mörgum stigum.   Niðurbrot á mörgum stigum er fyrir áætlaður kostnaður og hermun. Það er ekki notað fyrir staðalkostnaður.  
7. Smellið á „Í lagi“.
8. Smellt er á Skoða útreikningsupplýsingar.
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.  Í þessu tilfelli skal athuga hvernig BOM_2 hefur verið reiknað út með tilliti til hráefni, vinnsla og sameiginlegur kostnaður með samtals 29,40 í staðinn fyrir staðalkostnaðurinn 10, sem var virkjaður í upprunalega verkefnaleiðbeiningar í þessari línur.  
9. Smellt er á flipann Kostnaðarskjal.
    * Þegar litið er á flipinn Kostnaðarskjal eru samtölur á hvern kostnaðarflokkur ólíkur miðað við útreikningur sem gerður var í fyrri verkefnaleiðbeiningar.  
10. Á svæðinu Stig skal velja „Mörg stig“.
    * Þegar „Mörg stig“ eru valin eru kostnaður flokkaður samkvæmt samsetningu BOM_2, þar sem 10 kemur úr kostnaðarflokkur M1 (ITEM_C) og 15,60 kemur úr framleiðslu þar sem kostnaðarflokkur er L2. Óbeinn kostnaður er einnig mismunandi.  
11. Lokið síðunni.
12. Lokið síðunni.

