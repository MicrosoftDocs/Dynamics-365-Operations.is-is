---
title: Stuðningur fyrir Inventory Visibility af vörum í vöruhúsakerfi
description: Þessi grein lýsir stuðningi við Birgðasýnileika fyrir vörur sem eru virkjaðar fyrir vöruhúsastjórnunarferli (WMS vörur).
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762740"
---
# <a name="inventory-visibility-support-for-wms-items"></a>Stuðningur fyrir Inventory Visibility af vörum í vöruhúsakerfi

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

Við mælum með að þú notir WMS eiginleikann fyrir Birgðasýnileika í aðstæðum þar sem öll eftirfarandi skilyrði eru uppfyllt:

- Þú ert að samstilla Supply Chain Management gögn við Birgðasýnileika.
- Þú ert að nota WMS í Supply Chain Management.
- Notendur panta fyrir WMS vörur á stigum undir vöruhúsastigi (til dæmis á númeraplötustigi vegna þess að þú ert að vinna úr vöruhúsavinnu).

Í öðrum tilfellum verða niðurstöður fyrirspurna við höndina þær sömu, óháð því hvort Advanced WMS eiginleiki fyrir Birgðasýnileika er virkur. Að auki verður afköst betri ef þú kveikir ekki á eiginleikanum í þessum aðstæðum, vegna þess að það eru færri útreikningar og minni kostnaður.

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>Virkjaðu WMS eiginleikann fyrir Birgðasýnileika

Til að virkja WMS eiginleikann fyrir Birgðasýnileika skaltu fylgja þessum skrefum.

1. Skráðu þig inn á Supply Chain Management sem stjórnandi.
1. Opnaðu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnusvæði og virkjaðu eftirfarandi eiginleika í þessari röð:

    1. *Samþætting sýnileika birgða*
    1. *Virkja vörur vöruhúss í birgðasýnileika*

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**.
1. Á **Virkja WMS atriði** flipann, stilltu **Virkja WMS atriði** valmöguleika til *Já*.
1. Skráðu þig inn í Power Apps umhverfið og opnaðu **Birgðasýnileika**.
1. Opnaðu **Stillingar** síðu og síðan á **Eiginleikastjórnun** flipann, kveiktu á *AdvancedWHS* eiginleiki.
1. Í Supply Chain Management, farðu til **Vörustjórnun \> Reglubundin verkefni \> Samþætting birgðasýnileika**.
1. Á aðgerðarrúðunni velurðu **Slökkva** til að slökkva tímabundið á birgðasýnileika.
1. Á aðgerðarrúðunni velurðu **Virkja** til að virkja birgðasýnileika aftur. Viðbótin er endurhlaðin og nýi eiginleikinn er nú virkjaður. WMS-tengd gögn þín byrja að vera samstillt við Birgðasýnileika.

## <a name="query-on-hand-quantities-of-wms-items"></a>Spyrðu um magn af WMS hlutum sem eru í boði

Til að spyrjast fyrir um WMS hluti, notarðu það sama [forritunarviðmót (API) og setningafræði skilaboða](inventory-visibility-api.md) sem þú notar fyrir hluti sem ekki eru WMS. Þú þarft ekki að tilgreina hvort hlutur sé WMS vara eða ekki WMS vara. Birgðasýnileiki greinir sjálfkrafa á hlutum, byggt á gögnunum sem eru geymd.

Niðurstöður úr fyrirspurnum um WMS atriði eru í meginatriðum þær sömu og niðurstöður fyrir vörur sem ekki eru WMS. Eini munurinn er sá að eftirfarandi líkamlegar ráðstafanir frá`fno` gagnagjafar eru reiknaðir út frá WMS rökfræði í Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

Allar aðrar líkamlegar mælingar eru reiknaðar alveg eins og þær eru þegar WMS eiginleiki fyrir Birgðasýnileika er óvirkur.

Fyrir nákvæmar upplýsingar um hvernig útreikningar á hendi fyrir WMS hluti virka, sjá [Pantanir í vöruhúsastjórnun](https://www.microsoft.com/download/details.aspx?id=43284) hvítur pappír.

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>Á hendi listayfirlit og gagnaeining fyrir WMS hluti

The **Forhlaða samantekt birgðasýnileika** síða veitir útsýni fyrir *Forhlaða niðurstöður fyrir vísitölufyrirspurn* aðila. Ólíkt *Birgðayfirlit* eining, the *Forhlaða niðurstöður fyrir vísitölufyrirspurn* eining veitir birgðalista fyrir vörur ásamt völdum víddum. Birgðasýnileiki samstillir forhlaðna samantektargögnin á 15 mínútna fresti.

Ef þú notar birgðasýnileika með WMS hlutum og vilt skoða birgðalistann fyrir WMS hluti, mælum við með að þú virkja *Forhlaða samantekt birgðasýnileika* eiginleiki (sjá einnig [Forhlaða straumlínulagaða fyrirspurn](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)). Samsvarandi gagnaeining í Dataverse geymir niðurstöður fyrirspurnar fyrir forhleðslu þína, sem er uppfærð á 15 mínútna fresti. Nafn gagnaeiningarinnar er `Onhand Index Query Preload Result`.

> [!IMPORTANT]
> The Dataverse eining er skrifvarinn. Þú getur skoðað og flutt gögnin út í Birgðasýnileika einingunum, en **ekki breyta því**.

Breytingar á WMS vörumagni sem er geymt í Supply Chain Management gagnagjafa (`fno`) eru bönnuð. Þessi hegðun passar við hegðun annarra eiginleika birgðasýnileika. Þessari takmörkun er framfylgt til að koma í veg fyrir árekstra.

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS vörusamhæfi fyrir aðrar aðgerðir í Birgðasýnileika

[Mjúkir fyrirvarar](inventory-visibility-reservations.md) og [birgðaúthlutun](inventory-visibility-allocation.md) af WMS hlutum eru studdir. Þú getur tekið með WMS-tengdar líkamlegar mælingar í mjúkum fráteknum og úthlutunarútreikningum.

## <a name="calculate-available-to-promise-quantities"></a>Reiknaðu magn sem er tiltækt til að lofa

Lausnin styður að fullu [hægt að lofa (ATP)](inventory-visibility-available-to-promise.md) fyrir WMS hluti. Þú getur skilgreint ATP útreikninga án þess að hafa áhyggjur af WMS-sértækum upplýsingum.
