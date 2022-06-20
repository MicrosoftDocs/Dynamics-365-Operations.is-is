---
title: Frátekningar Inventory Visibility
description: Þessi grein lýsir því hvernig á að setja upp pöntunareiginleikann til að búa til pantanir, neyta bókana og/eða afpanta tiltekið birgðamagn með því að nota Birgðasýnileika.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3b74907709ab97ddf4cc829dba324df213ca229f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895729"
---
# <a name="inventory-visibility-reservations"></a>Frátekningar Inventory Visibility

[!include [banner](../includes/banner.md)]


Þessi grein lýsir því hvernig á að setja upp pöntunareiginleikann til að búa til pantanir, neyta bókana og/eða afpanta tiltekið birgðamagn með því að nota Birgðasýnileika.

Frátekningar merkja birgðamagn sem verður notað í framtíðinni. Þegar þú stofnar frátekningu kemur kerfið í veg fyrir að aðrar pantanir taki frá eða noti frátekinn varning þar til frátekningin er annaðhvort notuð eða hætt við hana. Frátekningar eru stofnaðar, notaðar og hætt við þær með því að nota API-köll í þjónustu birgðasýnileika.

Ef þú vilt þá getur þú sett upp Microsoft Dynamics 365 Supply Chain Management (og önnur kerfi þriðja aðila) til að sjálfkrafa mótbóka magnið sem hefur verið tekið frá með birgðasýnileika. Magni mótbókunar er eytt úr færslum frátekninga í birgðasýnileika.

Þegar þú kveikir á eiginleika frátekningar verður Supply Chain Management sjálfkrafa tilbúið til að mótbóka frátekningar sem eru gerðar með birgðasýnileika.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Kveikja á og setja upp eiginleika frátekningar

Til að kveikja á eiginleika frátekningar skal fylgja þessum skrefum.

1. Skráðu þig inn í Power Apps og opnaðu **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Eiginleikastjórnun** skal kveikja á eiginleikanum *OnHandReservation*.
1. Skráðu þig inn í Supply Chain Management.
1. Farðu á **[Vinnusvæði eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og virkjaðu eiginleikann *Samþætting birgðasýnileika með mótbókun frátekningar* (krefst útgáfu 10.0.22 eða síðar).
1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**, opnaðu flipann **Mótbókun frátekningar** og gerðu eftirfarandi stillingar:
    - **Virkja mótbókun frátekningar** – Stilltu á *Já* til að virkja þessa virkni.
    - **Breytilykill fyrir mótbókun frátekningar** – Veldu stöðu birgðafærslu sem mun mótbóka frátekningar sem gerðar eru í birgðasýnileika. Þessi stilling ákvarðar stöðu pöntunarúrvinnslu sem setur af stað mótbókanir. Staða á birgðafærslu pöntunar sér um að rekja stigið. Veljið um eitt af eftirfarandi:
        - *Í pöntun* – Fyrir stöðuna *Í færslu* mun pöntun senda beiðni um mótbókun þegar hún er stofnuð. Magn mótbókunar verður magn stofnaðrar pöntunar.
        - *Taka frá* – Fyrir stöðuna *Taka frá pantaða færslu* mun pöntun senda beiðni um mótbókun þegar hún er tekin frá, tínd, fylgiseðill bókaður eða hún reikningsfærð. Beiðnin verður aðeins sett af stað í eitt skipti fyrir fyrsta skrefið þegar uppgefið ferli á sér stað. Magn mótbókunar verður magnið þar sem staða birgðafærslu breyttist úr *Í pöntun* í *Frátekið pantað* (eða síðari staða) í samsvarandi pöntunarlínu.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Nota eiginleika frátekningar í birgðasýnileika

Þegar þú kallar á API frátekningar merki kerfið frátekningu tiltekins varnings og magns. Þú verður að skilgreina frátekningarstigveldi og bóka beiðnir sem stemma við frátekningarstigveldið. Síðan er hægt að taka frá með því að kalla á API frátekningar.

### <a name="configure-the-reservation-hierarchy"></a>Skilgreina frátekningarstigveldið

Frátekningarstigveldið útskýrir röð vídda sem þarf að tilgreina þegar frátekningar eru gerðar. Það virkar á sama hátt og stigveldi atriðaskráar virkar fyrir lagerfyrirspurnir.

Frátekningarstigveldið getið verið öðruvísi en stigveldi atriðaskráar. Þetta sjálfstæði gerir þér kleift að innleiða flokkastjórnun þar sem notendur sundurliðað víddirnar í smáatriði til að tilgreina kröfurnar við að gera nákvæmari frátekningar.

Til að skilgreina mjúkt frátekningarstigveldi í Power Apps skal opna síðuna **Skilgreining** og því næst í flipanum **Stigveldi mjúkrar frátekningar** skal setja upp frátekningarstigveldið með því að bæta við og/eða breyta víddum og stigveldi þeirra.

Mjúka frátekningastigveldið ætti að innihalda `SiteId` og `LocationId` sem þætti vegna þess að þeir setja saman skilgreiningu þáttunarinnar.

Frekari upplýsingar um hvernig á skilgreina frátekningar er að finna í [Skilgreining frátekningar](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Kalla á API frátekningar

Frátekningar eru gerðar í þjónustu birgðasýnileika með því að senda bókunarbeiðni á vefslóð þjónustunnar, t.d. `/api/environment/{environment-ID}/onhand/reserve`.

Fyrir frátekningu verður meginmál beiðninnar að innihalda auðkenni fyrirtækis, afurðarkenni, frátekið magn og víddir. Beiðnin býr til einkvæmt frátekningarkenni fyrir hverja færslu frátekningar. Færsla frátekningar inniheldur einkvæma samsetningu afurðarkennis og vídda.

Þegar þú kallar á API frátekningu er hægt að stjórna staðfestingu frátekningar með því að tilgreina Boolean `ifCheckAvailForReserv` færibreytu í meginmáli beiðninnar. Gildi `True` þýðir að staðfesting sé nauðsynleg og á móti merkir gildið `False` að staðfestingin er ekki nauðsynleg. Sjálfgefið gildi er `True`.

Ef þú vilt hætta við frátekningu eða afturkalla frátekningu á tilgreindu birgðamagni skaltu stilla magnið á neikvætt gildi og stilla `ifCheckAvailForReserv` færibreytuna á `False` til að sleppa villuleitinni.

Hér er dæmi um meginmál beiðni til viðmiðunar.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Frátekningar mótbókunar í Supply Chain Management

Fyrir stöður birgðafærslu sem fela í sér tiltekinn breytilykil fyrir mótbókun frátekningar mun uppfærsla færslunnar mótbóka samsvarandi frátekningarfærslu þegar öllum eftirfarandi skilyrðum er mætt:

- Frátekningarkennið í birgðafærslunni samsvarar frátekningarkenni frátekningarfærslunnar í þjónustu birgðasýnileika.
- Víddir birgðafærslunnar samsvara víddum frátekningarfærslunnar í þjónustu birgðasýnileika.
- Breytingar á stöðu birgðafærslu kveikir á mótbókun fyrir frátekningar þegar staða birgðafærslu endurspeglar þá staðreynd að pöntunarferlinu sé lokið eða því sleppt.

Mótbókað magn fylgir birgðamagninu sem er tilgreint í birgðafærslum. Mótbókunin tekur ekki gildi ef ekkert frátekið magn er áfram í þjónustu birgðasýnileika.

### <a name="set-up-the-reservation-offset-modifier"></a>Setja upp breytilykil fyrir mótbókun frátekningar

Ef þú hefur ekki gert það nú þegar skaltu setja upp breytilykil frátekningar eins og lýst er í [Kveikja á og setja upp eiginleika frátekningar](#turn-on).

### <a name="set-up-reservation-ids"></a>Setja upp auðkenni frátekninga

Frátekningarkennið merkir einkvæma frátekningarfærslu í birgðasýnileika. Í Supply Chain Management setja notendur frátekningar á pöntunarlínur til að merkja mótbókunina fyrir samsvarandi frátekningarfærslu.

Til að setja upp auðkenni frátekninga í Supply Chain Management skal fylgja þessum skrefum.

1. Opnaðu sölupöntun (til dæmis á síðunni **Allar sölupantanir**).
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja pöntunarlínu.
1. Í flýtiflipanum **Sölupöntunarlínur**, á tækjastikunni, skal velja **Uppfæra línu \> Birgðir \> Samþætting birgðasýnileika**.
1. Sláðu inn viðeigandi auðkenni frátekninga.

Breyting á birgðastöðu stemmir við uppsetningu breytilykils mótbókunar.
