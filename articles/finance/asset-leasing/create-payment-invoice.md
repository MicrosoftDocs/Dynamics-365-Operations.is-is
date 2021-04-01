---
title: Stofna launareikninga
description: Þetta efnisatriði útskýrir hvernig á að stofna mánaðarlega reikninga fyrir leigusamning. Hægt er að stofna reikninga fyrir tiltekna leigusamninga eða nota runuvinnslu til að stofna reikninga fyrir marga leigusamninga.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a8b9457b158afaa32718976a7a97f48411be0e1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241523"
---
# <a name="create-payment-invoices"></a>Stofna launareikninga

[!include [banner](../includes/banner.md)]

Hægt er að stofna mánaðarlega reikninga fyrir tiltekna leigusamninga eða nota runuvinnslu til að stofna reikninga fyrir marga leigusamninga. Eftirfarandi ferli sýnir hvernig á að stofna staka færslu leigugreiðslu þegar kveikt er á færibreytunni **Greiða lánardrottni** á síðunni **Uppsetning leigubókar**.

1. Á síðunni **Samantekt leigu** skal velja leigusamning og síðan **Bækur \> Greiðsluáætlun**.
2. Velja skal greiðsluna sem þarf að inna af hendi og síðan velja **Stofna færslubók**. Þú færð skilaboð um að færslubók hafi verið stofnuð gegn valinni greiðslu.
3. Veldu **Reikningabækur** og veldu reikninginn sem þarf að greiða.
4. Á flipanum **Línur** skal fara yfir bókarfærsluna áður en hún er bókuð í fjárhag.

    > [!NOTE]
    > Sjálfgefið er að reikningslínur lánardrottins sem eru stofnaðar noti bókunarreglu lánardrottins á síðunni **Færibreytur viðskiptaskulda**.

5. Veljið rétta færslubók og veljið svo þann reikning sem þarf að greiða.

    Í þessu dæmi er kveikt á færibreytunni **Greiða lánardrottni** í leigubókinni. Þar af leiðir verður reikningurinn í reikningabókinni. Í hlutanum **Yfirlit** birtist samantekt bókarfærslunnar og hlutinn **Línur** sýnir upplýsingar um raunverulegu færslubókarlínurnar.

    > [!NOTE]
    > Ef slökkt er á færibreytunni **Greiða lánardrottni** eru greiðslubókarfærslur skráðar á síðunni **Eignarleiga** fyrir leigubókina og kerfið stofnar eignaleigufærslu í stað reiknings. Leigugreiðslufærslan verður bókuð á færslubókarheitið sem er tilgreint í svæðinu **Mánaðarleg leigubók**.

6. Eftir að færslan er bókuð er hægt að skoða færsluupplýsingar og bókfært virði leiguskuldbindingar með því að velja **Skuldafærslur** í leigubókinni.

    Í greiðsluáætluninni er merkt í gátreitinn **Færslubók bókuð** og línan sýnir númer reikningabókar. Eftir að búið er að stofna greiðslubók og færslu fyrir þá færslubók verður að bakfæra færsluna áður en hægt er að endurgera hana.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]