---
title: Setja upp stigveldi innkaupategundar
description: Þetta ferli sýnir hvernig á að stofna nýja hnúta í tegundastigveldi innkaupa og hvernig á að skilgreina innkaupategund sem nota á í innkaupaferli.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569892"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="26d05-103">Setja upp stigveldi innkaupategundar</span><span class="sxs-lookup"><span data-stu-id="26d05-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26d05-104">Þetta ferli sýnir hvernig á að stofna nýja hnúta í tegundastigveldi innkaupa og hvernig á að skilgreina innkaupategund sem nota á í innkaupaferli.</span><span class="sxs-lookup"><span data-stu-id="26d05-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="26d05-105">Þessum verkefnum myndi venjulega að framkvæma af Innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="26d05-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="26d05-106">Áður en hægt er að hefja ferlið, verður að vera tegundastigveldi af gerðinni Innkaup.</span><span class="sxs-lookup"><span data-stu-id="26d05-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="26d05-107">Ef verið er að nota sýnigögn fyrirtæki er hægt að keyra þetta ferli í USMF fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="26d05-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="26d05-108">Bæta við nýrri innkaupategund</span><span class="sxs-lookup"><span data-stu-id="26d05-108">Add a new procurement category</span></span>
1. <span data-ttu-id="26d05-109">Fara í Innkaup og uppruni > Innkaupaflokkar.</span><span class="sxs-lookup"><span data-stu-id="26d05-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="26d05-110">Smella á Breyta tegundastigveldi.</span><span class="sxs-lookup"><span data-stu-id="26d05-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="26d05-111">Núverandi tegundastigveldi birtist vinstra megin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="26d05-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="26d05-112">Verið er að breyta stigveldi.</span><span class="sxs-lookup"><span data-stu-id="26d05-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="26d05-113">Smellt er á Nýr tegundahnútur.</span><span class="sxs-lookup"><span data-stu-id="26d05-113">Click New category node.</span></span>
    * <span data-ttu-id="26d05-114">Kerfið velur topphnútinn sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="26d05-114">The system selects the top node by default.</span></span> <span data-ttu-id="26d05-115">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk, er hægt að smella á hnappinn Aflæsa og velja annan yfirhnút til að setja inn nýjan hnútinn þinn.</span><span class="sxs-lookup"><span data-stu-id="26d05-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="26d05-116">Þegar því er lokið, skal loka aftur leiðarvísi fyrir verk og smellið síðan á Nýjan tegundahnút.</span><span class="sxs-lookup"><span data-stu-id="26d05-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="26d05-117">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="26d05-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="26d05-118">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="26d05-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="26d05-119">Í reitinn stutt heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="26d05-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="26d05-120">Stutt heiti er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="26d05-120">The friendly name is optional.</span></span> <span data-ttu-id="26d05-121">Það verður birt í uppflettingu tegunda ásamt heiti flokks.</span><span class="sxs-lookup"><span data-stu-id="26d05-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="26d05-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="26d05-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="26d05-123">Bæta afurðum við nýja innkaupategund</span><span class="sxs-lookup"><span data-stu-id="26d05-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="26d05-124">Fara í Innkaup og uppruni > Innkaupaflokkar.</span><span class="sxs-lookup"><span data-stu-id="26d05-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="26d05-125">Velja hnút sem var nýlega bætt við.</span><span class="sxs-lookup"><span data-stu-id="26d05-125">Select the node you just added.</span></span> <span data-ttu-id="26d05-126">Ef verið er að keyra þetta ferli sem leiðarvísi fyrir verk gæti þurft að aflæsa leiðarvísi fyrir verk til að velja hnútinn.</span><span class="sxs-lookup"><span data-stu-id="26d05-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="26d05-127">Víxla útvíkkun á liðnum afurð.</span><span class="sxs-lookup"><span data-stu-id="26d05-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="26d05-128">Smella á bæta við til að tengja afurðir við innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="26d05-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="26d05-129">Velja afurð sem á að bæta við innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="26d05-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="26d05-130">Smellið á örina til að velja afurðina.</span><span class="sxs-lookup"><span data-stu-id="26d05-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="26d05-131">Veljið aðra afurð til að bæta við innkaupategundina.</span><span class="sxs-lookup"><span data-stu-id="26d05-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="26d05-132">Smellið á örina til að velja afurðina.</span><span class="sxs-lookup"><span data-stu-id="26d05-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="26d05-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="26d05-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="26d05-134">Bæta við samþykktum og æskilegum lánardrottnum</span><span class="sxs-lookup"><span data-stu-id="26d05-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="26d05-135">Víxla útvíkkun á liðnum lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="26d05-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="26d05-136">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="26d05-136">Click Add.</span></span>
    * <span data-ttu-id="26d05-137">Hægt er að bæta lánardrottni við innkaupategund og tilgreina hvort lánardrottinn sé útvalinn eða aðeins samþykktur fyrir flokkinn.</span><span class="sxs-lookup"><span data-stu-id="26d05-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="26d05-138">Þegar lánardrottni er eytt úr tegund, er sögulegum færslum með lánardrottininn í tegundinn ekki eytt.</span><span class="sxs-lookup"><span data-stu-id="26d05-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="26d05-139">Finna lánardrottins sem óskað er að bæta við tegund.</span><span class="sxs-lookup"><span data-stu-id="26d05-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="26d05-140">Smellið á örina til að velja lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="26d05-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="26d05-141">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="26d05-141">Click OK.</span></span>
6. <span data-ttu-id="26d05-142">Veldu lánardrottnalínuna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="26d05-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="26d05-143">Í reitnum Staða lánardrottins skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="26d05-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="26d05-144">Stillingin val lánardrottna í tegundarstefnureglu stjórnar því hvort æskilegt, samþykkt eða alla lánardrottna eru tiltækir á innkaupabeiðnum.</span><span class="sxs-lookup"><span data-stu-id="26d05-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="26d05-145">Bæta við frekari upplýsingum við tegund</span><span class="sxs-lookup"><span data-stu-id="26d05-145">Add additional information to the category</span></span>
1. <span data-ttu-id="26d05-146">Víxla útvíkkun á hlutanum matsviðmiðaflokkur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="26d05-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="26d05-147">Þessi flipi gerir mögulegt að skilgreina hvaða skilyrði lánardrottna í innkaupategund á að gefa einkunn gagnvart.</span><span class="sxs-lookup"><span data-stu-id="26d05-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="26d05-148">Til að gera þetta myndirðu smella á bæta Við og veljið síðan matsviðmiðunarflokkur lánardrottins sem inniheldur skilyrðin sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="26d05-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="26d05-149">Víxla útvíkkun á liðnum Spurningalisti.</span><span class="sxs-lookup"><span data-stu-id="26d05-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="26d05-150">Þessi flipi gerir mögulegt að bæta spurningalistum sem mun birtast í beiðninni, svo lengi sem stillt er á gerð Verkþáttar „Innkaupabeiðni".</span><span class="sxs-lookup"><span data-stu-id="26d05-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="26d05-151">Umsækjandinn þarf svo að fylla út spurningalista áður en þeir senda innkaupabeiðni fyrir tiltekna vöru eða afurðir í innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="26d05-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="26d05-152">Víxla útvíkkun á hlutanum VSK-flokkur vöru.</span><span class="sxs-lookup"><span data-stu-id="26d05-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="26d05-153">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="26d05-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="26d05-154">Velja VSK-flokk.</span><span class="sxs-lookup"><span data-stu-id="26d05-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="26d05-155">Víxla útvíkkun á liðnum tegundasíða.</span><span class="sxs-lookup"><span data-stu-id="26d05-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="26d05-156">Tegundarsíður eru stofnaðar í síðu tegundastigveldis.</span><span class="sxs-lookup"><span data-stu-id="26d05-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="26d05-157">Þær innihalda upplýsingar um innkaupategundina, eins og upplýsingar um tegund afurða í flokknum, myndir af afurðum í flokki eða tilkynningar um að afsláttur sé í boði í flokknum.</span><span class="sxs-lookup"><span data-stu-id="26d05-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="26d05-158">Upplýsingarnar í tegundasíðu birtist á innkaupabeiðnum.</span><span class="sxs-lookup"><span data-stu-id="26d05-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="26d05-159">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="26d05-159">Close the page.</span></span>

