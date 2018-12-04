---
title: "Bóka eignafærslur í bókunalög"
description: "Þessi grein gefur yfirlit yfir virkni bókunarlags fyrir eignafærslur."
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b210bddf640dff2d65e2aec63a18c27acebdc5a8
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a>Bóka eignafærslur í bókunalög

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir virkni bókunarlags fyrir eignafærslur.

Eign er oft afskrifuð á mismunandi hátt í mismunandi tilgangi. Afskriftir fyrir skatta eru reiknaðar út eftir gildandi skattareglum til að ná sem mestum afskriftum fyrir skatta, en afskriftir fyrir skýrslugerð er reiknaðar eftir bókhaldslögum og stöðlum. Útreikningum og skráningum mismunandi afskrifta er haldið aðskildum í bókunarlögunum.

Hvert bók sem er tengt eign er uppsett fyrir ákveðið bókunarlag sem hefur heildarafskriftarviðfang. Bókunarlögin eru Tíu: Gildandi, Aðgerðir, Skatt og sjö Sérsniðna lögum. Hægt er að gera bókun í fjárhag fyrir bók óvirka með því að stilla reitinn Bóka í fjárhag á nei. Á Bókunarlag reit er þá sjálfvirkt stillt á Ekkert. Yfirleitt eru bækur sem bóka ekki í fjárhag notaðar fyrir skattskýrslugerð. Þessi nálgun gefur viðbótar sveigjanleika til að eyða sögulegum færslum fyrir eignabók þar sem þær hafa ekki verið bundnar í fjárhag.

Eignabækur eru skilgreindir með því að nota í  færslubókarheiti síðuna á fjárhags > færslubókaruppsetningu > færslubókarheiti. Hver færslubók, sem hægt er að bóka afskriftir í, er skilgreind með færslubókarheiti sínu fyrir einungis eitt bókunarlag. Ekki er hægt að breyta bókunarlaginu í færslubók. Takmarkanir tryggir að færslum í hverju bókunarlagi er haldið aðskildum. Það verður að stofna að minnsta kosti eitt færslubókarheiti fyrir hvert bókunarlag. Ef verið er að nota bækur sem ekki bóka í fjárhag, verður einnig að stofna færslubók þar sem bókunarlag stillt á Engin.

Hægt er að tilnefna fjárhagsreikninga sem færslur eigna eru bókaðar í á síðunni Bókunarreglur eigna. Fyrir hverja bókunarreglu verður að velja viðeigandi færslugerð og bóka, og svo þarf að tilnefna fjárhagslyklana. Setja upp færslu bókunarreglu fyrir hverja bók sem er bókuð í fjárhag.

> [!NOTE] 
> Með því að nota afleidd bækur er mögulegt að bóka færslur á mismunandi bókunarlög á sama tíma. Færslur aðalbókar eru stofnaðar í færslubók með bókunarlagi sem samsvarar bókunarlagi bókar. Á meðan á bókun stendur, eru færslur afleidda bóka bókaðar á þau bókunarlög sem tilheyra þeim.

Nánari upplýsingar eru í [Afleiddar bækur](derived-books.md) og [Bókað í afleiddar bækur](post-derived-value-models.md).




