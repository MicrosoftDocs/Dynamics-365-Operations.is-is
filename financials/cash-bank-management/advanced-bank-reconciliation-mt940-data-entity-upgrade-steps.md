---
title: "Ítarlegri bankaafstemmingu Innflutningur MT940 – Samsetta gagnaeiningu uppfærslu"
description: "Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: 3a4868045a12f7210a4d3924b4a335a52206341a
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Ítarlegri bankaafstemmingu Innflutningur MT940 – Samsetta gagnaeiningu uppfærslu

Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði. 

Fylgið eftirfarandi skrefum til að bæta einingunni innflutningur bankayfirlits til að styðja MT940 sniði.

1.  Taka saman og samstilla eftirfarandi:
    -   Samsett Eining\\BankStatementImportEntity
    -   Einingar\\BankStatementBalanceEntity
    -   Einingar\\BankStatementDocumentEntity
    -   Eining\\BankStatementEntity
    -   Eining\\BankStatementLineEntity
    -   Töflur\\BankStatementStaging

2.  Stjórnun gagna\\gögn verk.
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
            5.  Smellið á **Já ** til að mynda nýja vörpun.
            6.  Staðfestið að S**equenceNumber** er varpað.
                -   Smellt er á **Skoða kort** á yfirlitseiningunni.
                -   Staðfestið að **SequenceNumber** er varpað úr uppruna í sviðsetningu.

3.  Flytja inn nýtt uppgjör.



