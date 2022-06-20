---
title: Yfirlit flutningsstjórnunar
description: Þessi grein gefur yfirlit yfir virkni flutningsstjórnunar í Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "30251"
- intro-internal
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12f870c95f28e752c3c3b3dd4161d82815b9954a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897459"
---
# <a name="transportation-management-overview"></a>Yfirlit flutningsstjórnunar

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir virkni flutningsstjórnunar í Supply Chain Management.

Flutningsstjórnun leyfir þér að nota flutninga innan fyrirtækis þíns, og þekkja lausnir lánardrottna og leiðir fyrir pantanir á inn og útleið. Til dæmis er hægt að auðkenna hraðast leið eða ódýrast taxta fyrir sendingu. Eftirfarandi tafla lýsir helstu aðstæðum þar sem hægt er að nota flutningsstjórnun.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Aðstæður</th>
<th>Hvernig Flutningsstjórnun getur orðið að liði</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nota ytri vöruferilsstjórnun fyrir flutningsþætti.</td>
<td>Nota flutningsstjórnun fyrir flutning á innleið og/eða útleið.</td>
</tr>
<tr class="even">
<td>Bílafloti fyrirtækisins &#39; er tiltækur til að afhenda/sækja og afhendingargjöld eru sett á viðskiptavini.</td>
<td>Fyrir ferli á útleið er hægt að nota Flutningsstjórnun til að ákvarða flutningsgjöld og senda þau á viðskiptavini. Hins vegar er ferli afstemmingar reikninga flutningsaðila ekki áskilið.&#39;</td>
</tr>
<tr class="odd">
<td>Bílafloti fyrirtækisins er tiltækur til að afhenda/sækja en afhendingargjöld eru ekki sett á viðskiptavini af því að flutningur er innifalinn í verði vöru.&#39;&#39;</td>
<td>Margar aðgerðir í Flutningsstjórnun eru ekki nauðsynlegar.&#39; Hins vegar er hægt að nota flutningsstjórnun til að ákvarða flutningstaxta og leiðrétta söluverðið til samræmis við það.</td>
</tr>
<tr class="even">
<td>Þjónusta tengd vöruferilsstjórnun er veitt af öðrum lögaðila í sama fyrirtæki.</td>
<td><ul>
<li>Nota má flutningsstjórnun með því að meðhöndla hinn lögaðilann sem hvern annan farmflytjanda. Ekki er hægt að gera sjálfvirkar efnahagslegar færslur á milli lögaðila.&#39; Þess vegna þarf að gera þessar færslur handvirkt (til dæmis með því að stofna innkaupapöntun).</li>
<li>Lögaðila sem veitir þjónustu vörustjórnun, flutningsstjórnun má nota til að ákvarða flutningsstjórnunar taxta.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>Skipulagning á flutningi í Supply Chain Management
Í flutningsstjórnun, er hægt að byggja flutningsáætlun annað hvort á pöntunum eða á sendingunum sem eru stofnaðar samkvæmt þeim pöntunum. Sendingar eru alltaf til á einhverjum tímapunkti en þeirra er ekki þörf í flutningsáætlunum. Flutningspantanir eru hluti af aðstæðum á útleið og hægt er að áætla þær með sölupöntunum. 

![Sækja teikningu.](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Flutningur á innleið
Þegar vörur eru pantaðar frá lánardrottni og afhenda verður vörurnar til vöruhúsins, kann notandi að vilja raða flutningi varanna sjálfur. Hægt er að nota Supply Chain Management til að áætla flutning og móttöku hleðslu á innleið. Eftirfarandi skýringarmynd sýnir flæði viðskiptaferlis fyrir flutning á innleið farms fyrir áætlun. 

![Flæði viðskiptaferlis fyrir flutning farms á innleið.](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Flutningur á útleið
Hægt er að áætla og vinna farm á útleið til að senda tilteknar vörur úr vöruhúsi fyrirtækis til viðskiptavinar. Hægt er að nota Supply Chain Management til að áætla flutning og sendingu á farmi á útleið. Eftirfarandi skýringarmynd sýnir flæði viðskiptaferlis fyrir áætlanagerð og vinnslu á útleið farma fyrir sendingu. 

![Áætlun og vinnsla hleðslu á útleið.](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Hleðsluáætlun
Supply Chain Management býður upp á hleðsluáætlun sem nefnist hleðsluáætlun byggð á rúmmáli. Þessi aðferð gerir kleift að nota hámarks gildi sem eru tilgreind fyrir hæð og þyngd í hleðslusniðmátinu eða hnekkja stillingum með því að færa inn ný gildi. Til að nota þessa aðferð skal velja hana í reitnum **Hleðsluáætlun** á flýtiflipanum **Uppsetning** í skjámyndinni **Hlaða sniðmáti hleðslu**. Þar að auki, er hægt að bæta við eigin hleðsluáætlun með því að stofna nýjan klasa í Hugbúnaðarhlutatrénu (AOT).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]