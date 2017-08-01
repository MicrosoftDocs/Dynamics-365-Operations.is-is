---
title: "Vinnusvæði greiðslna lánardrottna"
description: "Þetta efnisatriði veitir upplýsingar um lánardrottnagreiðslu á fartækjavinnusvæði. Vinnusvæði greiðslur Lánardrottins sýnir upplýsingar sem tengjast vinnslu greiðslur til lánardrottna."
author: twheeloc
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 4011a2383fe4556b730fa0b6353ba0b9773a4eec
ms.contentlocale: is-is
ms.lasthandoff: 06/14/2017

---

# <a name="vendor-payments-workspace"></a>Vinnusvæði greiðslna lánardrottna

[!include[banner](../includes/banner.md)]

Vinnusvæði **Greiðslur Lánardrottins** sýnir upplýsingar sem tengjast vinnslu greiðslur til lánardrottna. Í þessu vinnusvæði er yfirlitið **Mín vinna** og síðan **Greiningar**. Í **Mínar vinnu** skoða sýnir samantekt tiles hnitanet færslu lánardrottins og tengdar lánardrottnaupplýsingum. Síðan **Greiningar** notar virkni Microsoft Power BI til að birta myndræna framsetningu á lánardrottnagreiðslum.

## <a name="my-work-view"></a>Skoða Mína vinnu

### <a name="summary-tiles"></a>Samantektarreitir

Reitirnir í hlutanum **Samantekt** veita yfirlit yfir stöðu greiðsluupplýsinganna. Hægt er að skoða greiðslubækur sem ekki hafa enn verið bókaðar, reikninga sem eru fram yfir gjalddaga, alla lánardrottna og viðskiptavini sem eru í bið. Frá því **Samantekt** hluta, er hægt að stofna nýja launatímabili.

Upplýsingum í **Samantekt** hluti er fyrir fyrirtækið sem er afskriftareglur skráður í.

### <a name="vendor-transactions-grids"></a>Færslur lánardrottna hnitanet

Hlutinn **Lánardrottnafærslur** inniheldur hnitanet sem sýnir reikninga sem eru gjaldfallnir og greiðslur sem ekki eru jafnaðar. Úr hnitanetinu **Gjaldfallnir reikningar** er hægt að skoða jöfnunarsögu fyrir valinn reikning. Úr hnitanetinu **Ójafnaðar greiðslur** er hægt að skoða jöfnunarsögu fyrir valinn reikning og jafna reikning.

Sé æskilegt að miðstýrðum greiðslum sölumenn með síu sem birtist efst á hverja hnitanetinu til að velja fyrirtæki. Taflan er síðan síuð þannig að það sýnir einungis fyrirtækin sem eru skilgreindar á miðstýrðum greiðslum stigveldisskipan sem afgreiðslumaður miðstýrðum greiðslum hafi heimildir til að skoða.

Í **Finna færslur** flipanum á **lánardrottnafærslur** hlutanum kleift að leita í færslu lánardrottins.

### <a name="related-information"></a>Tengdar upplýsingar

Hægt er að skoða í **Lánardrottins aldursgreiningarramma** skýrslu og **samantekt Greiðslu með** skýrslu með því að nota tenglana í í **Tengdar upplýsingar** hluta vinnusvæðisins.

## <a name="analytics-page"></a>Greiningasíða

Í **Samantektarlíkön** síða veitir mikilvæg mælikvörðum, svo sem reikninga lánardrottna sem eru fram gjalddaga og reikningar lánardrottins sem hafa gjalddaga í framtíðinni. Þessi síða inniheldur níu skýrslusíður. Ein síða veitir yfirlit og aðrar átta síður veita upplýsingar um Reikninga lánardrottna greiðslu mælikvörðum.

Eftirfarandi tafla sýnir sýnigögn sem eru tiltæk á hverri skýrslusíðu.

| Skýrslusíða | Myndbirting |
|-------------|---------------|
| Yfirlit yfir greiðslu lánardrottins | <ul><li>Gjaldfallnir reikningar</li><li>Reikningar á gjalddaga í dag</li><li>Afslættir gerð tapað afslætti</li><li>Reikningar til greiðslu í framtíðinni eftir staðgreiðsluafsláttardagsetningu</li><li>Reikningar til greiðslu í framtíðinni eftir gjalddaga</li><li>Reikningar greiddir seint reikningar greiddir tímanlega</li><li>Greiðsluverkflæðisúthlutun</li><li>Staða lánardrottins/viðskiptavinar</li><li>Opnir reikningar með greiðslubið</li></ul> |
| Gjaldfallnir reikningar | <ul><li>Gjaldfallnir reikningar</li><li>Gjalddagaupplýsingar reikninga</li><li>Samtala opinna reikninga</li><li>Gjaldfallnir reikningar eftir lánardrottnahóp</li><li>Gjaldfallnir reikningar á hvert fyrirtæki</li></ul> |
| Reikningar á gjalddaga í dag | <ul><li>Reikningar á gjalddaga í dag</li><li>Upplýsingar um reikninga á gjalddaga í dag</li><li>Rikningar gjaldfallnir í dag á hvert fyrirtæki</li><li>Reikningar gjaldfallnir í dag eftir lánardrottnahóp</li></ul> |
| Afslættir gerð tapað afslætti | <ul><li>Notaður afsláttur til tapaðs afsláttar</li><li>Upplýsingar um notaðan afslátt til tapaðs afsláttar</li><li>Notaður afsláttur til tapaðs afsláttar eftir fyrirtæki</li><li>Notaður afsláttur til tapaðs afsláttar eftir lánardrottnahóp</li></ul> |
| Reikningar gjaldfallir í framtíðinni | <ul><li>Reikningar gjaldfallir í framtíðinni</li><li>Upplýsingar um reikninga sem gjaldfalla í framtíðinni</li><li>Reikningar greiðslu í framtíðinni fyrir hvert fyrirtæki</li><li>Reikningar gjaldfallnir í framtíðinni eftir lánardrottnahóp</li><li>Reikningar til greiðslu í framtíðinni eftir staðgreiðsluafsláttardagsetningu</li><li>Reikningar til greiðslu í framtíðinni eftir gjalddaga</li></ul> |
| Reikningar greiddir seint | <ul><li>Reikningar greiddir eftir gjalddaga</li><li>Upplýsingar um reikninga greidda eftir gjalddaga</li><li>Reikningar greiddir eftir gjalddaga eftir fyrirtæki</li><li>Reikningar greiddir eftir gjalddaga eftir lánardrottnahóp</li><li>Reikningar greiddir seint á móti reikningum greiddum tímanlega</li></ul> |
| Greiðsluverkflæði | <ul><li>Verkflæðistilvik lánardrottnagreiðslna</li><li>Verkflæðistilvik lánardrottnagreiðslna eftir samþykktaraðila</li><li>Verkflæðistilvik lánardrottnagreiðslna eftir fyrirtæki</li><li>Meðaltal daga í verkflæði eftir samþykkjanda</li></ul> |
| Staða lánardrottins/viðskiptavinar | <ul><li>Staða lánardrottins/viðskiptavinar</li><li>Staða lánardrottins/viðskiptavinar eftir fyrirtæki</li><li>Upplýsingar um stöðu lánardrottins/viðskiptavinar</li></ul> |
| Reikningar með greiðslubið | <ul><li>Reikningar með greiðslubið</li><li>Reikningar með upplýsingar um greiðslubið</li><li>Reikningar með greiðslubið eftir fyrirtæki</li><li>Reikningar með greiðslubið eftir lánardrottnahóp</li></ul> |
