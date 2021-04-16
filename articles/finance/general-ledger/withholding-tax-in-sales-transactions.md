---
title: Staðgreiðsluskattur í sölufærslum
description: Þetta efnisatriði sýnir skrefin til að komast hjá útreikningi staðgreiðsluskatts fyrir valda viðskiptavini. Fyrir viðskiptavini sem tilgreina staðgreiðsluskatt í greiðslum til þín, er hægt að úthluta sjálfgefnum staðgreiðsluskattsflokki.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842345"
---
# <a name="withholding-tax-in-sales-transactions"></a>Staðgreiðsluskattur í sölufærslum

Þetta efnisatriði sýnir skrefin til að komast hjá útreikningi staðgreiðsluskatts fyrir valda viðskiptavini. Fyrir viðskiptavini sem tilgreina staðgreiðsluskatt í greiðslum til þín, er hægt að úthluta sjálfgefnum **Staðgreiðsluskattsflokki** á síðunni **Viðskiptavinir**. 

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