---
title: Endurúthlutun tekjuskráningar – Aðstæður 3
description: Þetta efnisatriði fer í gegnum aðstæður endurúthlutunar þar sem nýrri línu er bætt við fyrirliggjandi, reikningsfærða sölupöntun. Þegar nýrri vöru er bætt við samning er hægt að bæta henni við annaðhvort nýja sölupöntun eða fyrirliggjandi sölupöntun.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4242be761ed170155b70211d99eb5018fb254071
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356174"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Endurúthlutun tekjuskráningar – Aðstæður 3

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fer í gegnum aðstæður endurúthlutunar þar sem nýrri línu er bætt við fyrirliggjandi, reikningsfærða sölupöntun. Þegar nýrri vöru er bætt við samning er hægt að bæta henni við annaðhvort nýja sölupöntun eða fyrirliggjandi sölupöntun. Þessar aðstæður sýna einnig hvað gerist þegar viðskiptakröfur eru uppfærðar vegna endurúthlutunar.

Í þessum aðstæðum er valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** stilltur á **Já** í flipanum **Tekjuskráning** á síðunni **Fjárhagsfæribreytur** (**Tekjuskráning \> Uppsetning \> Fjárhagsfæribreytur**).

[![Valkosturinn Bóka leiðréttingar reiknings á viðskiptakröfur stilltur á Já.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Sölupöntun er stofnuð fyrir viðskiptavin US\_SI\_0003. Viðskiptavinurinn er að kaupa fartölvu (vörunúmer S0012) og þjónustuáætlun fyrir hana (vörunúmer S0008, „Viðvarandi tækniþjónustu“). Tekjur fyrir fartölvuna eru skráðar um leið. Tekjum fyrir þjónustuáætlunina verður seinkað og þær skráðar yfir 12 mánaða eins og það er skilgreint af tímabilinu í samningnum.

[![Sölupöntunarlínur fyrir fartölvu og þjónustuáætlun.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Sölupöntunin er staðfest. Þar sem bæði atriðin voru sett upp fyrir endurúthlutun tekjuupphæðar er tekjuupphæð reiknuð þegar sölupöntun er staðfest. Hægt er að skoða tekjurnar sem verða skráðar á síðunni **Úthlutun á tekjuupphæð** (á síðunni **Sölupöntun**, í aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Tekjuskráning** skal velja **Úthlutun á tekjuupphæð**). Tekjur fyrir fartölvuna verða bókaðar á tekjulykil að upphæð $1.008,01. Tekjur fyrir þjónustuáætlunina verða einnig bókaðar á frestaða tekjulykilinn að upphæð $190,99. Samtala tekjuupphæða verður að vera jöfn samtölu línanna sem voru settar upp til að sækja úthlutun tekjuupphæðar ($1.199,00).

[![Síða úthlutunar á tekjuupphæð.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Sölupöntunin er reikningsfærð að fullu. Eftirfarandi mynd sýnir bókhaldsfærsluna sem er bókuð fyrir reikninginn.

[![Bókhaldsfærsla fyrir sölupöntunina sem er reikningsfærð að öllu leyti.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Tekjuskráningaráætlun er einnig búin til. Eftir að nokkur tími er liðinn eru tveir af mánuðunum með skráðar tekjur fyrir þjónustuáætlunina.

[![Síða tekjuskráningaráætlunar eftir að tveir mánuðir eru liðnir.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Á þessu stigi ákveður viðskiptavinurinn að bæta við uppsetningarþjónustu (vörunúmer S0001). Þessari vöru er bætt við fyrirliggjandi sölupöntunina. Viðskiptavinurinn er beðinn um að staðfesta að hann vilji breyta reikningsfærðri sölupöntun og hann velur **Já**.

[![Sölupöntun eftir að línu fyrir uppsetningarþjónustu er bætt við.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Ef þessi nýja vara er eina breytingin á samningnum fyrir viðskiptavin er hægt að keyra endurúthlutunarferlið. Í sölupöntuninni skal velja **Endurúthluta verði með nýjum pöntunarlínum** til að opna síðuna **Endurúthluta verði með nýjum pöntunarlínum**. Veljið allar sölupöntunarlínur fyrir þessa sölupöntun og svo **Uppfæra endurúthlutun**. Dálkurinn **Endurúthlutuð upphæð** sýnir nýja tekjuupphæð fyrir hverja sölupöntunarlínu.

[![Nýjar tekjuupphæðir á endurúthlutun verðs með nýrri síðu pöntunarlínu.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Næst skal velja **Væntanlegt fylgiskjal** til að skoða bókhaldsfærslurnar. Þar sem valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** er stilltur á **Já** á síðunni **Fjárhagsfæribreytur** eru þessar bókhaldsfærslur bókaðar í fjárhag í gegnum kreditskjal og nýr reikningur verður búinn til í viðskiptakröfur.

[![Bókhaldsfærslur á síðunni Væntanlegt fylgiskjal.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Á síðunni **Væntanlegt fylgiskjal** bakfæra fjórar síðustu línurnar upprunalegri bókhaldsfærslu úr bókuðum reikningi. Fyrstu fimm línurnar eru nýju bókhaldsfærslurnar sem eru bókaðar fyrir reikninginn. Mikilvægt er að skilja að viðskiptavinurinn fær ekki sendan nýja reikninginn. Eftir Endurúthlutun, skuldar viðskiptavinur enn $1.276,94, sem er upphæðin sem verður að bóka á viðskiptakröfur í nýju bókhaldsfærslunni. Jöfnunarskattur og tekjur eða frestaðar tekjur eru samanlagt $995,83 + $188,69 + $77,94 = $1.262,46. Upphæð tekna eða frestaðra tekna hefur breyst vegna endurúthlutunarinnar. Mismunur upp á $14,48 er bókaður á millireikning fyrir tekjur hlutareiknings. Þessi staða verður hreinsuð þegar reikningurinn er bókaður fyrir nýju vörunni sem var bætt við sölupöntunina.

Til að ljúka endurúthlutuninni skal velja **Vinna úr**. Bókunardagsetning er færð inn. Eftir að Endurúthlutun er lokið sýnir síðan **Úthlutunar á tekjuupphæð** endurúthlutun verðs fyrir allar þrjár vörurnar.

[![Verðúthlutun fyrir allar þrjár vörurnar á síðunni Úthlutun á tekjuupphæð.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Tekjuskráningaráætlunin var einnig uppfærð á grunni nýrrar endurúthlutunar á tekjuupphæð. Á sölupöntuninni skal opna síðuna **Tekjuskráningaráætlun**. Áður voru 13 línur fyrir vöru S0008 (12 mánaða áætlun var úthlutað á þessa vöru). Nú eru 39 línur: 13 upprunalegar áætlunarlínur, 13 áætlunarlínur bakfærslu og 13 línur sem byggja á nýju tekjuupphæðinni.

[![Síða uppfærslu tekjuskráningaráætlunar með 39 línum fyrir vöru S0008.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Þegar **Fylgiskjal** er valið sýnir reikningabókin upprunalega bókhaldsfærsluna. Til að skoða bakfærsluna og nýju bókhaldsfærsluna úr sölupöntuninni skal velja **Leiðréttingar á tekjum** í aðgerðasvæðinu og síðan velja **Fylgiskjal**.

Næst skal opna síðuna **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**), velja viðskiptavin **US\_SI\_0003** og svo **Færslur**. Síðan **Færslur viðskiptavinar** sýnir upprunalegan reikning (000006), bakfærsluskjalið (000006-1) og nýja reikninginn (000006-2). Upprunalegi reikningurinn og bakfærsluskjalið eru jöfnuð á móti hvort öðru og eru með stöðuna 0 (núll). Skoðið fylgiskjal fyrir hvert skjal til að sjá áhrif í fjárhag.

[![Upprunalegur reikningur, bakfærsluskjal og nýr reikningur á síðunni Færslur viðskiptavinar.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Sölupöntunin er reikningsfærð aftur vegna vörunnar sem bætt var við. Heildarreikningurinn sem viðskiptavinurinn fær hljóðar upp á $300,00 + $19,50 í skatt = $319,50. Eftirfarandi mynd sýnir bókhaldsfærsluna sem er bókuð.

[![Síða fylgiskjalsfærsla með bókhaldsfærslu sem er bókuð.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Vegna þess að samtala tekna og sölu er meiri en $319,50 er mismunurinn bókaður fyrir -$14,48. Þessi upphæð hreinsar stöðuna úr tekjum millireiknings. Sú staða var uppfærð í nýju bókhaldsfærslunni sem var bókuð eftir endurúthlutun.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]