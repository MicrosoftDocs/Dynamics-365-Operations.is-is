---
title: Samstilla samkomulagsreikninga í Field Service við reikninga með frjálsum texta í Finance and Operations
description: Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla samningsreikninga úr Microsoft Dynamics 365 for Field Service við reikninga með frjálsum texta í Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "333255"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Samstilla reikningssamkomulag í Field Service við reikninga með frjálsum texta í Finance and Operations

[!include[banner](../includes/banner.md)]

Þetta efnisatriði fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla samningsreikninga úr Microsoft Dynamics 365 for Field Service við reikninga með frjálsum texta í Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að keyra samstillingu samkomulagsreikninga frá Field Service við reikninga með frjálsum texta í Finance and Operations.

**Heiti sniðmátsins í Gagnaflutningi:**

- Samningsreikningar (Field Service við Fin and Ops)

**Heiti verksins í gagnasamþættingarverki:**

- Reikningshausar
- Reikningslínur

Eftirfarandi samstillingar er krafist áður en samstilling samningsreikninga getur farið fram:

- Lyklar (Sales til Fin and Ops) - Beint

## <a name="entity-set"></a>Einingastamstæða

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| reikningar       | Frjálstextareikningshausar CDS viðskiptavinar |
| invoicedetails | Frjálstextareikningslínur CDS viðskiptavinar   |

## <a name="entity-flow"></a>Einingaflæði

Reikningar sem eru búnir til úr samningi í Field Service má samstilla við Finance and Operations með Common Data Service (CDS) gagnasamþættingarverki. Uppfærslur á þessum reikningum verða samstilltar við reikninga með frjálsum texta í Finance and Operations ef bókhaldsstaða reiknings með frjálsum texta er **Í vinnslu**. Eftir að reikningar með frjálsum texta eru bókaðir í Finance and Operations og bókhaldsstaðan er uppfærð í **Lokið** verður ekki lengur hægt að samstilla uppfærslur frá Field Service.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service

Reitnum **Er með línur með samningsuppruna** hefur verið bætt við eininguna **Reikningur**. Þessi reitur hjálpar til við að tryggja að aðeins reikningar sem eru búnir til úr samningi séu samstilltir. Gildið er **rétt** ef reikningurinn inniheldur að minnsta kosti eina reikningslínu sem kemur upprunalega úr samningi.

Reitnum **Er með samingsuppruna** hefur verið bætt við eininguna **Reikningslína**. Þessi reitur hjálpar til við að tryggja að aðeins reikningslínur sem eru búnar til úr samningi séu samstilltar. Gildið er **rétt** ef reikningslínan kemur upprunalega úr samningi.

**Reikningsdagsetning** er áskilinn reitur í Finance and Operations. Þess vegna verður reiturinn að hafa gildi í Field Service áður en samstillingin er gerð. Til að uppfylla þessa kröfu er eftirfarandi reglu bætt við:

- Ef reiturinn **Reikningsdagsetning** er auður á einingunni **Reikningur** (það er ef hann hefur ekkert gildi) er hann stilltur á núverandi dagsetningu þegar reikningslínu sem er upprunnin úr samningi er bætt við.
- Notandi getur breytt reitnum **Reikningsdagsetning**. Hins vegar, þegar notandi reynir að vista reikning sem er upprunninn úr samningi, fær hann eða hún viðskiptaferilsvillu ef reiturinn **Reikningsdagsetning** er auður á reikningi.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="in-finance-and-operations"></a>Í Finance and Operations

Setja verður upp uppruna reiknings fyrir samþættinguna til að greina reikninga með frjálsum texta í Finance and Operations sem eru búnir til úr samningsreikningum í Field Service. Þegar reikningur hefur uppruna reiknings af gerðinni **Samþætting samningsreiknings** er reiturinn **Ytra reikningsnúmer** sýndur á haus **Sölureiknings**.

Fyrir utan að birtast á reikningshausnum, er hægt að nota upplýsingarnar **Ytra reikningsnúmer** til að tryggja að reikningar sem eru búnir til úr samningsreikningum Field Service séu síaðir út við samstillingu reikninga úr Finance and Operations við Field Service.

1. Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Upprunakóðar reiknings**.
2. Veldu **Nýr** til að búa til nýjan uppruna reiknings.
3. Í reitnum **Uppruni reiknings** skal færa inn heiti fyrir uppruna reiknings, t.d. **FS**.
4. Í reitnum **Lýsing** skal færa inn lýsingu, t.d. **Samningsreikningur Field Service**.
5. Veldu gátreitinn **Úthlutun upprunagerðar**.
6. Stillið reitinn **Uppgrunagerð reiknings** á **Samþætting samningsreiknings**.
7. Veldu **Vista**.

### <a name="in-the-data-integration-project"></a>Í gagnasamþættingarverkinu

Verkefni: **Reikningslínur**  

Gakktu úr skugga um að sjálfgefið gildi fyrir Finance and Operations reitinn **Birt gildi aðallykils** sé uppfært til að passa við æskilegt gildi.

Sjálfgefið sniðmátsgildi er **401100**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Samningsreikningar (Field Service to Fin og Ops): Reikningshausar

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Samningsreikningar (Field Service to Fin og Ops): Reikningslínur

[![Sniðmátsvörpun í Gagnasamþættingu](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
