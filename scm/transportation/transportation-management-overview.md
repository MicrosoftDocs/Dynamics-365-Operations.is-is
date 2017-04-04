---
title: "Yfirlit yfir flutningsstjórnun"
description: "Í þessu Umfjöllunarefni er að finna yfirlit yfir Flutningar Stjórnun virkni í Microsoft Dynamics 365 for Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Yfirlit yfir flutningsstjórnun

Í þessu Umfjöllunarefni er að finna yfirlit yfir Flutningar Stjórnun virkni í Microsoft Dynamics 365 for Operations.

Flutningsstjórnun leyfir þér að nota og stjórna flutningum innan fyrirtækis þíns, og þekkja lausnir lánardrottna og leiðir fyrir pantanir á inn og útleið. Til dæmis er hægt að auðkenna hraðast leið eða ódýrast taxta fyrir sendingu. Eftirfarandi tafla lýsir helstu aðstæðum þar sem hægt er að nota flutningsstjórnun í Microsoft Dynamics 365 for Operations.

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
<td>Bílafloti fyrirtækisins er tiltækur til að afhenda/sækja og afhendingargjöld eru sett á viðskiptavini.</td>
<td>Fyrir ferli á útleið er hægt að nota Flutningsstjórnun til að ákvarða flutningsgjöld og senda þau á viðskiptavini. Hins vegar er ferli afstemmingar reikninga flutningsaðila ekki áskilið.</td>
</tr>
<tr class="odd">
<td>Bílafloti fyrirtækisins er tiltækur til að afhenda/sækja en afhendingargjöld eru ekki sett á viðskiptavini af því að flutningur er innifalinn í verði vöru.</td>
<td>Margar aðgerðir í Flutningsstjórnun eru ekki nauðsynlegar. Hins vegar er hægt að nota flutningsstjórnun til að ákvarða flutningstaxta og leiðrétta söluverðið til samræmis við það.</td>
</tr>
<tr class="even">
<td>Þjónusta tengd vöruferilsstjórnun er veitt af öðrum lögaðila í sama fyrirtæki.</td>
<td><ul>
<li>Nota má flutningsstjórnun með því að meðhöndla hinn lögaðilann sem hvern annan farmflytjanda. Ekki er hægt að gera sjálfvirkar efnahagslegar færslur á milli lögaðila. Þess vegna þarf að gera þessar færslur handvirkt (til dæmis með því að stofna innkaupapöntun).</li>
<li>Lögaðila sem veitir þjónustu vörustjórnun, flutningsstjórnun má nota til að ákvarða flutningsstjórnunar taxta.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Skipulagning Flutningur í Dynamics 365 for Operations
Í flutningsstjórnun, er hægt að byggja flutningsáætlun annað hvort á pöntunum eða á sendingunum sem eru stofnaðar samkvæmt þeim pöntunum. Sendingar eru alltaf til á einhverjum tímapunkti en þeirra er ekki þörf í flutningsáætlunum. Flutningspantanir eru hluti af aðstæðum á útleið og hægt er að áætla þær með sölupöntunum. 

![Hlaða teikningu](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Flutningur á innleið
Þegar vörur eru pantaðar frá lánardrottni og verður að vera afhent vörurnar í vöruhúsinu, mætti raða flutning varanna. Hægt er að nota Dynamics 365 aðgerða til að áætla flutning og móttöku hleðslu á innleið. Eftirfarandi skýringarmynd sýnir flæði viðskiptaferlis fyrir flutning á innleið farms fyrir áætlun. 

![Flæði viðskiptaferlis fyrir flutning farms á innleið](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Flutningur á útleið
Hægt er að áætla og vinna farm á útleið til að senda tilteknar vörur úr vöruhúsi fyrirtækis til viðskiptavinar. Hægt er að nota Dynamics 365 for Operations til að áætla flutning og sendingu hleðslu á útleið. Eftirfarandi skýringarmynd sýnir flæði viðskiptaferlis fyrir áætlanagerð og vinnslu á útleið farma fyrir sendingu. 

![Hleður áætlanagerð og vinnslu á útleið](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Hleðsluáætlun
Dynamics 365 for Operations býður upp á hleðsluáætlun sem nefnist hleðsluáætlun byggð á rúmmáli. Þessi aðferð gerir kleift að nota hámarks gildi sem eru tilgreind fyrir hæð og þyngd í hleðslusniðmátinu eða hnekkja stillingum með því að færa inn ný gildi. Til að nota þessa aðferð skal velja hana í reitnum **Hleðsluáætlun** á flýtiflipanum **Uppsetning** í skjámyndinni **Hlaða sniðmáti hleðslu**. Þar að auki, er hægt að bæta við eigin hleðsluáætlun með því að stofna nýjan klasa í Hugbúnaðarhlutatrénu (AOT).


