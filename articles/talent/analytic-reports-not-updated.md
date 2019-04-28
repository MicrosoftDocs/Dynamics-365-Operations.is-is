---
title: Greiningarskýrslur eru ekki uppfærðar
description: Þetta efnisatriði útskýrir hvað eigi gera ef gagnabreytingar viðskiptamanns birtast ekki í neinum vinnusvæðum hans.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6a6487b50908093f876237ffef840a3144b3fe6
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "857454"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="5d813-103">Greiningarskýrslur eru ekki uppfærðar</span><span class="sxs-lookup"><span data-stu-id="5d813-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d813-104">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="5d813-104">**Issue**</span></span>

<span data-ttu-id="5d813-105">Gagnabreytingar viðskiptamanns birtast ekki á flipunum **Greiningar** í einhverjum vinnusvæða hans.</span><span class="sxs-lookup"><span data-stu-id="5d813-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="5d813-106">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="5d813-106">**Cause**</span></span>

<span data-ttu-id="5d813-107">Skýrslur Microsoft Power BI eru endurnýjaðar á fjögurra klukkustunda fresta samkvæmt áætlun runuvinnslu fyrir framkvæmd mælingar.</span><span class="sxs-lookup"><span data-stu-id="5d813-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="5d813-108">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="5d813-108">**Resolution**</span></span>

<span data-ttu-id="5d813-109">Þetta mál snýst hugsanlega bara um tímasetningu.</span><span class="sxs-lookup"><span data-stu-id="5d813-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="5d813-110">Fylgið eftirfarandi skrefum til að hefja runuvinnslu og uppfæra greiningarvinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="5d813-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="5d813-111">Opnið síðuna **Runuvinnslur** í **Kerfisstjórnun \> Tenglar \> Runuvinnslur \> Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="5d813-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="5d813-112">Önnur leið er að nota leitina og slá inn **Runuvinnslur**.</span><span class="sxs-lookup"><span data-stu-id="5d813-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="5d813-113">Finnið verkið **Framkvæma mælingu** í listanum.</span><span class="sxs-lookup"><span data-stu-id="5d813-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="5d813-114">Veljið **Breyta** efst á síðunni og stillið áætlaðan upphafsdag/tíma á gildi sem endurnýjar greiningarnar nær núgildandi tíma.</span><span class="sxs-lookup"><span data-stu-id="5d813-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Runuvinnslur](media/batch-jobs.png)
