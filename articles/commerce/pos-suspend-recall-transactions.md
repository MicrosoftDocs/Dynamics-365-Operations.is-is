---
title: Gera hlé á og halda áfram með færslu á sölustaðnum (POS)
description: Þessi grein útskýrir hvernig notendur geta stöðvað viðskipti sem eru í gangi og síðan haldið þeim áfram síðar eða á annarri skrá með því að nota Dynamics 365 Commerce.
author: josaw1
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.industry: Retail
ms.openlocfilehash: 0b85bdb043e0bffed83ad6ffcb9269773c89facf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269082"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Gera hlé á og halda áfram með færslu á sölustaðnum (POS)

[!include [banner](includes/banner.md)]


Notendur sölustaðar (POS) geta gert hlé á færslum í vinnslu og síðan haldið áfram með þær seinna eða á öðrum afgreiðslukassa. Oft er gert hlé á færslum til að losa afgreiðslukassa á fljótlegan hátt fyrir annað verk án þess að glata núverandi færslu. Til dæmis byrjar aðili tengdur verslun að vinna með færslu viðskiptavinar á fartæki en verður að klára færsluna á afgreiðslukassa sem er með peningaskúffu. Í þessu tilfelli getur aðili tengdur verslun gert hlé á færslunni á fartækinu og síðan kallað hana aftur fram og haldið áfram með hana á afgreiðslukassa.

## <a name="configure-suspend-and-resume-functionality"></a>Skilgreina virkni frestunar og áframhalds

### <a name="pos-operations"></a>POS-aðgerðir

Tvær [POS-aðgerðir](pos-operations.md) leyfa sölustað að styðja við atburðarásir frestunar og áframhalds. Þú getur úthlutað þessum aðgerðum til [hnappahnita](pos-screen-layouts.md) á færslusíðunni eða upphafssíðunni.

- 503: Fresta færslu
- 504: Endurheimta færslu

### <a name="receipt-template"></a>Sniðmát kvittunar

Hægt er að grunnstilla sölustaðinn til að búa til prentaðan strimil þegar færslu er frestað. Þennan strimil er hægt að nota til að bera strax kennsl á og endurheimta færslu seinna meir.

Til að gera sölustað kleift að prenta strimil verður þú að bæta kvittunarsniðinu **Frestuð færsla** við forstillingu kvittunar fyrir verslun. Þú getur hannað kvittunarsniðið þannig að það innihaldi eða útiloki tilteknar upplýsingar um færsluna. Til dæmis getur sniðið innihaldið strikamerki til að bjóða upp á skönnun.

### <a name="receipt-numbering"></a>Númer kvittunar

Hvað varðar aðrar POS-færslugerðir sem búa til prentaða kvittun, getur þú skilgreint númeraröð fyrir frestaðar færslur í hlutanum **Númerun kvittana** í virknireglu verslunar.

### <a name="void-when-closing-shift"></a>Ógild við lok vaktar

Þú getur notað valkostinn **Ógilda við lok vaktar** svo notendur verði að ljúka við eða ógilda allar frestaðar færslur áður en þeir loka vaktinni. Á meðan aðgerðin **Loka vakt** stendur yfir mun sölustaðurinn biðja notendur um að annaðhvort skoða eða ógilda allar útistandandi frestaðar færslur.

## <a name="suspend-and-resume-a-transaction"></a>Fresta og endurheimta færslu

### <a name="suspend-a-transaction"></a>Fresta færslu

Notendur sem hafa nægar heimildir og sem eru með skjáútlit sem felur í sér aðgerðina **Fresta færslu** geta frestað færslu þannig að hægt sé að endurheimta hana seinna eða ná í hana á öðrum afgreiðslukassa.

Aðeins er hægt að fresta færslum ef þær innihalda **ekki** eftirfarandi gerðir af línum:

- Virkar greiðslulínur
- Línur gjafakorts (annaðhvort til að gefa út gjafakort eða bæta á stöðu gjafakorts)

Frestuð færsla hefur ekki áhrif á söluupplýsingar eða upplýsingar um birgðaframboð fyrir verslunina.

### <a name="resume-a-suspended-transaction"></a>Halda áfram með frestaða færsla

Hvaða notandi sem er með nægar heimildir getur endurheimt og haldið áfram með frestaðar færslur í sömu verslun, og sem er einnig með útlit sem inniheldur aðgerðina **Endurheimta færslu**.

Til að auðveldlega endurheimta frestaða færslu skal skanna strikamerkið á prentaða strimlinum þegar listi yfir færslur er skoðaður úr aðgerðinni **Endurheimta færslu**.

### <a name="considerations-for-offline-mode"></a>Hvað skal hafa í huga ef utan nets

- Öllum þeim færslum sem er frestað í sölustað með nettengingu er ekki hægt að halda áfram með utan nets vegna þess að gögnin eru ekki samstillt við ótengdan gagnagrunn.
- Ef þú frestar færslu í sölustað utan nets er hægt að ná í hana aftur án nettengingar, svo lengi sem sölustaðurinn hafi ekki verið færður aftur í nettengdan ham einhvern tímann eftir að færslunni var frestað. Þegar sölustaðurinn er færður aftur í nettengdan ham er gögn um frestaðar færslur flutt aftur í nettengdan gagnagrunn og þeim eytt úr ótengdum gagnagrunni. Þar af leiðandi er aðeins hægt að halda áfram með færslur í nettengdum ham. Ef sölustaðurinn er færður aftur í ótengdan ham verður ekki hægt að halda áfram með þessar frestuðu færslur vegna þess að þær hafa þegar verið fjarlægðar úr ótengda gagnagrunninum.

### <a name="void-a-suspended-transaction"></a>Ógilda frestaða færslu

Hægt er að ógilda frestaðar færslur annaðhvort með því að endurheimta færsluna og framkvæma síðan aðgerðina **Ógilda færslu** eða með því að velja færsluna í listanum **Endurheimta færslu** og velja **Ógilda** á forritastikunni. Að öðrum kosti er hægt að stilla verslunina til að biðja notendur um ógilda frestaðar færslur þegar þeir loka vaktinni.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
