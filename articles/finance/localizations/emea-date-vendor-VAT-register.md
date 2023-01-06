---
title: Dagsetning VSK-skrár lánardrottins
description: Þessi grein veitir upplýsingar um eiginleika til að virkja dagsetningu fyrir VSK-skrá lánardrottins.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278279"
---
# <a name="date-of-vendor-vat-register"></a>Dagsetning VSK-skrár lánardrottins

Í Microsoft Dynamics 365 Finance-útgáfu 10.0.24 er nýr reitur **Dagsetning VSK-skrár lánardrottins** í boði fyrir lánardrottnareikninga. Þessi reitur tilgreinir dagsetningu skattskylds framboðs fyrir innkaup.

Til að virkja nýja reitinn skal fara á vinnusvæðið **Eiginleikastjórnun**, finna og velja eiginleikann **Virkja dagsetningu VSK-skráar lánardrottins í lánardrottnareikningum** og síðan velja **Virkja núna**.

Reikningar á innleið frá birgjum geta verið með tvær dagsetningar: dagsetninguna þegar lánardrottinn gaf út reikninginn og dagsetningu skattskyldra birgða (þ.e. dagsetningin þegar lánardrottinn innheimti skuld virðisaukaskatts [VSK]) Í sumum tilvikum gætu þessar tvær dagsetningar verið frábrugðnar.

Þú getur dregið frá VSK-upphæð á innleið fyrir innkaupareikning og haft þann reikning í VSK-skýrslum síðar á dagsetningu sem er önnur en báður dagsetningarnar sem minnst var á. Þessari dagsetningu er stýrt af staðbundnum reglum um frestaðan frádrátt á virðisaukaskatti fyrir sumar aðstæður. Það er mismunandi eftir löndum eða svæðum.

Sumar VSK-skýrslur, t.d. [Skýrsla VSK-stýringar](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) í Tékklandi krefjast þess að dagsetning skattskyldra birgða sé gefin upp fyrir innkaupaskjal. Tilkynna verður um þessa dagsetningu svo að skattayfirvöld geti stemmt af VSK-skýrsluna á milli mótaðila.

Í Finance er hægt að skilgreina dagsetningar í eftirfarandi reitum:

- **Reikningsdagsetning** – Dagsetningin þegar birgir gaf út reikninginn.
- **Dagsetning VSK-skráar** – Dagsetning frádráttar VSK-upphæðar fyrir innkaupareikninginn.
- **Dagsetning VSK-skráar lánardrottins** – Dagsetning skattskyldra birgða lánardrottins.
- **Móttökudagsetning skjals** – Dagsetningin þegar þú fékkst reikninginn.

Þessir reitir eru á eftirfarandi síðum:

- Reikningur frá lánardrottni
- Komubók lánardrottins
- Samþykkt á reikningi lánardrottins
- Reikningabók lánardrottins

Eftir að reikningur lánardrottins er bókaður geturðu yfirfarið dagsetningarnar á síðunum **Reikningabók** og **Lánardrottnafærslur**.
