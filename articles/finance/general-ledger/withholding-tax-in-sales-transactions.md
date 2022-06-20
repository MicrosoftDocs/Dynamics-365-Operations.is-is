---
title: Staðgreiðsluskattur í sölufærslum
description: Þessi grein sýnir skrefin til að forðast útreikning á staðgreiðslu fyrir valda viðskiptavini. Fyrir viðskiptavini sem tilgreina staðgreiðsluskatt í greiðslum til þín, er hægt að úthluta sjálfgefnum staðgreiðsluskattsflokki.
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
ms.openlocfilehash: 75a7fc62c1d493007f3aa88a723465828c557df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910085"
---
# <a name="withholding-tax-in-sales-transactions"></a>Staðgreiðsluskattur í sölufærslum

Þessi grein sýnir skrefin til að forðast útreikning á staðgreiðslu fyrir valda viðskiptavini. Fyrir viðskiptavini sem tilgreina staðgreiðsluskatt í greiðslum til þín, er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki** á síðunni **Viðskiptavinir**. 

1. Farið í **Yfirlitssvæði > Einingar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.

2. Smellið á tilheyrandi viðskiptavinalykil og smellið á **Breyta**.

3. Í flipanum **Reikningsfæra og afhenda** skal stilla reitinn **Reikna staðgreiðsluskatt** á **Já**.

   > [!NOTE] 
   > Staðgreiðsluskattur verður ekki reiknaður ef ekki er kveikt á **Reikna staðgreiðsluskatt** fyrir þennan viðskiptavin í aðalgögnunum.

4. Veljið flokk staðgreiðsluskatts í **Staðgreiðsluskattsflokkur**.

5. Smellt er á **Vista**.

Fyrir vörur/þjónustu þar sem þarf að greiða staðgreiðsluskatt er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki vöru** í **Útgefnar afurðir**.

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.

2. Smellið á viðkomandi vörunúmer og smellið á **Breyta**.

3. Í flipanum **Selja** skal smella á **Reikna staðgreiðsluskatt**.

   > [!NOTE] 
   > Staðgreiðsluskattur verður ekki reiknaður ef **Reikna staðgreiðsluskatt** er ekki stillt á **Já** fyrir þessa vöru í flipanum **Selja** á síðunni **Útgefin afurð**.

4. Veljið staðgreiðsluskattflokk vöru úr listanum **Staðgreiðsluskattsflokkur**.

5. Smellt er á **Vista**.

Hægt er að úthluta staðgreiðsluskattsflokkum og staðgreiðsluskattflokkum vöru með því að nota síðuna **Sölupöntun**. 

Sjálfgefinn staðgreiðsluskattsflokkur og staðgreiðsluskattflokkur vöru verða notaðir sem sjálfgefnar færslur í sölupöntunarlínum þegar ný sölupöntun er stofnuð.

Staðgreiðsluskattur er reiknaður og bókaður með **Greiðslubók viðskiptavinar**. Hægt er að leiðrétta viðeigandi staðgreiðsluskattskóða handvirkt rétt eins og raunverulega upphæð staðgreiðsluskatts í flipanum **Staðgreiðsluskattur** á síðunni **Jafna færslur**.

Reiknuð upphæð staðgreiðsluskatts verður dregin frá lánardrottnagreiðslunni og bókuð í **Mótlykli staðgreiðsluskatts** í tengdu fylgiskjali.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
