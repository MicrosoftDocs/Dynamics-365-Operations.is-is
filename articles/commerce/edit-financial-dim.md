---
title: Breytið fjárhagsvíddum fyrir smásölufærslur
description: Þetta efnisatriði lýsir því hvernig á að breyta fjárhagsvíddum fyrir smásölufærslur í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: d5fee5f5dfee73ddb9fbcf8a33df66c29f9438b49136181633b989d1a02ef4f5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765315"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Breytið fjárhagsvíddum fyrir smásölufærslur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að breyta fjárhagsvíddum fyrir smásölufærslur í Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Breyta fjárhagsvíddum

Fylgið eftirfarandi skrefum til að breyta fjárhagsvíddum fyrir smásölufærslur í Commerce Headquarters.

1. Opnið síðuna **Fjárhagsvíddarskilgreining fyrir samþættingu forrita**.
1. Veljið virku færsluna **Samþætting sjálfgefinna vídda**.
1. Athugið flýtiflipann **Fjárhagsvíddir** og gangið úr skugga um að allar víddir sem á að breyta í Excel-vinnublaðinu séu til staðar á listanum **Val**. Frekari upplýsingar eru í [Gagnaeiningar](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. Sækið og opnið Excel-skrána á síðunni **Yfirlit**, á síðunni **Smásölufærslur** eða reitinn **Bilanir við villuleit í færslu** á vinnusvæðinu **Fjármál verslunar**.
1. Veljið **Hönnun** til að breyta fjárhagsvídd færslunnar og smellið síðan á blýantstáknið við hlið raðarinnar **Færsla (sannprófanleg)**.
1. Leitið að og veljið svæðið **FinancialDimensionDisplayValue**, veljið haushluta Excel-vinnublaðsins og síðan **Bæta við merki**.
1. Velja skal hólf fyrir neðan hólfið sem valið var í fyrra skrefi, velja **Bæta við gildi** og síðan **Uppfæra**. Fjárhagsvíddunum er bætt við Excel-vinnublaðið og síðan er hægt að gera breytingar á þeim og birta þær.
1. Til að breyta víddunum í færslulínunum skal velja röðina **Sölufærslur (sannprófanlegar)**, velja blýantstáknið og síðan endurtaka skref 6 og 7.
1. Til að breyta víddunum í greiðslulínunum skal velja röðina **Greiðslufærslur (sannprófanlegar)**, velja blýantstáknið og síðan endurtaka skref 6 og 7.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár](edit-cash-trans.md)

[Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar](edit-order-trans.md)

[Stofna Excel-vinnubók til að breyta smásölufærslum](create-excel-edit.md)

[Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]