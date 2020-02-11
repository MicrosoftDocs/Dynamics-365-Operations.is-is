---
title: Bæta við lógói
description: Þetta efni lýsir því hvernig á að bæta merki við á vefsvæði í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914623"
---
# <a name="add-a-logo"></a>Bæta við lógói

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að bæta merki við á vefsvæði í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Þegar þú byggir vefsvæðið er eitt af fyrstu hlutunum sem þú munt líklega gera er að bæta fyrirtækinu þínu eða merki vörumerkis við haus svæðisins. Byrjunareining Dynamics 365 Commerce á netinu veitir einingu sem gerir þetta verkefni auðvelt.

Þú getur bætt merki beint við í sniðmát, skipulag eða síðu. Á þennan hátt geturðu auðveldlega breytt merkinu sem birtist á tilteknum síðum eða síðuhópum. En þetta efni nær yfir algengustu atburðarásina, þar sem þú bætir merkinu við hausbrot sem hægt er að endurnýta á öllum síðum vefsvæðisins.

## <a name="prerequisites"></a>Forkröfur

Það verður að ljúka þessum verkefnum áður en þú getur bætt merki við allar síður vefsvæðisins.

1. Flyttu merkið þitt upp á stafræna eignastjórann sem þú getur fengið aðgang að af síðunni **Eignir**.
1. Stofna hausbrot. Fyrir frekari upplýsingar um hvernig á að búa til og nota brot, sjá [Unnið með brot](work-with-fragments.md).
1. Láttu hausbrotið fylgja með í sniðmátinu sem vefsíður þínar nota fyrir skipulags- og einingavalkosti. Nánari upplýsingar um sniðmát er að finna í [Unnið með sniðmát](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Bæta merki við hausbrot

Fylgdu þessum skrefum til að bæta við merki við hausbrotið fyrir vefsvæðið.

1. Í yfirlitssvæðinu til vinstri velurðu **Brot** og velur síðan hausbrotið sem var stofnað.
2. Velja **Skrá út**.
3. Stækkaðu hólfið **Haus** og hólfið **Merki**.
4. Veldu úrfellingarhnappinn (**...**) fyrir hólfið **Merki** og veldu síðan **Bæta við einingu**.
5. Veldu merkiseininguna.
6. Í eiginleikaglugganum til hægri stillirðu merkjaeininguna þannig að hún sýni merkið þitt.
7. Vistaðu fyrirsagnarbrotið, skráðu það inn og gefðu það út.

Eftir að þú hefur birt uppfært hausbrot birta allar vefsíðurnar sem nota sniðmátið sem inniheldur hausbrotið merkið þitt.

## <a name="additional-resources"></a>Frekari upplýsingar

[Velja þema svæðis](select-site-theme.md)

[Unnið með CSS hnekkiskrám](css-override-files.md)

[Bæta við táknmynd](add-favicon.md)

[Bæta við opnunarkveðju](add-welcome-message.md)

[Bæta við yfirlýsingu um höfundarrétt](add-copyright-notice.md)

[Bæta tungumálum við síðuna](add-languages-to-site.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)
