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
ms.openlocfilehash: 387caeee3ba44e1fbc661e2c31915b75dd80c31e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892130"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="c89b6-103">Skoða og vinna með aðsetursbreytingar</span><span class="sxs-lookup"><span data-stu-id="c89b6-103">View and manage address changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c89b6-104">Þetta efnisatriði útskýrir hvernig hægt er að skoða og hafa umsjón með breytingum á aðsetri á sjálfsafgreiðslusíðu starfsmanns **Breyta persónuupplýsingum** eða á upplýsingasíðunni **Starfsmaður** í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c89b6-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c89b6-105">Mörg fyrirtæki vilja að starfsmenn hafi umsjón með persónulegum upplýsingum sínum í gegnum sjálfsafgreiðsluumhverfið.</span><span class="sxs-lookup"><span data-stu-id="c89b6-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="c89b6-106">Hægt er að leyfa notendum að uppfæra aðsetur sitt á vinnusvæðinu **Sjálfsafgreiðsla starfsmanna**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="c89b6-107">Síðan er hægt að fylgjast með þessum breytingum á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="c89b6-108">Til að nota þennan eiginleika þarf að tilgreina dagafjöldann sem á að skoða breytingar fyrir á síðunni **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="c89b6-109">Skilgreina færibreytur fyrir breytingu á aðsetri</span><span class="sxs-lookup"><span data-stu-id="c89b6-109">Configure address change parameters</span></span>

<span data-ttu-id="c89b6-110">Til að skilgreina fjölda daga sem birta á breytingar á aðsetri fyrir á vinnusvæðinu **Starfsmannastjórnun**, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c89b6-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="c89b6-111">Á yfirlitssvæðinu skal velja **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="c89b6-112">Veljið **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-112">Select **Links**.</span></span>

3. <span data-ttu-id="c89b6-113">Veljið **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="c89b6-114">Í reitinn **Fjöldi daga** undir **Breytingar á aðsetri**, skal slá inn dagafjöldann sem birta á breytingar á aðsetri fyrir á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="c89b6-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c89b6-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="c89b6-116">Stofna eða breyta aðsetri starfsmanns</span><span class="sxs-lookup"><span data-stu-id="c89b6-116">Create or change an employee address</span></span>

<span data-ttu-id="c89b6-117">Starfsmenn geta uppfært eigið aðsetur á vinnusvæðinu **Sjálfsafgreiðsla starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="c89b6-118">Fylgið þessum skrefum til að stofna eða breyta aðsetri:</span><span class="sxs-lookup"><span data-stu-id="c89b6-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="c89b6-119">Veldu reitinn **Sjálfsafgreiðsla starfsmanns** á heimasíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="c89b6-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="c89b6-120">Veldu **Breyta persónulegum upplýsingum**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="c89b6-121">Til að bæta við aðsetri skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-121">To add an address, select **Add**.</span></span> <span data-ttu-id="c89b6-122">Til að uppfæra fyrirliggjandi aðsetur skal velja aðsetrið í listanum og velja svo **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="c89b6-123">Færið inn **Heiti eða lýsing**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="c89b6-124">Veljið fellilistann **Tilgangur** og veljið síðan gerð aðseturs.</span><span class="sxs-lookup"><span data-stu-id="c89b6-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="c89b6-125">Færið inn **Land/svæði**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="c89b6-126">Færið inn **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="c89b6-127">Færið inn **Götuheiti**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="c89b6-128">Færið inn **Borg**, **Ríki** og **Sýsla**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="c89b6-129">Yfirleitt eru þessir reitir sjálfkrafa stilltir samkvæmt reitnum **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="c89b6-130">Einnig má velja reitinn **Aðal** til að gefa upp aðalaðsetur.</span><span class="sxs-lookup"><span data-stu-id="c89b6-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="c89b6-131">Aðeins er hægt að merkja eitt aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="c89b6-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="c89b6-132">Ef annað aðsetur er þegar merkt sem aðalaðsetur þarf að staðfesta að ætlunin sé að nota þetta aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="c89b6-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="c89b6-133">Það má velja reitinn **Einkamál** til að gefa til kynna að aðsetrið sé einkamál.</span><span class="sxs-lookup"><span data-stu-id="c89b6-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="c89b6-134">Aðeins notendur með sérstakar heimildir til að skoða upplýsingar um einkaaðsetur geta skoðað þetta aðsetur.</span><span class="sxs-lookup"><span data-stu-id="c89b6-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="c89b6-135">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="c89b6-136">Búa til eða breyta aðsetri starfsmanns</span><span class="sxs-lookup"><span data-stu-id="c89b6-136">Create or change a worker address</span></span>

<span data-ttu-id="c89b6-137">Hægt er að uppfæra aðsetur á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="c89b6-138">Fylgið þessum skrefum til að stofna eða breyta aðsetri:</span><span class="sxs-lookup"><span data-stu-id="c89b6-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="c89b6-139">Á vinnusvæðinu **Starfsmannastjórnun** skal velja **Tenglar** og síðan velja **Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="c89b6-140">Veljið starfsmanninn og því næst **Aðsetur**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="c89b6-141">Til að bæta við aðsetri skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-141">To add an address, select **Add**.</span></span> <span data-ttu-id="c89b6-142">Til að uppfæra fyrirliggjandi aðsetur skal velja aðsetrið í listanum og velja svo **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="c89b6-143">Færið inn **Heiti eða lýsing**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="c89b6-144">Veljið fellilistann **Tilgangur** og veljið síðan gerð aðseturs.</span><span class="sxs-lookup"><span data-stu-id="c89b6-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="c89b6-145">Færið inn **Land/svæði**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="c89b6-146">Færið inn **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="c89b6-147">Færið inn **Götuheiti**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="c89b6-148">Færið inn **Borg**, **Ríki** og **Sýsla**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="c89b6-149">Yfirleitt eru þessir reitir sjálfkrafa stilltir samkvæmt reitnum **Póstnúmer**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="c89b6-150">Einnig má velja reitinn **Aðal** til að gefa upp aðalaðsetur.</span><span class="sxs-lookup"><span data-stu-id="c89b6-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="c89b6-151">Aðeins er hægt að merkja eitt aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="c89b6-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="c89b6-152">Ef annað aðsetur er þegar merkt sem aðalaðsetur þarf að staðfesta að ætlunin sé að nota þetta aðsetur sem aðal.</span><span class="sxs-lookup"><span data-stu-id="c89b6-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="c89b6-153">Það má velja reitinn **Einkamál** til að gefa til kynna að aðsetrið sé einkamál.</span><span class="sxs-lookup"><span data-stu-id="c89b6-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="c89b6-154">Aðeins notendur með sérstakar heimildir til að skoða upplýsingar um einkaaðsetur geta skoðað þetta aðsetur.</span><span class="sxs-lookup"><span data-stu-id="c89b6-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="c89b6-155">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="c89b6-156">Búa til breytingu á aðsetri fram í tímann</span><span class="sxs-lookup"><span data-stu-id="c89b6-156">Create a future change for an address</span></span>

<span data-ttu-id="c89b6-157">Í sumum tilfellum gæti verið gott að uppfæra aðsetur sem á að breytast seinna meir.</span><span class="sxs-lookup"><span data-stu-id="c89b6-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="c89b6-158">Til dæmis gæti þetta reynst gagnlegt ef starfsmaður ætlar að flytja þann fimmtánda næsta mánaðar.</span><span class="sxs-lookup"><span data-stu-id="c89b6-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="c89b6-159">Opnið síðuna **Stjórna aðsetrum** með því að velja **Fleiri valkostir > Ítarlegt** úr hvaða aðseturstöflu sem er.</span><span class="sxs-lookup"><span data-stu-id="c89b6-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="c89b6-160">Velja skal **Nýtt** til að búa til nýtt aðsetur.</span><span class="sxs-lookup"><span data-stu-id="c89b6-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="c89b6-161">Færið inn upplýsingar um aðsetrið.</span><span class="sxs-lookup"><span data-stu-id="c89b6-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="c89b6-162">Veljið flýtiflipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="c89b6-163">Í reitnum **Gildisdagsetning** skal velja dagsetninguna þegar nýja aðsetrið á að taka gildi.</span><span class="sxs-lookup"><span data-stu-id="c89b6-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="c89b6-164">Í reitnum **Lokadagsetning** má velja hvenær aðsetrið á ekki að gilda lengur.</span><span class="sxs-lookup"><span data-stu-id="c89b6-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="c89b6-165">Lokaðu síðunum.</span><span class="sxs-lookup"><span data-stu-id="c89b6-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="c89b6-166">Skoða og fylgjast með breytingum á aðsetri</span><span class="sxs-lookup"><span data-stu-id="c89b6-166">View and monitor address changes</span></span>

<span data-ttu-id="c89b6-167">Starfsmaður mannauðsmála getur skoðað og fylgst með breytingum á aðsetri á vinnusvæðinu **Starfsmannastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="c89b6-168">Til að skoða breytingar á aðsetri skal opna reitinn **Starfsmannastjórnun** á síðunni **Heima**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="c89b6-169">Breytingar á aðsetri birtast í reit ofarlega í hægra horninu.</span><span class="sxs-lookup"><span data-stu-id="c89b6-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="c89b6-170">Talan fyrir ofan **Breytingar á aðsetri** sýnir hversu margar breytingar á aðsetri voru gerðar yfir tiltekinn dagafjölda á síðunni **Færibreytur mannauðs**.</span><span class="sxs-lookup"><span data-stu-id="c89b6-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="c89b6-171">Þegar reiturinn **Breytingar á aðsetri** er valinn, sýnir ný síða upplýsingarnar um allar breytingar á aðsetri.</span><span class="sxs-lookup"><span data-stu-id="c89b6-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="c89b6-172">Hægt er að velja **Hafa seinni tíma breytingar á aðsetri með** ofarlega í hægra horninu til að sýna breytingar á aðsetri með dagsetningu fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="c89b6-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="c89b6-173">Ef óskað er eftir að fá tilkynningu eða tölvupóst um þessar breytingar á aðsetri, er hægt að stofna nýja tilkynningarreglu í flipanum **Valkostir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c89b6-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="c89b6-174">Frekari upplýsingar um tilkynningarreglur er að finna í [Stofna tilkynningarreglur](../fin-ops-core/fin-ops/get-started/create-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="c89b6-174">For more information about alert rules, see [Create alert rules](../fin-ops-core/fin-ops/get-started/create-alerts.md).</span></span><br><br>

> <span data-ttu-id="c89b6-175">Ef ætlunin er að skilgreina verkflæði fyrir breytingar á aðsetri er hægt að velja valkostinn **Senda út á við** í tilkynningarreglunni og nota síðan Power Automate til að kveikja á viðskiptatilvikinu og skilgreina verkflæði.</span><span class="sxs-lookup"><span data-stu-id="c89b6-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="c89b6-176">Frekari upplýsingar er að finna í [Tilkynningar sem viðskiptatilvik](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).</span><span class="sxs-lookup"><span data-stu-id="c89b6-176">For more information, see [Alerts as business events](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]