---
title: "Taka efnislegt virði með"
description: "Gátreiturinn Taka með efnislegt virði á flýtiflipanum Birgðalíkan í skjámyndinni Vörulíkanaflokkar er notaður til að tilgreina hvort efnislega uppfærðar færslur eru teknar með þegar meðaltal kostnaðarverðs er reiknað út fyrir vöru."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa59031ed2144c2e92399933cd5dd40bfca0f2ae
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="include-physical-value"></a>Taka efnislegt virði með

[!include[banner](../includes/banner.md)]


Gátreiturinn Taka með efnislegt virði á flýtiflipanum Birgðalíkan í skjámyndinni Vörulíkanaflokkar er notaður til að tilgreina hvort efnislega uppfærðar færslur eru teknar með þegar meðaltal kostnaðarverðs er reiknað út fyrir vöru.

Gátreiturinn **Taka með efnislegt virði** hefur eftirfarandi gildi.

| Gildi    | Niðurstaða                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Valið | Bæði efnislega og fjárhagslega uppfærðar færslur eru notaðar til að reikna út meðalkostnaðarverðið. |
| Hreinsað  | Aðeins fjárhagslega uppfærðar færslur eru notaðar til að reikna meðalkostnaðarverðið.                                     |

Gátreiturinn hefur svolítið ólík áhrif eftir því hvaða birgðalíkan er notað.

-   Ef valinn er gátreiturinn **Taka með efnislegt virði** þegar FIFO (Fyrst inn, fyrst út), LIFO (Síðast inn, fyrst út) eða LIFO birgðalíkanið er notað gerir birgðalokun líka leiðréttingar á efnislega uppfærðum færslum.
-   Ef gátreiturinn **Taka með efnislegt virði** er ekki valinn þegar þessi birgðalíkön eru notuð mun birgðalokun aðeins gera uppgjör í þeim færslum sem hafa verið fjárhagslega uppfærðar.
-   Þegar notuð eru birgðalíkön vegins meðaltals eða dagsetningarbirgðalíkön vegins meðaltals jafnar birgðalokun eingöngu fjárhagslega uppfærðar færslur hvort sem gátreiturinn **Taka með efnislegt virði** var valinn eða ekki.

**Dæmi 1** Gátreiturinn **Taka með efnislegt virði** hefur verið valinn og eftirfarandi innkaupapantanir hafa verið mótteknar:

-   Innkaupapöntun fyrir magnið 2 á kostnaðarverði 10,00 USD hefur verið uppfærð með fylgiseðli
-   Innkaupapöntun fyrir magnið 3 á kostnaðarverði 12,00 USD hefur verið uppfærð með reikningi

Í þessu tilfelli verður meðalkostnaðarverð 11,20 USD af því að bæði efnislega og fjárhagslega uppfærðar færslur eru notaðar til að reikna út kostnaðarverðið. **Dæmi 2** Gátreiturinn **Taka með efnislegt virði** hefur ekki verið valinn og kostnaðarverð uppsetningar vörunnar er 10,00 USD. Innkaupapöntun fyrir magnið 20 á kostnaðarverði 12,00 USD hefur verið móttekin og uppfærð með fylgiseðli. Þegar sölupöntun er bókuð mun kerfið bóka kostnaðarupphæðina 10,00 USD vegna þess að meðalkostnaðarverðið mun ekki innihalda efnislega bókaðar færslur. **Athugasemd:** Til samanburðar, ef gátreiturinn **Taka með efnislegt virði** er valinn þegar sölupöntun er bókuð, verður bókaða kostnaðarupphæðin 12,00 USD.




