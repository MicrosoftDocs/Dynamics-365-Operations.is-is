---
title: Eigendur afurða
description: Þessi grein gefur upplýsingar um mat á framleiðslueigendum. Eigendur afurða er hópur notenda sem ber ábyrgð á tilteknum afurðum. Aðeins meðlimir í hópnum geta losað þessar afurðir. Einnig er hægt að nota Eigendur afurða í samþykktarverkflæðinu.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5e09fdbbe14aa5a5ffbc5f07ae90b5d307a9e155
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907523"
---
# <a name="product-owners"></a>Eigendur afurða

[!include [banner](../includes/banner.md)]

Eigendur afurðanna er hópur notenda sem ber ábyrgð á tilteknum afurðum. Þegar hóp fyrir Eigendur afurða er úthlutað á afurð geta aðeins meðlimir þess hóps losað afurðina. Einnig er hægt að nota eiganda afurðarinnar í samþykktarverkflæði í umsjón hönnunarbreytinga.

Eigendur afurðar eru Altækar stillingar. Þar af leiðandi eru þeir tiltækir öllum lögaðilum.

## <a name="create-a-product-owner-group"></a>Stofna hóp fyrir Eigendur afurða

Til að stofna hóp fyrir Eigendur afurða og bæta meðlimum við hann skal fylgja þessum skrefum.

1. Farið í **Umsjón hönnunarbreytinga \> Uppsetning \> hóp fyrir Eigendur afurða**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Eigandi afurðar** er fært inn heiti fyrir flokkinn.
4. Í reitnum **Heiti** skal slá inn lýsingu á hópnum.
5. Í flýtiflipanum **Meðlimir** skal bæta við starfsmönnum sem eiga að vera meðlimir í hópnum.

## <a name="assign-a-product-owner-to-a-product"></a>Úthluta eiganda afurðar á afurð

Til að úthluta eiganda afurðar á afurð, skal fylgja þessum skrefum:

1. Opnið **Upplýsingar um afurð** síðuna fyrir viðkomandi afurð eða umsjónarmann afurðar.
1. Í flýtiflipanum **Almenn atriði** er reiturinn **Eigandi afurðar** stilltur á heiti viðkomandi hóps fyrir eigendur afurða.

Þegar eiganda afurðar er úthlutað á afurð geta aðeins meðlimir í hóp fyrir eigendur afurða breytt stillingunni **Eigandi afurðar**.

Eigandi afurðar er einnig sýnilegur á síðunni **Losaðar afurðir**.

## <a name="product-owners-and-product-releases"></a>Eigendur afurða og afurðarlosun

Aðeins notendur úr hópi fyrir eigendur afurða geta losað afurðina. Hins vegar er undantekning þegar afurðin er undireining og yfireining hennar er losuð af eiganda yfireiningarinnar. Ef afurðin er hluti af UPPSKRIFT annarrar afurðar, kannar kerfið ekki eiganda hverrar afurðar í UPPSKRIFTINNI. Það athugar aðeins eiganda afurðar fyrir yfirafurðina.

Til dæmis er afurð X úthlutað á afurðareigendahópinn *Hanna skápa*. Afurð X er einnig hluti af UPPSKRIFT afurðar Y, sem er úthlutað á afurðareigendahópinn *Hanna hátalara*. Ef notandi úr afurðareigendahópnum *Hanna hátalara* losar afurð Y og uppskrift hennar verður afurð X losuð saman um leið og afurð Y.

## <a name="product-owners-and-approvals"></a>Eigendur afurða og samþykktir

Vegna þess að afurðareigendur vita hvort tilteknar hönnunarbreytingar muni koma sér vel fyrir þeirra afurð er oft skynsamlegt að taka þær með sem hluta af samþykktarferlinu í umsjón hönnunarbreytinga. Hægt er að innleiða þessa nálgun með því að setja upp vörueigendur sem þátttakanda í verkflæðinu sem er notað fyrir umsjón hönnunarbreytinga. Kerfið mun þá úthluta samþykktarverkefnum í verkflæði, byggt á þeim afurðum sem eru í stjórnunarbeiðnum og beiðnum um hönnunarbreytingar. Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]