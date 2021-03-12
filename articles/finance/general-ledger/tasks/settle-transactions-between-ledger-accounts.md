---
title: Jafna færslur á milli fjárhagslykla
description: Þessi verklýsing sýnir hvernig á að jafna færslur á milli fjárhagslykla og hætta við fjárhagsjöfnun.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994416"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="4f704-103">Jafna færslur á milli fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="4f704-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4f704-104">Þessi verklýsing sýnir hvernig á að jafna færslur á milli fjárhagslykla og hætta við fjárhagsjöfnun.</span><span class="sxs-lookup"><span data-stu-id="4f704-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="4f704-105">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="4f704-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="4f704-106">Jafna færslu milli fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="4f704-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="4f704-107">Fara í Fjárhag > Reglubundin verkefni > Fjárhagsjafnanir.</span><span class="sxs-lookup"><span data-stu-id="4f704-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="4f704-108">Í listanum skal velja færsluna sem á að leysa.</span><span class="sxs-lookup"><span data-stu-id="4f704-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="4f704-109">Staða upphæðar verður að vera núll.</span><span class="sxs-lookup"><span data-stu-id="4f704-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="4f704-110">Smellt er á Hafa með.</span><span class="sxs-lookup"><span data-stu-id="4f704-110">Click Include.</span></span>
4. <span data-ttu-id="4f704-111">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="4f704-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="4f704-112">Hætta við fjárhagsjöfnun</span><span class="sxs-lookup"><span data-stu-id="4f704-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="4f704-113">Fara í Fjárhag > Fyrirspurnir og skýrslur > Prófjöfnuður.</span><span class="sxs-lookup"><span data-stu-id="4f704-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="4f704-114">Smelltu á Færibreytur til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4f704-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="4f704-115">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="4f704-115">Click Update.</span></span>
4. <span data-ttu-id="4f704-116">Í listanum finnurðu lykilinn sem er með jöfnuðu færsluna.</span><span class="sxs-lookup"><span data-stu-id="4f704-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="4f704-117">Smellt er á Allar færslur.</span><span class="sxs-lookup"><span data-stu-id="4f704-117">Click All transactions.</span></span>
6. <span data-ttu-id="4f704-118">Nota verður síu til að finna færsluna í listanum.</span><span class="sxs-lookup"><span data-stu-id="4f704-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="4f704-119">Smellt er á Fjárhagsjafnanir.</span><span class="sxs-lookup"><span data-stu-id="4f704-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="4f704-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="4f704-120">In the list, mark the selected row.</span></span>

