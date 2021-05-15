---
title: Stofna sölupöntun fyrir skilgreinanlega afurð
description: Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921290"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a>Stofna sölupöntun fyrir skilgreinanlega afurð

[!include [banner](../../includes/banner.md)]

Þetta verkefni sýnir hvernig á að nota grunnstillingarsniðmát fyrir afurð á sölupöntun. Þetta dæmi notar D0006 líkanið í USMF sýnigögnum fyrirtækis. Venjulega notar sölupantanavinnsla þetta ferli.

## <a name="create-a-sales-order"></a>Stofna sölupöntun

1. Farið í **Sala og markaðssetning \> Vinnusvæði \> Vinnsla og fyrirspurnir sölupantana**.
1. Veljið **Nýtt**.
1. Veldu **Velja sölupöntun**.
1. Í reitnum **Viðskiptavinalykill** skal velja *US-001*. 
1. Veljið **Í lagi**.
1. Í svæðið **Vörunúmer** veldu *D0006*.
    * Fyrir þetta verk þarf að velja samskipanlega afurð.  
1. Veljið **Afurð og framboð**.
1. Veljið **Skilgreina línu**.
    * Athugið að verði hefur verið breytt, byggt á stillingunni sem var valin, og að **Taka með kapla** svæðið er núna stillt á *Satt*.  
    * Athugið sjálfgefna verð- og stillingar sem eru valdar fyrir á köplum.  
1. Veljið **Hleðslusniðmát**.
    * Þetta dæmi sýnir hvernig hægt er að nota sniðmát til að velja forskilgreind afbrigði. Ef þetta ferli er notað sem verkleiðbeining og þú vilt sjá hin eigindargildin sem eru tiltæk verður þú velja hnappinn **Opna**.  
1. Veljið **Í lagi**.
1. Veljið **Í lagi**.
1. Útvíkkaðu hlutann **upplýsingar Línu**.
1. Veljið flipann **Afurð**.
    * Afbrigði vörunnar er nú skráður undir afurðarvíddum.  
1. Lokið síðunni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]