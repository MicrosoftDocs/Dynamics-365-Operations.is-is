---
title: Röðun samstæðu
description: Þetta efnisatriði útskýrir samstæðuröðun
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e28051097905503e291e0c15a50e9363b39b2daa
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548332"
---
# <a name="intercompany-master-scheduling"></a>Röðun samstæðu

[!include [banner](../../includes/banner.md)]

Aðalröðun samstæðu er sú aðferð sem notuð er þegar þarfir eru reiknaðar og áætlaðar samstæðupantanir útbúnar á milli nokkurra samstæðufyrirtækja. Aðalröðun samstæðu er framkvæmd fyrir fjölda ítrekana sem tilgreindur er. Til að Microsoft Dynamics 365 Supply Chain Management framkvæmi aðalröðun samstæðu verður að setja upp aðalröðun í öllum samstæðufyrirtækjum. Það leiðir af sér fjölda ítrekana þar sem Microsoft Dynamics 365 Supply Chain Management útbýr sjálfkrafa samstæðuinnkaupapöntun sem aftur leiðir til sjálfvirkrar stofnunar á samstæðusölupöntun sem aftur leiðir af sér nýja eftirspurn.

Aðaláætlun og aðalröðun fyrir samstæðu eru settar upp í færibreytum fyrir **Aðaláætlanagerð** í hverju samstæðufyrirtæki.

Til að ná yfir eftirspurn í allri samstæðunni þarf að stilla færibreytur svo tryggt sé að áætlaðar innkaupapantanir séu sjálfkrafa staðfestar; þ.e. ekki er hægt að breyta pöntunum hvað varðar magn. Settu upp **Tímamörk staðfestingar** í þekjuflokknum eða **Tímamörk staðfestingar** í aðaláætluninni. Ef engin **Tímamörk staðfestingar** eru sett upp eru engar samstæðuinnkaupapantanir stofnaðar sjálfkrafa. Aðeins fyrsta framkvæmd aðaláætlanagerðar leiðir til áætlaðra pantana. En vegna þess að engin samstæðuinnkaupapöntun er stofnuð, engin samstæðusölupöntun er stofnuð og þar af leiðandi eru engar fleiri samstæðuinnkaupapantanir stofnaðar og svo framvegis.

Þegar aðalröðun samstæðu er keyrð framkvæmir Microsoft Dynamics 365 Supply Chain Management aðeins eina aðalröðun í hverju samstæðufyrirtæki og framkvæmir svo aðra aðalröðun í hverju samstæðufyrirtæki, o.s.frv, þar til ákveðnum fjölda ítrekana er náð. Að hámarki eru 30 ítrekanir mögulegar en því fleiri ítrekanir sem eru valdar aftur á móti þeim mun lengri tíma tekur röðunin.

Þar sem aðalröðun innan fyrirtækis er stjórnað af röð aðalröðunar, þ.e. af þeirri röð sem forritið forgangsraðar aðalröðun á milli samstæðufyrirtækja er hægt að hefja aðalröðun samstæðu frá hvaða samstæðufyrirtæki sem er. Þar sem röð samstæðuaðalröðunar ákvarðar í hvaða röð aðalröðun er framkvæmd innan fyrirtækja skiptir litlu máli hvar aðalröðun samstæðu hefst. Við hverja ítrekun er gildandi fyrirtæki það síðasta í röðinni.

> [!NOTE]
> Besta leiðin er að leyfa aðalröðun samstæðu að hefjast frá einu Microsoft Dynamics 365 Supply Chain Management fyrirtæki.

Á síðunni **Samstæðuröðun** er hægt að hefja röð aðalröðunar þar sem aðalröðun er framkvæmd í fyrsta sinn með uppfærslureglum fyrir þarfaútreikning sem valdar hafa verið fyrir fyrstu ítrekun fyrir öll samstæðufyrirtækin. Síðari ítrekanir nota aukareglu sem valin er fyrir næstu ítrekun og þeirri reglu er beitt þar til þeim fjölda ítrekana sem tilgreindur er hefur verið náð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
