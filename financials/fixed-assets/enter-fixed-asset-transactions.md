---
title: "Eignafærslukostir"
description: "Þessi grein lýsir mismunandi aðferðum sem eru tiltækar til að stofna eignafærslu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 40ab6f8d7e7b7a04ec1533acf2919dea345b0804
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="fixed-asset-transaction-options"></a>Eignafærslukostir

[!include[banner](../includes/banner.md)]


Þessi grein lýsir mismunandi aðferðum sem eru tiltækar til að stofna eignafærslu.

Þú getur sett upp eign fyrir sameiningu með viðskiptaskuldir, viðskiptakröfur, innkaup og uppruna og fjárhag. Einnig er hægt að flytja vörur í birgðastjórnun á eignir eigi að nota þær vörur innan kerfis.

## <a name="accounts-payable"></a>Viðskiptaskuldir
Hægt er að færa inn eignafærslur í síðunni færslubókarfylgiskjal. Þessa síða er aðeins hægt að opna úr skjámyndinni reikningabók. Einnig er hægt að opna síðuna færslubókarfylgiskjal frá síðu færslubókarsamþykkt reiknings. Í svæðinu mótlykill, veljið eignir. Síðan, í  mótlykill reit verður að velja númer eignar. Á flipanum eignir færirðu inn gildi í reitina færslugerð og bók.

## <a name="accounts-receivable"></a>Viðskiptakröfur
Hægt er að færa inn eignafærslur í síðunni reikningur með frjálsum texta.  Veljið línuatriði í síðunni reikningur með frjálsum texta, í hnitanetinu reikningslínur. Smellið á flýtiflipa „Upplýsingar um línur“. Færðu inn eignanúmer og bók fyrir afskráningarfærslu. Fyrir reikninga með valfrjálsum texta er gerð eignafærslunnar alltaf afskráninga - sala.

## <a name="procurement-and-sourcing"></a>Innkaup og aðföng
Hægt er að færa inn eignafærslur í síðunni innkaupapöntun. Færa skal inn allar upplýsingar sem krafist er til að búa til innkaupapöntun og síðan smella á Í lagi. Í síðunni innkaupapöntun, Smellið á flýtiflipa „Upplýsingar um línur“. Síðan skal færa inn upplýsingar um eignina á flipann Eignir. 

Til að bóka kaupfærslu fyrir fyrirliggjandi eign skal tilgreina eignanúmer, bók og færslutegund. Eign er hægt að bóka ef einhvern af þessum upplýsingum vantar. Til að bóka kaupfærslu fyrir nýja eign skal velja valkostinn ný eign? og síðan velja eignaflokk til að úthluta nýrri eign á. Hins vegar eru engin af eignasvæðunum fyrir hendi fyrir línu ef varan er í birgðalíkanaflokki sem notar birgðalíkan staðalkostnaðar. Þar að auki, valkostir sem eru skilgreindar í    síðunni færibreytur eignar ákvarða hvort hægt er að bóka kaupfærslur frá innkaupaeiningum. 

Þegar færslubók innkaupapöntunar eða færslubók birgða til eigna eru notaðar fyrir eignakaup hefur það áhrif á birgðavirðið.

## <a name="general-ledger"></a>Fjárhagur
Allar gerðir eignafærsla má bóka í  síðunni almenn færslubók. Einnig er hægt að nota færslubækur í eignum til að bóka eignafærslur.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Valkostir innfærslu á eignafærslugerðum


| Færslugerð                    | Kerfi                   | Valréttarsamningar                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Yfirtaka, leiðrétting kaupa | Eignir             | Eignir, birgðir til eigna   |
|                                     | Fjárhagur           | Almenn færslubók                           |
|                                     | Viðskiptaskuldir         | Reikningabók, Staðfestingarbók reiknings |
|                                     | Innkaup og aðföng | Innkaupapöntun                            |
| Afskrift                        | Eignir             | Eignir                              |
|                                     | Fjárhagur           | Almenn færslubók                           |
| Losun                            | Eignir             | Eignir                              |
| ** **                               | Fjárhagur           | Almenn færslubók                           |
| ** **                               | Viðskiptakröfur      | Textareikningur                         |



Frekari upplýsingar eru í [Samþætting eigna](fixed-asset-integration.md).




