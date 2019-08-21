---
title: Vinna úr úthlutunum
description: Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 for Finance and Operations og hvernig nota má þær í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a1946875460e9dfafb481b288a6d6a10ba8931d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846800"
---
# <a name="process-allocations"></a>Vinna úr úthlutunum

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 for Finance and Operations og hvernig nota má þær í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.

Microsoft Dynamics 365 for Finance and Operations býður upp á eftirfarandi getu til að styðja þetta ferli:

-   Úthluta færsluupphæðum handvirkt með því að nota aðgerðina „Skipta“ í dreifingu fjárhagsupphæðar eða með því að nota sjálfgefin sniðmát fjárhagsvídda við skjal. Frekari upplýsingar eru í [Dreifing á fjárhagsupphæð.](../accounts-payable/accounting-distributions.md)
-   Úthluta sjálfkrafa færsluupphæðum á grundvelli úthlutunarskilmála sem eru tilgreindir á einstökum aðallyklum. Úthlutun lykilfærslna verður mynduð fyrir hverja færslubók á grundvelli hlutfalls og áfangastaðar fjárhagsreikninga hvenær sem bókhaldsfærsla uppfyllir skilyrði sem eru skilgreind sem upprunafjárhagsreikningur.
-   Úthluta sjálfkrafa fjárhagsstöður eða föstum upphæðum samkvæmt úthlutunarreglum fjárhags. Úthlutunarreglur fjárhags eru unnar með úthlutunarbókum með reglulegu millibili. 

###  <a name="allocations-in-budget-planning"></a>Úthlutun í fjárhagsáætlunargerð

Hægt er að nota úthlutunarreglur fjárhags fyrir fjárhagsáætlunargerð. Þegar notaðar eru úthlutunarreglur fjárhags í fjárhagsáætlunargerð virka úthlutunarreglur á sama hátt og þær myndu gera í fjárhag, en upprunagögn og áfangastaður gagna kemur úr fjárhagsáætlunargerð. Hægt er að velja handvirkt úthlutunarreglur fjárhags til að nota fyrir fjárhagsáætlanir. Einnig er hægt að nota úthlutunaráætlun sem keyrir sem hluti af verkflæðisferli.

> [!NOTE]
> Hægt er að nota úthlutunarreglur fjárhags innan samstæðu fyrir fjárhagsáætlunargerð.





