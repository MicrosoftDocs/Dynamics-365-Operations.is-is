---
title: fjárhagsskýrslur Prófjafnaðar
description: Þessi grein lýsir sjálfgefnum skýrslum fyrir prófjöfnuði. Hún lýsir einnig einingum sem tengjast þessum skýrslum og hvernig hægt er að breyta skýrslum eftir þörfum.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103659"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="b0315-104">fjárhagsskýrslur Prófjafnaðar</span><span class="sxs-lookup"><span data-stu-id="b0315-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0315-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir prófjöfnuði.</span><span class="sxs-lookup"><span data-stu-id="b0315-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="b0315-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum og hvernig hægt er að breyta skýrslum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b0315-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="b0315-107">Skýrslur fyrir sjálfgefinn prófjöfnuð</span><span class="sxs-lookup"><span data-stu-id="b0315-107">Default trial balance reports</span></span>

<span data-ttu-id="b0315-108">Þrjár prófjöfnuð skýrslur eru tiltækar í fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="b0315-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="b0315-109">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="b0315-109">Default report</span></span>                                 | <span data-ttu-id="b0315-110">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="b0315-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0315-111">Ítarlegur prófjöfnuður - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="b0315-112">Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.</span><span class="sxs-lookup"><span data-stu-id="b0315-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="b0315-113">Samantekt á prófjöfnuði - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="b0315-114">Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.</span><span class="sxs-lookup"><span data-stu-id="b0315-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="b0315-115">Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="b0315-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="b0315-116">Veitir upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra fyrir núgildandi ár og síðastliðið ár.</span><span class="sxs-lookup"><span data-stu-id="b0315-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="b0315-117">Einingar</span><span class="sxs-lookup"><span data-stu-id="b0315-117">Building blocks</span></span>
<span data-ttu-id="b0315-118">Fjárhagsskýrslur prófjöfnuðar nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="b0315-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="b0315-119">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="b0315-119">Default report</span></span>                                 | <span data-ttu-id="b0315-120">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="b0315-120">Row definition</span></span>          | <span data-ttu-id="b0315-121">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="b0315-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="b0315-122">Ítarlegur prófjöfnuður - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="b0315-123">prófjöfnuður - sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-123">Trial Balance - Default</span></span> | <span data-ttu-id="b0315-124">Ítarlegur prófjöfnuður - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="b0315-125">Samantekt á prófjöfnuði - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="b0315-126">prófjöfnuður - sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-126">Trial Balance - Default</span></span> | <span data-ttu-id="b0315-127">Samantekt á prófjöfnuði - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="b0315-128">Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="b0315-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="b0315-129">prófjöfnuður - sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="b0315-129">Trial Balance - Default</span></span> | <span data-ttu-id="b0315-130">Samantekt á Prófjöfnuði frá Ári til Árs – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="b0315-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="b0315-131">Þegar skýrslan **Prófjöfnuður** er keyrð í fjárhagsskýrslugerð skal ganga úr skugga um að velja gátreitina fyrir **Birta línur með engum upphæðum** og **Birta skýrslur með engum virkum línum** í flipanum **Stillingar**.</span><span class="sxs-lookup"><span data-stu-id="b0315-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="b0315-132">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="b0315-132">Row definition</span></span>

<span data-ttu-id="b0315-133">Línuskilgreining, Prófjöfnuð – Sjálfgefið, inniheldur eina línu sem sækir allar aðallykla.</span><span class="sxs-lookup"><span data-stu-id="b0315-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="b0315-134">Þess vegna getur hver sem er búið til skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="b0315-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="b0315-135">Þegar skýrslan er skoðuð er kafað í eina línu til að sjá upplýsingar um hvern reikning.</span><span class="sxs-lookup"><span data-stu-id="b0315-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="b0315-136">Hægt er að breyta línuskilgreiningu þannig að hún felur í sér nánari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b0315-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="b0315-137">til að breyta Prófjöfnuð – Sjálfgefna línuskilgreiningu þannig að hún felur í sér raðir fyrir alla lykla. Fylgið eftirfarandi skrefum</span><span class="sxs-lookup"><span data-stu-id="b0315-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="b0315-138">Smellt er á **breyta** og svo á **Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="b0315-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="b0315-139">**Setja inn línur úr víddum** skipunin gerir kleift að velja hvaða víddir óskað er að hafa í línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0315-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="b0315-140">Fyrir þessa línuskilgreiningu muntu nota **Aðallykil**.</span><span class="sxs-lookup"><span data-stu-id="b0315-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="b0315-141">Gangið úr skugga um **Aðallykill** innihaldi öll og-merki og velja **í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b0315-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="b0315-142">Línuskilgreining inniheldur nú alla aðallykla fyrir þinn sjálfgefna lögaðila.</span><span class="sxs-lookup"><span data-stu-id="b0315-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="b0315-143">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="b0315-143">Column definition</span></span>

<span data-ttu-id="b0315-144">Hver skýrslu prófjöfnuðar notar mismunandi dálkskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b0315-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="b0315-145">Þessar dálkaskilgreiningar innihalda mismunandi gerðir dálka á að veita mismunandi stig upplýsinga og fjárhagsgögn.</span><span class="sxs-lookup"><span data-stu-id="b0315-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="b0315-146">**Ítarlegur prófjöfnuður - Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="b0315-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="b0315-147">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0315-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b0315-148">**ACCT** – Kóðar lykils</span><span class="sxs-lookup"><span data-stu-id="b0315-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="b0315-149">**ATTR (3)** – Eigindir:</span><span class="sxs-lookup"><span data-stu-id="b0315-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="b0315-150">Færsludagsetning</span><span class="sxs-lookup"><span data-stu-id="b0315-150">Transaction Date</span></span>
        -   <span data-ttu-id="b0315-151">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="b0315-151">Voucher</span></span>
        -   <span data-ttu-id="b0315-152">Lýsing færslubókar</span><span class="sxs-lookup"><span data-stu-id="b0315-152">Journal Description</span></span>
    -   <span data-ttu-id="b0315-153">**FD** – Fjárhagsgögn sem inniheldur aðeins debet</span><span class="sxs-lookup"><span data-stu-id="b0315-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="b0315-154">**FD** – fjárhagsgögn sem inniheldur aðeins kredit</span><span class="sxs-lookup"><span data-stu-id="b0315-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="b0315-155">**CALC** – Nettó mismunur</span><span class="sxs-lookup"><span data-stu-id="b0315-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="b0315-156">**Samantekt á prófjöfnuði - Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="b0315-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="b0315-157">**ACCT** – Kóðar lykils</span><span class="sxs-lookup"><span data-stu-id="b0315-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="b0315-158">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0315-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b0315-159">**ATTR** – Eigind:</span><span class="sxs-lookup"><span data-stu-id="b0315-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="b0315-160">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="b0315-160">Voucher</span></span>
    -   <span data-ttu-id="b0315-161">**FD** – upphafsstaða fjárhagsgagna</span><span class="sxs-lookup"><span data-stu-id="b0315-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="b0315-162">**FD** – Fjárhagsgögn sem inniheldur aðeins debet</span><span class="sxs-lookup"><span data-stu-id="b0315-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="b0315-163">**FD** – fjárhagsgögn sem inniheldur aðeins kredit</span><span class="sxs-lookup"><span data-stu-id="b0315-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="b0315-164">**CALC** – Nettó mismunur</span><span class="sxs-lookup"><span data-stu-id="b0315-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="b0315-165">**CALC** – Lokastaða</span><span class="sxs-lookup"><span data-stu-id="b0315-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="b0315-166">**Samantekt á Prófjöfnuði frá Ári til Árs – Sjálfgefin**</span><span class="sxs-lookup"><span data-stu-id="b0315-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="b0315-167">**ACCT** – Kóðar lykils</span><span class="sxs-lookup"><span data-stu-id="b0315-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="b0315-168">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0315-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b0315-169">**ATTR** – Eigind</span><span class="sxs-lookup"><span data-stu-id="b0315-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="b0315-170">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="b0315-170">Voucher</span></span>
    -   <span data-ttu-id="b0315-171">**FD** – upphafsstaða fjárhagsgagna fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="b0315-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="b0315-172">**FD** – Fjárhagsgögn sem inniheldur aðeins debet fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="b0315-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="b0315-173">**FD** – Fjárhagsgögn sem inniheldur aðeins kredit fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="b0315-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="b0315-174">**CALC** – Nettó mismunur</span><span class="sxs-lookup"><span data-stu-id="b0315-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="b0315-175">**CALC** – Lokastaða</span><span class="sxs-lookup"><span data-stu-id="b0315-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="b0315-176">**FD** – Fjárhagsgögn sem inniheldur aðeins debet fyrir síðasta ár</span><span class="sxs-lookup"><span data-stu-id="b0315-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="b0315-177">**FD** – Fjárhagsgögn sem inniheldur aðeins kredit fyrir síðasta ár</span><span class="sxs-lookup"><span data-stu-id="b0315-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b0315-178">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b0315-178">Additional resources</span></span>

[<span data-ttu-id="b0315-179">Yfirlitssíða fjárhagsskýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b0315-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="b0315-180">Skoða fjárhagsskýrslur</span><span class="sxs-lookup"><span data-stu-id="b0315-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="b0315-181">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="b0315-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
