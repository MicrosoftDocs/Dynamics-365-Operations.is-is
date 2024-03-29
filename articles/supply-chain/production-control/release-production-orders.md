---
title: Losa framleiðslupantanir
description: Útgefin framleiðslupöntun er pöntun sem hefur verið samþykkt til framleiðslu. Hugtakið útgefið er notað til að lýsa stöðu í líftíma framleiðslupöntunar þar sem framleiðslupöntunin er tiltæk fyrir framkvæmd í framleiðsluvinnusal og fyrir ferli vöruhúss.
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 740ac516ffa01d8930aedabb9873834b07b7debf700dc61b14d93ac8d6dcd086
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718871"
---
# <a name="release-production-orders"></a>Losa framleiðslupantanir

[!include [banner](../includes/banner.md)]

Útgefin framleiðslupöntun er pöntun sem hefur verið samþykkt til framleiðslu. Hugtakið útgefið er notað til að lýsa stöðu í líftíma framleiðslupöntunar þar sem framleiðslupöntunin er tiltæk fyrir framkvæmd í framleiðsluvinnusal og fyrir ferli vöruhúss.

## <a name="characteristics-of-the-released-state"></a>Einkennandi þættir Losunarstöðu

**Losað** staða er ein staða í lífsferli framleiðslupöntunar Framleiðslupantanir sem eru í **Losaðar** stöðu eru tiltækar fyrir framkvæmd á framleiðsluvinnusal og fyrir ferli vöruhúsa. **Losað** staða hefur eftirfarandi eiginleika:

- Hægt er að breyta framleiðslupöntun í **Losaða** stöðu annað hvort úr framleiðslupöntun eða með því að nota runuvinnslu. Framleiðslupöntunina má einnig uppfæra sjálfkrafa úr áætlaðar framleiðslupantanir sem eru festaar með því að nota í **tímamörk festingar** á í **aðaláætlun** síðu.
- **Losað** staða er merki fyrir virknitákn vinnusals til að byrja að framkvæma framleiðsluverk í vinnusal.
- framleiðsluskjöl eins og leiðarspjöld, leiðarvinnslur og verkspjöld veita upplýsingar um framleiðsluverk og má gefa út.
- Fyrir Efni sem eru efnislega teknar frá, er  vöruhúsavinnu mynduð til að taka til efni fyrir framleiðslupöntun.

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

- Staðsetningarleiðbeiningar fyrir tiltekt hráefnis sem ákvarðar í hvaða staðsetningu innan vöruhúss á að taka til efni í
- Bylgjusniðmát furir hráefni, þar sem reglurnar fyrir framkvæmd vinnu vöruhúss eru skilgreindar.
- Staðsetning framleiðsluinntaks sem ákvarðar hvar efni eru sett

Þegar notaðar eru númeraplötustýrðar staðsetningar er hægt að velja hvort tína eigi pantað magn eða allt tiltækt magn vörunnar þegar tiltekt hráefnisins er afgreidd. Til að stilla þennan valkost:

1. Opnið **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir** og opnið viðkomandi afurð.
1. Flýtiflipinn **Vöruhús** er stækkaður.
1. Veljið einn af eftirfarandi valkostum fyrir reitinn **Tiltekt hráefnis í staðsetningum númeraplatna**:
    - *Pöntunartiltekt*: aðeins ætti að taka til pantað magn.
    - *Sviðsetning*: Þegar mögulegt ætti að tína allt tiltækt magn á númeraplötunni. Til að starfsmaður geti tínt allt magn númeraplötu má númeraplatan ekki innihalda blandaðar vörur og má ekki verð með blandaðar víddir. Ef númeraplatan inniheldur blandaðar víddir eða vörur mun tiltektin halda áfram eins og hún væri stillt á *Tiltekt pöntunar*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]