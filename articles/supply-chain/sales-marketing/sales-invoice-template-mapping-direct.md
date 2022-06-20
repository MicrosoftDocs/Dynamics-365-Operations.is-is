---
title: Samstilla hausa og línur sölureiknings beint úr Supply Chain Management í Sales
description: Þessi grein fjallar um sniðmát og undirliggjandi verkefni sem eru notuð til að samstilla hausa og línur sölureikninga beint frá Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: Henrikan
ms.date: 10/26/2017
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
ms.openlocfilehash: de4bdd07127b65321540543040192eb7811850da
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862541"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Samstilla hausa og línur sölureiknings beint úr Sales við Finance and Operations

[!include [banner](../includes/banner.md)]

Þessi grein fjallar um sniðmát og undirliggjandi verkefni sem eru notuð til að samstilla hausa og línur sölureikninga beint frá Dynamics 365 Supply Chain Management til Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gagnaflæði í Prospect to cash

Prospect to lausnin notar gagnasamþættingu til að samstilla gögn yfir tilvik Supply Chain Management og Sales. Prospect to cash sniðmát sem eru í boði með gagnasamþættingu leyfir flæði gagna um reikninga, tengiliði, vörur, sölutilboða, sölutilboð, sölupantana og sölureikningagagna milli Supply Chain Management og Sales. Eftirfarandi mynd sýnir hvernig gögnin eru samstillt milli Supply Chain Management og Sales.

[![Gagnaflæði í Prospect to cash.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sniðmát og verkefni

Til að opna fyrirliggjandi sniðmát skaltu opna [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration). Veldu **Verk** og svo, í efra hægra horninu, velurðu **Nýtt verk** til að velja opin sniðmát.

Eftirfarandi sniðmát og undirliggjandi verkefni eru notuð til að samstilla reikningshausa og línur úr Supply Chain Management í Sales:

- **Heiti sniðmátsins í Gagnaflutningi:** Sölureikningar (Fin og Ops í Sales) - beint
- **Heiti verksins í gagnasamþættingarverki:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Eftirfarandi samstillingarverkefni eru nauðsynleg áður en samstillingar sölureikningshausa og línum geta átt sér stað:

- Afurðir (Supply Chain Management itl Sales) - Beint
- Lyklar (Sales til Supply Chain Management) - Bein (ef notað)
- Tengiliðir (Sales til Supply Chain Management) - Bein (ef notað)
- Hausar og línur sölupantana (Supply Chain Management í Sales) - Beint

## <a name="entity-set"></a>Einingastamstæða

| Birgðakeðjustjórnun                              | Sala          |
|------------------------------------------------------|----------------|
| Sölureikningshausar viðskiptavinar sem unnið er með utan frá | Reikningar       |
| Sölureikningslínur viðskiptavinar sem unnið er með utan frá   | InvoiceDetails |

## <a name="entity-flow"></a>Einingaflæði

Sölureikningar eru búnir til í Supply Chain Management og samstilltir við Sales.

> [!NOTE]
> Eins og er er skattur tengdur gjöldum á sölureikningshaus er ekki tekinn með í samstillingu úr Supply Chain Management í Sales. Sales styður ekki skattupplýsingar á hausstiginu. Hinsvegar er skattur sem tengist gjöldum á línustigi er innifalinn í samstillingu.

## <a name="prospect-to-cash-solution-for-sales"></a>Prospect to cash lausn fyrir Sales

- Reitnum **Reikningsnúmer** er bætt við eininguna **Reikningur** og birtur á síðunni.
- Hnappurinn **Stofna reikning** á **Sölupöntun** síðunni er falinn vegna þess að reikningar verða búnir til í Supply Chain Management og samstilltir við Sales. Ekki er hægt að breyta siðunni **Reikningur** vegna þess að reikningar verða samstilltir úr Supply Chain Management.
- **Staða sölupöntunar** breytist sjálfkrafa í **Reikningsfært** þegar tengdur reikningur úr Supply Chain Management hefur verið samstilltur við Sales. Einnig var eiganda sölupöntunar sem reikningurinn var búinn til úr úthlutað sem eiganda reikningsins. Því getur eigandi sölurekningsins skoðað reikninginn.

## <a name="preconditions-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en sölureikningar eru samstilltir er mikilvægt að eftirfarandi stillingar séu uppfærðar í kerfunum.

### <a name="setup-in-sales"></a>Uppsetning í Sales

Farið í **Stillingar** > **Stjórnun** > **Kerfisstillingar** > **Sales** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

- **Nota reikningskerfi verðs** valkosturinn er stilltur á **Já**.
- **Reikningsaðferð reikningsafslátta** reiturinn er stilltur á **Línuatriði**.

### <a name="setup-in-the-data-integration-project"></a>Setja upp gagnasamþættingarverk

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader task

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **InvoiceCountryRegionId** í **BillingAddress\_Land**.

    Sniðmátsgildið er gildisvörpun þar sem nokkur lönd eða svæði eru vörpuð.

- Verðlisti er nauðsynlegur til að búa til reikninga í Sales. Uppfæra gildarvörpun í **pricelevelid.name \[Heiti verðlista\]** í verðlistann sem er notaður í Sales eftir gjaldmiðli. Hægt er að nota sjálfgefinn verðlista fyrir einn gjaldmiðil. Einnig er hægt að nota gildarvörpun ef verðlistar eru til staðar í mörgum gjaldmiðlum.

    Sniðmátsgildið fyrir **pricelevelid.name \[Heiti verðlista\]** er gildisvörpun sem byggir á gjaldmiðli með USD = CRM Service USA (dæmi).  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine verkefni

- Gangið úr skugga um að nauðsynleg vörpun sé til staðar fyrir **Mælieining**.
- Gangið úr skugga um að nauðsynleg gildisvörpun fyrir **SalesUnitSymbol** í Supply Chain Management sé til staðar.

    Sniðmátsgildi með gildisvörpun er skiglreint fyrir **SalesUnitSymbol** í **Magn\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Sniðmátsvörpun í Gagnasamþættingu

> [!NOTE]
> Reitirnir **Greiðsluskilmálar**, **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum reitum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem einingin er samstillt á milli.

Eftirfarandi skýringarmynd sýnir dæmi um vörpunarsniðmát í gagnasamþættingu. 

> [!NOTE]
> Vörpunin sýnir hvaða reitaupplýsingar verða samstilltar úr Sales í Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Sniðmátsvörpun í gagnasamþættingu fyrir SalesInvoiceHeader.](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Sniðmátsvörpun í gagnasamþættingu fyrir SalesInvoiceLine.](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-articles"></a>Tengdar greinar

[Viðfang til sjóðstreymis](prospect-to-cash.md)

[Samstilla lykla beint úr Sales við viðskiptavini í Supply Chain Management](accounts-template-mapping-direct.md)

[Samstilla vörur beint úr Sales við viðskiptavini í Supply Chain Management við vörur í Sales](products-template-mapping-direct.md)

[Samstilla tengiliði beint úr Sales við tengiliði eða viðskiptavini í Supply Chain Management](contacts-template-mapping-direct.md)

[Samstilling sölupantana beint á milli Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]