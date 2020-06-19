---
title: Vinna með CSS-hnekkingarskrár
description: Þetta efni lýsir hvers vegna, hvenær og hvernig á að nota Cascading Style Sheets (CSS) hnekkingarskrár í Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3ec43b16b1df07400cffe597378ad4035e4d07e0
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411248"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="354d1-103">Vinna með CSS-hnekkingarskrár</span><span class="sxs-lookup"><span data-stu-id="354d1-103">Work with CSS override files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="354d1-104">Þetta efni lýsir hvers vegna, hvenær og hvernig á að nota Cascading Style Sheets (CSS) hnekkingarskrár í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="354d1-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="354d1-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="354d1-105">Overview</span></span>

<span data-ttu-id="354d1-106">Varanlegir svæðisstílar ættu venjulega að vera meðhöndlaðir með þema svæðisins.</span><span class="sxs-lookup"><span data-stu-id="354d1-106">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="354d1-107">Þemu veita grunninn að CSS og stílstillingar fyrir einingarnar á hvaða síðu sem er á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="354d1-107">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="354d1-108">Þemu eru búin til með því að nota Dynamics 365 Commerce hugbúnaðarþróunarbúnað (SDK) á netinu og þau eru send á vefsíður þínar í gegnum Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="354d1-108">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="354d1-109">Kembigeta fyrir þemu og stillingar á einingaviðmótum í SDK hjálpa vefhönnuðum við að skapa sérsníðanlega og samloðandi vefhönnunarpakka.</span><span class="sxs-lookup"><span data-stu-id="354d1-109">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="354d1-110">Þegar þessir hönnunarpakkar eru settir á vefsvæði geta höfundar vefsvæðisins lagt áherslu á að búa til, breyta og birta efni í stað þess að þróa vefinn.</span><span class="sxs-lookup"><span data-stu-id="354d1-110">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="354d1-111">Í ljósi venjulegs líftíma þema getur hæði við hönnuði að gera stílbreytingar í gegnum uppsetningarleiðslu SDK og LCS verið hindrandi í sumum tilfellum.</span><span class="sxs-lookup"><span data-stu-id="354d1-111">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="354d1-112">Frumgerð vefsvæða eða bráðabóta geta virst fyrirferðarmikil ef SDK er ekki stillt eða ef þú hefur ekki tíma til að bíða eftir LCS-dreifingu.</span><span class="sxs-lookup"><span data-stu-id="354d1-112">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="354d1-113">Í þessum atburðarásum geta CSS hnekkingarskrár hjálpað.</span><span class="sxs-lookup"><span data-stu-id="354d1-113">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="354d1-114">Í höfundatækjum Commerce geta staðfestir notendur flutt upp CSS-skrá, forskoðað hana og virkjað síðan til að hnekkja þema vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="354d1-114">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="354d1-115">Ekki er krafist kostnaðar við uppsetningu á SDK eða LCS.</span><span class="sxs-lookup"><span data-stu-id="354d1-115">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="354d1-116">Hnekkingar sem eru tilgreindar í CSS-hnekkingarskrá geta verið eins litlar og breyting á einum textastíl eða eins umfangsmiklar og algjör yfirhalning vörumerkis.</span><span class="sxs-lookup"><span data-stu-id="354d1-116">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="354d1-117">Áður en þú notar CSS-hnekkingarskrár skaltu hafa eftirfarandi takmarkanir í huga:</span><span class="sxs-lookup"><span data-stu-id="354d1-117">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="354d1-118">Aðeins ein CSS-hnekkingarskrá í einu getur verið virk á vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="354d1-118">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="354d1-119">Þess vegna verða allar virkar hnekkingar að vera til staðar í einni hnekkingarskrá.</span><span class="sxs-lookup"><span data-stu-id="354d1-119">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="354d1-120">Þrátt fyrir að þú getir forskoðað hnekkingar í höfundatækjum Commerce eru engir sérstakir kembieiginleikar til að hjálpa til við að bera kennsl á villur sem hnekkingarnar koma á.</span><span class="sxs-lookup"><span data-stu-id="354d1-120">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="354d1-121">Með öðrum orðum, þegar þú notar CSS-hnekkingarskrár ertu ekki með sama verkfæri og SDK veitir fyrir staðfestingu eininga og höfundar.</span><span class="sxs-lookup"><span data-stu-id="354d1-121">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="354d1-122">Samt sem áður veita CSS-hnekkingarskrár skjóta leið til að frumgera hönnun eða útfæra bráðabót áður en full þemuuppfærsla er þróuð og dreift.</span><span class="sxs-lookup"><span data-stu-id="354d1-122">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="354d1-123">Stofna CSS-hnekkingarskrá</span><span class="sxs-lookup"><span data-stu-id="354d1-123">Create a CSS override file</span></span>

<span data-ttu-id="354d1-124">Til að búa til CSS-hnekkingarskrá er hægt að nota hvaða Integrated Development Environment (IDE), textaritil eða frumkóðaritil sem er.</span><span class="sxs-lookup"><span data-stu-id="354d1-124">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="354d1-125">Dæmigerð nálgun er að nota stöðluð kembiforrit í vafranum til að bera kennsl á stílveljara, eiginleika og gildi á núverandi svæði.</span><span class="sxs-lookup"><span data-stu-id="354d1-125">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="354d1-126">Flestir vafrar gera þér klefta að breyta gildum og forskoða þau í kembiforritinu.</span><span class="sxs-lookup"><span data-stu-id="354d1-126">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="354d1-127">Eftir að þú hefur bent á breytingarnar sem þú vilt gera geturðu vistað þær í þína eigin CSS-skrá.</span><span class="sxs-lookup"><span data-stu-id="354d1-127">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="354d1-128">Hlaða upp CSS-hnekkingarskrá</span><span class="sxs-lookup"><span data-stu-id="354d1-128">Upload a CSS override file</span></span>

<span data-ttu-id="354d1-129">Til að hlaða upp CSS-skrá á síðuna þína í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="354d1-129">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="354d1-130">Farðu á vefsvæðið í höfundatólunum.</span><span class="sxs-lookup"><span data-stu-id="354d1-130">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="354d1-131">Í stýriglugganum vinstra megin velurðu **Hanna**.</span><span class="sxs-lookup"><span data-stu-id="354d1-131">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="354d1-132">Það fer eftir útgáfu af höfundatækjum Commerce sem þú notar en þú gætir þurft að stækka **Stillingar** í leiðsöguglugganum áður en þú getur valið **Hönnun**.</span><span class="sxs-lookup"><span data-stu-id="354d1-132">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="354d1-133">Efst í aðalhönnunarglugganum velurðu flipann **CSS-hnekking**, ef hann hefur ekki þegar verið valinn.</span><span class="sxs-lookup"><span data-stu-id="354d1-133">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="354d1-134">Undir **Tiltækar CSS-hnekkingar** velurðu **Hlaða upp CSS-skrá**.</span><span class="sxs-lookup"><span data-stu-id="354d1-134">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="354d1-135">Gluggi í File Explorer birtist.</span><span class="sxs-lookup"><span data-stu-id="354d1-135">A File Explorer window appears.</span></span>
1. <span data-ttu-id="354d1-136">Í File Explorer flettirðu að og velur CSS-skrá og velur síðan **Opið**.</span><span class="sxs-lookup"><span data-stu-id="354d1-136">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="354d1-137">Uppflutt CSS-skrá birtist nú undir **Tiltækar CSS-hnekkingar**.</span><span class="sxs-lookup"><span data-stu-id="354d1-137">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="354d1-138">Forskoðun á CSS-hnekkingarskrá</span><span class="sxs-lookup"><span data-stu-id="354d1-138">Preview a CSS override file</span></span>

<span data-ttu-id="354d1-139">Til að forskoða CSS-hnekkingarskrá áður en þú gerir hana virka á lifandi vefsvæði skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="354d1-139">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="354d1-140">Í yfirlitssvæðinu til vinstri skaltu velja **Hanna** og síðan, á flipanum **CSS-hnekking**, undir **Tiltækar CSS-hnekkingar** skaltu finna CSS-skrána sem þú ætlar að forskoða.</span><span class="sxs-lookup"><span data-stu-id="354d1-140">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="354d1-141">Við hliðina á CSS-skráarheiti skaltu velja **Forskoða svæði**.</span><span class="sxs-lookup"><span data-stu-id="354d1-141">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="354d1-142">Í glugganum **Velja slóð** skaltu velja slóð vefsvæðisins sem þú vilt sjá að hnekkingu beitt á og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="354d1-142">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="354d1-143">Ef mörg afbrigði eru fyrir valda slóði skaltu velja afbrigðið sem óskað er í glugganum **Forskoða afbrigði** sem birtist.</span><span class="sxs-lookup"><span data-stu-id="354d1-143">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="354d1-144">Nýr vafraflipi eða -gluggi opnast þar sem þú getur sannreynt stílhnekkingar gagnvart vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="354d1-144">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="354d1-145">Þú getur síðan deilt slóðinni með öðrum staðfestum notendum Commerce til skoðunar og endurgjafar.</span><span class="sxs-lookup"><span data-stu-id="354d1-145">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="354d1-146">Virkja CSS-hnekkingarskrá á lifandi vefsvæði</span><span class="sxs-lookup"><span data-stu-id="354d1-146">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="354d1-147">Eftir að þú hefur forskoðað og samþykkt CSS-hnekkingarskrá geturðu virkjað hana á lifandi vefsvæði þínu.</span><span class="sxs-lookup"><span data-stu-id="354d1-147">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="354d1-148">Aðeins ein CSS-hnekkingarskrá í einu getur verið virk á vefsíðunni.</span><span class="sxs-lookup"><span data-stu-id="354d1-148">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="354d1-149">Ef þú virkjar nýja hnekkingarskrá er fyrri hnekkingarskráin óvirk.</span><span class="sxs-lookup"><span data-stu-id="354d1-149">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="354d1-150">Gakktu þess vegna úr skugga um að allar nauðsynlegar hnekkingar séu til staðar í einni CSS-hnekkingarskrá.</span><span class="sxs-lookup"><span data-stu-id="354d1-150">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="354d1-151">Til að virkja CSS-hnekkingarskrá skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="354d1-151">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="354d1-152">Í yfirlitssvæðinu til vinstri skaltu velja **Hanna** og síðan, á flipanum **CSS-hnekking**, undir **Tiltækar CSS-hnekkingar** skaltu finna CSS-skrána sem þú ætlar að virkja.</span><span class="sxs-lookup"><span data-stu-id="354d1-152">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="354d1-153">Undir CSS-skráarheiti velurðu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="354d1-153">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="354d1-154">Hnekkingarskráin verður strax virk á lifandi vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="354d1-154">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="354d1-155">Afvirkja CSS-hnekkingarskrá á lifandi vefsvæði</span><span class="sxs-lookup"><span data-stu-id="354d1-155">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="354d1-156">Til að afvirkja CSS-hnekkingarskrá á vefsvæðinu skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="354d1-156">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="354d1-157">Í yfirlitssvæðinu til vinstri skaltu velja **Hanna** og síðan, á flipanum **CSS-hnekking**, undir **Tiltækar CSS-hnekkingar** skaltu finna CSS-skrána sem þú ætlar að afvirkja.</span><span class="sxs-lookup"><span data-stu-id="354d1-157">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="354d1-158">Undir CSS-skráarheiti velurðu **Afvirkja**.</span><span class="sxs-lookup"><span data-stu-id="354d1-158">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="354d1-159">Hnekkingarskráin verður strax óvirk á lifandi vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="354d1-159">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="354d1-160">Til að fá aðgang að viðbótarmöguleikum fyrir CSS-hnekkingarskrár skaltu velja úrfellingarmerkið (**...**) við hliðina á CSS-skráarheitinu.</span><span class="sxs-lookup"><span data-stu-id="354d1-160">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="354d1-161">Valkostirnir **Hlaða niður**, **Endurnefna** og **Skipta út** eru nauðsynlegir fyrir snöggar breytingar á fyrirliggjandi CSS-hnekkingarskrá.</span><span class="sxs-lookup"><span data-stu-id="354d1-161">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="354d1-162">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="354d1-162">Additional resources</span></span>

[<span data-ttu-id="354d1-163">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="354d1-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="354d1-164">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="354d1-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="354d1-165">Vinna með forstillta stíla</span><span class="sxs-lookup"><span data-stu-id="354d1-165">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="354d1-166">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="354d1-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="354d1-167">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="354d1-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="354d1-168">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="354d1-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="354d1-169">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="354d1-169">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="354d1-170">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="354d1-170">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
