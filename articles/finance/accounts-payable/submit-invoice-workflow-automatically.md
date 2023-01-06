---
title: Senda reikninga í verkflæðiskerfi og jafna línur á innhreyfingarskjali afurða
description: Þessi grein útskýrir hvernig á að senda reikninga lánardrottna í verkflæðiskerfið og jafna sjálfkrafa bókaðar línur innhreyfingarskjals afurðar fyrir reikninga lánardrottins.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 960a08eb5e98cac034bbd41335b616ff41bf6fd4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861619"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Senda reikninga í verkflæðiskerfi og jafna línur á innhreyfingarskjali afurða

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að senda reikninga lánardrottna í verkflæðiskerfið og jafna sjálfkrafa bókaðar línur innhreyfingarskjals afurðar fyrir reikninga lánardrottins.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Senda inn reikninga lánardrottins í verkflæðiskerfið og jafna bókaðar innhreyfingarlínur afurða við reikningslínur lánardrottins í bið

Sem hluti af snertilausu reikningsfærsluferli Viðskiptaskulda, er hægt að senda sjálfkrafa inn innfluttan reikning í verkflæðiskerfið. Hægt er að skilgreina ferlið við að senda innflutta reikninga í verkflæðiskerfið í flipanum **Sjálfvirkni reikninga lánardrottins** á síðunni **Færibreytur viðskiptaskulda** (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**). Ferlið „senda í verkflæði“ verður keyrt í bakgrunni, eins oft og gefið er upp (annaðhvort á klukkutímafresti eða daglega).

Þegar reikningar eru sendir sjálfkrafa í verkflæðiskerfið verður að byrja á innfluttum reikningi. Til að tryggja að hægt sé að vinna úr reikningnum frá upphafi til enda án afskipta notandans, þarf að hafa með sjálfvirkt bókunarverk í skilgreiningu verkflæðisins. Reikningar sem eru tengdir innkaupapöntunum og reikningar sem innihalda innkaupategund sem tengist hvorki innkaupapöntun né birgðalínum, er hægt að senda sjálfkrafa inn í verkflæðiskerfið. Reikningar sem eru færðir handvirkt inn verða að vera sendir handvirkt inn í verkflæðiskerfið.

Gildið **Sent inn af** í verkflæðinu er notandakennið sem fært var inn fyrir bakgrunnsverkið **Senda reikninga lánardrottna í verkflæði** á síðunni **Sjálfvirkni ferlis**. Notandinn sem er með þetta notandakenni getur afturkallað reikninginn úr verkflæðiskerfinu eftir þörfum.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Jöfnun innhreyfingarskjala afurða við reikningslínur sem eru með þríhliða jöfnunarreglu

Sem hluti af snertilausu reikningsfærsluferli viðskiptaskulda, er hægt að sjálfkrafa jafna bókuð innhreyfingarskjöl afurðar við reikningslínur. Skilgreina þarf þríhliða jöfnunarreglu fyrir þetta verk. Þessi eiginleiki er í boði ef eiginleikinn **Sjálfvirkni reiknings lánardrottins** hefur verið virkjaður á síðunni **Eiginleikastjórnun**.

Ferlið keyrir þangað til magn jafnaðs innhreyfingarskjals afurðar jafngildir magni reiknings. Margar vöruinnhreyfingar eru hins vegar til staðar fyrir eina reikningslínu og nauðsynlegt er að keyra ferlið mörgum sinnum til að ná magnsamsvörun. Hægt er að tilgreina hámarksfjölda skipta sem kerfið á að reyna að jafna innhreyfingarskjöl afurðar við reikningslínu áður en ákveðið er að vinnslan hafi mistekist. Ferlið verður keyrt í bakgrunni, annaðhvort á klukkutíma fresti eða daglega. 

Hægt er að keyra sjálfvirka jöfnunarferlið sem hluta af ferlinu við að senda reikninga í verkflæðiskerfið. Að öðrum kosti er hægt að keyra það sem sjálfstæðan ferli. Stillingar fyrir ferlið „jafna innhreyfingarskjöl afurðar við reikningslínur“ eru gerðar í flipanum **Sjálfvirkni reikninga lánardrottins** á síðunni **Færibreytur viðskiptaskulda** (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**).

Reikningslínur sem eru með þríhliða jöfnunarreglu, þar sem jafnað innhreyfingarmagn er minna en magn á reikningi, verða teknar með í sjálfvirku jöfnunarferli innhreyfingarskjala.

Til að skoða stöðuna **Síðasta jöfnun** fyrir reikninga sem eru ekki hluti af sjálfvirka ferlinu „senda í verkflæði“, skal opna reikninginn af síðunni **Reikningar lánardrottins**. Þegar reikningurinn er skoðaður eru upplýsingar um prófun jöfnunar uppfærðar. Hægt að uppfæra **Síðasta samsvörunarstaða** sjálfkrafa með **Staðfesta reikningsjöfnun** bakgrunnsverk. Hægt er að skilgreina ferlið sjálfkrafa með því að uppfæra stöðuna **Síðasta samsvörunarstaða** á **Bakgrunnsferli** flipanum á síðunni **Sjálfvirkni ferlis** (**Kerfisstjórnun\> Uppsetning\> Sjálfvirkni ferlis**).

Reikningslína verður útilokuð frá sjálfvirku vinnslunni ef eitthvert eftirfarandi skilyrðanna er uppfyllt:

- Gildið **Staða sjálfvirkrar jöfnunar innhreyfingar** í reikningslínunni er **Tókst ekki**.
- Verið er að nota reikninginn.
- Reikningurinn er í verkflæðiskerfinu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
