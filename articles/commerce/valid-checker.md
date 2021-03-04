---
title: Samræmisprófun smásölufærslna
description: Þetta efnisatriði lýsir virkni samræmisprófunar færslna í Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/07/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 869230c0003735c1e9f48170a16ca9409a9edc19
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976540"
---
# <a name="retail-transaction-consistency-checker"></a>Samræmisprófun smásölufærslna

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir virkni samræmisprófunar færslna í Microsoft Dynamics 365 Commerce. Í samræmisprófuninni eru færslur með ósamræmi greindar og einangraðar áður en þær eru teknar inn í bókunarferlið.

Þegar uppgjör er bókað getur bókun mistekist vegna ósamræmis í gögnum í færslutöflum viðskiptanna. Gagnavillan getur orðið vegna ófyrirséðra vandamála í forritinu á sölustað (POS) eða vegna villu í flutningi á færslum úr sölustaðarkerfi þriðja aðila. Dæmi um þessi ósamræmi eru meðal annars: 

- Heildarfærsla í haustöflu er ekki í samræmi við heildarfærslu í línunum.
- Línufjöldi í haustöflu er ekki í samræmi við fjölda lína í færslutöflunni.
- Skattar í haustöflu eru ekki í samræmi við skattupphæð í línunum. 

Þegar færslur með ósamræmi eru teknar inn í bókunarferlið verða til sölureikningar og greiðslubækur með ósamræmi og villa kemur upp í öllu bókunarferlinu. Í því tilfelli þarf flóknar gagnaleiðréttingar í mörgum færslutöflum til að endurheimta færslurnar. Samræmisprófun færslna kemur í veg fyrir slík vandamál.

Eftirfarandi tafla sýnir bókunarferli með samræmisprófun smásölufærslna.

![Bókunarferli uppgjörs með samræmisprófun færslu](./media/validchecker.png "Bókunarferli uppgjörs með samræmisprófun smásölufærslna")

Með runuvinnslunni **Villuleita í færslum verslunar** er samræmi viðskiptafærslutaflna athugað við eftirfarandi aðstæður.

- **Viðskiptamannalykill** – Staðfestir að viðskiptamannalykillinn í færslutöflunum sé til staðar í HQ-aðalgögnum viðskiptamanns.
- **Línufjöldi** – Staðfestir að línufjöldi, samkvæmt haustöflu færslna, sé í samræmi við fjölda lína í sölufærslutöflunum.
- **Verð er með skatti** – Staðfestir að færibreytan **Verð er með skatti** er í samræmi við allar færslulínur og að verðið á sölulínunni er í samræmi við skilgreiningu Verð er með skatti og skattundanþágu.
- **Greiðsluupphæð** – Staðfestir að greiðslufærsla samsvari greiðsluupphæð í haus og tekur einnig með í reikninginn skilgreiningu aurasléttunar í fjárhagi.
- **Brúttóupphæð** – Staðfestir að brúttóupphæð í hausnum er summa nettóupphæða í línunum ásamt skattupphæðinni og tekur einnig með í reikninginn skilgreiningu aurasléttunar í fjárhagi.
- **Nettóupphæð** – Staðfestir að nettóupphæð í hausnum er summa nettóupphæða í línunum og tekur einnig með í reikninginn skilgreiningu aurasléttunar í fjárhagi.
- **Vangreiðsla/ofgreiðsla** – Staðfestir að mismunur milli brúttóupphæðar í hausnum og greiðsluupphæðar fer ekki umfram skilgreiningu á hámarki fyrir vangreiðslu/ofgreiðslu og tekur einnig með í reikninginn skilgreiningu aurasléttunar í fjárhagi.
- **Afsláttarupphæð** – Staðfestir að samræmi er á afsláttarupphæð í afsláttartöflum og afsláttarupphæð í færslulínutöflum, að afsláttarupphæð í hausnum er summa afsláttarupphæða í línunum og tekur einnig með í reikninginn skilgreiningu aurasléttunar í fjárhagi.
- **Línuafsláttur** – Staðfestir að línuafsláttur í færslulínunni er summa allra línanna í afsláttartöflunni sem eru í samræmi við færslulínuna.
- **Gjafakortsvara** – Commerce styður ekki skil á gjafakortsvörum. Hins vegar er hægt að leysa út stöðu á gjafakorti í reiðufé. Gjafakortsvara sem er meðhöndluð sem skilalína í stað línu reiðufjárúttektar kemst ekki í gegnum bókunarferli uppgjörs. Staðfestingarferlið fyrir gjafakortsvörur hjálpar til við að tryggja að skilalínur gjafakortsvara í færslutöflunum séu eingöngu línur reiðufjárúttektar fyrir gjafakort.
- **Neikvætt verð** – Staðfestir að engar færslulínur með neikvæðu verði eru til staðar.
- **Vara og afbrigði** – sannprófar að vörur og afbrigði í færslulínum eru til staðar í grunnskjali fyrir vöru og afbrigði.
- **Skattupphæð** – sannprófar að skattafærslur passi við skattupphæðir í línunum.
- **Raðnúmer** – sannprófar að raðnúmer sé til staðar í færslulínum fyrir vörur sem er stjórnað af raðnúmeri.
- **Tákn** – sannprófar að tákn fyrir magn og nettóupphæð sé hið sama í öllum færslulínum.
- **Viðskiptadagur** – Staðfestir að fjárhagstímabil fyrir alla viðskiptadaga færslnanna séu opin.
- **Gjöld** – Staðfestir að hausinn og upphæð greiðslu í línu sé í samræmi við verð, þ.m.t. skilgreiningu á skatti og skattundanþágu.

## <a name="set-up-the-consistency-checker"></a>Setja upp samræmisprófun

Skilgreina skal runuvinnsluna „Villuleita í færslum verslunar“ í **Retail og Commerce \> Upplýsingatækni Retail og Commerce \> Sölustaðarbókun** til að keyra vinnsluna reglulega. Hægt er að skipuleggja runuvinnsluna á grundvelli stigveldis fyrirtækisins, svipað því hvernig ferlin „Reikna uppgjör í runu“ og „Bóka uppgjör í runu“ eru sett upp. Við mælum með að þú stillir runuvinnsluna þannig að hún sé keyrð oft á dag og að loknu hverju P-verki.

## <a name="results-of-validation-process"></a>Niðurstöður villuleitar

Niðurstöðum villuleitar er bætt við viðkomandi færslu. Svæðið **Staða villuleitar** í viðkomandi færslu er ýmist stillt á **Lokið** eða **Villa** og dagsetning síðustu villuleitar birtist á svæðinu **Tími síðustu villuleitar**.

Til að sjá nákvæmari villuboðatexta sem tengist villu í villuleit skal velja viðkomandi færsluskrá verslunar og smella á hnappinn **Villur við villuleit**.

Færslur sem standast ekki villuleit og færslur sem enn á eftir að villuleita í eru ekki teknar inn í uppgjör. Í ferlinu „Reikna uppgjör“ fá notendur tilkynningu um færslur sem eru ekki með í uppgjörinu en hefðu getað verið það.

Ef villa finnst við villuleit er einungis hægt að lagfæra hana með því að hafa samband við notendaþjónustu Microsoft. Í síðari útgáfu munu notendur geta lagfært skrár með villum í notendaviðmótinu. Einnig bætast við endurskoðunar- og skráningareiginleikar til að rekja breytingarsöguna.

> [!NOTE]
> Frekari villuleitarreglum til að styðja við fleiri aðstæður verður bætt við í síðari útgáfu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]