---
title: Uppsetning á nýjum leigjanda rafrænna viðskipta
description: Þetta efnisatriði lýsir því hvernig á að setja upp nýtt Dynamics 365 Commerce svæði fyrir rafræn viðskipti með því að nota Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936707"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Uppsetning á nýjum leigjanda rafrænna viðskipta

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp nýtt Dynamics 365 Commerce svæði fyrir rafræn viðskipti með því að nota Microsoft Dynamics Lifecycle Services (LCS).

Microsoft Dynamics Lifecycle Services (LCS) er skýjasamvinnuvinnusvæði sem samstarfsaðilar og viðskiptavinir geta notað til að stjórna verkum sínum og umhverfi, skoða nýjustu upplýsingarnar um vörur og aðgerðir Microsoft Dynamics og stofna, fylgjast með og vafra um stuðningsatvik. Eiginleikar E-Commerce Management eru samþættir við LCS.

Til að læra meira um LCS, sjá [Notendahandbók um Lifecycle Services](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).
    
## <a name="get-started"></a>Hafist handa

Áður en hægt er að frumstilla rafræn viðskipti þarf að frumstilla verk, umhverfi og Retail Cloud Scale Unit (RCSU). Til að gera frumstillingu í LCS verður þú að hafa heimildir fyrir annað hvort verkefnaeiganda eða umhverfisstjóra. Framleiðslu- og sandkassaumhverfisgrannfræði eru studd.

Nánari upplýsingar um umhverfi, sjá [Umhverfisskipulag](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning). Frekari upplýsingar um RCSU er að finna í [Frumstilla Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).

## <a name="initialize-e-commerce"></a>Frumstilla rafræn viðskipti

Notið þetta ferli til að frumstilla eiginleika rafrænna viðskipta í umhverfi sem er til staðar.

Vertu viss um að hafa eftirfarandi nauðsynlegar upplýsingar áður en þú byrjar:

- RCSU sem notað verður.
- Öryggisflokkur Microsoft Azure Active Directory sem verður notaður fyrir kerfisstjóra í rafrænum viðskiptum.
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

> [!NOTE]
> Þessum upplýsingum má bæta síðar með þjónustubeiðni.

Eftir að þú hefur safnað nauðsynlegum upplýsingum skaltu fylgja þessum skrefum til að frumstilla rafræn viðskipti.

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com).
1. Opnið verkið sem inniheldur umhverfið þar sem á að ræsa rafræn viðskipti.
1. Í hlutanum **Umhverfi**, veldu umhverfið.
1. Undir **Eiginleikar umhverfis**, veldu tengilinn **Stjórnun smásölu**.
1. Á flipanum **rafræn viðskipti**, veldu **Uppsetning**. Gluggi birtist þar sem þú verður að slá inn upplýsingarnar sem þarf til úthlutunar.
1. Fylltu út nauðsynlegar upplýsingar og farðu síðan á næstu síðu.
1. Á næstu síðu fyllirðu út nauðsynlegar upplýsingar og sendir formið síðan. Þú ert komin/n aftur á flipann **rafræn viðskipti** þar sem þú ættir að sjá að byrjað hefur verið á frumstillingu.
1. Til að skoða frumstillingarstöðuna skaltu annaðhvort **Endurnýja** eða fara aftur á flipann **e-Commerce** seinna.
    
Þegar rafræn viðskipti eru ræst úr LCS úthlutar kerfið nokkrum hlutum sem eru nauðsynlegir fyrir rafræna viðskipti og tengir þá við umhverfið. Eftir að úthlutun er lokið er flipinn **rafræn viðskipti** á síðunni **Smásölustjórnun** uppfærð til að endurspegla úthlutunina. Á síðunni birtast nýjustu dreifingaraðgerðirnar og staðan fyrir aðrar áframhaldandi dreifingar. Þar er einnig að finna tengla á svæði fyrir rafræn viðskipti og smið rafrænna viðskipta þar sem svæði eru tengd.

## <a name="access-commerce-site-builder"></a>Access smiður rafrænna viðskipta

Til að fá aðgang að Commerce Site Builder er farið á flipann **<Rafræn viðskipti** á flipanum **Smásölustjórnun** í LCS og tengillinn **Svæðisstjórnunarverkfæri rafrænna viðskipta** valinn. Áfangasíða byggingaraðila sýnir yfirlit leigjenda. Af þessari síðu er hægt að:

- Breyta stillingum leigjenda.
- Fara á hvaða síðu sem þú hefur búið til og hefur heimild til að skoða. 
- Fara í umsögnir, eins og stjórnun og skýrslugerð.
- Stofna nýtt svæði. Nánari upplýsingar um hvernig eigi að stofna nýja síðu er að finna í [Búa til nýtt svæði fyrir rafræn viðskipti](create-ecommerce-site.md). 

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]