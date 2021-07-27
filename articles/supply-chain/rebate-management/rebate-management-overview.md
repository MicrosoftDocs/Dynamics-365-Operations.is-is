---
title: Yfirlit einingar fyrir stjórnun eftirágreidds afsláttar
description: Þetta efnisatriði býður upp á yfirlit yfir stjórnunareiningu eftirágreidds afsláttar fyrir Microsoft Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 577d48e207c8ce5911d104e657101a8557100064
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339995"
---
# <a name="rebate-management-module-overview"></a>Yfirlit einingar fyrir stjórnun eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Hægt er að nota eininguna **Stjórnun eftirágreidds afsláttar** til að búa til samninga, tilboð eða samkomulag milli fyrirtækisins og viðskiptavina eða lánardrottna þess þannig að hægt sé að reikna út eftirágreidda afslætti, lækkanir og afnotagreiðslur. Stjórnun eftirágreidds afsláttar rekur og vinnur með færslur eftirágreidds afsláttar og lækkunar á miðlægri staðsetningu þar sem notendur geta á skilvirkan hátt búið þær til, farið yfir þær og unnið úr þeim.

Stjórnun eftirágreidds afsláttar styður stofnun, viðhald og úrvinnslu *eftirágreiddra afslátta*. Eftirágreiddur afsláttur er það þegar seljandi eða kaupandi skilar hluta innkaupaverðsins. Eftirágreiddan afsláttur miðast yfirleitt við kaup á tilteknu magni eða verðmæti vöru á tilteknu tímabili. Ólíkt afsláttum eru eftirágreiddir afslættir gerðir eftir að upphæð innkaupanna hefur verið reikningsfærð að fullu.

Stjórnun eftirágreidds afsláttar styður líka *lækkanir*. Lækkun eru bætur, endurgjald eða þóknun sem er greidd annaðhvort fyrir leyfi eða afnotarétt hugverks á borð við vörumerki, höfundarrétt eða einkaleyfis, eða vegna réttinda til að nota náttúrulega auðlind t.d. í því skyna að stunda fiskveiðar, veiðar eða námugröft. Lækkanir eru yfirleitt reiknaðar út sem prósenta af tekjum eða hagnaði af skráðri notkun. Því meira sem hugverkið eða náttúrulega auðlindin er notuð, því meiri verður skráð lækkun.

Auk þess styður stjórnun eftirágreidds afsláttar *afnotagreiðslur* viðskiptavinar. Afnotagreiðslur eru greiðslur sem einn aðili greiðir leyfishafa eða umboðsmanni fyrir réttinn til að nota eign.

Stjórnun eftirágreidds afsláttar gerir kleift að skilgreina bókunarreglur fyrir úthlutanir, eftirágreidda afslætti og afskriftir. Þar að auki er hægt að skilgreina bókanir fyrir tiltekinn viðskiptavin eða lánardrottinn. Á þennan hátt er hægt að rekja tilboð, sem gilda ekki um allar aðstæður viðskiptavinar eða lánardrottins, í gegnum bókanir.

Færslur eftirágreidds afsláttar eru sjálfkrafa myndaðar samkvæmt útreikningsaðferðinni sem er valin og tímasett í runuvinnslum. Auk þess er hægt að setja upp verkferla til að hafa umsjón með, yfirfara og samþykkja samkomulög.

## <a name="basis-calculation"></a>Útreikningsgrunnur

Eftirágreiddir afslættir, afnotagreiðslur viðskiptavinar og eftirágreiddir afslættir lánardrottins geta öll notað mismunandi grunn sem fer eftir viðskiptakröfunum:

- Eftirágreiddir afslættir viðskiptavinar geta byggst á sölupöntunum, fylgiseðlum eða reikningum.
- Afnotagreiðslur viðskiptavinar geta byggst á sölupöntunum, fylgiseðlum eða greiddum reikningum.
- Eftirágreiddur afsláttur lánardrottins geta byggst á annaðhvort innkaupapöntunum eða sölupöntunum. Hægt er að reikna þá út samkvæmt afurðum sem eru keyptar frá lánardrottni eftirágreidds afsláttar og seldir viðskiptavinum í gegnum sölureikninga.

## <a name="flexible-calculations"></a>Sveigjanlegir útreikningar

Útreikningstímabil eftirágreiddra afslátta eru í boði fyrir bæði tilboð viðskiptavina og lánardrottna. Útreikningstímabil skilgreinir lengd tímabilsins, útreikningstíðninni og útreikningstímabilinu. Hægt er að safna upp eftirágreiddum afsláttum samvkæmt magni sölupöntunar eða magni viðurkenndra afurða á tímabili eftirágreidds afsláttar.

Fyrir hvern útreikning á samkomulagi er hægt að stilla eitthvert eftirfarandi tímabila:

- Reikningur
- Dagur
- Vika
- Mánuður
- Ársfjórðungur
- Ár
- Sérstillt tímabil
- Eitthvert margfeldi einhvers af fyrri birtum tímabilum

Hægt er að nota útreikninginn fyrir einstaka viðskiptavini og afurðir, hópa af viðskiptavinum og afurðum eða alla viðskiptavini og afurðir. Afslættir sem eru með margar upplýsingalínur geta verið með mismunandi viðurkennd dagsetningabil. Tímabil úthlutunar og innheimtu getur verið frábrugðið. Til dæmis er hægt að vinna úr úthlutunum daglega á meðan innheimtur eru gerðar mánaðarlega.

Hægt er að skilgreina eftirágreidda afslætti út frá mörgum mismunandi færibreytum. Til dæmis er hægt að skilgreina þá sem prósentu, taxta eða fasta upphæð. Fjórar meginaðferðir eru til við útreikning:

- Þrepaskipt
- Uppsöfnun
- Völsun
- Heildarvirði

Einnig er hægt að lækka útkomu útreiknings á eftirágreiddum afslætti af hálfu annarra eftirágreiddra afslátta eftir því hvort eftirágreiddur afsláttur er settur upp til að gera útreikning út frá nettóupphæðinni.

Hjá lánardrottni geta eftirágreiddir afslættir sem byggja á sölupöntunum reiknað út verðið byggt á fyrst inn, fyrst út (FIFO) reglunni, síðasta innkaupaverði, meðaltali innkaupaverðs eða söluverði.

## <a name="rebate-target-transactions"></a>Markfærslur eftirágreidds afsláttar

Niðurstöður tilboðs eða samkomulags eftirágreidds afsláttar geta verið fjárhagslegar eða vörur.

Fjárhagslegar niðurstöður ákvarðast af greiðslugerðinni sem samkomulaginu er úthlutað úr bókunarreglunni. Þessar útkomur geta falið í sér frádráttarbækur viðskiptavina, reikninga með frjálsum texta og lánardrottnareikninga. Vegna endurskoðunar geta fjárhagslegar markfærslur eftirágreidds afsláttar falið í sér tilvísun í upprunalegan samning um eftirágreiddan afslátt.

Útkomur í formi vöru búa til sölupöntun ókeypis vöru fyrir eftirágreidda afslætti viðskiptavinar og innkaupapöntun fyrir eftirágreidda afslætti lánardrottins. Markfærslur eftirágreidds afsláttar í formi vöru innihalda valkosti til að skera úr um hvaða tilvísun eftirágreidds afsláttar á að færa inn á sölupöntun eða innkaupapöntun ókeypis vöru.

## <a name="accurate-rebate-calculations"></a>Nákvæmir útreikningar eftirágreidds afsláttar

Samsetning tengdra tilboða, tíðni útreikninga, grunnur útreiknings og útreikningsaðferðin sem er valið sker úr um nákvæmni útreikninga eftirágreidds afsláttar. Hægt er að nota úthlutanir eftirágreidds afsláttar til að safna upp bókuðu og innheimtu virði.

Úthlutunum er hægt að stjórna daglega, vikulega, mánaðarlega eða samkvæmt sérstilltu tímabili. Hinsvegar getur virknin úthlutað eða greitt eftirágreiddan afslátt eða tekið við greiðslu vegna hans samkvæmt skilgreindri tíðni sem er af sömu lengd eða lengri en tíðni úthlutunar. Afskrift notar sömu tíðni og eftirágreiddur afsláttur. Notendur geta á einfaldan hátt breytt áætlun eða greiðsluupphæðum hvenær sem er við greiðslu.

Notendur þurfa ekki lengur að afgreiða tilboð eða úthlutanir í tveimur skrefum. Úthlutanir og afskriftir eru bókaðar beint í fjárhag. Auk þess er hægt að búa til kreditnótur sjálfkrafa. Þar af leiðandi er full samþætting við viðskiptaskuldir og viðskiptakröfur. Við úrvinnslu geta útreikningar tekið mið af uppgjörsafsláttum, greiddum reikningum, viðskiptaafsláttum og fyrirliggjandi kreditnótum til að tryggja nákvæman útreikning á upphæðum og virði.

Þegar eftirágreiddir afslættir eru reiknaðir út býr ferlið til færslur sem hægt er að yfirfara áður en er bókað. Aðskilið ferli bókar færslur eftirágreidds afsláttar. Síðan er hægt að búa til færslubók, kreditnótu eða debetfærslu við bókun á framlögðum færslum. Hægt er að sækja skýrslu með lista yfir uppgjör og færslur til að tryggja reglufylgni, árangur og gegnsæi.


## <a name="guaranteed-royalty-payments"></a>Tryggðar afnotagreiðslur

Í stjórnunar eftirágreidds afsláttar gerir sjálfvirk greiðslumyndun afnotagreiðslum kleift að afgreiða afnotagreiðslur á fljótlegan og einfaldan hátt jafnvel þegar lágmarkstrygging á við. 

## <a name="maximizing-spend-versus-rebates"></a>Hámarka eyðslu í samanburði við eftirágreidda afslætti

Hægt er að flokka lánardrottna og afurðir eftir umráðasvæði og hægt er að bjóða upp á mismunandi tilboð eftir því hvert land eða svæði færslunnar er. Þegar notendur velja afurðir geta þeir skilgreint vörurnar sem eru hafðar með og vörufjöldann sem verður notaður í uppgjöri eftirágreidds afsláttar.
