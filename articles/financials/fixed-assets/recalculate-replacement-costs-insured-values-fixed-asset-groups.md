---
title: "Endurreikna endurnýjunarverð og vátryggt virði fyrir eignaflokka"
description: "Þessi grein útskýrir ferlið að uppfæra endurnýjunarverð og vátryggt virði fyrir eignir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 74af494f261af20d6762176d780e90b4d6644b4c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Endurreikna endurnýjunarverð og vátryggt virði fyrir eignaflokka

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir ferlið að uppfæra endurnýjunarverð og vátryggt virði fyrir eignir.

Reglulega geta komið tilkynningar um að kostnaðurinn við að skipta út eða tryggja tiltekna eign hafi breyst. Til dæmis gæti yfirmaður tilkynnt að verðbólgan hafi verð 3 prósent á síðasta ári, þannig að nauðsynlegt væri að hækka endurnýjunarverð allra eigna um 3 prósent. 

Þó svo hægt sé að breyta endurnýjunarverði og vátryggðu virði einstakra eigna í skjámyndinni , er hægt að nota skjámyndina  uppfæra endurnýjunarverð og vátryggt virði einstakra eigna til að uppfæra þessi gildi fyrir heilan flokk af eignum á sama tíma. Þessar upplýsingar lýsa því hvernig uppfæra eigi gildi fyrir eignaflokka eða fyrir tilteknar eignir í flokkana.

## <a name="how-values-are-updated"></a> Hvernig gildi eru uppfærð
Ef endurreikna á endurnýjunarverð og vátryggð virði eigna, verður fyrst að tilgreina hlutfall breytingarinnar á endurnýjunarverðum og vátryggðu virði sem fyrir eru, og framkvæma svo reglubundnu uppfærsluna til að raunverulega endurreikna gildin. Tilgreina prósentu í stuðul Endurnýjunarverðs og stuðull Vátryggðs virðis svæðum í skjámyndinni eignaflokkar. Þó að þessir stuðlar séu tilgreindir fyrir allan eignaflokkinn er hægt, þegar þú notar skjámyndina uppfæra endurnýjunarverð og vátryggt virði einstakra eigna, geturðu valið að endurreikna endurnýjunarverð og vátryggð virði eingöngu fyrir tilteknar eignir í flokki. 

Þegar þú notar skjámyndina uppfæra endurnýjunarverð og vátryggt virði einstakra eigna, geturðu valið að endurreikna endurnýjunarverð og vátryggð virði, skal nota eftirfarandi formúlur:

-   \[(Stuðull endurnýjunarverðs eignaflokks / 100) + 1\] \* Núverandi endurnýjunarverð eignar
-   \[(Stuðull vátryggðs virðis eignaflokks / 100) + 1\] \* Núverandi vátryggt virði eignar

> [!NOTE] 
> Þegar þú notar skjámyndina uppfæra endurnýjunarverð og vátryggt virði einstakra eigna, eru bæði endurnýjunarverð og vátryggð virði uppfærð fyrir valdar eignir; þú getur ekki tilgreint að aðeins eitt gildi eigi að vera uppfært. Ef skilja á eftir eitt gildi eins á meðan annað gildi er uppfært, skal færa inn 0 (núll) sem stuðul í skjámyndinni Eignaflokkar. Auður stuðull eða með núllgildi velur því að útreikningnum er sleppt í uppfærslu. Reglubundna uppfærslan hefur engin áhrif á bókfært verð og nettó bókfært verð eigna. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Hvernig nota á dagsetningu til að velja hvaða atriði á að uppfæra
Sjálfgefið uppfærir uppfærsluferlið valdar eignir sem ekki hafa verið uppfærðar á gildandi degi, en hafa ef til vill verið uppfærðar á undanförnum dögum. Til dæmis þýðir &lt; núverandi dagsetning "fyrir daginn í dag." Hægt er að breyta dagsetningunni í skjámyndinni Uppfæra endurnýjunarverð og vátryggð gildi með því að smella á hnappinn Velja. Dagsetningarskilyrðið sem er tilgreint er borið saman við dagsetninguna í síðustu reglubundnu uppfærslu eigna (síðasta reglubundna gildið/uppfærslureitur kostnaðar í skjámyndinni eignir). Hvert sinn sem tekist hefur að uppfæra endurnýjunarverð og vátryggt virði fyrir eign, uppfærir kerfið sjálfkrafa svæðið síðasta reglubundna gildi/uppfærslureitur kostnaðar með gildandi dagsetningu. 

Dæmi 

Þú Uppfærðir endurnýjunarverð farartækja, skrifstofuhúsgagna, og byggingaflokka um 5 prósent í gær, og er nú litið á þessar eignir sem rétt uppfærðar. Ef útiloka á þessar eignir þegar allar aðrar eignir eru uppfærðar í dag, er dagsetning færð inn í svæðið síðasta reglubundna gildi/ kostnaður uppfærslureitur sem er á undan gærdeginum (&lt; dagsetning gærdagsins) vegna þess að síðasta uppfærslan fyrir farartækin, skrifstofuhúsgögnin og byggingarnar átti sér stað utan dagsetningarskilyrðisins sem fært var inn.

## <a name="cumulative-effect-of-each-update"></a> Uppsöfnuð áhrif hverrar uppfærslu
hver uppfærslu er með Uppsöfnuð áhrif Þess vegna að áætla uppfærslur varlega. Til dæmis, ef allar eignir eru auknar um 3 prósent á þriðjudegi og skrifstofuhúsgögn aukin um 4 prósent á föstudegi, skrifstofuhúsgögn hækka þá um samtals 7.12 prósent.

## <a name="scenario"></a>Aðstæður
Yfirmaðurinn biður um eftirfarandi breytingar á eignum:
-   Hækka endurnýjunarverð allra eigna, nema tölva, um 3.25 prósent.
-   Auka endurnýjunarverð allra húsgagna um 1 prósent til viðbótar.
-   Draga úr endurnýjunarverði og vátryggðu virði allra tölva um 10 prósent.

Gerðu eftirfarandi breytingar.
1.  Í skjámyndinni eignaflokkar, fyrir alla eignaflokka nema flokk skrifstofuhúsgagna og tölvuflokk, færirðu inn skal rita 3.25  í svæðinu  og þáttur endurnýjunarverðs reit og 0 í þáttur vátryggðs virðis reit.
2.  Fyrir flokk skrifstofuhúsgagna , færirðu inn skal rita 4.25  í svæðinu endurnýjunarverð  og 0 í þáttur vátryggðs virðis reit.
3.  Fyrir flokk tölvu , færirðu inn skal rita -10  í svæðinu endurnýjunarverð  og -10 í þáttur vátryggðs virðis reit.
4.  Í skjámyndinni Uppfæra endurnýjunarverð og tryggingarvirði er smellt á í lagi til að framkvæma endurútreikning allra eigna.

Næsta dag segir yfirmaðurinn að tölvurnar hafi dregist saman um 8 prósent í stað 10 prósenta, þannig að nauðsynlegt er að leiðrétta endurnýjunarverðin og tryggingarvirði. Hægt er að nota aðra hvora aðferðina til að leiðrétta villuna:
-   Handvirkt breyta Vátryggt virði og Endurnýjunarverðs svæðin í skjámyndinni eignir fyrir hverja eign í eignaflokki Tölva. Reikna og handvirkt færa inn gildin eins og upprunalega upphæðin hafi verið dregin saman um 8 prósent. Með þessari aðferð er ekki notuð skjámyndin Uppfæra endurnýjunarverð og vátryggð gildi.
-   Færið inn þætti endurnýjunarverðs og vátryggðs virðis fyrir tölvuflokk í reiti fyrir þætti endurnýjunarverðs og Vátryggðs virðis í skjámyndinni eignaflokkar. Þetta bæði endurstillir eignir aftur í upprunalegt verð (fyrir 10 prósenta minnkun) og notar 8 prósenta minnkun á upprunalegt gildi. Notaðu síðan skjámyndina Uppfæra endurnýjunarverð og tryggingarvirði til að endurreikna gildin eftir þáttum sem voru færðar inn.

> [!NOTE]  
> Ekki er hægt að bakfæra –10 stuðul með því að færa inn jákvæðan stuðul upp á 10 (eða stuðulinn 2, mismuninn á –10 og –8), vegna þess að upphæðirnar reiknast ekki eins og til er ætlast. 






