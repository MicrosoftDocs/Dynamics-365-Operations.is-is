---
title: Flytja út gögn úr Attract og Onboard
description: Flytja út gögn úr Dynamics 365 Talent - Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975935"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="4f027-103">Flytja út gögn úr Attract og Onboard</span><span class="sxs-lookup"><span data-stu-id="4f027-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f027-104">Eins og tilkynnt var í [Forritin Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard tekin úr notkun](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) tökum við Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard úr notkun 1. febrúar 2022.</span><span class="sxs-lookup"><span data-stu-id="4f027-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="4f027-105">Til að hjálpa við flutning þinn í aðra afurð, bjóða bæði forritin nú útflutningsgetu gagna.</span><span class="sxs-lookup"><span data-stu-id="4f027-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="4f027-106">Flytja gögn út úr Attract</span><span class="sxs-lookup"><span data-stu-id="4f027-106">Export data from Attract</span></span>

<span data-ttu-id="4f027-107">Þú getur flutt gögn út án þess að takmarka aðgang að umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="4f027-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="4f027-108">Þú gætir viljað gera þetta í prófunarskyni eða til að skilja gagnaskipan okkar.</span><span class="sxs-lookup"><span data-stu-id="4f027-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="4f027-109">Þegar þú ert tilbúin/n að flytja skaltu takmarka aðgang að aðlaðandi umhverfi þínu með því að nota leiðbeiningarnar eftir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="4f027-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="4f027-110">Passaðu þig að flytja gögnin út aftur.</span><span class="sxs-lookup"><span data-stu-id="4f027-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="4f027-111">Opnið [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="4f027-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="4f027-112">Undir **Gagnaútflutningur** velurðu **Biðja um gagnaflutning**.</span><span class="sxs-lookup"><span data-stu-id="4f027-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="4f027-113">Biðja um gagnaflutning úr Attract</span><span class="sxs-lookup"><span data-stu-id="4f027-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="4f027-114">Þegar skilaboðareiturinn **Verið er að vinna úr beiðninni** birtist velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4f027-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="4f027-115">Gagnaútflutningurinn getur tekið allt að 20 mínútur, fer eftir stærð útflutningsins.</span><span class="sxs-lookup"><span data-stu-id="4f027-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="4f027-116">Þegar útflutningi þínum er lokið skaltu velja hnappinn **Sækja** við hliðina.</span><span class="sxs-lookup"><span data-stu-id="4f027-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="4f027-117">Allur útflutningur gagna er í boði í sjö daga, en þá rennur tengillinn **Sækja** út.</span><span class="sxs-lookup"><span data-stu-id="4f027-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="4f027-118">Niðurhalið inniheldur .zip-skrá með Attract gögnum þínum, þar á meðal eftirfarandi möppum:</span><span class="sxs-lookup"><span data-stu-id="4f027-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="4f027-119">Nafn möppu</span><span class="sxs-lookup"><span data-stu-id="4f027-119">Folder name</span></span> | <span data-ttu-id="4f027-120">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4f027-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="4f027-121">Stillingar stjórnanda</span><span class="sxs-lookup"><span data-stu-id="4f027-121">Admin settings</span></span> | <span data-ttu-id="4f027-122">Stillingar stjórnendamiðstöðvar Attract.</span><span class="sxs-lookup"><span data-stu-id="4f027-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="4f027-123">Umsækjendur</span><span class="sxs-lookup"><span data-stu-id="4f027-123">Candidates</span></span> | <span data-ttu-id="4f027-124">Allir umsækjendur sem bættust við störf eða hæfileikasöfn.</span><span class="sxs-lookup"><span data-stu-id="4f027-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="4f027-125">Sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="4f027-125">Email templates</span></span> | <span data-ttu-id="4f027-126">Öll tölvupóstsniðmát sem voru stillt fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="4f027-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="4f027-127">Sniðmát starfstilboðspakka</span><span class="sxs-lookup"><span data-stu-id="4f027-127">Job offer package templates</span></span> | <span data-ttu-id="4f027-128">Öll pakkasniðmát fyrir atvinnutilboð sem var búið til, ásamt tilheyrandi stillingum þeirra.</span><span class="sxs-lookup"><span data-stu-id="4f027-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="4f027-129">Reglusett starfstilboða</span><span class="sxs-lookup"><span data-stu-id="4f027-129">Job offer rule sets</span></span> |  <span data-ttu-id="4f027-130">Öllum reglusettaskrár sem hlaðið var upp til að stjórna tilboðum.</span><span class="sxs-lookup"><span data-stu-id="4f027-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="4f027-131">Sniðmát starfstilboða</span><span class="sxs-lookup"><span data-stu-id="4f027-131">Job offer templates</span></span> | <span data-ttu-id="4f027-132">Öll skjalasniðmát fyrir atvinnutilboð búin til fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="4f027-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="4f027-133">Laus störf</span><span class="sxs-lookup"><span data-stu-id="4f027-133">Job openings</span></span> | <span data-ttu-id="4f027-134">Öll stofnuð störf.</span><span class="sxs-lookup"><span data-stu-id="4f027-134">All created jobs.</span></span> <span data-ttu-id="4f027-135">Eydd störf eru ekki flutt út.</span><span class="sxs-lookup"><span data-stu-id="4f027-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="4f027-136">Undirmöppurnar innihalda umsækjendur, með undirmöppum fyrir viðbætur við umsækjendur og bjóða upp á pakka, þar sem við á.</span><span class="sxs-lookup"><span data-stu-id="4f027-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="4f027-137">Sniðmát fyrir laus störf</span><span class="sxs-lookup"><span data-stu-id="4f027-137">Job opening templates</span></span> | <span data-ttu-id="4f027-138">Sarfsferlissniðmát sem voru stillt í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="4f027-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="4f027-139">Hæfileikasöfn</span><span class="sxs-lookup"><span data-stu-id="4f027-139">Talent pools</span></span> | <span data-ttu-id="4f027-140">Öll stofnuð hæfileikasöfn, framlagslistar þeirra og listarnir yfir umsækjendur fyrir hæfileikasafnið.</span><span class="sxs-lookup"><span data-stu-id="4f027-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="4f027-141">Starfskraftar</span><span class="sxs-lookup"><span data-stu-id="4f027-141">Workers</span></span> | <span data-ttu-id="4f027-142">Listi yfir alla starfsmenn sem eru í umhverfinu auk hlutverka þeirra.</span><span class="sxs-lookup"><span data-stu-id="4f027-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="4f027-143">(rótarmappa)</span><span class="sxs-lookup"><span data-stu-id="4f027-143">(root folder)</span></span> | <span data-ttu-id="4f027-144">JSON skemaskrá sem lýsir reitum gagnaskipulags.</span><span class="sxs-lookup"><span data-stu-id="4f027-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="4f027-145">Takmarka aðgang að Attract</span><span class="sxs-lookup"><span data-stu-id="4f027-145">Restrict access to Attract</span></span>

<span data-ttu-id="4f027-146">Þegar þú ert tilbúin/n að flytja skaltu takmarka þá sem ekki hafa umsjón með aðgangi að Attract-umhverfi þínu og flytja gögnin út.</span><span class="sxs-lookup"><span data-stu-id="4f027-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="4f027-147">Takmörkun á aðgangi að Attract-umhverfi þínu er varanleg og ekki er hægt að afturkalla hana.</span><span class="sxs-lookup"><span data-stu-id="4f027-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="4f027-148">Ef þú vilt að aðrir notendur en stjórnendur muni halda áfram að fá aðgang að umhverfinu skaltu sleppa þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="4f027-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="4f027-149">Opnið [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="4f027-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="4f027-150">Til að takmarka aðgang fyrir aðra en stjórnendur að Attract-umhverfi þínu skaltu undir **Takmarka aðgang að þessu forriti** velja **Takmarka aðgang núna**.</span><span class="sxs-lookup"><span data-stu-id="4f027-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="4f027-151">Takmörkun aðgangs fjarlægir einnig öll virk störf sem hafa verið send.</span><span class="sxs-lookup"><span data-stu-id="4f027-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="4f027-152">Takmarka aðgang annarra en stjórnenda að Attract</span><span class="sxs-lookup"><span data-stu-id="4f027-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="4f027-153">Þegar þú sérð viðvörunina **Þetta er varanleg breyting** skaltu velja **Takmarka aðgang** til að takmarka varanlega aðra notendur en stjórnendur frá þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="4f027-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="4f027-154">Ef þú ert ekki tilbúin/n að ljúka þessu skrefi skaltu velja **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="4f027-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="4f027-155">Varað er við því takmörkun aðgangs er varanleg breyting</span><span class="sxs-lookup"><span data-stu-id="4f027-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="4f027-156">Stjórnendur geta haldið áfram að fá aðgang að gagnaútflutningi og skýrslusíðum einstaklinga eftir að þú hefur takmarkað aðgang að Attract-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="4f027-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="4f027-157">Flytja gögn út úr Onboard</span><span class="sxs-lookup"><span data-stu-id="4f027-157">Export data from Onboard</span></span>

<span data-ttu-id="4f027-158">Þegar þú ert tilbúin/n geturðu sótt sniðmát, leiðbeiningar og gögn um umsækjendur úr Onboard.</span><span class="sxs-lookup"><span data-stu-id="4f027-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="4f027-159">Opnið [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="4f027-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="4f027-160">Undir **Gagnaútflutningur** velurðu **Biðja um gagnaflutning**.</span><span class="sxs-lookup"><span data-stu-id="4f027-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="4f027-161">Biðja um gagnaflutning úr Onboard</span><span class="sxs-lookup"><span data-stu-id="4f027-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="4f027-162">Þegar skilaboðareiturinn **Verið er að vinna úr beiðninni** birtist velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4f027-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="4f027-163">Gagnaútflutningurinn getur tekið allt að 20 mínútur, fer eftir stærð útflutningsins.</span><span class="sxs-lookup"><span data-stu-id="4f027-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="4f027-164">Þegar útflutningi þínum er lokið skaltu velja hnappinn **Sækja** við hliðina.</span><span class="sxs-lookup"><span data-stu-id="4f027-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="4f027-165">Sækja gagnaútflutning úr Onboard</span><span class="sxs-lookup"><span data-stu-id="4f027-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="4f027-166">Gagnaútflutningur þinn er í boði í sjö daga.</span><span class="sxs-lookup"><span data-stu-id="4f027-166">Your data export is available for seven days.</span></span> <span data-ttu-id="4f027-167">Eftir sjö daga rennur tengillinn **Sækja** út og þú verður að biðja um nýjan útflutning ef þú þarft að sækja gögnin aftur.</span><span class="sxs-lookup"><span data-stu-id="4f027-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="4f027-168">Þegar þú hefur nýjan gagnaflutning renna öll fyrirliggjandi niðurhöl út þegar nýi útflutningurinn tekst.</span><span class="sxs-lookup"><span data-stu-id="4f027-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="4f027-169">Niðurhalið er .zip-skrá sem inniheldur:</span><span class="sxs-lookup"><span data-stu-id="4f027-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="4f027-170">Mappn **Sniðmát** sem inniheldur Onboard-sniðmát á Word-sniði.</span><span class="sxs-lookup"><span data-stu-id="4f027-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="4f027-171">Mappn **Guides** sem inniheldur Onboard-leiðbeiningar á Word-sniði.</span><span class="sxs-lookup"><span data-stu-id="4f027-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f027-172">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4f027-172">See also</span></span>

[<span data-ttu-id="4f027-173">Forritin Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard tekin úr notkun</span><span class="sxs-lookup"><span data-stu-id="4f027-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)