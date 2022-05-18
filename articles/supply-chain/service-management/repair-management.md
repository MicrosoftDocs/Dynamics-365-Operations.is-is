---
title: Viðgerðarstjórnun
description: Flokkaðu vandamál á kerfisbundinn hátt til auðvelda tillögur að lausnum sem hafa gengið vel áður.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f969224f48cdb1f12b48b9f5d839d7c88168e87d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674254"
---
# <a name="repair-management"></a>Viðgerðarstjórnun       

[!include [banner](../includes/banner.md)]


Fyrir viðgerðarstjórnun geturðu flokkað vandamál kerfisbundið. Þetta er til að hjálpa með tillögur að lausnum sem hafa gengið vel áður.

Þú setur upp stillingar einkenna, greiningar og úrlausnar. Hægt er að nota þær allar seinna þegar þú færð svipaða vöru til viðgerðar. Þú getur einnig sett upp viðgerðarstig sem geta fylgst með framvindu viðgerðarverkefnis.

## <a name="setting-up-repair-management"></a>Uppsetning viðgerðarstjórnar

Notaðu eftirfarandi skjámyndir uppsetningar til að slá inn upplýsingar sem nota skal til að tilgreina einkenni, greiningu og úrlausn viðgerðar.

- Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Skilyrði**.
- Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Einkennasvæði**.
-  Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Greiningarsvæði**.
- Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Úrlausnir**.
- Veljið **Þjónustustjórnun** \> **Uppsetning** \> **Viðgerð** \> **Viðgerðarstig**.

## <a name="symptoms-and-conditions"></a>Einkenni og skilyrði

Einkenni eru hvernig viðskiptavinurinn lýsir vandamálinu. Einkenni eru athuganir viðskiptavinar sem gefa til kynna þörf fyrir viðgerð.

Hægt er að setja upp einkennasvæði, einkennakóða og skilyrði. Einkennasvæðið nær yfir bilunarþáttinn og einkenniskóðinn nær yfir bilunareinkennin. Skilyrðin lýsa kringumstæðum eða umhverfi sem er til staðar þegar vandamálið kemur fram.

**Dæmi**

Komið er með tölvu í viðgerð vegna þess að harði diskurinn bilar eftir langan notkunartíma. Bilun á harða disknum veldur villu með bláum skjá. Tæknimaðurinn sem fær tölvuna færir inn eftirfarandi einkenni og skilyrði:

1.  Einkennasvæðið er harði diskurinn

2.  Einkennakóðinn er villan með bláum skjá

3.  Skilyrðin eru að diskurinn bilar eftir langvarandi notkun

## <a name="diagnosis-and-resolutions"></a>Greining og lausnir

Svæðin greining og lausnir eru yrðingar frá sjónarhorni viðgerðarinnar. Þetta eru skrefin sem tæknimaður fór í gegnum til þess að kanna vandamálið.

Greiningarsvæðið nær yfir aðgerðina sem verður að eiga sér stað til þess að leysa viðfangsefnið. Greiningarkóðinn sýnir hvernig vandamálið var meðhöndlað og lausn vandamálsins gæti falist í viðgerð vöru, að henni sé skipt út eða því að viðskiptavinur hætti við pöntunina. Til dæmis, ef gert er við tölvuna, gæti greiningarsvæðið verið „gallaður hluti“, greiningarkóðinn gæti verið „nýtt skjákort sett upp“ og úrlausnin gæti verið „skipt um“.

## <a name="repair-stages"></a>Viðgerðarstig

Viðgerðarstig taka fram hver framvindan er í viðgerðarferlinu. Viðgerðarstigið er með útskráningarfæribreytuna **Lokið** sem gefur til kynna að viðgerðarlínunni sé lokið og lokadagsetning og tími hefur verið skráður.

## <a name="applying-repair-management"></a>Notkun viðgerðarstjórnunar

Til þess að nota viðgerðarstjórnun á vöru, verður að setja vöruna upp með þjónustuhlutatengslum í þjónustupöntuninni. Úr þjónustupöntuninni er síðan hægt að stofna viðgerðarlínu með upplýsingum um núverandi verkefni. Í viðgerðarlínunni er þjónustuhluturinn sem er í viðgerð síðan skilgreindur og upplýsingar gefnar um einkenni, greiningu og framkvæmd. Einnig er hægt að stofna athugasemd í viðgerðarlínuna.

Hægt er að stofna viðhaldslínur fyrir hvert skref í viðgerðarferlinu.

## <a name="create-a-repair-line-on-a-service-order"></a>Stofna viðgerðarlínu í þjónustupöntun.

1.  Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.

2.  Veljið þjónustupöntunina með þjónustuhlutnum sem þarfnast viðgerðar.

3.  Veljið **Viðgerð** \> **Viðgerðarlínur** til að opna skjámyndina **Viðgerðarlínur**.

4.  Veljið **Nýtt** til að stofna nýja línu.

5.  Velja þjónustuhlut. Hægt er að velja hvaða þjónustuhlut sem settur hefur verið upp með hlutatengslum í þjónustupöntuninni.

6.  Veldu eitthvað af forstilltum einkennum, greiningum og framkvæmdargildi sem eru viðeigandi í viðgerðarlínunni og veldu síðan flipann **Athuga** til að búa til minnismiða á viðgerðarlínunni, ef þörf krefur.

7.  Veljið **Vista** til að vista nýju viðgerðarlínuna. Reiturinn **Stofna dagsetningu og tíma** á flipanum **Almennt** í skjámyndinni **Viðgerðarlínur** er uppfærður þegar vistun á sér stað.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>Að fylgjast með framvindu og finna úrlausn á viðgerðarverkefni

Hægt er að stilla viðgerðarstig viðgerðarlínu til að fylgjast með framvindu viðgerðarinnar.

Þegar viðgerðarverkefni er leyst er hægt að loka viðgerðarlínunni. Setjið viðgerðarstigið á stig með **Lokið** eiginleikann virkan. Núverandi dagsetning og tími er skráður sem tími viðgerðarloka í línuna.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Loka viðgerðarlínu fyrir leyst verkefni

1.  Opnaðu skjámyndina **Viðgerðarlínur**. Fylgdu ferlinu fyrr í þessu efnisatriði til að búa til viðgerðarlínu.

2.  Velja viðgerðarlínu með viðgerðarverkefni sem ætlunin er að loka.

3.  Í reitnum **Viðgerðarsvið** skal velja stig með eiginleikann **Lokið** virkan.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]