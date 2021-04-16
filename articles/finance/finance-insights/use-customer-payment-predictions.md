---
title: Nota greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði fer með þig í gegnum áskildar forsendur og áskilin skref til að nota prufuútgáfu Fjármálainnsýnar.
author: ShivamPandey-msft
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 51cd69563a7a5b30e932f1aad828d095cc55b075
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827219"
---
# <a name="use-customer-payment-predictions-preview"></a>Nota greiðsluspár viðskiptavinar (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hverni gá að nota greiðsluspár viðskiptavinar. Gakktu úr skugga um að ljúka við uppsetningarskrefin áður en þú notar þennan eiginleika. Nánari upplýsingar eru í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md).

Þú getur skoðað greiðsluspár viðskiptavinar á vinnusvæðinu **Stjórna skuldum og innheimtu viðskiptavinar** og á tveimur nýjum listasíðum **Greiðsluspár fyrir hverja færslu** og **Greiðsluspár fyrir hvern viðskiptavin**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Stjórna vinnusvæði skulda og innheimtu viðskiptavinar

Vinnusvæðið **Stjórna skuldum og innheimtu viðskiptavinar** inniheldur tvo nýja reiti, **Greiðsluspár fyrir hverja færslu** og **Viðskiptavinir með stöður sem áætlað er að verði á eftir áætlun**.

- Reiturinn **Greiðsluspár fyrir hverja færslu** sýnir fjölda opinna færslna viðskiptavinar þar sem líkur á að greiðsla sé á réttum tíma eru innan við 50 prósent í rammanum **Á réttum tíma**. Þú getur valið þennan reit til að opna listasíðuna **Greiðsluspár fyrir hverja færslu**.
- Reiturinn **Viðskiptavinir með stöður sem áætlað er að verði á eftir áætlun** sýnir fjölda viðskiptavina þar sem áætlað er að helmingur (50 prósent) af heildarstöðunni verði greiddur seint og/eða mjög seint. Þú getur valið þennan reit til að opna listasíðuna **Greiðsluspár fyrir hvern viðskiptavin**.

[![Viðskiptavinir með stöður sem áætlað er að verði á eftir áætlun](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Listasíða greiðsluspár fyrir hverja færslu

Á listasíðunni **Greiðsluspár fyrir hverja færslu** getur þú skoðað líkurnar á greiðslu fyrir opnar færslur í römmunum **Á réttum tíma**, **Seint**, og **Mjög seint**. Fyrir hverja færslu á hnitanetinu sýnir dálkurinn **Líkur á réttum tíma** líkurnar á því að reikningurinn verði greiddur á eða fyrir gjalddaga. Þegar líkurnar á greiðslu á réttum tíma eru minni en 50 prósent birtist rauður hringur við hliðina á prósentuhlutfallinu í dálkinum **Líkur á réttum tíma** til að tilgreina hættuna á greiðsludrætti.

[![Síða greiðsluspár fyrir hverja færslu](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Í glugganum **Tengdar upplýsingar** hægra megin á síðunni birtast frekari upplýsingar um spárnar:

- Fyrir færsluna sem er valin á hnitanetinu sýnir flýtiflipinn **Greiðsluspá** frekari upplýsingar um greiðsluspár í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**. Hlutinn **Helstu þættir** sýnir helstu þættina sem hafa áhrif á spárnar. Helstu þættir eru eiginleikar valinnar færslu og/eða viðskiptavinurinn fyrir umrædda færslu.
- Flýtiflipinn **Innsýn í viðskiptavini** sýnir núverandi reikning, greiðslu og tölfræði innheimtu fyrir valda færslu.
- Flýtiflipinn **Ferill viðskiptavinar** sýnir greiðsluferil viðskiptavinarins í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.

Gögnin í hlutanum **Helstu þættir** og á flýtiflipunum **Innsýn í viðskiptavini** og **Ferill viðskiptavinar** hjálpa til við að útskýra greiðsluspárnar. Slíkt getur aukið traust þitt á áreiðanleika slíkra spáa.

[![Myndrænir vísar fyrir greiðsluspár í glugganum tengdar upplýsingar](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Listasíða greiðsluspár fyrir hvern viðskiptavin

Listasíðan **Greiðsluspár fyrir hvern viðskiptavin** sýnir opnunarstöðu samtals og upphæðina sem spáð er að greidd verði í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.

[![Síða greiðsluspár fyrir hvern viðskiptavin](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

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

- Fyrir færsluna sem er valin á hnitanetinu sýnir flýtiflipinn **Greiðsluspár** frekari upplýsingar um greiðsluspár í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**. Hlutinn **Helstu þættir** sýnir helstu þættina sem hafa áhrif á greiðslurnar. Helstu þættir eru eiginleikar valinnar færslu og/eða viðskiptavinurinn fyrir umrædda færslu.
- Flýtiflipinn **Innsýn í viðskiptavini** sýnir núverandi reikning, greiðslu og tölfræði innheimtu fyrir valda færslu.
- Flýtiflipinn **Ferill viðskiptavinar** sýnir greiðsluferil viðskiptavinarins í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.

Gögnin í hlutanum **Helstu þættir** og á flýtiflipunum **Innsýn í viðskiptavini** og **Ferill viðskiptavinar** hjálpa til við að útskýra greiðsluspárnar. Slíkt getur aukið traust þitt á áreiðanleika slíkra spáa.

## <a name="improving-the-accuracy-of-payment-predictions"></a>Auka nákvæmni greiðsluspáa

Þú getur skoðað nákvæmni greiðsluspáa með því að opna **Skuldir og innheimta \> Uppsetning \> Fjármálainnsýn \> Færibreytur fjármálainnsýnar**. Á flipanum **Innsýn í greiðslu viðskiptavinar** sýnir hlutinn **Spálíkan** nákvæmni spálíkansins sem prósentuhlutfall.

[![Nákvæmni greiðsluspáa](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Ef nákvæmnin telst ekki vera fullnægjandi skaltu velja tengilinn **Auka nákvæmni líkans** til að opna upplifun AI Builder-viðbótarinnar. Í upplifun AI Builder-viðbótarinnar getur þú valið að hætta við val á svæðum þar til þú hefur valið reitina sem þú telur vera mikilvægasta til að spá fyrir um greiðslulíkur á nákvæman hátt. Þegar því er lokið getur þú auðveldlega endurþjálfað spálíkanið og birt breytingarnar þínar. Nýþjálfaða spálíkanið verður sjálfkrafa valið fyrir spár í Dynamics 365 Finance.

[![Upplifun AI Builder-viðbótar](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Upplýsingar um losun

Almenn forskoðun Fjármálainnsýnar er í boði til uppsetningar í Bandaríkjunum, Evrópu og Bretlandi. Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.

Aðeins er hægt og aðeins skal kveikja á eiginleikum almennrar forskoðunar í tveggja laga sandkassaumhverfi. Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru ekki hægt að flytja yfir í vinnsluumhverfi. Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Tilkynning um persónuvernd

Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]