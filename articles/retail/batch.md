---
title: Betri meðhöndlun á runuröktum vörum
description: Þetta efnisatriði lýsir endurbótum sem hafa verið gerðar á meðhöndlun á runum fyrir runuraktar vörur í bókunarferli smásöluuppgjörs.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617390"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Betri meðhöndlun á runuröktum vörum

Á sölustaðnum Microsoft Dynamics 365 for Retail er ekki hægt að sækja rununúmer fyrir runuraktar vörur þegar sala stendur yfir. Hins vegar, fyrir ákveðnar skilgreiningar, þegar sölur eru bókaðar í höfuðstöðvunum í gegnum pantanir viðskiptamanns eða bókun á uppgjöri gerir Microsoft Dynamics-kerfið ráð fyrir því að gild rununúmer fyrir runuraktar vörur séu til staðar og að þau verði notuð í reikningsfærsluferlinu.

Ef gild rununúmer eru í boði fyrir vörur eru þau notuð í reikningsfærsluferli viðskiptamannapöntunar og reikningsfærsluferli sölupöntunar úr bókun uppgjörs. Annars nær reikningsfærsluferli viðskiptamannapöntunar ekki að bóka og notandi sölustaðar fær villuboð. Smásöluuppgjör fer þá í villustöðu. Þessi villustaða kemur upp jafnvel eftir að kveikt hefur verið á neikvæðri birgðastöðu fyrir vörurnar.

Endurbætur sem gerðar hafa verið á Microsoft Dynamics for Retail útgáfu 10.0.4 og nýrri hjálpa til við að tryggja, þegar kveikt er á neikvæðri birgðastöðu fyrir runuraktar vörur, að ekki sé lokað fyrir reikningsfærslu viðskiptamannapöntunar og reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri fyrir þessar vörur ef birgðir eru 0 (núll) eða rununúmer er ekki til staðar. Nýja virknin notar sjálfgefið runukenni fyrir sölulínur þegar rununúmer eru ekki í boði.

Til að skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptamanna skal á síðunni **Smásölufæribreytur**, í flipanum **Pantanir viðskiptamanna**, í flýtiflipanum **Pöntun**, stilla reitinn **Sjálfgefið auðkenni runu**.

Til að skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri skal á síðunni **Smásölufæribreytur**, í flipanum **Bókun**, í flýtiflipanum **Birgðauppfærsla**, stilla reitinn **Sjálfgefið auðkenni runu**.

> [!NOTE]
> Þessi virkni er aðeins í boði þegar kveikt er á ítarlegu vöruhúsakerfi fyrir tiltekna verslun, vöruhús og vörur. Í seinni útgáfu verður virknin einnig studd fyrir aðstæður þar sem ítarlegt vöruhúsakerfi er ekki notað.
