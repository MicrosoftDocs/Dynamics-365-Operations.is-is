---
title: Endurúthlutun tekjuskráningar – Aðstæður 2
description: Þessi grein fjallar um endurúthlutun þar sem tvær sölupantanir eru færðar inn og viðskiptavinurinn bætir atriði við samninginn eftir að fyrsta sölupöntunin er reikningsfærð. Þegar nýrri vöru er bætt við samning er hægt að bæta henni við annaðhvort nýja sölupöntun eða fyrirliggjandi sölupöntun.
author: bking
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5f8dac2991b309bb91faaa3107480ca3860af008
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348382"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Endurúthlutun tekjuskráningar – Aðstæður 2

[!include [banner](../includes/banner.md)]

Þessi grein fjallar um endurúthlutun þar sem tvær sölupantanir eru færðar inn og viðskiptavinurinn bætir atriði við samninginn eftir að fyrsta sölupöntunin er reikningsfærð. Þegar nýrri vöru er bætt við samning er hægt að bæta henni við annaðhvort nýja sölupöntun eða fyrirliggjandi sölupöntun.

Í þessum aðstæðum er valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** stilltur á **Nei** í flipanum **Tekjuskráning** á síðunni **Fjárhagsfæribreytur** (**Tekjuskráning \> Uppsetning \> Fjárhagsfæribreytur**).

[![Valkosturinn Bóka leiðréttingar reiknings á viðskiptakröfur stilltur á Nei.](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Sölupöntun er stofnuð fyrir viðskiptavin US\_SI\_0003. Viðskiptavinurinn er að kaupa uppsetningarþjónustu (vörunúmer S0001) og þjónustuáætlun (vörunúmer S0008) fyrir fartölvu, en hann hefur ekki enn valið fartölvuna. Tekjum uppsetningarþjónustunnar verður frestað fram að þeim degi þegar fartölvan er keypt. Tekjum fyrir þjónustuáætlunina verður seinkað og þær skráðar yfir 12 mánaða eins og það er skilgreint af tímabilinu í samningnum.

[![Sölupöntunarlínur fyrir uppsetningarþjónustu og þjónustuáætlun.](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Sölupöntunin er staðfest. Þar sem bæði atriðin voru sett upp fyrir endurúthlutun tekjuupphæðar er tekjuupphæð reiknuð þegar sölupöntun er staðfest. Hægt er að skoða tekjurnar sem verða skráðar á síðunni **Úthlutun á tekjuupphæð** (á síðunni **Sölupöntun**, í aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Tekjuskráning** skal velja **Úthlutun á tekjuupphæð**). Tekjur fyrir uppsetningarþjónustuna verða bókaðar á frestaðan tekjulykil í upphæð $250,00. Tekjur fyrir þjónustuáætlunina verða einnig bókaðar á frestaðan tekjulykil að upphæð $150,00. Samtala tekjuupphæða verður að vera jöfn samtölu línanna sem voru settar upp til að sækja úthlutun tekjuupphæðar ($400,00).

[![Síða úthlutunar á tekjuupphæð.](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Sölupöntunin er reikningsfærð að fullu. Eftirfarandi mynd sýnir bókhaldsfærsluna sem er bókuð fyrir reikninginn.

[![Bókhaldsfærsla fyrir sölupöntunina sem er reikningsfærð að öllu leyti.](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Tekjuskráningaráætlunin er einnig búin til, en engar tekjur eru skráðar enn sem komið er.

[![Síða tekjuskráningaráætlunar.](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Nokkrum dögum síðar velur viðskiptavinurinn fartölvu. Önnur sölupöntun er færð inn fyrir viðskiptavininn.

[![Sölupöntunarlína fyrir fartölvuna.](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Seinni sölupöntunin er staðfest. Þar sem þessi sölupöntun inniheldur aðeins eina línu fer úthlutun tekjuverðs ekki fram þegar sölupöntunin er staðfest. Úthlutun tekjuupphæðar á sér aðeins stað ef um er að ræða tvær eða fleiri einkvæmar vörur og ef þær eru settar upp fyrir úthlutun tekjuupphæðar.

Ef þessi nýja sölupöntun er eina breytingin á samningi viðskiptavinar er hægt að keyra endurúthlutunarferlið. Í annarri sölupöntuninni skal velja **Endurúthluta verði með nýjum pöntunarlínum** til að opna síðuna **Endurúthluta verði með nýjum pöntunarlínum**. Einnig er hægt að fara í **Tekjuskráning \> Reglubundin verk \> Endurúthluta verði með nýjum pöntunarlínum**. Veljið tvær eftirstandandi sölupöntunarlínur og samsvarandi sölupöntunarlínur og veljið svo **Uppfæra endurúthlutun**. Dálkurinn **Endurúthlutuð upphæð** sýnir nýja tekjuupphæð fyrir hverja sölupöntunarlínu.

[![Nýjar tekjuupphæðir á endurúthlutun verðs með nýrri síðu pöntunarlínu.](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Næst skal velja **Væntanlegt fylgiskjal** til að skoða bókhaldsfærslurnar sem aðeins verða bókaðar í fjárhag. Þar sem valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** er stilltur á **Nei** á síðunni **Fjárhagsfæribreytur** er engu breytt í viðskiptakröfum þegar endurúthlutun fer fram.

[![Bókhaldsfærslur á síðunni Væntanlegt fylgiskjal.](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Á síðunni **Væntanlegt fylgiskjal** bakfæra þrjár síðustu línurnar upprunalegri bókhaldsfærslu úr bókuðum reikningi. Fyrstu fjórar línurnar mynda nýja bókhaldsfærslu sem er bókuð fyrir reikninginn. Mikilvægt er að skilja að viðskiptavinurinn fær ekki sendan nýja reikninginn. Eftir Endurúthlutun, skuldar viðskiptavinur enn $426,00, sem er upphæðin sem verður að bóka á viðskiptakröfur í nýju bókhaldsfærslunni. Jöfnunarskattur og frestaðar tekjur eru samanlagt $188,69 + $314,48 + $26,00 = $529,17. Upphæð frestaðrar tekjufærslu hefur breyst vegna endurúthlutunarinnar. Mismunur upp á $103,17 er bókaður á millireikning fyrir tekjur hlutareiknings. Þessi staða verður hreinsuð þegar reikningur er bókaður fyrir seinni sölupöntunina sem var tekin með í endurúthlutuninni.

Til að ljúka endurúthlutuninni skal velja **Vinna úr**. Beðið er um bókunardagsetningu jafnvel þótt ekkert hafi verið bókað. Þegar endurúthlutuninni er lokið sýnir síðan **Úthlutun á tekjuupphæð** fyrir hverja sölupöntun úthlutunarupphæðina fyrir allar vörur í báðum sölupöntununum. Síðan **Úthlutun á tekjuupphæð** fyrir hverja sölupöntun mun sem sagt innihalda vöru sem er ekki til í þeirri sölupöntun vegna þess að hún er hluti af sama samningnum en í annarri sölupöntun.

> [!TIP]
> Til að setja í samhengi af hverju þessar vörur eru sýndar er hægt að bæta öðrum dálkum við hnitanetið, t.d. **Kenni endurúthlutunar** og **Sölupöntun**.
> 
> [![Viðbótardálkar á síðunni Úthlutun tekjuupphæðar.](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

Í sölupöntun 00036 var tekjuskráningaráætlunin einnig uppfærð á grunni nýrrar endurúthlutunar á tekjuupphæð. Á þessari sölupöntun skal opna síðuna **Tekjuskráningaráætlun**. Áður voru 13 línur fyrir vöru S0008 (12 mánaða áætlun var úthlutað á þessa vöru). Nú eru 39 línur: 13 upprunalegar áætlunarlínur, 13 áætlunarlínur bakfærslu og 13 línur sem byggja á nýju tekjuupphæðinni.

[![Síða uppfærslu tekjuskráningaráætlunar með 39 línum fyrir vöru S0008.](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Sömuleiðis voru áður tvær línur fyrir vöru S0001 en nú eru þær sex.

[![Síða uppfærslu tekjuskráningaráætlunar með sex línum fyrir vöru S0001.](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Þegar **Fylgiskjal** er valið í sölupöntun 000036 sýnir reikningabókin upprunalega bókhaldsfærsluna. Til að skoða bakfærsluna og nýju bókhaldsfærsluna úr sölupöntuninni skal velja **Leiðréttingar á tekjum** í aðgerðasvæðinu og síðan velja **Fylgiskjal**.

[![Sölupöntun 000036.](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Næst skal opna síðuna **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**), velja viðskiptavin **US\_SI\_0003** og svo **Færslur**. Opni reikningur af sölupöntun 000036 verður sýndur. Ef þú velur fylgiskjalið birtist upprunalega bókhaldsfærslan, ekki nýja bókhaldsfærsla endurúthlutunarinnar. Ekki er hægt að skoða bakfærsluna og nýju bókhaldsfærsluna úr viðskiptakröfum.

Seinni sölupöntunin hefur verið reikningsfærð. Heildarreikningurinn sem viðskiptavinurinn fær hljóðar upp á $1.099,00 + $71,44 í skatt = $1.170,44. Eftirfarandi mynd sýnir bókhaldsfærsluna sem er bókuð.

[![Síða fylgiskjalsfærsla með bókhaldsfærslu sem er bókuð.](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Vegna þess að samtala tekna og sölu er meiri en $1.170,44 er mismunurinn bókaður fyrir -$130,17. Þessi upphæð hreinsar stöðuna úr tekjum millireiknings. Þessi staða er bókuð í nýju bókhaldsfærslunni eftir endurúthlutun.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
