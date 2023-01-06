---
title: Nota fyrirframgreiðslur sjálfkrafa í reikningum lánardrottins
description: Þessi grein útskýrir möguleikann á að nota fyrirframgreiðslur sjálfkrafa á reikninga lánardrottins.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 547573d187460a900df7f4927ac062bd9d456729
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900072"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Nota sjálfkrafa á reikninga lánardrottins

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir möguleikann á að nota fyrirframgreiðslur sjálfkrafa á reikninga lánardrottins. Hægt er að stofna fyrirframgreiðslu fyrir innkaupapöntun sem hluta af innkaupasamningi. Eftir að reikningur lánardrottins hefur borist er hægt að nota fyrirframgreiðsluna til að gera upp viðskiptaskuldina í reikningi lánardrottins. Nýi eiginleikinn gerir kerfinu kleift að nota sjálfkrafa innkaupapöntunarnúmer á reikningi lánardrottins til að fletta upp samsvarandi fyrirframgreiðslum þegar reikningur lánardrottins er fluttur inn.

Ef fyrirframgreiðslur finnast og hægt er að nota þær er línum bætt við fyrirliggjandi reikningslínur til að nota fyrirframgreiðslurnar. Fyrirframgreiðslulínurnar eru aldrei teknar til greina meðan á reikningsjöfnunarferlinu stendur.

Eftirfarandi atriði lýsa því hvernig staðgreiðslur eru notaðar þegar mismunandi innkaupaferlum er fylgt:

- **Einn lánardrottnareikningur á hverja innkaupapöntun** – Fyrirframgreiðslan á innkaupapöntuninni verður notuð í reikning lánardrottins.
- **Einn lánardrottnareikningur á margar innkaupapantanir** – Fyrirframgreiðslurnar á öllum innkaupapöntunum verða notaðar í reikning lánardrottins.
- **Margir lánardrottnareikningar á hverja innkaupapöntun** – Fyrirframgreiðslan á innkaupapöntuninni verður notuð í fyrsta innflutta reikning lánardrottins. Ef upphæð fyrirframgreiðslu er hærri en reikningsupphæðin mistekst fyrirframgreiðslan og nota verður hana handvirkt.
- **Margir lánardrottnareikningar fyrir margar innkaupapantanir** – Fyrirframgreiðslurnar á innkaupapöntunum verða notaðar í fyrsta viðeigandi reikningnum. Ef upphæð fyrirframgreiðslu er hærri en reikningsupphæðin mistekst fyrirframgreiðslan og nota verður hana handvirkt. Ef einhverjar fyrirframgreiðslur eru eftir þegar fyrirframgreiðslur eru notaðar er hægt að nota þær á reikninga sem á eftir koma.

Ef reynt að nota fyrirframgreiðslu en notkun mistekst, fara næstu skref eftir stillingu á valkostinum **Loka fyrir sjálfvirkan eftirfylgniferil ef notkun fyrirframgreiðslu mistekst**:

- **Já** – Villuboðin „Sjálfvirk notkun fyrirframgreiðslu: Mistókst“ er bætt við í sjálfvirkniferlinum og reikningurinn er áfram á listanum yfir reikninga lánardrottins sem eru í bið. Reikningurinn verður áfram útilokaður þar til þú notar fyrirframgreiðsluna handvirkt.

Farðu á lánardrottnareikning í bið til að nota fyrirframgreiðslur handvirkt. Á síðunni **Reikningsupplýsingar** skal stilla valkostinn **Hafa með í sjálfvirkri vinnslu** fyrir útilokaðan reikning á **Nei**. Nú er hægt að nota fyrirframgreiðsluna handvirkt. Eftir að fyrirframgreiðslan hefur verið notuð skaltu stilla valkostinn **Hafa með í sjálfvirkri vinnslu** aftur á **Já** svo hægt sé að vinna úr reikningnum sjálfkrafa.

Þú getur sneitt framhjá sjálfvirkri notkun fyrirframgreiðslu með því að stilla valkostinn **Hafa með í sjálfvirkri vinnslu** á **Nei** og síðan stilla hann aftur á **Já**. Þú færð eftirfarandi skilaboð: „Fyrirframgreiðsla er þegar til staðar fyrir innkaupapöntunina. Á að hunsa þetta fyrir valinn reikning lánardrottins? Velja skal **Já**. Skilaboðunum „Notkun fyrirframgreiðslu sleppt handvirkt“ er bætt við í sjálfvirkniferlinum og reikningur lánardrottins verður ekki útilokaður þegar sjálfvirka ferlið er keyrt aftur.

- **Nei** – Eftirfylgni sjálfvirkniferla mun halda áfram. Enn er hægt að nota fyrirframgreiðsluna við jöfnun.
