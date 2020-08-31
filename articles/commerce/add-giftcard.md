---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661243"
---
# <a name="gift-card-module"></a>Gjafakortseining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Gjafakort eru algeng greiðsluform og hægt er að nota gjafakortseininguna í kassaeiningu til að taka við gjafakortum. Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort. Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila.

Nánari upplýsingar um stuðning við utanaðkomandi gjafakort eins og SVS og Givex er að finna í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md)

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
