---
title: Losa framleiðslupantanir
description: Útgefin framleiðslupöntun er pöntun sem hefur verið samþykkt til framleiðslu. Hugtakið útgefið er notað til að lýsa stöðu í líftíma framleiðslupöntunar þar sem framleiðslupöntunin er tiltæk fyrir framkvæmd í framleiðsluvinnusal og fyrir ferli vöruhúss.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 400c2786d80681827829286e6e9667b4d51612c4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "339373"
---
# <a name="release-production-orders"></a>Losa framleiðslupantanir

[!include [banner](../includes/banner.md)]

Útgefin framleiðslupöntun er pöntun sem hefur verið samþykkt til framleiðslu. Hugtakið útgefið er notað til að lýsa stöðu í líftíma framleiðslupöntunar þar sem framleiðslupöntunin er tiltæk fyrir framkvæmd í framleiðsluvinnusal og fyrir ferli vöruhúss. 

<a name="characteristics-of-the-released-state"></a>Einkennandi þættir Losunarstöðu
-------------------------------------

**Losað** staða er ein staða í lífsferli framleiðslupöntunar Framleiðslupantanir sem eru í **Losaðar** stöðu eru tiltækar fyrir framkvæmd á framleiðsluvinnusal og fyrir ferli vöruhúsa. **Losað** staða hefur eftirfarandi eiginleika:

-   Hægt er að breyta framleiðslupöntun í **Losaða** stöðu annað hvort úr framleiðslupöntun eða með því að nota runuvinnslu. Framleiðslupöntunina má einnig uppfæra sjálfkrafa úr áætlaðar framleiðslupantanir sem eru festaar með því að nota í **tímamörk festingar** á í **aðaláætlun** síðu.
-   **Losað** staða er merki fyrir virknitákn vinnusals til að byrja að framkvæma framleiðsluverk í vinnusal.
-   framleiðsluskjöl eins og leiðarspjöld, leiðarvinnslur og verkspjöld veita upplýsingar um framleiðsluverk og má gefa út.
-   Fyrir Efni sem eru efnislega teknar frá, er  vöruhúsavinnu mynduð til að taka til efni fyrir framleiðslupöntun.

## <a name="releasing-jobs-to-the-shop-floor"></a>Losa vinnslu í vinnusal
Eftir að framleiðslupöntun er losuð,eru framleiðsluverk sem eru tengd pöntuninni sýnileg og tilbúin fyrir skráningu. Virknitákn geta framkvæmt vinnsluskráningar, eins og Hefja, Stöðva og Lokið, í annað hvort síðunni **Afgreiðslustöð verkspjalda** eða síðunni **Verkspjaldstæki**. Skráður tími og magn eru sjálfvirkt fluttar úr skráningasíðum í framleiðslubækur til að fylgjast með notuðum tíma og magni.

## <a name="route-cards"></a>Leiðarspjöld
leiðarspjaldi veitir yfirlit yfir upplýsinga sem koma úr leið og uppsetningu aðgerða, og úr aðgerð og vinnsluröðunaraðferðum.

## <a name="route-jobs"></a>Leiðarvinnslur
Leiðarvinnsla er með lista yfir sérhverja vinnslu aðgerðar í smáatriðum, þar á meðal uppsetningu, ferli, röð, og flutningstíma. Til dæmis, Aðgerð eins og málun gæti til dæmis útheimt einstakar vinnslur, eins og uppsetningu tíma, keyrslutíma (fyrir málningarferlið) og biðtíma (fyrir þornun).

## <a name="job-cards"></a>Vinnsluspjöld
vinnsluspjaldi er listi yfir einstök vinnslunúmer fyrir tiltekna aðgerð. Eitt verk birtist í hverri síðu Vinnslurnar sem eru hafðar á vinnsluspjaldi, og áætlaður tími, koma úr upplýsingum um uppsetningu leiða og aðgerða. Frá vinnsluspjaldi er hægt að opna **framleiðslubókarlínur**, **vinnsluspjald** síðu. Einstaklingarnir sem keyra rekstrartilföng geta gefið svörun um framleiðsluferlið. Fyrirliggjandi eru svæði þar sem hægt er að færa inn talnagögn um notkun og upplýsingar eins og gallað magn.

## <a name="warehouse-work-for-raw-material-picking"></a>Vinna vöruhúss fyrir tiltekt hráefnis.
Vinnu fyrir tiltekt hráefnis er stofnuð á meðan á losun stendur. Vinna er mynduð aðeins fyrir magn efnis sem var efnislega tekin frá fyrir framleiðslupöntunina áður en pöntunin var losuð. Eftirfarandi uppsetning er nauðsynleg til að mynda vöruhúsavinnu fyrir tiltekt hráefnis:

-   Staðsetningarleiðbeiningar fyrir tiltekt hráefnis sem ákvarðar í hvaða staðsetningu innan vöruhúss á að taka til efni í
-   Bylgjusniðmát furir hráefni, þar sem reglurnar fyrir framkvæmd vinnu vöruhúss eru skilgreindar.
-   Staðsetning framleiðsluinntaks sem ákvarðar hvar efni eru sett




