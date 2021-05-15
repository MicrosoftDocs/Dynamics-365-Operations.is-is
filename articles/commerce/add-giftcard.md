---
title: Gjafakortseining
description: Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962764"
---
# <a name="gift-card-module"></a>Gjafakortseining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um gjafakortseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

Hægt er að nota einingar gjafakorta við greiðslueiningar til að taka á móti gjafakortum, sem er algeng gerð greiðsla sem eru notaðar fyrir rafræn viðskipti. Gjafakortseiningin styður Dynamics 365, SVS og Givex gjafakort. Gjafakort SVS og Givex eru innleyst með Adyen greiðsluþjónustuaðila. Frekari upplýsingar um stuðning við gjafakort, svo sem SVS og Givex, eru í [Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md).

> [!NOTE]
> Stuðningur við innlausn SVS og Givex-gjafakorta við greiðsluferli er í boði í Dynamics 365 Commerce útgáfu 10.0.11. 

Tvær gjafakortseiningar eru í boði:

- **Gjafakort** - Hægt er að nota þessa einingu á greiðslusíðu til að innleysa gjafakort sem tilboð. 
- **Könnun á stöðu gjafakorts** - Hægt er að nota þessa einingu á hvaða síðu sem er til að skoða stöðuna á gjafakorti. Þessi eining er tiltæk í Commerce Release 10.0.14 og nýrri.

> [!NOTE]
> Stuðningur við fyrir athugunarstöðu gjafakorts er tiltækur í Dynamics 365 Commerce útgáfu 10.0.14.

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

> [!IMPORTANT]
> Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.11 og eru aðeins nauðsynlegar ef stuðningur er fyrir SVS eða Givex-gjafakort. Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>Útvíkka notkun innri gjafakorta til að nota í netverslun rafrænna viðskipta

Innri gjafakort eru sjálfgefið ekki stillt inn á notkun í netverslunum rafrænna viðskipta. Áður en leyft er að nota innri gjafakort fyrir greiðslu ætti því að stilla þau með viðbótum sem stuðla að því að gera þau öruggari. Hér eru gjafakortasvæðin sem ætti að víkka út áður en leyfa á notkun innri gjafakorta í framleiðslu:

- **Gjafakortsnúmer** – Númeraraðir er notaðar til að mynda gjafakortsnúmer fyrir innri gjafakort. Þar sem auðvelt er að spá fyrir um númeraraðir ættir þú að víkka út myndun á gjafakortanúmerum þannig að handahófskenndir, dulkóðaðir strengir séu notaðir fyrir gjafakortanúmer sem gefin eru út.
- **GetBalance** – **GetBalance** API er notað til að fletta upp á innistæðum gjafakorta. Þetta API er opinbert að sjálfgefnu. Ef ekki er krafist PIN-númers til að fletta upp á innistæðum gjafakorta er hætt á að kerfisbundnar árásir noti **GetBalance** API í tilraun til að fletta upp á gjafakortanúmerum sem eru með innstæður. Með því að innleiða bæði kröfur um PIN-númer fyrir innri gjafakort og API-takmörkun geturðu stuðlað að því að draga úr áhættunni.
- **PIN** – Innri gjafakort styðja ekki PIN-númer. Þú ættir að framlengja innri gjafakort þannig að það þarf PIN-númer til að fletta upp stöðu. Þessa virkni er einnig hægt að nota til að læsa gjafakortum eftir nokkrar rangar tilraunir í röð við að slá inn PIN-númer.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Virkja gjafakortagreiðslur fyrir greiðsluferli gests

Sjálfgefið er að gjafakortsgreiðslur séu ekki virkar fyrir (nafnlausar) greiðslur gesta. Til að virkja þetta skal fylgja þessum skrefum.

1. Í Commerce Headquarters skal fara í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> POS-aðgerðir**.
1. Veljið og haldið (eða hægrismellið) á haus netsins og veljið svo **Setja inn dálka**.
1. Í svarglugganum **Setja inn dálka** skal velja gátreitinn **AllowAnonymousAccess**.
1. Veldu **Uppfæra**.
1. Fyrir aðgerðir **520** (innistæða gjafakorts) og **214** skal stilla gildið **AllowAnonymousAccess** á **1**.
1. Veljið **Vista**.
1. Keyrið verkraðara **1090** til að samstilla breytingar við gagnagrunn rásarinnar. 

## <a name="add-a-gift-card-module-to-a-page"></a>Bæta gjafakortseiningu við síðu

Leiðbeiningar um hvernig bæta skuli gjafakortseiningu við greiðslusíðu og stilla nauðsynlega eiginleika er að finna í [Greiðsluferliseining](add-checkout-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Körfueining](add-cart-module.md)

[Körfutáknseining](cart-icon-module.md)

[Greiðsluferliseining](add-checkout-module.md)

[Greiðslueining](payment-module.md)

[Sendingaraðseturseining](ship-address-module.md)

[Afhendingarkostaeining](delivery-options-module.md)

[Eining fyrir afhendingarupplýsingar](pickup-info-module.md)

[Pöntunarupplýsingaeining](order-confirmation-module.md)

[Stuðningur við utanaðkomandi gjafakort](./dev-itpro/gift-card.md)

[Uppfærslur á SDK og kjarnasafni](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
