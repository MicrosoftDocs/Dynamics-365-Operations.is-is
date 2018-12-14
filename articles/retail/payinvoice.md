---
title: "Uppsetning á greiðsluaðstæðum reikninga"
description: "Þetta efnisatriði lýsir því hvernig á að grunnstilla Dynamics 365 for Retail til að styðja ýmsar aðstæður sem tengjast greiðslu reikninga."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 53c4b9a9c9dac1add7021d909b2c8900d11e5c0c
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pay-invoice-scenarios"></a>Uppsetning á greiðsluaðstæðum reikninga

[!include [banner](includes/banner.md)]

Greiðsluaðgerð reiknings í Dynamics 365 for Retail hefur verið víkkuð út til að styðja:
- Greiðslu á mörgum sölupöntunarreikningum í einni POS-færslu.
- Greiðslu á ýmsum reikningsgerðum viðskiptavina, þ.á.m. reikningum með frjálsum texta, verktengdum reikningum og kreditnótum.

Til að virkja þessar aðstæður þarf að grunnstilla virkniregluna fyrir verslanir eins og útskýrt er hér að neðan.  

1. Opnið **Retail > Uppsetning rásar > Uppsetning sölustaðar > Forstillingar sölustaðar > Virknireglur** og veljið forstillingu sem tengd er við verslanirnar sem á að gera breytingar á.

1. Á flipanum **Aðgerðir** skal skilgreina eftirfarandi færibreytur eftir þörfum.

    - **Sölupöntunarreikningur** - Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga sem tengjast sölupöntun í einni POS-færslu.

    - **Reikningur með frjálsum texta** - Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga með frjálsum texta í einni POS-færslu.

    - **Verkreikningur** - Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga sem tengjast verki í einni POS-færslu.

    - **Kreditnóta sölupöntunar** - Veljið **Já** til að gera notendum kleift að gera upp margar kreditnótur sem tengjast sölupöntun gagnvart opnum reikningum eða vinna úr endurgreiðslu til viðskiptavinar vegna opinnar kreditnótu.

> [!NOTE]
> Greiðsla eða uppgjör upphæða að hluta til er ekki enn studd.

