--- 
title: "Jafna færslur á milli fjárhagslykla"
description: "Þessi verklýsing sýnir hvernig á að jafna færslur á milli fjárhagslykla og hætta við fjárhagsjöfnun."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 97a28069f8d560c98099a667852c932ba7658996
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="5e392-103">Jafna færslur á milli fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="5e392-103">Settle transactions between ledger accounts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e392-104">Þessi verklýsing sýnir hvernig á að jafna færslur á milli fjárhagslykla og hætta við fjárhagsjöfnun.</span><span class="sxs-lookup"><span data-stu-id="5e392-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="5e392-105">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="5e392-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="5e392-106">Jafna færslu milli fjárhagslykla</span><span class="sxs-lookup"><span data-stu-id="5e392-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="5e392-107">Fara í Fjárhag > Reglubundin verkefni > Fjárhagsjafnanir.</span><span class="sxs-lookup"><span data-stu-id="5e392-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="5e392-108">Í listanum skal velja færsluna sem á að leysa.</span><span class="sxs-lookup"><span data-stu-id="5e392-108">In the list, find the transaction that you want to settle.</span></span>
    * <span data-ttu-id="5e392-109">Staða upphæðar verður að vera núll.</span><span class="sxs-lookup"><span data-stu-id="5e392-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="5e392-110">Smellt er á Hafa með.</span><span class="sxs-lookup"><span data-stu-id="5e392-110">Click Include.</span></span>
4. <span data-ttu-id="5e392-111">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="5e392-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="5e392-112">Hætta við fjárhagsjöfnun</span><span class="sxs-lookup"><span data-stu-id="5e392-112">Cancel a ledger settlement</span></span>
1. <span data-ttu-id="5e392-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5e392-113">Close the page.</span></span>
2. <span data-ttu-id="5e392-114">Fara í Fjárhag > Fyrirspurnir og skýrslur > Prófjöfnuður.</span><span class="sxs-lookup"><span data-stu-id="5e392-114">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
3. <span data-ttu-id="5e392-115">Smelltu á Færibreytur til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="5e392-115">Click Parameters to open the drop dialog.</span></span>
4. <span data-ttu-id="5e392-116">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="5e392-116">Click Update.</span></span>
5. <span data-ttu-id="5e392-117">Í listanum finnurðu lykilinn sem er með jöfnuðu færsluna.</span><span class="sxs-lookup"><span data-stu-id="5e392-117">In the list, find the account that has the settled transaction.</span></span>
6. <span data-ttu-id="5e392-118">Smellt er á Allar færslur.</span><span class="sxs-lookup"><span data-stu-id="5e392-118">Click All transactions.</span></span>
7. <span data-ttu-id="5e392-119">Nota verður síu til að finna færsluna í listanum.</span><span class="sxs-lookup"><span data-stu-id="5e392-119">Use a filter to easily find the transaction in the list.</span></span>
8. <span data-ttu-id="5e392-120">Smellt er á Fjárhagsjafnanir.</span><span class="sxs-lookup"><span data-stu-id="5e392-120">Click Ledger settlements.</span></span>
9. <span data-ttu-id="5e392-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="5e392-121">In the list, mark the selected row.</span></span>


