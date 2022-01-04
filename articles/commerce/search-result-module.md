---
title: Leitarniðurstöðueining
description: Þetta efnisatriði fjallar um leitarniðurstöðueiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/15/2021
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
ms.openlocfilehash: bae825ed7093494c48abac119c480be0dba4f951
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919475"
---
# <a name="search-results-module"></a>Leitarniðurstöðueining

[!include [banner](includes/banner.md)]


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

Til að bæta leitarniðurstöðueiningu við flokkasíðu skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát** skal slá inn heitið **Leitarniðurstöður** og síðan velja **Í lagi**.
1. Í hólfinu **Meginmál** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.
1. Í svarglugganum **Bæta við einingu** skal velja eininguna **Brauðmylsna** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu **Brauðmylsna** skal færa inn gildið **1** fyrir **Lágmark atvika**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (...) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Leitarniðurstöður** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu **Leitarniðurstöður** skal slá inn gildið **1** fyrir **Lágmark atvika** og síðan stilla alla aðra nauðsynlega eiginleika fyrir leitarniðurstöðueininguna. Með því að stilla þessa eiginleika í sniðmátinu er gengið úr skugga um að allar sérstillingar á tiltekinni flokkasíðu muni sjálfkrafa hafa með þessar stillingar.
1. Veldu **Ljúka við breytingar** og síðan **Birta** til að birta sniðmátið.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í glugganum **Velja sniðmát** skal velja sniðmátið **Leitarniðurstöður** sem var búið til, slá inn **Flokkasíða** fyrir **Síðuheit** og síðan velja **Í lagi**. Þar sem öll gildin eru stillt í sniðmátinu er síðan tilbúin til birtingar.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Virkja birgðavitneskju fyrir einingu leitarniðurstöðu

Viðskiptavinir gera almennt ráð fyrir að svæði rafrænna viðskipta hafi vitneskju um birgðir í gegnum flettiupplifunina þannig að þeir geti ákveðið hvað skuli gera ef engar birgðir eru til fyrir afurð. Hægt er að bæta einingu leitarniðurstöðu þannig að hún taka til greina birgðaupplýsingar og bjóði upp á eftirfarandi upplifanir:

- Sýna merki um framboð birgða með afurðum.
- Fela afurðir sem ekki eru til á lager.
- Sýna afurðir sem ekki eru til á lager neðst á lista yfir leitarniðurstöður.
    
Til að virkja þessar upplifanir þarf að skilgreina eftirfarandi stillingar skilyrða í Commerce Headquarters.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Virkja eiginleikann fyrir bætta uppgötvun afurða í rafrænum viðskiptum þannig að birgðir verði teknar til greina

> [!NOTE]
> Eiginleikinn **Bætt uppgötvun afurða í rafrænum viðskiptum þannig að birgðir verði teknar til greina** er í boði frá og með útgáfu 10.0.20 af Commerce.

Til að virkja eiginleikann **Bætt uppgötvun afurða í rafrænum viðskiptum þannig að birgðir verði teknar til greina** í Commerce Headquarters skal fylgja þessum skrefum.

1. Opna skal **Vinnusvæði \> Eiginleikastjórnun**.
1. Leitaðu að eiginleikanum **Bætt uppgötvun afurða í rafrænum viðskiptum þannig að birgðir verði teknar til greina** og virkjaðu hann svo.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Stilltu verkið Fylla út afurðareigindir með birgðastöðu

Verkið **Fylla út afurðareigindir með birgðastöðu** býr til nýja afurðareigind til að sækja birgðaframboð og stillir síðan eigindina á nýjasta gildi birgðastöðu fyrir hverja aðalafurð. Þar sem birgðaframboð afurðar eða vöruúrval sem er selt breytist stöðugt mælum við eindregið með því að verkið verði tímasett sem runuvinnsla.

Til að skilgreina verkið **Fylla út afurðareigindir með birgðastöðu** í Commerce Headquarters skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Upplýsingatækni smásölu og viðskipta \> Afurðir og birgðir**.
1. Velja **Fylla út afurðareigindir með birgðastöðu**.
1. Í svarglugganum **Fylla út afurðareigindir með birgðastöðu** skal fylgja þessum skrefum:

    1. Undir **Færibreytur**, í reitnum **Afurðareigind og heiti gerðar**, skal tilgreina heiti fyrir sérstaka afurðareigind sem verður stofnuð til að sækja birgðaframboð.
    1. Undir **Færibreytur**, í reitnum **Birgðaframboð samkvæmt**, skal velja magnið sem útreikningur birgðastöðu á að byggja á (til dæmis **Efnislegt magn til ráðstöfunar**).
    1. Undir **Keyra í bakgrunni** skal skilgreina verkið sem á að keyra í bakgrunni og valfrjálst kveikja á valkostinum **Runuvinnsla**. 

> [!NOTE]
> Til að fá stöðugan útreikning á birgðastöðu á upplýsinga- og listasíðum afurða á svæði rafrænna viðskipta skal ganga úr skugga um að velja sama valkost magns fyrir bæði stillinguna **Birgðaframboð samkvæmt** í Commerce Headquarters og stillinguna **Birgðastaða samkvæmt** í vefsmið Commerce. Frekari upplýsingar um birgðastillingar í vefsmið er að finna í [Nota birgðastillingar](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Skilgreina nýja afurðareigind

Þegar búið er keyra verkið **Fylla út afurðareigindir með birgðastöðu** þarf að skilgreina nýlega stofnaða afurðareigind á svæði rafrænna viðskipta þar sem þú vilt virkja birgðavitneskju fyrir einingu leitarniðurstöðu.

Til að skilgreina nýja afurðareigind í Commerce Headquarters skal fylgja þessum skrefum.

1. Farðu í **Smásala og viðskipti \> Uppsetning rásar \> Rásarflokkar og afurðareigindir** og veldu svæði rafrænna viðskipta.
1. Veldu og opnaðu viðkomandi eigindaflokk, bættu nýlega stofnaðri afurðareigind við hann og lokaðu svo síðunni.
1. Veldu **Stilla lýsigögn eigindar**, veldu nýlega viðbættri afurðareigind og kveiktu svo á valkostunum **Sýna eigind á rás**, **Hægt að sækja**, **Fínstilling möguleg** og **Fyrirspurn möguleg**.

> [!NOTE]
> Fyrir afurðir sem eru sýndar í einingu leitarniðurstöðu er birgðastaðan færð inn á stig aðalafurðar í staðinn fyrir einstök afbrigðisstig. Aðeins tvö möguleg gildi eru til: „tiltækt“ og „ekki til á lager“. Raunverulegur texti fyrir gildin er sóttur úr skilgreiningunni [forstilling birgðastöðu](inventory-buffers-levels.md). Aðalafurð er aðeins talin ekki til á lager þegar öll afbrigði hennar eru ekki til á lager. Birgðastaða afbrigðis er ákvarðað samkvæmt skilgreiningu á forstillingu birgðastöðu afurðarinnar. 

Eftir að búið er að ljúka öllum fyrri skilgreiningarskrefum munu afmarkanir á síðum leitarniðurstöðu sýna síu sem byggir á birgðum og eining leitarniðurstöðu mun sækja birgðaupplýsingar í bakgrunni. Síðan er hægt að skilgreina stillinguna **Birgðastillingar fyrir afurðalistasíður** í vefsmið Commerce til að stýra því hvernig eining leitarniðurstöðu sýnir afurðir sem ekki eru til á lager. Nánari upplýsingar er að finna í [Nota birgðastillingar](inventory-settings.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu](category-search-page-overview.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[Flýtiskoðunareining](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
