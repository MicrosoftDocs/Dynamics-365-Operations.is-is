---
title: Ekki var hægt að hreinsa upp bylgju
description: Ekki var hægt að hreinsa upp bylgju
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924328"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="0de26-103">Ekki var hægt að hreinsa upp bylgju</span><span class="sxs-lookup"><span data-stu-id="0de26-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="0de26-104">Villukóði: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="0de26-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="0de26-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="0de26-105">Symptoms</span></span>

<span data-ttu-id="0de26-106">Kerfið sýnir eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="0de26-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0de26-107">Ekki er hægt að hreinsa upp bylgju %1.</span><span class="sxs-lookup"><span data-stu-id="0de26-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="0de26-108">Ekki er hægt að hreinsa bylgjugögnin.</span><span class="sxs-lookup"><span data-stu-id="0de26-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="0de26-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="0de26-109">Cause</span></span>

<span data-ttu-id="0de26-110">Bylgjan er í vinnslu eins og gefið er til kynna með einu af eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="0de26-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="0de26-111">Reiturinn **Staða bylgju** er stilltur á *Keyrir*.</span><span class="sxs-lookup"><span data-stu-id="0de26-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="0de26-112">Þegar þú velur **Runuvinnsla** í hópnum **Bylgja** á flipanum **Bylgja** í aðgerðasvæðinu er **Staða** reiturinn ekki stilltur á *Lokið*, *Villa* eða *Hætt við*.</span><span class="sxs-lookup"><span data-stu-id="0de26-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="0de26-113">Þess vegna er runuvinnsla í keyrslu.</span><span class="sxs-lookup"><span data-stu-id="0de26-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="0de26-114">Upplausn</span><span class="sxs-lookup"><span data-stu-id="0de26-114">Resolution</span></span>

<span data-ttu-id="0de26-115">Á Aðgerðasvæði, á flipanum **Bylgja** í **flokknum Bylgja** skal velja **Runuvinnsla** og síðan fylgja einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="0de26-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="0de26-116">Ef **Staða** svæðið er stillt á *Keyra*: Á Aðgerðasvæði, á flipanum **Runuvinnsla** í **flokknum Runuvinnsla** skal velja **Skoða verkefni**.</span><span class="sxs-lookup"><span data-stu-id="0de26-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="0de26-117">Hægt er að fylgjast með framvindunni með því að uppfæra síðuna **Runuverk**.</span><span class="sxs-lookup"><span data-stu-id="0de26-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="0de26-118">Ef **Staða** svæðið er ekki stillt á *Keyra*: Á Aðgerðasvæði, á flipanum **Runuvinnsla** í flokknum **Aðgerðir** skal velja **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="0de26-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="0de26-119">Í **Velja nýja stöðu** reitnum skal velja *Í bið*.</span><span class="sxs-lookup"><span data-stu-id="0de26-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="0de26-120">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0de26-120">Then select **OK**.</span></span>
