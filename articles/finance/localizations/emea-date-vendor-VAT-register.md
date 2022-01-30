---
title: Dagsetning VSK-skrár lánardrottins
description: Þetta efnisatriði veitir upplýsingar um eiginleika til að virkja dagsetningu virðisaukaskattsskrár lánardrottins
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 882d5a8718d819cff80bfa5b86e054a39e9db159
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7991730"
---
# <a name="date-of-vendor-vat-register"></a>Dagsetning VSK-skrár lánardrottins

Í Microsoft Dynamics 365 Finance útgáfa 10.0.24, ný **Dagsetning virðisaukaskattsskrá söluaðila** reiturinn er tiltækur fyrir reikninga lánardrottins. Þessi reitur tilgreinir dagsetningu skattskyldrar afhendingar fyrir kaup.

Til að virkja nýja reitinn, farðu í **Eiginleikastjórnun** vinnusvæði, finndu og veldu **Virkja dagsetningu virðisaukaskattsskrá lánardrottins á reikningum lánardrottins** eiginleiki og veldu síðan **Virkja núna**.

Innkomnir reikningar frá birgjum þínum geta haft tvær dagsetningar: dagsetninguna þegar seljandinn gaf út reikninginn og dagsetning skattskyldrar afhendingar (þ.e. dagsetningin þegar seljandinn innheimti virðisaukaskatt [VSK] sem ber að greiða). Í sumum tilfellum gætu þessar tvær dagsetningar verið mismunandi.

Þú getur dregið frá innkominni virðisaukaskattsupphæð fyrir innkaupareikning og sett þann reikning á virðisaukaskattsskýrslur síðar, á dagsetningu sem er frábrugðin báðum áðurnefndum dagsetningum. Þessi dagsetning er stjórnað af staðbundnum reglum um frestun á virðisaukaskattsfrádrætti fyrir sumar aðstæður. Það er mismunandi eftir löndum eða svæðum.

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

Eftir að reikningur lánardrottins er bókaður er hægt að skoða dagsetningarnar á **Reikningardagbók** og **Viðskipti söluaðila** síður.
