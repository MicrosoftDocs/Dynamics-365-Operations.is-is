---
title: Jafna færslur á milli fjárhagslykla
description: Þessi verklýsing sýnir hvernig á að jafna færslur á milli fjárhagslykla og hætta við fjárhagsjöfnun.
author: aprilolson
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2594b90ed58a1e7f12c8a94d3c48266faef557f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817054"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="1f56e-103">Jafna færslur á milli fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="1f56e-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f56e-104">Þessi verklýsing sýnir hvernig á að jafna færslur á milli fjárhagslykla og hætta við fjárhagsjöfnun.</span><span class="sxs-lookup"><span data-stu-id="1f56e-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="1f56e-105">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="1f56e-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="1f56e-106">Jafna færslu milli fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="1f56e-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="1f56e-107">Fara í Fjárhag > Reglubundin verkefni > Fjárhagsjafnanir.</span><span class="sxs-lookup"><span data-stu-id="1f56e-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="1f56e-108">Í listanum skal velja færsluna sem á að leysa.</span><span class="sxs-lookup"><span data-stu-id="1f56e-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="1f56e-109">Staða upphæðar verður að vera núll.</span><span class="sxs-lookup"><span data-stu-id="1f56e-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="1f56e-110">Smellt er á Hafa með.</span><span class="sxs-lookup"><span data-stu-id="1f56e-110">Click Include.</span></span>
4. <span data-ttu-id="1f56e-111">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="1f56e-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="1f56e-112">Hætta við fjárhagsjöfnun</span><span class="sxs-lookup"><span data-stu-id="1f56e-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="1f56e-113">Fara í Fjárhag > Fyrirspurnir og skýrslur > Prófjöfnuður.</span><span class="sxs-lookup"><span data-stu-id="1f56e-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="1f56e-114">Smelltu á Færibreytur til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="1f56e-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="1f56e-115">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="1f56e-115">Click Update.</span></span>
4. <span data-ttu-id="1f56e-116">Í listanum finnurðu lykilinn sem er með jöfnuðu færsluna.</span><span class="sxs-lookup"><span data-stu-id="1f56e-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="1f56e-117">Smellt er á Allar færslur.</span><span class="sxs-lookup"><span data-stu-id="1f56e-117">Click All transactions.</span></span>
6. <span data-ttu-id="1f56e-118">Nota verður síu til að finna færsluna í listanum.</span><span class="sxs-lookup"><span data-stu-id="1f56e-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="1f56e-119">Smellt er á Fjárhagsjafnanir.</span><span class="sxs-lookup"><span data-stu-id="1f56e-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="1f56e-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f56e-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]