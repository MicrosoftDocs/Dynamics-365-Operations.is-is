---
title: Orðalisti síðulíkans
description: Þetta efni lýsir hinum ýmsu þáttum sem eru notaðir á síðum Microsoft Dynamics 365 Commerce vefsvæðis.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c7b79e8b3bd68ba6246fe24916c60f476a26605
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697958"
---
# <a name="page-model-glossary"></a>Orðalisti síðulíkans

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni lýsir hinum ýmsu þáttum sem eru notaðir á síðum Microsoft Dynamics 365 Commerce vefsvæðis.

## <a name="page-element-definitions"></a>Skilgreiningar á síðueiningum

Eftirfarandi tafla gefur yfirlit yfir hugtök sem þú ættir að þekkja þegar þú breytir útliti og innihaldi vefsvæðisins. Fylgdu krækjunum fyrir ítarlegri skýringar og verklagsferli.

| Hugtak | Lýsing og athugasemdir |
|------|-----------------------|
| [Kerfiseining](work-with-modules.md) | <p>**Skilgreining:** Einingar eru byggingareining sem hægt er að skrifa og mynda beinagrind vefsíðu. Sem dæmi má nefna fyrirsagna-, hetju- og myndaræmueiningar.</p><p>**Þar sem það er valið:** Hægt er að velja og skilgreina uppsettar einingar í ýmsum stigum höfundarverkflæðis svæðis, svo sem sniðmáti, útliti, síðu og broti höfundarstigs.</p><p>**Þar sem því er breytt:** Sérsniðnar einingar eru búnar til í kóða með því að nota hugbúnaðarþróunarbúnaðinn (SDK). Þeim er síðan hlaðið inn á síðuna þína, þar sem þær verða tiltækar fyrir val.</p> |
| Eiginleiki einingar | <p>**Skilgreining:** Eiginleikar einingar eru sérstakar stillingar sem eru skilgreindar af einingunni. Hægt er að breyta þeim í höfundatækjum rafrænna viðskipta. Til dæmis eru einingareiginleikar notaðir til að stilla fyrirsögn og bakgrunnsmynd borðaeiningar.</p><p>**Þar sem það er stillt:** Eiginleikar einingar eru valdir og stillt í eiginleikaglugganum sem birtist í höfundarumhverfinu (ritstjórar) fyrir sniðmát, útlit, síður, brot og forritsstillingar.</p> |
| [Sniðmát](templates-layouts-overview.md) | <p>**Skilgreining:** Sniðmát skilgreina einingasamsetningar og valkosti sem ætti að nota fyrir flokk af síðum (til dæmis markaðssíðum, flokksíðum og vörusíðum).</p><p>**Þar sem það er valið:** Hægt er að velja sniðmát í verkflæði síðu eða útlitsstofnunar.</p><p>**Þar sem því er breytt:** Sniðmát eru skrifuð í sniðmáti ritstjóra. Enginn kóði er nauðsynlegur til að búa til eða breyta þeim.</p> |
| [Útlit](templates-layouts-overview.md) | <p>**Skilgreining:** Útlit skilgreinir endanlegt val og tilhögun eininga úr valmöguleikum yfirsniðmátsins. Hægt er að stilla útlit fyrir eina síðu (*sérsniðið útlit*), eða það er hægt að deila með mörgum síðum (*forstillt útlit*).</p><p>**Þar sem það er valið:** Hægt er að velja útlit við nýja blaðsíðu eða þegar annað útlit er nauðsynlegt fyrir núverandi síðu.</p><p>**Þar sem því er breytt:** Útlit eru skrifuð í útlitsritli. Enginn kóði er nauðsynlegur til að búa til eða breyta þeim.</p> |
| Síðutilvik | <p>**Skilgreining:** Síðuatvik skilgreina endanlegt, síðusértækt staðfært efni fyrir eina síðu. Þetta efni er dregið af gildum einingareiginleika.</p><p>**Þar sem það er valið:** Síður eru valdar þegar vefslóðum er úthlutað.</p><p>**Þar sem því er breytt:** Síðum er breytt í síðuritli. Enginn kóði er nauðsynlegur til að búa til eða breyta þeim.</p> |
| [Þema](select-site-theme.md) | <p>**Skilgreining:** Þemu skilgreina stölluð stílblöð (CSS) og ákvarða útlit eininganna sem gefnar eru upp á síðu.</p><p>**Þar sem það er valið:** Eftir að þema er hlaðið inn á síðuna þína með því að nota Microsoft Dynamics Lifecycle Services (LCS), það er hægt að velja það sem eign í síðu gámaeiningarinnar.</p><p>**Þar sem henni er breytt:** Þemu eru nú búin til og breytt með því að nota SDK. Þeim er síðan hlaðið inn á síðuna þína með því að nota LCS.</p> |
| [Brot](work-with-fragments.md) | <p>**Skilgreining:** Brot eru fullkomlega stilltar einingar sem hafa staðfært efni sem hægt er að endurnýta og uppfæra miðsvæðis á mörgum síðum. Til dæmis er hægt að nota brot sem er búið til úr hausseiningunni í öllum sniðmátum og á öllum síðum á vefsíðunni þinni og uppfæra miðlægt á einum stað.</p><p>**Þar sem það er valið:** Hægt er að velja brot hvar sem hægt er að velja einingar. Þeir geta komið í stað einingar til að auka skilvirkni með endurnýtanlegri og miðstýrðri höfundaritun.</p><p>**Þar sem því er breytt:** Brotum er breytt í brotaritli. Enginn kóði er nauðsynlegur til að búa til eða breyta þeim.</p> |
| Vefslóð | <p>**Skilgreining:** Samræmdar tilfangaslóðir (URLs) eru netföng sem vísa á vefsíður eða aðrar slóðir.</p><p>**Þar sem það er valið:** Vefslóðir eru valdar í hvert sinn sem tengla vantar á milli síðna.</p><p>**Þar sem því er breytt:** Vefslóðum er breytt í vefslóðaritli. Enginn kóði er nauðsynlegur til að búa til eða breyta þeim.</p> |
| Eign | <p>**Skilgreining:** Eignir eru tvíundarskrár sem hafa framlengingu eins og .jpg, .docx, .pdf eða .mpg.</p><p>**Þar sem það er valið:** Eignir eru valdar sem einingareiginleikar fyrir einingar sem krefjast þeirra.</p><p>**Þar sem henni er breytt:** Eignum er hlaðið upp og tilheyrandi lýsigögnum er breytt í eignastjóranum.</p> |

## <a name="additional-resources"></a>Frekari upplýsingar

[Leiðir til að bæta við efni](add-manage-content.md)

[Staða skjala og líftíma](document-states-overview.md)

[Vinna með einingar](work-with-modules.md)

[Vinna með brot](work-with-fragments.md)

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Sérstilla yfirlit svæðis](customize-site-navigation.md)
