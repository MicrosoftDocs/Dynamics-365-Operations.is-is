---
title: Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar
description: Raðnúmeri þarf að bæta við einingunni innflutningur bankayfirlits til að styðja MT940 sniði.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c891a5139ff7de85e6762513f57236e24f1644529d7825c9ce5e1dfda50fbad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739384"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Innflutningur ítarlegrar bankaafstemmingar MT940 – Uppfærsla samsettrar gagnaeiningar

[!include [banner](../includes/banner.md)]

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
            6.  Staðfestið að S **equenceNumber** er varpað.
                -   Smellt er á **Skoða kort** á yfirlitseiningunni.
                -   Staðfestið að **SequenceNumber** er varpað úr uppruna í sviðsetningu.

3.  Flytja inn nýtt uppgjör.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]