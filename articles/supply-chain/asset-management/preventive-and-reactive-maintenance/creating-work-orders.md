---
title: Verkbeiðnir stofnaðar
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir í eignastýringu.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836735"
---
# <a name="creating-work-orders"></a>Verkbeiðnir stofnaðar

[!include [banner](../../includes/banner.md)]

Þegar fyrirbyggjandi viðhaldsverk hafa verið tímasett er næsta skref að stofna verkbeiðnir fyrir þau. Hægt er að ljúka þessu skrefi með því að nota eina af viðhaldsáætlunum. Áætlaðar vinnslur í viðhaldsáætlun geta haft mismunandi tilvísunargerðir eins og lýst er í eftirfarandi töflu.

| Gerð tilvísunar | lýsing |
|---|---|
| Viðhaldsáætlanir | Fyrirbyggjandi viðhaldsverk sem byggja á viðhaldsáætlunargerðinni *Tími* eða *Teljari*. |
| Viðhaldslotur | Fyrirbyggjand viðhaldsverk sem innihalda nokkrar eignir sem þurfa sams konar viðhald. |
| Viðhaldsbeiðni | Handvirk stofnun beiðni um viðhald eða viðgerð á eign. Hægt er að umreikna þessa beiðni í verkbeiðni. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Stofna verkbeiðnir út frá viðhaldsáætluninni

Til að stofna verkbeiðnir sem byggja á viðhaldsáætluninni skal fylgja þessum skrefum.

1. Opnið eina af eftirfarandi síðum, allt eftir því hvernig velja á áætlunarvörur fyrir verkbeiðnir:

    - Öll viðhaldsáætlun (**Eignastýring \> Áætlun stjórnunar \> Öll viðhaldsáætlun**)
    - Opna viðhaldsáætlunarlínur (**Eignastýring \> Áætlun stjórnunar \> Opna áætlunarlínur viðhalds**)
    - Opna viðhaldsáætlunarhópa (**Eignastýring \> Áætlun stjórnunar \> Opna áætlunarhópa viðhalds**)

1. Í hnitanetinu skal velja gátreitinn fyrir hvert verk viðhaldsáætlunar sem á að stofna verkbeiðni fyrir. Á aðgerðasvæðinu skal síðan velja **Verkbeiðni**.

    Gátreiturinn **Stofna verkbeiðnir** birtist. Reiturinn **Vinnustundir viðhaldsspár** sýnir heildarfjölda vinnustunda fyrir spá fyrir valdar línur.

    ![Búa til svarglugga verkbeiðna](media/18-preventive-maintenance.png)

1. Í hlutanum **Færibreytur** skal tilgreina þann fjölda verkbeiðna sem á að stofna. Veldu einn af eftirfarandi valkostum:

    - **Ein verkbeiðni á línu** – Stofnið eina verkbeiðni á hverja viðhaldsáætlunarlínu.
    - **Ein verkbeiðni á** – Stofnið verkbeiðnir sem eru flokkaðar samkvæmt stillingum hinna valkostanna sem verða tiltækir þegar þessi valkostur er valinn.

1. Í reitnum **Gerð verkbeiðni** skal velja verkbeiðnigerðina sem á að nota fyrir allar verkbeiðnir sem eru stofnaðar.
1. Veljið **Í lagi** til að stofna verkbeiðnir samkvæmt stillingunum.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Flokka verkbeiðnilínur sem eru sjálfkrafa stofnaðar meðan á viðhaldsáætlun stendur

Þessi eiginleiki gerir kleift að skilgreina reglur fyrir flokkun verkbeiðnilína undir einni verkbeiðni þegar kerfið er stillt á að búa sjálfkrafa til verkbeiðnir sem byggja á viðhaldsáætlun. Áður gátu sjálfkrafa myndaðar verkbeiðnir aðeins innihaldið eina línu. Nú er hins vegar hægt að flokka verkbeiðnir eftir til dæmis eign, eignagerð eða virkri staðsetningu. (Handvirkt myndaðar verkbeiðnir var aðeins hægt að flokka á þennan hátt eins og lýst er í hlutanum hér á undan í þessu efnisatriði.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Virkja flokkun fyrir sjálfkrafa myndaðar verkbeiðnir

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Eignastjórnun*
- **Heiti eiginleika:** *Notið reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Setja upp flokkun fyrir sjálfkrafa myndaðar verkbeiðnir

Til að setja upp flokkun fyrir sjálfkrafa myndaðar verkbeiðnir skal fylgja þessum skrefum.

1. Farið í **Eignastýring \> Uppsetning \> Fyrirbyggjandi viðhald \> Viðhaldsáætlanir**.
1. Fyrir hverja áætlun þar sem á að mynda flokkaðar verkbeiðnir skal fylgja þessum skrefum:

    1. Velja skal áætlunina á listasvæðinu.
    1. Í flýtiflipanum **Línur** skal ganga úr skugga um að gátreiturinn **Stofna sjálfvirkt** sé valinn í hverri línu.

1. Farið í **Eignastýring \> Reglubundið \> Fyrirbyggjandi viðhald \> Tímasetja viðhaldsáætlanir**.
1. Í svarglugganum **Tímasetja viðhaldsáætlanir**, í hlutanum **Tímabil**, skal tilgreina hámarkstíma fyrir áætlunina (hversu langt fram í tímann er horft þegar fundin eru verk viðhaldsáætlunar til að mynda vinnu fyrir).
1. Stillið valkostinn **Stofna verkbeiðni sjálfkrafa úr áætlun** á *Já*.
1. Veldu einn af eftirfarandi valkostum í hlutanum **Verkbeiðni**:

    - **Ein verkbeiðni á línu** – Stofnið eina verkbeiðni á hverja viðhaldsáætlunarlínu. (Þessi valkostur veitir sömu virkni og er tiltæk þegar slökkt er á eiginleikanum *Nota reglur fyrir flokkun verkbeiðna á meðan viðhaldsáætlun er keyrð*.)
    - **Ein verkbeiðni á** – Stofnið verkbeiðnir sem eru flokkaðar samkvæmt stillingum hinna valkostanna sem verða tiltækir þegar þessi valkostur er valinn.

1. Ef ætlunin er að valkostirnir séu notaðir þegar aðeins sumar viðhaldsáætlanir eru keyrðar skal í flýtiflipanum **Færslur til að taka með** sía eftir þörfum, rétt eins og yrði gert fyrir aðrar runuvinnslur í Microsoft Dynamics 365 Supply Chain Management.
1. Í flýtiflipanum **Keyra í bakgrunni** skal setja upp runu og áætlunarvalkosti eftir þörfum, rétt eins og yrði gert fyrir aðrar runuvinnslur í Supply Chain Management.
1. Veljið **Í lagi** til að keyra og/eða tímasetja valdar viðhaldsáætlanir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]