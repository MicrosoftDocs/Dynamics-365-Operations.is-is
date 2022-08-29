---
title: Skattar á pöntunum á netinu eru ekki rétt reiknaðir
description: Þessi grein veitir leiðbeiningar um úrræðaleit sem geta hjálpað þegar skattar á netpantanir eru rangt reiknaðir eða þegar skattflokkurinn á sölulínunni er ekki rétt stilltur.
author: Reza-Assadi
ms.date: 02/16/2022
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: a85b03cb6245c7c2e3622abc61a7887030927432
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285579"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a>Skattar á pöntunum á netinu eru ekki rétt reiknaðir

[!include [banner](../../includes/banner.md)]

Þessi grein veitir leiðbeiningar um úrræðaleit sem geta hjálpað þegar skattar á netpantanir eru rangt reiknaðir eða þegar skattflokkurinn á sölulínunni er ekki rétt stilltur.

## <a name="description"></a>lýsing

Þegar pöntun rafrænna viðskipta er gerð eru skattarnir rangt reiknaðir eða skattflokkur í sölulínunum er ekki rétt stilltur.

## <a name="resolution"></a>Upplausn

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a>Skilgreina almenna söluskattflokka í Commerce Headquarters

Til að skilgreina almenna söluskattflokka í Commerce Headquarters skal fylgja þessum skrefum.

1. Farið í **Skattur \> Óbeinir skattar \> Söluskattur \> Söluskattflokkur**.
1. Í vinstri yfirlitsrúðunni, veldu skattaflokkinn sem á að stilla.
1. Í flipanum **Skattur byggður á áfangastað smásölu** skal skilgreina skatta fyrir söluskattflokkinn.

> [!NOTE]
> Fyrir sendingu sem inniheldur ekki söluskatt sem ákvarðast af heimilisfangi viðskiptavinarins, ákvarða afhendingarheimilisfang línunnar og skattar sem eru byggðir á áfangastað sem eru stilltir fyrir skattflokkinn skattflokkinn. Frekari upplýsingar er að finna í [Setja upp skatta fyrir netverslanir á grundvelli áfangastaðar](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

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

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina söluskatt fyrir pantanir á netinu](../sales-tax-config.md)
