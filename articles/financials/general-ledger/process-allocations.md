---
title: "Vinna úr úthlutunum"
description: "Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og hvernig má nota þá í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb12e24fcb8e8c91f90b91e2fdb3039dd1735ca3
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="process-allocations"></a>Vinna úr úthlutunum

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og hvernig má nota þá í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.

Microsoft Dynamics 365 for Finance and Operations býður upp á eftirfarandi getu til að styðja þetta ferli:

-   Úthluta færsluupphæðum handvirkt með því að nota aðgerðina „Skipta“ í dreifingu fjárhagsupphæðar eða með því að nota sjálfgefin sniðmát fjárhagsvídda við skjal. Frekari upplýsingar eru í [Dreifing á fjárhagsupphæð.](../accounts-payable/accounting-distributions.md)
-   Úthluta sjálfkrafa færsluupphæðum á grundvelli úthlutunarskilmála sem eru tilgreindir á einstökum aðallyklum. Úthlutun lykilfærslna verður mynduð fyrir hverja færslubók á grundvelli hlutfalls og áfangastaðar fjárhagsreikninga hvenær sem bókhaldsfærsla uppfyllir skilyrði sem eru skilgreind sem upprunafjárhagsreikningur.
-   Úthluta sjálfkrafa fjárhagsstöður eða föstum upphæðum samkvæmt úthlutunarreglum fjárhags. Úthlutunarreglur fjárhags eru unnar með úthlutunarbókum með reglulegu millibili. 

###  <a name="allocations-in-budget-planning"></a>Úthlutun í fjárhagsáætlunargerð

Hægt er að nota úthlutunarreglur fjárhags fyrir fjárhagsáætlunargerð. Þegar notaðar eru úthlutunarreglur fjárhags í fjárhagsáætlunargerð virka úthlutunarreglur á sama hátt og þær myndu gera í fjárhag, en upprunagögn og áfangastaður gagna kemur úr fjárhagsáætlunargerð. Hægt er að velja handvirkt úthlutunarreglur fjárhags til að nota fyrir fjárhagsáætlanir. Einnig er hægt að nota úthlutunaráætlun sem keyrir sem hluti af verkflæðisferli.

> [!NOTE]
> Hægt er að nota úthlutunarreglur fjárhags innan samstæðu fyrir fjárhagsáætlunargerð.






