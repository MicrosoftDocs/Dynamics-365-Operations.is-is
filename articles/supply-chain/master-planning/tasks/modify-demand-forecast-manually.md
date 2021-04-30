---
title: Breyta eftirspurnarspá handvirkt
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889025"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="a472a-103">Breyta eftirspurnarspá handvirkt</span><span class="sxs-lookup"><span data-stu-id="a472a-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a472a-104">Þessi verklýsing sýnir hvernig á að breyta spá fyrir vöru.</span><span class="sxs-lookup"><span data-stu-id="a472a-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="a472a-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="a472a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a472a-106">Þetta ferli er ætluð fyrir framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="a472a-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="a472a-107">Breyta spá fyrir valda vöru</span><span class="sxs-lookup"><span data-stu-id="a472a-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="a472a-108">Til að breyta spá fyrir valið atriði:</span><span class="sxs-lookup"><span data-stu-id="a472a-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="a472a-109">Farið í **Einingar \> Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="a472a-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a472a-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a472a-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="a472a-111">Velja vöruna sem ætlunin er að breyta spánni.</span><span class="sxs-lookup"><span data-stu-id="a472a-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="a472a-112">Á aðgerðasvæðinu skal opna flipann **Áætlun** og velja **Eftirspurnarspá**.</span><span class="sxs-lookup"><span data-stu-id="a472a-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="a472a-113">Í listanum velurðu línu.</span><span class="sxs-lookup"><span data-stu-id="a472a-113">In the list, select a row.</span></span> <span data-ttu-id="a472a-114">Ef það eru engar spárlínur skal stofna nýja línu með því að velja **Ný** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="a472a-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="a472a-115">Í reitnum **Sölumagn** skal slá inn jákvæða tölu.</span><span class="sxs-lookup"><span data-stu-id="a472a-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="a472a-116">Þetta númer stendur fyrir spáð magn vörunnar.</span><span class="sxs-lookup"><span data-stu-id="a472a-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="a472a-117">Villa birtist ef neikvæð tala er færð inn.</span><span class="sxs-lookup"><span data-stu-id="a472a-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="a472a-118">Fyllið út í önnur svæði eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="a472a-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="a472a-119">Í aðgerðaglugganum velurðu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a472a-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="a472a-120">Breyta spá fyrir eina eða fleiri vörur Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="a472a-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="a472a-121">Til að breyta spá fyrir eina eða fleiri vörur Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="a472a-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="a472a-122">Gerið eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="a472a-122">Do one of the following:</span></span>
    - <span data-ttu-id="a472a-123">Farið á síðuna **Eftirspurnarspá** fyrir einhverja vöru (skiptir ekki máli hvaða vöru) eins og lýst er í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="a472a-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="a472a-124">Farið í **Aðaláætlanagerð \> Spá \> Handvirk spárfærsla \> Eftirspurnarspárlínur**.</span><span class="sxs-lookup"><span data-stu-id="a472a-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="a472a-125">Á aðgerðasvæðinu skal velja **Opna í Microsoft Office \> Eftirspurnarspáfærslur**.</span><span class="sxs-lookup"><span data-stu-id="a472a-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="a472a-126">Veljið niðurhalsstað, vistið og opnið síðan sótta skrá í Excel.</span><span class="sxs-lookup"><span data-stu-id="a472a-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="a472a-127">Ef viðvörun kemur upp skal velja **Virkja breytingar**.</span><span class="sxs-lookup"><span data-stu-id="a472a-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="a472a-128">Í Excel skal skrá sig inn í Supply Chain Management með því að nota Microsoft Dynamics verksvæðið.</span><span class="sxs-lookup"><span data-stu-id="a472a-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="a472a-129">Nauðsynlegt er að skrá sig inn með valkostinn **Halda mér innskráðum** virkan og treysta verður á gagnatengingarforritið.</span><span class="sxs-lookup"><span data-stu-id="a472a-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="a472a-130">Excel-töflureiknirinn sýnir nú allar núverandi eftirspurnarspárlínur fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="a472a-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="a472a-131">Bætið við, eyðið og breytið eftirspurnarspárlínum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="a472a-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="a472a-132">Veljið **Birta** á Microsoft Dynamics verksvæðinu til að hlaða breytingunum aftur upp í Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a472a-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
