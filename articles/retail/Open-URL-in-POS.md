---
title: Opna vefslóð í POS
description: Þetta efnisatriði gefur yfirlit yfir úrbætur sem hafa verið gerðar á vöru og viðskiptahugbúnaði í Dynamics 365 Retail.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 406dad1709dc837f7f87817241d7062f6b08d8fd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025887"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="074e0-103">Opna vefslóð í POS</span><span class="sxs-lookup"><span data-stu-id="074e0-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="074e0-104">Þetta efnisatriði lýsir því hvernig hægt er að skilgreina hnapp í Retail-sölustað (POS) til að opna vefslóð.</span><span class="sxs-lookup"><span data-stu-id="074e0-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="074e0-105">Þessi eiginleiki krefst ekki sérstillingar á kóða og einhver sem ekki er í hlutverki þróunaraðila getur stillt hann.</span><span class="sxs-lookup"><span data-stu-id="074e0-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="074e0-106">Þessi eiginleiki leyfir stillingu á hnapp í POS með hönnuði hnappahnits til að opna vefslóð.</span><span class="sxs-lookup"><span data-stu-id="074e0-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="074e0-107">Sem stendur er þetta stutt í eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="074e0-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="074e0-108">Opna í nýjum glugga.</span><span class="sxs-lookup"><span data-stu-id="074e0-108">Open in new window.</span></span>
- <span data-ttu-id="074e0-109">Opna innan POS.</span><span class="sxs-lookup"><span data-stu-id="074e0-109">Open within POS.</span></span>
- <span data-ttu-id="074e0-110">Opna native-forrit.</span><span class="sxs-lookup"><span data-stu-id="074e0-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="074e0-111">Opna í nýjum glugga</span><span class="sxs-lookup"><span data-stu-id="074e0-111">Open in new window</span></span>

<span data-ttu-id="074e0-112">Þessi stilling skilgreinir hvort vefslóðin verði opnuð í nýjum glugga eða innan forritsins.</span><span class="sxs-lookup"><span data-stu-id="074e0-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="074e0-113">Yfirlitssvæðið til hliðar og efsta slá POS eru sýnileg og í boði fyrir notandann þegar stillt er á að vefslóð verði opnuð í forriti.</span><span class="sxs-lookup"><span data-stu-id="074e0-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="074e0-114">Vefslóðin opnast í nýjum glugga forrits í Modern POS fyrir Windows og í nýjum vafraglugga í öllum öðrum POS-biðlurum þegar stillt er á að nýr gluggi eigi að opnast.</span><span class="sxs-lookup"><span data-stu-id="074e0-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="074e0-115">Til að virkja þetta verður að stilla vefslóðina með því að velja valkostinn **Opna í nýjum glugga**.</span><span class="sxs-lookup"><span data-stu-id="074e0-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="074e0-116">Opna innan POS</span><span class="sxs-lookup"><span data-stu-id="074e0-116">Open within POS</span></span>

<span data-ttu-id="074e0-117">Opnun vefslóðar innan POS er sem stendur aðeins stutt fyrir Modern POS í Windows.</span><span class="sxs-lookup"><span data-stu-id="074e0-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="074e0-118">Á öðrum biðlurum er þessi möguleiki í þróun og áætlað er að gefa hann út í síðari uppfærslum.</span><span class="sxs-lookup"><span data-stu-id="074e0-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="074e0-119">Til að virkja þetta verður að stilla vefslóðina með því að velja ekki valkostinn **Opna í nýjum glugga**.</span><span class="sxs-lookup"><span data-stu-id="074e0-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="074e0-120">Opna native-forrit</span><span class="sxs-lookup"><span data-stu-id="074e0-120">Open a native app</span></span>

<span data-ttu-id="074e0-121">Þessi eiginleiki leyfir þér einnig að tilgreina slóðir sem ekki eru vefslóðir til að opna native-forrit.</span><span class="sxs-lookup"><span data-stu-id="074e0-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="074e0-122">Til dæmis er hægt að tilgreina samskiptareglur slóðar, eins og MailTo, SIP, IM eða MSTEAMS, sem native-forrit á tæki hýsils getur síðan meðhöndlað.</span><span class="sxs-lookup"><span data-stu-id="074e0-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="074e0-123">Til að virkja þetta verður að stilla vefslóðina með því að velja valkostinn **Opna í nýjum glugga**.</span><span class="sxs-lookup"><span data-stu-id="074e0-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="074e0-124">Fyrir Windows-tölvur skal skoða [Flytja út eða flytja inn sjálfgefnar forritatengingar](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) til að stilla sjálfgefnar tengingar samskiptareglu ef verið er að setja upp tölvuna með DISM (meðhöndlun afritsmynda).</span><span class="sxs-lookup"><span data-stu-id="074e0-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="074e0-125">Ef MDM er notað, t.d. Intune til að stjórna Windows-tölvunni, skal skoða [CSP-regla - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="074e0-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="074e0-126">Ef þú ert þróunaraðili að smíða sérsniðna vefsíðu skaltu skoða [Ræsa sjálfgefið forrit fyrir URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="074e0-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="074e0-127">Opna native-forrit án vandkvæða</span><span class="sxs-lookup"><span data-stu-id="074e0-127">Open a native app seamlessly</span></span>

<span data-ttu-id="074e0-128">Windows, iOS og Android leyfa einnig ræsingu forrita án vandkvæða, sem byggist á samskiptareglutengingu forrits.</span><span class="sxs-lookup"><span data-stu-id="074e0-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="074e0-129">Ef forritið þitt er ekki þegar stillt til að meðhöndla ræsingu úr vafra, gæti verið að þu þurfir þróunaraðila til að stilla þetta.</span><span class="sxs-lookup"><span data-stu-id="074e0-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="074e0-130">Fyrir Windows skal skoða [Virkja forrit fyrir vefsíður sem nota URI-forritarekla](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="074e0-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="074e0-131">Fyrir iOS skal skoða [Altækir tenglar fyrir þróunaraðila](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="074e0-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="074e0-132">Fyrir Android, sjá [Meðhöndlun Android forritatengla](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="074e0-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="074e0-133">Biðlari</span><span class="sxs-lookup"><span data-stu-id="074e0-133">Client</span></span>                | <span data-ttu-id="074e0-134">Opna í nýjum glugga</span><span class="sxs-lookup"><span data-stu-id="074e0-134">Open in new window</span></span> | <span data-ttu-id="074e0-135">Opna native-forrit</span><span class="sxs-lookup"><span data-stu-id="074e0-135">Open native app</span></span> | <span data-ttu-id="074e0-136">Opna innan POS</span><span class="sxs-lookup"><span data-stu-id="074e0-136">Open within POS</span></span> | <span data-ttu-id="074e0-137">Upplýsingar</span><span class="sxs-lookup"><span data-stu-id="074e0-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="074e0-138">Modern POS í Windows</span><span class="sxs-lookup"><span data-stu-id="074e0-138">Modern POS on Windows</span></span> | <span data-ttu-id="074e0-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="074e0-139">✓\*</span></span>                | <span data-ttu-id="074e0-140">✓</span><span class="sxs-lookup"><span data-stu-id="074e0-140">✓</span></span>               | <span data-ttu-id="074e0-141">✓</span><span class="sxs-lookup"><span data-stu-id="074e0-141">✓</span></span>              | <span data-ttu-id="074e0-142">\* Opnast í nýjum glugga Modern POS</span><span class="sxs-lookup"><span data-stu-id="074e0-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="074e0-143">Sölustaður í skýi</span><span class="sxs-lookup"><span data-stu-id="074e0-143">Cloud POS</span></span>             | <span data-ttu-id="074e0-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="074e0-144">✓\*</span></span>                | <span data-ttu-id="074e0-145">✓</span><span class="sxs-lookup"><span data-stu-id="074e0-145">✓</span></span>               | <span data-ttu-id="074e0-146">X</span><span class="sxs-lookup"><span data-stu-id="074e0-146">X</span></span>              | <span data-ttu-id="074e0-147">\* Opnast í nýjum vafraglugga</span><span class="sxs-lookup"><span data-stu-id="074e0-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="074e0-148">Modern POS í iOS</span><span class="sxs-lookup"><span data-stu-id="074e0-148">Modern POS on iOS</span></span>     | <span data-ttu-id="074e0-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="074e0-149">✓\*</span></span>                | <span data-ttu-id="074e0-150">✓</span><span class="sxs-lookup"><span data-stu-id="074e0-150">✓</span></span>               | <span data-ttu-id="074e0-151">X</span><span class="sxs-lookup"><span data-stu-id="074e0-151">X</span></span>              | <span data-ttu-id="074e0-152">\* Opnast í nýjum vafraglugga</span><span class="sxs-lookup"><span data-stu-id="074e0-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="074e0-153">Modern POS í Android</span><span class="sxs-lookup"><span data-stu-id="074e0-153">Modern POS on Android</span></span> | <span data-ttu-id="074e0-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="074e0-154">✓\*</span></span>                | <span data-ttu-id="074e0-155">✓</span><span class="sxs-lookup"><span data-stu-id="074e0-155">✓</span></span>               | <span data-ttu-id="074e0-156">X</span><span class="sxs-lookup"><span data-stu-id="074e0-156">X</span></span>              | <span data-ttu-id="074e0-157">\* Opnast í nýjum vafraglugga</span><span class="sxs-lookup"><span data-stu-id="074e0-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="074e0-158">Áður en hafist er handa</span><span class="sxs-lookup"><span data-stu-id="074e0-158">Before you begin</span></span>

<span data-ttu-id="074e0-159">Áður en hafist er handa skal yfirfara hvernig á að stilla [Skjáútlit fyrir sölustað (POS)](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="074e0-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="074e0-160">Opna vefslóð í POS</span><span class="sxs-lookup"><span data-stu-id="074e0-160">Open URL in POS</span></span>

<span data-ttu-id="074e0-161">Til að stilla vefslóð svo hún opnist í POS, skal framkvæma eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="074e0-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="074e0-162">Á aðalskrifstofu skal fara í **Smásala \> Uppsetning rásar \> Uppsetning sölustaðar \> Sölustaður \> Útlit afgreiðsluskjás**.</span><span class="sxs-lookup"><span data-stu-id="074e0-162">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="074e0-163">Veljið **Hnappahnit \> Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="074e0-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="074e0-164">Búið til nýjan hnapp.</span><span class="sxs-lookup"><span data-stu-id="074e0-164">Create a new button.</span></span>
4. <span data-ttu-id="074e0-165">Veljið eiginleikana **Hnappur**.</span><span class="sxs-lookup"><span data-stu-id="074e0-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="074e0-166">Veljið **Opna vefslóð** sem aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="074e0-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="074e0-167">Færið inn vefslóðina sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="074e0-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="074e0-168">Stillið hvort eigi að opna vefslóðina eða nýjan glugga.</span><span class="sxs-lookup"><span data-stu-id="074e0-168">Configure whether to open the URL in a new window.</span></span>
