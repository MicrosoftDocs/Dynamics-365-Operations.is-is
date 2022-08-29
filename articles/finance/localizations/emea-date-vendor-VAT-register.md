---
title: Dagsetning VSK-skrár lánardrottins
description: Þessi grein veitir upplýsingar um eiginleika til að virkja dagsetningu virðisaukaskattsskrár lánardrottins
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278279"
---
# <a name="date-of-vendor-vat-register"></a>Dagsetning VSK-skrár lánardrottins

Í Microsoft Dynamics 365 Finance útgáfa 10.0.24, ný **Dagsetning virðisaukaskattsskrá söluaðila** reiturinn er tiltækur fyrir reikninga lánardrottins. Þessi reitur tilgreinir dagsetningu skattskyldrar afhendingar fyrir kaup.

Til að virkja nýja reitinn, farðu í **Eiginleikastjórnun** vinnusvæði, finndu og veldu **Virkja dagsetningu virðisaukaskattsskrá lánardrottins á reikningum lánardrottins** eiginleiki og veldu síðan **Virkja núna**.

Innkomnir reikningar frá birgjum þínum geta haft tvær dagsetningar: dagsetninguna þegar seljandinn gaf út reikninginn og dagsetning skattskyldrar afhendingar (þ.e. dagsetningin þegar seljandinn innheimti virðisaukaskatt [VSK] sem ber að greiða). Í sumum tilfellum gætu þessar tvær dagsetningar verið mismunandi.

Hægt er að draga frá innkominni virðisaukaskattsupphæð fyrir innkaupareikning og setja þann reikning á virðisaukaskattsskýrslur síðar, á dagsetningu sem er frábrugðin báðum áðurnefndum dagsetningum. Þessi dagsetning er stjórnað af staðbundnum reglum um frestun á virðisaukaskattsfrádrætti fyrir sumar aðstæður. Það er mismunandi eftir löndum eða svæðum.

Sumar virðisaukaskattsskýrslur, svo sem [VSK Eftirlitsskýrsla](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) í Tékklandi, krefjast þess að dagsetning skattskyldrar afhendingu sé gefin upp fyrir innkaupaskjal. Tilkynna þarf þessa dagsetningu svo skattyfirvöld geti samræmt virðisaukaskattsskýrslu milli mótaðila.

Í Fjármálum er hægt að skilgreina dagsetningar í eftirfarandi reitum:

- **Dagsetning reiknings** – Dagsetningin þegar reikningurinn var gefinn út af birgi.
- **Dagsetning virðisaukaskattsskrár** – Dagsetning frádráttar virðisaukaskattsupphæðar fyrir innkaupareikninginn.
- **Dagsetning virðisaukaskattsskrá söluaðila** – Dagsetning skattskyldrar afhendingar seljanda.
- **Fá skjal dagsetningu** – Dagsetningin þegar þú fékkst reikninginn.

Þessir reitir eru á eftirfarandi síðum:

- Reikningur frá lánardrottni
- Komubók lánardrottins
- Samþykkt á reikningi lánardrottins
- Reikningabók lánardrottins

Eftir að reikningur lánardrottins er bókaður er hægt að skoða dagsetningarnar á **Reikningadagbók** og **Viðskipti söluaðila** síður.
