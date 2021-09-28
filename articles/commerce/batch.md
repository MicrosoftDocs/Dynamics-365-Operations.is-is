---
title: Betri meðhöndlun á runuröktum vörum
description: Þetta efnisatriði lýsir betri meðhöndlun á runuröktum vörum í bókunarferlinu fyrir uppgjör í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/09/2021
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
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485784"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Betri meðhöndlun á runuröktum vörum

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir betri meðhöndlun á runuröktum vörum í bókunarferlinu fyrir uppgjör í Microsoft Dynamics 365 Commerce.

Á sölustaðnum Dynamics 365 Commerce er ekki hægt að sækja rununúmer fyrir runuraktar vörur þegar sala stendur yfir. Hins vegar, fyrir tilgreindar skilgreiningar, þegar sölur eru bókaðar í höfuðstöðvum Commerce í gegnum pantanir viðskiptavinar eða bókun á uppgjöri gerir Commerce ráð fyrir því að gild rununúmer fyrir runuraktar vörur séu til staðar og verði notuð í reikningsfærsluferlinu.

Ef gild rununúmer eru í boði fyrir afurðir eru þau notuð bæði í reikningsfærsluferli viðskiptavinapöntunar og reikningsfærsluferli sölupöntunar úr bókun uppgjörs. Ef gild rununúmer eru ekki tiltæk fyrir afurðir nær reikningsfærsluferli viðskiptavinapöntunar ekki að bóka og notandi sölustaðar fær villuboð. Þá kemur villustaða upp fyrir bókun uppgjörs, jafnvel þó að kveikt hafi verið á neikvæðri birgðastöðu fyrir afurðirnar.

Endurbætur á Commerce hjálpa til við að tryggja, þegar kveikt er á neikvæðri birgðastöðu fyrir runuraktar vörur, að ekki sé lokað fyrir reikningsfærslu viðskiptavinapöntunar og reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri fyrir þessar vörur ef birgðir eru 0 (núll) eða rununúmer er ekki til staðar. Endurbætta virknin notar sjálfgefið runukenni fyrir sölulínur þegar rununúmer eru ekki í boði.

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>Skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptavina

Fylgja skal þessum leiðbeiningum til að skilgreina sjálfgefið runukenni sem notað er fyrir pantanir viðskiptavina.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur Commerce**.
1. Á flipanum **Pantanir viðskiptavinar**, á flýtiflipanum **Pöntun**, skal slá inn gildi í svæðið **Sjálfgefið auðkenni runu**.

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>Skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri

Til að skilgreina sjálfgefið runukenni sem notað er fyrir reikningsfærslu sölupöntunar í gegnum bókun á uppgjöri skal fylgja þessum leiðbeiningum.

1. Opnið **Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur Commerce**.
1. Á flipanum **Bókun**, á flýtiflipanum **Birgðauppfærsla**, skal slá inn gildi í svæðið **Sjálfgefið auðkenni runu**.

> [!NOTE]
> - Virkni fyrir sjálfgefið runukenni er aðeins í boði þegar kveikt er á ítarlegu vöruhúsakerfi fyrir tiltekna verslun, vöruhús og vörur. Í síðari útgáfu verður virkni fyrir sjálfgefið runukenni einnig studd fyrir aðstæður þar sem ítarlegt vöruhúsakerfi er ekki virkt.
> - Stuðningur við bætta meðhöndlun runuraktra vara við uppgjörsbókun fyrir sviðsmyndir vöruhúsakerfis sem ekki er ítarlegt var kynntur í Commerce-útgáfu 10.0.5.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
