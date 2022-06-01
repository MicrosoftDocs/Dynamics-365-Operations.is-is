---
title: Uppfæra yfirfærslu fjárhagsáætlunar eftir lækkun á innkaupapöntunum og reikningum
description: Þetta efnisatriði lýsir því hvernig á að stjórna því hvað verður um yfirfærslu fjárhagsáætlunar þegar innkaupapantanir eru afturkallaðar eða lækkaðar og þegar reikningar eru lækkaðir.
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 3b0f06b8d5a38252fc8ff6662f3d454adffffe60
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803043"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Uppfæra yfirfærslu fjárhagsáætlunar eftir lækkun á innkaupapöntunum og reikningum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði lýsir því hvernig á að stjórna því hvað verður um yfirfærslu fjárhagsáætlunar þegar innkaupapantanir eru afturkallaðar eða lækkaðar og þegar reikningar eru lækkaðir.

Fyrir upplýsingar um hvernig innkaupapantanir eru unnar í árslok, sjá [Afgreiða innkaupapantanir í árslok](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Kveiktu eða slökktu á flutningslækkunum fjárhagsáætlunar fyrir reikningsfrávik

Kerfið getur alltaf uppfært yfirfærslukostnaðaráætlun þegar innkaupapöntun er afturkölluð eða lækkuð. Hins vegar, ef þú vilt uppfæra yfirfærslu fjárhagsáætlunar þegar reikningur er lækkaður, verður þú að kveikja á *Draga úr yfirfærslukostnaði þegar reikningur á móti innkaupapöntun er lækkaður með fráviki* eiginleiki. Stjórnendur geta kveikt eða slökkt á þessum eiginleika með því að leita að honum í **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** vinnurými.

## <a name="purchase-order-reductions-and-cancellations"></a>Lækkun innkaupapöntunar og afpöntun

Burtséð frá því hvort *Draga úr yfirfærslukostnaði þegar reikningur á móti innkaupapöntun er lækkaður með fráviki* kveikt er á eiginleikum, verður kostnaðarhámarkið til yfirfærslu uppfært þegar gjaldgeng innkaupapöntun er afturkölluð eða lækkuð. Þú getur stillt hvern aðalbókarsjóð til að bregðast við á einn af eftirfarandi leiðum:

- Halda áframhaldandi fjárhagsáætlun eins og hún var búin til.
- Stilltu sjálfkrafa yfirfærslukostnaðaráætlun til að fjarlægja afturkallaða eða lækkaða upphæð.

Aðeins innkaupapöntunarlínur sem hafa dreifingar sem innihalda sjóð eru tiltækar fyrir sjálfvirka leiðréttingu fjárhagsáætlunar. Sjálfvirk leiðrétting fjárhagsáætlunar á sér stað þegar innkaupapöntun er lokið eða lækkun innkaupapöntunar er staðfest.

## <a name="invoice-reductions"></a>Lækkun reikninga

Þegar *Draga úr yfirfærslukostnaði þegar reikningur á móti innkaupapöntun er lækkaður með fráviki* kveikt er á eiginleikum geturðu tilgreint hvort hver sjóður eigi að lækka yfirfærsluáætlun þegar reikningur er lækkaður, auk þess sem innkaupapöntun er lækkuð eða afturkölluð. Reikningurinn verður að vera fyrir innkaupapöntun sem hefur yfirfærslukostnað. Lækkunin felur í sér verðfrávik, gjaldfrávik og skattfrávik. Þegar yfirfærð innkaupapöntun er lækkuð við reikningagerð myndast frávik. Þegar reikningurinn er bókaður mun kvaðning innkaupapöntunar lækka um upphæð fráviksins. Eiginleikinn mun einnig búa til sjálfvirka leiðréttingu fjárhagsáætlunar fyrir upphæð fráviksins.

Þegar *Draga úr yfirfærslukostnaði þegar reikningur á móti innkaupapöntun er lækkaður með fráviki* slökkt er á eiginleikum, þá er framfærsla fjárhagsáætlunar ekki skert í þessari atburðarás. Þess vegna er eftirstandandi yfirfærslufjárveiting fyrir upphæð fráviksins skilin eftir.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Stilltu yfirfærslumöguleika fjárhagsáætlunar fyrir hvern sjóð

Fylgdu þessum skrefum fyrir hvern bókhaldssjóð sem ætti að geta dregið úr yfirfærslukostnaði þegar innkaupapöntun eða reikningur er lækkaður.

1. Fara til **Aðalbók \> Reikningsyfirlit \> Sjóðir \> Sjóðir**.
1. Veldu sjóðinn sem þú vilt stofna.
1. Undir **Innkaupapöntun árslokaferli**, vertu viss um að **Hneka valinn árslokavalkost** valkostur er stilltur á *Já*.
1. Undir **Staða fjárhagsáætlunar yfirfærslu**, stilltu **Settu fjárhagsáætlunina aftur inn þegar yfirfærð innkaupapöntun er afturkölluð eða lækkuð** reit eins og þú þarfnast. Stillingarnar hafa aðeins mismunandi áhrif, eftir því hvort *Draga úr yfirfærslukostnaði þegar reikningur á móti innkaupapöntun er lækkaður með fráviki* kveikt er á eiginleikanum í kerfinu þínu.

    - Þegar slökkt er á eiginleikanum bregst kerfið aðeins við afturkölluðum eða minni innkaupapöntunum. Valkostastillingarnar virka á eftirfarandi hátt:

        - *Nei* – Kerfið býr til færslu fjárhagsáætlunarskrár fyrir eftirstöðvar innkaupapantana sem hafa verið afturkallaðar eða lækkaðar.
        - *Já* – Kerfið gerir kleift að hætta við eða minnka innkaupapantanir, en býr ekki til fjárhagsáætlunarskrárfærslu. Fjárhagsáætlunin er áfram tiltæk til notkunar fyrir önnur skjöl.

    - Þegar kveikt er á eiginleikanum bregst kerfið bæði við reikningsfrávikum og afturkölluðum eða lækkuðum innkaupapöntunum. Valkostastillingarnar virka á eftirfarandi hátt:

        - *Nei* – Fyrir reikningsfrávik stofnar kerfið færslu fjárhagsáætlunarskrár á móti innkaupapöntuninni fyrir frávikslækkunarupphæðina. Fyrir afturkallaðar eða minnkaðar innkaupapantanir hefur þessi stilling sömu áhrif og hún hefur þegar slökkt er á eiginleikanum.
        - *Já* – Fyrir reikningsfrávik leyfir kerfið lækkun reiknings en býr ekki til færslu fjárhagsáætlunarskrár. Fjárhagsáætlunin er áfram tiltæk til notkunar fyrir önnur skjöl. Fyrir afturkallaðar eða minnkaðar innkaupapantanir hefur þessi stilling sömu áhrif og hún hefur þegar slökkt er á eiginleikanum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Meðhöndla innkaupapantanir í lok árs](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Vinna með almennar frátektir fjárhagsáætlunar](general-budget-reservation-tasks.md)
- [Sjóðir hjá hinu opinbera](funds-public-sector.md)
- [Setja upp sjóð fyrir opinberi geirann](tasks/set-up-fund-public-sector.md)
