---
title: Ábyrgðarsamningar
description: Þetta efni útskýrir ábyrgðarsamninga í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: da60d098aff96780ca1e40832db34e3c9cc835e7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569686"
---
# <a name="warranty-agreements"></a><span data-ttu-id="746c7-103">Ábyrgðarsamningar</span><span class="sxs-lookup"><span data-stu-id="746c7-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="746c7-104">Í eignastjórnun geturðu sett upp ábyrgðarskilmála sem hægt er að tengja við eign eða eignategund.</span><span class="sxs-lookup"><span data-stu-id="746c7-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="746c7-105">Ábyrgðarskilmálar eru búnir til fyrir tiltekið tímabil.</span><span class="sxs-lookup"><span data-stu-id="746c7-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="746c7-106">Hægt er að setja upp ábyrgð til að veita fulla tryggingu eða hlutfallslega tryggingu og þú getur sett upp skilmála sem tengjast tíma, kostnaði og vörum.</span><span class="sxs-lookup"><span data-stu-id="746c7-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="746c7-107">Fyrsta skrefið er að búa til hvaða ábyrgðarsamninga lánardrottna sem þú hefur fyrir búnaðinn þinn.</span><span class="sxs-lookup"><span data-stu-id="746c7-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="746c7-108">Þú hengir síðan ábyrgðarsamninga við eignir eða eignategundir.</span><span class="sxs-lookup"><span data-stu-id="746c7-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="746c7-109">Ábyrgðarsamningar lánardrottna eru aðeins notaðir til upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="746c7-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="746c7-110">Ef ábyrgð lánardrottins er sett upp á eign geturðu séð ábyrgðartímabil tryggingar á eigninni.</span><span class="sxs-lookup"><span data-stu-id="746c7-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="746c7-111">Stofna ábyrgðarsamning</span><span class="sxs-lookup"><span data-stu-id="746c7-111">Create a warranty agreement</span></span>

<span data-ttu-id="746c7-112">Í ábyrgðarsamningi geta verið nokkrar samningslínur til að standa straum af ábyrgðinni á vinnutíma, kostnaði og hlutum.</span><span class="sxs-lookup"><span data-stu-id="746c7-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="746c7-113">Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Ábyrgð**.</span><span class="sxs-lookup"><span data-stu-id="746c7-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="746c7-114">Veljið **Ný** til að stofna nýja afurð.</span><span class="sxs-lookup"><span data-stu-id="746c7-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="746c7-115">Í reitinn **Ábyrgð** skaltu færa inn kenni ábyrgðar.</span><span class="sxs-lookup"><span data-stu-id="746c7-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="746c7-116">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="746c7-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="746c7-117">Á flýtflipanum **Upplýsingar** sýnir reiturinn **Eignir** fjölda virkra eigna sem nota ábyrgðarsamninginn.</span><span class="sxs-lookup"><span data-stu-id="746c7-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="746c7-118">Á flýtiflipunum **Klukkustundaábyrgð** og **Vöruábyrgð** skaltu fylgja þessum skrefum til að bæta við línum sem ættu að vera með í ábyrgðarsamningi sem lýtur að klukkustundum eða vörum:</span><span class="sxs-lookup"><span data-stu-id="746c7-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="746c7-119">Veljið **Bæta við línu** til að bæta nýju skilyrði við ábyrgðina.</span><span class="sxs-lookup"><span data-stu-id="746c7-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="746c7-120">Raðlínunúmer er sjálfvirkt sett inn í reitinn **Lína**.</span><span class="sxs-lookup"><span data-stu-id="746c7-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="746c7-121">Í reitinn **Tímabil** skal velja gerð ábyrgðartímabils.</span><span class="sxs-lookup"><span data-stu-id="746c7-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="746c7-122">Í reitinn **Tímabil** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="746c7-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="746c7-123">Þessi reitur skilgreinir fjölda tímabila sem ábyrgðin ætti að gilda fyrir.</span><span class="sxs-lookup"><span data-stu-id="746c7-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="746c7-124">Í reitnum **Prósenta** slærðu inn tryggingarhlutfall fyrir ábyrgðarlínuna.</span><span class="sxs-lookup"><span data-stu-id="746c7-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="746c7-125">Hlutfallið gefur til kynna hve mikið fyrirtækið þitt tryggir.</span><span class="sxs-lookup"><span data-stu-id="746c7-125">The percentage indicates how much is covered by your company.</span></span>

![Ábyrgðarsíða](media/01-warranty.png)
