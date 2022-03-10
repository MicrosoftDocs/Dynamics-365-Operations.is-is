---
title: Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu
description: Þetta efni veitir yfirlit yfir sjálfgefna áfangasíðu flokks og leitarniðurstöðusíðu í Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f61ee8ec212185e195e2cf1a9d6d25c31e4f672
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982435"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu

[!include [banner](includes/banner.md)]

Þetta efni veitir yfirlit yfir sjálfgefna áfangasíðu flokks og leitarniðurstöðusíðu í Microsoft Dynamics 365 Commerce rafræn viðskipti.

## <a name="default-category-landing-page"></a>Sjálfgefin lendingarsíða flokks

Sjálfgefin lendingasíða flokks er sú síðu sem notendur vefsíðna eru venjulega færðir til þegar þeir velja flokk í yfirlitsstigveldi. Flokkasíðan gerir þér kleift að fletta og einnig er hægt að flokka og fínstilla flokkaðar vörur.

![Sjálfgefin lendingarsíða flokks.](./media/SimpleCategoryLandingDressCategory.png)

Efst á síðunni er haus sem sýnir alla vöruflokka og aðrar síður sem vörustjórinn hefur flokkað. Stillingar eru gerðar sem hluti af stillingum yfirlitsstigveldis rásar. Neðst á síðunni er fótur sem inniheldur fljótlega tengla á ýmis efni sem kaupandi gæti haft áhuga á.

Eftirfarandi þættir eru nauðsynlegir fyrir flokk:

- **Afurðastaðsetningarritir** sýna vörurnar sem verslunarstjórinn hefur skilgreint í flokk sem hluta af stillingum yfirlitsstigveldisins.
- **Yfirlit yfir hreinsara og val** eru síur sem veita fjölda og sem hægt er að nota til að fínstilla vörur. Vörustjórinn stillir þá sem hluta af uppsetningu lýsigagnanna sem tengjast rásaflokkum og afurðareigindum.
- **Flokkunarvalkostir** eru notaðir af gestum vefsíðna til að flokka vörurnar. Sjálfgefið er að eftirfarandi flokkunarvalkostir eru tiltækir:

    - Verð – lægsta til hæsta
    - Verð – hæsta til lægsta
    - Afurðaheiti – \[A-Z\]
    - Afurðaheiti – \[Z-A\]
    - Einkunnir – lægsta til hæsta
    - Einkunnir – hæsta til lægsta

- **Síðuskipting** gerir gestum vefsíðu kleift að fara af einni síðu með flokkaðar vöruniðurstöður á aðra síðu.
- **Heildarfjöldi** veitir heildarfjölda vara sem eru skilgreindar í flokk.

## <a name="enrich-a-category-landing-page"></a>Bæta lendingarsíðu flokks

Ef þú vilt að lendingasíða flokks hafi sérsniðnari reynslu fyrir ákveðinn flokk geturðu „auðgað“ lendingarsíðuna fyrir þann flokk. Til dæmis er hægt að bæta við markaðssetningarmyndbandi og sögufrásögn í flokknum til að ná athygli kaupandans. Sjá frekari upplýsingar [Bæta lendingarsíðu flokks](enrich-category-page.md).

![Bætt lendingarsíða flokks.](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Niðurstöðusíður sjálfvirkra uppástungna og leitar

Notendur vefsíðna geta kannað síðu annaðhvort með því að fara í flokk úr yfirlitsstigveli eða með því að slá inn leitarorð í leitarreitinn.

Um leið og notendur byrja að slá inn í leitarreitinn upplifa þeir þá heildstæðu sjálfvirkni sem stingur upp á leitarskilyrðum.

Hér eru nokkrar af þeim tegundum tillagna sem gætu verið sýndar:

- **Lykilorð** eru notuð til að finna vörur í öllum afurðum sem eru flokkaðar í rásina.
- **Afurðir** veita beina tengla á upplýsingasíðu afurða.
- **Leitartillögur fyrir víðtækan flokk** skráir ýmsa flokka og lætur notendur leita að leitarorðinu í tilteknum flokki.

![Heildstæð sjálfvirk tillaga.](./media/ImmersiveAutoSuggestUX.png)

Þegar notendur velja eitt af lykilorðum eða víðtækum leitarflokkum í leitartillögum eða ef það eru engar tillögur að leitarorðinu sem þeir slá inn, er þeim vísað á leitarniðurstöðusíðuna. Notendur geta síðan flett, flokkað og betrumbætt lista yfir leitarniðurstöður til að finna þá vöru sem óskað er.

![Leitarlending.](./media/SearchLanding.png)

Eftirfarandi þættir eru nauðsynlegir fyrir leitarniðurstöðusíðu:

- **Afurðastaðsetningarreitir** sýna afurðir fyrir notandaleitina. Sjálfgefið er að þessir reitir séu flokkaðir eftir skýjadrifnu mikilvægisstigi leitar fyrir notendaleit.
- **Yfirlit yfir hreinsara og val** eru síur sem veita fjölda og sem hægt er að nota til að fínstilla vörur. Vörustjórinn stillir þá sem hluta af uppsetningu lýsigagnanna sem tengjast lýsigögnum „rásaflokka og afurðareiginda“.
- **Flokkunarvalkostir** eru notaðir af gestum vefsíðna til að flokka vörurnar. Sjálfgefið er að eftirfarandi flokkunarvalkostir eru tiltækir:

    - Verð – lægsta til hæsta
    - Verð – hæsta til lægsta
    - Afurðaheiti – \[A-Z\]
    - Afurðaheiti – \[Z-A\]
    - Einkunnir – lægsta til hæsta
    - Einkunnir – hæsta til lægsta
    - Sjálfgefinn

- **Síðuskipting** gerir gestum vefsíðu kleift að fara af einni síðu með flokkaðar vöruniðurstöður á aðra síðu.
- **Heildarfjöldi** veitir heildarfjölda vara sem eru skilgreindar í flokk og samsvara leitarskilyrðum.

>[!NOTE]
>Þessir leitareiginleikar í skýi eru tiltækir frá útgáfu 10.0.8. Gangið úr skugga um að undir **Viðskiptafæribreytur > Skilgreiningarfæribreytur** sé færsla fyrir „ProductSearch.UseAzureSearch stillt á true“. 
![Færibreytur skilgreininga fyrir leit í skýinu.](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Leitaryfirlit í skýinu](cloud-powered-search-overview.md)

[Yfirlit heimasíðu](quick-tour-home-page.md)

[Yfirlýt upplýsingasíðu afurða](quick-tour-pdp.md)

[Yfirlit yfir síður körfu og greiðsluferlis](quick-tour-cart-checkout.md)

[Yfirlit yfir síður fyrir stjórnun reikninga](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]