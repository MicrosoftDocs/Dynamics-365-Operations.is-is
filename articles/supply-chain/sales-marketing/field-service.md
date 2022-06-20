---
title: Samþættingu við yfirlit yfir Microsoft Dynamics 365 Field Service
description: Þessi grein veitir yfirlit yfir samþættingu við Microsoft Dynamics 365 Field Service.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b0427d33ac39d34bccc302e58bb84e1ad4c3598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888442"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Samþættingu við yfirlit yfir Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]



Supply Chain Management virkjar samstillingu viðskiptaferla á milli Dynamics 365 Supply Chain Management og Dynamics 365 Field Service. Samþættingarsviðin eru grunnstillt með því að nota sniðmát teygjanlegrar gagnasamþættingar og Microsoft Dataverse til að gera samþættingu viðskiptaferla virka.
Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum dálkum og töflum , til að aðlaga samþættinguna og uppfylla sérstakar viðskiptaþarfir. 

Samþætting field service byggir ofan á fyrirliggjandi prospect-to-cash virknina.

![Samstilling viðskiptaferla milli Supply Chain Management og Field Service.](./media/field-service-integration.png)

Fyrsti áfangi samþættingar milli Field Service og Supply Chain Management einblínir á að gera kleift að reikningsfæra vinnupantanir og samninga frá Field Service til Supply Chain Management. Studda flæðið byrjar í Field Service, þar sem upplýsingar frá vinnupöntunum eru samstilltar við Supply Chain Management sem sölupantanir. Í Supply Chain Management eru sölupantanir innheimtir til að búa til reikningsgögn. Að auki eru upplýsingarnar frá samþykktum reikningum Field Service samstilltar við Supply Chain Management. Gagnasamþætting Microsoft Dynamics 365 samstillir gögn með sérsniðnum verkum. Hægt er að nota stöðluð sniðmát til að búa til sérsniðin samþættingarverk þar sem hægt er að varpa stöðluðum og sérsniðnum dálkum og töflum , til að aðlaga samþættinguna og uppfylla sérstakar þarfir.

Fyrsti áfangi samþættingar milli Field Service og Supply Chain Management virkjar samstillingu á eftirfarandi atriðum:

- [Samstilla vörur í Supply Chain Management við vörur í Field Service](field-service-product.md)
- [Samstilla vinnupantanir úr Field Service við sölupantanir í Supply Chain Management](field-service-work-order.md)
- [Samþætta reikningssamkomulag í Field Service við reikninga með frjálsum texta í Supply Chain Management](field-service-invoice.md)

Til að sjá dæmi um hvernig þú getur samstillt vinnupöntun milli Field Service og Supply Chain Management skaltu horfa á stutta YouTube vídeóið [Hvernig á að samstilla vinnupöntun við Microsoft Dynamics 365 samþættingu](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Samþætting við Field Service, þ.m.t. birgðir og verkupplýsingar

Viðbótarvirknin í þessum seinni áfanga lagði áherslu á að veita tæknimönnum á vettvangi innsýn í birgðaupplýsingar frá Supply Chain Management, sem gerir þeim kleift að uppfæra birgðastöður og sjá um flutning á efni. Að auki njóta fyrirtæki, sem setja upp eða þjónusta seldar vörur, ávinnings af betri stýringu og sýnileika á sölu- og þjónustuferlinu út í gegn með samþættingu frá verkum.

### <a name="functionality-includes-integration-of"></a>Virkni felur í sér samþættingu á:
- Upplýsingum um vöruhúsa
- Upplýsingum um lagerbirgðir
- Birgðaflutningum
- Leiðrétting birgða
- Verkefni Supply Chain Management tengd verkbeiðnir Dynamics 365 Field Service
- Dynamics 365 Field Service vinnupantanir með tengli við verk Supply Chain Management, nota þetta verknúmer á sölupöntun til að gera reikningsfærslu úr verkinu mögulega. 

![Samstilling viðskiptaferla milli Supply Chain Management og Field Service, þ.m.t. upplýsingar um birgðir og verk.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Seinni áfangi samþættingar milli Field Service og Supply Chain Management virkjar samstillingu við eftirfarandi sniðmát:
- Vöruhús (Framboðsstjórnun að sviði þjónustu) - Vöruhús frá Supply Chain Management til Field Service [Ítarleg fyrirspurn] 
- Birgðir afurðar (Supply Chain Management að Field Service) - Upplýsingar um birgðastöðu frá Supply Chain Management til Field Service [Ítarleg fyrirspurn] 
- Leiðrétting birgða (Field Service til Supply Chain Management) - Leiðrétting birgða frá Field Service til Supply Chain Management [Ítarleg fyrirspurn] 
- Birgðaflutningar (Field Service til Supply Chain Management) - Birgðaflutningar frá Field Service til Supply Chain Management [Ítarleg fyrirspurn] 
- Verk (Supply Chain Management að Field Service) - Verklisti frá Supply Chain Management til Field Service 
- Vinnupantanir með Project (Field Service til Supply Chain Management) - Vinnupantanir í Field Service til sölupantana í Supply Chain Management, með stuðningi fyrir Project [Ítarleg fyrirspurn] 
- Afurðir Field Service með birgðaeiningu (Supply Chain Management til Sales) - Supply Chain Management „Seljanlegar útgefnar afurðir“ Finance and Operations til „afurða“ Sales fyrir Field Service, þ.m.t. birgðaeiningu 

## <a name="system-requirements"></a>Kerfiskröfur

### <a name="system-requirements-for-supply-chain-management"></a>Kerfiskröfur fyrir Supply Chain Management
Samþætting Field Service styður eftirfarandi útgáfur:

- Dynamics 365 for Finance and Operations útgáfa 8.1.2 (desember 2018) var gefin út í desember 2018 og hefur útgáfunúmer forrits 8.1.195 með verkvangsuppfærslu 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Kerfisskilyrði fyrir Field Service
Til að nota samþættingarlausn Field Service verður að setja upp eftirfarandi hluti:

- Field Service (útgáfa 8.2.0.286) eða nýrri útgáfa á Dynamics 365 9.1.x - Gefin út í nóvember 2018
- Prospect to Cash (P2C) lausn fyrir Dynamics 365, útgáfa 1.15.0.1 eða nýrri útgáfa. Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- Samþætting Field Service, verk- og birgðalausnir fyrir Dynamics 365, útgáfa 2.0.0.0 eða nýrri útgáfa. Lausnina er hægt að sækja hjá [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]