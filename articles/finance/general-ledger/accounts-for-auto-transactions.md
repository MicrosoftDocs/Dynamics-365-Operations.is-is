---
title: Lyklar fyrir sjálfvirkar færslur
description: Þetta efnisatriði útskýrir hvernig reikningar fyrir sjálfvirkar færslur eru notaðar til að bóka í gegnum Microsoft Dynamics 365, og gefur dæmi um lykilreikninga fyrir sjálfvirkar færslur.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275c74d673d1ba2468e23c5fa443c9272d13a184
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735261"
---
# <a name="accounts-for-automatic-transactions"></a>Lyklar fyrir sjálfvirkar færslur

The **Reikningar fyrir sjálfvirkar færslur** síða (**Aðalbók&gt; Uppsetning færslu&gt; Reikningar fyrir sjálfvirkar færslur**) er notað til að skilgreina sjálfgefna aðalreikninginn sem er notaður fyrir hverja bókunartegund í kerfinu. Þó að hægt sé að stilla flestar birtingargerðir á sértækri einingu eða eiginleikasértækri síðu, er aðeins hægt að stilla sumar birtingargerðir á **Reikningar fyrir sjálfvirkar færslur** síðu.

Til dæmis geturðu tilgreint aðalreikninginn sem er notaður fyrir **Jafnvægi viðskiptavina** staða tegund the **Samantekt** sviði á **Færsluprófíl viðskiptavinar** síðu og notaðu annan aðalreikning fyrir hvern viðskiptavinaprófíl. Þannig hefurðu nákvæmari stjórn á færslunum. Aftur á móti geturðu aðeins tilgreint villureikninginn á **Reikningar fyrir sjálfvirkar færslur** síðu.

Þegar þú opnar **Reikningar fyrir sjálfvirkar færslur** síðu í nýjum lögaðila, listi yfir reikninga verður tómur. Þú getur bætt við algengustu færslugerðum sem ætti að stilla á síðunni með því að velja **Búðu til sjálfgefnar tegundir** takki. Síðan, fyrir hverja röð, geturðu valið aðalreikninginn í **Aðalreikningur** sviði. Ef þú yfirgefur **Aðalreikningur** reiturinn auður fyrir bókunartegund og þú hefur ekki stillt aðalreikning á sértækri einingu eða eiginleikasértækri síðu færðu villuboð þegar þú bókar færslu sem notar bókunargerðina. Venjulega munu skilaboðin vera „Reikningurinn fyrir\[ Tegund færslu\] er ekki hægt að finna."

## <a name="default-posting-types"></a>Sjálfgefnar færslugerðir

Eftirfarandi tafla sýnir dæmi um sjálfgefnar færslugerðir sem eru búnar til þegar þú velur **Búðu til sjálfgefnar tegundir** á **Reikningar fyrir sjálfvirkar færslur** síðu. Það sýnir sýnishorn af aðalreikningum og lýsingum. "Debet/kredit?" Dálkurinn gefur til kynna hvort færslunni er venjulega bókað debet eða kredit. Í sumum tilfellum getur færsla bókað annað hvort debet eða kredit. Dálkurinn „Jöfnunarreikningur“ gefur til kynna hvort bókunartegundin sé jöfnunarreikningur. Ef bókunartegundin er jöfnunarreikningur er upphæðin sem er bókuð á reikningnum sjálfkrafa bakfærð þegar síðari færsla er bókuð.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Auramismunur í skýrslugjaldmiðli | 618160 | Ýmis kostnaður | Kostnaður | Bæði | Nr. | Þessi bókunartegund er notuð þegar eyrismunur á sér stað þegar færsluupphæð í erlendum gjaldmiðli er umreiknuð í skýrslugjaldmiðilinn. |
| Auramismunur í bókhaldsgjaldmiðli | 618160 | Ýmis kostnaður | Kostnaður | Bæði | Nr. | Þessi bókunartegund er notuð þegar eyrismunur á sér stað þegar færsluupphæð í erlendum gjaldmiðli er færð yfir á bókhaldsgjaldmiðilinn. |
| Villulykill | 999999 | Villureikningur | Kostnaður | Bæði | Nr. | Þessi bókunartegund er notuð þegar villa kemur upp í kerfinu. Reikningurinn ætti að vera staðfestur á hverju tímabili og allar villur ætti að leysa. |
| Niðurstaða í árslok | 300160 | Óráðstafað eigið fé | Eigið fé | Bæði | Nr. | Þessi bókunartegund er notuð þegar lokaferli ársins er keyrt til að færa stöðu reikninga á **Hagnaður og tap** sláðu inn á aðalreikninginn sem er valinn fyrir árslokauppgjör. |
| Staðgreiðsluafsláttur viðskiptavinar | Á ekki við | Á ekki við | Á ekki við | Á ekki við | Nr. | Birtingartegundin sem er skilgreind á **Reikningar fyrir sjálfvirkar færslur** síða er ekki notuð. Aðalreikningur er nauðsynlegur þegar staðgreiðsluafsláttur er stilltur í Viðskiptakröfur.|
| Staðgreiðsluafsláttur lánardrottins | Á ekki við | Á ekki við | Á ekki við | Á ekki við | Nr. | Birtingartegundin sem er skilgreind á **Reikningar fyrir sjálfvirkar færslur** síða er ekki notuð. Aðalreikningur er nauðsynlegur þegar staðgreiðsluafsláttur er stilltur í Viðskiptaskuldir. |

## <a name="additional-posting-types"></a>Fleiri færslugerðir

Eftirfarandi tafla sýnir dæmi um fleiri færslugerðir sem þarf að stilla ef þú ætlar að nota tengda eiginleika. Fyrir þessar færslugerðir er engin uppsetning færslusniðs tiltæk í annarri einingu. "Debet/kredit?" Dálkurinn gefur til kynna hvort færslunni er venjulega bókað debet eða kredit. Í sumum tilfellum getur færsla bókað annað hvort debet eða kredit. Dálkurinn „Jöfnunarreikningur“ gefur til kynna hvort bókunartegundin sé jöfnunarreikningur. Ef bókunartegundin er jöfnunarreikningur er upphæðin sem er bókuð á reikningnum sjálfkrafa bakfærð þegar síðari færsla er bókuð.

| Bókunargerð | Dæmi um aðalreikning | Dæmi um nafn aðalreiknings | Lykilgerð | Debet/kredit? | Millireikningur | Lýsing |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Jafnvægisreikningur fyrir samstæðumun | 801200 | Hagnaður og tap - Endurmat | Kostnaður | Bæði | Nr. | Þessi bókunartegund er notuð þegar þú framkvæmir samstæðu sem felur í sér endurmat gjaldmiðils og munur á krónum kemur fram við endurmatið. |
| Rekstrarreikningur fyrir samstæðumismun | 801200 | Hagnaður og tap - Endurmat | Kostnaður | Bæði | Nr. | Þessi bókunartegund er notuð þegar þú framkvæmir samstæðu sem felur í sér endurmat gjaldmiðils og munur á krónum kemur fram við endurmatið. |
| Millieiningar – debet | 133500 | Innheimta milli eininga | Eign | Debet | Nr. | Þessi bókunartegund er notuð þegar þú velur jöfnunarvídd á **Fjárhagsbók** síðu og víddin kemur ekki í jafnvægi í færslu sem er bókuð. |
| Millieining - kredit | 233500 | Greiðsla milli eininga | Skuld | Kredit | Nr. | Þessi bókunartegund er notuð þegar þú velur jöfnunarvídd á **Fjárhagsbók** síðu og víddin kemur ekki í jafnvægi í færslu sem er bókuð. |
