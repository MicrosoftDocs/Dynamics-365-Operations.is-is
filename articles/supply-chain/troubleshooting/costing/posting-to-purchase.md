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
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722176"
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
