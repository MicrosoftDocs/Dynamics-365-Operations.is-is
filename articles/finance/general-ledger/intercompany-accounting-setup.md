---
title: Uppsetning samstæðulykils
description: Þessari grein útskýrir hvernig skal setja upp bókhald innan samstæðu svo að hægt sé að nota færslubók innan samstæðu fyrir daglega færslubók, reikning lánardrottinns og greiðslubók.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09c8933b08710ec82dbb449f2ba7f7c29cc24ff3a4c9b73178aa916ea0fab83a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715071"
---
# <a name="intercompany-accounting-setup"></a>Uppsetning samstæðulykils

[!include [banner](../includes/banner.md)]

Þessari grein útskýrir hvernig skal setja upp bókhald innan samstæðu svo að hægt sé að nota færslubók innan samstæðu fyrir daglega færslubók, reikning lánardrottinns og greiðslubók.

Stofna má samstæðufærslubækur í ýmsum tilvikum, eins og fyrir daglegar færslubækur, reikningsbækur lánardrottins, fjárhagsúthlutanir og miðstýrðar greiðslur. Til að virkja þessi tilvik, verður að setja upp bókhald innan samstæðu.

## <a name="define-main-accounts"></a>Skilgreina aðallykla
Fyrst þarf að stofna aðallykla innan samstæðu til að nota fyrir „Vegna“ og „Gjalddagi“ úr bókhaldsfærslum. Gott er að nota einstaka aðallykla°fyrir hvert fyrirtæki til að auðvelda afstemmingu og losun á bókhaldsfærslum innan samstæðu. Ef verið er að nota viðskiptaaðila eða mótaðilavídd að auðkenna samstæðuaðila er hægt að skilgreina víddina sem°fasta vídd í aðallykli sem er skilgreind í samstæðubókhaldi. Þegar°settir eru upp á aðallyklar ætti að stilla svæðið í **Gerð aðallykils** á **Efnahagsreikningur** á síðunni **Aðallyklar**.

## <a name="define-journal-names"></a>Skilgreina heiti færslubókar
Næst skal skilgreina færslubókarheiti. Stillið **Færslubókargerð** á **Daglega** á síðunni **Heiti færslubóka**. Gott er að nota sértækt færslubókarheiti fyrir samstæðu°bókhald.

## <a name="define-intercompany-accounting-setup"></a>Skilgreina uppsetningu samstæðulykils
Síðan **Samstæðulyklar**,er notuð til að stofna pör lögaðila sem geta átt viðskipti saman. Uppsetning samstæðulykils er samnýtt svo að uppsetningin er sýnileg öllum lögaðilum. Þegar stofna á nýtt lögaðilapar skal tryggja að þú virit hvaða lögaðili er skilgreindur sem upprunafyrirtæki, en ekki áfangastaðarfyrirtæki Þegar viðskipti innan samstæðu eru færð inn ákvarðar færslan hvaða lögaðili er að hefja eða er uppruni færslunnar. Uppsetning samstæðulykils er til dæmis uppsetning fyrir USMF (uppruni) og USSI (áfangastaður). Ef notandi er virkur í USSI og færir inn samstæðufærsla með USMF, verður færslan ekki bíðu þar sem samstæðulyklar eru aðeins skilggreindir fyrir USMF sem uppruna. Ef bæði fyrirtæki geta verið uppruni færslu þarf að stofna annað lögaðilapar fyrir umhverfa uppsetningu. 

Veldu **Debetreikningur (á gjalddaga frá)** og **Kreditlykill (í gjalddaga til)** fyrir bæði uppruna- og áfangastaðarlögaðila. Skilgreindu hvaða **Heiti færslubókar** er notað þegar færslan er stofnuð í áfangastaðarfyrirtækinu. Færslubók upprunafyrirtæki er þegar þekkt þar sem hún er valin af notanda þegar samstæðufærslan er stofnuð. 

Loks skal velja hvaða lögaðili fær sent bókhald fyrir stuðningsupphæðir, s.s. staðgreiðsluafslátt eða innleystur hagnaður/tap fyrir miðstýrð greiðsla. 

Hægt er að setja upp umhverf tengsl á síðunni **Samstæðulyklar** með því að nota hnappinn **Stofna umhverf tengsl** eftir að fyrsta lögaðilaparið er stofnað. Þegar gangkvæmt par er stofnað eru upplýsingar um áfangastaðarfyrirtæki afritaðar í upprunafyrirtækið og öfugt. Færslubókin sem skilgreind er fyrir áfangastaðarfyrirtækið helst óbreytt. Flest fyrirtæki nota sömu nafngiftarvenjur fyrir færslubókarheiti og því er heiti færslubókar það sama. Ef heiti færslubókar er annað birtist viðvörun í reitnum til að láta þig vita að færslubók sé ekki til og að hægt sé að velja aðra færslubók.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]