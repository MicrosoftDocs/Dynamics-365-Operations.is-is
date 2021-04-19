---
title: Flutningsstjórnunarstöður
description: Þetta efnisatriði útskýrir hvernig á að búa til flutningsstöðu og varpa þeirri stöðu á stöðu flutningsaðila.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3a2b9e50dddf0f015cdd3f16d6d93fcc03d464d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807609"
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