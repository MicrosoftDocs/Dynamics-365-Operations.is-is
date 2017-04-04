---
title: "Setja upp aðgerðir fyrir aukin innskráning starfsmanns fyrir POS Skýi og MPOS"
description: "Þessi wiki nær yfir valmöguleikarnir til að setja upp aukin innskráning starfsmanns fyrir Skýi POS og Retail Modern POS (MPOS)."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 0dc80784a5c9a7de6009826284cb68f1aee83f70
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a>Setja upp aðgerðir fyrir aukin innskráning starfsmanns fyrir POS Skýi og MPOS

Þessi wiki nær yfir valmöguleikarnir til að setja upp aukin innskráning starfsmanns fyrir Skýi POS og Retail Modern POS (MPOS).

<a name="setting-up-extended-logon"></a>Setja upp aukna innskráningu starfsmanns
=========================

Hægt er að finna uppsetningu strikamerkja á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingar**&gt;**virknireglur**. Flýtiflipinn **Aðgerðir** inniheldur eftirfarandi valkosti sem eru tengdir lengdri innskráningu starfsmanns.

### <a name="staff-bar-code-logon"></a>Strikamerkisinnskráning starfsmanns

Þegar valkosturinn **Strikamerkisinnskráning starfsmanns** er virkjaður geta starfsmenn sem hafa aukna innskráningu úthlutað á sölustað sinn (POS) skráð sig inn með því að nota strikamerki.

### <a name="staff-bar-code-logon-requires-password"></a>Nota þarf aðgangsorð með strikamerkisskráningu starfsmanns

Þegar valkosturinn **Strikamerkisinnskráning starfsmanns krefst aðgangsorðs** er virkjaður velur strikamerkisinnskráning starfsmanns aðeins þann starfsmann sem er úthlutað á þá auknu innskráningu sem er sýnd. Starfsmenn þurfa samt að færa inn aðgangsorð sitt þegar þessi valkostur er gerður virkur.

### <a name="staff-card-logon"></a>Kortainnskráning starfsmanns

Þegar valkosturinn **Kortainnskráning starfsmanns** er virkjaður geta starfsmenn sem hafa aukna innskráningu úthlutað á sölustað sinn (POS) skráð sig inn með því að nota segulrönd.

### <a name="staff-card-logon-requires-password"></a>Nota þarf aðgangsorð með kortainnskráningu starfsmanns

Þegar valkosturinn **Kortainnskráning starfsmanns krefst aðgangsorðs** er virkjaður velur kortainnskráning starfsmanns aðeins þann starfsmann sem er úthlutað á þá auknu innskráningu sem er sýnd. Starfsmenn þurfa samt að færa inn aðgangsorð sitt þegar þessi valkostur er gerður virkur.

<a name="assigning-an-extended-logon"></a>Úthlutun aukinnar innskráningu
===========================

Að sjálfgefnu geta aðeins stjórnendur úthlutað aukinni innskráningu til starfsmanna. Til að úthluta aukin innskráning starfsmanns, er farið **Auknu innskráning** á Sölustað. Síðan leita starfsmann með því að færa inn Kenni stjórnanda hans eða hennar í svæðinu leita. Veljið notanda og smellið á **Úthluta**. Á næstu síðu skal lesa eða skanna aukna innskráningu til að úthluta á starfsmanninn. Ef kortalestur eða skönnun er var lesin verður hnappuinn **Í lagi **tiltækur. Smellið á **Í lagi** til að vista aukna innskráningu fyrir þann starfsmann.

<a name="deleting-an-extended-logon"></a>Eyðing aukinnar innskráningar
==========================

Til að eyða aukinni innskráningu sem er úthlutað á starfsmann, skal leita að starfsmanni með því að nota aðgerðina **Aukin innskráning**. Veljið notanda og smellið á **Hætta við úthlutun**. Öll útvíkkuð skilríki sem eru tengd við starfsmanninn eru fjarlægð.

<a name="extending-extended-logon"></a>Útvíkkun aukinnar innskráningar
========================

Hægt er að auka innskráningarþjónustu til að styðja til viðbótar aukin innskráningartæki, eins og lófaskanna. Nánari upplýsingar fást í fylgigögnum um POS.

<a name="using-extended-logon"></a>Notkun aukinnar innskráningar
====================

Þegar aukin innskráning er skilgreind og starfsmanni hefur verið úthlutað á strikamerki eða segulrönd, þarf starfsmaðurinn aðeins að renna eða skanna kortið sitt meðan síðan Innskráning á sölustað birtist. Ef aðgangsorðs er einnig krafist áður en innskráning getur haldið áfram er starfsmaður beðinn um að færa inn aðgangsorð sitt.


