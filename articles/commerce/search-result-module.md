---
title: Leitarniðurstöðueining
description: Þetta efnisatriði fjallar um leitarniðurstöðueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dcf3dedbb7c499135bbae45b917153854ecd4a28
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780919"
---
# <a name="search-results-module"></a>Leitarniðurstöðueining

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um leitarniðurstöðueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.

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

Fylgdu þessum skrefum til að bæta leitarniðurstöðueiningu við flokkasíðu í vefsíðugerð.

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

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Virkja birgðavitneskju fyrir einingu leitarniðurstöðu

Viðskiptavinir búast almennt við að vefsíðan fyrir rafræn viðskipti sé meðvituð um birgðahald í gegnum vafraupplifunina, svo að þeir geti ákveðið hvað þeir eigi að gera ef engar birgðir eru fyrir vöru. Hægt er að stilla leitarniðurstöðueininguna til að fella inn birgðagögn og veita eftirfarandi upplifun:

- Sýndu birgðamiða ásamt vörunni.
- Fela vörur sem eru ekki á lager af vörulistanum.
- Sýndu vörur sem eru ekki til á lager aftast á vörulistanum.
- Sía vörur í leitarniðurstöðum eftir birgðastigi.

Til að virkja þessa upplifun verður þú fyrst að virkja **Aukin vöruuppgötvun rafræn viðskipti til að vera meðvituð um birgðahald** eiginleiki í **Eiginleikastjórnun** vinnurými.

> [!NOTE]
> The **Aukin vöruuppgötvun rafræn viðskipti til að vera meðvituð um birgðahald** eiginleiki er fáanlegur í útgáfu Commerce útgáfu 10.0.20 og síðar.

Birgðameðvituð vöruleit notar vörueiginleika til að fá upplýsingar um framboð á birgðum. Sem forsenda eiginleikans þarf að búa til sérstaka vörueiginleika, slá inn birgðagögn fyrir þá og bæta þeim við netrásina. 

Til að búa til sérstaka vörueiginleika til að styðja við birgðameðvitaða leitarniðurstöðueiningu skaltu fylgja þessum skrefum.

1. Í höfuðstöðvunum, farðu til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Vörur og lager**.
1. Veldu og opnaðu **Fylltu vörueiginleika með birgðastigi**.
1. Í svarglugganum skaltu slá inn eftirfarandi upplýsingar:

    1. Í **Vörueiginleiki og tegundarheiti** reit, tilgreindu heiti fyrir sérstaka vörueigind sem verður búin til til að fanga birgðagögn.
    1. Í **Birgðaframboð byggt á** reit, veldu magntegundina sem útreikningur birgðastigs ætti að byggja á (td.**Í boði líkamlegt**). 

1. Keyrðu verkið í bakgrunni. Vegna þess að vörubirgðir breytast stöðugt í umnichannel umhverfi, mælum við eindregið með því að þú tímasetur þetta verk sem runuferli.

> [!NOTE]
> Til að fá samræmdan útreikning á birgðastigi yfir síður og einingar á netverslunarvefsíðunni þinni, vertu viss um að velja sömu magnstegund fyrir báðar **Birgðaframboð byggt á** stilling í Commerce höfuðstöðvum og **Birgðastig miðað við** stilling í Commerce site builder. Frekari upplýsingar um birgðastillingar í vefsmið er að finna í [Nota birgðastillingar](inventory-settings.md).

Til að stilla vörueiginleika fyrir netrás skaltu fylgja þessum skrefum. 

1. Í höfuðstöðvunum, farðu til **Verslun og verslun \> Rásaruppsetning \> Rásarflokkar og vörueiginleikar**.
1. Veldu netrás til að virkja birgðameðvitaða leitarniðurstöðueiningu fyrir.
1. Veldu og opnaðu tengdan eigindahóp og bættu síðan nýstofnuðu vörueigindinni við hann.
1. Fyrir viðskiptaútgáfur fyrir útgáfu 10.0.27, veldu **Stilltu lýsigögn eiginda**, veldu nýlega bætta vörueiginleikann og kveiktu síðan á **Sýna eigind á rás**, **að sækja**, **að betrumbæta**, og **Hægt að spyrjast fyrir** valkostir.
1. Fara til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**, og keyra **1150 (Vörulisti)** starf. Ef þú tímasetur **Fylltu vörueiginleika með birgðastigi** verk sem runuferli, mælum við með að þú tímasetur einnig 1150 verkið sem runuferli sem keyrir á sömu tíðni.

> [!NOTE]
> Fyrir vörur sem eru sýndar í leitarniðurstöðueiningunni er birgðastigið sýnt á aðalvörustigi í stað einstaks afbrigðisstigs. Aðeins tvö möguleg gildi eru til: „tiltækt“ og „ekki til á lager“. Raunverulegt merki fyrir gildið er sótt frá [birgðastigssnið](inventory-buffers-levels.md) skilgreiningu. Aðalafurð er aðeins talin ekki til á lager þegar öll afbrigði hennar eru ekki til á lager.

Eftir að búið er að ljúka öllum fyrri skilgreiningarskrefum munu afmarkanir á síðum leitarniðurstöðu sýna síu sem byggir á birgðum og eining leitarniðurstöðu mun sækja birgðaupplýsingar í bakgrunni. Síðan er hægt að skilgreina stillinguna **Birgðastillingar fyrir afurðalistasíður** í vefsmið Commerce til að stýra því hvernig eining leitarniðurstöðu sýnir afurðir sem ekki eru til á lager. Nánari upplýsingar er að finna í [Nota birgðastillingar](inventory-settings.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[Flýtiskoðunareining](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
