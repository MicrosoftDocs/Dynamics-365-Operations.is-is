---
title: "Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar"
description: "Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 672697254c1bf06e193a51c5c7c83c467a220ce8
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar

[!include[banner](../includes/banner.md)]


Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði. 

Fylgið eftirfarandi skrefum til að bæta einingunni innflutningur bankayfirlits til að styðja MT940 sniði.

1.  Taka saman og samstilla eftirfarandi:
    -   Samsett eining\\BankStatementImportEntity
    -   Eining\\BankStatementBalanceEntity
    -   Eining\\BankStatementDocumentEntity
    -   Eining\\BankStatementEntity
    -   Entity\\BankStatementLineEntity
    -   Töfbles\\BankStatementStaging

2.  Gagnastjórnun\\gagnaverk.
    1.  Hlaða MT940 innflutningsverk
        1.  Breyta XSLT.
            -   Smellið á **Skoða kort**.
            -   Smellt er á **Skoða kort** á skjal bankayfirlits.
            -   Smelltu á **Umbreytingar**
            -   Eyða skrá BankReconiliation-to-Composite.xslt.
            -   Bætið nýja útgáfu af BankReconiliation-to-Composite.xsl.

        2.  Sýna **Raðnúmer** á **Upprunagögn** útlit.
            1.  Snið upprunagagna = XML-Element.
            2.  Nafn einingar = bankayfirlit.
            3.  Hlaða upp gagnaskrá = ný útgáfa SampleBankCompositeEntity.xml.
            4.  Smellið á **„Já“** til að skrifa yfir núgildandi skrá.
            5.  Smellið á **Já** til að mynda nýja vörpun.
            6.  Staðfestið að S**equenceNumber** er varpað.
                -   Smellt er á **Skoða kort** á yfirlitseiningunni.
                -   Staðfestið að **SequenceNumber** er varpað úr uppruna í sviðsetningu.

3.  Flytja inn nýtt uppgjör.




