---
title: Skilgreina og viðhalda Smásölurásir
description: Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem verslanir í Dynamics 365 Commerce. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp verslun.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413076"
---
# <a name="define-and-maintain-retail-channels"></a>Skilgreina og vinna með smásölurásir

[!include [banner](includes/banner.md)]

Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem verslanir í Dynamics 365 Commerce. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp verslun.

Commerce styður fjölda smásölurása, þ.m.t. netverslanir og markaðstorg á netinu og verslanir á staðnum. Verslun á staðnum er kölluð verslun. Hver verslun getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk. Setja verður upp allar þessar einingar fyrir verslun áður en hún er stofnuð. Eftir að þú stofnar verslun, úthluta þér afurðir sem þú vilt að verslunin selji. Einnig er starfsmönnum, afgreiðslukössum og viðskiptavinum úthlutað til verslunar. Að lokum bætirðu nýju versluninni við stigveldi fyrirtækis.

## <a name="setting-up-stores"></a>Setja upp verslanir

Áður en þú getur sett upp verslun í Commerce verður þú að ljúka nokkrum frumskilyrðisverkefnum. Hægt er að stofna verslunar og bæta við upplýsingar.

### <a name="prerequisites"></a>Forkröfur

Áður en hægt er að setja upp verslun, verður að ljúka við eftirfarandi verk:

1. Skilgreina skipulag fyrirtækis þíns og setja upp stigveldi fyrirtækis fyrir smásöluúrval, áfyllingar og skýrslugerð.
2. Setja upp vöruhús til að tákna verslun.
3. Setja upp númeraraðir fyrir verslanir, verslunaruppgjör og uppgjör fylgiskjöl.
4. Skilgreina færibreytur fyrir Commerce.
5. Setja upp greiðsluhátt sem verslunin tekur á móti.
6. Til að vinna úr kreditkortafærslum á sölustað (POS) kassa, er einnig hægt að setja upp greiðsluþjónustu.
7. Setja upp VSK-flokka.
8. Setja upp afurðir. Sem hluti af þessu verki, er einnig sett upp stigveldi afurðar, afurðarafbrigði og úrvali afurða.
9. Setja upp verðflokka afurðar.
10. Setja upp afurðaverðlagningu. Sem hluti af þessu verki, er einnig sett upp verðleiðrétting, afslættir og afsláttartímabil.
11. Setja upp starfsfólk

    > [!NOTE]
    > Einnig verður að úthluta viðeigandi heimildum fyrir starfsmenn, þannig að þeir geti skráð sig inn og framkvæmt verkefni með því að nota kerfið POS.

12. Skilgreina skal sölustaðaforstillingar til að úthluta á verslun. Þetta felur í sér mörg verk, s.s. uppsetningu afgreiðslukassa, uppsetningu ótengt snið, og uppsetning snið kvittunar og forstillingar.

Fara yfir öll verk í sem eru innifalin í þessum frumskilyrðum, og ljúka aðeins þeim verkum sem eiga við þig.

### <a name="set-up-a-store"></a>Setja upp verslun

Eftir að þú hefur lokið við frumskilyrðisverk skaltu ljúka þessum verkefnum til að setja upp upplýsingar fyrir verslun:

1. Búa til verslun.
2. Úthluta VSK-flokki á verslunina.
3. Úthluta viðurkenndum greiðsluaðferðum á verslun.
4. Bæta upplýsingum við afurðalýsingar fyrir afurðir sem á að bjóða í verslununum. Til dæmis er hægt að bæta rtf-texta og myndum. Þessar upplýsingar um afurð birst í mismunandi samhengi. eins og á afgreiðslukassa Sölustaðar eða prentaðir merkimiðar.
5. Bæta versluninni við sjálfgefið stigveldi fyrirtækis sem er úthlutað á málefni fyrir **vöruúrval smásölu**, **smásöluáfyllingu** eða **skýrslugerð í smásölu**.

### <a name="after-you-set-up-a-store"></a>Eftir að þú setur upp verslun

Eftir að þú slærð inn upplýsingar fyrir verslun þarf að ljúka þessum verkum til að senda ný gögn verslunarinnar til POS.

1. Skilgreina afgreiðslukassa sölustaðar fyrir verslunina.
2. Úthluta vöruúrvali á verslunina.
3. Vinna úr úrvali til að mynda lista yfir afurðir sem eru teknar með í úrvalið og til að nálgast afurðir í verslunar.
4. Senda gögn eins og númeraraðir, vélbúnaðarreglur, útlit afgreiðsluskjás sölustaðar til afgreiðslukassi.
5. Birta verslun til að senda gögn verslunar til sölustaðar.
6. Keyra vinnslur til að senda gögn verslunar til sölustaðar.

## <a name="organization-hierarchies"></a>Stigveldi fyrirtækis

Commerce notar stigveldi stofnunar fyrir uppbyggingu á rásum. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri. Þegar að settar eru upp verslanir er hægt að bæta þeim við stigveldi fyrirtækis. Verslanir deila sem notaður er fyrir úrval áfyllingar og skýrslugerð.

> [!NOTE]
> Til að nota söluaðgerðir Commerce verður stillingarlykilinn fyrir **Sent mörgum** að vera virkur. Þennan stillingarlykil er að finna í lyklunum **Stillingu viðskipta** undir **Kerfisstjórnun**\> **Uppsetning** \> **Stilling leyfis**. Þetta er nauðsynlegt vegna ýmissa sannprófana á grundvelli afhendingarfangs sem er stillt á sölupöntunarlínustig.

