---
title: Afkastaaukning fyrir virkjun lykilskipulags
description: Í þessari grein er ný afkastaaukning fyrir virkjunarferli lykilskipulags útskýrð.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/22/2022
ms.locfileid: "9714000"
---
# <a name="account-structure-activation-performance-enhancement"></a>Afkastaaukning fyrir virkjun lykilskipulags

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Þessi afkastaaukning gerir notanda kleift að virkja lykilskipulag hraðar með því að keyra margar færsluuppfærslur samtímis. Að auki er skipulagið sjálft merkt sem virkt eftir að það hefur verið sannprófað og úrvinnsla færslna getur haldið áfram á meðan óbókaðar færslur eru uppfærðar í nýja skipulagið. Þar sem uppfærslur á færslum geta tekið nokkurn tíma er hægt að fylgjast með stöðu virkjunarinnar með því að velja **Sjá virkjunarstöðu** fyrir ofan hnitanetið á síðunni **Lykilskipulag**. Einnig er hægt að sjá virkjunarstöðuna með því að velja **Skoða** á aðgerðarúðunni og velja síðan **Virkjunarstaða** á fellivalmyndinni.

[![Síðan Lykilskipulag.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Eftir að **Sjá virkjunarstöðu** er valið birtist svargluggi sem sýnir einstök verk sem eru í gangi sem hluti af virkjunarferlinu. Fyrir hvert verk er hægt að skoða stöðuna og, eftir að verkinu er lokið, dagsetningu og tíma verkloka.

[![Tímalína virkjunar lykilskipulags.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Ráð um virkjun lykilskipulags

Virkjunargluggi lykilskipulags sem birtist þegar **Virkja** er valið fyrir drög að lykilskipulagi er með flipahluta með heitinu **Uppfæra óbókaðar færslur**. Í þessum hluta er valkostur sem er nefndur **Þvinga uppfærslu**. Hægt er að velja þennan valkost til að uppfæra allar óbókaðar færslur í núverandi skipulag. Hins vegar ætti aðeins að nota þennan valkost þegar villa hefur komið upp eða notendaþjónusta Microsoft hefur bent þér á að nota hann.

Hér eru nokkrir af þeim þáttum sem geta haft áhrif á afköst virkjunarferlisins:

- Margar óbókaðar bókarfærslur
- Mikill fjöldi skjala í opnum hugbúnaði, svo sem reikningar með frjálsum texta, reikningar lánardrottna og tengd skjöl, sem nota rammann fyrir upprunaskjöl og eru með opnar dreifingar á fjárhagsupphæðum
- Gagnamagn í TaxUncommitted
- Magn opinna fjárhagsáætlunargagna
- Innflutningur færslubókargagna meðan virkjunarverk eru enn í gangi

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
