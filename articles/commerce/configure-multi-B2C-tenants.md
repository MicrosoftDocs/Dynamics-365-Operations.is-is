---
title: Stilla marga B2C leigjendur í viðskiptaumhverfi
description: Þetta efni lýsir því hvenær og hvernig á að setja upp margar á rás Microsoft Azure Active Directory (Azure AD) viðskipti til neytenda (B2C) leigjendur fyrir auðkenningu notenda í sérhæfðu umhverfi Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ddc8cea42ab0b5a319d4725ce8c75e57529cc63
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477757"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="8fdc5-103">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="8fdc5-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8fdc5-104">Þetta efni lýsir því hvenær og hvernig á að setja upp margar á rás Microsoft Azure Active Directory (Azure AD) viðskipti til neytenda (B2C) leigjendur fyrir auðkenningu notenda í sérhæfðu umhverfi Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="8fdc5-105">Dynamics 365 Commerce notar Azure AD B2C skýjaeiningarþjónusta til að styðja skilríki notenda og auðkenningarflæði.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="8fdc5-106">Notendur geta notað auðkenningarflæðin til að skrá sig, skrá sig inn og endurstilla lykilorð sitt.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="8fdc5-107">Azure AD B2C geymir viðkvæmar sannvottunarupplýsingar notanda, svo sem notandanafn og lykilorð.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-107">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="8fdc5-108">Notendaskráin er einstök fyrir hvern B2C leigjanda og hún notar annað hvort notendanafn (netfang) eða persónuskilríki.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="8fdc5-109">Í flestum tilvikum einn Azure AD B2C leigjandi er notaður í viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="8fdc5-110">Viðskiptavinir geta síðan búið til og birt margar síður í sama viðskiptaumhverfi og sömu persónuskilríki viðskiptavina verða notuð á þessum vefsvæðum.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="8fdc5-111">Ef hins vegar ætti að meðhöndla vefsvæðin í umhverfinu sem mismunandi tegundir og birtast notendum sem aðskild fyrirtæki, er hægt að stilla B2C leigjanda fyrir rásina sem er notuð við aðskilnað vefsins/vörumerkisins.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="8fdc5-112">Til athugunar þegar margir B2C leigjendur eru settir upp á hverja rás</span><span class="sxs-lookup"><span data-stu-id="8fdc5-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="8fdc5-113">Oft, þegar hver rás eða síða er meðhöndluð sem sérstök viðskipti, er besti kosturinn varðandi auðkenningu notenda í viðskiptum að nota aðskilda lögaðila.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="8fdc5-114">Hins vegar, ef þú vilt halda hverri rás/vefsvæði í sama umhverfi og lögaðilum, en vilt hafa sérstaka auðkenningu notenda fyrir hverja síðu, þá er það mikilvægt að þú lítur á eftirfarandi atriði áður en þú heldur áfram:</span><span class="sxs-lookup"><span data-stu-id="8fdc5-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="8fdc5-115">Notendur munu hafa sín sérstöku persónuskilríki fyrir hverja rás/vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="8fdc5-116">Sami einstaklingur getur haft tvo aðskilda reikninga á hverri rás/vefsvæði, vegna þess að hver reikningur verður einstök færsla í sérstakan B2C leigjanda.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="8fdc5-117">Í umhverfi Microsoft Dynamics verður aðskildum viðskiptamannaskrám skilað fyrir altæka skráaleit.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="8fdc5-118">Ef notandi notar sama netfang á rásir/vefsvæði mun altæk leit viðskiptavina skila niðurstöðum fyrir hverja rás/síðu.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="8fdc5-119">(Rásavísir verður sýndur.)</span><span class="sxs-lookup"><span data-stu-id="8fdc5-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="8fdc5-120">Hægt er að nota veffangaskrána til að hjálpa hópnotendum, svo hægt sé að rekja þá á hverri rás.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="8fdc5-121">Fjöldi skráningar viðskiptavina á hverja rás gæti aukist og þessi aukning gæti haft áhrif á árangur altækrar leitar viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="8fdc5-122">Leigja verður B2C leigjendur að rás til að koma í veg fyrir aðstæður þar sem viðskiptavinir skrá sig í rangan leigjanda.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="8fdc5-123">Annars geta rugl eða rekja vandamál komið upp.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="8fdc5-124">Eftirfarandi mynd sýnir marga B2C leigjendur í viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Margir B2C leigjendur í viðskiptaumhverfi](media/MultiB2C_In_Environment.png)

<span data-ttu-id="8fdc5-126">Ef þú ákveður að fyrirtæki þitt þurfi sérstaka B2C leigjendur á hverja rás í sama viðskiptaumhverfi skaltu ljúka verklagsreglunum í eftirfarandi hlutum til að biðja um þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="8fdc5-127">Biðja um að B2C á hverja rás verði virkt í umhverfi þínu</span><span class="sxs-lookup"><span data-stu-id="8fdc5-127">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="8fdc5-128">Eins og er, ef þú vilt að sérstakir B2C leigjendur á hvern rás séu tiltækir í sama viðskiptaumhverfi, verður þú að leggja fram beiðni til Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-128">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="8fdc5-129">Fyrir frekari upplýsingar, sjá [Fáðu stuðning við Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), eða ræddu þetta mál með tengiliðnum þínum um viðskiptalausnir.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-129">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="8fdc5-130">Stilla B2C leigjendur í umhverfi þínu</span><span class="sxs-lookup"><span data-stu-id="8fdc5-130">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="8fdc5-131">Til að stilla B2C leigjendur í umhverfi þínu skaltu ljúka viðeigandi verklagsreglum í þessum kafla.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-131">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="8fdc5-132">Bættu við Azure AD B2C leigjanda</span><span class="sxs-lookup"><span data-stu-id="8fdc5-132">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="8fdc5-133">Til að bæta við Azure AD B2C leigjanda að umhverfi þínu, fylgdu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-133">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="8fdc5-134">Skráðu þig inn í vefsvæði byggingaraðila fyrir umhverfi þitt sem kerfisstjóri. Til að stilla Azure AD B2C leigjendur, þú verður að vera kerfisstjóri fyrir viðskiptaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-134">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="8fdc5-135">Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-135">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="8fdc5-136">Smellið á **B2C-stillingar** og veljið síðan **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-136">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="8fdc5-137">Velja skal **Bæta við B2C-forriti** og færið síðan inn eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="8fdc5-137">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="8fdc5-138">**Heiti umsóknar**: Sláðu inn nafnið sem ætti að nota fyrir forritið í tengslum við stjórnun þess í verslun.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-138">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="8fdc5-139">Við mælum með að þú notir heiti forritsins sem þú valdir þegar þú settir upp Azure AD B2C forrit í Azure vefsíðunni.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-139">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="8fdc5-140">Á þennan hátt getur þú hjálpað til við að draga úr rugli þegar þú stjórnar B2C leigjendum í verslun.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-140">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="8fdc5-141">**Nafn leigjanda**: Sláðu inn B2C leigjanda nafn eins og það birtist í Azure vefsíðunni.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-141">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="8fdc5-142">**Gleymdu auðkenni lykilorðsstefnu**: Sláðu inn stefnuskilríkið (nafn stefnunnar á Azure vefsíðunni).</span><span class="sxs-lookup"><span data-stu-id="8fdc5-142">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="8fdc5-143">**Reglukenni skráningar og innskráningar**: Sláðu inn stefnuskilríkið (nafn stefnunnar á Azure vefsíðunni).</span><span class="sxs-lookup"><span data-stu-id="8fdc5-143">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="8fdc5-144">**GUID biðlara**: Sláðu inn Azure AD B2C leigjandaauðkenni eins og það birtist í Azure vefsíðunni (ekki forritsauðkenni B2C leigjanda).</span><span class="sxs-lookup"><span data-stu-id="8fdc5-144">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="8fdc5-145">**Breyta auðkenni forstillingarreglu**: Sláðu inn stefnuskilríkið (nafn stefnunnar á Azure vefsíðunni).</span><span class="sxs-lookup"><span data-stu-id="8fdc5-145">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="8fdc5-146">Þegar þú hefur lokið við að slá inn þessar upplýsingar skaltu velja **Í lagi** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-146">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="8fdc5-147">Þú ættir að hafa reiti eins og **Umfang**, **Ógagnvirk reglukenni**, **Ógagnvirk biðlarakenni**, **Sérstillt lén innskráninga** og **Reglukenni skráningar** auða nema teymi Dynamics 365 Commerce leiðbeini þér að stilla þá.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-147">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="8fdc5-148">Nýi Azure AD B2C-leigjandinn ætti nú að birtast á listanum undir **Stjórna B2C forritum**.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-148">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="8fdc5-149">Hafa umsjón með eða eyða Azure AD B2C-leigjanda</span><span class="sxs-lookup"><span data-stu-id="8fdc5-149">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="8fdc5-150">Skráðu þig inn í vefsvæði byggingaraðila fyrir umhverfi þitt sem kerfisstjóri. Til að stilla Azure AD B2C leigjendur, þú verður að vera kerfisstjóri fyrir viðskiptaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-150">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="8fdc5-151">Í vinstri yfirlitsglugganum velurðu **Leigjandastillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-151">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="8fdc5-152">Smellið á **B2C-stillingar** og veljið síðan **Stjórna**.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-152">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="8fdc5-153">Veldu blýantstáknið við hliðina til að breyta B2C leigjanda.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-153">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="8fdc5-154">Til að eyða B2C leigjanda skaltu velja ruslatunnutáknið við hliðina.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-154">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="8fdc5-155">Veldu **Vista** og veldu síðan **Birta** til að virkja breytingarnar þínar.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-155">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="8fdc5-156">Þegar leigjandi B2C er stilltur fyrir lifandi/birta síðu gætu notendur skráð sig með því að nota reikninga sem eru til staðar á leigjandanum.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-156">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="8fdc5-157">Ef þú eyðir stillta leigjanda í valmyndinni **Leigjanda stillingar \> B2C leigjandi**, fjarlægir þú félag þess B2C leigjanda frá vefsvæðum sem tengjast einhverjum farvegi leigjanda.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-157">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="8fdc5-158">Í þessu tilfelli gætu notendur þínir ekki lengur getað skráð sig inn á reikninga sína.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-158">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="8fdc5-159">Því skal gæta fyllstu varúðar þegar þú eyðir stilltum leigjanda.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-159">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="8fdc5-160">Þegar uppsettum leigjanda er eytt verður B2C leigjanda og gögnum haldið áfram, en viðskiptakerfisstillingu viðkomandi leigjanda verður breytt eða fjarlægt.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-160">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="8fdc5-161">Notendur sem reyna að skrá sig eða skrá sig inn á vefinn munu búa til nýja reikningsskrá í sjálfgefna eða nýlega tengda B2C leigjanda sem er stilltur fyrir rás vefsins.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-161">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="8fdc5-162">Stilla rásina þína með B2C leigjanda</span><span class="sxs-lookup"><span data-stu-id="8fdc5-162">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="8fdc5-163">Skráðu þig inn í vefsvæði byggingaraðila fyrir umhverfi þitt sem kerfisstjóri. Til að stilla Azure AD B2C leigjendur, þú verður að vera kerfisstjóri fyrir viðskiptaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-163">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="8fdc5-164">Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-164">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="8fdc5-165">Veldu **Rásir** og veldu síðan rásina sem á að stilla.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-165">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="8fdc5-166">Í eignarrúðunni til hægri, í reitnum **Velja B2C forrit**, veldu stillan Azure AD B2C leigjandi til að nota fyrir þessa rás.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-166">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="8fdc5-167">Veldu á skipanastikunni **Vista og birta** til að festa nýja eða uppfærða stillingu.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-167">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="8fdc5-168">Ef þú breytir B2C forritinu sem er úthlutað á rásina fjarlægir þú núverandi tilvísanir sem hafa verið settar upp fyrir alla notendur sem þegar hafa skráð sig í umhverfið.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-168">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="8fdc5-169">Í þessu tilfelli eru öll skilríki sem eru tengd B2C forritinu sem nú er úthlutað ekki tiltæk fyrir notendur.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-169">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="8fdc5-170">Þess vegna skaltu breyta rás Azure AD B2C stillingar aðeins ef þú ert að setja upp rásina í fyrsta skipti og engir notendur hafa getað skráð sig.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-170">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="8fdc5-171">Annars gætu notendur þurft að skrá sig aftur til að koma upp met í nýju Azure AD B2C leigjandi.</span><span class="sxs-lookup"><span data-stu-id="8fdc5-171">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="8fdc5-172">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8fdc5-172">Additional resources</span></span>

[<span data-ttu-id="8fdc5-173">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="8fdc5-173">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8fdc5-174">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="8fdc5-174">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8fdc5-175">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="8fdc5-175">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8fdc5-176">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="8fdc5-176">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8fdc5-177">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="8fdc5-177">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8fdc5-178">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="8fdc5-178">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8fdc5-179">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="8fdc5-179">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8fdc5-180">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="8fdc5-180">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="8fdc5-181">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="8fdc5-181">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8fdc5-182">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="8fdc5-182">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
