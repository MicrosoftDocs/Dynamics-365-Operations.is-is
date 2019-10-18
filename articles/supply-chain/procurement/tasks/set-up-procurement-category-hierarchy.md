---
title: Setja upp stigveldi innkaupategundar
description: Þetta ferli sýnir hvernig á að stofna nýja hnúta í tegundastigveldi innkaupa og hvernig á að skilgreina innkaupategund sem nota á í innkaupaferli.
author: mkirknel
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7010a1c612b9b3884c675f578657d951da06c38
ms.sourcegitcommit: 25fe679b73663fda6b5b3c32646026d0993a9f00
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/12/2019
ms.locfileid: "1995283"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="bdf40-103">Setja upp stigveldi innkaupategundar</span><span class="sxs-lookup"><span data-stu-id="bdf40-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdf40-104">Þetta ferli sýnir hvernig á að stofna nýja hnúta í tegundastigveldi innkaupa og hvernig á að skilgreina innkaupategund sem nota á í innkaupaferli.</span><span class="sxs-lookup"><span data-stu-id="bdf40-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="bdf40-105">Þessum verkefnum myndi venjulega að framkvæma af Innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="bdf40-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="bdf40-106">Áður en hægt er að hefja ferlið, verður að vera tegundastigveldi af gerðinni Innkaup.</span><span class="sxs-lookup"><span data-stu-id="bdf40-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="bdf40-107">Ef verið er að nota sýnigögn fyrirtæki er hægt að keyra þetta ferli í USMF fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="bdf40-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="bdf40-108">Bæta við nýrri innkaupategund</span><span class="sxs-lookup"><span data-stu-id="bdf40-108">Add a new procurement category</span></span>
1. <span data-ttu-id="bdf40-109">Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Vörusending > Innkaupaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="bdf40-110">Í aðgerðarúðunni velurðu **Breyta tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-110">On the action pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="bdf40-111">Núverandi tegundastigveldi birtist vinstra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="bdf40-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="bdf40-112">Verið er að breyta stigveldi.</span><span class="sxs-lookup"><span data-stu-id="bdf40-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="bdf40-113">Í aðgerðarúðunni velurðu **Nýr tegundahnútur**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-113">On the action pane, select **New category node**.</span></span> <span data-ttu-id="bdf40-114">Kerfið velur topphnútinn sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="bdf40-114">The system selects the top node by default.</span></span> <span data-ttu-id="bdf40-115">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk, er hægt að smella á hnappinn Aflæsa og velja annan yfirhnút til að setja inn nýjan hnútinn þinn.</span><span class="sxs-lookup"><span data-stu-id="bdf40-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="bdf40-116">Þegar því er lokið, skal loka aftur leiðarvísi fyrir verk og smellið síðan á Nýjan tegundahnút.</span><span class="sxs-lookup"><span data-stu-id="bdf40-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="bdf40-117">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bdf40-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="bdf40-118">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bdf40-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="bdf40-119">Í reitnum **Stutt heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="bdf40-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="bdf40-120">Stutt heiti er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="bdf40-120">The friendly name is optional.</span></span> <span data-ttu-id="bdf40-121">Það verður birt í uppflettingu tegunda ásamt heiti flokks.</span><span class="sxs-lookup"><span data-stu-id="bdf40-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="bdf40-122">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="bdf40-123">Bæta afurðum við nýja innkaupategund</span><span class="sxs-lookup"><span data-stu-id="bdf40-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="bdf40-124">Farðu í **Innkaup og aðföng > Vörusending > Innkaupaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="bdf40-125">Velja hnút sem var nýlega bætt við.</span><span class="sxs-lookup"><span data-stu-id="bdf40-125">Select the node you just added.</span></span> <span data-ttu-id="bdf40-126">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk gæti þurft að aflæsa leiðarvísi fyrir verk til að velja hnútinn.</span><span class="sxs-lookup"><span data-stu-id="bdf40-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="bdf40-127">Víxla útvíkkun á liðnum **Afurðir**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="bdf40-128">Veldu **Bæta við** til að tengja afurðir við innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="bdf40-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="bdf40-129">Velja afurðir sem á að bæta við innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="bdf40-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="bdf40-130">Veldu örina til að bæta afurðunum við töfluna **Valið**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="bdf40-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bdf40-131">Select **OK**.</span></span>
