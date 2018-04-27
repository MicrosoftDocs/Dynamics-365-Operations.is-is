---
title: Beinar afhendingar
description: "Þessi grein veitir upplýsingar um beinar afhendingar. Beinar afhendingar sendingar sem eru sendar beint frá lánardrottni til viðskiptavinar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1f2cdae674dc88a4d533258e24b1ecf7ec4cf55b
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="direct-deliveries"></a>Beinar afhendingar

[!INCLUDE [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um beinar afhendingar. Beinar afhendingar sendingar sem eru sendar beint frá lánardrottni til viðskiptavinar.

Beinar afhendingar sparar afhendingartíma og birgðakostnaður, vegna þess að þú þarft ekki að hafa afurðirnar í vöruhúsinu áður en þú sendir þær til viðskiptavinarins.  

Hægt er að stofna beinar afhendingar úr **sölupöntun**  síðu. Fyrst skal Stofna sölupöntun og pöntunarlínur Þá er farið í Aðgerðarúða og á flipann **sölupöntun** og smellt á **bein afhending** Að lokum, Tilgreina línur sem þarf að meðhöndla sem beina afhendingu. Tenging er núna stofnuð á milli sölupöntunarlínu fyrir beina afhendingu og samsvarandi innkaupapöntunarlína.  

**Athugasemd** Ef hluti af pöntuðu magni hefur þegar verið afhent, verður að skipta eftirstandandi magn. Stofna nýja línu með því magni sem þarf að afhenda beint og draga það magn af magninu í upphaflegu línunni. Til dæmis, ef upphaflega magnið var 15 og fimm hafa verið afhent, verður að stofna nýja línu fyrir eftirstöðvar 10 og minnka upphaflegt magn um þá upphæð.  

Eftir að búið er að stofna beina afhendingartengilinn á milli sölupöntunarlínanna og innkaupapöntunarinnar er hægt að uppfæra sölupöntun með fylgiseðli. Keyra annað hvort fylgiseðilsuppfærslu eða reikningsuppfærslu úr innkaupapöntuninni. Þú þarft að reikningsfæra sölupöntun úr **sölupöntun** skjámynd. Uppfærsla reiknings má ekki valda því að magnið á sölupöntun verði meira magn en það magn sem hefur verið skráð sem móttekið. Til dæmis sölupöntunarlínu er með 10 stykki, en aðeins fimm hlutar úr sölupöntunarlínu hafa verið uppfærðar með fylgiseðli. Ef valið er **allt** í á **magn** listanum þegar þú uppfærir reikning sölupöntunar, einungis þær vörur sem hafa verið efnislega mótteknar, eða uppfærðar með fylgiseðli, eru reikningsuppfærðar. Heila sölupöntunarlínunni er ekki uppfærð.

## <a name="delivery-date"></a>Afhendingardagsetning
þegar svæðið **umbeðin móttökudagsetning** á sölupöntunarlína er uppfært eru svæðin **afhendingardagur** og  á samsvarandi sölupöntunarlínum einnig uppfærð. Á sama hátt þegar svæðið **staðfesta** á innkaupapöntunarlínunni er uppfært eru svæðin **staðfest móttökudagsetning** og **staðfest sendingardagsetning** á samsvarandi sölupöntunarlínum einnig uppfærð.

## <a name="delivery-address"></a>Afh.aðsetur
Yfirleitt er afhendingaraðsetur fyrir innkaupapöntun aðsetur fyrirtækisins. Hins vegar þegar bein afhending er stofnuð er aðsetur viðskiptavinarins fært inn sem afhendingaraðsetrið. Ef afhendingaraðsetrinu á innkaupapöntunarlínu af afhendingargerðinni **bein afhending** er breytt er afhendingaraðsetur fyrir samsvarandi sölupöntunarlínu líka uppfært. Á sama hátt er það svo að ef afhendingaraðsetrinu á sölupöntunarlínunni er breytt er afhendingaraðsetrið á innkaupapöntunarlínunni einnig uppfært.

## <a name="deleting-order-lines"></a>Eyða pantanalínum
Reynirðu að eyða sölupöntunarlínu sem hefur afhendingargerðina **bein afhending**, er skilaboð birt sem segir að sölupöntunarlínur eru tengdar línunni. Ef búið er að afhenda sölupöntunarlínuna að hluta til er hvorki hægt að eyða sölupöntunarlínunni né innkaupapöntunarlínum sem eru tengdar henni.

## <a name="warehouse"></a>Vöruhús
Þegar bein afhending er stofnuð berast vörur sem eru seldar aldrei í vöruhússið. Hins vegar enn verður að tilgreina vöruhús á sölupöntunarlínunni. Á sama hátt eru tiltektarkröfur kannski tilgreindar í vörulíkanaflokkur fyrir vöru. Hins vegar vegna þess að vörurnar berast aldrei efnislega í vöruhúsi fyrirtækisins, eru þessar kröfur hunsaðar þegar sölupöntunin er bein afhending.




