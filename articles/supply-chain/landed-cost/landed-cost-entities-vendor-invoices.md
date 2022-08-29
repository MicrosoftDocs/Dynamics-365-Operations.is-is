---
title: Reikningaeiningar lánardrottins
description: Þessi grein veitir upplýsingar um reikningseiningar lánardrottins, sem gera kleift að stilla kostnaðartegundakóða fyrir innri kostnað eða kostnað sem er afleiddur að utan.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: f0371cf9862afaf3bc43a44def725c420e9aaf56
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166744"
---
# <a name="vendor-invoice-entities"></a>Reikningaeiningar lánardrottins

[!include [banner](../includes/banner.md)]

The **Landaður kostnaður** eining gerir kleift að stilla kostnaðartegundarkóða fyrir innri kostnað eða kostnað sem er afleiddur að utan. Ef kostnaður er utan fyrirtækis er gert ráð fyrir reikningi frá þjónustuveitanda. Þessi reikningur er unninn sem reikningsbók sem hægt er að tengja við ferð og hægt er að dreifa verðmæti reikningsins á einn eða fleiri kostnað við ferðina.

Reikningseiningar lánardrottins gera kleift að úthluta verðmæti færslubókarlínu yfir einn eða fleiri kostnað í ferð sem deila sama kostnaðartegundarkóða.

Kostnaði er aðeins hægt að úthluta ef haus reikningsbókar og reikningsbókarlínur eru til.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Úthlutun ferðakostnaðar söluaðila (ITMLedgerJournalCostLinesVoyagesEntity)

Gagnaeiningin um úthlutun ferðakostnaðar lánardrottins gerir kleift að úthluta reikningslínu lánardrottins á einn eða fleiri kostnað sem er notaður á ferðakostnaðarsvæðið. Þessi virkni er studd af`ITMLedgerJournalCostLinesVoyagesEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Númeric(32, 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Númeric(32, 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar (20) | **Já** | Nr. |
| Ferð | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Sendingargámakostnaðarúthlutun seljanda (ITMLedgerJournalCostLinesContainersEntity)

Gagnaeiningin um úthlutun flutningsgámakostnaðar lánardrottins gerir kleift að úthluta reikningslínu lánardrottins á einn eða fleiri kostnað sem er notaður á kostnaðarsvæði sendingargáma. Þessi virkni er studd af`ITMLedgerJournalCostLinesContainersEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Númeric(32, 6) | Nr. | Nr. |
| Gámur | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Númeric(32, 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar (20) | **Já** | Nr. |
| Ferð | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Kostnaðarúthlutun seljanda (ITMLedgerJournalCostLinesFoliosEntity)

Gagnaeining lánardrottins kostnaðarúthlutunar gerir kleift að úthluta reikningslínu lánardrottins á einn eða fleiri kostnað sem er notaður á kostnaðarsvæðið blaðsíðu. Þessi virkni er studd af`ITMLedgerJournalCostLinesFoliosEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Númeric(32, 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |
| Fólíó | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Númeric(32, 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar (20) | **Já** | Nr. |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Úthlutun kostnaðar innkaupapöntunar lánardrottins (ITMLedgerJournalCostLinesPurchTableEntity)

Gagnaeiningin um úthlutun kostnaðar innkaupapöntunar lánardrottins gerir kleift að úthluta reikningslínu lánardrottins á einn eða fleiri kostnað sem er notaður á kostnaðarsvæði innkaupapöntunar. Þessi virkni er studd af`ITMLedgerJournalCostLinesPurchTableEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Númeric(32, 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Númeric(32, 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar (20) | **Já** | Nr. |
| Innkaupapöntun | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Kostnaðarúthlutun söluaðila (ITMLedgerJournalCostLinesPurchLineEntity)

Gagnaeining kostnaðarúthlutunar lánardrottins gerir kleift að úthluta reikningslínu lánardrottins á einn eða fleiri kostnað sem er notaður á vörukostnaðarsvæðið. Kostnaðarsvæði vöru nær yfir kostnað á innkaupapöntunarlínunni. Þessi virkni er studd af`ITMLedgerJournalCostLinesPurchLineEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Númeric(32, 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Númeric(32, 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar (20) | **Já** | Nr. |
| Innkaupapöntun | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |
| Númer innkaupapöntunarlínu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Úthlutun kostnaðarlínu fyrir millifærslu lánardrottins (ITMLedgerJournalCostLinesTransferLineEntity)

Gagnaeiningin fyrir kostnaðarúthlutun millifærslupöntunar lánardrottins gerir kleift að úthluta reikningslínu lánardrottins á einn eða fleiri kostnað sem er notaður á kostnaðarsvæði millifærslulínunnar. Þessi virkni er studd af`ITMLedgerJournalCostLinesTransferLineEntity` aðila. Eftirfarandi tafla sýnir reiti og vörp sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Númeric(32, 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Númeric(32, 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar (20) | **Já** | Nr. |
| Flutningspöntun | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar (20) | **Já** | Nr. |
| Flytja pöntunarlínunúmer | ITMLedgerJournalCostLines.CostTransRefRecId | Númeric(32, 16) | **Já** | Nr. |

### <a name="reference-table"></a>Tilvísanatafla

Ferðakostnaðarlínur hafa bein tengsl við kostnaðarfærsluskrá. Þessi skrá inniheldur **Auðkenni tilvísunartöflu** gildi. Þetta gildi er einstakt fyrir hvert kostnaðarsvæði (sigling, flutningsgámur og svo framvegis). Þegar vísað er til tiltekinna töflunúmera fyrir gögn sem eru búin til með því að nota gagnaeiningar, er einingunum skipt á grundvelli **Auðkenni tilvísunartöflu** gildi.

Gildin fyrir viðmiðunartöfluna (`RefTableId`) og tegund viðskipta (`TransType`) eru óbein í vali á annaðhvort landaða kostnaðarkaupalínu eða landaða kostnaðartilfærslulínu.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Reikningsbókarlínur lánardrottins (VendorInvoiceJournalLineEntity)

Áður en hægt er að úthluta færslubókarlínugildi á einn eða fleiri kostnað í **Landaður kostnaður** mát, færslubókarlínan verður að vera tengd við kostnaðarsvæði. Til að styðja þessa virkni, er **Landaður kostnaður** mát bætir nokkrum nýjum reitum við töfluna færslubókarlínur (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Reitum bætt við línueininguna reikningsbók lánardrottins

Eftirfarandi tafla sýnir reitina sem **Landaður kostnaður** eining bætist við línueininguna reikningsbók lánardrottins (`VendorInvoiceJournalLineEntity`). Þessir reitir gera kerfinu kleift að búa til færslubókarlínur og úthluta kostnaði á móti þeim.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Kostnaðarsvæði | LedgerJournalTrans.ITMCostArea | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | LedgerJournalTrans.ITMCostTypeId | Nvarchar (20) | Nr. | Nr. |

### <a name="mainoffset-account"></a>Aðal/jöfnunarreikningur

Aðal-/jöfnunarreikningur fyrir reikningsbókarlínu sem er tengd við landaða kostnaðarferð ræðst af kóða kostnaðartegundar. Þegar kostnaðartegundarkóði er innifalinn í reikningsbókarlínunni verður jöfnunarreikningur kóðans notaður sem annað hvort aðalreikningur eða mótreikningur, allt eftir atburðarásinni:

- **Einlínu dagbók** – Ef aðalreikningur (með öðrum orðum lánardrottinsreikningur) er skilgreindur og kostnaðartegundarkóði er gefinn upp, verður virðisaukareikningsgildi fyrir þann kostnaðartegundarkóða færð inn á mótreikninginn.
- **Marglínu dagbók** – Ef aðalreikningur er ekki skilgreindur, en kostnaðartegundarkóði er gefinn upp, verður verðmæti jöfnunarreiknings fyrir þann kostnaðartegundarkóða fært inn á aðalreikninginn. Færslubókarlínan sem lánar lánardrottinn mun ekki vísa til kostnaðartegundarkóða.

## <a name="sequencing"></a>Röðun

Vegna ósjálfstæðis milli færslubókar- og færslubókarlínatöflunnar verður að stofna ferðina fyrst. Aðeins er hægt að búa til ferðalínur eftir að ferðin, flutningsgámurinn og blöðin hafa verið búin til.

Til að úthluta ferðareikningi verður kerfið að vinna einingarnar í eftirfarandi röð:

1. Haus reikningsbókar (`VendInvoiceJournalHeaderEntity`)
1. Reikningsbókarlína (`VendInvoiceJournalLineEntity`)
1. Landað kostnaðarúthlutun (`ITMLedgerJournalEntities`)