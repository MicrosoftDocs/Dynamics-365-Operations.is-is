---
title: Hlutaafhending á flutningsfarmi
description: Þetta efnisatriði útskýrir hvernig hægt er að afhenda hluta úr farmi og fresta áætlun um afkastagetu farmsins.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 5ea844531314b4dd2ff3fa46d8f0b57d9c47059e684d677f06f8259b264d4a90
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782300"
---
# <a name="partial-shipment-of-a-transport-load"></a>Hlutaafhending á flutningsfarmi

[!include[banner](../includes/banner.md)]

Með því að setja upp hlutaafhendingu á farmi er hægt að meðhöndla farm þar sem ekki er hægt að ákvarða afkastagetu fyrr en öllum sölulínum hefur verið bætt við farm. Þá er hægt að ljúka ferlinu þegar nákvæm brettatalning er þekkt. Þess vegna þarf ekki að ákveða hvaða brettum verður úthlutað á hvaða flutning fyrr en á augnablikinu sem verið er að hlaða flutning úr uppsettum birgðum.

Þessi eiginleiki býður upp á annan valkost við framfylgni á stífara skipulagi þar sem þarf að ákveða hvaða brettum verður úthlutað á hvaða flutning áður en hægt er að búa til tiltekt eða hleðsluvinnu. Í staðinn geta notendur stillt einstakar hleðslur fyrir staðfesta hlutaafhendingu. Flutningshleðsluferli fyrir þessar hleðslur getur þá átt sér stað. Þess vegna getur flutningsáætlunardeildin skipulagt farma án þess að þurfa að íhuga getu einstakra flutninga.

Við hleðslu geta starfskraftar skilgreint nýjan flutningsfarm sem hægt er að hlaða bretti á. Að öðrum kosti geta þeir borið kennsl á flutningsfarm sem er til staðar. Hægt er að skrá þessi gögn í gegnum fartæki. Þess vegna geta nokkrir starfskraftar í vöruhúsi hlaðið birgðum frá sömu hleðslu yfir á aðra hleðslu á sama vörubílnum. Síðan er hægt að afhenda farminn að fullu eða að hluta til.

> [!NOTE] 
> Til að hlaða birgðum frá farmi yfir á sérstakan flutningsfarm og afhenda farminn að hluta til, þarf að búa til vinnu með hleðsluflokki í vinnusniðmáti. Ekki er hægt að hlaða venjulega tiltekt af gerðinni **Tiltekt** á flutningsfarm eins og vörubíl.

## <a name="set-up-transport-loads-for-partial-shipment"></a>Setja upp flutningsfarma fyrir hlutaafhendingu

Uppsetning á hlutaafhendingu farma samanstendur af eftirfarandi tveimur ferlum.

### <a name="set-the-loading-strategy"></a>Stilltu hleðsluáætlunina

Þú verður að virkja að hlutahleðslu með því að stilla hleðsluáætlunina. Þú getur stillt hleðsluáætlunina eftir að þú hefur búið til hleðslu.

1. Veldu **Vöruhúsakerfi** \> **Hleðslur** \> **Allar hleðslur**.
2. Veldu hleðslu og smelltu síðan á **Haus**.
3. Í reitnum **Hleðsluáætlun** skal velja **Afhending hlutahleðsla leyfð**.

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a>Búðu til valmyndaratriði fyrir hleðslu flutningsfarms

Þú verður að búa til nýtt valmyndaratriði sem gerir kleift að hlaða flutningsfarmi. Flutningsfarmur gerir þér kleift að flokka vinnulínur frá einni hleðslu eða mörgum hleðslum. Allt sem er bætt við flutningsfarminn getur síðan verið afhent með því að nota farsímaskanna.

1. Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.
2. Veldu **Nýtt** og síðan í reitnum **Snið** skal velja **Vinna**.
3. Stilltu valkostinn **Nota fyrirliggjandi vinnu** á **Já**.
4. Í flipanum **Almennt**, í reitnum **Stýrt af** skal velja **Flutningshleðsla**.
5. Til að virkja staðfestingu á afhendingu á farsímaskanna skal í reitnum **Leyfð gerð á staðfestingu afhendingar** velja **Flutningsfarmur**.

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a>Staðfestu afhendingu á flutningsfarmi frá viðskiptavininum

Þessi uppsetning gerir þér kleift að staðfesta flutningsfarm sem inniheldur fulla hleðslu eða hlutahleðslu sem á að afhenda.

1. Veldu **Vöruhúsakerfi** \> **Hleðslur** \> **Flutningshleðslur**.
2. Í aðgerðasvæðinu, í flipanum **Afhenda og móttaka** í flokknum **Staðfesta** skal velja **Flutningur**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]