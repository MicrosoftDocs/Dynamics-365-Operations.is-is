---
title: Frátekningar sýnilegra birgða
description: Þetta efnisatriði lýsir því hvernig á að setja upp eiginleika frátekningar til að stofna frátekningar, nota frátekningar og/eða hætta við frátekningu á tilteknu birgðamagni með því að nota birgðasýnileika.
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
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345150"
---
# <a name="inventory-visibility-reservations"></a>Frátekningar sýnilegra birgða

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Þetta efnisatriði lýsir því hvernig á að setja upp eiginleika frátekningar til að stofna frátekningar, nota frátekningar og/eða hætta við frátekningu á tilteknu birgðamagni með því að nota birgðasýnileika.

Frátekningar merkja birgðamagn sem verður notað í framtíðinni. Þegar þú stofnar frátekningu kemur kerfið í veg fyrir að aðrar pantanir taki frá eða noti frátekinn varning þar til frátekningin er annaðhvort notuð eða hætt við hana. Frátekningar eru stofnaðar, notaðar og hætt við þær með því að nota API-köll í þjónustu birgðasýnileika.

Ef þú vilt þá getur þú sett upp Microsoft Dynamics 365 Supply Chain Management (og önnur kerfi þriðja aðila) til að sjálfkrafa mótbóka magnið sem hefur verið tekið frá með birgðasýnileika. Magni mótbókunar er eytt úr færslum frátekninga í birgðasýnileika.

Þegar þú kveikir á eiginleika frátekningar verður Supply Chain Management sjálfkrafa tilbúið til að mótbóka frátekningar sem eru gerðar með birgðasýnileika.

> [!NOTE]
> Virkni mótbókunar krefst útgáfu 10.0.22 eða nýrri af Supply Chain Management. Ef þú vilt nota frátekningar birgðasýnileika er mælt með því að bíða þangað til þú hefur uppfært Supply Chain Management í útgáfu 10.0.22 eða nýrri.

## <a name="turn-on-the-reservation-feature"></a>Kveikja á eiginleika frátekningar

Til að kveikja á eiginleika frátekningar skal fylgja þessum skrefum.

1. Í Power Apps skal opna **Birgðasýnileika**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Eiginleikastjórnun** skal kveikja á eiginleikanum *OnHandReservation*.
1. Skráðu þig inn í Supply Chain Management.
1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**.
1. Undir **Mótbókun frátekningar** skal stilla valkostinn **Virkja mótbókun frátekningar** á *Já*.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Nota eiginleika frátekningar í birgðasýnileika

Þegar þú kallar á API frátekningar merki kerfið frátekningu tiltekins varnings og magns. Þú verður að skilgreina frátekningarstigveldi og bóka beiðnir sem stemma við frátekningarstigveldið. Síðan er hægt að taka frá með því að kalla á API frátekningar.

### <a name="configure-the-reservation-hierarchy"></a>Skilgreina frátekningarstigveldið

Frátekningarstigveldið útskýrir röð vídda sem þarf að tilgreina þegar frátekningar eru gerðar. Það virkar á sama hátt og stigveldi atriðaskráar virkar fyrir lagerfyrirspurnir.

Frátekningarstigveldið getið verið öðruvísi en stigveldi atriðaskráar. Þetta sjálfstæði gerir þér kleift að innleiða flokkastjórnun þar sem notendur sundurliðað víddirnar í smáatriði til að tilgreina kröfurnar við að gera nákvæmari frátekningar.

Til að skilgreina mjúkt frátekningarstigveldi í Power Apps skal opna síðuna **Skilgreining** og því næst í flipanum **Vörpun mjúkrar frátekningar** skal setja upp frátekningarstigveldið með því að bæta við og/eða breyta víddum og stigveldi þeirra.

### <a name="call-the-reservation-api"></a>Kalla á API frátekningar

Frátekningar eru gerðar í þjónustu birgðasýnileika með því að senda bókunarbeiðni á vefslóð þjónustunnar, t.d. `/api/environment/{environment-ID}/onhand/reserve`.

Fyrir frátekningu verður meginmál beiðninnar að innihalda auðkenni fyrirtækis, afurðarkenni, frátekið magn og víddir. Beiðnin býr til einkvæmt frátekningarkenni fyrir hverja færslu frátekningar. Færsla frátekningar inniheldur einkvæma samsetningu afurðarkennis og vídda.

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

> [!NOTE]
> Virkni mótbókunar er í boði frá og með útgáfu 10.0.22

### <a name="set-up-the-reserve-offset-modifier"></a>Setja upp breytilykil fyrir mótbókun frátekningar

Breytilykill fyrir mótbókun frátekningar ákvarðar stig pöntunarúrvinnslu sem setur af stað mótbókanir. Staða á birgðafærslu pöntunar sér um að rekja stigið. Til að setja upp breytilykil fyrir mótbókun frátekningar skal fylgja þessum skrefum.

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika \> Mótbókun frátekningar**.
1. Stilltu reitinn **Breytilykill fyrir mótbókun frátekningar** á eitt af eftirfarandi gildum:

    - *Í pöntun* – Fyrir stöðuna *Í færslu* mun pöntun senda beiðni um mótbókun þegar hún er stofnuð.
    - *Taka frá* – Fyrir stöðuna *Taka frá pantaða færslu* mun pöntun senda beiðni um mótbókun þegar hún er tekin frá, tínd, fylgiseðill bókaður eða hún reikningsfærð. Beiðnin verður aðeins sett af stað í eitt skipti fyrir fyrsta skrefið þegar uppgefið ferli á sér stað.

### <a name="set-up-reservation-ids"></a>Setja upp auðkenni frátekninga

Frátekningarkennið merkir einkvæma frátekningarfærslu í birgðasýnileika. Í Supply Chain Management setja notendur frátekningar á pöntunarlínur til að merkja mótbókunina fyrir samsvarandi frátekningarfærslu.

Til að setja upp auðkenni frátekninga í Supply Chain Management skal fylgja þessum skrefum.

1. Opnaðu sölupöntun (til dæmis á síðunni **Allar sölupantanir**).
1. Í flýtiflipanum **Sölupöntunarlínur** skal velja pöntunarlínu.
1. Í flýtiflipanum **Sölupöntunarlínur**, á tækjastikunni, skal velja **Uppfæra línu \> Birgðir \> Samþætting birgðasýnileika**.
1. Sláðu inn viðeigandi auðkenni frátekninga.

Breyting á birgðastöðu stemmir við uppsetningu breytilykils mótbókunar.
