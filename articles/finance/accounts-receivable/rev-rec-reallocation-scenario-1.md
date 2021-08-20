---
title: Endurúthlutun tekjuskráningar – Aðstæður 1
description: Þetta efnisatriði fjallar um endurúthlutun þar sem tvær sölupantanir eru færðar inn, en báðar eru aðeins staðfestar. Sömu aðstæður leiða til svipaðrar niðurstöðu ef fleiri en tvær sölupantanir eru með staðfesta stöðu.
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
ms.openlocfilehash: d63082553f8625a9953b0a85d59a4949a37c92770ce2a41a43d78cf0266f3b85
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770714"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Endurúthlutun tekjuskráningar – Aðstæður 1

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fjallar um endurúthlutun þar sem tvær sölupantanir eru færðar inn, en báðar eru aðeins staðfestar. Sömu aðstæður leiða til svipaðrar niðurstöðu ef fleiri en tvær sölupantanir eru með staðfesta stöðu.

Í þessum aðstæðum er valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** stilltur á **Nei** í flipanum **Tekjuskráning** á síðunni **Fjárhagsfæribreytur** (**Tekjuskráning \> Uppsetning \> Fjárhagsfæribreytur**).

[![Valkosturinn Bóka leiðréttingar reiknings á viðskiptakröfur stilltur á Nei.](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Sölupöntun er stofnuð fyrir viðskiptavin US\_SI\_0003. Viðskiptavinurinn er að kaupa fartölvu (vörunúmer S0012) og þjónustuáætlun fyrir hana (vörunúmer S0008, „Viðvarandi tækniþjónustu“). Tekjur fyrir fartölvuna eru strax skráðar (engin tekjuskráningaráætlun er til staðar). Tekjum fyrir þjónustuáætlunina verður seinkað og þær skráðar yfir 12 mánaða eins og það er skilgreint af tímabilinu í samningnum.

[![Sölupöntunarlínur fyrir fartölvu og þjónustuáætlun.](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Sölupöntunin er staðfest. Þar sem bæði atriðin voru sett upp fyrir endurúthlutun tekjuupphæðar er tekjuupphæð reiknuð þegar sölupöntun er staðfest. Hægt er að skoða tekjurnar sem verða skráðar á síðunni **Úthlutun á tekjuupphæð** (á síðunni **Sölupöntun**, í aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Tekjuskráning** skal velja **Úthlutun á tekjuupphæð**). Tekjur fyrir fartölvuna verða bókaðar á tekjulykil að upphæð $1.008,01. Tekjur fyrir þjónustuáætlunina verða einnig bókaðar á frestaða tekjulykilinn að upphæð $190,99. Samtala tekjuupphæða verður að vera jöfn samtölu línanna sem voru settar upp til að sækja úthlutun tekjuupphæðar ($1.199,00).

[![Síða úthlutunar á tekjuupphæð.](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Viðskiptavinurinn kaus að kaupa ekki uppsetningarþjónustu (vörunúmer S0001) á þeim tíma sem salan var gerð en skipti síðan um skoðun. Því er önnur sölupöntun er færð inn fyrir sama viðskiptavin.

[![Sölupöntunarlína fyrir uppsetningarþjónustu.](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Seinni sölupöntunin er staðfest. Þar sem þessi sölupöntun inniheldur aðeins eina línu fer úthlutun tekjuverðs ekki fram þegar sölupöntunin er staðfest. Úthlutun tekjuupphæðar á sér aðeins stað ef um er að ræða tvær eða fleiri einkvæmar vörur og ef þær eru settar upp fyrir úthlutun tekjuupphæðar.

Ef þessi nýja sölupöntun er eina breytingin á samningi viðskiptavinar er hægt að keyra endurúthlutunarferlið. Í annarri sölupöntuninni skal velja **Endurúthluta verði með nýjum pöntunarlínum** til að opna síðuna **Endurúthluta verði með nýjum pöntunarlínum**. Einnig er hægt að fara í **Tekjuskráning \> Reglubundin verk \> Endurúthluta verði með nýjum pöntunarlínum**. Veljið tvær eftirstandandi sölupöntunarlínur og samsvarandi sölupöntunarlínur og veljið svo **Uppfæra endurúthlutun**. Dálkurinn **Endurúthlutuð upphæð** sýnir nýja tekjuupphæð fyrir hverja sölupöntunarlínu.

[![Nýjar tekjuupphæðir á endurúthlutun verðs með nýrri síðu pöntunarlínu.](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Ef **Væntanlegt fylgiskjal** er valið birtist ekkert, þar sem engir reikningar hafa verið bókaðir.

Til að ljúka endurúthlutuninni skal velja **Vinna úr**. Beðið er um bókunardagsetningu jafnvel þótt ekkert hafi verið bókað. Þegar endurúthlutuninni er lokið sýnir síðan **Úthlutun á tekjuupphæð** fyrir hverja sölupöntun úthlutunarupphæðina fyrir allar vörur í báðum sölupöntununum. Síðan **Úthlutun á tekjuupphæð** fyrir hverja sölupöntun mun sem sagt innihalda vöru sem er ekki til í þeirri sölupöntun vegna þess að hún er hluti af sama samningnum en í annarri sölupöntun.

> [!TIP]
> Til að setja í samhengi af hverju þessar vörur eru sýndar er hægt að bæta öðrum dálkum við hnitanetið, t.d. **Kenni endurúthlutunar** og **Sölupöntun**.
> 
> [![Viðbótardálkar á síðunni Úthlutun tekjuupphæðar.](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]