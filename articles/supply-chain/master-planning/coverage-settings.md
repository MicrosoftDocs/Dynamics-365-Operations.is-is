---
title: Þekjustillingar
description: Þetta efnisatriði veitir upplýsingar um þekjustillingar sem aðalröðun notar til að reikna út vöruþarfir.
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
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538895"
---
# <a name="coverage-settings"></a>Þekjustillingar

[!include [banner](../includes/banner.md)]

Aðalröðun notar þekjustillingar til þess að reikna vöruþarfir.

Hægt er að tilgreina þekjustillingar með nokkrum aðferðum:

- Tilgreina þekjustillingar fyrir þekjuflokk.

    Hægt er að stofna þekjuflokk sem inniheldur stillingar fyrir allar afurðir sem eru tengdar við þekjuflokkinn. Til að stofna þekjuflokk skal opna **Aðaláætlanagerð &gt; Uppsetning &gt; Þekja &gt; Þekjuflokkar**. Hægt er að tengja þekjuflokk við vöru. Ef tengillinn er tilgreindur fyrir svæði, vöruhús eða afurðarvídd skal nota reitinn **Þekjuflokk** á síðunni **Vöruþekja**. Sé tengillinn almennur, án tillits til afurðarvídda, skal nota reitinn **Þekjuflokk** á flýtiflipanum **Áætlun** á síðunni **Afurðarupplýsingar**. Ef þú tengir ekki þekjuflokk við afurð notar aðaláætlanagerð sem sjálfgildi almennan þekjuflokk sem tilgreindur er á síðunni **Færibreytur áætlanagerðar**.

- Tilgreinið þekjustillingar fyrir afurð.

    Hægt er að breyta stillingunni fyrir ákveðna framleiðslupöntun hvenær sem er. Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**. Veljið afurðina og síðan í Aðgerðarrúðu á flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja** til að opna síðuna **Vöruþekja**. Ef afurð er tengd þekjuflokki er hægt að hnekkja þekjuflokksstillingum með því að nota reitinn **Hnekkja**. Þekjustillingar á síðunni**Vöruþekja** taka forgang yfir stillingar á síðunni **Þekjuflokkur**.

- Tilgreinið þekjustillingar fyrir afurð með því að nota leiðsagnarforrit.

    Leiðsagnarforritið leiðir þig skref fyrir skref í gegnum ferlið við að setja upp færibreytur fyrir helstu vöruþekjuna. Á síðunni **Vöruþekja**, í aðgerðarúðunni, er valið **Leiðsagnarforrit** til að opna **Leiðsagnarforrit vöruþekju**.

- Tilgreinið þekjustillingar fyrir víddarflokk.

    Opna **Afurðaupplýsingastjórnun &gt; Afurðir &gt; Útgefnar afurðir**. Á síðunni **Upplýsingar um losaðar afurðir** á flýtiflipanum **Almennt**, í hlutanum **Stjórnun**, er smellt á tengilinn í reitnum **Geymsluvíddarflokkur**. Á síðunni **Geymsluvíddarflokkur** skal velja gátreitinn **Þekjuáætlun eftir vídd** til að stofna þekjustillingar fyrir vídd í geymsluvíddarflokknum. Velja verður reitinn **Þekjuáætlun eftir vídd** fyrir allar afurðarvíddir, t.d. skilgreiningu, lit, stærð og stíl.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðaláætlanir](master-plans.md)
