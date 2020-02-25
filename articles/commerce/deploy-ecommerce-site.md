---
title: Uppsetning á nýjum leigjanda rafrænna viðskipta
description: Þetta efni lýsir því hvernig nota á nýjan leigjanda í netverslun með því að nota Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d7dfcaf244260de5f39a1201ec1ea78e94351e7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001784"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Uppsetning á nýjum leigjanda rafrænna viðskipta


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig nota á nýtt svæði í netverslun með því að nota Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>Yfirlit

Microsoft Dynamics Lifecycle Services (LCS) er skýjasamvinnuvinnusvæði sem samstarfsaðilar og viðskiptavinir geta notað til að stjórna verkum sínum og umhverfi, skoða nýjustu upplýsingarnar um vörur og aðgerðir Microsoft Dynamics og stofna, fylgjast með og vafra um stuðningsatvik. Aðgerðir stjórnun rafrænna viðskipta eru samþættar LCS.

Til að læra meira um LCS, sjá [Notendahandbók um Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Leiðsögn

Áður en hægt er að frumstilla rafræn viðskipti verður þú að frumstilla verkefni, umhverfi og Retail Cloud Scale Unit (RCSU). Til að gera frumstillingu í LCS verður þú að hafa heimildir fyrir annað hvort verkefnaeiganda eða umhverfisstjóra. Framleiðslu- og sandkassaumhverfisgrannfræði eru studd.

Nánari upplýsingar um umhverfi, sjá [Umhverfisskipulag](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Frekari upplýsingar um RCSU er að finna í [Frumstilla Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti

Notaðu þessa aðferð til að frumstilla eiginleikann rafræn viðskipti í núverandi umhverfi.

Vertu viss um að hafa eftirfarandi nauðsynlegar upplýsingar áður en þú byrjar:

- RCSU sem notað verður.
- Microsoft Azure Active Directory öryggishópur sem notaður verður við kerfisstjórnendur e-Commerce.
- Microsoft Azure Active Directory öryggishópur sem notaður verður af gæslumönnum einkunna og umsagna.
- Lénin sem verða tengd umhverfinu.

Að auki geturðu safnað eftirfarandi valfrjálsum upplýsingum:

- Azure AD upplýsingar frá viðskiptum til neytenda (B2C):

    - Heiti leigjanda.
    - Biðlarakenni.
    - Sérstillt lén innskráninga.
    - Svarslóð.
    - Reglukenni skráningar og innskráningar.
    - Reglukenni endurstillingar aðgangsorðs.
    - Breyta auðkenni forstillingarreglu.

[!NOTE]
Þessum upplýsingum má bæta síðar með þjónustubeiðni.

Eftir að þú hefur safnað nauðsynlegum upplýsingum skaltu fylgja þessum skrefum til að frumstilla rafræn viðskipti.

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com).
1. Opnaðu verkefnið sem inniheldur umhverfið þar sem þú vilt frumstilla rafræn viðskipti.
1. Í hlutanum **Umhverfi**, veldu umhverfið.
1. Undir **Eiginleikar umhverfis**, veldu tengilinn **Stjórnun smásölu**.
1. Á flipanum **rafræn viðskipti**, veldu **Uppsetning**. Gluggi birtist þar sem þú verður að slá inn upplýsingarnar sem þarf til úthlutunar.
1. Fylltu út nauðsynlegar upplýsingar og farðu síðan á næstu síðu.
1. Á næstu síðu fyllirðu út nauðsynlegar upplýsingar og sendir formið síðan. Þú ert komin/n aftur á flipann **rafræn viðskipti** þar sem þú ættir að sjá að byrjað hefur verið á frumstillingu.
1. Til að skoða frumstillingarstöðuna skaltu annaðhvort **Endurnýja** eða fara aftur á flipann **e-Commerce** seinna.
    
Þegar rafræn viðskipti eru frumstill úr LCS, þá er kerfið með nokkra íhluti sem þarf til rafrænna viðskipta og tengir þá við umhverfið. Eftir að úthlutun er lokið er flipinn **rafræn viðskipti** á síðunni **Smásölustjórnun** uppfærð til að endurspegla úthlutunina. Á síðunni birtast nýjustu dreifingaraðgerðirnar og staðan fyrir aðrar áframhaldandi dreifingar. Það felur einnig í sér tengla á netverslunarsíðuna og vefsvæðishönnuð e-Commerce þar sem vefsvæði eru sett upp.

## <a name="access-site-builder"></a>Aðgangur að vefsvæðishönnuði

Farðu á flipann **e-Commerce** á síðunni **Verslunarstjórnun** í LCS og veldu tengilinn **Stjórnunartæki fyrir netverslun**. Áfangasíða byggingaraðila sýnir yfirlit leigjenda. Af þessari síðu er hægt að:

- Breyta stillingum leigjenda.
- Fara á hvaða síðu sem þú hefur búið til og hefur heimild til að skoða. 
- Fara í umsögnir, eins og stjórnun og skýrslugerð.
- Stofna nýtt svæði. Nánari upplýsingar um hvernig á að stofna nýtt svæði er að finna í [Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Stjórna robots.txt-skrám](manage-robots-txt-files.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
