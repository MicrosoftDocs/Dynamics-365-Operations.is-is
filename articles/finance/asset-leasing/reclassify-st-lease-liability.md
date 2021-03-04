---
title: Endurflokka skammtímahluta leiguskuldbindingar
description: Þetta efnisatriði útskýrir hvernig á að stofna mánaðarlega færslubókarfærslu til að endurflokka hluta af leiguskuldbindingunni sem skammtíma.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444574"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Endurflokka skammtímahluta leiguskuldbindingar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna mánaðarlega færslubókarfærslu til að endurflokka hluta af leiguskuldbindingunni sem skammtíma. Þegar áætlunin sem er valin í runuvinnslunni er **endurflokkun skammtíma leiguskuldbindingar** er færslubókarfærsla stofnuð. Þessi færsla er notuð til að bóka núverandi hluta leiguskuldarinnar á síðasta degi mánaðarins. Á sama tíma er bakfærsla bókuð frá fyrsta degi næsta mánaðar.

Skammtímahluti leiguskuldbindingar er sýndur í afskriftaráætlun skuldar. Þegar færslubókarfærslan er bókuð verður dálkurinn **Endurflokkunarbók skuldar stofnuð** tiltækur og færslubókarkennið er einnig fyllt út í áætluninni.

Til að stofna og bóka færslu í endurflokkunarbók skammtímaskuldar skal fylgja þessum skrefum.

1. Opnið **Eignarleiga \> Reglubundið \> Stofnun runubókar**.
2. Í svarglugganum **Stofnun runubókar**, á svæðinu **Velja áætlun** skal velja **Endurflokkun skuldbindingar skammtímaleigu**.
3. Í reitnum **Leigusamningsflokkur** skal velja leigusamningsflokk. Einnig er hægt að velja bókarkennið í reitnum **Bókarkenni** .
4. Kveikja skal á færibreytunni **Bóka**. Einnig er hægt að stofna færsluna en ekki bóka hana með því að hafa slökkt á þessari færibreytu.
5. Kveikja skal á færibreytunni **Forskoða fyrir bókun** til að skoða færsluna áður en hún er bókuð.
6. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]