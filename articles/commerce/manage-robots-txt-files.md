---
title: Vinna með skrárnar robots.txt
description: Þetta efnisatriði lýsir hvernig á að stjórna robots.txt skrám í Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477709"
---
# <a name="manage-robotstxt-files"></a>Vinna með skrárnar robots.txt

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stjórna robots.txt skrám í Microsoft Dynamics 365 Commerce.

Útilokunarstaðall þjarka, eða robots.txt, er staðall sem vefsíður nota til að eiga samskipti við vefþjarka. Hann leiðbeinir vefþjörkum um öll svæði á vefsíðu sem ætti ekki að heimsækja. Þjarkar eru oft notaðir af leitarvélum til að skrá vefsíður.

Til að útiloka þjarka frá netþjóni skaltu stofna skrá á netþjóninum. Í þessari skrá tilgreinirðu aðgangsstefnu fyrir þjarka. Skráin verður að vera aðgengileg með HTTP á vefslóðinni **/robots.txt**. Robots.txt skráin hjálpar leitarvélum að skrá innihaldið á vefsíðunni.

Dynamics 365 Commerce gerir þér kleift að hlaða upp robots.txt skrá fyrir lénið þitt. Fyrir hvert lén í viðskiptaumhverfi þínu geturðu hlaðið upp einni robots.txt skrá og tengt hana við það lén.

Frekari upplýsingar um robots.txt skrána er að finna á [Síður vefþjarka](https://www.robotstxt.org/).

## <a name="upload-a-robotstxt-file"></a>Hlaða upp robots.txt skrá

Eftir að þú hefur búið til og breytt robots.txt skránni þinni í samræmi við [útilokunarstaðal þjarka](https://www.robotstxt.org/orig.html) skaltu ganga úr skugga um að skráin sé aðgengileg á tölvunni þar sem þú munt nota höfundatólin fyrir viðskipti. Skráin verður að heita **robots.txt**. Til að ná sem bestum árangri verður það að vera með því sniði sem fram kemur í staðlinum. Sérhver viðskiptavinur Commerce er ábyrgur fyrir því að staðfesta og viðhalda innihaldi robots.txt skráarinnar. Til að hlaða upp robots.txt skrá verður þú að vera skráður inn í Commerce sem kerfisstjóri.

Til að hlaða upp robots.txt-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.

1. Skráðu þig inn í Commerce sem kerfisstjóri.
2. Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.
3. Undir **Stillingar leigjanda** velurðu **Robots.txt**. Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.
4. Veldu **Stjórna** til að hlaða upp robots.txt skrá fyrir lén í umhverfi þínu.
5. Á valmyndinni til hægri velurðu hnappinn **Hlaða upp** (örina sem vísar upp) við hlið lénsins sem er tengt robots.txt skránni. Gluggi skráavals birtist.
6. Í valglugganum skaltu fletta að og velja robots.txt-skrána sem þú vilt hlaða upp fyrir tengt lén og veldu síðan **Opna** til að ljúka uppflutningnum.

> [!NOTE] 
> Við upphleðslu staðfestir Commerce að skjalið sé textaskrá, en það staðfestir ekki innihald skrárinnar.

## <a name="download-a-robotstxt-file"></a>Hlaða niður robots.txt skrá

Til að hlaða niður robots.txt-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.

1. Skráðu þig inn í Commerce sem kerfisstjóri.
2. Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.
3. Undir **Stillingar leigjanda** velurðu **Robots.txt**. Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.
4. Veldu **Stjórna** til að hlaða niður robots.txt skrá fyrir lén í umhverfi þínu.
5. Á valmyndinni til hægri velurðu hnappinn **Hlaða niður** (örina sem vísar niður) við hlið lénsins sem er tengt robots.txt skránni. Gluggi skráavals birtist.
6. Í valglugganum skaltu fara á óskaðan stað á drifinu þínu, staðfesta eða slá inn skráarheiti og velja síðan **Vista** til að ljúka niðurflutningnum.

> [!NOTE]
> Þetta ferli er hægt að nota til að hlaða aðeins niður robots.txt skrám sem áður var hlaðið upp með höfundatækjum Commerce.

## <a name="delete-a-robotstxt-file"></a>Eyða robots.txt skrá

Til að eyða robots.txt-skrá á síðunni þinni í Commerce skaltu fylgja þessum skrefum.

1. Skráðu þig inn í Commerce sem kerfisstjóri.
2. Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.
3. Undir **Stillingar leigjanda** velurðu **Robots.txt**. Listi yfir öll lénin sem tengjast umhverfi þínu birtist í meginhluta gluggans.
4. Veldu **Stjórna** til að eyða robots.txt skrá fyrir lén í umhverfi þínu.
5. Á valmyndinni til hægri velurðu hnappinn **Eyða** (öskutunnutáknið) við hlið lénsins sem er tengt robots.txt skránni. Gluggi skráavals birtist.
6. Í skráavalsglugganum skaltu fletta að og velja robots.txt-skrána sem þú vilt eyða fyrir lénið og veldu síðan **Opna**. Viðvörunarskilaboð birtast.
7. Í skilaboðaglugganum velurðu **Eyða** til að staðfesta eyðingu á robots.txt file.

> [!NOTE] 
> Þetta ferli er hægt að nota til að eyða aðeins robots.txt skrám sem áður var hlaðið upp með höfundatækjum Commerce.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

[Stofna svæði fyrir rafræn viðskipti](create-ecommerce-site.md)

[Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
