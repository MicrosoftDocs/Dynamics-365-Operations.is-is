---
title: Stofna og viðhalda á birgðalæsing
description: Í þessari grein er lýst hvernig birgðalæsing er notuð til að koma í veg fyrir að efnislegar lagerbirgðir verði teknar frá af öðrum upprunaskjölum á útleið.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95b689bedfc76598dfa81548a074f4fb7c833a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859344"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Stofna og viðhalda á birgðalæsing

[!include [banner](../../includes/banner.md)]

Í þessari grein er lýst hvernig birgðalæsing er notuð til að koma í veg fyrir að efnislegar lagerbirgðir verði teknar frá af öðrum upprunaskjölum á útleið. Áður en hafist er handa við ferlin í þessari grein verður þú að vera með vöru þar sem efnislegar lagerbirgðir eru í boði.

## <a name="block-inventory"></a>Birgðum læst

Fylgið eftirfarandi skrefum til að stofna birgðalokunarskrá svo birgðir séu lokaðar.

1. Farið í **Birgðastjórnun \> Reglubundin verk \> Birgðalæsing**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í haus nýju lokunarfærslunnar á að setja **Vörunúmer** reitinn á vöruna sem á að loka á og slá inn lýsingu.
1. Í flýtiflipanum **Almennt**, í reitnum **Magn**, skal færa inn vörufjöldann sem á að læsa.
1. Í flýtiflipanum **Birgðavíddir** skal tilgreina svæðið og vöruhúsið þar sem vörurnar sem á að læsa eru staðsettar.
1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Uppfæra skilyrðum fyrir birgðalæsing

Fylgið eftirfarandi skrefum til að uppfæra birgðalokunarfærslu.

1. Farið í **Birgðastjórnun \> Reglubundin verk \> Birgðalæsing**.
1. Á listasvæðinu skal velja lokunarfærsluna sem á við.
1. Breyta færslunni eftir þörfum. Til dæmis væri hægt að breyta gildinu í reitnum **Væntanleg dagsetning** til að tilgreina hvenær læstar birgðir verða væntanlega aðgengilegar fyrir frátekningu. Ef valkosturinn **Áætluð innhreyfing** er valinn mun dagsetningin birtast á væntanlegri færslu. (Valkosturinn **Væntanlegar innhreyfingar** er sjálfgefið valinn þegar lokunarfærsla er stofnuð handvirkt.)
1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="unblock-inventory"></a>Birgðir opnaðar

Fylgja skal eftirfarandi skrefum til að fjarlægja birgðalokunarfærslu þannig að birgðir séu opnaðar.

1. Farið í **Birgðastjórnun \> Reglubundin verk \> Birgðalæsing**.
1. Á listasvæðinu skal velja lokunarfærsluna sem á við.
1. Á aðgerðasvæðinu skal velja **Eyða**.
1. Þú færð kvaðningu um að staðfesta aðgerðina. Veldu **Já** til að halda áfram.
1. Lokið síðunni.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
