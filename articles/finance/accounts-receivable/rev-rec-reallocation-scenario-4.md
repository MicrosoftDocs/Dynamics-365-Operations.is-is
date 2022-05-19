---
title: Endurúthlutun tekjuskráningar – Aðstæður 4
description: Þetta efnisatriði fer í gegnum aðstæður endurúthlutunar þar sem lína er fjarlægð úr fyrirliggjandi sölupöntun sem er reikningsfærð að hluta til. Þessar aðstæður leiða til sömu niðurstöðu burtséð frá því hvort línan er fjarlægð úr sölupöntuninni eða fær stöðu afturköllunar.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7d37877e914856baf5e5e38871f5b0b1c1eff526
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725736"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Endurúthlutun tekjuskráningar – Aðstæður 4

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fer í gegnum aðstæður endurúthlutunar þar sem lína er fjarlægð úr fyrirliggjandi sölupöntun sem er reikningsfærð að hluta til. Þessar aðstæður leiða til sömu niðurstöðu burtséð frá því hvort línan er fjarlægð úr sölupöntuninni eða fær stöðu afturköllunar.

Í þessum aðstæðum er valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** stilltur á **Nei** í flipanum **Tekjuskráning** á síðunni **Fjárhagsfæribreytur** (**Tekjuskráning \> Uppsetning \> Fjárhagsfæribreytur**).

[![Valkosturinn Bóka leiðréttingar reiknings á viðskiptakröfur stilltur á Nei.](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Sölupöntun er stofnuð fyrir viðskiptavin US\_SI\_0003. Viðskiptavinurinn er að kaupa fartölvu (vörunúmer S0012), uppsetningarþjónustu (vörunúmer S0001) og þjónustuáætlun fyrir fartölvuna (vörunúmer 0008, „Viðvarandi tækniþjónustu“). Tekjur fyrir fartölvuna og uppsetningarþjónustuna eru skráðar um leið. Tekjum fyrir þjónustuáætlunina verður seinkað og þær skráðar yfir 12 mánaða eins og það er skilgreint af tímabilinu í samningnum.

[![Sölupöntunarlínur fyrir fartölvu, uppsetningarþjónustu og þjónustuáætlun.](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Sölupöntunin er staðfest. Þar sem öll þrjú atriðin voru sett upp fyrir endurúthlutun tekjuupphæðar er tekjuupphæð reiknuð þegar sölupöntun er staðfest. Hægt er að skoða tekjurnar sem verða skráðar á síðunni **Úthlutun á tekjuupphæð** (á síðunni **Sölupöntun**, í aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Tekjuskráning** skal velja **Úthlutun á tekjuupphæð**). Tekjur fyrir fartölvuna verða bókaðar á tekjulykil að upphæð $995,84. Tekjur fyrir uppsetningarþjónustuna verða einnig bókaðar á tekjulykil að upphæð $314,47. Tekjur fyrir þjónustuáætlunina verða bókaðar á frestaðan tekjulykil í upphæð $188,69. Samtala tekjuupphæða verður að vera jöfn samtölu línanna sem voru settar upp til að sækja úthlutun tekjuupphæðar ($1.499,00).

[![Síða úthlutunar á tekjuupphæð.](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Viðskiptavinurinn er reikningsfærður fyrir fartölvunni og þjónustuáætluninni, en ekki fyrir uppsetningarþjónustunni. Eftirfarandi mynd sýnir bókhaldsfærsluna sem er bókuð fyrir reikninginn.

[![Bókhaldsfærsla fyrir sölupöntunina sem er reikningsfærð.](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Færslur bókhaldsfærslna $1.276,94 til viðskiptakrafna. Þar sem þessi reikningur er hins vegar hlutareikningur, eru tekjurnar eða frestuðu tekjurnar auk skatts ekki sömu og upphæð viðskiptakrafa. Mismunur upp á $14,47 er bókaður á millireikning fyrir tekjur hlutareiknings.

Tekjuskráningaráætlun er einnig búin til.

[![Síða tekjuskráningaráætlunar fyrir hlutareikning.](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Síðar ákveður viðskiptavinurinn að kaupa ekki uppsetningarþjónustu. Þessi lína er þar af leiðandi fjarlægð úr sölupöntuninni. Athugið að ekki er hægt að staðfesta sölupöntunina aftur, þar sem aðeins reikningsfærðar línur eru eftir á sölupöntuninni.

[![Sölupöntun eftir að lína fyrir uppsetningarþjónustuna er fjarlægð.](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Þótt ekki sé hægt að staðfesta sölupöntunina er samt sem áður hægt að endurúthluta henni. Í sölupöntuninni skal velja **Endurúthluta verði með nýjum pöntunarlínum** til að opna síðuna **Endurúthluta verði með nýjum pöntunarlínum**. Veljið tvær eftirstandandi sölupöntunarlínur og veljið svo **Uppfæra endurúthlutun**. Dálkurinn **Endurúthlutuð upphæð** sýnir nýja tekjuupphæð fyrir hverja eftirstandandi sölupöntunarlínu.

[![Nýjar tekjuupphæðir á endurúthlutun verðs með nýrri síðu pöntunarlínu.](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Næst skal velja **Væntanlegt fylgiskjal** til að skoða bókhaldsfærslurnar.

[![Bókhaldsfærslur á síðunni Væntanlegt fylgiskjal.](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Á síðunni **Væntanlegt fylgiskjal** bakfæra fimm síðustu línurnar upprunalegri bókhaldsfærslu úr bókuðum reikningi. Fyrstu fjórar línurnar eru nýju bókhaldsfærslurnar sem eru bókaðar fyrir reikninginn. Mikilvægt er að skilja að viðskiptavinurinn fær ekki sendan nýja reikninginn. Eftir Endurúthlutun, skuldar viðskiptavinur enn $1.276,94, sem er upphæðin sem verður að bóka á viðskiptakröfur í nýju bókhaldsfærslunni. Nýju tekjurnar eða frestuðu tekjurnar auk skatts jafngilda $1.276,94. Þar af leiðandi þarf ekki að bóka á millireikning fyrir tekjur hlutareiknings.

Til að ljúka endurúthlutuninni skal velja **Vinna úr**. Bókunardagsetning er færð inn. Eftir að Endurúthlutun er lokið sýnir síðan **Úthlutunar á tekjuupphæð** endurúthlutun verðs fyrir vörurnar tvær sem eru eftir.

[![Verðúthlutun fyrir eftirstandandi vörur á síðunni Úthlutun á tekjuupphæð.](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Tekjuskráningaráætlunin var einnig uppfærð á grunni nýrrar endurúthlutunar á tekjuupphæð. Á sölupöntuninni skal opna síðuna **Tekjuskráningaráætlun**. Áður voru 13 línur fyrir vöru S0008 (12 mánaða áætlun var úthlutað á þessa vöru). Nú eru 39 línur: 13 upprunalegar áætlunarlínur, 13 áætlunarlínur bakfærslu og 13 línur sem byggja á nýju tekjuupphæðinni.

[![Síða uppfærslu tekjuskráningaráætlunar með 39 línum fyrir vöru S0008.](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Þegar **Fylgiskjal** er valið sýnir reikningabókin upprunalega bókhaldsfærsluna. Til að skoða bakfærsluna og nýju bókhaldsfærsluna úr sölupöntuninni skal velja **Leiðréttingar á tekjum** í aðgerðasvæðinu og síðan velja **Fylgiskjal**.

Næst skal opna síðuna **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**), velja viðskiptavin **US\_SI\_0003** og svo **Færslur**. Síðan **Færslur viðskiptavinar** sýnir aðeins upprunalegan reikning (000008) ásamt upprunalegri bókhaldsfærslu. Þar sem valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** er stilltur á **Nei** á síðunni **Fjárhagsfæribreytur** er aðeins fjárhagur uppfærður. Þess vegna eru bakfærðu og uppfærðu bókhaldsfærslurnar ekki sýndar. Athugið að leiðréttar tekjufærslur sem voru stofnaðar í [aðstæðum 3](rev-rec-reallocation-scenario-3.md) eru sýndar.

[![Upprunaleg bókhaldsfærsla á síðunni Viðskiptavinafærslur.](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
