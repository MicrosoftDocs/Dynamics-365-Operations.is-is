---
title: Yfirlit ítarlegrar bankaafstemmingar
description: Þessi grein lýsir flæðinu fyrir ítarlegt ferli bankaafstemmingar. Ítarleg afstemming aðgerð gerir það mögulegt að flytja inn bankayfirlit sem er hægt að stemma af beint innan úr bankafærslu.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83852509ad7dd1057906c0e12ffc278768ea986
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830569"
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
    -   Jöfnunarregla afstemmingar er safn skilyrða sem eru notuð til að sía bankayfirlitslínur og bankaskjalslínur Microsoft Dynamics 365 Finance á meðan á afstemmingarferlinu stendur. Hægt er að setja upp fleiri en eina samsvörunarreglu til að gera sjálfvirkt og bæta ferli við afstemmingar eftir þörfum fyrirtækisins.

3.  Stemma af bankayfirlit með bankafærslum Finance.
    -   Framkvæma sjálfvirka jöfnun og stofnun afstemmingafærslubóka.
    -   Skoða bankayfirlit og bankafærslur Finance hlið við hlið.
    -   Sjálfkrafa bókun á bankafærslum Finance ef þær birtast á bankayfirlitum en birtast ekki í forritinu Finance.
    -   Búa til afstemmingaryfirlit.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]