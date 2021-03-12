---
title: Endurreikna endurnýjunarverð og vátryggt virði fyrir eignaflokka
description: Þessi grein útskýrir ferlið að uppfæra endurnýjunarverð og vátryggt virði fyrir eignir.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66f51a513524cfad7fb5382efa748197f9b4bac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990515"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Endurreikna endurnýjunarverð og vátryggt virði fyrir eignaflokka

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir ferlið að uppfæra endurnýjunarverð og vátryggt virði fyrir eignir.

Reglulega geta komið tilkynningar um að kostnaðurinn við að skipta út eða tryggja tiltekna eign hafi breyst. Til dæmis gæti yfirmaður tilkynnt að verðbólgan hafi verð 3 prósent á síðasta ári, þannig að nauðsynlegt væri að hækka endurnýjunarverð allra eigna um 3 prósent. 

Þótt þú getir breytt endurnýjunarverði og vátryggðu virði einstakra eigna á síðunni **Eignir** geturðu notað síðuna **Uppfæra endurnýjunarverð og vátryggt virði** til að uppfæra þessi gildi fyrir heilan flokk af eignum á sama tíma. Þessar upplýsingar lýsa því hvernig uppfæra eigi gildi fyrir eignaflokka eða fyrir tilteknar eignir í flokkana.

## <a name="how-values-are-updated"></a>Hvernig gildi eru uppfærð
Ef endurreikna á endurnýjunarverð og vátryggð virði eigna, verður fyrst að tilgreina hlutfall breytingarinnar á endurnýjunarverðum og vátryggðu virði sem fyrir eru, og framkvæma svo reglubundnu uppfærsluna til að raunverulega endurreikna gildin. Þú tilgreinir prósentuna í svæðunum **Stuðull endurnýjunarverðs** og **Stuðull vátryggðs virðis** á síðunni **Eignaflokkar**. Þótt þú tilgreinir þessa stuðla fyrir eignaflokkinn, þegar þú notar síðuna **Uppfæra endurnýjunarverð og vátryggt virði**, getur þú valið að endurreikna endurnýjunarverð og vátryggt virði fyrir aðeins tilteknar eignir í flokki. 

Þegar þú notar síðuna **Uppfæra endurnýjunarverð og vátryggt virði** til að endurreikna endurnýjunarverð og vátryggt virði eignanna eru eftirfarandi formúlur notuð:

-   \[(Stuðull endurnýjunarverðs eignaflokks / 100) + 1\] \* Núverandi endurnýjunarverð eignar
-   \[(Stuðull vátryggðs virðis eignaflokks / 100) + 1\] \* Núverandi vátryggt virði eignar

> [!NOTE] 
> Þegar þú notar síðuna **Uppfæra endurnýjunarverð og vátryggt virði** eru bæði endurnýjunarverð og vátryggt virði uppfærð fyrir valdar eignir; þú getur ekki tilgreint að aðeins eitt gildi verði uppfært. Ef skilja á eftir eitt gildi óbreytt og uppfæra annað gildi skaltu færa inn 0 (núll) sem stuðul á síðunni **Eignaflokkar**. Auður stuðull eða með núllgildi velur því að útreikningnum er sleppt í uppfærslu. Reglubundna uppfærslan hefur engin áhrif á bókfært verð og nettó bókfært verð eigna. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a>Hvernig nota á dagsetningu til að velja hvaða atriði á að uppfæra
Sjálfgefið uppfærir uppfærsluferlið valdar eignir sem ekki hafa verið uppfærðar á gildandi degi, en hafa ef til vill verið uppfærðar á undanförnum dögum. Til dæmis þýðir &lt; núverandi dagsetning "fyrir daginn í dag." Hægt er að breyta dagsetningunni á síðunni **Uppfæra endurnýjunarverð og vátryggt virði** með því að smella á hnappinn **Velja**. Dagsetningarskilyrðið sem ertilgreint er borið saman við dagsetninguna á síðustu reglubundnu uppfærslu á eigninni (**Síðasta reglubundna gildið/kostnaðaruppfærsla** svæðið á síðunni **Eignir**). Hvert sinn sem tekist hefur að uppfæra endurnýjunarverð og vátryggt virði fyrir eign, uppfærir kerfið sjálfkrafa svæðið **Síðasta reglubundna gildið/kostnaðaruppfærsla** núgildandi dagsetningu. 

Dæmi 

Þú Uppfærðir endurnýjunarverð farartækja, skrifstofuhúsgagna, og byggingaflokka um 5 prósent í gær, og er nú litið á þessar eignir sem rétt uppfærðar. Ef útiloka á þessar eignir þegar allar aðrar eignir eru uppfærðar í dag, er dagsetning færð inn í svæðið **Síðasta reglubundna gildið/kostnaðaruppfærsla** sem er á undan gærdeginum (&lt; dagsetning gærdagsins) vegna þess að síðasta uppfærslan fyrir flokkana **Farartæki**, **Skrifstofuhúsgögn** og **Byggingar** átti sér stað utan dagsetningarskilyrðisins sem fært var inn.

## <a name="cumulative-effect-of-each-update"></a>Uppsöfnuð áhrif hverrar uppfærslu
hver uppfærslu er með Uppsöfnuð áhrif Þess vegna að áætla uppfærslur varlega. Til dæmis, ef allar eignir eru auknar um 3 prósent á þriðjudegi og skrifstofuhúsgögn aukin um 4 prósent á föstudegi, skrifstofuhúsgögn hækka þá um samtals 7.12 prósent.

## <a name="scenario"></a>Aðstæður
Yfirmaðurinn biður um eftirfarandi breytingar á eignum:
-   Hækka endurnýjunarverð allra eigna, nema tölva, um 3.25 prósent.
-   Auka endurnýjunarverð allra húsgagna um 1 prósent til viðbótar.
-   Draga úr endurnýjunarverði og vátryggðu virði allra tölva um 10 prósent.

Gerðu eftirfarandi breytingar.
1.  Á síðunni **Eignaflokkar** fyrir alla eignaflokka nema flokkinn **Skrifstofuhúsgögn** og flokkinn **Tölvur**, skaltu færa inn 3,25 í svæðið **Stuðull endurnýjunarverðs** og 0 í svæðið **Stuðull vátryggðs virðis**.
2.  Fyrir flokkinn **Skrifstofuhúsgögn** skaltu færa inn 4,25 í svæðið **Stuðull endurnýjunarverðs** og 0 í svæðið **Stuðull vátryggðs virðis**.
3.  Fyrir flokkinn **Tölvur** skaltu færa inn -10 í svæðið **Stuðull endurnýjunarverðs** og -10 í svæðið **Stuðull vátryggðs virðis**.
4.  Á síðunni **Uppfæra endurnýjunarverð og vátryggt virði** skaltu smella á **Í lagi** til að framkvæma endurútreikning á öllum eignum.

Næsta dag segir yfirmaðurinn að tölvurnar hafi dregist saman um 8 prósent í stað 10 prósenta, þannig að nauðsynlegt er að leiðrétta endurnýjunarverðin og tryggingarvirði. Hægt er að nota aðra hvora aðferðina til að leiðrétta villuna:
-   Breyttu handvirkt svæðunum **Vátryggt virði** og **Endurnýjunarverð** á síðunni **Eignir** fyrir hverja eign í eignaflokknum **Tölvur**. Reikna og handvirkt færa inn gildin eins og upprunalega upphæðin hafi verið dregin saman um 8 prósent. Með því að nota þessa aðferð notarðu ekki síðuna **Uppfæra endurnýjunarverð og vátryggt virði**.
-   Sláðu inn stuðla endurnýjunarverðs og vátryggðs virði fyrir hópinn **Tölvur** í svæðunum **Stuðull endurnýjunarverðs** og **Stuðull vátryggðs virðis** á síðunni **Eignaflokkar**. Þetta bæði endurstillir eignir aftur í upprunalegt verð (fyrir 10 prósenta minnkun) og notar 8 prósenta minnkun á upprunalegt gildi. Notaðu síðan síðuna **Uppfæra endurnýjunarverð og vátryggt virði** til að endurreikna gildin, byggt á stuðlunum sem þú færðir inn.

> [!NOTE]  
> Ekki er hægt að bakfæra –10 stuðul með því að færa inn jákvæðan stuðul upp á 10 (eða stuðulinn 2, mismuninn á –10 og –8), vegna þess að upphæðirnar reiknast ekki eins og til er ætlast. 





