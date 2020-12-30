---
title: Yfirlit yfir vinnuflæði áskrifta
description: Þetta efnisatriði veitir yfirlit yfir vinnuflæði áskrifta.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f023ddd8d6f9350702f687763b53b057baa9aed8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430285"
---
# <a name="subscription-workflow-overview"></a>Yfirlit yfir vinnuflæði áskrifta 

[!include [banner](../includes/banner.md)]


Þú ert umsjónarmaður áskrifta fyrir ljósafyrirtæki sem býður upp á áskriftir fyrir viðhald á ljósabúnaði. Viðskiptavinur hefur samband við fyrirtækið þitt til að kaupa árlega áskrift fyrir viðhald á ljósabúnaði.

## <a name="setting-up-subscriptions"></a>Áskriftir settar upp

Til að setja upp áskrift verður þú fyrst að búa til áskriftarflokk fyrir nýja þjónustusamninginn eða staðfesta að áskriftarflokkurinn sé til staðar. Ef áskriftarflokkur er til staðar verður þú að setja hann upp til að reikningsfæra viðskiptavininn árlega og til að safna upp sölutekjum fyrir hvern mánuð ársins. Nánari upplýsingar um hvernig á að setja upp áskriftir er að finna í [Setja upp áskriftarflokka](set-up-subscription-groups.md).

Þegar áskriftarhópur hefur verið stofnaður er hægt að stofna áskrift. Nánari upplýsingar um hvernig á að búa til þjónustuáskriftir, sjá [Búa til þjónustuáskriftir út frá áskriftarflokki](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Búðu til og breyttu áskriftarfærslum

Eftir að þú hefur sett upp áskriftina stofnarðu færslu áskriftargjalds fyrir fyrsta reikningsfærslutímabilið, sem er eitt ár. Færslurnar eru af gerðinni **Venjulegt**. Þ.a.l. er aðeins hægt að búa til áskriftarfærslu þar sem dagsetning frá og dagsetning til samsvara tímabilunum sem áður voru búin til í skjámyndinni **Tímabilsgerðir**. Nánari upplýsingar um þóknunarfærslur, sjá [Þóknunarfærslur áskriftar](create-subscription-fee-transactions.md).

Eftir að þú hefur sett upp áskriftina fyrir viðskiptavininn þinn, manstu eftir því að þeir hafa samið um 10 prósent afslátt á öllum listaverðum fyrir þjónustuframboð. Þess vegna verður þú að draga úr verði þóknunarfærslu sem þú bjóst til.

Síðar um daginn hringir tengiliður viðskiptavinarins að þótt þeir vilji enn þjónustusamninginn fyrir ljósabúnaðinn er á stefnuskránni að kynna til sögunnar nýjan ljósabúnað seinna á árinu. Þess vegna þurfa þeir aðeins að tryggja viðhald þar til í október 2013. Til að draga úr fjölda mánaða fyrir áskrift viðskiptavinarins býrðu til nýja þóknunarfærslu áskriftar af gerðinni **Minnkunardagar**. Nánari upplýsingar um hvernig á að fækka dögum, sjá [Fækka dögum á áskrifargjöldum](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Reikningsfæra og safna saman áskriftarfærslum

Þú hefur nú lokið við að setja upp áskriftina og þú ert tilbúin(n) til að reikningsfæra viðskiptavininn fyrir henni. Frekari upplýsingar um hvernig á að reikningsfæra áskriftir er að finna í [Reikningsfæra áskriftarfærslur](invoice-subscription-transactions.md).

Tveimur dögum síðar hringir viðskiptavinurinn að segja þér að áskriftin skuli reikningsfærð í Bandaríkjadölum, ekki evrum. Þess vegna stofnarðu kreditnótu og einnig stofnarðu nýja áskriftarfærslu í réttum gjaldmiðli. Nánari upplýsingar um hvernig á að fá kreditfæra áskriftarfærslur er að finna í [Kreditfæra áskriftarfærslur](credit-subscription-transactions.md).

Í lok hvers mánaðar má safna upp mánaðartekjum frá áskrift viðskiptavinar yfir á rekstrarreikning og VÍV-reikning. Nánari upplýsingar um hvernig á að safna tekjum vegna áskriftar er að finna í [Safna upp áskriftartekjum](accrue-subscription-revenue.md).

  


