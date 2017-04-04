---
title: "Fella niður, endurskipa eða bakfæra vaxtagjöld"
description: "Þessi grein útskýrir hvernig skal fella niður, endurskipa, og bakfæra gjald fyrir vextir og gjöld."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 25c2f85298bb89cb2802c7f0f7ff632c08aeca8f
ms.lasthandoff: 03/31/2017


---

# <a name="waive-reinstate-or-reverse-interest-fees"></a>Fella niður, endurskipa eða bakfæra vaxtagjöld

Þessi grein útskýrir hvernig skal fella niður, endurskipa, og bakfæra gjald fyrir vextir og gjöld.

Hægt er að nota hnappana í **Sækja**flipanum á **Allir viðskiptavinir** listasíðu til að fella niður, bakfæra eða virkja gjöld:

-   Niðurfelld gjöld eru látin gleymd. Hægt að fella niður gjald ef til dæmis viðskiptavinur hefur ágreining um gjaldið, og óskað er að halda góðum viðskiptatengslum við viðskiptavininn.
-   Virkjuð gjöld komast aftur á gjalddaga. Hægt er að virkja gjöld sem áður voru felld niður. Það gæti þurft að endurskipa gjöld ef ákveðið er að þau ættu ekki að hafa verið felld niður.
-   Bakfærð gjöld eru fjarlægð úr reikningi viðskiptavinar, og eru ekki lengur á gjalddaga. Það getur þurft að bakfæra gjöld ef, til dæmis, valin var röng vaxtaprósenta til að reikna upphæðina sem viðskiptavinur skuldar. Hægt er að nota aðskilið ferli til að endurreikna vexti og búa til vaxtanótu með nýjum gjöldum fyrir viðskiptavininn.

Allar þessar aðgerðir breyta vaxtanótu. Vaxtanóta er viðskiptaskjal sem tilkynnir viðskiptavini þegar vextir eða gjöld hafa verið gjaldfærð á reikning þeirra. Þegar fellt er niður eða bakfært vextir eða gjöld, er kreditnóta eða leiðréttingarreikning sjálfkrafa stofnuð til að jafna gjöld. Ef virkja á niðurfelld gjöld, er stofnaður sjálfkrafa reikningur með debetupphæð til að virkja gjöldin sem viðskiptavinurinn skuldar. Eftirfarandi upplýsingar lýsa niðurstöðum hverrar aðgerðar.

| Aðgerð                                                                                                                                                                                                            | Niðurstaða fyrir viðskiptavininn                                                                                             | Ferli                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fella niður heilar vaxtanótur með öllum vöxtum og gjöldum sem þær innihalda. -eða- Velja og fella niður gjöld eða vaxtafærslur sem eru hluti af vaxtanótum.                                        | Gjöldin eru látin gleymd.                                                                                           | Kreditnóta eða leiðréttingarreikningur eru stofnuð fyrir viðskiptavininn. Kreditnóta°er notuð til að jafna sjálfkrafa vaxtanótuna, eða vaxtafærslurnar eða gjöldin sem voru valin. Jöfnuð upphæð er jöfn heildarupphæð gjalda, mínus fyrri greiðslur viðskiptavinar, og mínus allar upphæðir sem áður voru felldar niður eða afskrifaðar. Ef upphæð kreditnótu er hærri en viðskiptavinurinn skuldar, er hægt að umbreyta kreditnótu í reikning lánardrottins. Síðan er hægt að endurgreiða viðskiptavininum.                                                       |
| Fella niður heilar vaxtanótur með öllum vöxtum og gjöldum sem þær innihalda. -eða- Velja og endurskipa gjöld eða vaxtafærslur sem eru hluti af vaxtanótum.                                | Niðurfellda upphæðin er gjaldfallin aftur.                                                                                     | Reikningur með debetupphæð er stofnaður, og upphæðin er sjálfkrafa jöfnuð á móti gjöldunum sem áður voru felld niður. Raunverulegar vaxtanótur eru ekki endurskipaðar. Þess í stað er reikningur búinn til sem sýnir upphæðina sem gjaldfellur frá viðskiptamanni. Kreditnótur, eða leiðréttingarreikningar, sem stofnuð voru til að jafna niðurfelldar vaxtanótur geta enn verið til ef þau voru ekki notuð til að jafna vaxtanótur.. Þegar það gerist eru útistandandi kreditnótur ógiltar. Útistandandi kreditnótur eru oftast sjálfkrafa jafnaðar þegar vaxtanótur eru felldar niður. Hins vegar gæti útistandandi kreditnóta verið til ef viðskiptavinur greiddi vaxtanótu, jafnvel þótt viðskiptavinur hafi uppi ágreining um gjöldin. |
| Bakfæra heilar vaxtanótur. -eða- Bakfæra valdar vaxtafærslur sem eru hluti af vaxtanótum. **Athugið:** Ekki er hægt að bakfæra þóknun. Hins vegar er hægt að bakfæra heila vaxtanótu sem inniheldur þóknun. | Gjöldin eru ekki lengur á gjalddaga frá viðskiptamanni. Hins vegar gjaldfalla gjöld aftur ef vextir eru endurreiknaðir. | Ferlið er það sama og við niðurfellingu vaxtanóta eða valdar vaxtafærslur. Kreditnóta eða leiðréttingarreikningur eru stofnuð fyrir viðskiptavininn. Þessi kreditnóta er notuð til að jafna sjálfkrafa vaxtanótuna. Hægt er að nota aðskilið ferli til að endurreikna vexti og stofna nýja vaxtanótu.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Einnig er hægt að nota aðskilinn ferli til að afskrifa skuldir gallað. Þetta ferli merkir allar viðskiptavinafærslur til jöfnunar í stað þess að fella aðeins niður gjöld sem eru hluti af vaxtanótum.

## <a name="adjust-interest-for-invoices"></a>Leiðrétta vexti fyrir reikninga
Auk þess að leiðrétta vaxtanótur, er hægt að fjarlægja°vaxtagjöld á reikningum með því að°nota eitt af eftirfarandi ferlum. Bæði ferlin gera einnig leiðréttingar á tengdum vaxtanótum.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Leiðrétta reikning með tengda vexti

Hægt er að°leiðrétta bókaðan reikning sem er innifalinn í vaxtanótu. Þetta ferli afritar upplýsingar úr fyrirliggjandi reikningi í nýjan til að gera eingöngu þær leiðréttingar sem notandi vill. Reikningurinn er afturkallaður og nýr stofnaður. Vextir á færsluna eru einnig bakfærðir á vaxtanótu, ef vaxtanóta var bókuð. 

Hægt er að gera leiðréttingu með því að nota **Leiðrétta reikning** hnapp á Aðgerðarúðu textareikningsins. Þessi hnappur er bara tiltækur ef **Leiðrétta textareikning** skilgreiningarlykill er valinn.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Bakfæra viðskiptavinafærslu með tengda vexti

Hægt er að nota þetta ferli til að bakfæra viðskiptavinafærslu á reikningi, þegar reikningurinn var stofnaður á rangan hátt. Ef bakfærða viðskiptavinarfærslan hefur vexti á vaxtanótu, og vaxtanótan var bókuð eru vextir á færsluna einnig bakfærðir á vaxtanótu. Hætt er við vaxtanótuna ef hún hefur ekki verið bókuð. 

Hægt er að bakfæra færslur viðskiptavinar°með því að nota **Bakfæra **hnappinn á **Viðskiptavinafærslur** síðu.

## <a name="waive-or-reinstate-interest-notes"></a>Fella niður eða endurskipa vaxtanótur
Hægt er að fella niður eða endurskipa öll gjöld á vaxtanótum sem valdar voru. Þegar gjöld eru felld niður, getur heildarupphæðin sem á að fella niður ekki verið hærri en upphæðartakmörk sem hafa verið valin. Hægt er að endurskipa vaxtanótu eingöngu ef hún var felld niður. 

Hægt er að fella niður eða endurskipa vaxtanótur með því að nota **Vaxtanótu** hnappinn í **Safna** flipanum á **Viðskiptavinar** síðu.

## <a name="waive-or-reinstate-interest-transactions"></a>Fella niður eða endurskipa vaxtafærslur
Hægt er að fella niður eða endurskipa tilteknar vaxtafærslur á vaxtanótu í stað þess að leiðrétta öll gjöld á vaxtanótunni. Þegar gjöld eru felld niður, getur heildarupphæðin sem á að fella niður ekki verið hærri en upphæðartakmörk sem hafa verið valin. Hægt er að endurskipa vaxtafærslu eingöngu ef hún var felld niður. 

Hægt er að fella niður eða endurskipa vaxtanótur með því að nota°**Vaxtanótu**°hnappinn á **Safna** flipanum á **Viðskiptavinar** síðu.

## <a name="waive-or-reinstate-fees"></a>Fella niður eða endurskipa gjöld
Hægt er að fella niður eða endurskipa tiltekin gjöld á vaxtanótu í stað þess að leiðrétta öll gjöld á vaxtanótunni. Þegar gjöld eru felld niður, getur heildarupphæðin sem á að fella niður ekki verið hærri en upphæðartakmörk sem hafa verið valin. Hægt er að endurskipa gjöld eingöngu ef þau voru felld niður. 

Hægt er að fella niður eða endurskipa vaxtanótur með því að nota°**Gjald**°hnappinn á **Safna** flipanum á **Viðskiptavinar** síðu.

## <a name="reverse-interest-notes"></a>Bakfæra vaxtanótur
Hægt er að bakfæra öll gjöld á vaxtanótur sem valdar voru. Bakfærð gjöld eru fjarlægð úr reikningi viðskiptavinar, og eru ekki lengur á gjalddaga. Eftir að vaxtanóta er bakfærð er hægt er að endurreikna vexti og stofna nýja vaxtanótu. 

Hægt er að bakfæra vaxtanótur með því að nota°**Vaxtanótu** hnappinn í **Safna** flipanum á **Viðskiptavinar** síðu.

## <a name="reverse-interest-transactions"></a>Bakfæra vaxtafærslur
Hægt er að bakfæra allar vaxtafærslur sem valdar eru. Bakfærð gjöld eru fjarlægð úr reikningi viðskiptavinar, og eru ekki lengur á gjalddaga. Eftir að færslurnar eru bakfærðar er hægt er að endurreikna vexti og stofna nýja vaxtanótu.

Hægt er að bakfæra vaxtanótur með því að°nota **vaxtanótu** hnappinn í **Safna** flipanum á **Viðskiptavinar** síðu.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Skoða sögu leiðréttinga fyrir gjöld sem voru felld niður, endurskipuð, eða bakfærð.
Hægt er að skoða nákvæma sögu leiðréttinga sem gerðar voru fyrir vaxtanótur, eins og notandann sem stofnaði leiðréttinguna, gerð leiðréttingar, upphæðina, og hvenær leiðrétting var færð inn. Til dæmis gæti þurft að skoða fyrri leiðréttingar sem voru færðar inn fyrir vaxtanótu áður en ný vaxtanóta er stofnuð. 

Hægt er að bakfæra vaxtanótur með því að nota°**Saga** hnappinn í **Safna** flipanum á **Viðskiptavinar** síðu.


