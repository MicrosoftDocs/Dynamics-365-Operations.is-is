---
title: Nota greiðsluspár viðskiptavinar
description: Þessi grein fer með þig í gegnum áskildar forsendur og áskilin skref til að nota prufuútgáfu Finance Insights.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 330642624b55a6772ef149b70873021401a6bd83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901403"
---
# <a name="use-customer-payment-predictions"></a>Nota greiðsluspár viðskiptavinar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að nota greiðsluspár viðskiptavinar. Gakktu úr skugga um að ljúka við uppsetningarskrefin áður en þú notar þennan eiginleika. Nánari upplýsingar eru í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md).

Þú getur skoðað greiðsluspár viðskiptavinar á vinnusvæðinu **Stjórna skuldum og innheimtu viðskiptavinar** og á tveimur nýjum listasíðum **Greiðsluspár færslu** og **Greiðsluspár viðskiptavinar**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Stjórna vinnusvæði skulda og innheimtu viðskiptavinar

Vinnusvæðið **Stjórna skuldum og innheimtu viðskiptavinar** inniheldur tvo nýja reiti, **Greiðsluspár færslu** og **Greiðsluspár viðskiptavinar**.

### <a name="transaction-payment-predictions-list-page"></a>Listasíða greiðsluspár færslu

Á listasíðunni **Greiðsluspár færslu** getur þú skoðað líkurnar á greiðslu fyrir opnar færslur í römmunum **Á réttum tíma**, **Seint**, og **Mjög seint**. Fyrir hverja færslu á hnitanetinu sýnir dálkurinn **Líkur á réttum tíma** líkurnar á því að reikningurinn verði greiddur á eða fyrir gjalddaga. Þegar líkurnar á greiðslu á réttum tíma eru minni en 50 prósent birtist rauður hringur við hliðina á prósentuhlutfallinu í dálkinum **Líkur á réttum tíma** til að tilgreina hættuna á greiðsludrætti.

[![Síða greiðsluspár fyrir hverja færslu.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Í glugganum **Tengdar upplýsingar** hægra megin á síðunni birtast frekari upplýsingar um spárnar:

- Fyrir færsluna sem er valin á hnitanetinu sýnir flýtiflipinn **Greiðsluspá** frekari upplýsingar um greiðsluspár í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**. Hlutinn **Helstu þættir** sýnir helstu þættina sem hafa áhrif á spárnar. Helstu þættir eru eiginleikar valinnar færslu og/eða viðskiptavinurinn fyrir umrædda færslu.
- Flýtiflipinn **Innsýn í viðskiptavini** sýnir núverandi reikning, greiðslu og tölfræði innheimtu fyrir valda færslu.
- Flýtiflipinn **Ferill viðskiptavinar** sýnir greiðsluferil viðskiptavinarins í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.

Gögnin í hlutanum **Helstu þættir** og á flýtiflipunum **Innsýn í viðskiptavini** og **Ferill viðskiptavinar** hjálpa til við að útskýra greiðsluspárnar. Slíkt getur aukið traust þitt á áreiðanleika slíkra spáa.

[![Myndrænir vísar fyrir greiðsluspár í glugganum tengdar upplýsingar.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="customer-payment-predictions-list-page"></a>Listasíða greiðsluspár viðskiptavinar

Listasíðan **Greiðsluspár viðskiptavinar** sýnir opnunarstöðu samtals og upphæðina sem spáð er að greidd verði í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.

[![Síða greiðsluspár fyrir hvern viðskiptavin.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Greiðsluupphæðin í hverjum ramma er reiknuð út sem summa af vegnu meðaltali færsluupphæðarinnar. Þessi upphæð er reiknuð út miðað við greiðslulíkur fyrir hvern ramma fyrir sig.

Viðskiptavinur er t.d. með þrjár opnar færslur sem hafa eftirfarandi greiðslulíkur í hverjum ramma fyrir sig.

| Færsla | Upphæð | Líkur á greiðslu á réttum tíma | Líkur á greiðslu seint | Líkur að greiðslu mjög seint |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 prósent                  | 50 prósent               | 40 prósent                    |
| T2          | 1.000  | 50 prósent                  | 30 prósent               | 20 prósent                    |
| T3          | 10,000 | 1 prósent                   | 4 prósent                | 95 prósent                    |

Í slíku tilviki eru greiðslur áætlaðar fyrir hvern ramma á eftirfarandi hátt.

| Rammar   | Færsla T1      | Færsla T2         | Færsla T3            | Alls |
|-----------|---------------------|------------------------|---------------------------|-------|
| Á réttum tíma   | 100 × 10 ÷ 100 = 10 | 1.000 × 50 ÷ 100 = 500 | 10.000 × 1 ÷ 100 = 100    | 610   |
| Á eftir áætlun      | 100 × 50 ÷ 100 = 50 | 1.000 × 30 ÷ 100 = 300 | 10.000 × 4 ÷ 100 = 400    | 750   |
| Mjög seint | 100 × 40 ÷ 100 = 40 | 1.000 × 20 ÷ 100 = 200 | 10.000 × 95 ÷ 100 = 9.500 | 9,740 |

Í hlutanum **Tengdar upplýsingar** hægra megin á síðunni birtast frekari upplýsingar um spárnar:

- Fyrir færsluna sem er valin á hnitanetinu sýnir flýtiflipinn **Greiðsluspár** frekari upplýsingar um greiðsluspár í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.
- Flýtiflipinn **Innsýn í viðskiptavini** sýnir núverandi reikning, greiðslu og tölfræði innheimtu fyrir valda færslu.
- Flýtiflipinn **Ferill viðskiptavinar** sýnir greiðsluferil viðskiptavinarins í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.

Gögnin í hlutanum **Innsýn í viðskiptavini** og á flýtiflipunum **Ferill viðskiptavinar** hjálpa til við að útskýra greiðsluspárnar. Slíkt getur aukið traust þitt á áreiðanleika slíkra spáa.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Auka nákvæmni greiðsluspáa

Þú getur skoðað nákvæmni greiðsluspáa með því að opna **Skuldir og innheimta \> Uppsetning \> Fjármálainnsýn \> Færibreytur fjármálainnsýnar**. Á flipanum **Innsýn í greiðslu viðskiptavinar** sýnir hlutinn **Spálíkan** nákvæmni spálíkansins sem prósentuhlutfall.

Ef nákvæmnin telst ekki vera fullnægjandi skaltu velja tengilinn **Auka nákvæmni líkans** til að opna upplifun AI Builder-viðbótarinnar. Í upplifun AI Builder-viðbótarinnar getur þú valið að hætta við val á svæðum þar til þú hefur valið reitina sem þú telur vera mikilvægasta til að spá fyrir um greiðslulíkur á nákvæman hátt. Þegar því er lokið getur þú auðveldlega endurþjálfað spálíkanið og birt breytingarnar þínar. Nýþjálfaða spálíkanið verður sjálfkrafa valið fyrir spár í Dynamics 365 Finance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
