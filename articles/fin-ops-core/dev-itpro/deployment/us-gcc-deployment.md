---
title: Dynamics 365 Finance og Dynamics 365 Supply Chain Management í US Government Community Cloud (GCC)
description: Þetta efni veitir upplýsingar um Microsoft Dynamics 365 vörur frá bandarískum stjórnvöldum sem eru í boði fyrir hæfa stjórnvöld og einkaaðila.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 17702ada5bf75a44652e194c2555a83e76e7a36b
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817468"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance og Dynamics 365 Supply Chain Management í US Government Community Cloud (GCC)

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Veldu Microsoft Dynamics 365 United States (US) Ríkisvörur eru í boði fyrir hæfa stjórnvöld og einkaaðila. Þessar einingar takmarkast við eftirfarandi gerðir:

- Bandarískir alríkis-, fylkis-, staðbundnar, ættbálkar- og landstjórnarstofnanir
- Einkaaðilar sem nota Dynamics 365 US Government til að útvega lausnir til ríkisaðila eða til hæfra meðlima skýjasamfélagsins
- Einkaaðilar sem hafa viðskiptamannagögn sem eru háð reglum stjórnvalda og Dynamics 365 US Government er viðeigandi þjónusta til að uppfylla reglugerðarkröfur

Fyrir upplýsingar, sjá [Dynamics 365 Bandarísk stjórnvöld](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Innleiðing

Til að ljúka fyrstu inngöngu í innleiðingarverkefni í Microsoft Dynamics Lifecycle Services (LCS), fylgdu leiðbeiningunum í [Um borð í framkvæmdaverkefni](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Hins vegar skaltu ekki nota hlekkinn á opinbera LCS sem er að finna í þessum leiðbeiningum. Þess í stað skaltu nota eftirfarandi vefslóð til að opna LCS fyrir US Government Community Cloud (GCC):<https://gov.lcs.microsoftdynamics.us>.

Eftir að fyrstu inngöngu um borð er lokið skaltu fylgja leiðbeiningunum í [Inngangur verkefna](../lifecycle-services/project-onboarding.md). Enn og aftur, notaðu [LCS fyrir GCC](https://gov.lcs.microsoftdynamics.us) í stað opinbers LCS.

## <a name="environment-deployment"></a>Umhverfisdreifing

Eftir að þú hefur lokið inngöngu í verkefni geturðu skoðað viðbótarmöguleika LCS sem lýst er í [Lifecycle Services (LCS) fyrir Finance and Operations viðskiptavinum apps](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md). Farðu síðan yfir í umhverfisdreifingu.

- Til að dreifa Microsoft-stýrðu umhverfi í gegnum LCS skaltu fylgja leiðbeiningunum í [Lifecycle Services (LCS) fyrir Finance and Operations viðskiptavinum apps](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Fyrir skýhýst umhverfi, sjá [Dreifa og fá aðgang að þróunarumhverfi](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Þú verður einnig að ljúka viðbúnaðarferli Resource Manager fyrir tengin þín, eins og lýst er í [Ljúktu við inngönguferli Azure Resource Manager fyrir líftímaþjónustuverkefni bandarískra stjórnvalda](arm-onbarding-us-goverment.md).

> [!NOTE]
> Fyrir LCS verkefni bandarískra stjórnvalda eru aðeins Azure Government-sértækar Azure áskriftir studdar.

## <a name="features-that-arent-available"></a>Eiginleikar sem eru ekki tiltækir

Sumir eiginleikar verða ekki tiltækir fyrir uppsetningu í GCC, eða þeir verða ekki tiltækir til notkunar með Dynamics 365 í GCC. Til dæmis,Azure DevOps Þjónusta verður ekki í boði í GCC. Hins vegar á staðnum Azure DevOps eða opinbert Azure DevOps hægt er að nota þjónustu. Fyrir nákvæmar upplýsingar um tiltækileika eiginleika, sjá [Viðskiptaforrit Framboð á eiginleikum bandarískra stjórnvalda](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Algengar spurningar

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Eru Dynamics 365 Finance og Dynamics 365 Supply Chain Management studd í GCC-High?

Nr. Dynamics 365 Finance og Dynamics 365 Supply Chain Management eru aðeins studdar í GCC.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Get ég notað public Azure DevOps með fjármála- og birgðakeðjustjórnun í GCC?

Já, þú getur notað public Azure DevOps þjónustu ef þú hefur ekki kröfur um lausn sem er vottuð af Federal Risk and Authorization Management Program (FEDRAMP). Að öðrum kosti geturðu notað Azure DevOps Server.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Get ég sett upp skýhýst umhverfi Tier-1 þróunarumhverfi í Azure viðskiptaáskrift?

Nr. Í [LCS fyrir GCC](https://gov.lcs.microsoftdynamics.us), þú verður að nota Azure Government áskrift til að setja upp skýhýst umhverfi.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Hvað get ég gert ef ég þarf pakka frá Samnýtt eignasafni, en hann er ekki fáanlegur í LCS fyrir GCC?

Þú getur halað niður sama pakka frá Samnýtt eignasafni í [opinbert LCS](https://lcs.dynamics.com). Að öðrum kosti getur félagi þinn hjálpað þér að hlaða niður pakkanum.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Er kóðauppfærslutólið fáanlegt í GCC?

Nei, kóðauppfærslutólið er ekki fáanlegt í GCC eins og er. Hins vegar getur þú búið til tilvonandi verkefni í [opinbert LCS](https://lcs.dynamics.com) og notaðu kóðauppfærslutólið. Athugaðu að þú munt ekki geta notað umhverfi í tilvonandi verkefnum.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Getur félagi minn opnað stuðningsmiða fyrir mína hönd?

Já. Hins vegar, ef félagi þinn notar auðkenni sem ekki er GCC, verður stuðningsmiðanum vísað í opinberu stuðningsröðina. Við mælum með því að þú notir GCC réttindi viðskiptavina í LCS til að opna stuðningsmiða.

## <a name="see-also"></a>Sjá einnig

- [Dynamics 365 Bandarísk stjórnvöld](/power-platform/admin/microsoft-dynamics-365-government)
- [Viðskiptaforrit Framboð á eiginleikum bandarískra stjórnvalda](https://aka.ms/BAPFunctionalParity).
- [Notandahandbók Lifecycle Services (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Yfirlit yfir uppsetningu skýs](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
