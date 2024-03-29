---
title: Brauðmylsnueining
description: Þessi grein fjallar um brauðmolaeiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fe5dfea7e579d54d11be35eb657a1c1f617a5724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277086"
---
# <a name="breadcrumb-module"></a>Brauðmylsnueining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um brauðmolaeiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Brauðmylsnueiningar eru notaðar til að bjóða upp á aukaleiðsögn á vefsíðum. Þær eru venjulega sýndar efst á síðunni, undir hausnum. Þrátt fyrir að hægt sé að bæta brauðmylsnueiningum við hvaða síðu sem er, eru þær oftast notaðar upplýsingasíðum afurða til að sýna tegundastigveldi afurðar og bjóða upp á styttri leið til að flakka um svæði. Einnig er hægt að nota brauðmylsnueininguna til að sýna tengilinn „Aftur í niðurstöður“ þegar notendur opna upplýsingasíðu afurðar af leitar- eða listasíðu. Á þennan hátt geta notendur á fljótlegan hátt farið aftur á síuðu listasíðuna til að halda áfram að versla.

Á síðum sem eru með samhengi afurðategunda, t.d. upplýsingasíður afurða og flokkasíður, sýna brauðmylsnueiningar tegundastigveldið. Á síðum sem eru ekki með flokkasamhengi, sýna brauðmylsnueiningar sjálfgefið **&lt;Rót svæðis&gt; / &lt;Núverandi síða&gt;**. Einnig er hægt að skilgreina brauðmylsnueiningar handvirkt á öðrum gerðum svæðissíðna til að sýna tengla á ákveðnar síður á svæðinu.

> [!NOTE]
> Brauðmylsnueiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.12.

Eftirfarandi mynd sýnir dæmi um brauðmylsnueiningu sem sýnir tegundastigveldi á upplýsingasíðu afurðar.

![Dæmi um brauðmylsnueiningu.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Stillingar brauðmylsnueiningar

Brauðmylsnueiningin er háð stillingunni **Birtingargerð brauðmylsnu á upplýsingasíðu afurðar** sem er skilgreind í **Stillingar svæðis \> Viðbætur** í svæðissmið. Þessi stilling er með þrjú möguleg gildi:

- **Sýna tegundastigveldi** – Þegar þetta gildi er valið sýnir brauðmylsnueiningin allt tegundastigveldi afurðarinnar sem er sýnt á upplýsingasíðu afurðar.
- **Sýna aftur í niðurstöður** - Þegar þetta gildi er valið mun brauðmylsnueiningin sýna „Aftur í niðurstöður“ tengil á upplýsingasíðu afurðar ef notandinn opnaði upplýsingasíðu afurðar úr einingunni sem leyfir tengil fyrir „Aftur í niðurstöður“. Þessi virkni er í boði þegar notendur fara úr flokka-, leitar-, lista- og tillögulistasíðum. Til að styðja þessa virkni eru einingar vörusafns og leitarniðurstaðna með eiginleika sem heitir **Leyfa aftur í niðurstöður á upplýsingasíðu afurðar**. Þessi eiginleiki gefur sveigjanleika til að skilgreina hvaða einingar eigi að styðja virknina fyrir tengil „Aftur í niðurstöður“ á upplýsingasíðu afurðar. Til dæmis þegar **Sýna aftur í niðurstöður** er valið fyrir stillinguna **Birtingargerð brauðmylsna á upplýsingasíðu afurðar** á brauðmylsnueiningunni og **Leyfa aftur í niðurstöður á upplýsingasíðu afurðar** er valið fyrir einingu leitarniðurstaðna leitarsíðu, er tengill fyrir „Aftur í niðurstöður“ sýndur þegar notendur fara frá leitarsíðunni til upplýsingasíðu afurðar.
- **Sýna tegundastigveldi og aftur í niðurstöður** – Þetta gildi er samsetning fyrri tveggja. Þegar þetta gildi er valið sýnir brauðmylsnueiningin bæði allt tegundastigveldið og tengilinn „Aftur í niðurstöður“ (ef hann er skilgreindur) á upplýsingasíðu afurðar.

> [!IMPORTANT]
> Þessar stillingar eru í boði í Dynamics 365 Commerce útgáfu 10.0.12. Ef verið er að uppfæra úr eldri útgáfu af Dynamics 365 Commerce verður að uppfæra appsettings.json-skrána handvirkt. Leiðbeiningar um uppfærslu appsettings.json skrárinnar er að finna í [Uppfærslur á SDK og einingasafni](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Eiginleikar brauðmylsnueiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Rót | Texti eða tengill| Þessi valfrjálsi eiginleiki sýnir texta tengils og viðtökustað tengils fyrir rót brauðmylsnusvæðis. Ef þessi eiginleiki er ekki stilltur verður engin rót skilgreind. |
| Brauðmylsnutengill | Tengill | Þessi valfrjálsi eiginleiki sýnir tengla fyrir handvirkt stillta brauðmylsnu ef þessir tenglar eru nauðsynlegir. Tenglar birtast í þeirri röð sem þeir eru sýndir. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Bæta brauðmylsnueiningu við nýja síðu

Til að bæta brauðmylsnueiningu við upplýsingasíðu afurðar og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.

1. Farið í **Stillingar svæðis \> Viðbætur** og síðan, fyrir stillinguna **Birtingargerð brauðmylsnu á upplýsingasíðu afurðar**, skal velja **Sýna tegundastigveldi**.
1. Opnið **Sniðmát** og veljið sniðmát upplýsingasíðu afurðar.
1. Í **Ílát** rauf sem inniheldur kaupboxseininguna, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Brauðmola** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farið á **Síður**, og Opnið PDP sem notar PDP-sniðmátið. Ef PDP er ekki til staðar skal stofna eitt.
1. Í **Ílát** rauf sem inniheldur kaupboxseininguna, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Brauðmola** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði hólfsins **Brauðmylsna**, undir **Rót**, skal velja **Texti tengils**.
1. Í svarglugganum **Texti tengils** skal slá inn **Heim** og síðan, undir **Viðtökustaður tengils**, skal velja **Bæta við tengli**.
1. Í svarglugganum **Bæta við tengli** skal velja tengil fyrir brauðmylsnurótina og síðan velja **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining yfirlitsvalmyndar](nav-menu-module.md)

[Vefsíðuvalseining](site-selector.md)

[Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu](category-search-page-overview.md)

[Afurðasafnseiningar](product-collection-module-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Uppfærslur á SDK og kjarnasafni](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
