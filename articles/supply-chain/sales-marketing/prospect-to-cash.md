---
title: Prospect to cash
description: "Þetta efnisatriði veitir yfirlit yfir Prospect to cash milli Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>Prospect to cash  

[!include[banner](../includes/banner.md)]

Prospect to cash lausnin notar [Gagnasamþættingu](/common-data-service/entity-reference/dynamics-365-integration) til að samstilla gögn milli Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Dynamics 365 for Sales tilvik með Common Data Service (CDS). Prospect to cash sniðmát í boði með gagnasamþættingu leyfir flæði milli reikninga, tengiliða, vara, sölutilboða, sölupantana og sölureikningagagna milli Finance and Operations og Sales. Þegar gögnin flæði á milli Finance and Operations og Sales er hægt að framkvæma sölu- og markaðsstarf í Sales og meðhöndla pöntunina í birgðastjórnun í Finance and Operations. 

Þessi lausn veitir samþættingu á eftirfarandi sviðum: 

-   [Viðhalda reikningum í Sales og samstilla þá við Finance and Operations](accounts-template-mapping.md)
-   [Viðhalda tengiliðum í Sales og samstilla þá við Finance and Operations](contacts-template-mapping.md)
-   [Viðhalda vörum í Finance and Operations og samstilla þær við Sales](products-template-mapping.md)
-   [Búa til sölutilboð í Sales og samstilla þau við Finance and Operations](sales-quotation-template-mapping.md)
-   [Búa til sölupantanir í Finance and Operations og samstilla þær við Sales](sales-order-template-mapping.md)
-   [Búa til sölureikninga í Finance and Operations og samstilla þá við Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Kerfiskröfur fyrir Dynamics 365 for Finance and Operations, Enterprise Edition

Eftirfarandi verður að setja upp áður en Prospect to cash er notað:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017) með verkvangsuppfærslu 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)

- Tvær bráðabætur fyrir Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017).

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - Þessi bráðabót gerir samstillingu sölupöntunarlína við gagnasamþættingarkost mögulegan frá Finance and Operations við Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)- Þessi bráðabót gerir samstillingu sölupantana við gagnasamþættingarkost mögulegan frá Finance and Operations við Sales.
    
**Athugaðu**: Þú þarft aðeins að setja upp KB4036524 vegna þess að uppsetningin inniheldur breytingar frá KB4036461.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Kerfiskröfur fyrir Dynamics 365 for Sales

Eftirfarandi verður að setja upp áður en Prospect to cash er notað:

- Dynamics 365 for Sales útgáfa 1612 (8.2.1.207) (DB 8.2.1.207) á netinu eða nýrri.
- Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.14.0.0 (v14) eða nýrri.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Settu upp Prospect to cash lausn fyrir Sales

- Sæktu [Prospect to cash fyrir Dynamics 365 for Sales solution package zip-skrá](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) á CustomerSource.

- Gakktu úr skugga um að zip-skráin sé ólæst þannig að þú fáir ekki villuskilaboðin „Engir innflutningspakkar fundust“ þegar þú setur upp pakkann. Til að opna skrána skaltu gerirðu eftirfarandi:

    -  Hægrismelltu á zip-skrána.
    -  Veldu **Eiginleikar** og Svo **Opna**. 

- Opnaðu hana og keyrðu PackageDeployer.exe.

- Settu upp Prospect í Cash lausn í Sales tilvikið þitt.

    - Veldu **Office 365** Deployment.
    - Veldu **Sýna ítarlegt**.
    - Veldu **Svæði** fyrir skjóta uppsetningu. Ef þú velur **Veit ekki** leitar kerfið að öllum svæðum og uppsetning tekur lengri tíma.
    - Sláðu inn **Notandanafn** og **Aðgangsorð** kerfisnotanda sem hefur leyfi til að setja upp.

