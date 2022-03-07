---
title: Villa kemur upp þegar staðsetning er valin við skráningu tiltektarlista
description: Villa kemur upp þegar staðsetning er valin við skráningu tiltektarlista.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ef34b4fdcc572c56319f6cbf4913d822d8857595
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474965"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Villa kemur upp þegar staðsetning er valin við skráningu tiltektarlista

KB númer: 4613106

## <a name="symptoms"></a>Einkenni

Þetta vandamál kemur upp þegar kerfið er sett upp til að taka frá sölupantanir sjálfkrafa. Ef reynt er að velja staðsetningu fyrir skráningarlínu tínslulista birtast eftirfarandi villuboð þegar frátekningarferli vöruhúsastjórnunar (WMS) eru notuð:

> Ekki er hægt að uppfæra magn með nýjum víddum

Þetta vandamál getur komið upp vegna þess að það eru of litlar birgðir á tiltekinni staðsetningu.

## <a name="resolution"></a>Upplausn

Kerfið hagar sér eins og það er hannað.

Við mælum með því að notuð séu handvirk bókunarferli frá vallínunni í tilvikum þar sem frátekningarferli er notað á vöruhúsastigi, ef birgðir eru ekki fráteknar á öllum birgðavíddum og ekki eru nægar birgðir á tilteknum stað. Síðan er hægt að nota aðgerðina *Frátektarlota* til að dreifa lægri frátekningum, svo sem staðsetningu, fyrir allt tiltækt magn.
