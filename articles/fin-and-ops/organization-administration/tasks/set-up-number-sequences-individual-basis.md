---
title: Setja upp númeraröð á einstaklingsgrundvelli
description: Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6734d66a06f8a8dc90a48bd68b7b4e22177b4672
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560591"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Setja upp númeraröð á einstaklingsgrundvelli

[!include [task guide banner](../../includes/task-guide-banner.md)]

Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra. Skýrsla aðalgagna eða færslu sem krefst kennis er kölluð Tilvísun. Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina. Stofna má bókhald fyrir allar númeraraðir sem þörf er á samtímis með því að nota leiðsagnarforritið eða hægt er að stofna eða breyta einstaka númeraröðum með því að nota númeraröð síða.

1. Fara í Fyrirtækisstjórnun > Númeraröð > Númeraröð.
2. Smella á númeraröð.
3. Í reitinn kóði númeraraðar skal slá inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Útvíkka hlutann gildissvið færibreytur.
    * Á færibreytur sviðs flýtiflipanum, velja svið fyrir númeraröðina og velja gildi sviða.     Umfang skilgreinir hvaða fyrirtæki nota númeraröðina. Auk þess, númeraraðir sem hafa svið önnur en samnýtt geta haft hluta sem eiga við þeirra svið. Til dæmis getur talnaröð með umfangið lögaðili innihaldið hluta lögaðila. Frekari upplýsingar um umfang, sjá "Númeraraðar yfirlit" í Hjálp efnisatriði.  
6. Stækka the hlutann hlutir.
    * Á hluti flýtiflipanum skal skilgreina snið fyrir númeraröðina með því að bæta við, fjarlægja og endurraða hlutum.  
    * Númeraraðir á öllum sviðum getur innihaldið Fasta hluta og bók- og tölustafi hluta. Fasta hluta innihalda tölu- og bókstafi sem breytast ekki. Nota þessi hlutagerð til að bæta bandstriki eða öðrum skiltákn milli hlutar númeraraðar. Bók-eða tölustafir hlutar innihalda samsetningu númerstákn (#) og og-merki (&). Þessar stafir tákna tölustafi og bókstafi sem hækka í hvert sinn sem númerið úr röðin er notað. Nota númerstákn (#) til að tilgreina hækkandi tölustafi og og-merki (&) til að tilgreina hækkandi bókstafi. Sniðið #####_2014 stofnar til dæmis röðina 00001_2014, 00002_2014 o.s.frv.     Að minnsta kosti einn hluti bók - og tölustafa verður að vera til staðar. Sviðshlutar, eins og fyrirtæki eða lögaðili, eru ekki skylda. Hinsvegar jafnvel þó sviðshlutar eru ekki hafðir með í sniðinu, eru númer fyrir valda tilvísun samt sem áður mynduð fyrir hvert svið.  
7. Víkkið út hlutann tilvísanir.
    * Á tilvísun flýtiflipanum skal velja gerð skjals eða skýrslu til að úthluta þessa númeraröð til.     Valfrjálst fyrir raðir sem eru skilgreindar fyrir sérstakt notkunarmynstur forrits. Í þessu dæmi er nýtt númer myndað með því að nota gildi kóða númeraraðar eða kenni, án þess að nota tilvísun. Dæmi um sérstakt notkunarmynstur forrits er fylgiskjalaruna sem er notuð fyrir ákveðin færslubókanöfn. Hins vegar ekki mælt með að það séu notuð slík mynstur.  
8. Víkkið út almenna hlutann.
    * Á almennt flýtiflipanum skal tilgreina hvort númeraröðin sé handvirk, og samfelld eða ósamfelld. Auk þess eru færðir inn lægstir og hæstir tölustafir sem hægt er að nota í númeraröðinni.     Við mælum ekki með því að breyta ósamfelldri númeraröð í samfellda númeraröð. Númeraröðin verður ekki sannlega samfelld. Þessi breyting getur líka valdið broti á tvítekningarlykli í gagnagrunninum. Að auki er hafa samfelldar númeraraðir meiri áhrif á afköst.   
9. Smellið á „Vista“.

