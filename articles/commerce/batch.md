---
title: Betri meðhöndlun á runuröktum vörum
description: Þetta efnisatriði lýsir endurbótunum sem hafa verið gerðar á meðhöndlun á runum fyrir runuraktar vörur í bókunarferlinu fyrir uppgjör.
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799710"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Betri meðhöndlun á runuröktum vörum


[!include [banner](includes/banner.md)]


Á sölustaðnum er ekki hægt að sækja rununúmer fyrir runuraktar vörur þegar sala stendur yfir. Hins vegar, fyrir ákveðnar skilgreiningar, þegar sölur eru bókaðar í höfuðstöðvunum í gegnum pantanir viðskiptamanns eða bókun á uppgjöri gerir Microsoft Dynamics-kerfið ráð fyrir því að gild rununúmer fyrir runuraktar vörur séu til staðar og að þau verði notuð í reikningsfærsluferlinu.

Ef gild rununúmer eru í boði fyrir vörur eru þau notuð í reikningsfærsluferli viðskiptamannapöntunar og reikningsfærsluferli sölupöntunar úr bókun uppgjörs. Annars nær reikningsfærsluferli viðskiptamannapöntunar ekki að bóka og notandi sölustaðar fær villuboð. Smásöluuppgjör fer þá í villustöðu. Þessi villustaða kemur upp jafnvel eftir að kveikt hefur verið á neikvæðri birgðastöðu fyrir vörurnar.

Endurbætur sem gerðar hafa verið á Retail-útgáfu 10.0.4 og nýrri hjálpa til við að tryggja, þegar kveikt er á neikvæðri birgðastöðu fyrir runuraktar vörur, að ekki sé lokað fyrir reikningsfærslu viðskiptamannapöntunar og reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri fyrir þessar vörur ef birgðir eru 0 (núll) eða rununúmer er ekki til staðar. Nýja virknin notar sjálfgefið runukenni fyrir sölulínur þegar rununúmer eru ekki í boði.

Til að skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptamanna skal á síðunni **Viðskiptafæribreytur**, í flipanum **Pantanir viðskiptamanna**, í flýtiflipanum **Pöntun**, stilla reitinn **Sjálfgefið auðkenni runu**.

Til að skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri skal á síðunni **Viðskiptafæribreytur**, í flipanum **Bókun**, í flýtiflipanum **Birgðauppfærsla**, stilla reitinn **Sjálfgefið auðkenni runu**.

> [!NOTE]
> Þessi virkni er aðeins í boði þegar kveikt er á ítarlegu vöruhúsakerfi fyrir tiltekna verslun, vöruhús og vörur. Í seinni útgáfu verður virknin einnig studd fyrir aðstæður þar sem ítarlegt vöruhúsakerfi er ekki notað.

> [!NOTE]
> Stuðningur við bætta meðhöndlun runuraktra vara við uppgjörsbókun fyrir sviðsmyndir vöruhúsakerfis sem ekki er ítarlegt var kynntur í Retail-útgáfu 10.0.5.


[!INCLUDE[footer-include](../includes/footer-banner.md)]