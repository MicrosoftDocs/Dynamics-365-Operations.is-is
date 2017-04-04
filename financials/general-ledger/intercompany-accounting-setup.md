---
title: "Uppsetning bókhalds innan samstæðu"
description: "Í þessu efnisatriði er útskýrt hvernig á að setja upp bókhald innan samstæðu svo að hægt er að nota samstæðu færslubækur fyrir úthlutun fjárhags og fjárhagsbækur daglegar færslubækur, reikningabókum lánardrottins og greiðslubókum."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Uppsetning bókhalds innan samstæðu

Í þessu efnisatriði er útskýrt hvernig á að setja upp bókhald innan samstæðu svo að hægt er að nota samstæðu færslubækur fyrir úthlutun fjárhags og fjárhagsbækur daglegar færslubækur, reikningabókum lánardrottins og greiðslubókum.

Samstæðu stofna má færslubækur í ýmsum tilvikum, eins og fyrir daglegar færslubækur reikningabók lánardrottna, fjárhagsúthlutunum og miðstýrðar greiðslur. Til að virkja þessi tilvik, verður að setja upp bókhald innan samstæðu.

## <a name="define-main-accounts"></a>Skilgreina aðallykla
Fyrst þarf að stofna aðallykla innan samstæðu til að nota fyrir „Vegna“ og „Gjalddagi“ úr bókhaldsfærslum. Gott er að nota einstaka aðallykla°fyrir hvert fyrirtæki til að auðvelda afstemmingu og losun á bókhaldsfærslum innan samstæðu. Ef verið er að nota til að auðkenna samstæðu aðila viðskiptaaðila eða hliðstæð vídd, hægt er að skilgreina víddina sem föst vídd í aðallykil sem er skilgreind í samstæðubókhaldi. Þegar sett er upp á aðallykla ætti að setja í **lykilgerð Aðal** á **efnahagsreikningur** á í **aðallykla** síðu.

## <a name="define-journal-names"></a>Skilgreina færslubókarheiti
Næst skal skilgreina færslubókarheiti. Setja í **færslubókargerð** á **Daglega** á í **færslubókarnöfn** síðu. Gott er að nota sértækt færslubókarheiti fyrir samstæðu°bókhald.

## <a name="define-intercompany-accounting-setup"></a>Skilgreina uppsetningu bókhald innan samstæðu
Í **samstæðubókhald** síða er notuð til að stofna pörum lögaðila sem hægt er að transact með hver annarri. Uppsetning bókhalds innan Samstæðu er samnýtt, þannig að uppsetningu er ekki sýnilegur úr innan alla lögaðila. Þegar nýr lögaðili par, tryggja að hafa í huga lögaðila sem er skilgreind sem upprunafyrirtækið samanborið við viðtökufyrirtækið. Þegar færslur innan samstæðu er færð inn færsluna ákvarðar hvaða lögaðila er byrjað eða færslan er upprunnin. Til dæmis bókhald innan samstæðu er sett upp fyrir USMF (upprunninn) og USSI (áfangastað). Ef notandi er virk í USSI og færir samstæðufærsla með USMF, færslan verður ekki bókuð því bókhald innan samstæðu er aðeins skilgreint fyrir USMF verið upphafsmanns. Ef annað hvort fyrirtækisins geta átt sér færslu, þarf að stofna aðra lögaðila par skráð gagnkvæmt uppsetningu. 

Velja á **Skuldfæra á reikning (Gjalddaga frá)** og **Kredit lykill (Gjalddaga til)** fyrir bæði uppruna- og viðtökuvöruhússins lögaðila. Skilgreina sem **færslubókarheiti** verður notað þegar færslan er stofnuð í fyrir viðtökufyrirtækið. Færslubók fyrir upprunafyrirtækið er þekkt þar sem hún valin af notanda þegar innan samstæðu er stofnuð. 

Að lokum skal velja lögaðilann sem fær bókhald fyrir styðja upphæðir staðgreiðsluafsláttar eða innleystur hagnaður/tap fyrir miðstýrðar greiðslur. 

Auðveldlega er hægt að setja skráð gagnkvæmt vensl á við **bókhald innan Samstæðu** síðu með því að nota í **Stofna vensl skráð gagnkvæmt** hnappinn eftir fyrsta par lögaðila er stofnuð. Þegar skráð gagnkvæmt par er stofnuð fyrir viðtökufyrirtækið upplýsingarnar eru afritaðar í upprunafyrirtækið og öfugt. Færslubók sem er skilgreind fyrir viðtökufyrirtækið haldast. Flest fyrirtæki nota sama nafnareglu fyrir færslubókarheiti þeirra, svo að heiti færslubókar sem er sú sama. Ef færslubókarheiti er mismunandi mun viðvörun birtast á svæðinu til að tilkynna sem er ekki til í færslubókinni og ekki er hægt að velja aðra færslubók.


