---
title: Tvöfaldur gjaldeyrisstuðningur fyrir skatta
description: Þetta efni útskýrir hvernig á að framlengja tvískiptan gjaldeyrisbókhald á skattalénum og áhrifin á útreikning skatta og bókun
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0a3245febe31857181d17bba42e12b65f4ebb40f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832971"
---
# <a name="dual-currency-support-for-sales-tax"></a>Tvöfaldur gjaldeyrisstuðningur fyrir virðisaukaskatt
[!include [banner](../includes/banner.md)]

Þetta efni útskýrir hvernig á að framlengja tvískipt gjaldeyrisbókhald fyrir virðisaukaskatt og áhrifin á útreikning virðisaukaskatts, bókun og uppgjör.

Eiginleikinn Tvískiptur gjaldmiðill fyrir Dynamics 365 Finance var kynntur í útgáfu 8.1 (október 2018). Hann breytir því hvernig bókhaldsskýrslur í skýrslugjaldmiðlinum eru reiknaðar.

Í fyrri útgáfum var færslum breytt í skýrslugjaldmiðilinn í eftirfarandi röð: 

- Heildarfjárhæð færslna var reiknuð í færslugjaldmiðlinum > Færsluupphæðin var umreiknuð í bókhaldsgjaldmiðil > Upphæð bókhaldsgjaldmiðils var umreiknuð í skýrslugjaldmiðilinn

Eftir að kveikt var á tvískiptum gjaldeyriseiginleika voru færslur umreiknaðar í skýrslugjaldmiðilinn í eftirfarandi röð:

- Færslugjaldmiðilsupphæð > skýrslugjaldmiðilsupphæð

Nánari upplýsingar um tvískiptan gjaldmiðil er að finna í [Tvöfaldur gjaldmiðill](dual-currency.md).

Sem afleiðing af stuðningi við tvískipta gjaldmiðla eru tveir nýir möguleikar fáanlegir í eiginleikastjórnun: 

- Umreikningur virðisaukaskatts (nýtt í útgáfu 10.0.13)

Tvöfaldur gjaldmiðilsstuðningur við virðisaukaskatta tryggir að skattar eru reiknaðir nákvæmlega í skattagjaldmiðlinum og að uppgjörsstaða virðisaukaskatts er reiknuð nákvæmlega bæði í bókhaldsgjaldmiðli og skýrslugjaldmiðli. 

## <a name="sales-tax-conversion"></a>Umskráning virðisaukaskatts

Færibreytan **Virðisaukaskattsbreyting** býður upp á tvo möguleika til að umreikna skattafjárhæð úr færslugjaldmiðli yfir í skattagjaldmiðil. 

- Bókhaldsgjaldmiðill: Slóðin verður „Upphæð í færslugjaldmiðli > Upphæð í bókhaldsgjaldmiðli > Upphæð í skattagjaldmiðli”. Gengisgerð bókhaldsgjaldmiðilsins (stillt í fjárhagsuppsetningu) verður notuð fyrir umreikning gjaldmiðils.
- Skýrslugjaldmiðill: Slóðin verður „Upphæð í færslugjaldmiðli > Upphæð í skýrslugjaldmiðli > Upphæð í skattagjaldmiðli”. Gengisgerð skýrslugjaldmiðils (stillt í fjárhagsuppsetningu) verður notuð fyrir umreikning gjaldmiðils.

### <a name="example"></a>Dæmi

Einfalt dæmi til að sýna fram á þessa virkni er:

Gjaldeyrisuppsetning fyrir fjárhag og skatta

| Færslugjaldmiðill | Bókhaldsgjaldmiðill | Skýrslugjaldmiðill | Skattagjaldmiðill |
| -------------------- | ------------------- | ------------------ | ------------ |
| EUR                  | USD                 | GBP                | GBP          |

Gengi

| Úr gjaldmiðli | Í gjaldmiðil | Stuðull | Gengi |
| ------------- | ----------- | ------ | ------------- |
| EUR           | USD         | 1      | 1.11          |
| EUR           | GBP         | 1      | 0.83          |
| USD           | GBP         | 1      | 0.75          |

Útreikningur skattaupphæðar í mismunandi færibreytuvalkostum

Skattaupphæð = 100 EUR

| Færibreytur umreiknings á virðisaukaskatti | Færslugjaldmiðill (EUR) | Bókhaldsgjaldmiðill (USD) | Skýrslugjaldmiðill (GBP) | Skattagjaldmiðill (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Bókhaldsgjaldmiðill             | 100                        | 111                       | 83                       | **83.25**          |
| Skýrslugjaldmiðill              | 100                        | 111                       | 83                       | **83**             |

Hægt er að stilla þessa færibreytu út frá samræmiþörf skattayfirvalda.


### <a name="upgrade-consideration"></a>Uppfæra umhugsunarefni

Þessi eiginleiki á aðeins við um nýjar færslur. Fyrir skattafærslu sem þegar er vistuð í TAXTRANS-töflunni en ekki enn gerð upp mun kerfið ekki endurútreikna skattaupphæð í skattagjaldmiðli þar sem gengi þegar skattur var bókaður vantar nú þegar.

Til að koma í veg fyrir fyrri atburðarás mælum við með því að breyta þessu færibreytugildi á nýju (hreinu) skattuppgjörstímabili sem ekki inniheldur óuppgerðar skattafærslur. Til að breyta þessu gildi á miðju skattauppgjörstímabili, vinsamlegast keyrðu forritið „Jafna og bóka virðisaukaskatt” fyrir núverandi skattauppgjörstímabil áður en þú breytir þessu færibreytugildi.


## <a name="track-reporting-currency-tax-amount"></a>Rekja skattaupphæð skýrslugjaldmiðils

Þremur nýjum reitum var bætt við skattskyldar töflur til að rekja fjárhæðir í skýrslugjaldmiðlinum. Þessir reitir eru í töflunum TAXUNCOMMITTTED og TAXTRANS:

- TaxAmountRep: skattaupphæð í skýrslugjaldmiðli
- TaxBaseAmountRep: grunnupphæð í skýrslugjaldmiðli
- TaxInCostPriceRep: ekki frádráttarbær fjárhæð í skýrslugjaldmiðli

Fyrir skatt sem eingöngu er vistaður í töflunni TAXUNCOMMITTTED en ekki enn verið bókaður mun kerfið endurreikna skattaupphæð í skýrslugjaldmiðli við bókun og vista í TAXTRANS töflunni.

Þessi útgáfa mun ekki innihalda breytingar á skýrslum og eyðublöðum sem sýna skattaupphæðina í skýrslugjaldmiðlinum. Breytingar á skýrslum og eyðublöðum verða afhentar í framtíðinni.



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a>Sjálfvirk staða skattauppgjörs í skýrslugjaldmiðli

Ef skattauppgjör er ekki jafnað í skýrslugjaldmiðli af einhverri ástæðu, svo sem að slóð umreiknings virðisaukaskatts er „Bókhaldsgjaldmiðill“, eða gengisbreyting er á einu skattjöfnunartímabili, þá myndar kerfið sjálfkrafa bókhaldsfærslur til að leiðrétta frávik skattupphæðar og mótfærir það gegn innleystum gengishagnaði/taplykli, sem er skilgreindur í fjárhagsgrunni.

Notaðu fyrra dæmið til að sýna fram á þennan eiginleika, gerðu ráð fyrir að gögnin í TAXTRANS töflunni við bókun séu eftirfarandi.

| Færibreytur umreiknings á virðisaukaskatti | Færslugjaldmiðill (EUR) | Bókhaldsgjaldmiðill (USD) | Skýrslugjaldmiðill (GBP) | Skattagjaldmiðill (GBP) |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| Bókhaldsgjaldmiðill             | 100                        | 111                       | 83                       | **83.25**          |
| Skýrslugjaldmiðill              | 100                        | 111                       | 83                       | **83**             |

Þegar þú keyrir uppgjörsáætlun virðisaukaskatts í lok mánaðarins verður bókhaldsfærslan eftirfarandi:
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a>Aðstæður: umreikningur virðisaukaskatts = „Bókhaldsgjaldmiðill”

| Aðallykill           | Færslugjaldmiðill (GBP) | Bókhaldsgjaldmiðill (USD) | Skýrslugjaldmiðill (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Inn- og útskattur | -83.25                     | -111                      | -83.25                   |
| Skattauppgjör         | 83.25                      | 111                       | 83.25                    |
| Innleystur hagnaður/tap     | 0                          | 0                         | -0.25                    |
| Inn- og útskattur | 0                          | 0                         | 0.25                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a>Aðstæður: umreikningur virðisaukaskatts = „Skýrslugjaldmiðill”


| Aðallykill           | Færslugjaldmiðill (GBP) | Bókhaldsgjaldmiðill (USD) | Skýrslugjaldmiðill (GBP) |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| Inn- og útskattur | -83                        | -110.67                   | -83                      |
| Skattauppgjör         | 83                         | 110.67                    | 83                       |
| Innleystur hagnaður/tap     | 0                          | 0.33                      | 0                        |
| Inn- og útskattur | 0                          | -0.33                     | 0                        |



Frekari upplýsingar er hægt að finna í eftirfarandi efni:

- [Tvöfaldur gjaldmiðill](dual-currency.md)
- [Yfirlit virðisaukaskatts](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]