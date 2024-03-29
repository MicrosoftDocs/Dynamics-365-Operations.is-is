---
title: Stofna sniðmátsuppskrift
description: Þú getur búið til sniðmátsuppskrift með því að nota ýmsar aðferðir.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169b54a0509a2e11ce2e888404da10fd81db475e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678207"
---
# <a name="create-a-template-bom"></a>Stofna sniðmátsuppskrift   

[!include [banner](../includes/banner.md)]


Hægt er að stofna sniðmátsuppskrift með hvaða af eftirfarandi aðferðum. Fyrir alla aðferðir eru **Frá dagsetning** og **Til dagsetning** reitir valfrjálst og aðeins til upplýsinga.

## <a name="create-a-template-bom-manually"></a>Stofna sniðmátsuppskrift handvirkt

1.  Opnið **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Veljið **Nýtt** til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Handvirkt** valkostinn.

4.  Í **Vörunúmer** reitnum, sláðu in vöru af gerðinni **Uppskrift**.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Veljið **Í lagi**.

Ný, tóm sniðmátsuppskrift er stofnuð.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Stofna sniðmátsuppskrift sem byggð er á annarri sniðmátsuppskrift

1.  Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Veljið **Nýtt** til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Sniðmátsuppskrift** valkostinn.

4.  Í **Tilvísunarnúmer** reitinn, skal velja fyrirliggjandi sniðmátsuppskrift til að afrita á nýja sniðmátsuppskrift þína.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Veljið **Í lagi**.

Ný sniðmátsuppskrift er stofnuð með því að notast við línur sem samsvara línunum í upprunalegu sniðmátsuppskriftinni.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Stofna sniðmátsuppskrift sem byggð er á uppskriftarvöru

1.  Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Veljið **Nýtt** til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Uppskrift**.

4.  Í **Tilvísunarnúmer** reitur, velja uppskriftar útgáfu. Vara af gerðinni Uppskrift er afrituð í **Vörunúmer**.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Veljið **Í lagi**.

Nýtt sniðmátsuppskrift er búið til með því að nota línur sem samsvara línunum í uppskriftinni sem er skráð í **Uppskriftir**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Stofna sniðmátsuppskrift sem byggð er á framleiðsluuppskrift

1.  Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Veljið **Nýtt** til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Framleiðsla**.

4.  Í **Tilvísunarnúmer** reitnum, velja framleiðsluuppskrift.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Veljið **Í lagi**.

Nýtt sniðmátsuppskrift er búið til með því að nota línur sem samsvara línunum í Uppskrift sem er skráð í **Uppskrift**.

## <a name="see-also"></a>Sjá einnig

[Uppskriftir sniðmáts](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]