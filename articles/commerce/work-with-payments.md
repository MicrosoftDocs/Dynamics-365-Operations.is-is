---
title: Greiðslumátar í símaverum
description: Þetta efnisatriði lýsir hinum ýmsu greiðslumátum sem hægt er að nota í símaveri Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8fede81aa8c61eddba72b9ba2e780d61731f8253
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989253"
---
# <a name="payment-methods-in-call-centers"></a>Greiðslumátar í símaverum

[!include [banner](includes/banner.md)]

Í Dynamics 365 Commerce inniheldur grunnstilling á rás símavers stillingu sem er kölluð **Virkja lok pöntunar**. Þessi stilling hjálpar til við að tryggja að allar pantanir sem notendur rásar búa til séu gefnar út til úrvinnslu pantana aðeins ef fyrirframgreiðsla eða fyrirframheimiluð greiðsla er til staðar sem er innan heimilaðra vikmarka. Ef kveikt er á stilllingunni **Virkja lok pöntunar** geta notendur símavers fært inn greiðslur gagnvart sölupöntun fyirr viðskiptavini með því að nota eiginleika greiðsluvinnslu símavers. Ef slökkt er á stillingunni geta notendur símavers ekki notað eiginleika greiðsluvinnslu, en þeir geta samt sem áður notað fyrirframgreiðslur á sölupöntunum með því að nota virknina venjulegar viðskiptakröfur.

Sem hluti af rásarstillingunni getur fyrirtæki skilgreint greiðslumáta sem eru heimilaðir fyrir rás símavers. Rás símavers notar sömu greiðslumátana og eru skilgreindir fyrir rásir verslunar.

Til að stilla greiðslumáta fyrir rás símavers skal fara í **Retail og Commerce** \> **Rásir** \> **Símaver** \> **Öll símaver** og síðan í valmyndinni **Setja upp** skal velja valkostinn **Greiðslumáti**.

Þegar greiðslumáti er búinn til eru fimm aðgerðir greiðslumáta sem hægt er að úthluta.

| Aðgerð            | lýsing |
|---------------------|-------------|
| Venjulegt              | Notaðu aðgerðina **Venjulegur** á greiðslumátanum þínum þegar þú skilgreinir greiðslumáta eins og reiðufé eða fylgiskjal. Þegar þessar tegundir greiðslna eru notaðar á sölupöntun í símaverinu mun flaggið **Fyrirframgreiða** að sjálfgefnu verða **Já**. Þetta mun um leið bóka fylgiskjal fyrirframgreiðslu á viðskiptavinalykil þegar þessi pöntun er send inn. Notendur geta breytt flagginu **Fyrirframgreiða** í **Nei** ef þess er óskað svo að fylgiskjal greiðslunnar er ekki búið til fyrr en við bókun reiknings. Fylgiskjal fyrirframgreiðslunnar er bókað í ferli viðskiptavinafærslu þar sem það mun vera kerfisbundið jafnað á móti reikningi sölupöntunarinnar. |
| Merkja               | Notaðu aðgerðina **Ávísun** þegar bankaávísun er skilgreind sem greiðslumáti. Þegar þessi tegund greiðslu er notuð í sölupöntun verður notandinn að færa inn ávísananúmer viðskiptavinar sem hluta af greiðslujöfnunarferlinu. Ávísanagreiðslur eru alltaf meðhöndlaðar sem fyrirframgreiðslur þegar þær eru notaðar og fylgiskjöl greiðslu eru búin til strax við innsendingu pöntunar. Þessi fylgiskjöl fyrirframgreiðslna verða kerfisbundið jöfnuð á móti reikningum sem eru búnir til fyrir pöntunina. |
| Kort               | Gerðir kortagreiðslna eiga við um hvers konar greiðslu sem krefst innsláttar kortanúmers sem hefur verið skilgreint á greiðslukorti viðskiptavinar. Dæmi eru kreditkort og gjafakort. Þegar þessar tegundir greiðslna eru stilltar þarf að nota valmyndina **Kortuppsetning** til að skilgreina kenni korts sem tengjast þessum greiðslumáta. Við pöntunarfærslu geta notendur tekið fram hvort kortagreiðslan verði fyrirframgreiðsla með því að nota valkostinn **Fyrirframgreiða** sem birtist á síðu greiðslufærslu. Nema viðskiptin krefjast fyrirframgreiðslna, er dæmigert flæði réttrar kreditkortagreiðslu ferli í tveimur skrefum, þar sem heimild er fengin við pöntunarfærslu og síðan er greiðsla afgreidd og innheimt frá kort viðskiptavinar þegar kemur að reikningsfærslu. Fyrir greiðslur með gjafakorti er mælt með fyrirframgreiðslu vegna þess að staða gjafakorts ætti að minnka strax svo viðskiptavinurinn geti ekki notað sama virðið einhvers staðar annars staðar. |
| Viðskiptavinur            | Aðgerðin **Viðskiptavinur** á greiðslumáta gefur í skyn að greiðslan verði jöfnuð við lánamark viðskiptavinar eða sett á „reikning“. Í Commerce er hægt að úthluta viðskiptavini lánamati sem hægt er að sannprófa við pöntunarfærslu. Greiðslur sem eru gerðar með því að nota greiðslumáta sem tengist aðgerðinni **Viðskiptavinur** skapar skuld á móti reikningi viðskiptavinari. Þegar sölupöntunin er reikningsfærð birtist gjaldfallin staða. Í þessum tilvikum senda viðskiptavinir venjulega greiðslur samkvæmt skilmálum sem hafa verið gefnir. Að öðrum kosti er hægt að nota áður opið inneignaskjal á reikningi viðskiptavinar til að jafna á móti gjaldfallinni stöðu. Athugaðu að jafnvel þótt þú skilgreinir þennan greiðslumáta birtist hann ekki í vali á greiðslumöguleikum í pöntunarfærslu símavers nema að flaggið **Leyfa á reikningi** sé stillt á viðskiptavinafærslu fyrir viðskiptavininn sem þú ert að vinna með. Þetta flagg er að finna í flipanum **Sjálfgefnar greiðslur** í færslu viðskiptavinar. |
| Fjarlægja skiptimynt | Aðgerðin **Fjarlægja skiptimynt** er ekki notuð af símaverinu. Það gildir aðeins þegar þú skilgreinir greiðslumáta sem forrit sölustaðar notar í rás verslunar. |

Úr því að greiðslumátar eru skilgreindir, eiga þeir að tengjast við fjárhag eða bankareikning. Ef þú sleppir þessu skrefi munu notendur fá upp villur þegar þeir reyna að vista greiðslugerð.

## <a name="refund-payment-methods"></a>Endurgreiðslumátar

Fyrir úrvinnslu á endurgreiðslum notar símaverið einnig suma greiðslumátana sem eru skilgreindir í viðskiptakröfum. Til að stilla þessa greiðslumáta skaltu fara í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning símavers** \> **Endurgreiðslumátar símavers**. Þú verður að ljúka þessum stillingum til að afgreiða endurgreiðsluávísanir til viðskiptavina. Til dæmis, ef viðskiptavinur sem upphaflega greiddi fyrir pöntun með því að nota reiðufé eða ávísun, gæti notandinn viljað senda viðskiptavininum endurgreiðsluávísun í gegnum viðskiptakröfur. Í þessu tilfelli verður að varpa greiðslumáta reiðufés og ávísunar í símaveri á réttan greiðslumáta í viðskiptakröfum til að tryggja að endurgreiðslan sé rétt afgreidd.

Að auki, ef notandi er að vinna úr skilapöntun sem notandi símavers í Commerce, en getur ekki tengt skilin við upprunalega sölu verður greiðslumátinn fyrir **Skila** að vera stilltur í færibreytum símavers. Farðu í **Retail og Commerce** \> **Uppsetning rásar** \> **Uppsetning símavers** \> **Færibreytur símavers** og síðan á flipanum **RMA/Skila** í reitnum **Greiðslumáti** skal tryggja að greiðslumáti sé skilgreindur. Greiðslumátinn verður greiðslumátinn sem er notaður fyrir endurgreiðslur. Venjulega verður hann skilgreindur sem annaðhvort prófunaraðferð eða aðferð viðskiptavinalykils.
