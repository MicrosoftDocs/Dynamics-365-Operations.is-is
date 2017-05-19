---
title: "Greiðsluseðilsskýrsla fyrir Evrópu"
description: "Þetta efnisatriði veitir upplýsingar um greiðsluseðilsskýrslur fyrir Evrópu."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 53b03f70ea10a340599ef73f12a9a1aa67bfcac4
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="payment-slip-report-for-europe"></a>Greiðsluseðilsskýrsla fyrir Evrópu

[!include[banner](../includes/banner.md)]


Þetta efnisatriði veitir upplýsingar um greiðsluseðilsskýrslur fyrir Evrópu.

Þessi eiginleiki fyrir greiðsluseðilsskýrslur er í boði fyrir lögaðila sem hafa aðalaðsetur í Danmörku, Belgíu, Noregi, Sviss eða Finnlandi. Fyrirtæki láta prentaða greiðsluseðla oft fylgja með reikningum sem greiðslutilvísun fyrir bókun og uppgjör. Hægt er að nota greiðsluseðillinn fyrir reikninga verks eða þjónustusamning , innheimtubréf, vaxtanótur og reikningsyfirlit auk sölureikninga og reikningur með frjálsum texta.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Setja upp kenninúmer lánardrottins (aðeins í Danmörku)
Fylgið eftirfarandi skrefum til að færa inn kennitölu lánveitanda fyrirtækisins. Fjármálastofnunin lætur þetta númer í té. Það er notað sem tilvísun þegar greiðslur viðskiptavinar eru mótteknar frá fjármálastofnunum.

1.  Smellt er á **Fyrirtækisstjórnun** &gt; **Setja upp** &gt; **Fyrirtæki** &gt; **Lögaðilar**.
2.  Í flýtiflipanum **Bankareikningsupplýsingar**, í reitnum **Kenni FI-Lánardrottins**, skal færa inn einkvæma, átta stafa kennitölu lánveitanda.
3.  Skjámyndinni er lokað til að vista breytingar.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Setja upp snið fyrir greiðsluseðil í viðhengi fyrir reikninga, vaxtanótur, innheimtubréf og reikningsyfirlit
Fylgið þessum leiðbeiningum til að setja upp snið fyrir greiðsluseðil í viðhengi til að fylgja með sölureikningum, reikningum með frjálsum texta, vaxtanótum, innheimtubréfum og reikningsyfirlitum.

1.  Smellt er á **Viðskiptakröfur** &gt; **Setja upp** &gt; **Skjámyndir** &gt; **Uppsetning skjámynda**.
2.  Í flipanum **Reikningur**, í reitnum **Tengd greiðslukvittun á svæði fyrir reikning viðskiptavinar**, skal velja snið greiðsluseðils í viðhengi.
3.  Í flipunum **Reikningur með frjálsum texta**, **Vaxtanóta**, **Innheimtubréf** og **Reikningsyfirlit** skal velja snið fyrir greiðsluseðil í viðhengi fyrir hverja gerð skjals.
4.  Skjámyndinni er lokað til að vista breytingar.

Fylgið þessum leiðbeiningum til að setja upp snið fyrir greiðsluseðil í viðhengi til að fylgja með verkreikningum.

1.  Smellt er á **Verkefnastjórnun og bókhald** &gt; **Uppsetning** &gt; **Skjámyndir** &gt; **Uppsetning skjámynda**.
2.  Í reitnum **Tengd greiðslukvittun** skal velja snið greiðsluseðils í viðhengi.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Snið greiðsluseðils í viðhengi tengt við viðskiptavinalykil
Þegar þú hefur sett upp snið fyrir í greiðsluseðill í viðhengi fyrir sölureikninga, reikninga með frjálsum texta, vaxtanótur, innheimtubréf, reikningsyfirlit og verkreikninga er hægt að tengja tiltekin snið við valda viðskiptavini.

1.  Smellt er á **Viðskiptakröfur** &gt; **Algengt** &gt; **Viðskiptavinir** &gt; **Allir viðskiptavinir**.
2.  Stofna nýjan viðskiptavin eða velja fyrirliggjandi viðskiptavin.
3.  Í flýtiflipanum **Reikningur og afhending**, í reitunum **Á reikningi viðskiptavinar**, **Á reikningi með frjálsum texta**, **Á vaxtanótu**, **Á innheimtubréfi**, **Á verkreikningi** og **Á reikningsyfirliti** skal velja snið fyrir greiðsluseðil í viðhengi sem mun fylgja með skjölum af hverri gerð sem send eru til valins viðskiptavinar.
4.  Skjámyndinni er lokað til að vista breytingar.





