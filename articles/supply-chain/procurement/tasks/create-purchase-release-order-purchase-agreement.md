---
title: Nota innkaupasamning þegar innkaupapöntun er stofnuð
description: Þessi ferli sýnir hvernig á að nota innkaupasamning þegar innkaupapöntun er stofnuð.
author: kamaybac
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1913181e85929951ce240ac31a0ac3f1351f6ae51f6ed2790bae577b2100b308
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731248"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Nota innkaupasamning þegar innkaupapöntun er stofnuð

[!include [banner](../../includes/banner.md)]

Þessi ferli sýnir hvernig á að nota innkaupasamning þegar innkaupapöntun er stofnuð. Innkaupasamning verður að nota þegar innkaupapöntun er stofnuð því afrita þarf almenna skilmála í haus innkaupapöntunarinnar. Þetta verk myndi venjulega framkvæmt af innkaupaaðila. Nauðsynleg frumforsenda þessari handbók, þú verður að hafa gildan innkaupasamning með í ráðstöfun afurðarmagns fyrir lánardrottinn og vörur. Hægt er að nota sömu aðferð ef þú ert með innkaupasamning með aðrar gerðir af ráðstafanir.

## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun

1. Farðu í **Framleiðsla og aðföng \> Vinnusvæði \> Undirbúningur innkaupapöntunar**.
1. Á aðgerðasvæðinu skal velja **Ný innkaupapöntun**.
1. Svarglugginn **Stofna innkaupapöntun** opnast. Veldu **Lánardrottnalykil**. Farðu yfir og breyttu öðrum reitum heimilisfangs eftir þörfum.
1. Útvíkka **Almennt** flýtiflipa.
1. Í reitnum **Innkaupasamningur** skal finna og velja gildan samning sem á að nota. Allar tiltækar samninga lánardrottins eru taldar upp hér.  
1. Velja skal **Já**.
1. Veldu **Í lagi**.

## <a name="add-a-line"></a>Bæta við línu

1. Í reitnum **Vörunúmer** skal slá inn gildi. Ef tilteknar víddir staðsetningar eða birgða eru á ráðstöfun verður þú að færa inn sama gildi í innkaupapöntunarlínu til að geta notað samningnum.
1. Í reitnum **Svæði** velurðu fellilistahnappinn til að opna uppflettinguna. Svæðið er hugsanlega útfyllt þegar með sjálfgefnu gildi úr pöntuninni, eða frá lánardrottni. Ef svo er er hægt að sleppa þessu þrepi.  
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
1. Í listanum skal velja tengilinn í valinni línu.
1. Í reitnum **Magn** slærðu inn tölu. Villuleita að verð er afritað úr ráðstöfun.  

## <a name="look-up-the-commitment"></a>Fletta upp á ráðstöfun

1. Veldu **Uppfæra línu**.
1. Veldu **Hengt við**. Hér er hægt að fá upplýsingar fyrir innkaupasamning. Til dæmis er hægt að sjá verð og hvort verð og afsláttur er fastur, sem þýðir að ef þú breytir verði eða afslætti á innkaupapöntun í annað gildi en á ráðstöfun, mun kerfið fjarlægja tengil svo innkaupapöntunarlínan uppfyllir ekki á ráðstöfun. Er einnig hægt að sjá hvort valkosturinn Hámark er notað er valinn, sem þýðir að magn á ráðstöfun má ekki fara fram úr með samlagningu allra innkaupa sem uppfylla ráðstöfun.  
1. Lokið síðunni.

## <a name="look-up-the-purchase-agreement"></a>Fletta upp á innkaupasamningur

1. Í **aðgerðasvæðinu** velurðu **Almennt**.
1. Veldu **Innkaupasamningur**.
1. Lokið síðunni.
1. Lokið síðunni.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]