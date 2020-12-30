---
title: Setja upp IoT-gervigreindarinnbótina í LCS
description: Þetta efnisatriði útskýrir hvernig á að setja upp IoT-gervigreind viðbótina í Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430645"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>Setja upp IoT-gervigreindarinnbótina í LCS

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp IoT-gervigreind viðbótina í Microsoft Dynamics Lifecycle Services (LCS). Athugaðu að ekki er hægt að setja innbætur í kynningu/prufuumhverfi. Áður en hægt er að setja upp viðbótina þarf [að stofna Azure tilföng](iot-azure-setup.md).

## <a name="set-up-the-lcs-environment"></a>Setja upp LCS-umhverfi

1. Opnaðu LCS og farðu í Microsoft Dynamics 365 Supply Chain Management umhverfið.
2. Flettu að hlutanum **Innbætur umhverfis**.
3. Veldu **Setja upp nýja innbót** til að sýna lista yfir innbætur sem hafa verið virkjaðar fyrir umhverfið.
4. Í glugganum **Velja innbót til að setja upp** skal velja **IoT-gervigreind**.
5. Í svarglugganum **Uppsetning á innbót** skal veita upplýsingar um IoT gátt og skyndiminni Redis. Hægt er að finna nauðsynleg gildi í lyklageymslunni sem stofnuð var í [Stofna Azure-tilföng](iot-azure-setup.md).

    + **Auðkenni leigjanda** – í Azure-gátt skal fara í lyklageymslu og velja síðan **Yfirlit** á vinstra yfirlitssvæði og afrita gildið **Skráasafnskenni**. Límið gildið í svarglugganum **Uppsetning á innbót**.
    + **Í samhæfri URI lyklageymslu endapunkts IoT miðstöðvar** – Farðu í lyklageymslu og veldu á vinstra yfirlitssvæðinu **Yfirlit** og afritaðu gildið **DNS-heiti**. Límið gildið í svarglugganum **Uppsetning á innbót**.
    + **Samhæft leyniorð fyrir IoT Event Hub** – Opnaðu lyklageymsluna og á vinstra yfirlitssvæðinu velurðu **Leyniorð** og afritar leyniheiti þar sem tengistrengur IoT miðstöðvar er vistaður. Límið gildið í svarglugganum **Uppsetning á innbót**.
    + **URI lyklageymslu Redis skyndiminnis** – Farðu í lyklageymslu og veldu á vinstra yfirlitssvæðinu **Yfirlit** og afritaðu gildið **DNS-heiti**. Límið gildið í svarglugganum **Uppsetning á innbót**.
    + **Leyniorð endapunkts fyrir Redis skyndiminni** – Opnaðu lyklageymsluna og á vinstra yfirlitssvæðinu velurðu **Leyniorð** og afritar leyniheitið þar sem tengistrengur Redis skyndiminnis er vistaður. Límið gildið í svarglugganum **Uppsetning á innbót**.

6. Velja þarf gátreitinn til að samþykkja skilmálana.
7. Velja **Setja upp**.
8. Skilaboðagluggi með skilaboðunum „Innbótin var sett í gang fyrir uppsetningu“ birtist. Veljið **Í lagi**.

LCS uppsetningu er nú lokið. Næsta skrefið er að [setja upp aðstæður](iot-scenario-setup.md).

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>Fjarlægja innbótina

1. Í Supply Chain Management skal [gera umhverfið óvirkt](iot-scenario-setup.md#disable-a-scenario).
2. Opnið upplýsingar umhverfis Supply Chain Management í LCS.
3. Flettu að hlutanum **Innbætur umhverfis**.
4. Veljið **Fjarlægja** fyrir innbótina IoT-gervigreind.
