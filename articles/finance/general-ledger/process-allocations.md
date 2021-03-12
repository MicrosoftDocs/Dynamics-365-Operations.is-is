---
title: Vinna úr úthlutunum
description: Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra í Microsoft Dynamics 365 Finance og hvernig nota má þær í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.
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
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a715fe2ae0cb32e523248ffb15bdde4b36bd01d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990215"
---
# <a name="process-allocations"></a>Vinna úr úthlutunum

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um úthlutanir, valkosti fyrir vinnslu þeirra og hvernig nota má þær í fjárhagsáætlunargerð. Úthlutanir eru notaðar til að dreifa upphæðum þvert á margar samsetningar fjárhagslykla. Þær auðvelda að tryggja að tekjur eða útgjöld séu innheimtar frá rétta viðfanginu í bókhaldi.

Eftirfarandi getu styður þetta ferli:

-   Úthluta færsluupphæðum handvirkt með því að nota aðgerðina „Skipta“ í dreifingu fjárhagsupphæðar eða með því að nota sjálfgefin sniðmát fjárhagsvídda við skjal. Frekari upplýsingar eru í [Dreifingar á fjárhagsupphæðir](../accounts-payable/accounting-distributions.md).
-   Úthluta sjálfkrafa færsluupphæðum á grundvelli úthlutunarskilmála sem eru tilgreindir á einstökum aðallyklum. Úthlutun lykilfærslna verður mynduð fyrir hverja færslubók á grundvelli hlutfalls og áfangastaðar fjárhagsreikninga hvenær sem bókhaldsfærsla uppfyllir skilyrði sem eru skilgreind sem upprunafjárhagsreikningur. Nánari upplýsingar er að finna í [Úthlutunarskilmálar aðallykils](../general-ledger/main-account-allocation-terms.md)
-   Úthluta sjálfkrafa fjárhagsstöður eða föstum upphæðum samkvæmt úthlutunarreglum fjárhags. Úthlutunarreglur fjárhags eru unnar með úthlutunarbókum með reglulegu millibili. Frekari upplýsingar er að finna í [Úthlutunarreglur](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Úthlutun í fjárhagsáætlunargerð

Hægt er að nota úthlutunarreglur fjárhags fyrir fjárhagsáætlunargerð. Þegar notaðar eru úthlutunarreglur fjárhags í fjárhagsáætlunargerð virka úthlutunarreglur á sama hátt og þær myndu gera í fjárhag, en upprunagögn og áfangastaður gagna kemur úr fjárhagsáætlunargerð. Hægt er að velja handvirkt úthlutunarreglur fjárhags til að nota fyrir fjárhagsáætlanir. Einnig er hægt að nota úthlutunaráætlun sem keyrir sem hluti af verkflæðisferli.

> [!NOTE]
> Hægt er að nota úthlutunarreglur fjárhags innan samstæðu fyrir fjárhagsáætlunargerð.

