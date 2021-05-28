---
title: Skattar á pöntunum á netinu eru ekki rétt reiknaðir
description: Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur hjálpað til þegar skattar á pöntunum á netinu eru ekki rétt reiknaðir eða þegar skattflokkur sölulínu er ekki rétt stilltur.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021104"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Skattar á pöntunum á netinu eru ekki rétt reiknaðir

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði býður upp á leiðsögn úrræðaleitar sem getur hjálpað til þegar skattar á pöntunum á netinu eru ekki rétt reiknaðir eða þegar skattflokkur sölulínu er ekki rétt stilltur.

## <a name="description"></a>lýsing

Þegar pöntun rafrænna viðskipta er gerð eru skattarnir rangt reiknaðir eða skattflokkur í sölulínunum er ekki rétt stilltur.

## <a name="resolution"></a>Upplausn

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a>Skilgreina söluskatt fyrir smásöluverslun í Commerce Headquarters

Til að skilgreina söluskatt fyrir smásöluverslun í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Smásala og viðskipti \> Rásir \> Allar verslanir**.
1. Veljið verslunina þar sem á að skilgreina söluskattinn.
1. Í flipanum **Almennt**, í hlutanum **Söluskattur**, skal skilgreina upplýsingar söluskatts fyrir verslunina.

> [!NOTE]
> Fyrir afurð sem sótt er í verslun er notaður skattflokkur verslunarinnar sem er valin til að vera sótt úr. Frekari upplýsingar er að finna í [Stilla aðra skattvalkosti fyrir verslanir](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a>Skilgreina söluskatt fyrir aðsetur viðskiptavinar í Commerce Headquarters

Til að skilgreina söluskatt fyrir aðsetur viðskiptavinar í Commerce Headquarters skal fylgja þessum skrefum.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veljið viðskiptavin þar sem á að skilgreina söluskatt.
1. Í flýtiflipanum **Aðsetur** skal velja aðsetrið sem skilgreina á söluskatta fyrir, velja **Fleiri valkostir** og síðan velja **Ítarlegt**.
1. Í flýtiflipanum **Almennt** skal velja **Skattflokkinn**.
1. Í reitnum **Söluskattur** skal velja viðeigandi gildi.

> [!NOTE]
> Fyrir sendingar sem fela í sér söluskatt á aðsetri viðskiptavinar mun afhendingaraðsetur línunnar ákvarða skattflokk fyrir línuna. Ef viðskiptavinur er að senda til fyrirliggjandi aðseturs sem er með skattflokk sem búið er að skilgreina verður fyrirliggjandi skattflokkur notaður. Sjálfgefið er að aðsetur eru ekki með skattflokk þegar þau eru búin til.

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Skilgreina almenna söluskattflokka í Commerce Headquarters

Til að skilgreina almenna söluskattflokka í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Skattur \> Óbeinir skattar \> Söluskattur \> Söluskattflokkur**.
1. Í vinstri flettingunni skal velja skattflokkinn sem á að skilgreina.
1. Í flipanum **Skattur byggður á áfangastað smásölu** skal skilgreina skatta fyrir söluskattflokkinn.

> [!NOTE]
> Fyrir sendingu sem felur ekki í sér söluskatt á aðsetri viðskiptavinar munu afhendingaraðsetur línunnar og skattur byggður á áfangastað sem er skilgreint fyrir skattflokkinn ákvarða skattflokkinn. Frekari upplýsingar er að finna í [Setja upp skatta fyrir netverslanir á grundvelli áfangastaðar](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina söluskatt fyrir pantanir á netinu](../sales-tax-config.md)