---
title: Uppsöfnuð innkaup sem eru með núllupphæð er færð sem núllgidli innhreyfingarskjals
description: Þegar innhreyfingarskjal með núllgildi er bókað býr kerfið til bókun til að uppsöfnun þar sem upphæðin er 0 (núll).
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026625"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Uppsöfnuð innkaup sem eru með núllupphæð er færð sem núllgidli innhreyfingarskjals

KB númer: 4612588

## <a name="symptoms"></a>Einkenni

Þegar innhreyfingarskjal með núllgildi er bókað býr kerfið til bókun til að uppsöfnun þar sem upphæðin er 0 (núll).

## <a name="resolution"></a>Upplausn

Fyrir fjárhagsbókanir af gerðinni *Uppsöfnuð innkaup* er `IsTransferredIndetail` reiturinn alltaf stilltur á *Samantekt* í færslum undirbókar. Kerfið býr því til tengda færslu á fylgiskjali jafnvel þótt fjárhæðin sé 0 (núll).

Til að sleppa þessari bókunargerð þegar upphæðin er 0 (núll), skal nota `subledgerJournalizer.markDoNotTransferEntries` aðferðina þannig að hún innihaldi `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`eins og sýnt er í eftirfarandi dæmi.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
