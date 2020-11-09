---
title: Stofna eign
description: Þetta efnisatriði útskýrir hvernig á að stofna nýja eignafærslu úr listasíðu eignar.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000244"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="e6d10-103">Stofna eign</span><span class="sxs-lookup"><span data-stu-id="e6d10-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6d10-104">Þetta efnisatriði útskýrir hvernig á að stofna nýja eignafærslu af listasíðunni **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="e6d10-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="e6d10-105">Kerfið úthlutar eignanúmeri, byggt á númeraröðinni sem er úthlutað á eignaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="e6d10-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="e6d10-106">Ef þú notar eignarsniðmátið til að flytja inn eignir í Microsoft Excel -innbót, eða ef þú notar annað innflutningsverk stofnar kerfið sjálfkrafa eignafærslur og stigvaxandi eignanúmer.</span><span class="sxs-lookup"><span data-stu-id="e6d10-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="e6d10-107">Til að stofna eignafærslu handvirkt skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e6d10-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="e6d10-108">Opnaðu **Yfirlitssvæði \> Einingar \> Eignir \> Eignir \> Eignir**.</span><span class="sxs-lookup"><span data-stu-id="e6d10-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="e6d10-109">Í **aðgerðarúðunni** velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e6d10-109">On the **Action pane** , select **New**.</span></span>
3. <span data-ttu-id="e6d10-110">Í reitnum **Eignaflokkur** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e6d10-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="e6d10-111">Reiturinn **Númer** verður sjálfkrafa ef búið er að virkja **Sjálfvirka tölusetninaraðgerð eigna** í **Færibreytum eigna** og **Eignaflokki**.</span><span class="sxs-lookup"><span data-stu-id="e6d10-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="e6d10-112">Færa skal inn einkvæman kóða til að auðkenna eignina.</span><span class="sxs-lookup"><span data-stu-id="e6d10-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="e6d10-113">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e6d10-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="e6d10-114">Færið inn viðbótarupplýsingar sem fyrirtækið þarf fyrir þessa eign.</span><span class="sxs-lookup"><span data-stu-id="e6d10-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="e6d10-115">Á **aðgerðasvæðinu** skal velja **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="e6d10-115">On the **Action pane** , select **Books**.</span></span>
6. <span data-ttu-id="e6d10-116">Í reitinn **Kaupdagsetning** skal rita dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="e6d10-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="e6d10-117">Í reitinn **Kaupverð** skal rita tölu.</span><span class="sxs-lookup"><span data-stu-id="e6d10-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="e6d10-118">Sláið inn viðbótarupplýsingar sem fyrirtæki þarf fyrir þessa bók.</span><span class="sxs-lookup"><span data-stu-id="e6d10-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="e6d10-119">Færið inn viðbótarupplýsingar sem fyrirtækið þarf fyrir eftirstandandi bækur.</span><span class="sxs-lookup"><span data-stu-id="e6d10-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="e6d10-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e6d10-120">Close the page.</span></span>

<span data-ttu-id="e6d10-121">Einnig er hægt að flytja eignir inn með Excel-innbót eða með því að nota innflutningsverk úr **Gagnastjórnun** vinnusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="e6d10-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="e6d10-122">Áður en innflutningur er keyrður skal færa inn gildin fyrir áskilda reiti í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="e6d10-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="e6d10-123">Ef þú hefur ekki skilgreint eignanúmerið í sniðmáti Excel-innbótarinnar, eða í gagnastjórnun, stofnar kerfið númer eignar fyrir hverja innflutta eign og raðar sjálfkrafa númeraröðinni fyrir hverja.</span><span class="sxs-lookup"><span data-stu-id="e6d10-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="e6d10-124">Ef eignir eru hins vegar fluttar inn og skilgreind eignarnúmer í sniðmátinu er númeraröðinni **ekki** sjálfkrafa stigskipt.</span><span class="sxs-lookup"><span data-stu-id="e6d10-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="e6d10-125">Í þessu tilviki gæti stjórnandi þurft að uppfæra númeraröðina handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e6d10-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="e6d10-126">Ef eignanúmerið var skilgreint í sniðmáti Excel-innbótarinnar notar kerfið skilgreint eignanúmerið og stigvaxandi númeraröðina.</span><span class="sxs-lookup"><span data-stu-id="e6d10-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>
