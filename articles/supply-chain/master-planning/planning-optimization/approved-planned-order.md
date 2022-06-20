---
title: Skoða, stjórna og samþykkja áætlaðar pantanir
description: Þessi grein veitir upplýsingar um hvernig á að skoða, stjórna og samþykkja fyrirhugaðar pantanir í áætlanagerð fínstillingu.
author: t-benebo
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22c690222cdb72e2113ea137a05da21f315e5a33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887429"
---
# <a name="view-manage-and-approve-planned-orders"></a>Skoða, stjórna og samþykkja áætlaðar pantanir

[!include [banner](../../includes/banner.md)]

Þessi grein veitir upplýsingar um hvernig á að skoða, stjórna og samþykkja fyrirhugaðar pantanir í áætlanagerð fínstillingu.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Skoða og hafa umsjón með áætluðum pöntunum

Hægt er að skoða og stjórna áætlaðum pöntunum á listasíðu fyrir allar áætlaðar pantanir. Fara á einn af eftirfarandi stöðum eftir því hvaða tegund áætlaðra pantana á að vinna með:

- Aðaláætlanagerð \> Vinnusvæði \> Aðaláætlanagerð
- Áætlanagerð \> Aðaláætlanagerð \> Áætlaðar pantanir.
- Framleiðslustýring \> Framleiðslupantanir \> Áætlaðar framleiðslutillögur
- Innkaup og aðföng \> Innkaupapantanir \> Áætlaðar innkaupapantanir.
- Birgðastjórnun \> Pantanir á innleið \> Áætlaðir flutningar
- Birgðastjórnun \> Pantanir á útleið \> Áætlaðir flutningar

## <a name="view-and-edit-the-status-of-planned-orders"></a>Skoða og breyta stöðu áætlaðra pantana

Hægt er að nota reitinn **Staða** fyrir hverja áætlaða pöntun til að auðvelda að fylgjast með framgangi mála eða breyta því hvernig unnið verður úr áætlaðri pöntun. Eftirfarandi gildi fyrir **Stöðu** eru í boði:

- **Óunnið** – Þegar aðaláætlanagerð býr til áætlaðar pantanir fá þær þessa stöðu. Áætluðum pöntunum sem eru með þessa stöðu verður eytt við næstu áætlunarkeyrslu.
- **Lokið** – Þessi staða gefur til kynna að áætluðu pöntuninni sé lokið. Þegar valið er að staðfesta ekki áætlaða pöntun er hægt að breyta stöðu hennar í *Lokið*. Athugið að kerfið meðhöndlar stöðurnar *Óunnið* og *Lokið* á sama hátt.
- **Samþykkt** – Þessi staða gefur til kynna að áætluð pöntun sé samþykkt til staðfestingar. Ef staðfesta á áætlaða pöntun er hægt að breyta stöðunni í *Samþykkt*. Ef á að geyma breytingarnar sem voru gerðar á áætlaðri pöntun, eða ef áform eru um að staðfesta áætlaða pöntun, skal breyta stöðu hennar í *Samþykkt*. Fyrirhugaðar pantanir sem hafa stöðuna *Samþykktar* teljast fastar og væntanlegar birgðir samkvæmt aðaláætlun. Þeim er þar af leiðandi ekki breytt eða eytt í síðari áætlunarkeyrslum. Til að ná fram þessari hegðun afritar áætlanagerðin áætlaðar pantanir sem eru með stöðuna *Samþykkt* úr gömlu áætlunarútgáfunni yfir í nýja áætlunarútgáfu í aðaláætlanagerðinni. Athugið að áætlaðar pantanir með stöðuna *Samþykkt* teljast eingöngu framboð innan tiltekinnar aðaláætlunar.

Til að breyta stöðu einnar áætlaðrar pöntunar skal [opna einhverja listasíðu áætlaðra pantana](#view-planned-orders), opna pöntunina og síðan fylgja einu af þessum skrefum:

- Á flipanum **Almennt** er gildi reitsins **Staða** breytt.
- Á aðgerðasvæðinu, í flipanum **Áætluð pöntun**, í flokknum **Ferli**, skal velja **Breyta stöðu**.
- Veljið **Samþykkja** á aðgerðarúðunni til að merkja pöntunina sem samþykkta.

Til að breyta stöðu nokkurra áætlaðra pantana samtímis skal [opna einhverja listasíðu áætlaðra pantana](#view-planned-orders), velja gátreitinn fyrir hverja pöntun sem ætlunin er að breyta og því næst fylgja einu af þessum skrefum:

- Á aðgerðasvæðinu, í flipanum **Áætluð pöntun**, í flokknum **Ferli**, skal velja **Breyta stöðu**.
- Veljið **Samþykkja** á aðgerðarúðunni til að merkja pöntunirnar sem samþykktar.

## <a name="approve-planned-orders"></a>Samþykkja tillögur

Samþykki áætlaðra pantana er valfrjálst skref í ferlinu við að búa til staðfesta pöntun úr áætlaðri pöntun.

Eftirfarandi mynd sýnir hvernig hægt er að nota gildið fyrir **Stöðu** sem úthlutað er á hverja áætlaða pöntun til að innleiða samþykktarverkflæði. Til að innleiða samþykktarferli skal stilla gildið fyrir **Stöðu** á handvirkan hátt fyrir hverja áætlaða pöntun eins og lýst var í hlutanum hér á undan.

![Áætlað pöntunarflæði.](media/approved-planned-orders-1.png)

> [!TIP]
> Mælt er með því að breyttar áætlaðar pantanir séu samþykktar. Annars verða breytingarnar hunsaðar og skrifað yfir þær af næstu áætlunarkeyrslu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Staðfesta áætlaðar pantanir](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
