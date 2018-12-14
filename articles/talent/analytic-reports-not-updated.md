---
title: "Greiningarskýrslur eru ekki uppfærðar"
description: "Þetta efnisatriði útskýrir hvað eigi gera ef gagnabreytingar viðskiptamanns birtast ekki í neinum vinnusvæðum hans."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: is-is
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="9f537-103">Greiningarskýrslur eru ekki uppfærðar</span><span class="sxs-lookup"><span data-stu-id="9f537-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9f537-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="9f537-104">**Issue**</span></span>

<span data-ttu-id="9f537-105">Gagnabreytingar viðskiptamanns birtast ekki á flipunum **Greiningar** í einhverjum vinnusvæða hans.</span><span class="sxs-lookup"><span data-stu-id="9f537-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="9f537-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="9f537-106">**Cause**</span></span>

<span data-ttu-id="9f537-107">Skýrslur Microsoft Power BI eru endurnýjaðar á fjögurra klukkustunda fresta samkvæmt áætlun runuvinnslu fyrir framkvæmd mælingar.</span><span class="sxs-lookup"><span data-stu-id="9f537-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="9f537-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="9f537-108">**Resolution**</span></span>

<span data-ttu-id="9f537-109">Þetta mál snýst hugsanlega bara um tímasetningu.</span><span class="sxs-lookup"><span data-stu-id="9f537-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="9f537-110">Fylgið eftirfarandi skrefum til að hefja runuvinnslu og uppfæra greiningarvinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="9f537-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="9f537-111">Opnið síðuna **Runuvinnslur** í **Kerfisstjórnun \> Tenglar \> Runuvinnslur \> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="9f537-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="9f537-112">Önnur leið er að nota leitina og slá inn **Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="9f537-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="9f537-113">Finnið verkið **Framkvæma mælingu** í listanum.</span><span class="sxs-lookup"><span data-stu-id="9f537-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="9f537-114">Veljið **Breyta** efst á síðunni og stillið áætlaðan upphafsdag/tíma á gildi sem endurnýjar greiningarnar nær núgildandi tíma.</span><span class="sxs-lookup"><span data-stu-id="9f537-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Runuvinnslur](media/batch-jobs.png)

