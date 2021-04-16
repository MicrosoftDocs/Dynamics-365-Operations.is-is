---
title: Skoða og vinna með aðsetursbreytingar
description: Þetta efnisatriði útskýrir hvernig hægt er að skoða og hafa umsjón með breytingum á aðsetri í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5eca902ee7df7eb6835caf6f64b17f3f004b0776
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802456"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="7d34d-103">Skoða og vinna með aðsetursbreytingar</span><span class="sxs-lookup"><span data-stu-id="7d34d-103">View and manage address changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7d34d-104">Þetta efnisatriði útskýrir hvernig hægt er að skoða og hafa umsjón með breytingum á aðsetri á sjálfsafgreiðslusíðu starfsmanns **Breyta persónuupplýsingum** eða á upplýsingasíðunni **Starfsmaður** í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d34d-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7d34d-105">Mörg fyrirtæki vilja að starfsmenn hafi umsjón með persónulegum upplýsingum sínum í gegnum sjálfsafgreiðsluumhverfið.</span><span class="sxs-lookup"><span data-stu-id="7d34d-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="7d34d-106">Hægt er að leyfa notendum að uppfæra aðsetur sitt á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="7d34d-107">Síðan er hægt að fylgjast með þessum breytingum á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="7d34d-108">Til að nota þennan eiginleika þarf að tilgreina dagafjöldann sem á að skoða breytingar fyrir á síðunni **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="7d34d-109">Skilgreina færibreytur fyrir breytingu á aðsetri</span><span class="sxs-lookup"><span data-stu-id="7d34d-109">Configure address change parameters</span></span>

<span data-ttu-id="7d34d-110">Til að skilgreina fjölda daga sem birta á breytingar á aðsetri fyrir á vinnusvæðinu **Starfsmannastjórnun**, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="7d34d-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="7d34d-111">Á yfirlitssvæðinu skal velja **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="7d34d-112">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-112">Select **Links**.</span></span>

3. <span data-ttu-id="7d34d-113">Veljið **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="7d34d-114">Í reitinn **Fjöldi daga** undir **Breytingar á aðsetri**, skal slá inn dagafjöldann sem birta á breytingar á aðsetri fyrir á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="7d34d-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7d34d-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="7d34d-116">Stofna eða breyta aðsetri starfsmanns</span><span class="sxs-lookup"><span data-stu-id="7d34d-116">Create or change an employee address</span></span>

<span data-ttu-id="7d34d-117">Starfsmenn geta uppfært eigið aðsetur á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="7d34d-118">Fylgið þessum skrefum til að stofna eða breyta aðsetri:</span><span class="sxs-lookup"><span data-stu-id="7d34d-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="7d34d-119">Veldu reitinn **Sjálfsafgreiðsla starfsmanns** á heimasíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="7d34d-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="7d34d-120">Veldu **Breyta persónulegum upplýsingum**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="7d34d-121">Til að bæta við aðsetri skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-121">To add an address, select **Add**.</span></span> <span data-ttu-id="7d34d-122">Til að uppfæra fyrirliggjandi aðsetur skal velja aðsetrið í listanum og velja svo **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="7d34d-123">Færið inn **Heiti eða lýsing**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="7d34d-124">Veljið fellilistann **Tilgangur** og veljið síðan gerð aðseturs.</span><span class="sxs-lookup"><span data-stu-id="7d34d-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="7d34d-125">Færið inn **Land/svæði**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="7d34d-126">Færið inn **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="7d34d-127">Færið inn **Götuheiti**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="7d34d-128">Færið inn **Borg**, **Ríki** og **Sýsla**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="7d34d-129">Yfirleitt eru þessir reitir sjálfkrafa stilltir samkvæmt reitnum **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="7d34d-130">Einnig má velja reitinn **Aðal** til að gefa upp aðalaðsetur.</span><span class="sxs-lookup"><span data-stu-id="7d34d-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="7d34d-131">Aðeins er hægt að merkja eitt aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="7d34d-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="7d34d-132">Ef annað aðsetur er þegar merkt sem aðalaðsetur þarf að staðfesta að ætlunin sé að nota þetta aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="7d34d-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="7d34d-133">Það má velja reitinn **Einkamál** til að gefa til kynna að aðsetrið sé einkamál.</span><span class="sxs-lookup"><span data-stu-id="7d34d-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="7d34d-134">Aðeins notendur með sérstakar heimildir til að skoða upplýsingar um einkaaðsetur geta skoðað þetta aðsetur.</span><span class="sxs-lookup"><span data-stu-id="7d34d-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="7d34d-135">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="7d34d-136">Búa til eða breyta aðsetri starfsmanns</span><span class="sxs-lookup"><span data-stu-id="7d34d-136">Create or change a worker address</span></span>

<span data-ttu-id="7d34d-137">Hægt er að uppfæra aðsetur á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="7d34d-138">Fylgið þessum skrefum til að stofna eða breyta aðsetri:</span><span class="sxs-lookup"><span data-stu-id="7d34d-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="7d34d-139">Á vinnusvæðinu **Starfsmannastjórnun** skal velja **Tenglar** og síðan velja **Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="7d34d-140">Veljið starfsmanninn og því næst **Aðsetur**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="7d34d-141">Til að bæta við aðsetri skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-141">To add an address, select **Add**.</span></span> <span data-ttu-id="7d34d-142">Til að uppfæra fyrirliggjandi aðsetur skal velja aðsetrið í listanum og velja svo **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="7d34d-143">Færið inn **Heiti eða lýsing**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="7d34d-144">Veljið fellilistann **Tilgangur** og veljið síðan gerð aðseturs.</span><span class="sxs-lookup"><span data-stu-id="7d34d-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="7d34d-145">Færið inn **Land/svæði**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="7d34d-146">Færið inn **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="7d34d-147">Færið inn **Götuheiti**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="7d34d-148">Færið inn **Borg**, **Ríki** og **Sýsla**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="7d34d-149">Yfirleitt eru þessir reitir sjálfkrafa stilltir samkvæmt reitnum **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="7d34d-150">Einnig má velja reitinn **Aðal** til að gefa upp aðalaðsetur.</span><span class="sxs-lookup"><span data-stu-id="7d34d-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="7d34d-151">Aðeins er hægt að merkja eitt aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="7d34d-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="7d34d-152">Ef annað aðsetur er þegar merkt sem aðalaðsetur þarf að staðfesta að ætlunin sé að nota þetta aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="7d34d-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="7d34d-153">Það má velja reitinn **Einkamál** til að gefa til kynna að aðsetrið sé einkamál.</span><span class="sxs-lookup"><span data-stu-id="7d34d-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="7d34d-154">Aðeins notendur með sérstakar heimildir til að skoða upplýsingar um einkaaðsetur geta skoðað þetta aðsetur.</span><span class="sxs-lookup"><span data-stu-id="7d34d-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="7d34d-155">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="7d34d-156">Búa til breytingu á aðsetri fram í tímann</span><span class="sxs-lookup"><span data-stu-id="7d34d-156">Create a future change for an address</span></span>

<span data-ttu-id="7d34d-157">Í sumum tilfellum gæti verið gott að uppfæra aðsetur sem á að breytast seinna meir.</span><span class="sxs-lookup"><span data-stu-id="7d34d-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="7d34d-158">Til dæmis gæti þetta reynst gagnlegt ef starfsmaður ætlar að flytja þann fimmtánda næsta mánaðar.</span><span class="sxs-lookup"><span data-stu-id="7d34d-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="7d34d-159">Opnið síðuna **Stjórna aðsetrum** með því að velja **Fleiri valkostir > Ítarlegt** úr hvaða aðseturstöflu sem er.</span><span class="sxs-lookup"><span data-stu-id="7d34d-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="7d34d-160">Velja skal **Nýtt** til að búa til nýtt aðsetur.</span><span class="sxs-lookup"><span data-stu-id="7d34d-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="7d34d-161">Færið inn upplýsingar um aðsetrið.</span><span class="sxs-lookup"><span data-stu-id="7d34d-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="7d34d-162">Veljið flýtiflipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="7d34d-163">Í reitnum **Gildisdagsetning** skal velja dagsetninguna þegar nýja aðsetrið á að taka gildi.</span><span class="sxs-lookup"><span data-stu-id="7d34d-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="7d34d-164">Í reitnum **Lokadagsetning** má velja hvenær aðsetrið á ekki að gilda lengur.</span><span class="sxs-lookup"><span data-stu-id="7d34d-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="7d34d-165">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="7d34d-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="7d34d-166">Skoða og fylgjast með breytingum á aðsetri</span><span class="sxs-lookup"><span data-stu-id="7d34d-166">View and monitor address changes</span></span>

<span data-ttu-id="7d34d-167">Starfsmaður mannauðsmála getur skoðað og fylgst með breytingum á aðsetri á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="7d34d-168">Til að skoða breytingar á aðsetri skal opna reitinn **Starfsmannastjórnun** á síðunni **Heima**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="7d34d-169">Breytingar á aðsetri birtast í reit ofarlega í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="7d34d-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="7d34d-170">Talan fyrir ofan **Breytingar á aðsetri** sýnir hversu margar breytingar á aðsetri voru gerðar yfir tiltekinn dagafjölda á síðunni **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="7d34d-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="7d34d-171">Þegar reiturinn **Breytingar á aðsetri** er valinn, sýnir ný síða upplýsingarnar um allar breytingar á aðsetri.</span><span class="sxs-lookup"><span data-stu-id="7d34d-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="7d34d-172">Hægt er að velja **Hafa seinni tíma breytingar á aðsetri með** ofarlega í hægra horninu til að sýna breytingar á aðsetri með dagsetningu fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="7d34d-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="7d34d-173">Ef óskað er eftir að fá tilkynningu eða tölvupóst um þessar breytingar á aðsetri, er hægt að stofna nýja tilkynningarreglu í flipanum **Valkostir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="7d34d-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="7d34d-174">Frekari upplýsingar um tilkynningarreglur er að finna í [Stofna tilkynningarreglur](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts).</span><span class="sxs-lookup"><span data-stu-id="7d34d-174">For more information about alert rules, see [Create alert rules](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts).</span></span><br><br>

> <span data-ttu-id="7d34d-175">Ef ætlunin er að skilgreina verkflæði fyrir breytingar á aðsetri er hægt að velja valkostinn **Senda út á við** í tilkynningarreglunni og nota síðan Power Automate til að kveikja á viðskiptatilvikinu og skilgreina verkflæði.</span><span class="sxs-lookup"><span data-stu-id="7d34d-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="7d34d-176">Frekari upplýsingar er að finna í [Tilkynningar sem viðskiptatilvik](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events).</span><span class="sxs-lookup"><span data-stu-id="7d34d-176">For more information, see [Alerts as business events](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/create-alerts#alerts-as-business-events).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]