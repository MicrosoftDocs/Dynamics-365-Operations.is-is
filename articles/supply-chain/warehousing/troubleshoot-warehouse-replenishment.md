---
title: Úrræðaleit fyrir áfyllingar vöruhúss
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með áfyllingar vöruhúss í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7748a18d2b6f612b3ac9ac1a75efb6ae5f13859a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993882"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="794db-103">Úrræðaleit fyrir áfyllingar vöruhúss</span><span class="sxs-lookup"><span data-stu-id="794db-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="794db-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með áfyllingar vöruhúss í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="794db-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="794db-105">Ég fæ eftirfarandi villuboð: Ekki er hægt að opna fyrir vinnu %1 vegna þess að hún inniheldur ólokna áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="794db-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="794db-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="794db-106">Issue description</span></span>

<span data-ttu-id="794db-107">Tiltektarvinna er lokuð vegna háðrar áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="794db-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="794db-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="794db-108">Issue resolution</span></span>

<span data-ttu-id="794db-109">Þegar eftirspurnaráfylling bylgju er notuð, ef fylla verður á tiltektarstaðsetningu til að uppfylla eftirspurn upprunapöntunar, stofnar kerfið bæði áfyllingarvinnu og tiltektarvinnu.</span><span class="sxs-lookup"><span data-stu-id="794db-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="794db-110">Hins vegar lokar það tiltektarvinnu þar til áfyllingarvinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="794db-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="794db-111">Þessi hegðun er innbyggð, vegna þess að tiltektarstaðsetningin mun ekki innihalda nægar birgðir nema áfyllingarvinnu sé lokið.</span><span class="sxs-lookup"><span data-stu-id="794db-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="794db-112">Ljúka skal áfyllingarvinnu og vinna síðan tiltektarverk.</span><span class="sxs-lookup"><span data-stu-id="794db-112">Complete the replenishment work, and then process the picking work.</span></span>
