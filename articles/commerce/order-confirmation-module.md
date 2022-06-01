---
title: Eining pöntunarstaðfestingar
description: Þetta efnisatriði fjallar um staðfestingareiningar og lýsir því hvernig á að notar þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e74ffbdfe57f9220cc9ed85edae4270409165b41
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780385"
---
# <a name="order-confirmation-module"></a>Eining pöntunarstaðfestingar

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um staðfestingareiningar og lýsir því hvernig á að notar þær í Microsoft Dynamics 365 Commerce.

Pöntunarstaðfestingareiningin er notuð til að sýna upplýsingar pöntunarstaðfestinga eftir að pöntun hefur verið gerð. Hún sýnir staðfestingarkenni pöntunar, tengslaupplýsingar pöntunar og aðrar upplýsingar um pöntun, svo sem vörur sem voru keyptar, greiðsluupplýsingar, afhendingarmáta og sendingaraðferð.

## <a name="order-confirmation-module-properties"></a>Eiginleikar staðfestingareiningar pöntunar

| Nafn eiginleika  | Gildi | Lýsing |
|----------------|--------|-------------|
| Fyrirsögn        | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Pöntunarstaðfestingareiningin getur haft fyrirsögn. Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina. Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi. |
| Númer tengiliðar | Text | Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar. |
| Sýna upplýsingar um tímahólf afhendingar | Satt eða ósatt | Þessi eiginleiki er í boði í Dynamics 365 Commerce 10.0.15 og ´nýrri. Þegar eiginleikinn er sannur birtir hann upplýsingar um tímahólf afhendingar ef slíkt er í boði fyrir vöru til afhendingar|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Einingar sem hægt er að nota á staðfestingarsíðu pöntunar

Þegar stofnuð er síða pöntunarstaðfestingar er hægt að bæta við öðrum tengdum einingum til viðbótar við einingu pöntunarstaðfestingar. Hér eru nokkur dæmi:

- **Tillögueining** – Bæta má tillögueiningunni við síðu pöntunarstaðfestingar til að veita viðskiptavininum tillögur að öðrum vörum.
- **Markaðssetningareiningar** – Hægt er að bæta öllum markaðssetningareiningum á staðfestingarsíðu pöntunar til að sýna markaðsefni.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Bæta upplýsingaeiningu pöntunar við síðu

Til að bæta einingu pöntunarstaðfestingar við nýja síðu og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í **Nýtt sniðmát** svargluggi, undir **Nafn sniðmáts**, sláðu inn nafnið **Sniðmát fyrir staðfestingu pöntunar**, og veldu síðan **Allt í lagi**.
1. Í **Líkami** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Sjálfgefin síða** mát og veldu síðan **Allt í lagi**.
1. Í **Aðal** rifa á **Sjálfgefin síða** mát, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Staðfesting á pöntun** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða sniðmátið. Eining pöntunarstaðfestingar verður ekki myndþýdd vegna þess að hún krefst samhengis númers pöntunarstaðfestingarinnar.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Staðfestingarsíða pöntunar** og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu **Sniðmát fyrir staðfestingu pöntunar**, og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**. 
1. Í **Aðal** rifa á **Sjálfgefin síða** mát, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Staðfesting á pöntun** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæðinu fyrir einingu pöntunarstaðfestingar skal velja **Fyrirsögn** við hliðina á blýantstákninu.
1. Í reitinn **Fyrirsagnartexti** í svarglugganum **Fyrirsögn** skal slá inn fyrirsagnartextanum **Staðfesting pöntunar** og velja síðan **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Sendingaraðseturseining](ship-address-module.md)

[Afhendingarkostaeining](delivery-options-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Gjafakortseining](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
