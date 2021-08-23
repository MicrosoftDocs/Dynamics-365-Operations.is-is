---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f2db61cf23c217365274297c6e9878a4eb5679f8d9502cb70484372ae43f6b18
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716885"
---
# <a name="cart-module"></a>Körfueining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

Körfueining sýnir hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa. Einingin sýnir einnig samantekt á pöntun og gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.

Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur. Hún styður einnig tengilinn **Til baka í verslun**. Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.

Í körfueiningunni eru gögn byggð á körfuauðkenninu, sem er vafrakaka sem hægt er að nálgast á vefsvæðinu. 

Eftirfarandi mynd sýnir dæmi um körfusíðu á Fabrikam-svæðinu.

![Dæmi um körfueiningu á Fabrikam-síðu.](./media/cart2.PNG)

Eftirfarandi mynd sýnir dæmi um körfusíðu á Fabrikam-svæðinu. Í þessu dæmi er afgreiðslugjald fyrir línuatriði.

![Dæmi um körfueiningu með umsýslugjaldi fyrir línuatriði.](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Eiginleikar og hólf körfueininga

| Eiginleiki | Gildi | lýsing |
|----------------|--------|-------------|
| Fyrirsögn | Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Fyrirsögn fyrir körfuna, t.d. „Innkaupakarfa“ eða „Vörur í körfunni þinni“. |
| Sýna villuboðin Ekki til á lager | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Sat** sýnir körfusíðan villur sem tengjast birgðum. Mælt er með því að þessi eiginleiki sé stilltur á **Satt** ef birgðaathuganir eru notaðar á svæðinu. |
| Sýna sendingargjöld fyrir línuatriði | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** sýna línuatriði körfu sendingargjöld, ef þessar upplýsingar eru í boði. Þessi eiginleiki er ekki studdur í Fabrikam-skemanu því að notendur velja sendingu eingöngu í greiðsluferlinu. Hins vegar er hægt að kveikja á þessum eiginleika í öðrum verkflæðum ef það á við. |
| Sýna tiltæk kynningartilboð| **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** " sýnir karfan tiltæk kynningartilboð, byggt á vörum í körfunni. Þessi eiginleiki er í boði í Dynamics 365 Commerce útgáfu 10.0.16. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Einingar sem hægt er að nota í körfueiningu

- **Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni. Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS). Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“
- **Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru. Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu. Fyrir frekari upplýsingar um þessa einingu, sjá [Verslunarvalseiningu](store-selector.md).

## <a name="module-properties"></a>Eiginleikar einingar

Hægt er að skilgreina eftirfarandi stillingar fyrir körfueiningar á **Stillingar svæðis \> viðbætur**:

- **Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna. Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.
- **Birgðir** - Frekari upplýsingar um hvernig á að nota birgðastillingar er að finna í [Nota birgðastillingar](inventory-settings.md).
- **Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**. Hægt er að stilla leiðina á vettvangsstigi, sem gerir smásöluaðilum kleift að fara með viðskiptavininn aftur á heimasíðuna eða aðra síðu á síðunni.

> [!IMPORTANT]
> Í Dynamics 365 Commerce 10.0.14 útgáfu og síðar eru vörur í körfunni uppsafnaðar á grundvelli stillinga sem eru skilgreindar í virkniforstillingu á netinu fyrir netverslunina í höfuðstöðvum Commerce. Frekari upplýsingar um hvernig á að stofna virkniforstillingu á netinu og stilla eiginleikana sem þarf fyrir uppsöfnun er að finna í [Búa til virkniforstillingu á netinu](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Samskipti við Commerce Scale Unit

Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce. Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Bæta körfueiningu við síðu

Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.
1. Í svarglugganum **Nýtt brot** skal velja eininguna **Karfa**.
1. Undir **Heiti brots** skal slá inn heitið **Körfubrot** og síðan velja **Í lagi**.
1. Veldu hólfið **Karfa**.
1. Hægra megin á eiginleikasvæðinu skal velja blýantstáknið, slá inn texta fyrirsagnar í reitinn og síðan velja gátmerkistáknið.
1. Í hólfinu **Karfa**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Verslunarval** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.
1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn heiti fyrir sniðmátið.
1. Í trjáskipulaginu skal velja hólfið **Meginmál**, velja úrfellingarmerkið (**...**), og síðan velja **Bæta við broti**.
1. Í svarglugganum **Velja brot** skal velja síðubrotið **Körfubrot** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í glugganum **Velja sniðmát** skal velja sniðmátið sem var búið til, slá inn síðuheiti og síðan velja **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Sendingaraðseturseining](ship-address-module.md)

[Afhendingarkostaeining](delivery-options-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Gjafakortseining](add-giftcard.md)

[Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md)

[Búa til virkniforstillingu á netinu](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]