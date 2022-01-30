---
title: Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar
description: Þetta efnisatriði lýsir stofnun hlutastraumspöntunar fyrir færslur verslunar í Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 67b66cd4bf2a77f3ab7f33f691156e38cc13770a
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964630"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Stofnun hlutastraumspöntunar fyrir færslur smásöluverslunar

[!include [banner](includes/banner.md)]

Í Microsoft Dynamics 365 Commerce útgáfu 10.0.5 og síðar er ráðlagt að flytja öll bókunarferli uppgjöra yfir í bókunarferli uppgjöra með hlutastraum. Verulegur ávinningur fyrir afkomu og viðskipti fylgir því að nota hlutastraumsvirknina. Unnið er úr sölufærslum yfir daginn. Unnið er úr greiðslumáta- og reiðufjárstjórnunarfærslum á fjárhagsskýrslunni í lok dags. Hlutastraumsvirkni býður upp á stöðuga úrvinnslu sölupantana, reikninga og greiðslna. Af þeim sökum eru birgðir, tekjur og greiðslur uppfærðar nánast í rauntíma.

## <a name="use-trickle-feed-based-posting"></a>Nota bókun með hlutastraum

> [!IMPORTANT]
> Áður en bókun með hlutastraum er virkjuð verður að tryggja að ekki séu til staðar reiknuð og óbókuð uppgjör. Bóka skal öll uppgjör áður en eiginleikinn er virkjaður. Hægt er að leita að opnum uppgjörum á vinnusvæðinu **Fjármál verslunar**.

Til að virkja bókun smásölufærslna með hlutastraum skal virkja eiginleikann **Smásöluuppgjör – hlutastraumur** á vinnusvæðinu **Eiginleikastjórnun**. Uppgjörum verður skipt upp í tvær gerðir: færsluuppgjör og fjárhagsskýrslur.

### <a name="transactional-statements"></a>Færsluuppgjör

Vinnsla færsluuppgjöra á að vera keyrð mjög reglulega í gegnum daginn svo fylgiskjöl séu búin til þegar færslum er hlaðið upp í Commerce Headquarters. Færslum er hlaðið úr verslununum í Commerce Headquarters þegar **P-vinnslan** er keyrð. Einnig þarf að keyra vinnsluna **Villuleita í færslum verslunar** til að villuleita færslur svo að færsluuppgjörið telji þær með.

Tímasetja eftirfarandi vinnslur á að keyra mjög reglulega:

- Til að reikna út færsluuppgjör skal keyra vinnsluna **Reikna færsluuppgjör í runu** (**Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Sölustaðarbókun \> Reikna færsluuppgjör í runu**). Þessi vinnsla mun sækja allar óbókaðar og villuleitaðar færslur og bæta þeim við nýtt færsluuppgjör.
- Til að bóka færsluuppgjör í runu skal keyra vinnsluna **Bóka færsluuppgjör í runu** (**Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Sölustaðarbókun \> Bóka færsluuppgjör í runu**). Þessi vinnsla mun keyra bókunarferlið og búa til sölupantanir, sölureikninga, greiðslubækur, afsláttarbækur og tekju-/kostnaðarfærslur fyrir óbókuð uppgjör sem innihalda engar villur. 

### <a name="financial-statements"></a>Fjárhagsskýrslur

Vinnsla fjárhagsskýrslna á að fara fram í lok dags. Þessi gerð uppgjörsferlis styður aðeins lokunaraðgerðina **Vakt** og mun aðeins telja með lokaðar vaktir. Skýrslur takmarkast við fjárhagslega afstemmingu. Þær munu eingöngu búa til færslubækur fyrir upphæðamismun á milli talinnar upphæðar og færsluupphæðar fyrir greiðslumáta ásamt færslubókum fyrir aðrar reiðufjárstjórnunarfærslur.

Fjárhagsskýrslur gera notanda líka kleift að fara yfir eftirtaldar færslur: talningu skiptimyntar, greiðslufærslur, greiðslufærslur á vörslureikningi og greiðslufærslur í öryggisskáp. Upplýsingasíðan um greiðslumáta er aðeins sýnileg þegar fjárhagsskýrsla er valin.

![Mynd sem sýnir hlutann með upplýsingum um greiðslumáta á bókuðum yfirlitum aðeins þegar fjárhagsskýrsla er valin.](./media/Trickle-feed-posted-statements-transaction-view.png)

Tímasetja upphafs- og lokatíma eftirfarandi vinnsla við fjárhagsskýrslugerð miðað við áætluð dagslok:

- Til að reikna út fjárhagsskýrslu skal keyra vinnsluna **Reikna fjárhagsskýrslur í runu** (**Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Sölustaðarbókun \> Reikna fjárhagsskýrslur í runu**). Þessi vinnsla mun safna saman öllum óbókuðum fjárhagsfærslum og bæta þeim við nýja fjárhagsskýrslu.
- Til að bóka fjárhagsskýrslur í runu skal keyra vinnsluna **Bóka fjárhagsskýrslur í runu** (**Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Sölustaðarbókun \> Bóka fjárhagsskýrslur í runu**).

### <a name="manually-create-statements"></a>Stofna skýrslur handvirkt

Einnig er hægt að búa til gerðir af færsluuppgjörum og fjárhagsskýrslum handvirkt. 

1. Opnið **Retail og Commerce \> Rásir \> Verslanir** og veljið **Uppgjör**. 
2. Veljið **Nýtt** og síðan þá gerð uppgjörs sem stofna á. Svæðin á síðunni **Uppgjör** munu sýna gögn sem eiga við valda gerð uppgjörs og aðgerðir í **Uppgjörsflokkur** munu birta viðeigandi aðgerðir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
