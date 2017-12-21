---
title: Prospect to cash
description: "Þetta efnisatriði veitir yfirlit yfir Prospect to cash lausnarinnar á milli Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: is-is
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Prospect to cash

[!include[banner](../includes/banner.md)]

Prospect to cash lausnin veitir beina samstillingu milli Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition og Micorosoft Dynamics 365 for Sales. Prospect to cash sniðmát sem eru í boði með eiginleika gagnasamþættingar leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantanir og sölureikninga milli Finance and Operations og Sales. Á meðan gögnin flæði á milli Finance and Operations og Sales er hægt að framkvæma sölu- og markaðsstarf í Sales og meðhöndla pöntunaruppfyllingu með því að nota birgðastjórnun í Finance and Operations.

Í núverandi útgáfu býður Prospect to cash lausnin upp á eftirfarandi gerðir af beinni samstillingu:

- [Viðhalda reikningum í Sales og samstilla þá beint úr Sales við Finance and Operations](accounts-template-mapping-direct.md)
- [Viðhalda vörum í Finance and Operations og samstilla þær beint við Sales](products-template-mapping-direct.md)
- [Viðhalda tengiliðum í Sales og samstilla þá beint við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping-direct.md)
- [Samstilla sölutilboð beint úr Sales við Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Samstilla sölupantanir beint úr Finance and Operations við Sales](sales-order-template-mapping-direct.md)
- [Samstilla sölupantanir beint úr Sales við Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Samstilla sölureikninga beint úr Finance and Operations við Sales](sales-invoice-template-mapping-direct.md)

Í fyrri útgáfum veitir Prospect to cash lausnin eftirfarandi gerðir af óbeinni samstillingu:

- [Viðhalda reikningum í Sales og samstilla þá við Finance and Operations](accounts-template-mapping.md)
- [Viðhalda tengiliðum í Sales og samstilla þá við Finance and Operations](contacts-template-mapping.md)
- [Viðhalda vörum í Finance and Operations og samstilla þær við Sales](products-template-mapping.md)
- [Búa til sölutilboð í Sales og samstilla þau við Finance and Operations](sales-quotation-template-mapping.md)
- [Búa til sölupantanir í Finance and Operations og samstilla þær við Sales](sales-order-template-mapping.md)
- [Búa til sölureikninga í Finance and Operations og samstilla þá við Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Kerfisskilyrði fyrir Finance and Operations

Eftirfarandi einingar verður að setja upp áður en Prospect to cash lausin er notað:

### <a name="july-2017"></a>Júlí 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (July 2017) með verkvangsuppfærslu 8 (Forrit smíð 7.2.11792.56024 með verkvangur smíð 7.0.4565.16212)
- Eftirfarandi bráðabætur fyrir Finance and Operations:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Sales til Finance and Operations gegnum gagnasamþættingareiginleikann. Það veitir einnig nokkrar aðrar endurbætur.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupöntunarlína frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.

    > [!NOTE]
    > Þú þarft aðeins að setja upp KB4045570 vegna þess að uppsetningin inniheldur breytingar frá greinum í hinum Microsoft Þekkingargrunninum (KB).

### <a name="november-2016-version-1611"></a>Nóvember 2016 (útgáfa 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (nóvember 2016) með verkvangsuppfærslu 8 eða hærra.

- Eftirfarandi bráðabætur fyrir Finance and Operations:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Gera samstillingu sölupantana við gagnasamþættingu mögulega frá Microsoft Dynamics 365 for Finance and Operations til Sales. 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Gera samstillingu sölupantanahausa og lína við gagnasamþættingu mögulega frá Microsoft Dynamics 365 for Finance and Operations til Sales.
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Stuðningi við prospect to cash samþættingu gegnum gagnaeiningar er krafist
    
    > [!NOTE]
    > Eftir að hafa sett upp bráðabætur þarftu að kveikja á eftirfarandi runuvinnslu frá skjámyndinni SalesPopulateProspectToCash. Þetta form er falið þar sem þú þarft aðeins einu sinni. Til að fá aðgang að því skaltu bæta eftirfarandi við vafrafangið þitt, þegar þú ert skráð(ur) inn í umhverfið: &mi=action:SalesPopulateProspectToCash E.g. https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash Í skjámyndinni sem opnast skaltu smella á Í lagi.
    Þetta mun fylla upp í nýjan „LineCreationSequnceNumber“ reit í „SalesLine“, „SalesQuotationLine“ og „CustInvoiceTrans“ töflunum með einkvæmum gildum og endurhlaða afurðalistann. Þetta er nauðsynlegt til þess að P2C samþættingin virki á 7.1


## <a name="system-requirements-for-sales"></a>Kerfisskilyrði fyrir Sales

Eftirfarandi einingar verður að setja upp áður en Prospect to cash lausin er notað:

- Microsoft Dynamics 365 for Sales útgáfa 1612 (8.2.1.207) (DB 8.2.1.207) á netinu.
- Prospect to cash lausn fyrir Microsoft Dynamics 365 for Sales, útgáfa 1.15.0.0 (v15). 

   > [!NOTE]
   >
   > Sniðmát með útgáfu 1.0.0.0 og 1.0.0.1 eru studd á Prospect to cash lausn fyrir Microsoft Dynamics 365 for Sales, útgáfa 1.14.1.0
   >
   > Sniðmát með útgáfu 2.0.0.0 og 2.1.0.0 eru studd á Prospect to cash lausn fyrir Microsoft Dynamics 365 for Sales, útgáfa 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Settu upp Prospect to cash lausn fyrir Sales

1. Sæktu [Prospect to cash fyrir Dynamics 365 for Sales lausn pakki zip-skrá](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) frá CustomerSource.
2. Gakktu úr skugga um að opið sé fyrir zip-skrána. Annars birtast eftirfarandi villuboð þegar þú reynir að setja upp lausnapakkann: „Fann enga uppsetningarpakka.“ Til að opna fyrir zip-skrána, skaltu hægrismella á hana og velja **Eiginleikar**. Veldu síðan **Opna fyrir**.
3. Afþjappaðu hana og keyrðu **PackageDeployer.exe**.
4. Settu upp Prospect to Cash lausn á Sales tilvikinu þínu:

    1. Veldu **Office 365** sem uppsetningartegund.
    2. Veldu **Sýna ítarlegt**.
    3. Veldu svæði fyrir skjóta uppsetningu. Ef þú velur **Veit ekki** leitar kerfið að öllum svæðum og uppsetning tekur lengri tíma.
    4. Sláðu inn Notandanafn og Aðgangsorð kerfisnotanda sem hefur leyfi til að setja upp.

