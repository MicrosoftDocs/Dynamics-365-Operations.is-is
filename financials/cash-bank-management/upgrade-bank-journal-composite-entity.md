---
title: "Uppfæra í banka færslubók samsetta einingu"
description: "Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 14d58604f5c0aaa4725345f58982387ad0a23205
ms.lasthandoff: 03/31/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Uppfæra í banka færslubók samsetta einingu

Eftirfarandi skrefum þarf til að bæta við aukalegum reitnum BankTransactionType við samsetta BankJournalEntity.

Fylgið eftirfarandi skrefum til að bæta reitnum BankTransactionType við samsetta BankJournalEntity.

1.  Tala sa,am og samstilla eftirfarandi samsettar einingar færslubókar banka, einingar og sviðsetningartöflur:
    -   Samsett Eining\\BankJournalEntity
    -   Eining\\BankJournalHeaderEntity
    -   Eining\\BankJournalLineEntity
    -   Taflan\\BankJournalHeaderStaging
    -   Taflan\\BankJournalLineStaging

2.  Stjórnun gagna\\gögn verk
    -   Sýna **Bankafærslu ** gerð á **Upprunagögn **útlit.
        -   Snið upprunagagna = XML-Element.
        -   Nafn einingar = færslubók banka
        -   Hlaða upp gagnaskrá = ný útgáfa SampleBankJournalCompositeEntity.xml
        -   Smellið á **„Já“** til að skrifa yfir núgildandi skrá.
        -   Smellið á **Já ** til að mynda vörpun frá byrjun.
        -   Staðfestið að Bankafærslugerð er varpað.
            -   Smellið á **Skoða vörpun ** á Línueiningar.
            -   Staðfestið að bankafærslugerð er varpað úr uppruna í sviðsetningu.

3.  Flytja inn nýtt uppgjör.



