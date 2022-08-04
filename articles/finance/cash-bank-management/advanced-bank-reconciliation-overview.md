---
title: Yfirlit ítarlegrar bankaafstemmingar
description: Þessi grein lýsir flæðinu fyrir ítarlegt ferli bankaafstemmingar. Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit sem er hægt að stemma af beint innan úr bankafærslu.
author: angelad116
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96542aa2ee1fed85864b7695199df464ca7866be
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151654"
---
# <a name="advanced-bank-reconciliation-overview"></a>Yfirlit ítarlegrar bankaafstemmingar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir flæðinu fyrir ítarlegt ferli bankaafstemmingar. Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit sem er hægt að stemma af beint innan úr bankafærslu.

Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit. Innflutt bankayfirlit getur þá°verið afstemmt sjálfkrafa innan bankafærslna. Hér eru þrep í ítarlegu bankaafstemmingar°flæði.

1.  Setja upp innflutning bankayfirlits.
    -   Flytja inn bankayfirlit gegnum umgjörð gagnaeininga.
    -   Þrjú dæmigerð bankayfirlitssnið eru innbyggð: ISO20022, BAI2 og°MT940.
    -   Hægt er að auka virknina í hvaða snið sem er.

2.  Setja upp númeraröð til að nota°fyrir ítarlega bankaafstemmingu og skilgreina samsvörunarreglur bankaafstemmingar.
    -   Samsvörunarregla er sett af viðmiðum sem eru notuð til að sía bankayfirlitslínur og Microsoft Dynamics 365 Fjármálabankafærslulínur meðan á afstemmingu stendur. Hægt er að setja upp fleiri en eina samsvörunarreglu til að gera sjálfvirkt og bæta ferli við afstemmingar eftir þörfum fyrirtækisins.

3.  Stemma af bankayfirlit með bankafærslum Finance.
    -   Framkvæma sjálfvirka jöfnun og stofnun afstemmingafærslubóka.
    -   Skoða bankayfirlit og bankafærslur Finance hlið við hlið.
    -   Sjálfkrafa bókun á bankafærslum Finance ef þær birtast á bankayfirlitum en birtast ekki í forritinu Finance.
    -   Búa til afstemmingaryfirlit.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
