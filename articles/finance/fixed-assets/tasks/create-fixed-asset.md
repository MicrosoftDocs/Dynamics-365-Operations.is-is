---
title: Stofna eign
description: Þetta efnisatriði útskýrir hvernig á að stofna nýja eignafærslu úr listasíðu eignar.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817102"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="e225d-103">Stofna eign</span><span class="sxs-lookup"><span data-stu-id="e225d-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e225d-104">Þetta efnisatriði útskýrir hvernig á að stofna nýja eignafærslu af listasíðunni **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="e225d-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="e225d-105">Kerfið úthlutar eignanúmeri, byggt á númeraröðinni sem er úthlutað á eignaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e225d-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="e225d-106">Ef þú notar eignarsniðmátið til að flytja inn eignir í Microsoft Excel -innbót, eða ef þú notar annað innflutningsverk stofnar kerfið sjálfkrafa eignafærslur og stigvaxandi eignanúmer.</span><span class="sxs-lookup"><span data-stu-id="e225d-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="e225d-107">Til að stofna eignafærslu handvirkt skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e225d-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="e225d-108">Opnaðu **Yfirlitssvæði \> Einingar \> Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="e225d-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="e225d-109">Í **aðgerðarúðunni** velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e225d-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="e225d-110">Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e225d-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="e225d-111">Reiturinn **Númer** verður sjálfkrafa ef búið er að virkja **Sjálfvirka tölusetninaraðgerð eigna** í **Færibreytum eigna** og **Eignaflokki**.</span><span class="sxs-lookup"><span data-stu-id="e225d-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="e225d-112">Færa skal inn einkvæman kóða til að auðkenna eignina.</span><span class="sxs-lookup"><span data-stu-id="e225d-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="e225d-113">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e225d-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="e225d-114">Færið inn viðbótarupplýsingar sem fyrirtækið þarf fyrir þessa eign.</span><span class="sxs-lookup"><span data-stu-id="e225d-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="e225d-115">Á **aðgerðasvæðinu** skal velja **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="e225d-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="e225d-116">Í reitinn **Kaupdagsetning** skal rita dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="e225d-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="e225d-117">Í reitinn **Kaupverð** skal rita tölu.</span><span class="sxs-lookup"><span data-stu-id="e225d-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="e225d-118">Sláið inn viðbótarupplýsingar sem fyrirtæki þarf fyrir þessa bók.</span><span class="sxs-lookup"><span data-stu-id="e225d-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="e225d-119">Færið inn viðbótarupplýsingar sem fyrirtækið þarf fyrir eftirstandandi bækur.</span><span class="sxs-lookup"><span data-stu-id="e225d-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="e225d-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e225d-120">Close the page.</span></span>

<span data-ttu-id="e225d-121">Einnig er hægt að flytja eignir inn með Excel-innbót eða með því að nota innflutningsverk úr **Gagnastjórnun** vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="e225d-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="e225d-122">Áður en innflutningur er keyrður skal færa inn gildin fyrir áskilda reiti í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="e225d-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="e225d-123">Ef þú hefur ekki skilgreint eignanúmerið í sniðmáti Excel-innbótarinnar, eða í gagnastjórnun, stofnar kerfið númer eignar fyrir hverja innflutta eign og raðar sjálfkrafa númeraröðinni fyrir hverja.</span><span class="sxs-lookup"><span data-stu-id="e225d-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="e225d-124">Ef eignir eru hins vegar fluttar inn og skilgreind eignarnúmer í sniðmátinu er númeraröðinni **ekki** sjálfkrafa stigskipt.</span><span class="sxs-lookup"><span data-stu-id="e225d-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="e225d-125">Í þessu tilviki gæti stjórnandi þurft að uppfæra númeraröðina handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e225d-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="e225d-126">Ef eignanúmerið var skilgreint í sniðmáti Excel-innbótarinnar notar kerfið skilgreint eignanúmerið og stigvaxandi númeraröðina.</span><span class="sxs-lookup"><span data-stu-id="e225d-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="e225d-127">Eftir að afskriftin hefur verið bókfærð eru reitirnir **Tekin í notkun** og **Dagsetning afskriftarkeyrslu** læstir á síðunni **Bók**.</span><span class="sxs-lookup"><span data-stu-id="e225d-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="e225d-128">Hvorugt svæðið verður uppfært úr gagnaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="e225d-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="e225d-129">Eignafærslu er ekki eytt ef færslur voru bókaðar í tengdu bókinni eða ef nýstofnaða eignin er færð inn í færslubókarlínu en ekki bókuð.</span><span class="sxs-lookup"><span data-stu-id="e225d-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]