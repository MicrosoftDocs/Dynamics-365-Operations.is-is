---
title: fjárhagsskýrslur Prófjafnaðar
description: Þessi grein lýsir sjálfgefnum skýrslum fyrir prófjöfnuði. Hún lýsir einnig einingum sem tengjast þessum skýrslum og hvernig hægt er að breyta skýrslum eftir þörfum.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9e8c16724364df4dd62150056299e818470aa63
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "309105"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="f34b1-104">fjárhagsskýrslur Prófjafnaðar</span><span class="sxs-lookup"><span data-stu-id="f34b1-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f34b1-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir prófjöfnuði.</span><span class="sxs-lookup"><span data-stu-id="f34b1-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="f34b1-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum og hvernig hægt er að breyta skýrslum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f34b1-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="f34b1-107">Skýrslur fyrir sjálfgefinn prófjöfnuð</span><span class="sxs-lookup"><span data-stu-id="f34b1-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="f34b1-108">Þrjár prófjöfnuð skýrslur eru tiltækar í fjárhagsskýrslu í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f34b1-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="f34b1-109">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="f34b1-109">Default report</span></span>                                 | <span data-ttu-id="f34b1-110">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="f34b1-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34b1-111">Ítarlegur prófjöfnuður - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="f34b1-112">Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.</span><span class="sxs-lookup"><span data-stu-id="f34b1-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="f34b1-113">Samantekt á prófjöfnuði - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="f34b1-114">Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.</span><span class="sxs-lookup"><span data-stu-id="f34b1-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="f34b1-115">Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="f34b1-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="f34b1-116">Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra fyrir núgildandi ár og síðastliðið ár.</span><span class="sxs-lookup"><span data-stu-id="f34b1-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="f34b1-117">Einingar</span><span class="sxs-lookup"><span data-stu-id="f34b1-117">Building blocks</span></span>
<span data-ttu-id="f34b1-118">Fjárhagsskýrslur prófjöfnuðar nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="f34b1-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="f34b1-119">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="f34b1-119">Default report</span></span>                                 | <span data-ttu-id="f34b1-120">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="f34b1-120">Row definition</span></span>          | <span data-ttu-id="f34b1-121">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="f34b1-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="f34b1-122">Ítarlegur prófjöfnuður - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="f34b1-123">prófjöfnuður - sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-123">Trial Balance - Default</span></span> | <span data-ttu-id="f34b1-124">Ítarlegur prófjöfnuður - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="f34b1-125">Samantekt á prófjöfnuði - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="f34b1-126">prófjöfnuður - sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-126">Trial Balance - Default</span></span> | <span data-ttu-id="f34b1-127">Samantekt á prófjöfnuði - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="f34b1-128">Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="f34b1-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="f34b1-129">prófjöfnuður - sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="f34b1-129">Trial Balance - Default</span></span> | <span data-ttu-id="f34b1-130">Samantekt á Prófjöfnuði frá Ári til Árs – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="f34b1-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="f34b1-131">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="f34b1-131">Row definition</span></span>

<span data-ttu-id="f34b1-132">Línuskilgreining, Prófjöfnuð – Sjálfgefið, inniheldur eina línu sem sækir allar aðallykla.</span><span class="sxs-lookup"><span data-stu-id="f34b1-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="f34b1-133">Þess vegna getur hver sem er búið til skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="f34b1-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="f34b1-134">Þegar skýrslan er skoðuð er kafað í eina línu til að sjá upplýsingar um hvern reikning.</span><span class="sxs-lookup"><span data-stu-id="f34b1-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="f34b1-135">Hægt er að breyta línuskilgreiningu þannig að hún felur í sér nánari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f34b1-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="f34b1-136">til að breyta Prófjöfnuð – Sjálfgefna línuskilgreiningu þannig að hún felur í sér raðir fyrir alla lykla. Fylgið eftirfarandi skrefum</span><span class="sxs-lookup"><span data-stu-id="f34b1-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="f34b1-137">Smellt er á **breyta** og svo á **Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="f34b1-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="f34b1-138">**Setja inn línur úr víddum** skipunin gerir kleift að velja hvaða víddir óskað er að hafa í línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="f34b1-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="f34b1-139">Fyrir þessa línuskilgreiningu muntu nota **Aðallykil**.</span><span class="sxs-lookup"><span data-stu-id="f34b1-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="f34b1-140">Gangið úr skugga um **Aðallykill** innihaldi öll og-merki og velja **í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f34b1-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="f34b1-141">Línuskilgreining inniheldur nú alla aðallykla fyrir þinn sjálfgefna lögaðila.</span><span class="sxs-lookup"><span data-stu-id="f34b1-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="f34b1-142">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="f34b1-142">Column definition</span></span>

<span data-ttu-id="f34b1-143">Hver skýrslu prófjöfnuðar notar mismunandi dálkskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f34b1-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="f34b1-144">Þessar dálkaskilgreiningar innihalda mismunandi gerðir dálka á að veita mismunandi stig upplýsinga og fjárhagsgögn.</span><span class="sxs-lookup"><span data-stu-id="f34b1-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="f34b1-145">**Ítarlegur prófjöfnuður - Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="f34b1-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="f34b1-146">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="f34b1-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f34b1-147">**ACCT** – Kóðar lykils</span><span class="sxs-lookup"><span data-stu-id="f34b1-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f34b1-148">**ATTR (3)** – Eigindir:</span><span class="sxs-lookup"><span data-stu-id="f34b1-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="f34b1-149">Færsludagsetning</span><span class="sxs-lookup"><span data-stu-id="f34b1-149">Transaction Date</span></span>
        -   <span data-ttu-id="f34b1-150">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="f34b1-150">Voucher</span></span>
        -   <span data-ttu-id="f34b1-151">Lýsing færslubókar</span><span class="sxs-lookup"><span data-stu-id="f34b1-151">Journal Description</span></span>
    -   <span data-ttu-id="f34b1-152">**FD** – Fjárhagsgögn sem inniheldur aðeins debet</span><span class="sxs-lookup"><span data-stu-id="f34b1-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="f34b1-153">**FD** – fjárhagsgögn sem inniheldur aðeins kredit</span><span class="sxs-lookup"><span data-stu-id="f34b1-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="f34b1-154">**CALC** – Nettó mismunur</span><span class="sxs-lookup"><span data-stu-id="f34b1-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="f34b1-155">**Samantekt á prófjöfnuði - Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="f34b1-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="f34b1-156">**ACCT** – Kóðar lykils</span><span class="sxs-lookup"><span data-stu-id="f34b1-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f34b1-157">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="f34b1-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f34b1-158">**ATTR** – Eigind:</span><span class="sxs-lookup"><span data-stu-id="f34b1-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="f34b1-159">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="f34b1-159">Voucher</span></span>
    -   <span data-ttu-id="f34b1-160">**FD** – upphafsstaða fjárhagsgagna</span><span class="sxs-lookup"><span data-stu-id="f34b1-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="f34b1-161">**FD** – Fjárhagsgögn sem inniheldur aðeins debet</span><span class="sxs-lookup"><span data-stu-id="f34b1-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="f34b1-162">**FD** – fjárhagsgögn sem inniheldur aðeins kredit</span><span class="sxs-lookup"><span data-stu-id="f34b1-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="f34b1-163">**CALC** – Nettó mismunur</span><span class="sxs-lookup"><span data-stu-id="f34b1-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="f34b1-164">**CALC** – Lokastaða</span><span class="sxs-lookup"><span data-stu-id="f34b1-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="f34b1-165">**Samantekt á Prófjöfnuði frá Ári til Árs – Sjálfgefin**</span><span class="sxs-lookup"><span data-stu-id="f34b1-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="f34b1-166">**ACCT** – Kóðar lykils</span><span class="sxs-lookup"><span data-stu-id="f34b1-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="f34b1-167">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="f34b1-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="f34b1-168">**ATTR** – Eigind</span><span class="sxs-lookup"><span data-stu-id="f34b1-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="f34b1-169">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="f34b1-169">Voucher</span></span>
    -   <span data-ttu-id="f34b1-170">**FD** – upphafsstaða fjárhagsgagna fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="f34b1-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="f34b1-171">**FD** – Fjárhagsgögn sem inniheldur aðeins debet fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="f34b1-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="f34b1-172">**FD** – Fjárhagsgögn sem inniheldur aðeins kredit fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="f34b1-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="f34b1-173">**CALC** – Nettó mismunur</span><span class="sxs-lookup"><span data-stu-id="f34b1-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="f34b1-174">**CALC** – Lokastaða</span><span class="sxs-lookup"><span data-stu-id="f34b1-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="f34b1-175">**FD** – Fjárhagsgögn sem inniheldur aðeins debet fyrir síðasta ár</span><span class="sxs-lookup"><span data-stu-id="f34b1-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="f34b1-176">**FD** – Fjárhagsgögn sem inniheldur aðeins kredit fyrir síðasta ár</span><span class="sxs-lookup"><span data-stu-id="f34b1-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="f34b1-177">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f34b1-177">Additional resources</span></span>
--------

[<span data-ttu-id="f34b1-178">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="f34b1-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="f34b1-179">Skoðun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="f34b1-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="f34b1-180">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="f34b1-180">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)



