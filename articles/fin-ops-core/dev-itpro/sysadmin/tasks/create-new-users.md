---
title: Nýir notendur stofnaðir
description: Notendur eru innri starfsmenn fyrirtækisins, eða ytri viðskiptavinir og lánardrottnar sem þurfa aðgang að kerfinu til að framkvæma vinnslum.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d3f1fba05d944e78e4595018d190c3dc41e076
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907912"
---
# <a name="create-new-users"></a><span data-ttu-id="e8f84-103">Búa til nýja notendur</span><span class="sxs-lookup"><span data-stu-id="e8f84-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8f84-104">Áður en hægt er opna Finance and Operations-forrit þarf fyrst að bæta notanda við síðuna **Notendur** (**Kerfisstjórnun \> Notendur \> Notendur**).</span><span class="sxs-lookup"><span data-stu-id="e8f84-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="e8f84-105">Notendur samanstanda af innri starfsmönnum fyrirtækisins eða ytri viðskiptavinum og lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="e8f84-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="e8f84-106">Hægt er að flytja notendur inn eða bæta þeim við handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e8f84-106">Users can be imported or added manually.</span></span> <span data-ttu-id="e8f84-107">Allir notendur verða að vera með tilskilinn leyfi fyrir tilhlýðilega notkun.</span><span class="sxs-lookup"><span data-stu-id="e8f84-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="e8f84-108">Upplýsingar um hvernig á að kaupa og veita leyfi fyrir Finance and Operations-forrit er að finna í [Leyfishandbók Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="e8f84-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="e8f84-109">Úthluta leyfi til notanda</span><span class="sxs-lookup"><span data-stu-id="e8f84-109">Assign a license to a user</span></span>
<span data-ttu-id="e8f84-110">Kerfisstjórar geta það [úthluta leyfi til notenda](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) í [stjórnunarmiðstöð Microsoft 365](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="e8f84-110">System admins can [assign licenses to users](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="e8f84-111">Bæta ytri notanda við Azure AD og úthluta leyfi</span><span class="sxs-lookup"><span data-stu-id="e8f84-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="e8f84-112">Ytri notendur verða að koma fram í notendaskrá biðlara (Azure Active Directory (Azure AD)) þannig að hægt sé að úthluta þeim leyfum.</span><span class="sxs-lookup"><span data-stu-id="e8f84-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="e8f84-113">Þessum utanaðkomandi notendum ætti að bæta við leigjandann í Azure AD sem gestanotendum og úthluta þeim síðan viðeigandi leyfum.</span><span class="sxs-lookup"><span data-stu-id="e8f84-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="e8f84-114">Krafa Finance and Operations-forrita er að fyrirtæki gestanotenda verði að nota Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e8f84-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="e8f84-115">Nánari upplýsingar er að finna í [Bæta Azure Active Directory B2B samvinnunotendum við í Azure-gáttinni](/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="e8f84-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="e8f84-116">Flytja inn nýja notendur úr Azure AD</span><span class="sxs-lookup"><span data-stu-id="e8f84-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="e8f84-117">Farið í **Kerfisstjórnun** \> **Notandi** \> **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="e8f84-118">Á Aðgerðasvæðinu skal velja **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="e8f84-119">Veljið notendurnar sem á að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="e8f84-119">Select the users to be imported.</span></span> <span data-ttu-id="e8f84-120">Listinn inniheldur Azure AD notendur sem eru ekki notendur í þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="e8f84-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="e8f84-121">Veldu **Flytja inn notendur**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-121">Select **Import users**.</span></span>
5. <span data-ttu-id="e8f84-122">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f84-123">Gildið fyrir reitinn **Fyrirtæki** verður stillt samkvæmt núverandi lotufyrirtæki fyrir stjórnandann. Eftir innflutning þarf að úthluta hlutverkum og fyrirtækjum eins og við á.</span><span class="sxs-lookup"><span data-stu-id="e8f84-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="e8f84-124">Nánari upplýsingar er að finna á [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e8f84-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="e8f84-125">Einnig gæti verið nauðsynlegt að tengja notandann við **Einstakling** og uppfæra valkosti notanda, t.d. tungumál.</span><span class="sxs-lookup"><span data-stu-id="e8f84-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="e8f84-126">Bæta við nýjum notanda handvirkt</span><span class="sxs-lookup"><span data-stu-id="e8f84-126">Manually add a new user</span></span>
1. <span data-ttu-id="e8f84-127">Farið í **Kerfisstjórnun** \> **Notendur** \> **Notendur**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="e8f84-128">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="e8f84-129">Í reitnum **Notandakenni** er fært inn einkvæmt kenni fyrir notandann.</span><span class="sxs-lookup"><span data-stu-id="e8f84-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="e8f84-130">Í reitnum **Notandanafn** skal færa inn notandaheiti.</span><span class="sxs-lookup"><span data-stu-id="e8f84-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="e8f84-131">Í reitnum **Veita**:</span><span class="sxs-lookup"><span data-stu-id="e8f84-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="e8f84-132">Fyrir innri notendur skal nota sjálfgefið gildi.</span><span class="sxs-lookup"><span data-stu-id="e8f84-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="e8f84-133">Til dæmis er Azure AD-leigjandanum gefið forskeytið https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="e8f84-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="e8f84-134">Fyrir aðra en Azure AD-notendur, t.d. Service-2-Service-reikningar, skal færa inn einfalt textagildi.</span><span class="sxs-lookup"><span data-stu-id="e8f84-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="e8f84-135">Til dæmis, NA.</span><span class="sxs-lookup"><span data-stu-id="e8f84-135">For example, NA.</span></span> <span data-ttu-id="e8f84-136">Þetta gildi hjálpar til við að forðast rangar sannvottunarhringingar sem gætu skilað sér í villum ef gilt gildi fyrir auðkenni veitu er notað.</span><span class="sxs-lookup"><span data-stu-id="e8f84-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="e8f84-137">Fyrir ytri notendur eða gestanotendur skal bæta við heiti Azure AD-biðlarans á eftir https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="e8f84-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="e8f84-138">Í reitinn **Tölvupóstur** skal færa inn fullt heiti netfangs notanda/aðalheiti notanda.</span><span class="sxs-lookup"><span data-stu-id="e8f84-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="e8f84-139">Í reitnum **Fyrirtæki** skal velja sjálfgefið ræsingarfyrirtæki fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="e8f84-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="e8f84-140">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-140">Select **Save**.</span></span>

<span data-ttu-id="e8f84-141">Gildin fyrir kenni veitu og fjarmælingarkenni verða uppfærð samkvæmt kalli [Microsoft Graph](/graph/overview) þegar skrá notanda er vistuð.</span><span class="sxs-lookup"><span data-stu-id="e8f84-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="e8f84-142">Fjarmælingarkennið byggir á hlutarkenni/öryggiskenni notanda í Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e8f84-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f84-143">Eftir að notanda hefur verið bætt við þarf að úthluta hlutverkum og fyrirtækjum eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="e8f84-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="e8f84-144">Nánari upplýsingar er að finna á [Úthluta notendum á öryggishlutverk](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e8f84-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="e8f84-145">Einnig gæti verið nauðsynlegt að tengja notandann við **Einstakling** og uppfæra **Notandavalkosti**, t.d. tungumál.</span><span class="sxs-lookup"><span data-stu-id="e8f84-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="e8f84-146">Breyta notandakenni</span><span class="sxs-lookup"><span data-stu-id="e8f84-146">Change a user ID</span></span>
<span data-ttu-id="e8f84-147">Til að breyta notandakenni þarf að endurnefna lykilinn í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="e8f84-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="e8f84-148">Þegar notandakenni er breytt með því að nota þetta ferli er öllum tengdum notandastillingum breytt til að nota nýja notandakennið.</span><span class="sxs-lookup"><span data-stu-id="e8f84-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="e8f84-149">Til dæmis eru notkunarupplýsingar í töflunni **SysLastValue** uppfærðar til að vísa til nýja notandakennið.</span><span class="sxs-lookup"><span data-stu-id="e8f84-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="e8f84-150">Notandakennið er aðallykill töflunnar fyrir notandaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e8f84-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="e8f84-151">Það getur tekið sinn tíma að endurnefna aðallykilinn fyrir núverandi notendur vegna þess að allar tilvísanir í lykilinn eru einnig uppfærðar í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="e8f84-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="e8f84-152">Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="e8f84-153">Veljið notanda úr listanum og veljið **Valmöguleikar\> Færsluupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="e8f84-154">Velja **Endurnefna**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-154">Select **Rename**.</span></span>
4. <span data-ttu-id="e8f84-155">Færa skal inn nýtt einkvæmt gildi fyrir notandakennið og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e8f84-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="e8f84-156">Veljið **Já** til að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="e8f84-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8f84-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e8f84-157">Additional resources</span></span>

<span data-ttu-id="e8f84-158">Frekari möguleikar til að innleiða B2B-notendur er að finna í [Flytja út B2B-notendur í Azure AD](../implement-b2b.md).</span><span class="sxs-lookup"><span data-stu-id="e8f84-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="e8f84-159">Frekari upplýsingar um forstillta kerfisreikninga er að finna í [Forstilltir kerfisreikningar](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="e8f84-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]