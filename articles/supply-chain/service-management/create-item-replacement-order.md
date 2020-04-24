---
title: Stofnun skiptipöntunar vöru
description: Vöruskilapantanir eru yfirleitt stofnaðar eftir að vöru hefur verið skilað eftir skoðun.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b92c4400f2c852af49c78e9e94fdffa2e498b45c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202883"
---
# <a name="create-an-item-replacement-order"></a>Stofnun skiptipöntunar vöru 

[!include [banner](../includes/banner.md)]


Vöruskilapantanir eru yfirleitt stofnaðar eftir að vöru hefur verið skilað eftir skoðun. Hins vegar, ef nauðsynlegt er að skipta út vöru áður en henni hefur verið skilað, eða ef upprunalegu vörunni verður ekki skilað, er hægt að stofna vöruskiptapöntun um leið og búið er að stofna skilapöntun.

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a>Stofna skal skiptipöntun eftir að skilavara hefur verið móttekin

1.  Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.

2.  Búðu til nýtt skilapöntun, eða veldu skilapöntun frá listanum til að opna **Skilapöntun - RMA númer: %1, %2** skjámynd.

3.  Smelltu á **Skilalína** og veldu síðan **Skiptivara**.

4.  Veljið vöruna sem á að skipta út skilavörunni með. Færa skal inn nákvæma skilgreiningu og smella síðan á **Nota**.

5.  Smelltu á **Fylgiseðill** til að búa til fylgiseðill fyrir skilapöntunina. Sölupöntun er mynduð fyrir skiptivöruna sem var valin.
    
    Eftir að sölupöntunin er búin til fyrir skilavöruna er sölusamninga sjálfkrafa leitað og ef sölusamningur er fyrir hendi er hann settur á sölupöntunina.

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a>Stofna skal skiptipöntun áður en þú móttekur vöru sem verður skilað

1.  Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.

2.  Búðu til nýja skilapöntun, eða veldu skilapöntun af listanum til að opna skjámyndina **Skilapöntun - RMA númer: %1, %2**.

3.  Smelltu á **Finna sölupöntun** ef þú vilt auðkenna sölupöntun fyrir skilavörunni. Fylla út í **Finna sölupöntun** skjámynd og smelltu síðan **Í lagi** til að loka skjámynd og fara aftur í **Skilapöntun - RMA númer: %1, %2** skjámynd. Sölupöntunarlínan fyrir skilavöruna er afrituð í vöruskilapöntunina.

4.  Smelltu á **Skilapöntun** til að opna **Búa til sölupöntun** skjámynd.

5.  Veldu **Afrita skilapöntunarlínur** gátreitinn til að flytja upplýsingar úr skilapöntun sem þú valdir á **Skilapöntun - RMA númer: %1, %2** skjámynd yfir í þessa sölupöntun.

6.  Færa skal inn eða breyta upplýsingum eins og krafist er.
    
    Ef þú tilgreindir sölupöntunina í skrefi 3 og ef sölupöntunarlína fyrir skilavöruna er tengdur sölusamningi verður sjálfkrafa birt auðkenni á gildandi sölusamningi fyrir vöruskilapöntunina í **Sölusamningsauðkenni** reitnum.

7.  Smelltu **Í lagi** til að loka **Búa til sölupöntun** skjámynd og opnaðu **Sölupöntun** skjámynd, þar sem þú getur haldið áfram að slá inn upplýsingar um nýja sölupöntunina. Allar viðeigandi skilapöntunarlínur munu verða afritaðar á nýju sölupöntunina. 
    
    Ef sölusamningsauðkennið birtist sjálfkrafa í **Sölusamningnsauðkenni** reitnum, þá hefur sölusamningurinn verið tengdur við sölupöntunarhausinn fyrir skilavörupöntunina. Ef tiltæk ráðstöfun er til staðar í sölusamningnum sem ekki hefur verið uppfyllt ennþá og sölupöntunin er stofnuð áður en sölusamningurinn rennur út, er mynduð tenging milli sölusamningslínunnar og sölupöntunarlínunnar. Þess vegna eru upplýsingar úr sölusamningnum, t.d. vöruverð, afritaðar yfir í nýju sölupöntunarlínuna. 
  


