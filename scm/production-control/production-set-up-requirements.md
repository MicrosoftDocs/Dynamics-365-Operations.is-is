---
title: "Uppsetningarkröfur framleiðslu"
description: "Þessi grein veitir upplýsingar um uppsetningarskilyrðu áður en hægt er að vinna með framleiðslustýringu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 469cf4513a970effb34a857b71a89fd0a5499e25
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="production-setup-requirements"></a>Uppsetningarkröfur framleiðslu

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um uppsetningarskilyrðu áður en hægt er að vinna með framleiðslustýringu. 

Framleiðslustýring er samþætt við aðgerðir í öðrum kerfiseiningum. Vegna þessara tengsla er hægt að breyta framleiðslupöntunum og tryggja að þær uppfærist sjálfkrafa í öllum öðrum ferlum og útreikningum í kerfinu. Framkvæma ætti uppsetningaraðgerðirnar í þeirri röð sem þær birtast hér fyrir neðan.

## <a name="required-baseline-setup-in-other-modules"></a>Skyldug grunnuppsetning í öðrum kerfiseiningum
Setja verður upp upplýsingar í öðrum einingum áður en hægt er að vinna með framleiðslustýringu. Uppsetning felur í sér eftirfarandi verkefni:

-   Setja upp almennar upplýsingar um fyrirtækið.
-   Setja upp fjárhag.
-   Skilgreina vöruflokka.
-   Setja upp fjárhagslykla fyrir vöruflokka.
-   Setja upp töflu fyrir birgðavörur í Birgðastjórnun.
-   Stofna uppskriftir (BOMs) og uppskriftaútgáfur í birgðastjórnun.

## <a name="required-calendar-and-resource-setup"></a>Skyldug uppsetning dagatals og tilfanga
Áður en þú notar framleiðslustýring, opnaðu Fyrirtækisstjórnun og stofna og skilgreina dagatal og rekstrartilföng í eftirfarandi röð:

1.  **Sniðmát vinnutíma** – Setja upp sniðmát vinnutíma til að skilgreina tímana sem eru í boði fyrir framleiðsluröðun.
2.  **Dagatöl** – Setja upp vinnutímadagatal til að skilgreina daga ársins sem eru í boði fyrir framleiðsluröðun.
3.  **Tilfangaflokkar** – Setja upp tilfangaflokka til að flokka rekstrartilföngum, þannig að hægt er að fá yfirlit yfir allar lausa afkastagetu þegar röðun er keyrð. Ekki þarf að setja upp tilfangaflokka áður en þú setur upp rekstrartilföng. Þó er mælt með að skilja hvernig skuli flokka tilföng þegar sett er upp framleiðslustýringu.
4.  **Tilföng** - Setja upp rekstrartilföng til að skilgreina tilföng sem notuð eru til að ljúka framleiðsluferli og til að áætla afkastagetu.

## <a name="required-production-parameters-setup"></a>Skyldug uppsetning framleiðslufæribreyta
**Færibreytur framleiðslustýringar** – Setja upp grunnfæribreytur framleiðslu til að skilgreina hvernig kerfið meðhöndlar og vinnur úr framleiðslupöntunum. Skilgreinið hvernig á að stofna, meta, raða og nota framleiðslupantanir. Einnig er hægt að velja um svörun og hvernig kostnaðarbókhald fer fram.

## <a name="required-journal-name-identification"></a>Skyldug auðkenning færslubókarheita
**Heiti framleiðslubóka** – Tilgreina heiti framleiðslubóka sem eru notaðar til að skrá og bóka færslur.

## <a name="setup-if-you-use-operations"></a>Uppsetning ef aðgerðir eru notaðar
Aðgerðir tákna tiltekna verkþætti sem er lokið til að framleiða endanlega afurð. **Ábending:** Þú verður að þekkja gerðir verkþátta sem eru nauðsynleg til að framleiða vöruna, og röð og forgang þeirra verkþætti. Þú Verður einnig vitað er hvaða tilföng eru innifalin, og hversu margar.

1.  **Aðgerðir** - Setja upp aðgerðir sem standa fyrir þau verk sem þarf að ljúka til að framleiða lokna afurð.
2.  **Tengsl** - Setja upp vensl aðgerða til að gefa ítarlegri eiginleika. Vensl aðgerða eru skilgreind með því að smella á **Tengsl** á í **Aðgerðir** síðu.

## <a name="setup-if-you-use-routes"></a>Uppsetning ef leiðir eru notaðar
Ef unnið er með leiðir þarf að skilgreina aðgerðir fyrir hverja framleiðsluleið sem sett er upp. Leiðin sýnir hvernig varan fer á milli aðgerða, og frá upphafi framleiðsluferlis til enda.

1.  **Kostnaðartegundir** - Setja upp kostnaðartegundir til að skilgreina kostnað á hverja klukkustund í tilgreindum ferlum og uppsetningartímum.
2.  **Kostnaðarflokkar** - Setja upp kostnaðarflokka til að stofna og hafa umsjón með mörgum gerðum kostnaðar.
3.  **Leiðarflokkar** - Setja upp leiðaflokka til að skilgreina færibreytur sem eiga við um hópa af leiðum. Það verður að setja upp leiðaflokka áður en farið er að stofna framleiðsluleiðir.
4.  **Leiðir** Setja upp framleiðsluleiðir og skilgreinið sjálfgefnar stillingar til að stjórna röðun, kostnaðarútreikning og verðlagningu leiðaaðgerða og framvinduskýrslur.
5.  **Leiðir** - Setja upp leiðaútgáfur til að virkja vöruafbrigði í framleiðslu.

## <a name="optional-advanced-settings"></a>Valfrjálsar, ítarlegar stillingar
1.  **Framleiðsluflokkar** - Setja upp framleiðsluflokka til koma á tengslum milli framleiðslupöntunar og fjárhagslykla. Pantanir verða bókaðar í fjárhagslyklana eða flokkaðar í þá við skýrslugerð.
2.  **Framleiðsluhópar** - Stofna framleiðsluhópa til að flokka framleiðslupantanir fyrir vinnslu mikilvægra pantana eða til að eyða og bóka flokka pantana.
3.  **Eiginleikar** -Skilgreina eiginleika til að stofna sérstakar eigindir sem hægt er að tengja við tilföng til að stýra röð framleiðslna. Eigindirnar eru tengdar vinnutímasniðmátinu.





