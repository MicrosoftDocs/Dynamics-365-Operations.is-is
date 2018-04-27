---
title: "Þekjustillingar"
description: "Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 591b1cd739bb3be61299f33f180ca7c264d21a35
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="coverage-settings"></a>Þekjustillingar

[!INCLUDE [banner](../includes/banner.md)]

Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir. 

Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:

-   Tilgreina þekjustillingar fyrir þekjuflokk. Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn. Smellið á **Aðaláætlanagerð &gt; Uppsetning &gt; Trygging &gt; Þekjuflokkar** til að stofna þekjuflokk. Hægt er að tengja þekjuflokk við vöru. Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**. Sé tengillinn almennur, án tillits til afurðarvídda, skal nota **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**. Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð **Almennan þekjuflokk** sem tilgreindur er á síðunni **Færibreytur áætlanagerðar** sem sjálfgildi.

-   Tilgreinið þekjustillingar fyrir afurð. Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er. Smellið á **Upplýsingastjórnun afurða &gt; Afurðir &gt; Losaðar afurðir**. Veljið afurðina og síðan í **Aðgerðarrúðu** á flipanum **Áætlun**, í **Þekjuflokkur** er smellt á **Vöruþekja** til að opna síðuna **Vöruþekja**. Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**. Þekjustillingar á síðunni**Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.

<!-- -->

-   Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit. Leiðsagnarforritið er leiðsögn skref fyrir skref til að hjálpa þér að setja upp færibreytur fyrir vörutryggingu. Á síðunni **Vöruþekja** er smellt á **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.

<!-- -->

- Tilgreinið þekjustillingar fyrir víddarflokk. Smellið á <strong>Upplýsingastjórnun afurða &gt; Algengt &gt; Losaðar afurðir</strong>. Á flipanum <strong>Upplýsingar um útgefna afurð **síðu, á **Almennt</strong> í flokknum <strong>Stjórnun</strong> skal smella á tengilinn <strong>Flokkur geymsluvíddar</strong>. Á síðunni <strong>Geymsluvíddarflokkur</strong> skal velja <strong>Þekjuáætlun eftir vídd</strong> til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum. Allar afurðavíddir, eins og skilgreining, litur, stærð, stíll, verða að hafa reitinn <strong>Þekjuáætlun eftir vídd</strong> valinn.



<a name="see-also"></a>Sjá einnig
--------

[Aðaláætlanir](master-plans.md)




