---
title: Þekjustillingar
description: Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "322560"
---
# <a name="coverage-settings"></a>Þekjustillingar

[!include [banner](../includes/banner.md)]

Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir. 

Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:

-   Tilgreina þekjustillingar fyrir þekjuflokk. Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn. Smellið á **Aðaláætlanagerð &gt; Uppsetning &gt; Trygging &gt; Þekjuflokkar** til að stofna þekjuflokk. Hægt er að tengja þekjuflokk við vöru. Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**. Sé tengillinn almennur, án tillits til afurðarvídda, skal nota **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**. Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð **Almennan þekjuflokk** sem tilgreindur er á síðunni **Færibreytur áætlanagerðar** sem sjálfgildi.

-   Tilgreinið þekjustillingar fyrir afurð. Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir &gt; Losaðar afurðir**. Veljið afurðina og síðan í **Aðgerðarrúðu** á flipanum **Áætlun**, í **Þekjuflokkur** er smellt á **Vöruþekja** til að opna síðuna **Vöruþekja**. Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**. Þekjustillingar á síðunni**Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.

<!-- -->

-   Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit. Leiðsagnarforritið er leiðsögn skref fyrir skref til að hjálpa þér að setja upp færibreytur fyrir vörutryggingu. Á síðunni **Vöruþekja** er smellt á **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.

<!-- -->

- Tilgreinið þekjustillingar fyrir víddarflokk. Smellið á **Upplýsingastjórnun afurða &gt; Algengt &gt; Losaðar afurðir**. Á síðunni **Upplýsingar um losaða afurð** á flipanum **Almennt** í flokknum **Stjórnun** er smellt á tengilinn **Geymsluvíddaflokkur**. Á síðunni **Geymsluvíddarflokkur** skal velja **Þekjuáætlun eftir vídd** til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum. Allar afurðavíddir, eins og skilgreining, litur, stærð, stíll, verða að hafa reitinn **Þekjuáætlun eftir vídd** valinn.



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Aðaláætlanir](master-plans.md)



