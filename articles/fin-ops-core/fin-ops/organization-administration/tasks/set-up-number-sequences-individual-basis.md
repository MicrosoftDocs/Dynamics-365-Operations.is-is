---
title: Uppsetning númeraraða á einstaklingsgrunni
description: Þetta efni útskýrir hvernig setja skuli upp númeraraða á einstaklingsgrunni.
author: sericks007
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74422a9f2b737053288d21ba7a578c854cab1335
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747322"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Uppsetning númeraraða á einstaklingsgrunni

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig setja skuli upp númeraraða á einstaklingsgrunni. Númeraraðir eru notaðar til að mynda lesanleg, einkvæm kenni fyrir skýrslur aðalgagna og færslur sem krefjast þeirra. Skýrsla aðalgagna eða færslu sem krefst kennis er kölluð Tilvísun. Áður en hægt er að stofna nýjar færslur fyrir tilvísun verður að setja upp númeraröð og tengja hana við tilvísunina. Stofna má bókhald fyrir allar númeraraðir sem þörf er á samtímis með því að nota leiðsagnarforritið **Setja upp númeraraðir** eða hægt er að stofna eða breyta einstaka númeraröðum með því að nota **númeraröð** síða.

1. Farðu í **Skoðunarrúða > Kerfiseiningar > Fyrirtækjastjórnun > Númeraraðir > Númeraraðir**.
2. Velja **númeraraðir**.
3. Í reitnum **Kóði númeraraðar** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Á **færibreytur umfangs** flýtiflipanum, velja svið fyrir númeraröðina og velja gildi umfangs af fellilistanum. Umfang skilgreinir hvaða fyrirtæki nota númeraröðina. Auk þess, númeraraðir sem hafa annað umfang en **samnýtt** geta haft hluta sem eiga við þeirra umfang. Til dæmis getur talnaröð með umfangið lögaðili innihaldið umfangið **lögaðila**. Frekari upplýsingar um umfang, sjá [Númeraraðar yfirlit](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview). 
6. Stækkaðu hlutann **Hlutar**.
    - Skilgreina snið fyrir númeraröðina með því að bæta við, fjarlægja og endurraða hlutum.  
    - Númeraraðir á öllum sviðum geta innihaldið *Fasta hluta* og *bók- og tölustafi hluta*. Fasta hluta innihalda tölu- og bókstafi sem breytast ekki. Nota þessi hlutagerð til að bæta bandstriki eða öðrum skiltákn milli hlutar númeraraðar. Bók-eða tölustafir hlutar innihalda samsetningu númerstákn (#) og og-merki (&). Þessar stafir tákna tölustafi og bókstafi sem hækka í hvert sinn sem númerið úr röðin er notað. Nota númerstákn (#) til að tilgreina hækkandi tölustafi og og-merki (&) til að tilgreina hækkandi bókstafi. Sniðið `#####_2014` stofnar til dæmis röðina `00001_2014`, `00002_2014`, o.s.frv. Að minnsta kosti einn hluti bók - og tölustafa verður að vera til staðar. Sviðshlutar, eins og fyrirtæki eða lögaðili, eru ekki skylda. Hinsvegar jafnvel þó sviðshlutar eru ekki hafðir með í sniðinu, eru númer fyrir valda tilvísun samt sem áður mynduð fyrir hvert svið.  
7. Víkkið út hlutann **Tilvísanir**. Veldu gerð skjals eða skýrslu til að útnefna þessa númeraröð til. Valfrjálst fyrir raðir sem eru skilgreindar fyrir sérstakt notkunarmynstur forrits. Í þessu dæmi er nýtt númer myndað með því að nota gildi kóða númeraraðar eða kenni, án þess að nota tilvísun. Dæmi um sérstakt notkunarmynstur forrits er fylgiskjalaruna sem er notuð fyrir ákveðin færslubókanöfn. Hins vegar ekki mælt með að það séu notuð slík mynstur.  
8. Víkkaðu út hlutann **Almennt**. Á almennt flýtiflipanum skal tilgreina hvort númeraröðin sé handvirk, og samfelld eða ósamfelld. Auk þess eru færðir inn lægstir og hæstir tölustafir sem hægt er að nota í númeraröðinni. Við mælum ekki með því að breyta ósamfelldri númeraröð í samfellda númeraröð. Númeraröðin verður ekki sannlega samfelld. Þessi breyting getur líka valdið broti á tvítekningarlykli í gagnagrunninum. Að auki er hafa samfelldar númeraraðir meiri áhrif á afköst.   
9. Smellt er á **Vista**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]