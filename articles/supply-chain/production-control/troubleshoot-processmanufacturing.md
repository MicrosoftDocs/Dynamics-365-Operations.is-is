---
title: Úrræðaleit fyrir framleiðsluferli
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með framleiðsluferli.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d999c91aa1cc14f29ebfa6be8e456e45ef0d3fa4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966181"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="f1347-103">Úrræðaleit fyrir framleiðsluferli</span><span class="sxs-lookup"><span data-stu-id="f1347-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="f1347-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="f1347-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="f1347-105">Þegar ég nota verkspjaldstækið til að skrá hlutamagn í síðustu vinnslu framleiðslupöntunar er öllum fyrri vinnslum á pöntuninni sem hafa stöðuna í vinnslu sjálfkrafa lokið.</span><span class="sxs-lookup"><span data-stu-id="f1347-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="f1347-106">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="f1347-106">This behavior is by design.</span></span> <span data-ttu-id="f1347-107">Á síðunni **Sjálfgildi framleiðslupöntunar** á flipanum **Bóka sem tilbúið** er valkostur sem kallast **Merkja lok ferlis**.</span><span class="sxs-lookup"><span data-stu-id="f1347-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="f1347-108">Þegar þetta efnisatriði er stillt á *Já* er færslubók leiðarspjalds bókuð þegar starfskraftur notar verkspjaldstækið eða afgreiðslustöð verkspjalds til að skrá síðustu aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="f1347-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="f1347-109">Þessi færslubók merkir alla aðgerðir sem lokið og lýkur öllum framleiðsluverkum.</span><span class="sxs-lookup"><span data-stu-id="f1347-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="f1347-110">Þegar valkosturinn **Merkja lok ferlis** er stilltur á *Já* virðir kerfið ekki stöðu vinnslu sem starfskrafturinn valdi þegar hann tilkynnti um síðustu aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="f1347-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="f1347-111">Kerfið segir ekki til um það hvort starfskrafturinn sé að tilkynna um heildarmagn eða hluta.</span><span class="sxs-lookup"><span data-stu-id="f1347-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="f1347-112">Þegar ég reyni að loka birgðum fæ ég eftirfarandi viðvörunarboð: „Engin aðgerð til að framkvæma útreikning bakfærslukostnaðaraðferðar með dagsetningu %1 samsvarandi tímabil hefur verið skráð“.</span><span class="sxs-lookup"><span data-stu-id="f1347-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="f1347-113">Við notkun útgáfa sem eru eldri en útgáfa 10.0.13 og þú notar ekki kostnaðarflæði í Lean-framleiðslu færðu eftirfarandi viðvörunarboð að ósekju við birgðalokun:</span><span class="sxs-lookup"><span data-stu-id="f1347-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="f1347-114">Þú ert að fara að framkvæma birgðalokun með dagsetningu %1.</span><span class="sxs-lookup"><span data-stu-id="f1347-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="f1347-115">Engin keyrsla á bakfærslukostnaðaraðferð útreiknings með dagsetningu %1 sem samsvarar tímabilslokum hefur verið skráð.</span><span class="sxs-lookup"><span data-stu-id="f1347-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="f1347-116">Munið að keyra bakfærslukostnaðaraðferðar með dagsetningu á %1 sem samsvarar lokun tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="f1347-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="f1347-117">Mat á birgðum, kostnaði seldra vara og frávikum er mögulega ekki rétt í undirbók eða fjárhag fyrr en þetta hefur verið keyrt.</span><span class="sxs-lookup"><span data-stu-id="f1347-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="f1347-118">Leyst hefur verið úr vandamálinu í útgáfu 10.0.13 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="f1347-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="f1347-119">Frekari upplýsingar er að finna í [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="f1347-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>
