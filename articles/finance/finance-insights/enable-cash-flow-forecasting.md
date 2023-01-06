---
title: Virkja sjóðstreymisspá
description: Þessi grein útskýrir hvernig á að kveikja á eiginleikanum „Sjóðstreymisspár“ í Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859876"
---
# <a name="enable-cash-flow-forecasting"></a>Virkja sjóðstreymisspá

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að kveikja á eiginleikanum „Sjóðstreymisspár“ í Finance Insights.

> [!NOTE]
> Til að nota greiðsluspár í sjóðstreymi þarf að setja upp greiðsluspár viðskiptavinar eins og lýst er í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md).
  
1. Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:

    1. Veldu **Leita að uppfærslum**.
    2. Á flipanum **Allt** skal leita að **Sjóðstreymisspár**. Ef þú finnur ekki þennan eiginleika skaltu leita að **(Forskoða) Sjóðstreymisspár**. 
    3. Kveiktu á eiginleikanum.

2. Opnið **Reiðufjár- og bankastjórnun \> Uppsetning sjóðsstreymisspár** og bætið við greiðslugetulyklum sem eiga að vera með í spánum. Einnig skal setja upp greiðslugetulykil fyrir greiðslur á flipanum **Viðskiptakröfur** og **Viðskiptaskuldir**. Mundu að endurreikna sjóðstreymisspána.

    > [!NOTE]
    > Ef greiðslugetureikningar eru ekki settir upp er ekki hægt að mynda sjóðstreymið.
    >
    > Nánari upplýsingar um hvernig setja skuli upp sjóðstreymisspá eru að finna í [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md).

3. Opnaðu **Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn (forskoða) \> Sjóðsstreymisspár (forskoða)** og fylgdu eftirfarandi skrefum:

    1. Á flipanum **Sjóðsstreymisspá** skal velja **Virkja eiginleika**.
    2. Veljið **Stofna spálíkan**.

> [!NOTE]
> Reiknilíkan fyrir **Sjóðstreymisspá** krefst þjálfunar gagna með 100 eða fleiri færslum sem ná yfir meira en eitt ár. Við mælum með að notuð séu að minnsta kosti tvö ár af gögnum með meira en 1.000 færslur.

Frekari upplýsingar um afkastagetu sjóðstreymisspár er að finna í [Sjóðstreymisspár](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
