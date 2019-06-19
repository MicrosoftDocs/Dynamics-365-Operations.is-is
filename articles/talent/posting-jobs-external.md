---
title: Auglýsa störf á utanaðkomandi ráðningarsíðum úr Attract
description: Þetta efnisatriði útskýrir hvernig á að nota Dynamics 365 for Talent - Attract til að auglýsa störf á utanaðkomandi ráðningarsíðum
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590483"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="7491f-103">Auglýsa störf á utanaðkomandi ráðningarsíðum úr Attract</span><span class="sxs-lookup"><span data-stu-id="7491f-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7491f-104">Þú vilt að sem flestir hæfir umsækjendur sjái lausu stöðurnar þínar.</span><span class="sxs-lookup"><span data-stu-id="7491f-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="7491f-105">Ráðningarsíður á borð við Broadbean auðvelda þér að ná þessu markmiði.</span><span class="sxs-lookup"><span data-stu-id="7491f-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="7491f-106">Microsoft Dynamics 365 Talent: Attract gerir þér nú kleift að auglýsa störf á Broadbean og Microsoft er stöðugt að bjóða upp á nýjar leiðir í þessum efnum.</span><span class="sxs-lookup"><span data-stu-id="7491f-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="7491f-107">Auglýsa störf á Broadbean</span><span class="sxs-lookup"><span data-stu-id="7491f-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="7491f-108">Áður en þú getur auglýst störf á Broadbean þarf fyrst að stilla Broadbean-samþættinguna.</span><span class="sxs-lookup"><span data-stu-id="7491f-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="7491f-109">Til að auglýsa störf á utanaðkomandi síðum verður þú að hafa [Viðbót við alhliða ráðningar](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="7491f-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="7491f-110">Til að birta störf í Broadbean í gegnum Attract er nauðsynlegt að vera með Broadbean-áskrift.</span><span class="sxs-lookup"><span data-stu-id="7491f-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="7491f-111">Þessi eiginleiki er í forútgáfu sem stendur.</span><span class="sxs-lookup"><span data-stu-id="7491f-111">This feature is currently in preview.</span></span> <span data-ttu-id="7491f-112">Ef þú vilt prófa hann verður þú að [kveikja á honum í stjórnandastillingum Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="7491f-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="7491f-113">Skilgreina Broadbean-samþættingu</span><span class="sxs-lookup"><span data-stu-id="7491f-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="7491f-114">Skráðu þig inn í Attract sem stjórnandi.</span><span class="sxs-lookup"><span data-stu-id="7491f-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="7491f-115">Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Stjórnandamiðstöð**.</span><span class="sxs-lookup"><span data-stu-id="7491f-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="7491f-116">Í flipanum **Stillingar atvinnutorgs**, í hlutanum **Virkja Broadbean-samþættingu** skal kveikja á samþættingunni.</span><span class="sxs-lookup"><span data-stu-id="7491f-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="7491f-117">Hafðu samband við Broadbean og færðu inn upplýsingarnar í **Notandanafn, auðkenni notanda, dulritunarlykill**.</span><span class="sxs-lookup"><span data-stu-id="7491f-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="7491f-118">Broadbean-aðgangsupplýsingarnar þínar eru viðkvæmar og trúnaðarmál.</span><span class="sxs-lookup"><span data-stu-id="7491f-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="7491f-119">Þar af leiðandi skaltu geyma og deila þeim af varkárni.</span><span class="sxs-lookup"><span data-stu-id="7491f-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="7491f-120">Hver sá sem gegnir stjórnandahlutverki í Attract getur skoðað þessar aðgangsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7491f-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="7491f-121">Microsoft og Attract taka engan þátt í að búa til og viðhalda þessum gildum.</span><span class="sxs-lookup"><span data-stu-id="7491f-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="7491f-122">Það er á þína ábyrgð að halda þeim uppfærðum í Attract og vinna með Broadbean til að leysa úr öllum vandamálum sem hafa með aðgangsupplýsingarnar þínar að gera.</span><span class="sxs-lookup"><span data-stu-id="7491f-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="7491f-123">Auglýsa starf á Broadbean</span><span class="sxs-lookup"><span data-stu-id="7491f-123">Post a job to Broadbean</span></span>

<span data-ttu-id="7491f-124">Eftir að kveikt hefur verið á Broadbean geta ráðningaraðilar og stjórnendur birt störf þar.</span><span class="sxs-lookup"><span data-stu-id="7491f-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="7491f-125">Þú verður að hafa umsóknarvefslóð fyrir starfið.</span><span class="sxs-lookup"><span data-stu-id="7491f-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="7491f-126">Í Attract, opnaðu starfið sem þú vilt auglýsa á Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7491f-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="7491f-127">Í hlutanum **Birtingar** skal velja hnappinn **Birta núna** sem á við um Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7491f-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="7491f-128">Fylgdu leiðbeiningunum í Broadbean-glugganum.</span><span class="sxs-lookup"><span data-stu-id="7491f-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="7491f-129">Attract sendir eftirfarandi upplýsingar til Broadbean:</span><span class="sxs-lookup"><span data-stu-id="7491f-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="7491f-130">Beiðnikenni</span><span class="sxs-lookup"><span data-stu-id="7491f-130">Request ID</span></span>
- <span data-ttu-id="7491f-131">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="7491f-131">Job title</span></span>
- <span data-ttu-id="7491f-132">Lýsing vinnslu</span><span class="sxs-lookup"><span data-stu-id="7491f-132">Job description</span></span>
- <span data-ttu-id="7491f-133">Staðsetning starfs</span><span class="sxs-lookup"><span data-stu-id="7491f-133">Job location</span></span>
- <span data-ttu-id="7491f-134">Sækja um vefslóðin</span><span class="sxs-lookup"><span data-stu-id="7491f-134">Apply URL</span></span>
- <span data-ttu-id="7491f-135">Upplýsingar um ráðningaraðila</span><span class="sxs-lookup"><span data-stu-id="7491f-135">Recruiter information</span></span>

<span data-ttu-id="7491f-136">Eftir að Broadbean lýkur við birtinguna sýnir hlutinn **Birtingar** fyrir starfið í Attract stöðuna á Broadbean sem **Birt**.</span><span class="sxs-lookup"><span data-stu-id="7491f-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="7491f-137">Broadbean þarf á reitnum **Atvinnugrein** að halda.</span><span class="sxs-lookup"><span data-stu-id="7491f-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="7491f-138">Sem stendur er þessi reitur sjálfkrafa stilltur á **Upplýsingatækni**.</span><span class="sxs-lookup"><span data-stu-id="7491f-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="7491f-139">Hins vegar er hægt að breyta gildinu í rétta atvinnugrein í glugganum fyrir birtingar á störfum í Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7491f-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="7491f-140">Það tekur smá tíma fyrir Broadbean að birta starfið þitt á öllum atvinnutorgum sem þú hefur valið.</span><span class="sxs-lookup"><span data-stu-id="7491f-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="7491f-141">Því kunna að vera smá tafir áður en Attract birtir uppfærslu á stöðu fyrir starfið.</span><span class="sxs-lookup"><span data-stu-id="7491f-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="7491f-142">Skoða auglýst starf á Broadbean</span><span class="sxs-lookup"><span data-stu-id="7491f-142">View a Broadbean job posting</span></span>

<span data-ttu-id="7491f-143">Eftir að starf er auglýst á Broadbean er hægt að skoða það í Attract.</span><span class="sxs-lookup"><span data-stu-id="7491f-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="7491f-144">Opnaðu starfið í Attract sem þú vilt skoða á Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7491f-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="7491f-145">Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="7491f-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="7491f-146">Starfsauglýsingin í Broadbean birtist í nýjum glugga.</span><span class="sxs-lookup"><span data-stu-id="7491f-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="7491f-147">Uppfæra starfsauglýsingu í Broadbean</span><span class="sxs-lookup"><span data-stu-id="7491f-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="7491f-148">Hægt er að uppfæra starfsauglýsingu í Broadbean á tvenna vegu.</span><span class="sxs-lookup"><span data-stu-id="7491f-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="7491f-149">Opnaðu starfið í Attract sem þú vilt uppfæra.</span><span class="sxs-lookup"><span data-stu-id="7491f-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="7491f-150">Í hlutanum **Birtingar** skal velja hnappinn **Uppfæra auglýsingu** sem á við um Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7491f-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="7491f-151">Breyttu auglýsingunni í Broadbean-glugganum.</span><span class="sxs-lookup"><span data-stu-id="7491f-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="7491f-152">– eða –</span><span class="sxs-lookup"><span data-stu-id="7491f-152">–or–</span></span>

1. <span data-ttu-id="7491f-153">Opnaðu starfið í Attract sem þú vilt skoða á Broadbean.</span><span class="sxs-lookup"><span data-stu-id="7491f-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="7491f-154">Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="7491f-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="7491f-155">Í Broadbean-glugganum skal breyta upplýsingum um starfið og síðan birta starfið aftur.</span><span class="sxs-lookup"><span data-stu-id="7491f-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="7491f-156">Upplýsingar um starfið í Attract haldast óbreyttar.</span><span class="sxs-lookup"><span data-stu-id="7491f-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="7491f-157">Fjarlægja starfsauglýsingu úr Broadbean</span><span class="sxs-lookup"><span data-stu-id="7491f-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="7491f-158">Hægt er að fjarlægja starfsauglýsingu úr Broadbean ef þess gerist þörf.</span><span class="sxs-lookup"><span data-stu-id="7491f-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="7491f-159">Opnaðu starfið í Attract sem þú vilt fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="7491f-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="7491f-160">Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Fjarlægja auglýsingu**.</span><span class="sxs-lookup"><span data-stu-id="7491f-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="7491f-161">Eftir að Broadbean fjarlægir starfið verður Broadbean-atriðið í Attract með hnappinn **Birta núna**.</span><span class="sxs-lookup"><span data-stu-id="7491f-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="7491f-162">Hnappurinn gefur til kynna að starfið hafi verið fjarlægt og hægt sé að birta það aftur.</span><span class="sxs-lookup"><span data-stu-id="7491f-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="7491f-163">Úrræðaleita Broadbean-samþættinguna</span><span class="sxs-lookup"><span data-stu-id="7491f-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="7491f-164">Ef þú átt í vandræðum með að birta starf á Broadbean, reyndu þá þessi skref.</span><span class="sxs-lookup"><span data-stu-id="7491f-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="7491f-165">Staðfestu að aðgangsupplýsingarnar fyrir Broadbean sem þú slóst inn í Attract séu réttar og í gildi.</span><span class="sxs-lookup"><span data-stu-id="7491f-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="7491f-166">Ef upplýsingarnar eru enn í gildi og réttar skaltu hafa samband við [Notendaþjónusta Broadbean](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="7491f-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="7491f-167">Ef vandamálið er viðvarandi skaltu hafa samband við [Notendaþjónusta Microsoft](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="7491f-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
