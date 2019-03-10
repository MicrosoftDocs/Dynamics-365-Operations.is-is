---
title: Samræmisprófun smásölufærslna
description: Þetta efnisatriði lýsir virkni samræmisprófunar smásölufærslna í Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "302439"
---
# <a name="retail-transaction-consistency-checker"></a>Samræmisprófun smásölufærslna


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Þetta efnisatriði lýsir virkni samræmisprófunar smásölufærslna sem kynnt var til sögunnar í Microsoft Dynamics 365 for Finance and Operations útgáfu 8.1.3. Í samræmisprófuninni eru færslur með ósamræmi greindar og einangraðar áður en þær eru teknar inn í bókunarferlið.

Þegar uppgjör er bókað í Retail getur birtingin mistekist vegna ósamstæðra gagna í færslutöflum. Gagnavillan getur orðið vegna ófyrirséðra vandamála í forritinu á sölustað (POS) eða vegna villu í flutningi færslna úr sölustaðarkerfi þriðju aðila. Dæmi um þessi ósamræmi eru meðal annars: 

  - Heildarfærsla í haustöflu er ekki í samræmi við heildarfærslu í línunum.
  - Línufjöldi í haustöflu er ekki í samræmi við fjölda lína í færslutöflunni.
  - Skattar í haustöflu eru ekki í samræmi við skattupphæð í línunum. 
  
Þegar færslur með ósamræmi eru teknar inn í bókunarferlið verða til sölureikningar og greiðslubækur með ósamræmi og villa kemur upp í öllu bókunarferlinu. Í því tilfelli þarf flóknar gagnaleiðréttingar í mörgum færslutöflum til að endurheimta færslurnar. Samræmisprófun smásölufærslna kemur í veg fyrir slík vandamál.

Eftirfarandi tafla sýnir bókunarferli með samræmisprófun smásölufærslna.

![Bókunarferli uppgjörs með samræmisprófun smásölufærslna](./media/validchecker.png "Bókunarferli uppgjörs með samræmisprófun smásölufærslna")

Með runuvinnslunni **Villuleita í færslum verslunar** er samræmi smásölufærslutaflna athugað við eftirfarandi aðstæður.

- Viðskiptavinalykill - Staðfestir að viðskiptavinalykillinn í smásölufærslutöflunum sé til staðar í HQ-aðalgögnum viðskiptavinar.
- Línufjöldi - Staðfestir að línufjöldi, samkvæmt haustöflu færslna, sé í samræmi við fjölda lína í sölufærslutöflunum.

## <a name="set-up-the-consistency-checker"></a>Setja upp samræmisprófun
Skilgreina skal runuvinnsluna „Villuleita í færslum verslunar“ í **Smásölu \> Upplýsingatækni smásölu \> Sölustaðarbókun** til að keyra vinnsluna reglulega. Hægt er að skipuleggja runuvinnsluna á grundvelli stigveldis verslunarinnar, svipað því hvernig ferlin „Reikna uppgjör í runu“ og „Bóka uppgjör í runu“ eru sett upp. Við mælum með að þú stillir runuvinnsluna þannig að hún sé keyrð oft á dag og að loknu hverju P-verki.

## <a name="results-of-validation-process"></a>Niðurstöður villuleitar
Niðurstöðum villuleitar er bætt við viðkomandi smásölufærslu. Svæðið **Staða villuleitar** í viðkomandi uppgjörsfærslu er ýmist stillt á **Lokið** eða **Villa** og dagsetning síðustu villuleitar birtist á svæðinu **Tími síðustu villuleitar**.

Til að sjá nákvæmari villuboðatexta sem tengist villu í villuleit skal velja viðkomandi færsluskrá smásöluverslunar og smella á hnappinn **Villur við villuleit**.

Færslur sem standast ekki villuleit og færslur sem enn á eftir að villuleita í eru ekki teknar inn í uppgjör. Í ferlinu „Reikna uppgjör“ fá notendur tilkynningu um færslur sem eru ekki með í uppgjörinu en hefðu getað verið það.

Ef villa finnst við villuleit er einungis hægt að lagfæra hana með því að hafa samband við notendaþjónustu Microsoft. Í síðari útgáfu munu notendur geta lagfært skrár með villum í notendaviðmótinu. Einnig bætast við endurskoðunar- og skráningareiginleikar til að rekja breytingarsöguna.

> [!NOTE]
> Frekari villuleitarreglum til að styðja við fleiri aðstæður verður bætt við í síðari útgáfu.