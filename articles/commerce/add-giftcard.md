---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761082"
---
# <a name="gift-card-module"></a>Gjafakortseining

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Hægt er að nota einingar gjafakorta við greiðslueiningar til að taka á móti gjafakortum, sem er algeng gerð greiðsla sem eru notaðar fyrir rafræn viðskipti. Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort. Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila. Frekari upplýsingar um stuðning við gjafakort, svo sem SVS og Givex, eru í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md).

Tvær gjafakortseiningar eru í boði:

- **Gjafakort** - Hægt er að nota þessa einingu á greiðslusíðu til að innleysa gjafakort sem tilboð. 
- **Könnun á stöðu gjafakorts** - Hægt er að nota þessa einingu á hvaða síðu sem er til að skoða stöðuna á gjafakorti. Þessi eining er tiltæk í Commerce Release 10.0.14 og nýrri.

Eftirfarandi mynd sýnir dæmi um gjafakortseiningu á greiðsluferlissíðu.

![Dæmi um gjafakortseiningu](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

- **Sýna fleiri reiti** - Þessi eiginleiki skilgreinir hvaða reiti skuli birta fyrir gjafakort auk gjafakortsnúmersins sem er alltaf birt sjálfgefið. Til dæmis styðja sum gjafakort með birtinu á persónuauðkenni (PIN) og önnur styðja birtingu PIN og gildistíma. Að öðrum kosti væri hægt að stilla þennan eiginleika á „Enginn“, sem myndi aðeins sýna gjafakortsnúmerið og enga viðbótarreiti.

Studd gildi:
-   PIN
-   Gildistími
-   PIN og lokadagur 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Vefstillingar fyrir gjafakortseiningar

Í vefsvæðishönnuði Commerce undir **Vefstillingar \> Viðbætur** er stilling gjafakortseiningar sem kallast **Studd gerð gjafakorts**. Þessi stilling styður þrjú gildi:
- **Dynamics 365 gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365 gjafakortum. Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.
- **SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Givex og SVS gjafakortum. Þessi stilling er studd fyrir innskráða og nafnlausa notendur á e-verslunarsíðunni.
- **Dynamics 365, SVS og Givex gjafakort** - Þegar þessari stillingu er beitt leyfir gjafakortseiningin aðeins innlausn á Dynamics 365, Givex og SVS gjafakortum. Þessi stilling er aðeins studd fyrir innskráða notendur á e-verslunarsíðunni.

## <a name="add-a-gift-card-module-to-a-page"></a>Bæta gjafakortseiningu við síðu

Leiðbeiningar um hvernig bæta skuli gjafakortseiningu við greiðslusíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Eining sendingaraðseturs](ship-address-module.md)

[Eining afhendingarvalkosta](delivery-options-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md)
