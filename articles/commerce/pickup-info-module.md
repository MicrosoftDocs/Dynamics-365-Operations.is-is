---
title: Eining fyrir afhendingarupplýsingar
description: Þetta efnisatriði fjallar um einingu afhendingarupplýsinga og útskýrir hvernig á að bæta henni við greiðslusíður á vefsvæði Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d04e2650f9c601d008ebf19080059b70416d7917
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000610"
---
# <a name="pickup-information-module"></a>Eining fyrir afhendingarupplýsingar

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um einingu afhendingarupplýsinga og útskýrir hvernig á að bæta henni við greiðslusíður á vefsvæði Microsoft Dynamics 365 Commerce.

Hægt er að nota eininguna fyrir afhendingarupplýsingar í greiðsluferliseiningu til að sýna upplýsingar um tiltekt pantana. Viðskiptavinir geta skoðað tiltækar dagsetningar og tímahólf og valið hentugan tíma til að sækja pöntunina. Til dæmis getur viðskiptavinur valið að sækja pöntun klukkan 15:00 þann 21. mars frá San Francisco-versluninni.

Skilgreina verður tímahólf sóttra pantana fyrir viðeigandi verslanir í Commerce Headquarters. Frekari upplýsingar er að finna í [Stofna og uppfæra tímabil afhendingar til viðskiptavinar](dev-itpro/pickup-timeslots.md).

Þegar eining fyrir afhendingarupplýsingar er stofnuð á greiðsluferlissíðu en engin tímahólf eru skilgreind fyrir verslunina sem valin er til að sækja, sýnir einingin upplýsingar en notandinn getur ekki valið nein tímahólf. Tímahólf eru valkvæð og eru ekki nauðsynleg til að leggja pöntunina inn.

Þegar margar vörur eru valdar til að sækja í mörgum verslunum leyfir eining fyrir afhendingarupplýsingar notandanum að velja tímahólf fyrir hverja verslun fyrir sig, að því gefnu að tímahólf séu tiltæk fyrir slíkt.

> [!NOTE]
> Stuðningur við tímahólf og eining fyrir afhendingarupplýsingar greiðsluferils er tiltækt í Dynamics 365 Commerce útgáfu 10.0.15 og nýrri útgáfum.

Eftirfarandi skýringarmynd sýnir dæmi um val á tímahólfi á einingu afhendingarupplýsinga á greiðsluferlissíðu.

![Dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

- **Fyrirsögn** – Sláið inn fyrirsögn fyrir eininguna.

## <a name="show-time-slot-information-after-an-order-is-placed"></a>Sýna upplýsingar um tímahólf eftir að pöntun er gerð

Eftir að pöntun er gerð er hægt að skoða upplýsingar um valið tímahólf í [Einingu pöntunarstaðfestingar](order-confirmation-module.md) og [Upplýsingaeiningar pöntunar](account-management.md#order-details-page). Báðar þessar einingar hafa eiginleikann **Sýna upplýsingar um tímahólf**. Áður en hægt er að sýna valið tímahólf við pöntunarferlið verður að stilla þennan eiginleika á **Satt**.

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>Bæta við einingu afhendingarupplýsinga greiðsluferlis við síðu

Leiðbeiningar um hvernig bæta skuli einingu afhendingarupplýsinga við greiðsluferlissíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).

Eftirfarandi mynd sýnir dæmi um útskráningarsíðu e-Commerce sem inniheldur tímahólf fyrir línuvörur afhendingar.

![Dæmi um greiðsluferlissíðu e-Commerce sem inniheldur tímahólf fyrir línuatriði](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna og uppfæra tímabil afhendingar til viðskiptavinar](dev-itpro/pickup-timeslots.md)

[Greiðsluferliseining](add-checkout-module.md)

[Eining pöntunarstaðfestingar](order-confirmation-module.md)

[Pöntunarupplýsingaeining](account-management.md)
