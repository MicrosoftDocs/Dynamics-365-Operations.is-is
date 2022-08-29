---
title: Algengar spurningar um ósamstilltur viðskiptahamur
description: Þessi grein veitir svör við algengum spurningum um ósamstilltan viðskiptaham í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229974"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>Algengar spurningar um ósamstilltur viðskiptahamur

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein veitir svör við algengum spurningum um ósamstillta (ósamstillta) viðskiptaham í Microsoft Dynamics 365 Commerce.

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>Af hverju get ég ekki virkjað eiginleikann „Virkja klippingu viðskiptavina í ósamstilltri stillingu“?

Áður en þú virkjar **Virkjaðu að breyta viðskiptavinum í ósamstilltum ham** eiginleika, þú verður að virkja eftirfarandi eiginleika:

- Frammistöðubætir fyrir pantanir viðskiptavina og viðskipti viðskiptavina
- Virkjaðu aukna ósamstillta sköpun viðskiptavina
- Virkja ósamstillta stofnun fyrir aðsetur viðskiptavinar

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>Af hverju sé ég ennþá þjónustusímtöl í rauntíma til höfuðstöðva Commerce eftir að „Virkja klippingu viðskiptavina í ósamstilltri stillingu“ er virkjaður?

Þetta vandamál kemur upp þegar Commerce Data Exchange (CDX) störf hafa ekki verið keyrð til að tryggja að eiginleikastöðu og önnur lýsigögn rásar séu samstillt við rásina. Áður en þú reynir atburðarásina aftur skaltu ganga úr skugga um að eftirfarandi CDX störf séu keyrð í höfuðstöðvum Commerce:

- 1110 (alþjóðleg stilling)
- 1010 (Viðskiptavinir)
- 1070 (STilling rásar)

Gögn sem eru í skyndiminni í Commerce Scale Unit (CSU) endurspeglast kannski ekki strax í höfuðstöðvum Commerce eftir að CDX störfin hafa verið keyrð.

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Af hverju sýna höfuðstöðvar Commerce ekki sköpun viðskiptavina eða uppfærslur frá sölustað (POS) eða rafrænum viðskiptum?

Gakktu úr skugga um að eftirfarandi aðgerðir hafi verið gerðar í þeirri röð sem þær eru taldar upp hér.

1. Keyra CDX P-starfið í höfuðstöðvum Commerce til að tryggja að ósamstillt gögn viðskiptavina sem eru geymd í **VERSLUNARSYNKT ViðskiptavinurV2**, **·**, **VIÐVUNDASAMBAND**, **VIÐskiptavina**, og **VERSLUNARHYND VIÐVINNUSTAÐRIBUTEV2** töflur eru fáanlegar í höfuðstöðvum Commerce.
1. Keyra á **Samstilltu viðskiptavini og rásbeiðnir** hópvinna í höfuðstöðvum Commerce. Eftir árangursríka framkvæmd runuvinnunnar munu allar færslur sem hafa verið unnar úr áðurnefndum töflum hafa **Netaðgerð lokið** reit stillt á **1**.
