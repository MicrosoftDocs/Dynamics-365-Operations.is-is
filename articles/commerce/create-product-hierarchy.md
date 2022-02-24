---
title: Stofna nýtt afurðastigveldi
description: Þetta efni lýsir því hvernig á að stofna nýtt afurðastigveldi í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7d0c792a8590be474b05dea262ae11d15e0ada3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965212"
---
# <a name="create-a-new-product-hierarchy"></a>Stofna nýtt afurðastigveldi


[!include [banner](includes/banner.md)]

Þetta efni lýsir því hvernig á að stofna nýtt afurðastigveldi í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce styður margar smásölurásir. Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir). Hvert smásöluverslunarrás getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk. Setja verður upp allar þessar einingar áður en hægt er að stofna smásöluverslunarrás. 

Afurðastigveldi Commercer er notað til að skilgreina aðalstigveldi smásöluafurða fyrir fyrirtækið. Hægt er að nota afurðastigveldi Commerce fyrir smásölu, verðlagningu og kynningartilboð, skýrslugerð og skipulagningu úrvals. Aðeins er hægt að úthluta einum afurðastigveldi Commerce á hvert fyrirtæki.

## <a name="create-and-configure-a-product-hierarchy"></a>Stofna og stilla afurðastigveldi

Til að stofna og stilla afurðastigveldi Commerce fylgirðu þessum skrefum.

1. Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afurðastigveldi Commerce**.
1. Ef ekkert stigveldi er til ennþá, í **aðgerðaglugganum** veldu **Nýtt** til að búa til rót stigveldisins.
1. Undir **Almennt**:
    1. Í reitnum **Heiti** færirðu inn heiti.
    1. Í reitinn **Lýsing** skal færa inn lýsingu.
    1. Í reitinn **Stutt heiti** slærðu inn stutt heiti.
    1. Stilltu **Virkt** á **Já**.

## <a name="add-hierarchy-nodes"></a>Bæta við stigveldishnút

Fylgdu þessum skrefum til að bæta við stigveldishnútum.

1. Í aðgerðarúðunni velurðu **Breyta tegundastigveldi**.
1. Veldu yfirhnútinn sem þú vilt bæta nýjum hnút við og veldu síðan **Nýr flokkshnútur**.
1. Í kaflanum **Almennt** veitirðu **Heiti**, **Lýsingu**, **Stutt heiti** og **Lykilorð**.
1. Undir **Almennt**:
    1. Í reitnum **Heiti** færirðu inn heiti.
    1. Í reitinn **Lýsing** skal færa inn lýsingu.
    1. Í reitinn **Stutt heiti** slærðu inn stutt heiti.
    1. Í reitinn **Lykilorð** slærðu inn viðeigandi lykilorð.
    1. Í reitinn **Sýna röð** slærðu inn númer fyrir skjápöntunina (valfrjálst).
1. Í aðgerðaglugganum velurðu **Vista.**
1. Endurtaktu skrefin hér að ofan til að bæta við fleiri hnútum.

Eftirfarandi mynd sýnir stofnun nýs afurðastigveldishnúts.

![Stofna afurðastigveldi](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Aðrar stillingar

Einnig er hægt að úthluta flokknum eigindahópa eftir þörfum.  

## <a name="additional-resources"></a>Frekari upplýsingar

[stigveldi verslunar](retail-hierarchies.md)

[Stjórna afurðaflokkum og afurðum ](category-management-product-creation.md)

[Breyta röðun eininga markaðssetningar](custom-order-categories-nav-retail-prod-hierarchy.md)
