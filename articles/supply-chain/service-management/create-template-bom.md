---
title: Stofna sniðmátsuppskrift
description: Þú getur búið til sniðmátsuppskrift með því að nota ýmsar aðferðir.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566591"
---
# <a name="create-a-template-bom"></a>Stofna sniðmátsuppskrift   

[!include [banner](../includes/banner.md)]


Hægt er að stofna sniðmátsuppskrift með hvaða af eftirfarandi aðferðum. Fyrir alla aðferðir eru **Frá dagsetning** og **Til dagsetning** reitir valfrjálst og aðeins til upplýsinga.

## <a name="create-a-template-bom-manually"></a>Stofna sniðmátsuppskrift handvirkt

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Handvirkt** valkostinn.

4.  Í **Vörunúmer** reitnum, sláðu in vöru af gerðinni **Uppskrift**.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Smelltu á **Í lagi**.

Ný, tóm sniðmátsuppskrift er stofnuð.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Stofna sniðmátsuppskrift sem byggð er á annarri sniðmátsuppskrift

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Sniðmátsuppskrift** valkostinn.

4.  Í **Tilvísunarnúmer** reitinn, skal velja fyrirliggjandi sniðmátsuppskrift til að afrita á nýja sniðmátsuppskrift þína.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Smelltu á **Í lagi**.

Ný sniðmátsuppskrift er stofnuð með því að notast við línur sem samsvara línunum í upprunalegu sniðmátsuppskriftinni.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Stofna sniðmátsuppskrift sem byggð er á uppskriftarvöru

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Uppskrift**.

4.  Í **Tilvísunarnúmer** reitur, velja uppskriftar útgáfu. Vara af gerðinni Uppskrift er afrituð í **Vörunúmer**.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Smelltu á **Í lagi**.

Nýtt sniðmátsuppskrift er búið til með því að nota línur sem samsvara línunum í uppskriftinni sem er skráð í **Uppskriftir**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Stofna sniðmátsuppskrift sem byggð er á framleiðsluuppskrift

1.  Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónustuhlutir** \> **Sniðmátsuppskriftir**.

2.  Ýttu á CTRL + N til að opna **Búa til sniðmátsuppskrift** skjámynd.

3.  Undir **Afrita uppskriftarlínur frá tilvísun**, veldu **Framleiðsla**.

4.  Í **Tilvísunarnúmer** reitnum, velja framleiðsluuppskrift.

5.  Í **Heiti** reitinn, slá inn heiti fyrir sniðmátið.

6.  Í **Frá dagsetningu** og **Til dagsetningar** reitina, slá inn dagsetningu millibili þar sem sniðmátsuppskriftin er virkt.

7.  Smelltu á **Í lagi**.

Nýtt sniðmátsuppskrift er búið til með því að nota línur sem samsvara línunum í Uppskrift sem er skráð í **Uppskrift**.

## <a name="see-also"></a>Sjá einnig

[Uppskriftir sniðmáts](template-boms.md)

  


