---
title: Breytið fjárhagsvíddum fyrir smásölufærslur
description: Þetta efnisatriði lýsir því hvernig á að breyta fjárhagsvíddum fyrir smásölufærslur í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010176"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Breytið fjárhagsvíddum fyrir smásölufærslur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að breyta fjárhagsvíddum fyrir smásölufærslur í Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Breyta fjárhagsvíddum

Fylgið eftirfarandi skrefum til að breyta fjárhagsvíddum fyrir smásölufærslur í Commerce Headquarters.

1. Opnið síðuna **Fjárhagsvíddarskilgreining fyrir samþættingu forrita**.
1. Veljið virku færsluna **Samþætting sjálfgefinna vídda**.
1. Athugið flýtiflipann **Fjárhagsvíddir** og gangið úr skugga um að allar víddir sem á að breyta í Excel-vinnublaðinu séu til staðar á listanum **Val**. Frekari upplýsingar eru í [Gagnaeiningar](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
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