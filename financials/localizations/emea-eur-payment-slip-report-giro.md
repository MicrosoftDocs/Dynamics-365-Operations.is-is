---
title: "Fylgiseðils greiðsluskýrslu fyrir Europe"
description: "Þetta efni veitir upplýsingar um skýrslur fyrir Europe fylgiseðils."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264604
ms.assetid: 551e047b-4581-4a77-b470-c4f8d395c375
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c795466753ca1515790b7961b989aac6e7d63c2c
ms.lasthandoff: 03/31/2017


---

# <a name="payment-slip-report-for-europe"></a>Fylgiseðils greiðsluskýrslu fyrir Europe

Þetta efni veitir upplýsingar um skýrslur fyrir Europe fylgiseðils.

Virkni fyrir skýrslur fylgiseðils er tiltæk fyrir lögaðila með þeirra aðalaðsetur í Danmörku, Belgíu, Noregur, Sviss eða Finnland. Fyrirtæki oft tengja prentaða greiðslueðlar reikninga til að veita tilvísun greiðslu fyrir bókun og jöfnun. Hægt er að nota greiðsluseðillinn fyrir reikninga verks eða þjónustusamning , innheimtubréf, vaxtanótur og reikningsyfirlit auk sölureikninga og reikningur með frjálsum texta.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Setja upp Kenni númer lánardrottins (eingöngu Danmörk)
Fylgið eftirfarandi skrefum til að færa inn númer kenni lánardrottins fyrirtækisins. Samband fjármálastofnun veitir þetta númer. Það er notað sem tilvísun þegar greiðslur viðskiptavinar eru mótteknar með mismunandi fjármálastofnunum.

1.  Smellið á **fyrirtækisstjórnun**&gt;**Uppsetningu**&gt;**Fyrirtækis**&gt;**lögaðila**.
2.  Á við **bankareikningsupplýsingar** FastTab í á **FI-Lánardrottinskennið** skal færa inn númer lánardrottins einkvæmt átta tölustafa Kenni.
3.  Skjámyndinni er lokað til að vista breytingar.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Setja upp greiðslu viðhengið snið fylgiseðils fyrir reikninga, vaxtanótur, innheimtubréf og reikningsyfirlit
Fylgið eftirfarandi skrefum til að setja upp snið fyrir viðhengi fylgiseðils greiðslu sem er fylgt sölureikninga, textareikninga, vaxtanótur, innheimtubréf og reikningsyfirlit.

1.  Smellið á **Viðskiptakröfur**&gt;**Uppsetningu**&gt;**Skjámyndir**&gt;**bréfs**.
2.  Á í **Reiknings** flipanum, á **Viðhengd greiðslukvittun á reikningi viðskiptavinar** skal velja greiðslusnið fylgiseðils viðhengi.
3.  Á við **textareikning**, **vaxtanótu**, **innheimtubréf**, og **Lykill uppgjör** flipunum, veljið greiðslu viðhengið snið fylgiseðils fyrir hverja skjalagerð.
4.  Skjámyndinni er lokað til að vista breytingar.

Fylgið eftirfarandi skrefum til að setja upp snið fyrir viðhengi fylgiseðils greiðslu sem er fylgt verkreikninga.

1.  Smellt er á **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Skjámyndir**&gt;**bréfs**.
2.  Í því **Greiðsluviðhengi** skal velja greiðslusnið fylgiseðils viðhengi.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Úthluta snið fylgiseðils viðhengið greiðslu á viðskiptavinalykil
Eftir að setja upp fylgiseðils viðhengið greiðslusnið fyrir sölureikninga, textareikninga, vaxtanótur, innheimtubréf, reikningsyfirlit og verkreikningum hægt er að úthluta tilteknum snið fyrir valinn viðskiptavin.

1.  Smellið á **Viðskiptakröfur**&gt;**Algengar**&gt;**Viðskiptavini**&gt;**Alla viðskiptavini**.
2.  Stofna nýjan viðskiptavin eða veljið fyrirliggjandi viðskiptavini.
3.  Á við **Reikningur og afhending** FastTab í á **á reikningi viðskiptavinar**, **á textareikningi**, **á vaxtanótu**, **á innheimtubréf**, **á verkreikning**, og **á reikningsyfirliti** svæði, veljið snið fyrir viðhengi fylgiseðils greiðslu sem verður fylgt hver gerð skjala sem eru sendar til valins viðskiptavinar.
4.  Skjámyndinni er lokað til að vista breytingar.



