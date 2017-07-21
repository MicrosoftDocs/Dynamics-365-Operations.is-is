---
title: "Skilgreina og viðhalda Smásölurásir"
description: "Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem smásöluverslanir í Microsoft Dynamics 365 for Retail. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp smásöluverslun."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 3f0b566963574569cb40b72550e2337c9ba8a2ce
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="define-and-maintain-retail-channels"></a>Skilgreina og viðhalda Smásölurásir

[!include[banner](includes/banner.md)]


Þessi skrá veitir yfirlit yfir ferlið fyrir uppsetningu hefðbundinna verslana sem vísað er til sem smásöluverslanir í Microsoft Dynamics 365 for Retail. Það felur í sér upplýsingar um þau verk sem ljúka verður bæði áður en eða eftir að þú hefur lokið við að setja upp smásöluverslun.

Dynamics 365 for Retail styður fjölda smásölurása, þ.m.t. netverslanir, þjónustuver og verslanir á staðnum. Verslun á staðnum er kölluð smásöluverslun. Hvert smásöluverslun getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk. Setja verður upp allar þessar einingar fyrir smásöluverslun áður en hún er stofnuð. Eftir að þú stofnar smásöluverslun, úthluta þér afurðir sem þú vilt að verslunin selji. Einnig er starfsmönnum, afgreiðslukössum og viðskiptavinum úthlutað til verslunar. Að lokum bætirðu nýju versluninni við stigveldi fyrirtækis.

## <a name="setting-up-retail-stores"></a>Setja upp smásöluverslanir
Áður en hægt er að setja upp smásöluverslun í Dynamics 365 for Retail verður þú að ljúka nokkrum frumskilyrðisverkefni. Hægt er að stofna smásöluverslunar og bæta við upplýsingar.

### <a name="prerequisites"></a>Skilyrði

Áður en hægt er að setja upp smásöluverslun, verður að ljúka við eftirfarandi verk:

1.  Skilgreina skipulag fyrirtækis þíns og setja upp stigveldi fyrirtækis fyrir smásöluúrval, áfyllingar og skýrslugerð.
2.  Setja upp vöruhús til að tákna smásöluverslun.
3.  Setja upp númeraraðir fyrir smásöluverslanir, verslunaruppgjör og uppgjör fylgiskjöl.
4.  Skilgreina færibreytur fyrir smásölu.
5.  Setja upp greiðsluhátt sem verslunin tekur á móti.
6.  Til að vinna úr kreditkortafærslum á sölustað (POS) smásölukassa, er einnig hægt að setja upp greiðsluþjónustu.
7.  Setja upp VSK-flokka.
8.  Setja upp smásöluafurðir. Sem hluti af þessu verki, er einnig sett upp stigveldi smásöluafurðar, afurðarafbrigði og úrvali afurða.
9.  Setja upp verðflokka afurðar.
10. Setja upp verðlagningu smásöluafurða. Sem hluti af þessu verki, er einnig sett upp verðleiðrétting, afslættir og afsláttartímabil.
11. Setja upp starfsfólk **Ábending:** einnig verður að úthluta viðeigandi heimildir fyrir starfsmenn, þannig að þeir geti skráð sig inn og framkvæma verkefni með því að nota Dynamics 365 for Retail fyrir Retail POS.
12. Skilgreina skal Retail POS forstillingar til að tengja við verslun. Þetta felur í sér mörg verk, s.s. uppsetningu afgreiðslukassa, uppsetningu ótengt snið, og uppsetning snið kvittunar og forstillingar.

Fara yfir öll verk í sem eru innifalin í þessum frumskilyrðum, og ljúka aðeins þeim verkum sem eiga við þig.

### <a name="set-up-a-retail-store"></a>Setja upp smásöluverslun

Eftir að þú hefur lokið við frumskilyrðisverk skaltu ljúka þessum verkefnum til að setja upp upplýsingar fyrir smásöluverslun:

1.  Stofna smásöluverslun.
2.  Úthluta VSK-flokki á verslunina.
3.  Úthluta viðurkenndum greiðsluaðferðum á verslun.
4.  Bæta upplýsingum við afurðalýsingar fyrir afurðir sem á að bjóða í verslununum smásölu. Til dæmis er hægt að bæta rtf-texta og myndum. Þessar upplýsingar um afurð birst í mismunandi samhengi. eins og á afgreiðslukassa Sölustaðar eða prentaðir merkimiðar.
5.  Bæta versluninni við sjálfgefið stigveldi fyrirtækis sem er úthlutað á málefni fyrir **vöruúrval smásölu**, **smásöluáfyllingu** eða **skýrslugerð í smásölu**.

### <a name="after-you-set-up-a-retail-store"></a>Eftir að þú setur upp smásöluverslun

Eftir að þú slærð inn upplýsingar fyrir smásöluverslun þarf að ljúka þessum verkum til að senda ný gögn smásöluverslunarinnar til Retail POS:

1.  Skilgreina afgreiðslukassa sölustaðar fyrir verslunina.
2.  Úthluta vöruúrvali á verslunina.
3.  Vinna úr úrvali til að mynda lista yfir afurðir sem eru teknar með í úrvalið og til að nálgast afurðir í smásöluverslunar.
4.  Senda gögn eins og númeraraðir, vélbúnaðarreglur, útlit afgreiðsluskjás sölustaðar til afgreiðslukassi.
5.  Birta smásöluverslun til að senda gögn Retail POS.
6.  Keyra vinnslur til að senda gögn verslunar til  Retail POS.

## <a name="organization-hierarchies"></a>Stigveldi fyrirtækis
Retail notar stigveldi stofnunar fyrir uppbyggingu smásölurás. Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem þú ert með saman í rekstri. Þegar að settar eru upp verslanir er hægt að bæta þeim við stigveldi fyrirtækis. Verslanir deila sem notaður er fyrir úrval áfyllingar og skýrslugerð.




