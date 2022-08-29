---
title: Vefsíðuvalseining
description: Þessi grein fjallar um síðuvalseininguna og lýsir því hvernig á að bæta henni við síðusíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: efd58206d88618aedb6b574afb47da1e9e578ef1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276749"
---
# <a name="site-picker-module"></a>Vefsíðuvalseining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um síðuvalseininguna og lýsir því hvernig á að bæta henni við síðusíður í Microsoft Dynamics 365 Commerce.

Þegar fyrirtæki er með ólík svæði á mörkuðum, svæði og staðhætti þurfa notendur svæðis að skipta á milli svæða og velja æskilegt verslunarsvæði á einfaldan hátt. Til að mæta þessari atburðarás gerir vefvalseiningin notendum kleift að vafra um margar síður. Einnig er mælt með vefsíðuvali þegar [landfræðileg uppgötvun og tilvísun](geo-detection-redirection.md) hafa verið innleiddar fyrir netverslunarsíðuna þína, svo að viðskiptavinir hafi leið til að hnekkja síðuvalinu sem þeir gefa til kynna með því að nota [land/svæðavals](country-region-picker-module.md) mát. 

Vefvalareiningin verður að vera stillt með lista yfir vefsvæði (markaðir, svæði eða staðsetningar) sem notendur vefsvæðisins geta skoðað. Eftirfarandi mynd sýnir dæmi um síðuvalseiningu sem er í haus síðusíðu.

![Dæmi um síðuvalseiningu í haus síðusíðu.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Eiginleikar síðuvalseiningar

| Heiti eiginleika | Gildi                 | Lýsing |
|---------------|-----------------------|-------------|
| Yfirskrift       | Texti                  | Fyrirsögn einingarinnar. |
| Vefsvæðakostir  | Nafn, mynd, URL      | Þessi eiginleiki tilgreinir heiti, tengil á heimasíðu svæðisins og valfrjálsa mynd til að sýna fyrir hvert svæði sem er tekið með í einingunni. Myndin getur verið flagg eða einhver framsetning á markaði, svæði eða staðháttum. |

## <a name="add-a-site-picker-module-to-a-page"></a>Bættu síðuvalareiningu við síðu

Hægt er að bæta síðuvalseiningunni við **Vefsvæði velja** rifa á [haus mát](author-header-module.md). Eftir að síðuvalareiningu hefur verið bætt við geturðu skilgreint fyrirsögn einingar og síðuvalkosti. Yfirleitt er hauseining innifalin í hausbroti sem hægt er að deila á netviðskiptasíður fyrir síðu. 

Fylgdu þessum skrefum til að bæta vefvalseiningunni við hauseiningu.

1. Í **Vefsvæði velja** rauf á hauseiningu hausbrotsins, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, bættu við a **Vefsvæði velja** mát og veldu síðan **Allt í lagi**.
1. Í **Vefsvæði velja** eiginleikarúða, veldu **Bættu við lista yfir síðuvalkosti**. Breytanlegt **Listi yfir valkosti fyrir vefsvæði** valmöguleiki birtist.
1. Veldu **Listi yfir valkosti fyrir vefsvæði**. The **Listi yfir valkosti fyrir vefsvæði** svarglugginn birtist.
1. Undir **Heiti vefsvæðis**, sláðu inn nafn vefsvæðisins sem birtist í fellilistanum fyrir vefval.
1. Undir **Tilvísunarslóð vefsvæðis**, veldu **Bættu við tengli**. The **Bættu við tengli** útrásarglugginn birtist.
1. Í **Bættu við tengli** útfallsrúða, veldu **Sérsniðin síða**, og veldu síðan **Næst**.
1. Af vefslóðalistanum skaltu velja slóðina með slóðinni sem þú bjóst til þegar þú bættir rásinni við síðuna (td,`www.adventure-works.com/fr-ca`), og veldu síðan **Sækja um**.
1. Veldu **Í lagi**.
1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Veldu **Birta** að birta síðuna.

Í eftirfarandi dæmi hefur vefvalseiningunni verið bætt við **Vefsvæði velja** rauf á hauseiningu sem er í hausbroti sem er nefnt **Header Container**.

![Dæmi um svæðisvalseiningu í hausbroti.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining síðuhauss](author-header-module.md)

[Brauðmylsnueining](add-breadcrumb.md)

[Eining yfirlitsvalmyndar](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
