---
title: Uppsetningarvalkostir fyrir sjálfvirkni reiknings lánardrottins (forskoðun)
description: Í þessu efnisatriði er lýst valkostunum sem eru tiltækir til að setja upp og skilgreina sjálfvirkni reikninga lánardrottins.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ebab41d8b7697f20095d6d4654718b88c8b08a82
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665199"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Uppsetningarvalkostir fyrir sjálfvirkni reiknings lánardrottins

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst valkostunum sem eru tiltækir til að setja upp og skilgreina sjálfvirkni reikninga lánardrottins. Eiginleikar fyrir sjálfvirkni reiknings nota eftirfarandi gerðir af færibreytum uppsetningar:

- Færibreytur fyrir innsendingu reikninga lánardrottins í verkflæðiskerfið og jafna bókaðar innhreyfingarlínur afurða við reikningslínur lánardrottins í bið.
- Færibreytur fyrir vinnslu á sjálfvirkum bakgrunnsverkum. Sjálfvirknirammi ferlisins er notaður til að senda innflutta lánardrottnareikninga í verkflæðiskerfið. Hann er einnig notaður til að jafna sjálfkrafa bókaðar línur innhreyfingarskjals afurðar við reikningslínur lánardrottins í bið og til að villuleita reikningsjöfnun fyrir handvirka reikninga sem voru sjálfkrafa jafnaðir við línu innhreyfingarskjals afurðar. Mismunandi viðskiptaferlar nota þennan ramma til að skilgreina hversu oft valið ferli er keyrt. Tíðni sem er í boði fyrir bakgrunnsvinnslurnar **Jafna innhreyfingarskjal afurðar við reikningslínur** og **Senda reikninga lánardrottna í verkflæði** eru **Klukkustund** og **Daglega**.

Til að setja upp eða skoða upplýsingar um bakgrunnsverk skal fara í **Kerfisstjórnun \> Uppsetning \> Sjálfvirkni ferlis** og velja flipann **Bakgrunnsverk**.

Til að ná snertilausri sjálfvirkni úr innflutningsferlinu í gegnum bókun lánardrottnareiknings, þarf að setja upp verkflæði lánardrottnareiknings. Til að setja upp verkflæði skal fara í **Viðskiptaskuldir > Uppsetning > Færibreytur fyrir viðskiptaskuldir**. Til að tryggja að hægt sé að vinna úr reikningnum frá upphafi til enda án afskipta notandans, þarf að hafa með sjálfvirkt bókunarverk í skilgreiningu verkflæðisins.

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Færibreytur fyrir innsendingu á innfluttum reikningum lánardrottins í verkflæðiskerfið

Sérstakar færibreytur eru notaðar til að senda inn innflutta reikninga lánardrottins í verkflæðiskerfið. Að auki eru sumar færibreytur notaðar til að jafna bókaðar línur innhreyfingarskjals við línur lánardrottnareiknings í bið. Í flipanum **Sjálfvirkni reikninga lánardrottins** á síðunni **Færibreytur viðskiptaskulda**, eru færibreyturnar sem þarf að stilla skipt á milli eftirfarandi hluta:

- Verkflæði lánardrottnareiknings
- Jafna innhreyfingarskjöl afurða sjálfkrafa

Eftirfarandi færibreytur eru tiltækar:

- **Senda innflutta reikninga sjálfkrafa í verkflæði** - Ef þessi valkostur er stilltur á **Já**, eru innfluttir reikningar sjálfkrafa sendir inn í verkflæðiskerfið. Ef þessi valkostur er stilltur á **Nei** verða reikningar að vera sendir handvirkt. Með því að stilla þennan valkost á **Já** er snertilaust ferli virkjað fyrir útkomu innflutnings í gegnum bókun.

    Hægt er að stilla þennan valkost á **Já** aðeins ef verkflæði virks lánardrottnareiknings er sett upp fyrir lögaðilann. Til að setja upp verkflæði skal fara í **Viðskiptaskuldir \> Uppsetning \> Verkflæði viðskiptaskulda**.

- **Jafna innhreyfingarskjöl afurða við reikningslínur áður en sent er inn sjálfkrafa** - Ef þessi valkostur er stilltur á **Já**, er ekki hægt að senda innfluttan reikning sjálfkrafa í verkflæðiskerfið fyrr en jafnað magn innhreyfingarskjals samsvarar reikningsmagninu. Með því að stilla þenna valkost á **Já** er virkjuð sjálfvirk jöfnun á bókuðu innhreyfingarskjali við reikningslínur sem þríhliða jöfnunarregla er skilgreind fyrir. Þetta ferli keyrir þangað til magn jafnaðs innhreyfingarskjals afurðar jafngildir magni reiknings. Á þeim tímapunkti er reikningur sjálfkrafa sendur í verkflæðiskerfið.

    Valkosturinn fyrir „Jafna innhreyfingarskjöl afurða við reikningslínur áður en sent er inn sjálfkrafa“ er aðeins í boði ef valkosturinn **Gera villuprófun á reikningsjöfnun virka** er valinn. Þegar þessi valkostur er valinn mun valkosturinn **Jafna sjálfkrafa innhreyfingarskjöl afurða við reikningslínur** verða valinn sjálfkrafa.

- **Krefjast þess að útreiknaðar samtölur jafngildi innfluttum samtölum fyrir sjálfvirkri innsendingu í verkflæði** - Ef þessi valkostur er stilltur á **Já**, er ekki hægt að senda reikninginn sjálfkrafa inn í verkflæðiskerfið fyrr en samtölurnar sem eru reiknaðar fyrir reikninginn jafngilda innfluttum samtölum. Ef þessi valkostur er stilltur á **Nei**, er sjálfkrafa hægt að senda reikninginn í verkflæðiskerfið, en ekki er hægt að bóka hann fyrr en útreiknaðar samtölur eru leiðréttar þannig að þær stemmi við innfluttar samtölur. Ef reikningsupphæðin eða upphæð virðisaukaskatts er ekki flutt inn, á að stilla þennan valkost á **Nei**.
- **Jafna sjálfkrafa innhreyfingarskjöl afurða við reikningslínur** - Ef þessi valkostur er stilltur á **Já**, verður hægt að nota bakgrunnsvinnslur til að gera sjálfvirka jöfnun á bókuðum innhreyfingarskjölum við reikningslínur sem þríhliða jöfnunarregla er skilgreind fyrir. Þetta ferli keyrir þangað til magn jafnaðs innhreyfingarskjals afurðar jafngildir magni reiknings, eða þar til gildinu í reitnum **Fjöldi skipta sem á að reyna sjálfvirka jöfnun** er náð. Hægt er að keyra ferlið þar til reikningur hefur verið sendur inn í verkflæðiskerfið.

    Þessi reitur er aðeins í boði ef valkosturinn **Gera villuprófun á reikningsjöfnun virka** er valinn.

    Ef valkosturinn **Jafna innhreyfingarskjöl afurða við reikningslínur á undan sjálfkrafa jöfnun** er stilltur á **Já**, verður ekki hægt að stilla þennan valkost á **Nei**. Til að stilla þennan valkost á **Nei** þarf fyrst að stilla valkostinn **Jafna innhreyfingarskjöl afurða við reikningslínur á undan sjálfkrafa jöfnun** á **Nei**.

- **Fjöldi skipta sem á að reyna sjálfvirka jöfnun** - Veljið hversu oft kerfið á að reyna að jafna innhreyfingarskjöl afurða við reikningslínu áður en ákveðið er að vinnslan hafi mistekist. Þegar tilteknum fjölda tilrauna er náð er reikningurinn fjarlægður úr sjálfvirka ferlinu.

