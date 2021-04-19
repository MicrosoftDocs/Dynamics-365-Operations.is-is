---
title: Stofna virknireglu fyrir smásölu
description: Þetta efnisatriði lýsir hvernig á að stofna virknireglu í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791998"
---
# <a name="create-a-retail-functionality-profile"></a>Stofna virknireglu fyrir smásölu

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að stofna virknireglu í Microsoft Dynamics 365 Commerce.

Forstillingar viðskiptavirkni veita ýmsar stillingar sem notaðar eru fyrir netrásir. Hver rás verður að tilgreina virknireglu.

## <a name="create-a-functionality-profile"></a>Stofna virkniforstillingu

Til að stofna virknireglu skal fylgja þessum skrefum.

1. Farðu í **Einingar \> Uppsetning rásar \> POS-virknireglur \> Virknireglur**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitinn **Prófíll**, slærðu inn auðkenni fyrir sniðið („FN006” í myndinni hér að neðan).
1. Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).
1. Í kaflanum **Almennt**, veldu land fyrir **ISO** landstig.
1. Í kaflanum **Almennt**, breyttu öðrum stillingum, eftir þörfum.
1. Í kaflanum **Almennt**, veldu **Kenni kvittunarforstillingar** fyrir kvittanir í tölvupósti.
1. Í kaflanum **Aðgerðir**, breyttu stillingum, eftir þörfum.
1. Í kaflanum **Upphæð**, breyttu stillingum, eftir þörfum.
1. Í kaflanum **Upplýsingakóðar**, breyttu stillingum, eftir þörfum.
1. Í kaflanum **Kvittananúmer**, breyttu stillingum, eftir þörfum. 
  
Eftirfarandi mynd sýnir dæmi um virknireglu.
  
![Virknireglur fyrir forstillingu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Upplýsingakóðar og upplýsingakóðaflokkar](info-codes-retail.md)           

[Stofna nýja aðsetursbók](new-address-book.md) 

[Yfirlit skjáútlits](pos-screen-layouts.md)       

[Skilgreina og setja upp Retail Hardware Station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
