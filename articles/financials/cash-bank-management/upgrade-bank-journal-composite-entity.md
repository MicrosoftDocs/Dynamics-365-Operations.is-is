---
title: Uppfæra samsetta einingu færslubókar banka
description: Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 70db65dca4cfadd1ed8769386b4b437cecc217a2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565923"
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
    -   Sýna **Bankafærslu** gerð á **Upprunagögn**útlit.
        -   Snið upprunagagna = XML-Element.
        -   Nafn einingar = færslubók banka
        -   Hlaða upp gagnaskrá = ný útgáfa SampleBankJournalCompositeEntity.xml
        -   Smellið á **„Já“** til að skrifa yfir núgildandi skrá.
        -   Smellið á **Já** til að mynda vörpun frá byrjun.
        -   Staðfestið að Bankafærslugerð er varpað.
            -   Smellið á **Skoða vörpun** á Línueiningar.
            -   Staðfestið að bankafærslugerð er varpað úr uppruna í sviðsetningu.

3.  Flytja inn nýtt uppgjör.




