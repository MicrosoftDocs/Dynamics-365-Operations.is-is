---
title: Flutningsstjórnunarstöður
description: Þessi grein útskýrir hvernig á að búa til flutningsstöðu og varpa þeirri stöðu á stöðu flutningsaðila.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b20570a87a9f8969ca6dcf898176fd40f88eeca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897372"
---
# <a name="transportation-management-statuses"></a>Flutningsstjórnunarstöður

[!include [banner](../includes/banner.md)]

Setja upp aðalkóða fyrir flutningsstöður til að túlka kóða sem farmflytjendur útvega. Þetta gerir notanda kleift að samþætta við farmflytjanda til að gefa upp stöðu. Flutningsstaða sem gefnar eru upp fyrir flutningsstöðukóða getur hjálpað við að rekja stöðu hleðslu, sending eða gám. Aðeins er hægt að uppfæra tiltekna flutningsstöðu fyrir farm, sendingu eða gám með gagnasamþættingu og ekki handvirkt á notandaviðmótinu.

## <a name="create-a-transportation-status"></a>Býr til flutningsstöðu

Fylgdu þessum skrefum til að búa til flutningsstöðu:

1. Opnið **Flutningsstjórnun \> Uppsetning \> Sniðmát flutningsstöðu**.
1. Veldu **Nýtt** til að búa til sniðmát fyrir flutningsstöðu.
1. Í svæðinu **Sniðmát flutningsstöðu** er færður inn einkvæmur kóði fyrir flutningsstaða.
1. Í reitnum **Flutningsgerð** skal velja annað hvort *Farmflytjandi* eða *Miðstöð* sem gerð flutnings.
1. Sláðu inn heiti og flutningsstöðu.
1. Lokið síðunni.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Varpa flutningsstöðu í stöðu flutningsaðila

Til að varpa flutningsstöðu á stöðu flutningsaðila skal fylgja eftirfarandi skrefum:

1. Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Flutningsstöður flutningsaðila**.
1. Veljið **Nýtt** til að varpa kóða frá farmflytjanda til aðalkóða flutningsstöðu.
1. Velja einkvæmt auðkenni fyrir flutningsþjónustuna og farmflytjanda.
1. Veljið kóða flutningsstöðu sem á að varpa kóðanum fyrir valda farmflytjanda fyrirtækisins.
1. Færa skal inn ytri kóðann sem farmflytjandi notar.
1. Lokið síðunni.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]