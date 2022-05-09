---
title: Stuðningur við Inventory Visibility fyrir vöruhúsakerfisvörur
description: Þetta efnisatriði lýsir stuðningi við Birgðasýnileika fyrir vörur sem eru virkjaðar fyrir háþróaða vöruhúsaferli (WHS vörur).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625431"
---
# <a name="inventory-visibility-support-for-whs-items"></a>Stuðningur við Inventory Visibility fyrir vöruhúsakerfisvörur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir stuðningi við Birgðasýnileika fyrir vörur sem eru virkjaðar fyrir háþróaða vöruhúsaferli (WHS vörur). Eiginleikinn sem bætir þessari möguleika við Birgðasýnileika er nefndur *Háþróaður WHS*.

## <a name="whs-items"></a>WHS hlutir

WHS vara er vara sem er virkjuð fyrir háþróaða vöruhúsaferli (WHS) og unnin í vöruhúsi sem er einnig WHS virkt.

Fyrir frekari upplýsingar um WHS og **Vöruhússtjórnun** mát í Microsoft Dynamics 365 Supply Chain Management, sjá [Yfirlit yfir vöruhússtjórnun](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Umfang eiginleikans

Háþróaður WHS-eiginleikinn fyrir birgðasýnileika einbeitir sér að útreikningum á magni fyrir hendi sem eru byggðir á fyrirspurnum. Eiginleikinn er ekki ætlaður til að leyfa þér að nota Birgðasýnileika til að stjórna vöruhúsavinnslu almennt. Birgðasýnileiki afhjúpar ekki vöruhússsértæk hugtök fyrir notendum sínum. Hér eru nokkur dæmi um þessi hugtök:

- Frátekningarstigveldi
- Hvort vara eða vöruhús er WHS virkt
- Auðkenni röðunarflokks einingar
- Vöruhússértæk ferli, svo sem sendingar, farmur, bylgjur og vinna

Birgðasýnileiki ályktar um þessar upplýsingar, byggt á gögnunum sem eru send frá Supply Chain Management. WHS-sértæk gögn (með öðrum orðum, gögn frá`WHSInventReserve` borð) er ekki sýnilegt notendum.

Þegar þú notar Advanced WHS eiginleikann fyrir Birgðasýnileika, verða allar fyrirspurnarniðurstöður eins og niðurstöður úr fyrirspurnum sem eru gerðar beint í Supply Chain Management. Hins vegar verða þær ekki eins og niðurstöðurnar úr fyrirspurnum sem eru gerðar með því að nota vöruhússtjórnun farsímaforritið, vegna þess að farsímaforritið notar aðeins öðruvísi útreikningsrökfræði.

## <a name="when-to-use-the-feature"></a>Hvenær á að nota eiginleikann

Við mælum með því að þú notir Advanced WHS eiginleikann fyrir Birgðasýnileika í aðstæðum þar sem öll eftirfarandi skilyrði eru uppfyllt:

- Þú ert að samstilla gögn um birgðastjórnun við birgðasýnileika.
- Þú ert að nota WHS í Supply Chain Management.
- Notendur panta fyrir WHS vörur á öðrum stigum en vöruhúsastigi (til dæmis vegna þess að þú ert að nota vöruhúsavinnu).

Í öðrum tilfellum verða niðurstöður fyrirspurna við höndina þær sömu, óháð því hvort Advanced WHS eiginleiki fyrir Birgðasýnileika er virkur. Að auki verður afköst betri ef þú kveikir ekki á eiginleikanum í þessum aðstæðum, vegna þess að það eru færri útreikningar og minni kostnaður.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>Virkjaðu Advanced WHS eiginleikann fyrir birgðasýnileika

Til að virkja háþróaða WHS eiginleikann fyrir birgðasýnileika skaltu fylgja þessum skrefum.

1. Skráðu þig inn á Supply Chain Management sem stjórnandi.
1. Opnaðu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæði og virkjaðu eftirfarandi eiginleika í þessari röð:

    1. *Samþætting sýnileika birgða*
    1. *Virkja vörur vöruhúss í birgðasýnileika*

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**.
1. Á **Virkja WHS atriði** flipann, stilltu **Virkja WHS atriði** valmöguleika til *Já*.
1. Skráðu þig inn á Power Apps.
1. Opnaðu **Stillingar** síðu og síðan á **Eiginleikastjórnun** flipann, kveiktu á *AdvancedWHS* eiginleiki.
1. Í Supply Chain Management, farðu til **Vörustjórnun \> Reglubundin verkefni \> Samþætting birgðasýnileika**.
1. Á aðgerðarrúðunni velurðu **Slökkva** til að slökkva tímabundið á birgðasýnileika.
1. Á aðgerðarrúðunni velurðu **Virkja** til að virkja birgðasýnileika aftur. Viðbótin er endurhlaðin og nýi eiginleikinn er nú virkjaður. WHS-tengd gögn þín byrja að vera samstillt við Birgðasýnileika.

## <a name="query-on-hand-quantities-of-whs-items"></a>Spyrja um laust magn af WHS vörum

Til að spyrjast fyrir um WHS hluti notarðu það sama [forritunarviðmót (API) og setningafræði skilaboða](inventory-visibility-api.md) sem þú notar fyrir hluti sem ekki eru WHS. Þú þarft ekki að tilgreina hvort hlutur sé WHS vara eða ekki WHS vara. Birgðasýnileiki greinir sjálfkrafa á hlutum, byggt á gögnunum sem eru geymd.

Niðurstöður úr fyrirspurnum um WHS vörur eru í meginatriðum þær sömu og niðurstöður fyrir vörur sem ekki eru WHS. Eini munurinn er sá að eftirfarandi líkamlegar ráðstafanir frá`fno` gagnagjafar eru reiknaðir út frá WHS rökfræði í Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Allar aðrar líkamlegar mælingar eru reiknaðar alveg eins og þær eru þegar háþróaður WHS eiginleiki fyrir birgðasýnileika er óvirkur.

Fyrir nákvæmar upplýsingar um hvernig útreikningar á hendi fyrir WHS hluti virka, sjá [Pantanir í Vöruhúsastjórnun](https://www.microsoft.com/download/details.aspx?id=43284) hvítur pappír.

Gagnaeiningarnar sem fluttar eru út til Dataverse getur ekki enn uppfært magn fyrir WHS vörur. Magnið sem er sýnt í gagnaeiningunum er rétt bæði fyrir vörur sem ekki eru WHS og fyrir magn sem eru ekki fyrir áhrifum af WHS rökfræði (þ.e. mælingar nema`AvailPhysical`,`AvailOrdered`,`ReservPhysical`, og`ReservOrdered` í`fno` gagnagjafa).

Breytingar á WHS vörumagni sem eru geymdar í gagnagjafanum Supply Chain Management eru bannaðar. Hvað varðar aðra eiginleika birgðasýnileika er þessari takmörkun framfylgt til að koma í veg fyrir árekstra.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>Mjúkir fyrirvarar á WHS hlutum í birgðasýnileika

Almennt, [mjúkir fyrirvarar](inventory-visibility-reservations.md) á WHS atriði eru studd. Þú getur tekið með WHS-tengdar líkamlegar ráðstafanir í mjúkum fyrirvaraútreikningum. 

Í þekktri takmörkun er *hægt að panta* útreikningur er ekki studdur eins og er fyrir WHS hluti. Þess vegna, ef það er fyrirvari yfir núverandi víddum þar sem mjúkur fyrirvari á sér stað, *hægt að panta* útreikningur er rangur. Mjúkar bókanir verða ekki fyrir áhrifum þegar **ifCheckAvailForReserv** valkosturinn er óvirkur í [soft reservation API](inventory-visibility-api.md#create-one-reservation-event).

Þessi þvingun á einnig við um eiginleika og sérstillingar sem byggjast á mjúkum fyrirvörum (eins og úthlutun).

## <a name="calculate-available-to-promise-quantities"></a>Reiknaðu magn sem er tiltækt til að lofa

Lausnin styður að fullu [hægt að lofa (ATP)](inventory-visibility-available-to-promise.md) fyrir WHS hluti. Þú getur skilgreint ATP útreikninga án þess að hafa áhyggjur af WHS-sértækum upplýsingum.
