---
title: Villuleita greiningarskýrslur
description: Þessi grein útskýrir hvað eigi gera ef gagnabreytingar viðskiptamanns birtast ekki í neinum vinnusvæðum hans.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112968"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="64fc5-103">Villuleita greiningarskýrslur</span><span class="sxs-lookup"><span data-stu-id="64fc5-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="64fc5-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="64fc5-104">**Issue**</span></span>

<span data-ttu-id="64fc5-105">Gagnabreytingar viðskiptamanns birtast ekki á flipunum **Greiningar** í einhverjum vinnusvæða hans.</span><span class="sxs-lookup"><span data-stu-id="64fc5-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="64fc5-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="64fc5-106">**Cause**</span></span>

<span data-ttu-id="64fc5-107">Skýrslur Microsoft Power BI eru endurnýjaðar á fjögurra klukkustunda fresta samkvæmt áætlun runuvinnslu fyrir framkvæmd mælingar.</span><span class="sxs-lookup"><span data-stu-id="64fc5-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="64fc5-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="64fc5-108">**Resolution**</span></span>

<span data-ttu-id="64fc5-109">Þetta mál snýst hugsanlega bara um tímasetningu.</span><span class="sxs-lookup"><span data-stu-id="64fc5-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="64fc5-110">Fylgið eftirfarandi skrefum til að hefja runuvinnslu og uppfæra greiningarvinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="64fc5-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="64fc5-111">Opnið síðuna **Runuvinnslur** í **Kerfisstjórnun \> Tenglar \> Runuvinnslur \> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="64fc5-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="64fc5-112">Önnur leið er að nota leitina og slá inn **Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="64fc5-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="64fc5-113">Finnið verkið **Framkvæma mælingu** í listanum.</span><span class="sxs-lookup"><span data-stu-id="64fc5-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="64fc5-114">Veljið **Breyta** efst á síðunni og stillið áætlaðan upphafsdag/tíma á gildi sem endurnýjar greiningarnar nær núgildandi tíma.</span><span class="sxs-lookup"><span data-stu-id="64fc5-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Runuvinnslur](media/batch-jobs.png)
