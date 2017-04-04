---
title: "Setja upp vöruúrval"
description: "Þessi skrá lýsir því hvað úrval er og útskýrir hvernig á að setja upp úrval í Microsoft Dynamics 365 aðgerða - Smásölu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 906fc6eb42eb54cb3a3d5621377f250f59de20d7
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-assortments"></a>Setja upp vöruúrval

Þessi skrá lýsir því hvað úrval er og útskýrir hvernig á að setja upp úrval í Microsoft Dynamics 365 aðgerða - Smásölu.

Úrval er safn tengdra afurða sem úthluta á smásölurásar stað og mortar verslun eða netverslun. Notið úrval til að auðkenna vörurnar sem eru tiltækar í hverri verslun. Úrval getur innihaldið tegundir afurða. Þess vegna, Allar afurðir sem eru tengdar valinni tegund eru með í úrvalinu. Úrval getur einnig innihaldið tilteknar vörur og tiltekinn afbrigði afurða. Með því að setja upp úrval er hægt að tengja þúsundum afurðir við smásölurásir samtímis , í hvaða samsetningu sem verslununum krefjast. Hægt er að setja upp eins mörg vöruúrval sem þú krefst. Hægt er að taka með hverja vöru í einni eða fleiri úrvali og hvert úrval er hægt að úthluta á einn eða fleiri smásölurásir. Til dæmis er geturðu skilgreint einn úrval sem inniheldur grunnsamsetningu afurða. Allar verslanir taka við þessu úrvali. Svo er er að skilgreina annað úrval sem inniheldur aðeins stóran íþróttabúnað. Aðeins stærri verslununum þínum fá úrvalið. Eftirfarandi skýringarmynd sýnir hvernig hægt er að úthluta afurðir í úrval, og hvernig þær úrvali geta tilheyrt smásölurásum. ![Vensl vöruúrvals](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Skilyrði
Áður en hægt er að setja upp úrval og úthluta henni til smásölurásar, verður að ljúka eftirfarandi verkum.

| Verkefni                              | Lýsing                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Setja upp smásölurás.          | Smásölurásir fela í sér verslunarhúsnæði, netverslanir og markaðstorg á netinu. Þú verður að setja upp að minnsta kosti eitt smásölurás og skilgreina valkosti fyrir verslunina. Úrval er úthlutað á verslanir til að auðkenna vörurnar sem fylgir ákveðna verslun.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Stofna stigveldi fyrirtækisins. | Eftir að setja upp smásölurása fyrir fyrirtækið, þarf að skilgreina smásölustigveldi fyrirtækisins sem táknar skipulag fyrirtækisins fyrir smásölurásir. Til dæmis getur stigveldi fyrirtækis verið notað fyrir úrval, áfyllingu eða skýrslugerð. Með því að bæta smásölurásum við stigveldi fyrirtækis, geturðu úthlutað vöruúrvali á verslunarhópa. Í stað þess að úthluta úrvalinu sérstaklega á hverja verslun, úthlutarðu úrvalið á hástigs fyrirtækishnúta. Svo í hvert sinn sem ný smásölurásar er bætt við fyrirtækishnúta á háu stigi, erfir sú smásölurásar sjálfkrafa allt úrval sem var úthlutað á fyrirtækishnút á hærra stigi. Þú getur tengt úrval aðeins við smásölurása sem eru innifaldar í stigveldi fyrirtækis sem er úthlutað á **smásöluúrvals** málefni. |
| Skilgreina afurðir.                  | Áður en hægt er að bæta vörum við úrvalið, verður að bæta þeim í Microsoft Dynamics AX. Hægt er að bæta afurðum handvirkt eða flytja þær frá lánardrottni. Þegar búið er að bæta við afurðum, þarf að losa þær á lögaðila. Aðeins afurðir sem hafa verið losaðar til lögaðila geta verið gerðar tiltækar á smásölurásum þínum. Afurðir sem enn hefur ekki verið losað til lögaðila er hægt að bæta við úrval og hægt er að samþykkja úrvalinu. Hinsvegar, þar til afurðir sem hafa verið losaðar til lögaðila geta þær ekki verið gerðar tiltækar á smásölurásunum.                                                                                                                                                                                                                                                                                     |
| Setja upp tegundastigveldi.      | Þegar retail vörur er hægt að flokka og flokka þær eftir með því að nota tegund stigveldi í Dynamics 365 fyrir Aðgerðir. Hægt er að stofna eina kjarnauppsetning stigveldis til að flokka öllum afurðum sem dreifa skal gegnum smásölurása. Einnig er hægt að stofna aðskildar, viðbótartegundastigveldi til að flokka afurðir fyrir sérstaka tilgangi, svo sem kynningartilboð eða í úrvali. Með því að nota tegundastigveldi er hægt að tengja allar afurðir í tiltekinni tegund við úrval. Allar afurðir sem bætt er við tegundina sem er tekin með í úrvalið er sjálfkrafa teknar með í úrvalið. Síðan, í næsta sinn sem verkraðari smásöluúrvals er keyrð, þessar afurðir verða tiltækar til smásölurása sem er tengdur við úrvalið.                                            |

## <a name="setting-up-an-assortment"></a>Setja upp vöruúrval.
Eftir að forkröfur er lokið er hægt að stofna úrval og úthluta á smásölurásir. Til að setja upp vöruúrval, Það verður að ljúka eftirfarandi verkum:

1.  Stofna nýtt vöruúrval eða afrita fyrirliggjandi vöruúrval
2.  Veljið smásölurása eða hástigs flokka af smásölurása sem úrvalið á við.
3.  Bæta afurðaflokka, stakar afurðir eða afurðarafbrigði við úrvali. Hægt er að taka með allar vörur í tiltekinni tegund, eða hægt er að útiloka valdar afurðir úr tegund sem er tekin með í úrvalið.
4.  Birta vöruúrval verkraðari smásöluúrvals er keyrður sjálfkrafa þegar úrval er birt. Þetta ferli myndar lista yfir afurðir. Síðan þegar þessu ferli er lokið verða þessar afurðir tiltækar til smásölurása sem er tengdur við úrvalið. Ef breytingar eru gerðar á úrval sem hefur verið birt eða á smásölurás sem úrvalinu er úthlutað á, þarf að uppfæra úrvalinu. Hægt er að keyra verkraðari smásöluúrvals sem runuvinnslu til að uppfæra úrvalinu þegar breytingar eru gerðar.



