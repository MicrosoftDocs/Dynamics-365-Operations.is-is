---
title: Uppfæra samsetta einingu færslubókar banka
description: Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444245"
---
# <a name="update-the-bank-journal-composite-entity"></a>Uppfæra samsetta einingu færslubókar banka

[!include [banner](../includes/banner.md)]

Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity.

Fylgið eftirfarandi skrefum til að bæta reitnum BankTransactionType við samsetta BankJournalEntity.

1.  Tala sa,am og samstilla eftirfarandi samsettar einingar færslubókar banka, einingar og sviðsetningartöflur:
    -   Samsett eining\\BankJournalEntity
    -   Eining\\BankJournalHeaderEntity
    -   Eining\\BankJournalLineEntity
    -   Tafla\\BankJournalHeaderStaging
    -   Tafla\\BankJournalLineStaging

2.  Gagnastjórnun\\gagnaverk
    -   Sýna **Bankafærslu** gerð á **Upprunagögn** útlit.
        -   Snið upprunagagna = XML-Element.
        -   Nafn einingar = færslubók banka
        -   Hlaða upp gagnaskrá = ný útgáfa SampleBankJournalCompositeEntity.xml
        -   Smellið á **„Já“** til að skrifa yfir núgildandi skrá.
        -   Smellið á **Já** til að mynda vörpun frá byrjun.
        -   Staðfestið að Bankafærslugerð er varpað.
            -   Smellið á **Skoða vörpun** á Línueiningar.
            -   Staðfestið að bankafærslugerð er varpað úr uppruna í sviðsetningu.

3.  Flytja inn nýtt uppgjör.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]