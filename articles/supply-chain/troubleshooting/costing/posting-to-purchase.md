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
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="05dc6-103">Uppsöfnuð innkaup sem eru með núllupphæð er færð sem núllgidli innhreyfingarskjals</span><span class="sxs-lookup"><span data-stu-id="05dc6-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="05dc6-104">KB númer: 4612588</span><span class="sxs-lookup"><span data-stu-id="05dc6-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="05dc6-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="05dc6-105">Symptoms</span></span>

<span data-ttu-id="05dc6-106">Þegar innhreyfingarskjal með núllgildi er bókað býr kerfið til bókun til að uppsöfnun þar sem upphæðin er 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="05dc6-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="05dc6-107">Upplausn</span><span class="sxs-lookup"><span data-stu-id="05dc6-107">Resolution</span></span>

<span data-ttu-id="05dc6-108">Fyrir fjárhagsbókanir af gerðinni *Uppsöfnuð innkaup* er `IsTransferredIndetail` reiturinn alltaf stilltur á *Samantekt* í færslum undirbókar.</span><span class="sxs-lookup"><span data-stu-id="05dc6-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="05dc6-109">Kerfið býr því til tengda færslu á fylgiskjali jafnvel þótt fjárhæðin sé 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="05dc6-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="05dc6-110">Til að sleppa þessari bókunargerð þegar upphæðin er 0 (núll), skal nota `subledgerJournalizer.markDoNotTransferEntries` aðferðina þannig að hún innihaldi `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`eins og sýnt er í eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="05dc6-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
