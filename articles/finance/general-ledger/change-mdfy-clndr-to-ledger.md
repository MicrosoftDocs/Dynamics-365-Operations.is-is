---
title: Breyta eða endurúthluta fjárhagsdagatali
description: Þetta efnisatriði útskýrir hvernig á að breyta dagatalinu sem nú er úthlutað í fjárhag og hvernig á að úthluta nýju dagatali í fjárhag.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16000243bc8aa76b04ac56dfb8bfbab7cd644eb3120cc68493ff066598f6cf85
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758078"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Breyta eða endurúthluta fjárhagsdagatali

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að breyta dagatalinu sem nú er úthlutað í fjárhag og hvernig á að úthluta nýju dagatali í fjárhag.

## <a name="issue"></a>Gefa út

Stundum verða fyrirtæki annaðhvort að breyta núverandi dagatali sem er úthlutað í fjárhag eða úthluta nýju dagatali.

## <a name="resolution"></a>Lausn

Tvær aðstæður eru til staðar þar sem nauðsynlegt gæti verið að breyta eða endurúthluta fjárhagsdagatali. Fyrri felur í sér að breyta fyrirliggjandi dagatali sem þegar hefur verið úthlutað í fjárhag. Annað felur í sér að búa til nýtt dagatal og úthluta því í fjárhag. Hægt er að gera báðar breytingarnar hvenær sem er, jafnvel eftir að færslur hafa verið bókaðar í fjárhag.

### <a name="change-an-existing-fiscal-calendar"></a>Breyta fyrirliggjandi fjárhagsdagatali

Til að breyta fyrirliggjandi dagatali sem er úthlutað í fjárhag skaltu fara í **Fjárhagur \> Uppsetning fjárhags \> Fjárhagur** og velja tengilinn fyrir fjárhagsdagatalið til að opna síðuna **Fjárhagsdagatöl**.

Takmarkanir eru á því hverju er hægt að breyta í dagatali. Það er til dæmis hægt að breyta upphafs- og lokadegi *tímabilanna* á ári en ekki upphafs- og lokadegi *árs* í dagatalinu.

Til að breyta tímabilum árs skal velja viðeigandi dagatal og ár. Fyrst skaltu nota hnappinn **Eyða tímabili** til að eyða sumum eða öllum núverandi rekstrartímabilum. Hægt er að eyða öllum rekstrartímabilum nema því fyrsta. Notaðu síðan hnappinn **Skipta tímabili** til að skipta eftirstöðvum tímabila í ný tímabil með því að slá inn viðeigandi upphafsdag fyrir næsta tímabil.

Þegar þú breytir tímabilunum í dagatali verður þú að keyra ferlið **Endurreikna fjárhagstímabil** í öllum lögaðilum (fyrirtækjum) þar sem dagatalinu er úthlutað. Þrátt fyrir að engin viðvörunarskilaboð minni þig á að ljúka þessu skrefi er endurútreikningsferlið nauðsynlegt til að uppfæra tímabilið sem er úthlutað fyrir hverja færslu sem er bókuð í Fjárhag. Til að keyra endurútreikningsferlið velur þú **Endurreikna fjárhagstímabil** á síðunni **Fjárhagsuppsetning** í hverju fyrirtæki fyrir sig.

Ef endurútreikningsferlið er ekki keyrt gætu færslustöður í prófjöfnuði eða fjárhagsskýrslum verið ranglega hafðar með í tímabilum. Í þessu tilfelli er hægt að leiðrétta stöðurnar hvenær sem er með því að keyra endurútreikningsferlið.

### <a name="assign-a-new-fiscal-calendar"></a>Úthluta nýju fjárhagsdagatali

Til að úthluta nýju fjárhagsdagatali skal opna **Fjárhagur \> Fjárhagsuppsetning \> Fjárhagur** og velja **Breyta** til að færa síðu **Fjárhags** yfir í breytingastillingu. Því næst skal velja nýtt fjárhagsdagatal í reitnum **Fjárhagsdagatal**.

Þegar þú breytir fjárhagsdagatalinu fyrir fjárhag þarftu að keyra **Endurreikna fjárhagstímabil**. Þegar þú úthlutar nýju fjárhagsdagatali í bókhald birtast skilaboð sem minna þig á að ljúka þessu skrefi. Þó að skilaboðin virðist benda til þess að endurútreikningsferlið sé valfrjálst er það ekki svo. Það þarf að uppfæra tímabilið sem er úthlutað fyrir hverja færslu sem er bókuð í Fjárhag. Til að keyra endurútreikningsferlið velur þú **Endurreikna fjárhagstímabil** á síðunni **Fjárhagsuppsetning**.

Ef endurútreikningsferlið er ekki keyrt gætu færslustöður í prófjöfnuði eða fjárhagsskýrslum verið ranglega hafðar með í tímabilum. Í þessu tilfelli er hægt að leiðrétta stöðurnar hvenær sem er með því að keyra endurútreikningsferlið.
