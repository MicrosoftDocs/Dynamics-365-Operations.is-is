---
title: Skoða niðurstöður sjálfvirkni reiknings lánardrottins (forskoðun)
description: Þetta efnisatriði útskýrir hvernig á að skoða stöðu reikninga lánardrottna sem eru í sjálfvirka verkflæðisferlinu.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 872ec404da0cce41c4ea0f882a3fa8af56316ce3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837226"
---
# <a name="view-vendor-invoice-automation-results"></a>Skoða niðurstöður sjálfvirkni reiknings lánardrottins

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að skoða stöðu reikninga lánardrottna sem eru í sjálfvirka verkflæðisferlinu. Upplýsingum um sjálfvirkniferilinn er haldið við fyrir hvern innfluttan lánardrottnareikning. Það fer eftir viðskiptaferlunum sem voru gerðir sjálfvirkir, hvað síðan **Reikningar frá lánardrottni í bið** sýnir í gildunum **Staða sjálfvirkrar jöfnunar innhreyfingar** og **Staða sjálfvirkrar innsendingar í verkflæði**. Hægt er að skoða upplýsingarnar og gera áætlun um að einbeita sér að reikningunum sem tókust ekki í sjálfvirku skrefi. Eftir að vandamálið hefur verið lagað er hægt að halda áfram með sjálfvirka ferlið fyrir innfluttan reikning.

Áður en hægt er að breyta reikningi sem hefur verið sendur inn, verður að gera hlé á sjálfvirku vinnslunni. Ef gera verður hlé á sjálfvirkri innsendingu í verkflæði skal stilla reitinn **Hafa með í sjálfvirkri vinnslu** á **Nei** á síðunni **Reikningar frá lánardrottni**. Sjálfvirkni keyrir þá ekki fyrr en reiturinn **Hafa með í sjálfvirkri vinnslu** er stilltur á **Já**. Hægt er að gera hlé á reikningi frá frekari sjálfvirkni ef hann er ekki enn í verkflæðiskerfinu og er ekki notaður af sjálfvirka ferlinu.

Ef innfluttur reikningur er sendur í verkflæðisferlið er hægt að skoða gildið **Staða sjálfvirkni** á síðunni **Reikningar frá lánardrottni**. Eftirfarandi stöður eru raktar:

- **Tekið með** – Sjálfvirku ferlin sem eru skilgreind á síðunni **Færibreytur viðskiptaskulda** keyra á réttan hátt en þeim er enn ekki lokið.
- **Gert hlé** – Sjálfvirku ferlin sem eru skilgreind á síðunni **Færibreytur viðskiptaskulda** hafa verið keyrð, en að minnsta kosti eitt skref í ferlinu tókst ekki. Staðan **Gert hlé** er einnig notuð ef reiturinn **Hafa með í sjálfvirkri vinnslu** er stilltur á **Nei**. Hægt er að skoða bilanirnar með því að velja **Skoða nýjustu niðurstöður**.
- **Í verkflæði** - Innfluttur reikningur hefur verið sendur í verkflæðiskerfið, annaðhvort af sjálfvirkri innsendingu í verkflæðisferli eða handvirkt.
- **Verkflæði lokið** – Verkflæðisferlinu hefur verið lokið fyrir innfluttan reikning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]