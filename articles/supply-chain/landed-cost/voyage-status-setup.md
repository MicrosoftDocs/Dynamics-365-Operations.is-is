---
title: Staða ferðar
description: Þetta efnisatriði lýsir því hvernig á að koma á fót stöðugildunum sem notendur geta úthlutað á ferðir.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500887"
---
# <a name="voyage-status-setup"></a>Uppsetningarstaða ferðar

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Á síðunni **Ferðastöður** eru sett upp mengi stöðugilda sem notendur geta úthlutað á ferðir. Notendur geta úthlutað gildi ferðastöðu á öll stig ferðar: ferð, gám, fólíó, innkaupapöntun og vöru (innkaupalínur og flutningspöntunarlínur). Þetta er notað í tvennum tilgangi:

- Upplýsa skal notandann um stöðu á ferð, gámi, fólíói, innkaupapöntun eða vöru (innkaupalínum og flutningspöntunarlínum).
- Takmarka notkun kostnaðarsvæðisins við að koma í veg fyrir breytingar eða eyðingu.

Til að setja upp ferðastöður skal fara í **Heildarkostnaður \> Uppsetning \> Ferðastöður**. Þar er hægt að bæta við, fjarlægja og breyta stöðu með því að nota hnappana á aðgerðarúðunni.

Hvert kostnaðarsvæði er með eigin stillingar og stigveldi fyrir ferðastöðu. Þar af leiðandi, á síðunni **Ferðastöður**, í reitnum **Kostnaðarþáttur**, þarf fyrst að velja kostnaðarþáttinn sem á að skoða eða búa til stöðu ferðar fyrir. Fyrir hverja ferðastöðu skal því næst stilla reitina sem lýst er í eftirfarandi töflu, eftir því sem þörf krefur. Athugið að stöðu á ferð er einnig hægt að breyta sjálfkrafa eftir kerfisatvikum, eins og reglur sem hafa verið settar á með því að nota stjórnstöð rakningar.

| Svæði | lýsing |
|---|---|
| Staða ferðar | Færið inn heiti ferðastöðunnar. |
| lýsing | Færa inn lýsingu á ferðastöðunni. |
| Breyta | Veljið þennan gátreit ef notendur hafa leyfi til að breyta ferðum sem eru með þessa stöðu. |
| Eyða | Veljið þennan gátreit ef notendur hafa leyfi til að eyða ferðum sem eru með þessa stöðu. |
| Skylda | Veljið þennan gátreit til að gera ferðastöðuna áskilda, svo ekki sé hægt að sleppa henni. |
| Yfirstig | Notið þennan reit til að koma á stigveldi á meðal stöðugildanna. Aðeins er hægt að breyta ferðastöðum (annaðhvort handvirkt eða sjálfkrafa) niður á við í stigveldinu, frá stöðu yfireiningar til einnar af undireiningunum.

> [!NOTE]
> Aðeins þarf að setja upp tilgreinda ferðastöður sem fyrirtækið notar. Dæmigerðar stöður ferðar eru m.a. *Staðfest*, *Vörur í flutningi*, *Móttekið*, *Tilbúið fyrir kostnaðarútreikning* og *Kostnaðarútreikningur*. Hins vegar gætu aðrar stöður verið í boði.
