---
title: Uppfærsla samsettrar einingar bankafærslubókar
description: Þetta efnisatriði sýnir skrefin sem þarf til að bæta reitnum BankTransactionType við samsett BankJournalEntity.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 730e6bd10b0cdd1587c915bb9ec8d6a4792435d9
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727259"
---
# <a name="update-the-bank-journal-composite-entity"></a>Uppfærsla samsettrar einingar bankafærslubókar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði sýnir skrefin sem þarf til að bæta reitnum BankTransactionType við samsett BankJournalEntity.

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
