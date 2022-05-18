---
title: Jafnaðar færslubækur fyrir millieiningabókhald
description: Þessi grein sýnir hvernig færslubók er jöfnuð sjálfkrafa þegar jöfnunarfjárhagsvídd er valin á síðunni Fjárhagur.
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712315"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Jafnaðar færslubækur fyrir millieiningabókhald

[!include [banner](../includes/banner.md)]

Þessi grein sýnir hvernig færslubók er jöfnuð sjálfkrafa þegar jöfnunarfjárhagsvídd er valin á síðunni Fjárhagur. 

Ef bókhaldsfærslur eru ekki jafnaðar á stigi fjárhagsvíddargilda, eru sjálfkrafa stofnaðar lykilfærslur til að jafna við færslubókina. Þessar lykilfærslur nota **Millieining - debet** og **Millieining - kredit** bókunargerðir á síðunni **Fjárhagslyklar fyrir sjálfvirkar færslur** til að ákvarða aðallykilinn. Til dæmis er Fyrirtækiseining, sem er anna hluti fjárhagslykils, valið sem jöfnunarfjárhagsvídd og eftirfarandi bókhaldsfærslur verða síðan stofnaðar.

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100,00 DR |
| 6100 – NY – OU\_249  | 100,00 DR |
| 2100 – MSP – OU\_256 | 200,00 CR |

Í þessu tilfelli eru eftirfarandi stöður ákvarðaðar:

-   Fyrir fyrirtækiseiningu MSP = 100.00 CR
-   Fyrir fyrirtækiseiningu NY = 100.00 DR

Þessvegna eru°eftirfarandi bókhaldsfærslur stofnaðar sjálfkrafa til að jafna færslubókina á stigi fjárhagsvíddargilda.

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (Debet millieininga) – MSP – OU\_256 | 100,00 DR |
| (Kredit millieininga) – NY – OU\_249 | 100,00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
