---
title: Uppfæra fjárhagsáætlun frá fyrra tímabili eftir lækkun innkaupapantana og reikninga
description: Í þessari grein er því lýst hvernig á að stjórna því hvað verður um fjárhagsáætlun frá fyrra tímabili þegar hætt er við innkaupapantanir eða þær eru lækkaðar og þegar reikningar eru lækkaðir.
author: TaylorVH
ms.date: ''
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: TaylorVH
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: Version 1611
ms.search.form: LedgerFund
ms.openlocfilehash: 790f1e770fd77d5209436c1c89e0f6125aac150f
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573047"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Uppfæra fjárhagsáætlun frá fyrra tímabili eftir lækkun innkaupapantana og reikninga

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessari grein er því lýst hvernig á að stjórna því hvað verður um fjárhagsáætlun frá fyrra tímabili þegar hætt er við innkaupapantanir eða þær eru lækkaðar og þegar reikningar eru lækkaðir.

Frekari upplýsingar um vinnslu innkaupapantana í lok árs eru í [Meðhöndla innkaupapantanir í lok árs](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Kveikja eða slökkva á lækkun fjárhagsáætlunar frá fyrra tímabili vegna reikningsfrávika

Kerfið getur alltaf uppfært fjárhagsáætlun frá fyrra tímabili þegar hætt er við innkaupapöntun eða hún er minnkuð. Hins vegar ef þú vilt uppfæra fjárhagsáætlun frá fyrra tímabili þegar reikningur er lækkaður verður þú að kveikja á eiginleikanum *Lækka áætlun frá fyrra tímabili þegar reikningur gagnvart innkaupapöntun er lækkaður með fráviki*. Stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita á vinnusvæðinu **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Lækkanir og afturkallanir á innkaupapöntun

Óháð því hvort kveikt á eiginleikanum *Lækka áætlun frá fyrra tímabili þegar reikningur gagnvart innkaupapöntun er lækkaður með fráviki* verður fjárhagsáætlun frá fyrra tímabili uppfærð þegar fallið er frá gjaldgengri innkaupapöntun eða hún er minnkuð. Hægt er að stilla hvern fjárhag til að svara á einn af eftirfarandi háttum:

- Varðveita fjárhagsáætlun frá fyrra tímabili eins og hún var stofnuð.
- Breyta sjálfkrafa fjárhagsáætlun frá fyrra tímabili til að fjarlægja niðurfellda eða lækkaða upphæð.

Aðeins innkaupapantanalínur sem eru með dreifingar sem innihalda sjóð eru tiltækar til sjálfvirka leiðréttingu fjárhagsáætlunar. Sjálfvirk leiðrétting fjárhagsáætlunar á sér stað þegar gengið er frá innkaupapöntun eða lækkun innkaupapöntunar er staðfest.

## <a name="invoice-reductions"></a>Reikningslækkanir

Þegar kveikt er á eiginleikanum *Lækka áætlun frá fyrra tímabili þegar reikningur gagnvart innkaupapöntun er lækkaður með fráviki* er hægt að tilgreina hvort hver sjóður eigi að lækka fjárhagsáætlun frá fyrra tímabili þegar reikningur er lækkaður, til viðbótar við þegar innkaupapöntun er lækkuð eða felld niður. Reikningurinn verður að vera fyrir innkaupapöntun með áætlun frá fyrra tímabili. Lækkanir fela í sér verðfrávik, gjaldafrávik og skattafrávik. Þegar innkaupapöntun frá fyrra tímabili er lækkuð við reikningagerð er búið til frávik. Þegar reikningurinn er bókaður lækkar fjárúthlutun innkaupapöntunar um upphæð fráviksins. Þessi eiginleiki mun einnig búa til sjálfvirka leiðréttingu fjárhagsáætlunar fyrir upphæð fráviksins.

Þegar slökkt er á eiginleikanum *Lækka áætlun frá fyrra tímabili þegar reikningur gagnvart innkaupapöntun er lækkaður með fráviki* er fjárhagsáætlun frá fyrra tímabili ekki lækkuð við þessar aðstæður. Af þessum sökum er eftirstandandi upphæð fjárhagsáætlunar frá fyrra tímabili fyrir frávikið haldið eftir.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Skilgreina valkosti fjárhagsáætlunar frá fyrra tímabili fyrir hvern sjóð

Fylgdu þessum skrefum fyrir hvern fjárhagssjóð sem ætti að geta lækkað fjárhagsáætlun frá fyrra tímabili þegar innkaupapöntun eða reikningur er lækkaður.

1. Farðu í **Fjárhagur \> Bókhaldslyklar \> Sjóðir \> Sjóðir**.
1. Velja sjóðinn sem á að setja upp.
1. Undir **Ársendaferli innkaupapöntunar** skal tryggja að valkosturinn **Hnekkja völdum valkosti ársloka** sé stilltur á *Já*.
1. Undir **Staða fjárhagsáætlunar frá fyrra tímabili** skal stilla reitinn **Endurskipa fjárhagsáætlunina þegar hætt er við innkaupapöntun frá fyrra tímabili eða hún er minnkuð** eftir þörfum. Stillingarnar hafa mismunandi áhrif, allt eftir því hvort kveikt er á eiginleikinn *Lækka áætlun frá fyrra tímabili þegar reikningur gagnvart innkaupapöntun er lækkaður með fráviki* í kerfinu.

    - Þegar slökkt er á eiginleikanum bregst kerfið aðeins við innkaupapöntunum sem hætt er við eða sem eru lækkaðar. Valkostastillingarnar virka á eftirfarandi hátt:

        - *Nei* – Kerfið býr til færslu í fjárhagsáætlunarskrá fyrir eftirstöðvar innkaupapantana sem hafa verið felldar niður eða lækkaðar.
        - *Já* – Kerfið leyfir að innkaupapantanir séu felldar niður eða þeim fækkað en býr ekki til færslu í fjárhagsáætlunarskrá. Fjárhagsáætlun frá fyrra tímabili er áfram aðgengileg til neyslu með öðrum skjölum.

    - Þegar kveikt er á eiginleikanum bregst kerfið bæði við reikningsfrávikum og innkaupapöntunum sem hætt er við eða sem eru lækkaðar. Valkostastillingarnar virka á eftirfarandi hátt:

        - *Nei* – Kerfið býr til færslu í fjárhagsáætlunarskrá á móti innkaupapöntuninni fyrir lækkunarupphæð fráviks. Þessi stilling hefur sömu áhrif og þegar slökkt er á eiginleikanum þegar hætt er við innkaupapöntun eða hún er lækkuð.
        - *Já* – Kerfið leyfir lækkun reikninga en býr ekki til færslu í fjárhagsáætlunarskrá fyrir reikningsfrávik. Fjárhagsáætlun frá fyrra tímabili er áfram aðgengileg til neyslu með öðrum skjölum. Þessi stilling hefur sömu áhrif og þegar slökkt er á eiginleikanum þegar hætt er við innkaupapöntun eða hún er lækkuð.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Meðhöndla innkaupapantanir í lok árs](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Vinna með almennar frátektir fjárhagsáætlunar](general-budget-reservation-tasks.md)
- [Sjóðir hjá hinu opinbera](funds-public-sector.md)
- [Setja upp sjóð fyrir opinberi geirann](tasks/set-up-fund-public-sector.md)
