---
title: Uppsetning á greiðsluaðstæðum reikninga
description: Þetta efnisatriði lýsir því hvernig á að grunnstilla Dynamics 365 Commerce til að styðja ýmsar aðstæður sem tengjast greiðslu reikninga.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08d3cf48c0bea6f0e13dda49e53b314a6037860d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804554"
---
# <a name="set-up-pay-invoice-scenarios"></a>Uppsetning á greiðsluaðstæðum reikninga

[!include [banner](includes/banner.md)]

Greiðsluaðgerð reiknings í Dynamics 365 Commerce hefur verið víkkuð út til að styðja:

- Greiðslu á mörgum sölupöntunarreikningum í einni POS-færslu.
- Greiðslu á ýmsum reikningsgerðum viðskiptavina, þ.á.m. reikningum með frjálsum texta, verktengdum reikningum og kreditnótum.

Til að virkja þessar aðstæður þarf að grunnstilla virkniregluna fyrir verslanir eins og útskýrt er hér að neðan.

1. Opnið **Retail and Commerce\> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur** og veljið forstillingu sem tengd er við verslanirnar sem á að gera breytingar á.
2. Á flipanum **Aðgerðir** skal skilgreina eftirfarandi færibreytur eftir þörfum.

    - **Sölupöntunarreikningur** – Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga sem tengjast sölupöntun í einni sölustaðarfærslu.
    - **Reikningur með frjálsum texta** – Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga með frjálsum texta í einni sölustaðarfærslu.
    - **Verkreikningur** – Veljið **Já** til að gera notendum kleift að greiða einn eða fleiri reikninga sem tengjast verki í einni sölustaðarfærslu.
    - **Kreditnóta sölupöntunar** – Veljið **Já** til að gera notendum kleift að gera upp margar kreditnótur sem tengjast sölupöntun gagnvart opnum reikningum eða vinna úr endurgreiðslu til viðskiptavinar vegna opinnar kreditnótu.

> [!NOTE]
> Greiðsla eða uppgjör upphæða að hluta til er ekki enn studd.


[!INCLUDE[footer-include](../includes/footer-banner.md)]