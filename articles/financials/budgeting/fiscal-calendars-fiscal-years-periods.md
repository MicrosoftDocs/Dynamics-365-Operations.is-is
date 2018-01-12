---
title: "Fjárhagsdagatal, fjárhagsár og tímabil"
description: "Þessi grein fjallar um fjárhagsdagatöl, reikningsár og tímabil og hvernig á að nýta þau fyrir lögaðila, eignir og fjárhagsáætlanir."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FiscalCalendars
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25851
ms.assetid: a968a5e5-585e-4389-aa4e-c885a7e23413
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 431d654aaffc27d54fd590dc7d5d2ab6c2313908
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="fiscal-calendars-fiscal-years-and-periods"></a>Fjárhagsdagatal, fjárhagsár og tímabil

[!include[banner](../includes/banner.md)]


Þessi grein fjallar um fjárhagsdagatöl, reikningsár og tímabil og hvernig á að nýta þau fyrir lögaðila, eignir og fjárhagsáætlanir.

Fjárhagsdagatöl veita ramma fjárhagslegar verkþáttar fyrirtækis. Hvert fjárhagsdagatal inniheldur eitt eða fleiri fjárhagsár og hvert fjárhagsár inniheldur mörg tímabil. Hægt er að byggja fjárhagsdagatöl á 1. Janúar til almanaksárs 31. Desember eða á hvaða dagsetningar sem er valin. Till dæmis velja sum fyrirtæki fjárhagsdagatal sem byrjar 1. júlí eins árs og lýkur 30. júní næsta ár á eftir. 

Það er engin fjárhagsdagatöl sem hægt er að stofna fjölda, og engin mörk fjölda fjárhagsára sem hægt er að stofna fjárhagsdagatal. Hvert fjárhagsdagatal er óháð fyrirtækið og hægt er að nota það með marga lögaðila í fyrirtækinu. Til dæmis hefur fyrirtæki átta deildir og hver deild er sérstakur lögaðili. Fimm þeirra deila sama fjárhagsdagatal og nota þrjár mismunandi fjárhagsdagatöl. Hægt er að stofna eina fjárhagsdagatal fimm lögaðila sem deila sama fjárhagsdagatali og stofna síðan aðskilin fjárhagsdagatöl á aðra lögaðila.

## <a name="create-fiscal-calendars-fiscal-years-and-periods"></a>Stofna fjárhagsdagatöl, fjárhagsár og tímabil
Hægt er að stofna og eyða fjárhagsdagatölum, fjárhagsárum og tímabilum í síða fjárhagsdagatals . Einnig er hægt að skipta fyrirliggjandi tímabilum og stofna lokað tímabil sem hægt er að nota til að loka fjárhagsári. 

Lokunartímabil er notað til að aðgreina fjárhagsfærslur sem myndast þegar fjárhagsári er lokað. Þegar lokunarfærslurnar eru í einu fjárhagstímabili er auðveldara að stofna fjárhagsskýrslur sem annað hvort eru með eða án mismunandi gerða lokunarfærslna. Ef fjárhagsári er skipt í 12 fjárhagstímabil er lokunartímabilið er yfirleitt 13. tímabilið. Hins vegar er hægt að stofna lokunartímabil úr hvaða tímabil sem er sem hefur stöðuna opið. 

Þegar stofna á lokunartímabil, veljið tímabil sem hefur stöðuna opið og sem hefur dagsetningarnar sem óskað er að nota. Nýja lokunartímabilið afritar upphafs - og lokadagsetningar úr fyrirliggjandi tímabili. Upphaflega tímabili verður áfram til. Til dæmis valdi notandi tímabil 12 sem er síðasta tímabil í fjárhagsári og það er með dagsetningar 1. ágúst til og með 31. ágúst. Sláið inn heiti lokunartímabils, t.d. „Lokun“. Þegar búið er að stofna nýtt lokunartímabil er notandi nú með upphaflega tímabilið og lokunartímabilið. Bæði með dagsetningar sem hefjast 1. ágúst og enda á 31. ágúst.

## <a name="select-fiscal-calendars-for-ledgers-fixed-assets-and-budget-cycles"></a>Velja fjárhagsdagatöl fyrir fjárhag, eignum og fjárhagsáætlunarferli
Fjárhagsdagatöl eru notaðar við afskriftir eigna, fjárhagslegar færslur og ferli fjárhagsáætlunar. Þegar fjárhagsdagatal stofnað er hægt að nota það í margvíslegum tilgangi. Hægt er að velja fjárhagsdagatal í virðislíkani eða afskriftarbók til að gera dagatal fastra eigna. Hægt er að velja fjárhagsdagatal fyrir fjárhag til að gera dagatal fjárhags. Og þú getur valið fjárhagsdagatal fyrir ferli fjárhagsáætlunar til að gera það að dagatali fjárhagsáætlunar. Hægt er að nota sama fjárhagsdagatal fyrir þær allar.

### <a name="select-a-fiscal-calendar-for-your-legal-entity"></a>Veljið fjárhagsdagatal fyrir lögaðila þinn.

Velja fjárhagsdagatal sem á að nota fyrir við lögaðilann í fjárhag í fjárhags skjámynd. Fjárhagsdagatal verður að velja í fjárhags skjámynd fyrir hverja lögaðila. Eftir að fjárhagsdagatal er valið er hægt að setja upp staða tímabils og heimildir í fjárhagsdagatal síðu fyrir einhver tímabil sem eru hluti fjárhagsársins.

### <a name="select-a-fiscal-calendar-for-fixed-assets"></a>Veldu fjárhagsdagatal fyrir eignir

Hægt er að velja fjárhagsdagatal í virðislíkani eða afskriftabókar, og það fjárhagsdagatal verður notað með eignunum sem nota valda virðislíkanið eða afskriftarbók eigna. Hægt er að velja úr öllum fjárhagsdagatöl sem skilgreind eru á síðunni fjárhagsdagatöl.

### <a name="define-budget-cycle-time-spans"></a>Skilgreina tímabil fjárhagsáætlunar

Fjárhagsáætlunarferli eru lengd þess tíma þegar fjárhagsáætlun er notuð. Fjárhagsáætlunarferli geta verið hluti af fjárhagsári eða mörg fjárhagsár, fjárhagsáætlunarferli yfir tvö ár eða fjárhagsáætlunarferli á þremur árum. Ferli fjárhagsáætlunar fjárhagsáætlunarferlis skilgreinir fjölda tímabila sem eru innifaldar í ferli fjárhagsáætlunar. Til að tilgreina tímabil fjárhagsáætlunar skal nota tímabil fjárhagsáætlunar síða .

## <a name="maintain-periods-for-your-organization"></a>Viðhalda tímabilum fyrir fyrirtæki þitt
Hægt er að nota síðuna fjárhagsdagatal til að skoða upplýsingar um fjárhagsdagatal, fjárhagsára og tímabilum sem fyrirtæki þitt notar. Einnig er hægt að breyta stöðu tímabila og velja hvaða notendur geta bókað bókhaldsfærslur á tímabil. Til dæmis við upphaf nýs tímabils væri ef til vill vilji til að láta hóp notenda ljúka bókun fjárhagslegra færslna á fyrra tímabili, en hina hópana vinna aðeins á nýja tímabilinu.






