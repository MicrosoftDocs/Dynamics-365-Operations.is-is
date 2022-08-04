---
title: Stuðningur við birgðasýnileika fyrir WMS hluti
description: Þessi grein lýsir stuðningi við Birgðasýnileika fyrir vörur sem eru virkjaðar fyrir vöruhúsastjórnunarferli (WMS vörur).
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
ms.openlocfilehash: 54ce637d2d7b590988f7590eae5248276bcc4b96
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066611"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Stuðningur við birgðasýnileika fyrir WMS hluti

[!include [banner](../includes/banner.md)]

Þessi grein lýsir stuðningi við Birgðasýnileika fyrir vörur sem eru virkjaðar fyrir vöruhúsastjórnunarferli (WMS). Eiginleikinn sem bætir þessum möguleika við Birgðasýnileika er nefndur *Ítarlegt WMS*.

## <a name="wms-items"></a>WMS atriði

WMS vara er vara sem er virkjuð fyrir WMS og unnin í vöruhúsi sem einnig er WMS virkt.

Fyrir frekari upplýsingar um WMS og **Vöruhússtjórnun** mát í Microsoft Dynamics 365 Supply Chain Management, sjá [Yfirlit yfir vöruhússtjórnun](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>Umfang eiginleikans

Ítarlegri WMS-eiginleikinn fyrir Birgðasýnileika einbeitir sér að útreikningum á magni fyrir hendi sem byggjast á fyrirspurnum. Eiginleikinn er ekki ætlaður til að leyfa þér að nota Birgðasýnileika til að stjórna vöruhúsavinnslu almennt. Birgðasýnileiki afhjúpar ekki vöruhússsértæk hugtök fyrir notendum sínum. Hér eru nokkur dæmi um þessi hugtök:

- Frátekningarstigveldi
- Hvort vara eða vöruhús er WMS virkt
- Auðkenni röðunarflokks einingar
- Vöruhússértæk ferli, svo sem sendingar, farmur, bylgjur og vinna

Birgðasýnileiki ályktar um þessar upplýsingar, byggt á gögnum sem eru send frá Supply Chain Management. WMS-sértæk gögn (með öðrum orðum, gögn frá`WHSInventReserve` borð) er ekki sýnilegt notendum.

Þegar þú notar Advanced WMS eiginleikann fyrir Birgðasýnileika, verða allar fyrirspurnarniðurstöður eins og niðurstöður úr fyrirspurnum sem eru gerðar beint í Supply Chain Management. Hins vegar verða þær ekki eins og niðurstöðurnar úr fyrirspurnum sem eru gerðar með því að nota vöruhússtjórnun farsímaforritið, vegna þess að farsímaforritið notar aðeins öðruvísi útreikningsrökfræði.

## <a name="when-to-use-the-feature"></a>Hvenær á að nota eiginleikann

Við mælum með því að þú notir Advanced WMS eiginleikann fyrir Birgðasýnileika í aðstæðum þar sem öll eftirfarandi skilyrði eru uppfyllt:

- Þú ert að samstilla Supply Chain Management gögn við Birgðasýnileika.
- Þú ert að nota WMS í Supply Chain Management.
- Notendur panta WMS vörur á öðrum stigum en vöruhúsastigi (til dæmis vegna þess að þú ert að nota vöruhúsavinnu).

Í öðrum tilfellum verða niðurstöður fyrirspurna við höndina þær sömu, óháð því hvort Advanced WMS eiginleiki fyrir Birgðasýnileika er virkur. Að auki verður afköst betri ef þú kveikir ekki á eiginleikanum í þessum aðstæðum, vegna þess að það eru færri útreikningar og minni kostnaður.

## <a name="enable-the-advanced-wms-feature-for-inventory-visibility"></a>Virkjaðu Advanced WMS eiginleikann fyrir Birgðasýnileika

Til að virkja háþróaða WMS eiginleikann fyrir birgðasýnileika skaltu fylgja þessum skrefum.

1. Skráðu þig inn á Supply Chain Management sem stjórnandi.
1. Opnaðu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæði og virkjaðu eftirfarandi eiginleika í þessari röð:

    1. *Samþætting sýnileika birgða*
    1. *Virkja vörur vöruhúss í birgðasýnileika*

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**.
1. Á **Virkja WMS atriði** flipann, stilltu **Virkja WMS atriði** valmöguleika til *Já*.
1. Skráðu þig inn á Power Apps.
1. Opnaðu **Stillingar** síðu og síðan á **Eiginleikastjórnun** flipann, kveiktu á *AdvancedWHS* eiginleiki.
1. Í Supply Chain Management, farðu til **Vörustjórnun \> Reglubundin verkefni \> Samþætting birgðasýnileika**.
1. Á aðgerðarrúðunni velurðu **Slökkva** til að slökkva tímabundið á birgðasýnileika.
1. Á aðgerðarrúðunni velurðu **Virkja** til að virkja birgðasýnileika aftur. Viðbótin er endurhlaðin og nýi eiginleikinn er nú virkjaður. WMS-tengd gögn þín byrja að vera samstillt við Birgðasýnileika.

## <a name="query-on-hand-quantities-of-wms-items"></a>Spyrðu um magn af WMS hlutum sem eru til staðar

Til að spyrjast fyrir um WMS hluti, notarðu það sama [forritunarviðmót (API) og setningafræði skilaboða](inventory-visibility-api.md) sem þú notar fyrir hluti sem ekki eru WMS. Þú þarft ekki að tilgreina hvort hlutur sé WMS vara eða ekki WMS vara. Birgðasýnileiki greinir sjálfkrafa á hlutum, byggt á gögnunum sem eru geymd.

Niðurstöður úr fyrirspurnum um WMS atriði eru í meginatriðum þær sömu og niðurstöður fyrir vörur sem ekki eru WMS. Eini munurinn er sá að eftirfarandi líkamlegar ráðstafanir frá`fno` gagnagjafar eru reiknaðir út frá WMS rökfræði í Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Allar aðrar líkamlegar mælingar eru reiknaðar eins og þær eru þegar háþróaður WMS eiginleiki fyrir birgðasýnileika er óvirkur.

Fyrir nákvæmar upplýsingar um hvernig útreikningar á hendi fyrir WMS hluti virka, sjá [Pantanir í vöruhúsastjórnun](https://www.microsoft.com/download/details.aspx?id=43284) hvítur pappír.

Gagnaeiningarnar sem fluttar eru út til Dataverse getur ekki enn uppfært magn fyrir WMS vörur. Magnið sem er sýnt í gagnaeiningunum er rétt bæði fyrir vörur sem ekki eru WMS og fyrir magn sem eru ekki fyrir áhrifum af WMS rökfræði (þ.e. mælikvarða nema`AvailPhysical`,`AvailOrdered`,`ReservPhysical`, og`ReservOrdered` í`fno` gagnagjafa).

Breytingar á WMS vörumagni sem er geymt í gagnagjafanum Supply Chain Management eru bannaðar. Hvað varðar aðra eiginleika birgðasýnileika er þessari takmörkun framfylgt til að koma í veg fyrir árekstra.

## <a name="soft-reservations-on-wms-items-in-inventory-visibility"></a>Mjúkir fyrirvarar á WMS hlutum í Birgðasýnileika

Almennt, [mjúkir fyrirvarar](inventory-visibility-reservations.md) á WMS atriði eru studd. Þú getur tekið með WMS-tengdar líkamlegar mælingar í mjúkum fráteknum útreikningum. 

Í þekktri takmörkun er *hægt að panta* útreikningur er ekki studdur eins og er fyrir WMS hluti. Þess vegna, ef það er fyrirvari yfir núverandi víddum þar sem mjúkur fyrirvari á sér stað, *hægt að panta* útreikningur er rangur. Mjúkar bókanir verða ekki fyrir áhrifum þegar **ifCheckAvailForReserv** valkosturinn er óvirkur í [soft reservation API](inventory-visibility-api.md#create-one-reservation-event).

Þessi þvingun á einnig við um eiginleika og sérstillingar sem byggjast á mjúkum fyrirvörum (eins og úthlutun).

## <a name="calculate-available-to-promise-quantities"></a>Reiknaðu magn sem er tiltækt til að lofa

Lausnin styður að fullu [hægt að lofa (ATP)](inventory-visibility-available-to-promise.md) fyrir WMS hluti. Þú getur skilgreint ATP útreikninga án þess að hafa áhyggjur af WMS-sértækum upplýsingum.
