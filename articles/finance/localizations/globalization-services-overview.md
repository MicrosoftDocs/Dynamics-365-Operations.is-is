---
title: Altæk þjónusta Dynamics 365
description: Þetta efnisatriði sýnir yfirlit yfir altækar þjónustur Microsoft Dynamics 365.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 3fa4d5ea028e4b8bb0981674db2743df40348a9a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336609"
---
# <a name="dynamics-365-globalization-services"></a>Altæk þjónusta Dynamics 365

[!include [banner](../includes/banner.md)]

Hægt er að skilgreina eftirfarandi altækar þjónustur til að stækka möguleikana sem eru til staðar í sumum þjónustum Microsoft Dynamics 365 Online:

- **Regulatory Configuration Service (RCS)** styður skilgreiningu mismunandi gerða af rafrænum skjölum og skýrslum. RCS býður upp á bætta útgáfu af hönnuði rafrænnar skýrslugerðar þar sem skilgreiningageymslan er sjálfstæð þjónusta. Frekari upplýsingar er að finna í [Regulatory Configuration Service](rcs-overview.md).
- **Rafræn reikningsfærsla** sameinar stillanleg snið fyrir umbreytingar, stafrænar undirritanir og stillanlegar samþættingar fyrir tengingar við ytri vefþjónustur, þ.m.t. vottun og meðhöndlun svara. Frekari upplýsingar eru í [Rafrænar reikningsfærslur](e-invoicing-service-overview.md).
- **Skattaútreikningur** býður upp á aukinn sveigjanleika með því að styðja mörg skattkenni, ákvörðun skattkóða, hönnuð skattaútreiknings og keyrsluvél til að fylgja eftir flóknum skattareglum á heimsvísu. Nánari upplýsingar eru í [Skattaútreikningur](global-tax-calcuation-service-overview.md).

Þessar altæku þjónustur bjóða upp á tilbúna samþættingu við eftirfarandi þjónustur Dynamics 365 á netinu.

| Þjónusta á netinu | RCS | Rafræn reikningsfærsla | Skattaútreikningur (forskoðun) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Já | Já | Já | 
| Dynamics 365 Supply Chain Management | Já | Já | Já | 
| Dynamics 365 Project Operations | Já | Já | Ekki tiltækt | 
| Dynamics 365 Commerce | Já | Ekki tiltækt | Ekki tiltækt | 

> [!NOTE]
> Vegna þess að landfræðilegar staðsetningar Azure veita mismunandi aðgengi að RCS, gæti skilgreining á þessari þjónustu orðið til þess að gögn viðskiptavinar verði flutt út fyrir staðsetninguna sem er valin fyrir þá þjónustu Dynamics 365 á netinu sem á við. Frekari upplýsingar er að finna í [Dynamics 365 og Power Platform: Aðgengileiki, staðsetning gagna, tungumál og staðfærsla](https://aka.ms/rcs/D365Productavailabilityguide).