---
title: 'Leiðbeiningar: Breyta eftirspurnarspá handvirkt'
description: Í þessu efnisatriði er útskýrt hvernig á að breyta spá fyrir vöru
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224011"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="f5570-103">Leiðbeiningar: Breyta eftirspurnarspá handvirkt</span><span class="sxs-lookup"><span data-stu-id="f5570-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5570-104">Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="f5570-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="f5570-105">Þetta ferli er ætluð fyrir framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="f5570-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="f5570-106">Breyta spá fyrir valda vöru</span><span class="sxs-lookup"><span data-stu-id="f5570-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="f5570-107">Til að breyta spá fyrir valið atriði:</span><span class="sxs-lookup"><span data-stu-id="f5570-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="f5570-108">Farið í **Einingar \> Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="f5570-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f5570-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f5570-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="f5570-110">Velja vöruna sem ætlunin er að breyta spánni.</span><span class="sxs-lookup"><span data-stu-id="f5570-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="f5570-111">Á aðgerðasvæðinu skal opna flipann **Áætlun** og velja **Eftirspurnarspá**.</span><span class="sxs-lookup"><span data-stu-id="f5570-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="f5570-112">Í listanum velurðu línu.</span><span class="sxs-lookup"><span data-stu-id="f5570-112">In the list, select a row.</span></span> <span data-ttu-id="f5570-113">Ef það eru engar spárlínur skal stofna nýja línu með því að velja **Ný** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="f5570-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="f5570-114">Í reitnum **Sölumagn** skal slá inn jákvæða tölu.</span><span class="sxs-lookup"><span data-stu-id="f5570-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="f5570-115">Þetta númer stendur fyrir spáð magn vörunnar.</span><span class="sxs-lookup"><span data-stu-id="f5570-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="f5570-116">Villa birtist ef neikvæð tala er færð inn.</span><span class="sxs-lookup"><span data-stu-id="f5570-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="f5570-117">Fyllið út í önnur svæði eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f5570-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="f5570-118">Í aðgerðaglugganum velurðu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f5570-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="f5570-119">Breyta spá fyrir eina eða fleiri vörur með Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="f5570-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="f5570-120">Til að breyta spá fyrir eina eða fleiri vörur með Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="f5570-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="f5570-121">Gerið eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="f5570-121">Do one of the following:</span></span>
    - <span data-ttu-id="f5570-122">Farið á síðuna **Eftirspurnarspá** fyrir einhverja vöru (skiptir ekki máli hvaða vöru) eins og lýst er í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="f5570-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="f5570-123">Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Eftirspurnarspárlínur**.</span><span class="sxs-lookup"><span data-stu-id="f5570-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="f5570-124">Á aðgerðasvæðinu skal velja **Opna í Microsoft Office \> Eftirspurnarspáfærslur**.</span><span class="sxs-lookup"><span data-stu-id="f5570-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="f5570-125">Veljið niðurhalsstað, vistið og opnið síðan sótta skrá í Excel.</span><span class="sxs-lookup"><span data-stu-id="f5570-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="f5570-126">Ef viðvörun kemur upp skal velja **Virkja breytingar**.</span><span class="sxs-lookup"><span data-stu-id="f5570-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="f5570-127">Í Excel skal skrá sig inn í Supply Chain Management með því að nota Microsoft Dynamics verksvæðið.</span><span class="sxs-lookup"><span data-stu-id="f5570-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="f5570-128">Nauðsynlegt er að skrá sig inn með valkostinn **Halda mér innskráðum** virkan og treysta verður á gagnatengingarforritið.</span><span class="sxs-lookup"><span data-stu-id="f5570-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="f5570-129">Excel-töflureiknirinn sýnir nú allar núverandi eftirspurnarspárlínur fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f5570-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="f5570-130">Bætið við, eyðið og breytið eftirspurnarspárlínum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f5570-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="f5570-131">Veljið **Birta** á Microsoft Dynamics verksvæðinu til að hlaða breytingunum aftur upp í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f5570-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
