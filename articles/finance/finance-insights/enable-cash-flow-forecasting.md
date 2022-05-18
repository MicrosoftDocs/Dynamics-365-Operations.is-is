---
title: Virkja sjóðstreymisspá
description: Þetta efnisatriði útskýrir hvernig á að kveikja á eiginleikanum „Sjóðstreymisspár“ í fjármálainnsýn.
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
ms.openlocfilehash: 8dba56af53090d5d78632da4d414143b136f8a8d
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713755"
---
# <a name="enable-cash-flow-forecasting"></a>Virkja sjóðstreymisspá

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að kveikja á eiginleikanum Sjóðstreymisspár í Finance Insights.

> [!NOTE]
> Til að nota greiðsluspár í sjóðstreymi þarf að setja upp greiðsluspár viðskiptavinar eins og lýst er í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md).
  
1. Opnið vinnusvæðið **Eiginleikastjórnun** og fylgið eftirfarandi skrefum:

    1. Veldu **Leita að uppfærslum**.
    2. Á **Allt** flipi, leitaðu að **Sjóðstreymisspár**. Ef þú finnur ekki þann eiginleika skaltu leita að **(Preview) Sjóðstreymisspár**. 
    3. Kveiktu á eiginleikanum.

2. Opnið **Reiðufjár- og bankastjórnun \> Uppsetning sjóðsstreymisspár** og bætið við greiðslugetulyklum sem eiga að vera með í spánum. Settu einnig upp lausafjárreikning fyrir greiðslur á **Reikningur fáanlegur** og **Viðskiptaskuldir** flipa. Vertu viss um að endurreikna sjóðstreymisspána.

    > [!NOTE]
    > Ef greiðslugetureikningar eru ekki settir upp er ekki hægt að mynda sjóðstreymið.
    >
    > Fyrir frekari upplýsingar um hvernig á að setja upp sjóðstreymisspár, sjá [Sjóðstreymisspá](../cash-bank-management/cash-flow-forecasting.md).

3. Opnaðu **Reiðufjár- og bankastjórnun \> Uppsetning \> Fjármálainnsýn (forskoða) \> Sjóðsstreymisspár (forskoða)** og fylgdu eftirfarandi skrefum:

    1. Á flipanum **Sjóðsstreymisspá** skal velja **Virkja eiginleika**.
    2. Veljið **Stofna spálíkan**.

> [!NOTE]
> The **Sjóðstreymisspá** líkanþjálfun krefst gagna með 100 eða fleiri færslum sem spanna meira en eitt ár. Við mælum með að þú hafir að minnsta kosti tveggja ára gögn með meira en 1.000 færslum.

Frekari upplýsingar um afkastagetu sjóðstreymisspár er að finna í [Sjóðstreymisspár](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
