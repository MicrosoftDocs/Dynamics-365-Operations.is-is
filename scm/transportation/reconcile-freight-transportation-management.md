---
title: "Afstemming farms í flutningsstjórnun"
description: "Þessi grein útskýrir ferli afstemmingar farms."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 88633426fd23370f64730480629ab33ad7124812
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="reconcile-freight-in-transportation-management"></a>Afstemming farms í flutningsstjórnun

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir ferli afstemmingar farms.

Afstemming farms hægt að gera handvirkt eða hægt er að setja hann upp til að eiga sér stað sjálfkrafa. Til að nota afstemmingu farms sjálfvirk, verður að setja upp aðalgögn endurskoðunar þar sem hægt er að skilgreina skilyrði sem ákvarða hvaða farmbréf jafnað sjálfkrafa.

## <a name="the-freight-reconciliation-process"></a>Ferli afstemmingar farms
Farmgjöld eru reiknaðar af taxtavél sem tengist viðkomandi farmflytjanda. Þegar farmur er staðfest farmbréfs er mynduð og farmgjöld eru fluttar í honum. Skatthlutfall farms eru skipts sem ýmis gjöld fyrir viðkomandi upprunaskjalið (innkaupapöntun, sölupöntun, og/eða flutningspöntun), eftir uppsetningu sem er notuð fyrir venjulegum reikningsferli. Ferli afstemmingar farms (sem er einnig þekkt sem samsvarandi) getur hafist þegar farmreikninginn berst frá farmflytjandanum. Hægt er að fá reikningsins rafrænt eða á pappír. Ef reikningurinn er móttekin á pappír, hægt er að mynda rafræna reikninga með því að nota farmbréfið sem sniðmát. 

[![Afstemmingarferli farms](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>handvirkur afstemmingu
Ef verið er að afstemmingu farms handvirkt, verður að samsvara hverri reikningslínu með farmbréf línu eða línum fyrir farm sem verið er að reikningsfæra. Gera þetta jöfnun á **Farmbréf og reikningsjöfnun** síðu. Ef magn á reikningslínu passar ekki við upphæð farmbréf, verður að velja afstemmingarástæða fyrir mismuninn. Ef eru margar ástæður fyrir afstemmingu er hægt að skipta ójöfnuð upphæð á þeim. Ástæða afstemmingu ákvarðar hvernig mismunur upphæðirnar eru bókaðar í fjárhag. Þegar afstemmingu allt reikningsupphæð er tekið, er hún send til samþykkis og síðan bóka færslubókina. Eftirfarandi dæmi sýnir hvernig á að mynda reikning farms og framkvæma afstemmingu farms í Microsoft Dynamics 365 for Operations. 
[![Afstemmingarverkefni farms í Dynamics AX](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>Sjálfvirka afstemmingu
Til að nota sjálfvirka afstemmingu, verður að tilgreina áætlun fyrir afstemmingu, og reikninga og farmflytjendur að nota. Jöfnun reikningslínur og farmbréf er gert eftir uppsetningu á endurskoðunarsniðmát og farmbréfs gerð. Eftir sjálfvirka afstemmingu er keyrð, verður að meðhöndla hvaða reikninga sem kerfið getur ekki samsvarað. Verður svo að vinna þessar reikninga handvirkt áður en hægt er að bóka reikninga til greiðslu.




