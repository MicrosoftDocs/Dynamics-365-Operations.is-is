---
title: Eining lands-/svæðisvals
description: Þessi grein fjallar um land/svæðisvalseininguna og lýsir því hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 04/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 203a8e17e075f15b7ae3cceb98d24ced75539a01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270292"
---
# <a name="countryregion-picker-module"></a>Eining lands-/svæðisvals

[!include [banner](includes/banner.md)]

Þessi grein fjallar um land/svæðisvalseininguna og lýsir því hvernig á að stilla hana í Microsoft Dynamics 365 Commerce.

Land-/svæðisvalseiningin notar [landfræðileg uppgötvun og tilvísun](geo-detection-redirection.md) lögun í Dynamics 365 Commerce til að sýna viðskiptavinum sem mæla með vefsvæðum sem biðja um vefslóð rafrænna viðskiptasíðu sem er ekki tengd landi þeirra eða svæði.

Til dæmis biður viðskiptavinur í Kanada um vefslóð sem tengist öðru landi en Kanada. Í þessu tilviki sýnir eining lands-/svæðisvals svarglugga sem ráðleggur vefslóðir vefsvæða sem tengjast Kanada. 

## <a name="how-it-works"></a>Hvernig það virkar

Þegar landfræðileg uppgötvun og tilvísun eru virkjuð fyrir vefsvæði og viðskiptavinur biður um vefslóð vefsvæðis, er landið sem er greint fyrir viðskiptavininn og vefslóðin sem hann bað um notuð til að ákvarða hvort þessi vefslóð sé varpað á landið þar sem viðskiptavinurinn er. Kortlagningin milli vefslóða og landa er skilgreind á **Rásir** síðu undir **Vefstillingar** í viðskiptasíðugerð. 

Ef vefslóð beiðninnar passar ekki við neina vefslóð sem er kortlögð við land viðskiptavinarins, er listi yfir eina eða fleiri vefslóðir sem eru kortlagðar á það land skilað í svarinu. Landa-/svæðisvalinn ber saman hverja vefslóð á þeim lista við vefslóðirnar sem hafa verið stilltar í land-/svæðiseiningunni. Fyrir hverja nákvæma samsvörun sem finnst, sýnir lands-/svæðisvalið skjáfyrirsögnina, undirfyrirsögnina og myndina fyrir þá vefslóð og tengir þá þætti með því að nota vefslóðina.

Þegar viðskiptavinur velur valmöguleika í landa-/svæðisvalinu er hann færður á vefslóðina sem tengist tengilinn. Þessi vefslóð er skrifuð á **\_ msdyn365\_\_\_ síða\_** vafraköku þannig að hægt sé að nota hana sem síðuval viðskiptavinarins. Næst þegar viðskiptavinurinn biður um vefslóðina sem ekki er tengd við landið hans eða svæði, er honum sjálfkrafa vísað til viðkomandi lands. Þess vegna mælum við með að þú notir líka [síðuvalseining](site-selector.md) á e-verslunarsíðunni þinni, svo að viðskiptavinir hafi leið til að hnekkja eða uppfæra síðuval sitt. 

Ef viðskiptavinur lokar lands-/svæðavalglugganum er engin fótspor skrifuð og viðskiptavinurinn verður áfram á núverandi síðu. 

Eftirfarandi mynd sýnir dæmi um svarglugga lands-/svæðisvals.

![Dæmi um svarglugga lands-/svæðisvals á heimasíðu.](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>Eiginleikar einingar lands-/svæðisvals

| Nafn eiginleika              | Virði       | lýsing                                                  |
| -------------------------- | ----------- | ------------------------------------------------------------ |
| Haus                    | Texti        | Fyrirsögnin sem birtist efst í svarglugganum.       |
| Undirfyrirsögn                 | Texti        | Undirfyrirsögnin sem birtist fyrir neðan fyrirsögnina.               |
| Land: birtingarstrengur    | Texti        | Birtingarheiti fyrir valkost vefslóðar (til dæmis „Kanada“).   |
| Land: undirstrengur birtingar | Texti        | Valkvæmur undirstrengur sem birtist fyrir valkost vefslóðar (til dæmis „enska“ eða „franska“). |
| Land: Landsmynd     | Eign geymslumiðils | Valfrjáls mynd sem tengist valkosti vefslóðar (til dæmis mynd af kanadíska fánanum). |
| Land: vefslóð lands       | Texti        | Vefslóðin fyrir landið/svæðið sem verið er að stilla. Þessi vefslóð verður að passa nákvæmlega við vefslóðina sem þú tilgreindir fyrir þetta land/svæði á **Rásir** síðu undir **Vefstillingar** í viðskiptasíðugerð. Að auki verður lén vefslóðarinnar að vera sérsniðna lénið sem er tilgreint í **Passaðu lén** sviði á **Rásir** síðu, ekki vinnuvistfang síðunnar sem Commerce gefur upp þegar þú býrð til rafrænt viðskiptaumhverfi (td slóð`https://<yourcompany>.commerce.dynamics.com/`). |
| Aðgerðartengill                | Aðgerðartengill | Valfrjáls tengill sem birtist neðst í svarglugganum. Þessi tengill getur til dæmis bent á innri síðu þar sem er að finna lista yfir öll lönd og svæði sem vefsvæðið styður. |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>Bæta einingu lands-/svæðisvals við síðu

Hægt er að bæta einingu lands-/svæðisvals við hausaeininguna annaðhvort beint eða í gegnum samnýtt síðubrot. Frekari upplýsingar um hausaeiningar er að finna í [Hausaeining](author-header-module.md).

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Stilla einingu lands-/svæðisvals í vefsmið Commerce

> [!NOTE]
> Vefslóðir sem þú mælir með fyrir viðskiptavini þína verða að vera stilltar sem hlutar lands í einingu lands-/svæðisvals.

Fyrir hverja vefslóð sem þú vilt sýna og mæla með fyrir viðskiptavini skaltu fylgja þessum skrefum í Commerce site builder.

1. Veldu hólfaeiningu lands-/svæðisvals.
1. Á eiginleikasvæðinu undir **Landalisti** skal velja **Bæta við landi**.
1. Velja nýja **Land** reitinn.
1. Í reitinn **Birta streng** skal færa inn birtingarnafn (til dæmis **Kanada**).
1. Valfrjálst: Í reitinn **Birta undirstreng** skal færa inn undirstreng (til dæmis **franskur** eða **fr-ca**).
1. Valfrjálst: Veldu mynd úr miðlasafninu.
1. Í reitinn **Vefslóð lands** er slegin inn slóðin. Þessi vefslóð verður að passa nákvæmlega við vefslóðina sem birtist á **Rásir** síðu og sem er kortlagt við rásina, þar á meðal svæði sem tengist landinu eða svæðinu. 
1. Veldu **Í lagi**.
1. Endurtaktu skrefin fyrir allar vefslóðir annarra landa sem þú vilt að eining lands-/svæðisvals sýni.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp landfræðilega greiningu og áframsendingu](geo-detection-redirection.md)

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining síðuhauss](author-header-module.md)

[Vefsíðuvalseining](site-selector.md)

[Brauðmylsnueining](add-breadcrumb.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
