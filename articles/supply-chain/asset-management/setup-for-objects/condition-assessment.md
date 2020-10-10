---
title: Ástandsmat
description: Þetta efni útskýrir hvernig á að búa til ástandsmatsmát og skráningu á eign í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 774c788959c5ebea69b4d22c886ac673f50b97f5
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889794"
---
# <a name="condition-assessment"></a><span data-ttu-id="af368-103">Ástandsmat</span><span class="sxs-lookup"><span data-stu-id="af368-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="af368-104">Þetta efni útskýrir hvernig á að búa til ástandsmatsmát og skráningu á eign í eignastýringu.</span><span class="sxs-lookup"><span data-stu-id="af368-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="af368-105">Ástandsmat er framkvæmt með reglulegu millibili og meginmarkmiðið er að búa til og viðhalda skilyrðum um eignir.</span><span class="sxs-lookup"><span data-stu-id="af368-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="af368-106">Séð frá fyrirbyggjandi viðhaldssjónarmiði er mikilvægt að fylgjast með lykilupplýsingum eins og núverandi ástandi og endingartíma.</span><span class="sxs-lookup"><span data-stu-id="af368-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="af368-107">Enn fremur, ef þú framkvæmir ástandsmat með reglulegu millibili, muntu geta fylgst með og borið saman aðstæður á vélum í verksmiðjunni.</span><span class="sxs-lookup"><span data-stu-id="af368-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="af368-108">Hægt er að nota ástandsmat til að mæla og hafa eftirlit með mörgum aðstæðum á búnaði þínum.</span><span class="sxs-lookup"><span data-stu-id="af368-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="af368-109">Dæmi: Þú gætir mælt titring á vélunum þínum.</span><span class="sxs-lookup"><span data-stu-id="af368-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="af368-110">Eftir að þú hefur skráð titringsmælingar í Eignastjórnun á ýmsum gerðum búnaðar geturðu leitað að nýjasta skráða matinu og skoðað titringsmælingar.</span><span class="sxs-lookup"><span data-stu-id="af368-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="af368-111">Skilyrðamat er búið til á eignir.</span><span class="sxs-lookup"><span data-stu-id="af368-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="af368-112">Þú setur upp sniðmát fyrir mat á ástandi á eignategund áður en þú framkvæmir skilyrði fyrir mati á ástandi.</span><span class="sxs-lookup"><span data-stu-id="af368-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="af368-113">Ástæðan fyrir því að nota sniðmát til ástandsmats er að forðast breytileika á gögnum um svipaðar eignir.</span><span class="sxs-lookup"><span data-stu-id="af368-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="af368-114">Röðin til að setja upp og nota ástandsmat í eignastjórnun er: Fyrst setur þú upp nauðsynleg skilyrði fyrir mat á ástandi.</span><span class="sxs-lookup"><span data-stu-id="af368-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="af368-115">Næst tengir þú sniðmát við eignategundir í forminu **Gerðir eigna**.</span><span class="sxs-lookup"><span data-stu-id="af368-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="af368-116">Að lokum geturðu búið til skráningar á matsástandi á eign í forminu **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="af368-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="af368-117">Búðu til sniðmát fyrir ástandsmat</span><span class="sxs-lookup"><span data-stu-id="af368-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="af368-118">Veldu **Eignastýring** > **Uppsetning** > **Eignagerðir** > **Ástandsmat**.</span><span class="sxs-lookup"><span data-stu-id="af368-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="af368-119">Veldu **Nýtt** til að stofna nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="af368-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="af368-120">Settu inn auðkenni fyrir sniðmátið í reitnum **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="af368-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="af368-121">Í reitnum **Heiti** slærðu inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="af368-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="af368-122">Á flýtiflipann **Línur ástandsmats** bætirðu við línum sem krafist er fyrir ástandsmatið, þar með talið val á viðeigandi ástandsgerð og mælieining.</span><span class="sxs-lookup"><span data-stu-id="af368-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="af368-123">Á flýtiflipanum **Eignagerðir** bætirðu við eignagerðum sem ættu að nota sniðmátið fyrir ástandsmat.</span><span class="sxs-lookup"><span data-stu-id="af368-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="af368-124">Í reitunum **Línur** og **Eignagerðir** í hópnum **Upplýsingar** efst á skjánum muntu sjá fjölda matslína og eignagerða sem tengjast völdu sniðmáti fyrir ástandsmat.</span><span class="sxs-lookup"><span data-stu-id="af368-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="af368-125">Búðu til skráningu á matsástandi á eign</span><span class="sxs-lookup"><span data-stu-id="af368-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="af368-126">Veldu **Eignastýring** > **Sameiginlegt** > **Eignir** > **Allar eignir**.</span><span class="sxs-lookup"><span data-stu-id="af368-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="af368-127">Í listanum velurðu eignina sem þú vilt stofna skráningu ástandsmats fyrir.</span><span class="sxs-lookup"><span data-stu-id="af368-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="af368-128">Á flipanum **Almennt** er smellt á **Ástandsmat**.</span><span class="sxs-lookup"><span data-stu-id="af368-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="af368-129">Smelltu á **Nýtt** til að búa til nýja skráningu.</span><span class="sxs-lookup"><span data-stu-id="af368-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="af368-130">Veldu dagsetningu fyrir ástandsmatið í reitnum **Dagsetning**.</span><span class="sxs-lookup"><span data-stu-id="af368-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="af368-131">Veldu nafn starfsmannsins sem framkvæmdi matsskráninguna í reitnum **Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="af368-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="af368-132">Í reitnum **Línur** sérðu fjölda matslína sem settar eru upp í ástandasmati.</span><span class="sxs-lookup"><span data-stu-id="af368-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="af368-133">Veldu sniðmát fyrir ástandsmatið í reitnum **Sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="af368-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="af368-134">Heiti sniðmátsins er sjálfkrafa sett inn í reitnum **Heiti** og tengdar skráningarlínur eru settar inn á flýtiflipann **Línur ástandsmats**.</span><span class="sxs-lookup"><span data-stu-id="af368-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="af368-135">Þú getur sett inn athugasemdir sem tengjast völdum ástandsmati á flýtiflipann **Athugasemdir**.</span><span class="sxs-lookup"><span data-stu-id="af368-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="af368-136">Fyrir hverja línu ástandsmats skal setja inn mælingargögn í reitinn **Gildi**.</span><span class="sxs-lookup"><span data-stu-id="af368-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="af368-137">Hægt er að segja inn athugasemd varðandi valda skráningarlínu á flýtiflipann **Línur ástandsmats** > reitnum **Athugasemdir**.</span><span class="sxs-lookup"><span data-stu-id="af368-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="af368-138">Ef þú bætir athugasemd við línu, þá er gátreiturinn **Athugasemd** sjálfkrafa valinn.</span><span class="sxs-lookup"><span data-stu-id="af368-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="af368-139">Eftir að þú ert búinn að gera skráningu á ástandsmati á eign geturðu prentað skýrslu um ástandsmat.</span><span class="sxs-lookup"><span data-stu-id="af368-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="af368-140">Þú getur líka skráð ástandsmat í verkbeiðnihnappi (**Eignastýring** > **Sameiginlegt** > **Verkbeiðni** > **Allar verkbeiðnir** > **Ástandsmat**.)</span><span class="sxs-lookup"><span data-stu-id="af368-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
