---
title: Setja upp vöruúrval
description: Þessi grein lýsir því hvað vöruúrval er og útskýrir hvernig á að setja upp vöruúrval í Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26614d319453041177e8072793f09f52ebfd51fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022931"
---
# <a name="set-up-assortments"></a>Setja upp úrval

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvað vöruúrval er og útskýrir hvernig á að setja upp vöruúrval í Dynamics 365 Commerce.

Úrval er safn tengdra afurða sem úthlutað er á viðskiptarás, eins og verslun á staðnum eða netverslun. Notið úrval til að auðkenna vörurnar sem eru tiltækar í hverri verslun. Úrval getur innihaldið tegundir afurða. Þess vegna, Allar afurðir sem eru tengdar valinni tegund eru með í úrvalinu. Úrval getur einnig innihaldið tilteknar vörur og tiltekinn afbrigði afurða. Með því að setja upp úrval er hægt að tengja þúsundum afurðir við rásir samtímis , í hvaða samsetningu sem verslununum krefjast. Hægt er að setja upp eins mörg vöruúrval sem þú krefst. Hægt er að taka með hverja vöru í einni eða fleiri úrvali og hvert úrval er hægt að úthluta á einn eða fleiri rásir. Til dæmis er geturðu skilgreint einn úrval sem inniheldur grunnsamsetningu afurða. Allar verslanir taka við þessu úrvali. Svo er er að skilgreina annað úrval sem inniheldur aðeins stóran íþróttabúnað. Aðeins stærri verslununum þínum fá úrvalið. Eftirfarandi skýringarmynd sýnir hvernig hægt er að úthluta afurðir í úrval, og hvernig þær úrvali geta tilheyrt rásum.

![Vensl vöruúrvals](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að setja upp úrval og úthluta henni til viðskiptarásar, verður að ljúka eftirfarandi verkum.

| Verk                              | Lýsing |
|-----------------------------------|-------------|
| Setja upp rás.          | Rásir fela í sér verslunarhúsnæði, netverslanir og markaðstorg á netinu. Þú verður að setja upp að minnsta kosti eina rás og skilgreina valkosti fyrir verslunina. Úrval er úthlutað á verslanir til að auðkenna vörurnar sem fylgir ákveðna verslun. |
| Stofna stigveldi fyrirtækisins. | Eftir að setja upp viðskiptarása fyrir fyrirtækið, þarf að skilgreina stigveldi fyrirtækis sem táknar skipulag fyrirtækisins fyrir rásir. Til dæmis getur stigveldi fyrirtækis verið notað fyrir úrval, áfyllingu eða skýrslugerð. Með því að bæta rásum við stigveldi fyrirtækis, geturðu úthlutað vöruúrvali á verslunarhópa. Í stað þess að úthluta úrvalinu sérstaklega á hverja verslun, úthlutarðu úrvalið á hástigs fyrirtækishnúta. Svo í hvert sinn sem nýrri rás er bætt við fyrirtækishnúta á háu stigi, erfir sú rás sjálfkrafa allt úrval sem var úthlutað á fyrirtækishnút á hærra stigi. Þú getur tengt úrval aðeins við rásir sem eru innifaldar í stigveldi fyrirtækis sem er úthlutað á tilganginn **Viðskiptaúrval**. |
| Skilgreina afurðir.                  | Áður en hægt er að bæta vörum við úrvalið, verður að bæta þeim í Commerce. Hægt er að bæta afurðum handvirkt eða flytja þær frá lánardrottni. Þegar búið er að bæta við afurðum, þarf að losa þær á lögaðila. Aðeins afurðir sem hafa verið losaðar til lögaðila geta verið gerðar tiltækar á rásum þínum. Afurðir sem enn hefur ekki verið losað til lögaðila er hægt að bæta við úrval og hægt er að samþykkja úrvalinu. Hinsvegar, þar til afurðir sem hafa verið losaðar til lögaðila geta þær ekki verið gerðar tiltækar á rásunum. |
| Setja upp tegundastigveldi.      | Þegar viðskiptaafurðir eru stofnaðar, er hægt að flokka þær með því að nota tegundarstigveldi eiginleika. Hægt er að stofna eina kjarnauppsetning stigveldis til að flokka öllum afurðum sem dreifa skal gegnum rásir. Einnig er hægt að stofna aðskildar, viðbótartegundastigveldi til að flokka afurðir fyrir sérstaka tilgangi, svo sem kynningartilboð eða í úrvali. Með því að nota tegundastigveldi er hægt að tengja allar afurðir í tiltekinni tegund við úrval. Allar afurðir sem bætt er við tegundina sem er tekin með í úrvalið er sjálfkrafa teknar með í úrvalið. Síðan, í næsta sinn sem verkraðari viðskiptaúrvals er keyrð, þessar afurðir verða tiltækar til rása sem er tengdur við úrvalið. |

## <a name="setting-up-an-assortment"></a>Setja upp vöruúrval.

Eftir að forkröfur er lokið er hægt að stofna úrval og úthluta á rásir. Til að setja upp vöruúrval, Það verður að ljúka eftirfarandi verkum:

1. Stofna nýtt vöruúrval eða afrita fyrirliggjandi vöruúrval
2. Veljið rásir eða hástigs flokka af rása sem úrvalið á við.
3. Bæta afurðaflokka, stakar afurðir eða afurðarafbrigði við úrvali. Hægt er að taka með allar vörur í tiltekinni tegund, eða hægt er að útiloka valdar afurðir úr tegund sem er tekin með í úrvalið.
4. Birta vöruúrval Verkraðari úrvals er keyrður sjálfkrafa þegar úrval er birt. Þetta ferli myndar lista yfir afurðir. Síðan þegar þessu ferli er lokið verða þessar afurðir tiltækar til rása sem er tengdur við úrvalið. Ef breytingar eru gerðar á úrval sem hefur verið birt eða á rás sem úrvalinu er úthlutað á, þarf að uppfæra úrvalinu. Hægt er að keyra verkraðari úrvals sem runuvinnslu til að uppfæra úrvalinu þegar breytingar eru gerðar.
