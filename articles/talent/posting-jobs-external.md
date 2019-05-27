---
title: Auglýsa störf á utanaðkomandi ráðningarsíðum úr Attract
description: Þetta efnisatriði útskýrir hvernig á að nota Dynamics 365 for Talent - Attract til að auglýsa störf á utanaðkomandi ráðningarsíðum
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518281"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="bf993-103">Auglýsa störf á utanaðkomandi ráðningarsíðum úr Attract</span><span class="sxs-lookup"><span data-stu-id="bf993-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf993-104">Þú vilt að sem flestir hæfir umsækjendur sjái lausu stöðurnar þínar.</span><span class="sxs-lookup"><span data-stu-id="bf993-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="bf993-105">Ráðningarsíður á borð við Broadbean auðvelda þér að ná þessu markmiði.</span><span class="sxs-lookup"><span data-stu-id="bf993-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="bf993-106">Microsoft Dynamics 365 Talent: Attract gerir þér nú kleift að auglýsa störf á Broadbean og Microsoft er stöðugt að bjóða upp á nýjar leiðir í þessum efnum.</span><span class="sxs-lookup"><span data-stu-id="bf993-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="bf993-107">Auglýsa störf á Broadbean</span><span class="sxs-lookup"><span data-stu-id="bf993-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="bf993-108">Áður en þú getur auglýst störf á Broadbean þarf fyrst að stilla Broadbean-samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="bf993-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="bf993-109">Til að auglýsa störf á utanaðkomandi síðum verður þú að hafa [Viðbót við alhliða ráðningar](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="bf993-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="bf993-110">Þessi eiginleiki er í forútgáfu sem stendur.</span><span class="sxs-lookup"><span data-stu-id="bf993-110">This feature is currently in preview.</span></span> <span data-ttu-id="bf993-111">Ef þú vilt prófa hann verður þú að [kveikja á honum í stjórnandastillingum Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="bf993-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="bf993-112">Skilgreina Broadbean-samþættingu</span><span class="sxs-lookup"><span data-stu-id="bf993-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="bf993-113">Skráðu þig inn í Attract sem stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="bf993-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="bf993-114">Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Stjórnandamiðstöð**.</span><span class="sxs-lookup"><span data-stu-id="bf993-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="bf993-115">Í flipanum **Stillingar atvinnutorgs**, í hlutanum **Virkja Broadbean-samþættingu** skal kveikja á samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="bf993-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="bf993-116">Hafðu samband við Broadbean og færðu inn upplýsingarnar í **Notandanafn, auðkenni notanda, dulritunarlykill**.</span><span class="sxs-lookup"><span data-stu-id="bf993-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="bf993-117">Broadbean-aðgangsupplýsingarnar þínar eru viðkvæmar og trúnaðarmál.</span><span class="sxs-lookup"><span data-stu-id="bf993-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="bf993-118">Þar af leiðandi skaltu geyma og deila þeim af varkárni.</span><span class="sxs-lookup"><span data-stu-id="bf993-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="bf993-119">Hver sá sem gegnir stjórnandahlutverki í Attract getur skoðað þessar aðgangsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="bf993-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="bf993-120">Microsoft og Attract taka engan þátt í að búa til og viðhalda þessum gildum.</span><span class="sxs-lookup"><span data-stu-id="bf993-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="bf993-121">Það er á þína ábyrgð að halda þeim uppfærðum í Attract og vinna með Broadbean til að leysa úr öllum vandamálum sem hafa með aðgangsupplýsingarnar þínar að gera.</span><span class="sxs-lookup"><span data-stu-id="bf993-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="bf993-122">Auglýsa starf á Broadbean</span><span class="sxs-lookup"><span data-stu-id="bf993-122">Post a job to Broadbean</span></span>

<span data-ttu-id="bf993-123">Eftir að kveikt hefur verið á Broadbean geta ráðningaraðilar og stjórnendur birt störf þar.</span><span class="sxs-lookup"><span data-stu-id="bf993-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="bf993-124">Þú verður að hafa umsóknarvefslóð fyrir starfið.</span><span class="sxs-lookup"><span data-stu-id="bf993-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="bf993-125">Í Attract, opnaðu starfið sem þú vilt auglýsa á Broadbean.</span><span class="sxs-lookup"><span data-stu-id="bf993-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="bf993-126">Í hlutanum **Birtingar** skal velja hnappinn **Birta núna** sem á við um Broadbean.</span><span class="sxs-lookup"><span data-stu-id="bf993-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="bf993-127">Fylgdu leiðbeiningunum í Broadbean-glugganum.</span><span class="sxs-lookup"><span data-stu-id="bf993-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="bf993-128">Attract sendir eftirfarandi upplýsingar til Broadbean:</span><span class="sxs-lookup"><span data-stu-id="bf993-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="bf993-129">Beiðnikenni</span><span class="sxs-lookup"><span data-stu-id="bf993-129">Request ID</span></span>
- <span data-ttu-id="bf993-130">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="bf993-130">Job title</span></span>
- <span data-ttu-id="bf993-131">Lýsing vinnslu</span><span class="sxs-lookup"><span data-stu-id="bf993-131">Job description</span></span>
- <span data-ttu-id="bf993-132">Staðsetning starfs</span><span class="sxs-lookup"><span data-stu-id="bf993-132">Job location</span></span>
- <span data-ttu-id="bf993-133">Sækja um vefslóðin</span><span class="sxs-lookup"><span data-stu-id="bf993-133">Apply URL</span></span>
- <span data-ttu-id="bf993-134">Upplýsingar um ráðningaraðila</span><span class="sxs-lookup"><span data-stu-id="bf993-134">Recruiter information</span></span>

<span data-ttu-id="bf993-135">Eftir að Broadbean lýkur við birtinguna sýnir hlutinn **Birtingar** fyrir starfið í Attract stöðuna á Broadbean sem **Birt**.</span><span class="sxs-lookup"><span data-stu-id="bf993-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="bf993-136">Broadbean þarf á reitnum **Atvinnugrein** að halda.</span><span class="sxs-lookup"><span data-stu-id="bf993-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="bf993-137">Sem stendur er þessi reitur sjálfkrafa stilltur á **Upplýsingatækni**.</span><span class="sxs-lookup"><span data-stu-id="bf993-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="bf993-138">Hins vegar er hægt að breyta gildinu í rétta atvinnugrein í glugganum fyrir birtingar á störfum í Broadbean.</span><span class="sxs-lookup"><span data-stu-id="bf993-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="bf993-139">Það tekur smá tíma fyrir Broadbean að birta starfið þitt á öllum atvinnutorgum sem þú hefur valið.</span><span class="sxs-lookup"><span data-stu-id="bf993-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="bf993-140">Því kunna að vera smá tafir áður en Attract birtir uppfærslu á stöðu fyrir starfið.</span><span class="sxs-lookup"><span data-stu-id="bf993-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="bf993-141">Skoða auglýst starf á Broadbean</span><span class="sxs-lookup"><span data-stu-id="bf993-141">View a Broadbean job posting</span></span>

<span data-ttu-id="bf993-142">Eftir að starf er auglýst á Broadbean er hægt að skoða það í Attract.</span><span class="sxs-lookup"><span data-stu-id="bf993-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="bf993-143">Opnaðu starfið í Attract sem þú vilt skoða á Broadbean.</span><span class="sxs-lookup"><span data-stu-id="bf993-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="bf993-144">Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="bf993-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="bf993-145">Starfsauglýsingin í Broadbean birtist í nýjum glugga.</span><span class="sxs-lookup"><span data-stu-id="bf993-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="bf993-146">Uppfæra starfsauglýsingu í Broadbean</span><span class="sxs-lookup"><span data-stu-id="bf993-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="bf993-147">Hægt er að uppfæra starfsauglýsingu í Broadbean á tvenna vegu.</span><span class="sxs-lookup"><span data-stu-id="bf993-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="bf993-148">Opnaðu starfið í Attract sem þú vilt uppfæra.</span><span class="sxs-lookup"><span data-stu-id="bf993-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="bf993-149">Í hlutanum **Birtingar** skal velja hnappinn **Uppfæra auglýsingu** sem á við um Broadbean.</span><span class="sxs-lookup"><span data-stu-id="bf993-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="bf993-150">Breyttu auglýsingunni í Broadbean-glugganum.</span><span class="sxs-lookup"><span data-stu-id="bf993-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="bf993-151">– eða –</span><span class="sxs-lookup"><span data-stu-id="bf993-151">–or–</span></span>

1. <span data-ttu-id="bf993-152">Opnaðu starfið í Attract sem þú vilt skoða á Broadbean.</span><span class="sxs-lookup"><span data-stu-id="bf993-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="bf993-153">Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="bf993-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="bf993-154">Í Broadbean-glugganum skal breyta upplýsingum um starfið og síðan birta starfið aftur.</span><span class="sxs-lookup"><span data-stu-id="bf993-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="bf993-155">Upplýsingar um starfið í Attract haldast óbreyttar.</span><span class="sxs-lookup"><span data-stu-id="bf993-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="bf993-156">Fjarlægja starfsauglýsingu úr Broadbean</span><span class="sxs-lookup"><span data-stu-id="bf993-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="bf993-157">Hægt er að fjarlægja starfsauglýsingu úr Broadbean ef þess gerist þörf.</span><span class="sxs-lookup"><span data-stu-id="bf993-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="bf993-158">Opnaðu starfið í Attract sem þú vilt fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="bf993-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="bf993-159">Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Fjarlægja auglýsingu**.</span><span class="sxs-lookup"><span data-stu-id="bf993-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="bf993-160">Eftir að Broadbean fjarlægir starfið verður Broadbean-atriðið í Attract með hnappinn **Birta núna**.</span><span class="sxs-lookup"><span data-stu-id="bf993-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="bf993-161">Hnappurinn gefur til kynna að starfið hafi verið fjarlægt og hægt sé að birta það aftur.</span><span class="sxs-lookup"><span data-stu-id="bf993-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="bf993-162">Úrræðaleita Broadbean-samþættinguna</span><span class="sxs-lookup"><span data-stu-id="bf993-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="bf993-163">Ef þú átt í vandræðum með að birta starf á Broadbean, reyndu þá þessi skref.</span><span class="sxs-lookup"><span data-stu-id="bf993-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="bf993-164">Staðfestu að aðgangsupplýsingarnar fyrir Broadbean sem þú slóst inn í Attract séu réttar og í gildi.</span><span class="sxs-lookup"><span data-stu-id="bf993-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="bf993-165">Ef upplýsingarnar eru enn í gildi og réttar skaltu hafa samband við [Notendaþjónusta Broadbean](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="bf993-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="bf993-166">Ef vandamálið er viðvarandi skaltu hafa samband við [Notendaþjónusta Microsoft](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="bf993-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
