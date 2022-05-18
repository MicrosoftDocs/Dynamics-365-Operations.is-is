---
title: Staðgreiðsluskattur í innkaupafærslum
description: Fyrir lánardrottna sem þurfa að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefna **Staðgreiðsluskattsflokknum** á síðunni **Allir lánardrottnar**.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727203"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Staðgreiðsluskattur í innkaupafærslum

Fyrir lánardrottna sem þurfa að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefna **Staðgreiðsluskattsflokknum** á síðunni **Allir lánardrottnar**.

1. Farið í **Yfirlitssvæði > Einingar > Viðskiptaskuldir > Lánardrottnar > Allir lánardrottnar**.

2. Smellið á tilheyrandi lánardrottnalykil og smellið á **Breyta**.

3. Í flipanum **Reikningsfæra og afhenda** skal stilla reitinn **Reikna staðgreiðsluskatt** á **Já**.

   > [!NOTE] 
   > Staðgreiðsluskattur verður ekki reiknaður ef ekki er kveikt á **Reikna staðgreiðsluskatt** fyrir þennan lánardrottin í gögnunum.

4. Veljið flokk staðgreiðsluskatts í **Staðgreiðsluskattsflokkur**.

5. Smellt er á **Vista**.

Fyrir vörur/þjónustu þar sem þarf að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki vöru** í **Útgefnar afurðir**.

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.

2. Smellið á viðkomandi vörunúmer og smellið á **Breyta**.

3. Í flipanum **Innkaup** skal smella á **Reikna staðgreiðsluskatt**.

   > [!NOTE] 
   > Staðgreiðsluskattur verður ekki reiknaður ef **Reikna staðgreiðsluskatt** er ekki stillt á **Já** fyrir þessa vöru í flipanum **Innkaup** á síðunni **Útgefin afurð**.

4. Veljið staðgreiðsluskattflokk vöru úr listanum **Staðgreiðsluskattsflokkur**.

5. Smellt er á **Vista**.

Hægt er að úthluta staðgreiðsluskattsflokkum og staðgreiðsluskattflokkum vöru á síður: 

- **Innkaupapöntun**
- **Reikningur frá lánardrottni**
- **Reikningabók**

Sjálfgefinn staðgreiðsluskattsflokkur og staðgreiðsluskattflokkur vöru verða færðir inn í línurnar þegar **Innkaupapantanir** og/eða **Reikningar frá lánardrottni í bið** eru stofnaðir. Fyrir **Reikningabók lánardrottins** er hægt að kveikja á **Reikna staðgreiðsluskatt** og velja **Staðgreiðsluskattflokk vöru** í flipanum **Almennt** í færslubókinni.

Tímabundin upphæð staðgreiðsluskatts er í boði í reitnum **Leiðréttur staðgreiðsluskattur** í flipanum **Samtölur** á síðunni **Innkaupapöntun**.

![Staðgreiðsluskattur er hafður með í innkaupapöntuninni.](media/withholding-tax-adjusted.png)

Staðgreiðsluskattur er reiknaður í **Greiðslubók lánardrottins**. Hægt er að leiðrétta viðeigandi staðgreiðsluskattskóða handvirkt rétt eins og raunverulegum upphæðum staðgreiðsluskatts í flipanum **Staðgreiðsluskattur** á síðunni **Jafna færslur**.

![Staðgreiðslu er hægt að leiðrétta handvirkt á síðu færslujöfnunar.](media/withholding-tax-vendor-payment-tab.png)

Afleidd upphæð staðgreiðsluskatts verður dregin frá lánardrottnagreiðslunni og bókuð í **Staðgreiðsluskattslykli** í tengdu fylgiskjali.

![Staðgreiðsluskattslykill sem sýnir tengt fylgiskjal.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
