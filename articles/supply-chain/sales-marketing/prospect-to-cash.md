---
title: Prospect to cash
description: "Þetta efnisatriði veitir yfirlit yfir Prospect to cash lausnarinnar á milli Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
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
ms.sourcegitcommit: ce9c24a0a89dd4e6a0f3f2c7789b4f553d88d412
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.contentlocale: is-is
ms.lasthandoff: 08/13/2018

---

# <a name="prospect-to-cash"></a>Prospect to cash

[!include [banner](../includes/banner.md)]

Prospect to cash lausnin veitir beina samstillingu milli Dynamics 365 for Finance and Operations og Dynamics 365 for Sales. Prospect to cash sniðmát sem eru í boði með eiginleika gagnasamþættingar leyfir flæði gagna fyrir reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantanir og sölureikninga milli Finance and Operations og Sales. Á meðan gögnin flæði á milli Finance and Operations og Sales er hægt að framkvæma sölu- og markaðsstarf í Sales og meðhöndla pöntunaruppfyllingu með því að nota birgðastjórnun í Finance and Operations. 

Frekari upplýsingar um samþættingu Prospect to cash er hægt að skoða í stuttu YouTube myndbandi: [Prospect to cash samþætting](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Í núverandi útgáfu býður Prospect to cash lausnin upp á eftirfarandi gerðir af beinni samstillingu:

- [Viðhalda reikningum í Sales og samstilla þá beint úr Sales við Finance and Operations](accounts-template-mapping-direct.md)
- [Vinna með afurðir í Finance and Operations og samstilla þær beint við Sales](products-template-mapping-direct.md)
- [Vinna með tengiliði í Sales og samstilla þá beint við tengiliði eða viðskiptavini í Finance and Operations](contacts-template-mapping-direct.md)
- [Samstilla sölutilboð beint úr Sales við Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Samstilla sölupantanir beint milli Sales og Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Samstilla sölureikninga beint úr Finance and Operations við Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Kerfisskilyrði fyrir Finance and Operations
Prospect to cash samþætting er studd í eftirfarandi útgáfum:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (desember 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (desember 2017) - Smíðun forrits 7.3.11971.56116 með verkvangsuppfærslu 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) með verkvangsuppfærslu 8 (Smíðun forrits 7.2.11792.56024 með verkvangssmíði 7.0.4565.16212).
- Eftirtaldir bráðabætur eru nauðsynlegar:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Sales til Finance and Operations gegnum gagnasamþættingareiginleikann. Það veitir einnig nokkrar aðrar endurbætur.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupöntunarlína frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** - Þessi bráðabót gerir mögulega samstillingu sölupantana frá Finance and Operations til Sales gegnum gagnasamþættingareiginleikann.

    > [!NOTE]
    > Þú þarft aðeins að setja upp KB4045570 vegna þess að uppsetningin inniheldur breytingar frá öðrum bráðabótum. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations útgáfa 1611 (nóvember 2016)

- Microsoft Dynamics 365 for Finance and Operations útgáfa 1611 (nóvember 2016) með verkvangsuppfærslu 8 eða hærra

- Eftirtaldir bráðabætur eru nauðsynlegar:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Gera samstillingu sölupantana við gagnasamþættingu mögulega frá Finance and Operations til Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Gera samstillingu sölupantanahausa og lína við gagnasamþættingu mögulega frá Finance and Operations til Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Stuðningi við prospect to cash samþættingu gegnum gagnaeiningar er krafist.
    
    > [!NOTE]
    > Eftir að hafa sett upp bráðabætur þarftu að kveikja á eftirfarandi runuvinnslu frá skjámyndinni **SalesPopulateProspectToCash**. Þetta form er falið þar sem þú þarft það aðeins einu sinni. Til að fá aðgang að forminu skaltu skrá þig inn í umhverfið og bæta eftirfarandi við veffang vafra þíns: *&mi=action:SalesPopulateProspectToCash*, til dæmis, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Þegar formið opnast skaltu smella á Í lagi. Þetta mun fylla upp í nýjan **LineCreationSequnceNumber** reit í **SalesLine**, **SalesQuotationLine** og **CustInvoiceTrans** töflunum með einkvæmum gildum og endurhlaða afurðalistann. Þetta er áskilið svo að Prospect to cash samþættingin virki.


## <a name="system-requirements-for-sales"></a>Kerfisskilyrði fyrir Sales

Eftirfarandi einingar verður að setja upp áður en Prospect to cash lausin er notað:

- Dynamics 365 for Sales útgáfa 1612 (8.2.1.207) (DB 8.2.1.207) á netinu eða nýrri útgáfa
- Prospect to cash lausn fyrir Dynamics 365 for Sales, útgáfa 1.15.0.0 eða nýrri útgáfa. Lausnina er hægt að sækja hjá AppSource. [Sækja Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).

