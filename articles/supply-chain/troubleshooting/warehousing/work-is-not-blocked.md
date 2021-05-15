---
title: Ekki er lokað á vinnu
description: Ekki er lokað á vinnu
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924205"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="597c1-103">Ekki er lokað á vinnu</span><span class="sxs-lookup"><span data-stu-id="597c1-103">Work isn't blocked</span></span>

<span data-ttu-id="597c1-104">Villukóði: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="597c1-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="597c1-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="597c1-105">Symptoms</span></span>

<span data-ttu-id="597c1-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="597c1-106">The system shows the following error message:</span></span>

> <span data-ttu-id="597c1-107">Vinna með kenni %1 er ekki útilokuð.</span><span class="sxs-lookup"><span data-stu-id="597c1-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="597c1-108">Orsök</span><span class="sxs-lookup"><span data-stu-id="597c1-108">Cause</span></span>

<span data-ttu-id="597c1-109">Valkosturinn **Lokuð bylgja** á bylgjunni er stilltur á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="597c1-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="597c1-110">Ekki er hægt að opna vinnuna þar sem hún er ekki lokuð eins og er.</span><span class="sxs-lookup"><span data-stu-id="597c1-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="597c1-111">Upplausn</span><span class="sxs-lookup"><span data-stu-id="597c1-111">Resolution</span></span>

 <span data-ttu-id="597c1-112">Aðeins er hægt að opna vinnu þegar valkosturinn **Lokuð bylgja** er stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="597c1-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
