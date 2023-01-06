---
title: Dynamics 365 Finance, Supply Chain Management og Commerce í US Government Community Cloud (GCC)
description: Þessi grein veitir upplýsingar um vörur Microsoft Dynamics 365 US Government sem eru í boði fyrir viðurkennd yfirvöld og einkaaðila.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 41789d574cc7348dbf8a18db97da9c428da09602
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103939"
---
# <a name="dynamics-365-finance-supply-chain-management-and-commerce-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance, Supply Chain Management og Commerce í US Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]



Veldu vörur Microsoft Dynamics 365 United States (US) Government afurðir eru í boði fyrir viðurkennd yfirvöld og einkaaðila. Þessir aðilar takmarkast við eftirtaldar tegundir:

- Ríkis-, staðbundin-, ættbálka- og svæðisyfirvöld í Bandaríkjunum
- Einkaaðilar sem nota Dynamics 365 US Government til að bjóða upp á lausnir fyrir yfirvöld eða viðurkenndum meðlimum skýjasamfélagsins
- Einkaaðilar sem eru með gögn viðskiptavinar sem heyra undir reglur stjórnvalda og Dynamics 365 US Government er viðeigandi þjónusta til að uppfylla reglubundnar kröfur

Frekari upplýsingar eru í [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Innleiðing

Til að ljúka fyrstu innleiðingu fyrir innleiðingarverk í Microsoft Dynamics Lifecycle Services (LCS) skal fylgja leiðbeiningum í [Innleiðing innleiðingarverks](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Hins vegar skaltu ekki nota tengilinn á opinbert LCS sem gefinn er upp í þessum leiðbeiningum. Þess í stað skal nota eftirfarandi vefslóð til að opna LCS fyrir US Government Community Cloud (GCC): <https://gov.lcs.microsoftdynamics.us>.

Eftir að fyrstu innleiðingu er lokið skal fylgja leiðbeiningunum í [Innleiðing verks](../lifecycle-services/project-onboarding.md). Enn og aftur skaltu nota [LCS fyrir GCC](https://gov.lcs.microsoftdynamics.us) í stað opinberra LCS.

## <a name="environment-deployment"></a>Uppsetning umhverfis

Þegar innleiðingu verkefnis er lokið er hægt að fara yfir frekari möguleika LCS sem lýst er í [Lifecycle Services (LCS) fyrir viðskiptavini fjármála- og reksturs](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Snúðu þér því næst að umhverfi og útfærslu.

- Til að setja upp umhverfi sem Microsoft stýrir í gegnum LCS skal fylgja þessum leiðbeiningum í [Lifecycle Services (LCS) fyrir viðskiptavini fjármála- og reksturs](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Fyrir umhverfi í skýi sjá [Uppsetning og aðgangur að þróunarumhverfi](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Einnig þarf að ljúka við innleiðingarferli tilfangastjóra fyrir tenglana þína eins og lýst er í [Ljúka innleiðingarferli Azure Resource Manager fyrir Lifecycle Services-verkefni bandarískra stjórnvalda](arm-onbarding-us-goverment.md).

> [!NOTE]
> Fyrir LCS-verk bandarískra stjórnvalda er aðeins stuðningur fyrir Azure-áskrift tiltekinna stjórnvalda.

## <a name="features-that-arent-available"></a>Eiginleikar sem eru ekki í boði

Sumir eiginleikar verða ekki tiltækir í GCC eða þeir verða ekki tiltækir með Dynamics 365 í GCC. Til dæmis verður Azure DevOps-þjónusta óaðgengileg í GCC. Hins vegar er hægt að nota Azure DevOps eða opinbera Azure DevOps-þjónustu innanhúss. Frekari upplýsingar um stöðu eiginleika er að finna í [Framboð á eiginleika fyrir bandarísk stjórnvöld í viðskiptaforritum](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Er Dynamics 365 Finance og Dynamics 365 Supply Chain Management stutt í GCC-High?

Nr. Dynamics 365 Finance og Dynamics 365 Supply Chain Management er aðeins stutt í GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Get ég notað opinbert Azure DevOps með Finance og Supply Chain Management í GCC?

Já, þú getur notað opinbera Azure DevOps þjónustu ef þú ert ekki með kröfur fyrir lausn sem er vottuð af FEDRAMP (Federal Risk and Authorization Management Program). Þú getur einnig notað Azure DevOps Server.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Get ég sett upp einfalt lag af þróunarumhverfi í umhverfi sem hýst er í skýi í greiddri áskrift að Azure Commercial?

Nr. Í [LCS fyrir GCC](https://gov.lcs.microsoftdynamics.us) verður að nota Azure-áskrift stjórnvalda til að setja upp umhverfi hýst í skýi.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Hvað get ég gert ef ég þarf að fá pakka úr samnýttu eignasafni en hann er ekki fáanlegur í LCS fyrir GCC?

Þú getur sótt sama pakka úr Samnýttu eignasafni í [í LCS](https://lcs.dynamics.com). Einnig getur samstarfsaðili þinn hjálpað þér að sækja pakkann.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Er kóðauppfærslutólið fáanlegt í GCC?

Nei, uppfærslutólið fyrir kóða er ekki tiltækt í GCC eins og er. Hins vegar er hægt að stofna viðfangsverk í [opinberu LCS](https://lcs.dynamics.com) og nota verkfæri kóðauppfærslu. Athugið að ekki verður hægt að setja upp fleiri umhverfi viðfangsverkum.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Getur samstarfsaðili minn opnað þjónustubeiðni fyrir mína hönd?

Já. Ef samstarfsaðili þinn notar hins vegar auðkenni sem er ekki GCC verður þjónustubeiðninni beint til almennrar þjónustubiðraðar. Mælt er með að nota GCC-réttindi viðskiptavinar í LCS til að opna þjónustubeiðnir.

## <a name="see-also"></a>Sjá einnig

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Framboð á eiginleika fyrir bandaríska stjórnvöld í viðskiptaforritum](https://aka.ms/BAPFunctionalParity).
- [Notandahandbók Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Yfirlit yfir uppsetningu skýs](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

