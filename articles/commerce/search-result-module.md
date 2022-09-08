---
title: Leitarniðurstöðueining
description: Þessi grein fjallar um einingar fyrir leitarniðurstöður og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: eeb7cd0769fcb866a3d7dcc03e8e87daf24b2c5d
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405294"
---
# <a name="search-results-module"></a>Leitarniðurstöðueining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um einingar fyrir leitarniðurstöður og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Leitarniðurstöðueiningin skilar leitarniðurstöðum afurðar og lista yfir viðeigandi afmarkanir fyrir afurðirnar. Hægt er að nota leitarniðurstöðueiningar á svæðinu Dynamics 365 Commerce til að birta síður fyrir eftirfarandi aðstæður:

- Leitarniðurstöður sem koma til vegna leitar notanda
- Leitarniðurstöður sem sýna tiltekið safn afurða á borð við „Versla svipaðar vörur“
- Afurðalistar sem tilheyra flokki

Frekari upplýsingar um síður flokka og leitarniðurstaðna er að finna í [Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md).

Eftirfarandi mynd sýnir dæmi um leitarniðurstöðusíðu fyrir flokk á Fabrikam-svæðinu.

![Dæmi um leitarniðurstöðusíðu á Fabrikam-svæðinu.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Eiginleikar leitarniðurstöðueiningar

Í eftirfarandi töflu er listi yfir eiginleika leitarniðurstöðueininga, ásamt gildum þeirra og lýsingum.

| Eiginleiki | Gildi | lýsing |
|----------|--------|-------------|
| Vörur á síðu | Heiltala | Fjöldi vara sem á að sýna á hverri síðu. |
| Leyfa aftur á PDP | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt**, þegar notandi velur afurð á leitarniðurstöðusíðunni, mun brauðmylsnuleiðsögnin á upplýsingasíðu afurðar sem er opnuð sýna tengil fyrir „Aftur í niðurstöður“. |
| Fjölga afmörkunum | **Allt**, **1**, **2**, **3** eða **4** | Fjöldi afmarkana efst sem á að víkka út þegar síða er hlaðin. Ef þessi eiginleiki er til dæmis stilltur á **3** verða fyrstu þrjár afmarkanir á síðunni víkkaðar út. |
| Fela tegundastigveldi | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verður tegundastigveldið sem sýnt er á síðunni falið. Þennan eiginleika ætti að stilla á **Satt** ef notuð er [brauðmylsnueiningin](add-breadcrumb.md) til að sýna tegundastigveldið.|
| Hafa afurðareigindir með í leitarniðurstöðum | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verður eigindum skilað fyrir afurðirnar í leitarniðurstöðunum. Þrátt fyrir að hægt sé að sýna þessar eigindir á Commerce-svæði er þörf á viðbót.|
| Sýna tengsl verðs | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verða tengd verð afurðanna sýnd í leitarniðurstöðum þegar innskráður notandi skoðar síðuna. |
| Uppfæra afmörkunarsvæði | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** verður afmörkunarsvæðið uppfært þegar afmarkanir eru valdar. Í þessari stillingu virka sumar fjölvalsafmarkanir eins og einvalsafmarkanir þegar afmörkunarsvæðið er uppfært. |

> [!IMPORTANT]
> Í Commerce útgáfu 10.0.16 eða nýrri er hægt að nota skilgreininguna **Sýna tengsl verðs** til að sýna verðtengsl á síðunni.
>
> Í Commerce útgáfu 10.0.20 og nýrri er hægt að nota skilgreininguna **Uppfæra afmörkunarsvæði** til að uppfæra afmörkunarsvæðið við val á afmörkun.

## <a name="supported-modules"></a>Studdar einingar

Leitarniðurstöðueiningin styður [flýtiskoðunareininguna](quick-view-module.md), sem gerir notendum kleift að skoða afurðarupplýsingar og bæta vörum við körfuna úr síðu leitarniðurstaðna.

## <a name="add-a-search-results-module-to-a-category-page"></a>Bæta leitarniðurstöðueiningu við flokkasíðu

Fylgdu þessum skrefum til að bæta leitarniðurstöðueiningu við flokkasíðu í vefsvæðisgerð.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát** skal slá inn heitið **Leitarniðurstöður** og síðan velja **Í lagi**.
1. Í **Líkami** rauf, veldu sporbaug (...) og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Sjálfgefin síða** mát og veldu síðan **Allt í lagi**.
1. Í **Aðal** rifa á **Sjálfgefin síða** mát, veldu sporbaug (...) og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (...) og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Brauðmola** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæðinu **Brauðmylsna** skal færa inn gildið **1** fyrir **Lágmark atvika**.
1. Í **Ílát** rauf, veldu sporbaug (...) og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Leitarniðurstöður** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæðinu **Leitarniðurstöður** skal slá inn gildið **1** fyrir **Lágmark atvika** og síðan stilla alla aðra nauðsynlega eiginleika fyrir leitarniðurstöðueininguna. Með því að stilla þessa eiginleika í sniðmátinu er gengið úr skugga um að allar sérstillingar á tiltekinni flokkasíðu muni sjálfkrafa hafa með þessar stillingar.
1. Veldu **Ljúka við breytingar** og síðan **Birta** til að birta sniðmátið.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Flokkasíðu**, og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu **Leitarniðurstöður** sniðmát sem þú bjóst til og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="inventory-aware-search-results-module"></a>Birgðameðvituð leitarniðurstöðueining

Hægt er að stilla leitarniðurstöðueininguna til að fella inn birgðagögn og veita eftirfarandi reynslu:

- Sýndu merkimiða á birgðastigi við hlið afurða.
- Fela vörur sem eru ekki á lager af vörulistanum.
- Birta vörur sem eru ekki til á lager í lok vörulistans.
- Styðja vörusíun sem byggir á birgðum.

Til að virkja þessa upplifun verður þú fyrst að virkja **Aukin vöruuppgötvun rafræn viðskipti til að vera meðvituð um birgðahald** eiginleika, og stilltu síðan nokkrar forkröfustillingar í höfuðstöðvum Commerce. Fyrir frekari upplýsingar, sjá [Birgðameðvituð vöruskráning](inventory-aware-product-listing.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[Flýtiskoðunareining](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
