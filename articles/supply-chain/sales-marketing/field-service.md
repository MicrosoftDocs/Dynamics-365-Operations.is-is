---
title: "Samþætting við Microsoft Dynamics 365 for Field Service"
description: "Þetta efnisatriði veitir yfirlit yfir samþættingu við Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: is-is
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Samþætting við Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations virkjar samstillingu viðskiptaferla milli Finance and Operations og Microsoft Dynamics 365 for Field Service. Samþættingarsviðin eru grunnstillt með því að nota sniðmát teygjanlegrar gagnasamþættingar og Common Data Service (CDS) til að gera samþættingu viðskiptaferla virka.
Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum viðbótarreitum og einingum, til að aðlaga samþættinguna og uppfylla sérstakar viðskiptaþarfir. 

Samþætting field service byggir ofan á fyrirliggjandi prospect-to-cash virknina.

![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/field-service-integration.png)

Fyrsti áfangi samþættingar milli Field Service og Finance and Operations einblínir á að gera kleift að reikningsfæra vinnupantanir og samninga frá Field Service til Finance and Operations. Studda flæðið byrjar í Field Service, þar sem upplýsingar frá vinnupöntunum eru samstilltar við Finance and Operations sem sölupantanir. Í Finance and Operations eru sölupantanir reikningsfærðar til að búa til reikningsskjöl. Að auki eru upplýsingarnar frá samþykktum reikningum Field Service samstilltar við Finance and Operations. Gagnasamþætting Microsoft Dynamics 365 samstillir gögn með sérsniðnum verkum. Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum viðbótarreitum, ásamt einingum, til að aðlaga samþættinguna og uppfylla sérstakar kröfur.

Fyrsti áfangi samþættingar milli Field Service og Finance og Operations virkjar samstillingu á eftirfarandi atriðum:

- [Afurðir í Finance and Operations við afurðir í Field Service sem innihalda upplýsingar um gerð afurðar](field-service-product.md)
- [Vinnupantanir í Field Service við sölupantanir í Finance and Operations](field-service-work-order.md)
- [Reikningar í Field Service við reikninga með frjálsum texta í Finance and Operations](field-service-invoice.md)

Til að sjá dæmi um hvernig þú getur samstillt vinnupöntun milli Field Service og Finance and Operations skaltu horfa á stutta YouTube vídeóið [Hvernig á að samstilla vinnupöntun við Microsoft Dynamics 365 samþættingu](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Kerfisskilyrði fyrir Finance and Operations
Samþætting Field Service styður eftirfarandi útgáfur:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations útgáfa 8.0 (apríl 2018) eða nýrri

- Dynamics 365 for Finance and Operations útgáfa 8.0 (apríl 2018) var gefin út í apríl 2018 og hefur útgáfunúmer forrits 8.0.30.8020 með verkvangsuppfærslu 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Kerfisskilyrði fyrir Field Service
Til að nota samþættingarlausn Field Service verður að setja upp eftirfarandi hluti:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 eða nýrri

- Dynamics 365 for Field Service útgáfa 1612 (9.0.1.733) (DB 9.0.1.733) á netinu eða nýrri útgáfa.
- Prospect to Cash (P2C) lausn fyrir Dynamics 365, útgáfa 1.15.0.1 eða nýrri útgáfa. Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Samþættingarlausn Field Service fyrir Dynamics 365, útgáfa 1.0.0.0 eða nýrri útgáfa. Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Samþætting við Microsoft Dynamics 365 for Field Service, þ.m.t. birgðir og verkupplýsingar

Viðbótarvirknin í þessum seinni áfanga lagði áherslu á að veita tæknimönnum á vettvangi innsýn í birgðaupplýsingar frá Finance and Operations, sem gerir þeim kleift að uppfæra birgðastöður og sjá um flutning á efni. Að auki njóta fyrirtæki, sem setja upp eða þjónusta seldar vörur, ávinnings af betri stýringu og sýnileika á sölu- og þjónustuferlinu út í gegn með samþættingu frá verkum.

### <a name="functionality-includes-integration-of"></a>Virkni felur í sér samþættingu á:
- Upplýsingum um vöruhúsa
- Upplýsingum um lagerbirgðir
- Birgðaflutningum
- Leiðrétting birgða
- Verk Dynamics 365 for Finance and Operations tengd við vinnupantanir Dynamics 365 for Field Service
- Vinnupantanir Dynamics 365 for Field Service með tengingu við verk Dynamics 365 for Finance and Operations, nota þetta verknúmer á sölupöntun Dynamics 365 for Finance and Operations til að gera reikningsfærslu úr verkinu mögulega. 

![Samstilling viðskiptaferla milli Finance and Operations og Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Seinni áfangi samþættingar milli Field Service og Finance and Operations virkjar samstillingu við eftirfarandi sniðmát:
- Vöruhús (Fin and Ops til Field Service) - Vöruhús frá Finance and Operations til Field Service [Ítarleg fyrirspurn] 
- Birgðir afurðar (Fin and Ops til Field Service) - Upplýsingar um birgðastöðu frá Finance and Operations til Field Service [Ítarleg fyrirspurn] 
- Leiðrétting birgða (Field Service til Fin and Ops) - Leiðrétting birgða frá Field Service til Finance and Operations [Ítarleg fyrirspurn] 
- Birgðaflutningur (Field Service til Fin and Ops) - Birgðaflutningur frá Field Service til Finance and Operations [Ítarleg fyrirspurn] 
- Verk (Fin and Ops til Field Service) - Verklisti frá Finance and Operations til Field Service [Ítarleg fyrirspurn] 
- Vinnupantanir með Project (Field Service til Fin and Ops) - Vinnupantanir í Field Service til sölupantana  í Finance and Operations, með stuðningi fyrir Project [Ítarleg fyrirspurn] 
- Afurðir Field Service með birgðaeiningu (Fin and Ops til Sales) - „Seljanlegar útgefnar afurðir“ Finance and Operations til „afurða“ Sales fyrir Field Service, þ.m.t. birgðaeiningu 

## <a name="system-requirements-for-finance-and-operations"></a>Kerfisskilyrði fyrir Finance and Operations
Samþætting Field Service styður eftirfarandi útgáfur:

- Dynamics 365 for Finance and Operations útgáfa 8.1.2 (desember 2019) var gefin út í desember 2019 og hefur útgáfunúmer forrits 8.1.195 með verkvangsuppfærslu 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Kerfisskilyrði fyrir Field Service
Til að nota samþættingarlausn Field Service verður að setja upp eftirfarandi hluti:

- Field Service for Dynamics 365 (útgáfa 8.2.0.286) eða nýrri útgáfa á Dynamics 365 9.1.x - Gefin út í nóvember 2018
- Prospect to Cash (P2C) lausn fyrir Dynamics 365, útgáfa 1.15.0.1 eða nýrri útgáfa. Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Samþætting Field Service, verk- og birgðalausnir fyrir Dynamics 365, útgáfa 2.0.0.0 eða nýrri útgáfa. Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

