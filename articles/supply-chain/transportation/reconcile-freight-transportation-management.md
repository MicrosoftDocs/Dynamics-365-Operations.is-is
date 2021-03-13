---
title: Afstemming farms í flutningsstjórnun
description: Þetta efni útskýrir ferli afstemmingar farms.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014509"
---
# <a name="reconcile-freight-in-transportation-management"></a>Afstemming farms í flutningsstjórnun

[!include [banner](../includes/banner.md)]

Þetta efni útskýrir ferli afstemmingar farms.

Afstemming farms hægt að gera handvirkt eða hægt er að setja hann upp til að eiga sér stað sjálfkrafa. Til að nota afstemmingu farms sjálfvirk, verður að setja upp aðalgögn endurskoðunar þar sem hægt er að skilgreina skilyrði sem ákvarða hvaða farmbréf jafnað sjálfkrafa.

## <a name="the-freight-reconciliation-process"></a>Ferli afstemmingar farms

Farmgjöld eru reiknaðar af taxtavél sem tengist viðkomandi farmflytjanda. Þegar farmur er staðfest farmbréfs er mynduð og farmgjöld eru fluttar í honum. Skatthlutfall farms eru skipts sem ýmis gjöld fyrir viðkomandi upprunaskjalið (innkaupapöntun, sölupöntun, og/eða flutningspöntun), eftir uppsetningu sem er notuð fyrir venjulegum reikningsferli. Ferli afstemmingar farms (sem er einnig þekkt sem samsvarandi) getur hafist þegar farmreikninginn berst frá farmflytjandanum. Hægt er að fá reikningsins rafrænt eða á pappír. Ef reikningurinn er móttekin á pappír, hægt er að mynda rafræna reikninga með því að nota farmbréfið sem sniðmát.

[![Afstemmingarferli farms](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>handvirkur afstemmingu

Ef verið er að afstemmingu farms handvirkt, verður að samsvara hverri reikningslínu með farmbréf línu eða línum fyrir farm sem verið er að reikningsfæra. Gera þetta jöfnun á **Farmbréf og reikningsjöfnun** síðu. Ef magn á reikningslínu passar ekki við upphæð farmbréf, verður að velja afstemmingarástæða fyrir mismuninn. Ef eru margar ástæður fyrir afstemmingu er hægt að skipta ójöfnuð upphæð á þeim. Ástæða afstemmingu ákvarðar hvernig mismunur upphæðirnar eru bókaðar í fjárhag. Þegar afstemmingu allt reikningsupphæð er tekið, er hún send til samþykkis og síðan bóka færslubókina. Eftirfarandi dæmi sýnir hvernig á að mynda reikning farms og framkvæma afstemmingu farms.

[![Afstemmingarverk farms](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>Sjálfvirka afstemmingu

Til að nota sjálfvirka afstemmingu, verður að tilgreina áætlun fyrir afstemmingu, og reikninga og farmflytjendur að nota. Jöfnun reikningslínur og farmbréf er gert eftir uppsetningu á endurskoðunarsniðmát og farmbréfs gerð. Eftir sjálfvirka afstemmingu er keyrð, verður að meðhöndla hvaða reikninga sem kerfið getur ekki samsvarað. Verður svo að vinna þessar reikninga handvirkt áður en hægt er að bóka reikninga til greiðslu.

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>Stemma farmbréf við farmreikninga með sjálfvirkri eða handvirkri afstemmingu

*Samsvörun* er ferli sem finnur farmbréfin sem stemma við hvern farmreikning. Þetta er hægt að gera með því að samsvara reikningslínurnar hver af annarri (handvirk samsvörun) eða með því að samsvara alla tiltæka reikninga í einu (sjálfvirk samsvörun).

### <a name="auto-matching"></a>Jafna sjálfvirkt

Þegar margir farmreikningar eru samsvaraðir við sama farmbréfið, þá gengur sjálfvirka samsvörunarferlið svona fyrir sig:

1. Allir farmreikningar sem ekki eru samsvaraðir er raðað eftir upphæð þar sem hæsta upphæðin kemur fyrst.
1. Farmreikningarnir eru samsvaraðir einn af einum þar til farmbréfið er ekki lengur með neinar jákvæðar upphæðir.
1. Eftirstandandi upphæð er stillt eftir því hver uppsetning á endurskoðunarsniðmátinu er og eftirstandandi upphæð á farmreikningum.

### <a name="manual-matching"></a>Handvirk samsvörun

Öll farmbréf með jákvæðum upphæðum verða hægt að samsvara. Notandi getur, með svipuðum hætti og í sjálfvirkri samsvörun, aðeins samsvarað farmreikninga með neikvæðum upphæðum við farmbréf sem ekki eru samsvöruð að fullu.

### <a name="example"></a>Dæmi

Segjum að þú sért með farmbréf að upphæð 1500 og þú hefur stofnað þrjá farmreikninga fyrir farmbréfið með einni reikningslínu fyrir hvern reikning með eftirfarandi stillingum:

- Upprunalegt farmbréf: Upphæð 1500
- Reikningur 1 (Inv1): Upphæð 1000
- Reikningur 2 (Inv2): Upphæð 600
- Reikningur 3 (Inv3): Upphæð -100

#### <a name="automatic-matching-result"></a>Niðurstöður sjálfvirkrar samsvörunar

Sjálfvirk jöfnun mun keyra í eftirfarandi röð:

1. Raða öllum farmreikningum eftir upphæð í lækkandi röð: Inv1 -> Inv2 -> Inv3.
1. Jafna Inv1 við FB. Inv1 er með 1000 samsvarað og farmbréfið er með upphæð 500 þannig að staðan er stillt á *Samsvörun að hluta til*.
1. Jafna Inv2 við FB. Inv2 er með 500 samsvarað og farmbréfið er með 0 eftirstandandi þannig að staðan er stillt á *Samsvörun að fullu*.
1. Vegna þess að FB er nú að fullu jafnað verður Inv3 ekki unnið.

#### <a name="manual-matching-result"></a>Niðurstöður handvirkrar samsvörunar

Fyrir handvirka samsvörun fara niðurstöðurnar eftir röð samsvörunar eins og sýnt er í eftirfarandi dæmum.

##### <a name="manual-matching-case-1"></a>Handvirk samsvörun máls 1

Ein leið til að gera handvirka samsvörun í þessu dæmi er að halda áfram á eftirfarandi hátt:

1. Jafna FB með Inv1. Farmbréf er með 500 sem eftirstandandi upphæð þannig að staðan er stillt á *Samsvörun að hluta til*.
1. Jafna Inv2 við FB. Inv2 er með 500 samsvarað og farmbréfið er með 0 eftirstandandi þannig að staðan er stillt á *Samsvörun að fullu*.
1. Við handvirka samsvörun á Inv3 finnurðu engin ójöfnuð farmbréf.

Þetta tilfelli er í meginatriðum það sama og sjálfvirk samsvörun

##### <a name="manual-matching-case-2"></a>Handvirk samsvörun máls 2

Önnur leið til að gera handvirka samsvörun í þessu dæmi er að halda áfram á eftirfarandi hátt:

1. Jafna Inv3 við FB. Nú er farmbréfið með 1600 í eftirstöðvar sem er það sama og að draga frá neikvæða 100 ofan á 1500. Bæði farmbréfið og Inv3 eru með samsvaraða upphæð -100.
1. Jafna Inv1 og Inv 2 við farmbréf eitt á eftir öðru. Farmbréf er að samsvarað að fullu.

Eins og þetta dæmi sýnir á aðeina að samsvara farmreikninga með neikvæðum upphæðum handvirkt. Þetta tryggir að það sé alltaf hægt að samsvara farmreikninga með neikvæðum upphæðum við farmbréf sem ekki er samsvarað að fullu vegna þess að það gerir notanda kleift að hafa stjórnun á röð samsvörunar.
