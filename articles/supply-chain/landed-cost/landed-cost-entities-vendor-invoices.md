---
title: Reikningaeiningar lánardrottins
description: Í þessari grein er að finna upplýsingar um einingar lánardrottnareikninga sem gera kleift að skilgreina kóða kostnaðargerðar fyrir innri kostnað eða ytri afleiddan kostnað.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166744"
---
# <a name="vendor-invoice-entities"></a>Reikningaeiningar lánardrottins

[!include [banner](../includes/banner.md)]

Einingin **Heildarkostnaður** gerir kleift að skilgreina kóða kostnaðargerðar fyrir innri kostnað eða ytri afleiddan kostnað. Ef kostnaður er utanaðkomandi fyrir fyrirtæki er reikningur væntanlegur frá þjónustuveitunni. Unnið er úr þessum reikningi sem reikningabók sem hægt er að tengja við ferð og virði reikningsins er hægt að dreifa yfir einn eða fleiri kostnaði vegna ferðarinnar.

Einingar lánardrottnareikninga gera kleift að úthluta virðinu í færslubókarlínu á einn eða fleiri kostnaði vegna ferðar sem deilir sama kóða kostnaðargerðar.

Kostnaðaráætlun er aðeins hægt að úthluta ef haus reikningabókar og línur reikningabókar eru til staðar.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Kostnaðarúthlutanir vegna ferðar lánardrottins (ITMLedgerJournalCostLinesVoyagesEntity)

Gagnaeining fyrir kostnaðarúthlutanir vegna ferðar lánardrottins gerir kleift að úthluta línum lánardrottnareiknings á einn eða fleiri kostnaði sem eru notaðir á kostnaðarþátt ferðar. Þessi virkni er studd af `ITMLedgerJournalCostLinesVoyagesEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Tölustafir(32; 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Já** | Nr. |
| Ferð | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Kostnaðarúthlutanir á flutningsgámum lánardrottins (ITMLedgerJournalCostLinesContainersEntity)

Gagnaeining fyrir kostnaðarúthlutanir á flutningsgámum lánardrottins gerir kleift að úthluta línum lánardrottnareiknings á einn eða fleiri kostnaði sem eru notaðir á kostnaðarþátt flutningsgáms. Þessi virkni er studd af `ITMLedgerJournalCostLinesContainersEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Tölustafir(32; 6) | Nr. | Nr. |
| Gámur | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Já** | Nr. |
| Ferð | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Kostnaðarúthlutanir lánardrottnafólíó (ITMLedgerJournalCostLinesFoliosEntity)

Gagnaeining fyrir kostnaðarúthlutanir á fólíói lánardrottins gerir kleift að úthluta línum lánardrottnareiknings á einn eða fleiri kostnaði sem eru notaðir á kostnaðarþátt fólíós. Þessi virkni er studd af `ITMLedgerJournalCostLinesFoliosEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Tölustafir(32; 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Fólíó | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Já** | Nr. |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Kostnaðarúthlutanir vegna innkaupapöntunar lánardrottins (ITMLedgerJournalCostLinesPurchTableEntity)

Gagnaeining fyrir kostnaðarúthlutanir á innkaupapöntun lánardrottins gerir kleift að úthluta línum lánardrottnareiknings á einn eða fleiri kostnaði sem eru notaðir á kostnaðarþátt innkaupapöntunar. Þessi virkni er studd af `ITMLedgerJournalCostLinesPurchTableEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Tölustafir(32; 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Já** | Nr. |
| Innkaupapöntun | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Kostnaðarúthlutanir á vöru lánardrottins (ITMLedgerJournalCostLinesPurchLineEntity)

Gagnaeining fyrir kostnaðarúthlutanir á vöru lánardrottins gerir kleift að úthluta línum lánardrottnareiknings á einn eða fleiri kostnaði sem eru notaðir á kostnaðarþátt vöru. Kostnaðarsvæðið nær yfir kostnað á innkaupapöntunarlínunni. Þessi virkni er studd af `ITMLedgerJournalCostLinesPurchLineEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Tölustafir(32; 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Já** | Nr. |
| Innkaupapöntun | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |
| Númer innkaupapöntunarlínu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Kostnaðarúthlutanir vegna flutningspöntunarlínu lánardrottins (ITMLedgerJournalCostLinesTransferLineEntity)

Gagnaeining fyrir kostnaðarúthlutanir á flutningspöntunarlínu lánardrottins gerir kleift að úthluta línum lánardrottnareiknings á einn eða fleiri kostnaði sem eru notaðir á kostnaðarþátt flutningspöntunarlínu. Þessi virkni er studd af `ITMLedgerJournalCostLinesTransferLineEntity`-einingunni. Eftirfarandi tafla sýnir reitina og vörpun sem mynda þessa einingu.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Úthlutuð upphæð | ITMLedgerJournalCostLines.Amount | Tölustafir(32; 6) | Nr. | Nr. |
| Línunúmer kostnaðarfærslu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Númer færslubókarlínu | ITMLedgerJournalCostLines.RefRecId | Tölustafir(32; 16) | **Já** | Nr. |
| Færslubókarnúmer | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Já** | Nr. |
| Flutningspöntun | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Já** | Nr. |
| Númer flutningspöntunarlínu | ITMLedgerJournalCostLines.CostTransRefRecId | Tölustafir(32; 16) | **Já** | Nr. |

### <a name="reference-table"></a>Tilvísanatafla

Kostnaðarlínur ferðar tengjast skrá kostnaðarfærslu á beinan hátt. Þessi skrá inniheldur **Kenni tilvísunartöflu** gildi. Þetta gildi er einkvæmt fyrir hvern kostnaðarþátt (ferð, flutningsgámur og svo framvegis). Þegar vísað er í tiltekin töflunúmer fyrir gögn sem eru búin til með því að nota gagnaeiningar er einingunum skipt samkvæmt gildunum **Auðkenni tilvísanatöflu**.

Gildin fyrir viðmiðunartöfluna (`RefTableId`) og færslugerðina (`TransType`) eru sjálfgefin á annaðhvort í innkaupalínu heildarkostnaðar eða einingu flutningslínu heildarkostnaðar.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Línur reikningabókar lánardrottins (VendorInvoiceJournalLineEntity)

Áður en hægt er að úthluta gildi færslubókarlínu á einn eða fleiri kostnaði í einingunni **Heildarkostnaður** verður færslubókarlínan að tengjast kostnaðarþætti. Til að styðja við þessa virkni bætir einingin **Heildarkostnaður** nokkrum nýjum reitum við töflu færslubókarlína (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Reitum bætt við einingu reikningabókarlínu lánardrottins

Eftirfarandi tafla sýnir reitina sem einingin **Heildarkostnaður** bætir við einingu reikningabókarlínu lánadrottins (`VendorInvoiceJournalLineEntity`). Þessir reitir gera kerfinu kleift að búa til færslubókarlínur og úthluta kostnaði á móti þeim.

| Nafn | Vörpun | Gagnagerð | Lykill | Skylda |
|---|---|---|---|---|
| Kostnaðarsvæði | LedgerJournalTrans.ITMCostArea | Int | Nr. | Nr. |
| Kostnaðargerðarkóði | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nr. | Nr. |

### <a name="mainoffset-account"></a>Aðal/Mótlykill

Aðallykill/mótlykill fyrir reiknisdagbókarlínu sem er tengd við heildarkostnað ferðar ræðst af tegund kostnaðarkóða. Þegar kóði kostnaðargerðar er hafður með í línu reikningabókar verður millireikningur fyrir kóðann notaður sem annaðhvort aðallykill eða mótlykill eftir því hverjar aðstæðurnar eru:

- **Færslubók með einni línu** – Ef aðallykill (þ.e. lánardrottnalykillinn) er skilgreindur og kóði kostnaðargerðar er gefinn upp verður gildi millireiknings fyrir þann kóða kostnaðargerðar fært inn í mótlykilinn.
- **Færslubók með mörgum línum** – Ef aðallykill er ekki skilgreindur en kóði kostnaðargerðar er gefinn upp verður gildi millireiknings fyrir kóða kostnaðargerðar fært inn á aðallykilinn. Færslubókarlínan sem veitir lánardrottninum inneign mun ekki vísa í tegundarkóða kostnaðar.

## <a name="sequencing"></a>Röðun

Vegna tengsla á milli taflna færslubókar og færslubókarlína verður að stofna ferðafærsluna fyrst. Aðeins er hægt að búa til línur ferðar eftir að ferðin, gámurinn og fólíóin hafa verið búin til.

Til að úthluta ferðareikningi verður kerfið að vinna úr einingum á eftirfarandi hátt:

1. Haus reikningabókar (`VendInvoiceJournalHeaderEntity`)
1. Reikningabókarlína (`VendInvoiceJournalLineEntity`)
1. Úthlutun heildarkostnaðar (`ITMLedgerJournalEntities`)
