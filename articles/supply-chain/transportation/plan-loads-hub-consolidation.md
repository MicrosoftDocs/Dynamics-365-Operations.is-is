---
title: Yfirlit yfir áætlun farms með samstæðustöð
description: Greinin lýsir eiginleikanum að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d61527113746e76889d097e963f70ced24fd241
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016425"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Yfirlit yfir áætlun farms með samstæðustöð

[!include [banner](../includes/banner.md)]

Greinin lýsir eiginleikanum að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.

Það getur verið gagnlegt að sameina sendingar í stöðvar sem eru sendar úr mismunandi vöruhúsum til sama viðskiptavinar, eða þegar vörur eru sendar frá mörgum lánardrottnum til sama vöruhúss.

## <a name="building-loads"></a>Mynda hleðslur
Áður en hægt er að nota samstæðustöð þarf að virkja **áætlanagerð í flutningi** valkostinn á **færibreytur Flutningsstjórnunar** síðuna. Einnig verður að stofna stöðvum þar sem sameiningu munu eiga sér stað. Eftirfarandi skýringarmynd sýnir dæmi um samstæðustöð. Í þessu tilfelli sölupantanir úr mismunandi vöruhúsum fara til sama viðskiptavin. Grunnur hleðslur eru stofnaðar á grundvelli sölupantanir á hefðbundinn hátt með því að nota **vinnusvæði hleðsluáætlunar** síðu. Til að sameina tvær hleðslurnar í stöð áður en þær eru sendar til viðskiptavinarins, á **vinnusvæði Hleðsluáætlunar** síðunni, í **Flutningur** svæðinu, veljið **samstæðustöð**. Þegar velur rétt stöðvar fyrir hvern farm, farm hafa stöðvar sem ákvörðunarstað "afhenda". Einnig mun veitast tvö "flutningsbeiðnilínur" í **Framboð og Eftirspurn** hlutanum á **Vinnusvæði Hleðsluáætlunar** síðu. Hægt að bæta þessum tveimur línum í nýja hleðslu. Þessi nýja hleðslu hafa bæði sölupöntunarlínur og mun einnig hafa stöðvar sem aðsetur "sækja" og viðskiptavinur A sem ákvörðunarstað "afhenda". Hleðslurnar þrjár er hægt að gefa verð og beint eins og önnur hleðslu. Hægt er að velja hvaða farmflytjanda sem kerfið leggur fyrir hvern farm. [![Samstæðustöð](./media/hubconsol.jpg)](./media/hubconsol.jpg) Einnig er hægt að nota sömu aðferð til að sameina hleðslur fyrir margar pantanir. Í þessu tilfelli viðskiptavina A í síðustu skýringarmynd er vöruhús. Einnig er hægt að sameina hleðslur fyrir margar innkaupapantanir, þar sem farmarnir eru sendar frá mismunandi lánardrottnum í sama vöruhúss. Hægt er að hafa fleiri en einni samsetningu stöðvar og sameina í mörgum stöðvum fyrir fleiri farm sem koma úr mismunandi vöruhúsum. Eftir að byggja á grundvallar hleðsluna og nota valkosturinn stöðvar sameiningu þú byggja nýja farma með því að nota sameinaðar flutningsbeiðnilínur. Þá gefur þú hleðslu verð og leið.



