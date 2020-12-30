---
title: Losunarreglur
description: Þetta efnisatriði lýsir losunarreglunum fjórum sem notaðar eru fyrir notkun á hráefni.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9f7546b70ddef30d88a79b00fe31d4e82d9bfb9b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430268"
---
# <a name="flushing-principles"></a>Losunarreglur

[!include [banner](../includes/banner.md)]

Losunarreglurnar endurspegla mismunandi stefnur varðandi notkun hráefnis sem er notað í framleiðsluferlum. Notkun er það ferli sem dregur efni úr lagerbirgðum og stillir gildi notaðs efni á **Verk í vinnslu** (WIP) fyrir framleiðslupantanir og runupantanir. Hráefni er vanalega notað frá staðsetningu sem er skilgreind fyrir ferlið sem notar efnið. Þessi staðsetning kallast inntaksstaðsetning framleiðslu.

Áður en efni er notað er það flutt á inntaksstaðsetningu. Eftirfarandi mynd sýnir ferlið.

[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)

1. Hráefnisvöruhús
2. Tiltekt hráefnis
3. Staðsetning framleiðsluinntaks
4. Hráefnisnotkun
5. Framleiðsluferli

Efnisnotkun stýrist af eftirfarandi fjórum losunarreglum:

- Handvirkt
- Byrja
- Ljúk.  
- Tiltækt í staðsetningu

Losunarreglurnar eru skilgreindar í stigveldi sjálfgilda. Stigveldi byrjar á útgefinni afurð, þar sem losunarreglan hefur gildið **Ræsa**. Hægt er að hnekkja losunarreglunni frá afurðinni á uppskriftinni (BOM) eða formúlulínunni. Sjálfgefna losunarreglan á uppskriftarlínum framleiðslu eða formúlulínum runupantana er tekin frá vörunni eða hnekktu gildi á uppskriftinni eða formúlunum.

## <a name="description-of-the-flushing-principles"></a>Lýsing á losunarreglum

### <a name="manual"></a>Handvirkt
Handvirka losunarregla gefur til kynna að skráning á efnisnotkun sé handvirk aðgerð. Þessi regla á við ef þú vilt til dæmis geta rakið tíma, og fjöldi notaðra rununúmera eða raðnúmera þarf að vera tekinn með í rakninguna. Handvirk notkun er skráð í tiltektarlista framleiðslubókar. Hægt er að nota flæði sem haldið er á fyrir atriði sem eru virkjuð fyrir ítarleg vöruhúsaferli.

### <a name="start"></a>Byrja
Losunarreglan Ræsa gefur til kynna að efni verði sjálfkrafa notað þegar framleiðslupöntun er ræst. Magn efnis sem er notað er í hlutfalli við magnið sem er ræst. Þegar losunarreglan Ræsa er notuð ásamt framleiðslukerfinu er einnig hægt að nota hana til að losa efni þegar aðgerð eða ferlisvinnsla er ræst. Þessi regla á til dæmis við ef frávik í notkuninni eru lítil, efnið er lágvirðisefni, það eru engar rakningarkröfur eða ef aðgerðir hafa stuttan keyrslutíma. 

### <a name="finish"></a>Ljúk.  
Losunarreglan Ljúka gefur til kynna að efni verði sjálfkrafa notað þegar tilkynnt er að framleiðslupöntun sé lokið, eða þegar skráð er að aðgerð sem ætlað er að nota efnið sé lokið. Magn efnis sem er notað er í hlutfalli við magnið sem er skráð sem lokið. Þegar losunarreglan Ljúka er notuð ásamt framleiðslukerfinu er einnig hægt að nota hana til að losa efni þegar aðgerð eða ferlisvinnslu er lokið. Þessi regla á við við sömu aðstæður og reglan Ræsa. Aftur á móti er reglan Ljúka fyrir aðgerðir sem hafa lengri keyrslutíma, þar sem ekki ætti að stilla efni á VÍV áður en aðgerðinni er lokið. 

### <a name="available-at-location"></a>Tiltækt í staðsetningu
Losunarreglan Tiltækt í staðsetningu gefur til kynna að efnið verði sjálfkrafa notað þegar það er skráð sem tekið til fyrir framleiðslu. Efnið er skráð sem tekið til frá staðsetningu þegar vinnu við tiltekt á hráefni er lokið, eða þegar efni er tiltækt á staðsetningu framleiðsluinntaks og efnislínan er losuð til vöruhússins. Tiltektarlistinn sem verður til í ferlinu er birtur í runuvinnslu. Þessi regla á til dæmis við ef ert með marga tiltektarverkþætti á móti einni framleiðslupöntun. Í þessu tilfelli þarf ekki að uppfæra tiltektarlistann handvirkt, og þú færð núverandi yfirlit yfir VÍV-stöðuna.
