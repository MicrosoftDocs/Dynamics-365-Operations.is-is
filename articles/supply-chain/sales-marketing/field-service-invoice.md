---
title: Samþætta reikningssamkomulag í Field Service við reikninga með frjálsum texta í Supply Chain Management
description: Þessi grein fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla samningsreikninga í Dynamic 365 Field Service við reikninga með frjálsum texta í Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c4ef70af71ae223baaa2abb2b64428beab946e3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900884"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Samþætta reikningssamkomulag í Field Service við reikninga með frjálsum texta í Supply Chain Management

[!include[banner](../includes/banner.md)]



Þessi grein fjallar um sniðmátin og undirliggjandi verkefni sem notuð eru til að samstilla samningsreikninga úr Dynamics 365 Field Service við reikninga með frjálsum texta í Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að keyra samstillingu samkomulagsreikninga frá Field Service við reikninga með frjálsum texta í Supply Chain Management.

**Heiti sniðmátsins í Gagnaflutningi**

- Samkomulagsreikningar (Field Service til Supply Chain Management)

**Heiti verksins í gagnasamþættingarverki**

- Reikningshausar
- Línur á reikningi

Eftirfarandi samstillingar er krafist áður en samstilling samningsreikninga getur farið fram:

- Lyklar (Sales til Supply Chain Management) - Beint

## <a name="entity-set"></a>Einingastamstæða

| Field Service  | Birgðakeðjustjórnun                 |
|----------------|----------------------------------------|
| reikningar       | Dataverse textareikningsausar viðskiptavinar |
| invoicedetails | Dataverse textareikningslínur viðskiptavinar   |

## <a name="entity-flow"></a>Einingaflæði

Reikningar sem eru búnir til úr samningi í Field Service má samstilla við Supply Chain Management með Microsoft Dataverse gagnasamþættingarverki. Uppfærslur á þessum reikningum verða samstilltar við reikninga með frjálsum texta í Supply Chain Management ef bókhaldsstaða reiknings með frjálsum texta er **Í vinnslu**. Eftir að reikningar með frjálsum texta eru bókaðir í Supply Chain Management og bókhaldsstaðan er uppfærð í **Lokið** verður ekki lengur hægt að samstilla uppfærslur frá Field Service.

## <a name="field-service-crm-solution"></a>CRM-lausn Field Service

Dálkinum **Er með línur með samningsuppruna** hefur verið bætt við töfluna **Reikningur**. Þessi reitur hjálpar til við að tryggja að aðeins reikningar sem eru búnir til úr samningi séu samstilltir. Gildið er **rétt** ef reikningurinn inniheldur að minnsta kosti eina reikningslínu sem kemur upprunalega úr samningi.

Dálkinum **Er með samingsuppruna** hefur verið bætt við töfluna **Reikningslína**. Þessi dálkur hjálpar til við að tryggja að aðeins reikningslínur sem eru búnar til úr samningi séu samstilltar. Gildið er **rétt** ef reikningslínan kemur upprunalega úr samningi.

**Reikningsdagsetning** er áskilinn reitur í Supply Chain Management. Þess vegna verður dálkurinn að hafa gildi í Field Service áður en samstillingin er gerð. Til að uppfylla þessa kröfu er eftirfarandi reglu bætt við:

- Ef dálkurinn **Reikningsdagsetning** er auður á töflunni **Reikningur** (það er ef hann hefur ekkert gildi) er hann stilltur á núverandi dagsetningu þegar reikningslínu sem er upprunnin úr samningi er bætt við.
- Notandi getur breytt dálkinum **Reikningsdagsetning**. Hins vegar, þegar notandi reynir að vista reikning sem er upprunninn úr samningi, fær hann viðskiptaferilsvillu ef dálkurinn **Reikningsdagsetning** er auður á reikningi.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

### <a name="in-supply-chain-management"></a>Í Supply Chain Management

Setja verður upp uppruna reiknings fyrir samþættinguna til að greina reikninga með frjálsum texta í Supply Chain Management sem eru búnir til úr samningsreikningum í Field Service. Þegar reikningur hefur uppruna reiknings af gerðinni **Samþætting samningsreiknings** er reiturinn **Ytra reikningsnúmer** sýndur á haus **Sölureiknings**.

Fyrir utan að birtast á reikningshausnum, er hægt að nota upplýsingarnar **Ytra reikningsnúmer** til að tryggja að reikningar sem eru búnir til úr samningsreikningum Field Service séu síaðir út við samstillingu reikninga úr Supply Chain Management við Field Service.

1. Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Upprunakóðar reiknings**.
2. Veldu **Nýr** til að búa til nýjan uppruna reiknings.
3. Í reitnum **Uppruni reiknings** skal færa inn heiti fyrir uppruna reiknings, t.d. **FS**.
4. Í reitnum **Lýsing** skal færa inn lýsingu, t.d. **Samningsreikningur Field Service**.
5. Veldu gátreitinn **Úthlutun upprunagerðar**.
6. Stillið reitinn **Uppgrunagerð reiknings** á **Samþætting samningsreiknings**.
7. Veldu **Vista**.

### <a name="in-the-data-integration-project"></a>Í gagnasamþættingarverkinu

Verkefni: **Reikningslínur**  

Gakktu úr skugga um að sjálfgefið gildi fyrir Supply Chain Management reitinn **Birt gildi aðallykils** sé uppfært til að passa við æskilegt gildi.

Sjálfgefið sniðmátsgildi er **401100**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

Eftirfarandi myndir sýna sniðmátsvörpunina í Gagnasamþættingu.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Samkomulagsreikningar (Field Service til Supply Chain Management): Reikningshausar

[![Sniðmátsvörpun í Gagnasamþættingu fyrir reikningshausa.](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Samkomulagsreikningar (Field Service til Supply Chain Management): Reikningslínur

[![Sniðmátsvörpun í Gagnasamþættingu fyrir reikningslínur.](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]