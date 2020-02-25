---
title: Skilgreina valfrjálsa eiginleika forskoðunarumhverfis fyrir Dynamics 365 Commerce
description: Þetta efni útskýrir hvernig á að stilla valfrjálsa eiginleika fyrir Microsoft Dynamics 365 Commerce forskoðunarumhverfi.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024730"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="7f206-103">Skilgreina valfrjálsa eiginleika forskoðunarumhverfis fyrir Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="7f206-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7f206-104">Þetta efni útskýrir hvernig á að stilla valfrjálsa eiginleika fyrir Microsoft Dynamics 365 Commerce forskoðunarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="7f206-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7f206-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="7f206-105">Prerequisites</span></span>

<span data-ttu-id="7f206-106">Ef þú vilt meta viðskipti tölvupóstsaðgerða verður að uppfylla eftirfarandi forsendur:</span><span class="sxs-lookup"><span data-stu-id="7f206-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="7f206-107">Þú ert með tiltækan tölvupóstnetþjón (Simple Mail Transfer Protocol \[SMTP\] miðlara) sem er hægt að nota úr Microsoft Azure-áskriftinni þar sem þú útvegaðir forskoðunarumhverfið.</span><span class="sxs-lookup"><span data-stu-id="7f206-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="7f206-108">Þú ert með gilt lénsheiti (FQDN)/IP-tölu netþjónsins, SMTP-gáttarnúmer og staðfestingu upplýsingar tiltækar.</span><span class="sxs-lookup"><span data-stu-id="7f206-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="7f206-109">Ef þú vilt meta eiginleika stafrænna eignaumsjónarmiða með því að taka inn nýjar myndir af omni-rásum, verður þú að hafa nafn leigjanda efnisstjórnunarkerfisins (CMS) tiltækt.</span><span class="sxs-lookup"><span data-stu-id="7f206-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="7f206-110">Leiðbeiningar til að finna þetta nafn eru gefnar síðar í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="7f206-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="7f206-111">>>> (Sp.: Hvar eru leiðbeiningarnar?)</span><span class="sxs-lookup"><span data-stu-id="7f206-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="7f206-112">Stilla bak myndarinnar</span><span class="sxs-lookup"><span data-stu-id="7f206-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="7f206-113">Finndu grunnvefslóð miðla</span><span class="sxs-lookup"><span data-stu-id="7f206-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="7f206-114">Áður en þú getur klárað þessa aðferð verður þú að klára skrefin í [Settu upp síðuna þína í Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="7f206-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="7f206-115">Skráðu þig inn á stjórnunartól verslunarinnar með því að nota slóðina sem þú skrifaðir niður þegar þú frumstilltir e-Commerce við úthlutun (sjá [Frumstilla e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="7f206-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="7f206-116">Opnið svæðið **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="7f206-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="7f206-117">Á valmyndinni til vinstri velurðu **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="7f206-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="7f206-118">Veldu einhverja staka myndeign.</span><span class="sxs-lookup"><span data-stu-id="7f206-118">Select any single image asset.</span></span>
1. <span data-ttu-id="7f206-119">Í eiginleikaeftirlitinu til hægri skaltu finna eiginleikann **Opinber vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="7f206-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="7f206-120">Gildið er vefslóð.</span><span class="sxs-lookup"><span data-stu-id="7f206-120">The value is a URL.</span></span> <span data-ttu-id="7f206-121">Eftirfarandi er dæmi:</span><span class="sxs-lookup"><span data-stu-id="7f206-121">Here is an example:</span></span>

    <span data-ttu-id="7f206-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="7f206-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="7f206-123">Skiptu út síðasta auðkenni í slóðinni (**MA1nQC** í dæminu hér að undan) með strengnum **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="7f206-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="7f206-124">Svona lítur vefslóðarsýnishornið út þegar þessi breyting er gerð:</span><span class="sxs-lookup"><span data-stu-id="7f206-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="7f206-125">Þessi slóð er grunnvefslóð miðla þinna.</span><span class="sxs-lookup"><span data-stu-id="7f206-125">This URL is your media base URL.</span></span> <span data-ttu-id="7f206-126">Skrifaðu það hjá þér.</span><span class="sxs-lookup"><span data-stu-id="7f206-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="7f206-127">Uppfærðu grunnvefslóð miðla</span><span class="sxs-lookup"><span data-stu-id="7f206-127">Update the media base URL</span></span>

1. <span data-ttu-id="7f206-128">Innskráning í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="7f206-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="7f206-129">Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail \> Uppsetning rásar \> Rásaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="7f206-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="7f206-130">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7f206-130">Select **Edit**.</span></span>
1. <span data-ttu-id="7f206-131">Undir **Forstillingareiginleikum** skiptirðu út gildinu fyrir eiginleikann **Grunnvefslóð miðlaþjóns** með þeirri grunnvefslóð miðla sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="7f206-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7f206-132">Á listanum til vinstri, undir rásinni **Sjálfgefið**, velurðu aðra rás.</span><span class="sxs-lookup"><span data-stu-id="7f206-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="7f206-133">Undir **Forstillingareiginleikar** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7f206-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="7f206-134">Veldu fyrir eignina sem var bætt við **Grunnvefslóð miðlaþjóns** sem eiginleikalykill.</span><span class="sxs-lookup"><span data-stu-id="7f206-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="7f206-135">Sem eiginleikagildi skaltu slá inn grunnvefslóð miðla sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="7f206-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7f206-136">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7f206-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="7f206-137">Stilltu tölvupóstþjóninn</span><span class="sxs-lookup"><span data-stu-id="7f206-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="7f206-138">SMTP-miðlarinn eða tölvupóstþjónustan sem þú slærð inn hér verða að vera aðgengileg innan Azure áskriftarinnar sem þú notar fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="7f206-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="7f206-139">Skráðu þig inn á Retail.</span><span class="sxs-lookup"><span data-stu-id="7f206-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="7f206-140">Notaðu valmyndina til vinstri til að fara í **Einingar \> Kerfisstjórnun \> Uppsetning \> Tölvupóstur \> Færibreytur tölvupósts**.</span><span class="sxs-lookup"><span data-stu-id="7f206-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="7f206-141">Á flipanum **SMTP-stillingar**, í reitnum **Þjónn fyrir sendan póst**, slærðu inn FQDN eða IP-tölu SMTP-netþjónsins eða tölvupóstþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="7f206-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="7f206-142">Í reitnum **SMTP-númer tengis** slærðu inn númer tengisins.</span><span class="sxs-lookup"><span data-stu-id="7f206-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="7f206-143">(Ef þú ert ekki að nota Secure Sockets Layer \[SSL\] er sjálfgefið númer tengis **25**.)</span><span class="sxs-lookup"><span data-stu-id="7f206-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="7f206-144">Ef staðfesting er nauðsynleg skal slá inn gildi í reitina **Notandanafn** og **Lykilorð**.</span><span class="sxs-lookup"><span data-stu-id="7f206-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="7f206-145">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7f206-145">Select **Save**.</span></span>
1. <span data-ttu-id="7f206-146">Veldu **Endurnýja**.</span><span class="sxs-lookup"><span data-stu-id="7f206-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="7f206-147">Á flipanum **Prufupóstur**, í reitnum **Tölvupóstveita**, velurðu **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="7f206-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="7f206-148">Í reitinn **Senda til** slærðu inn netfangið sem prufupóstfangið skal afhent á.</span><span class="sxs-lookup"><span data-stu-id="7f206-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="7f206-149">Veldu **Senda prufupóst**.</span><span class="sxs-lookup"><span data-stu-id="7f206-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="7f206-150">Stilla tölvupóstsniðmát</span><span class="sxs-lookup"><span data-stu-id="7f206-150">Configure email templates</span></span>

<span data-ttu-id="7f206-151">Uppfæra verður tölvupóstsniðmátið fyrir hvert færslutilvik sem þú vilt senda tölvupóst með gildu netfangi sendanda.</span><span class="sxs-lookup"><span data-stu-id="7f206-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="7f206-152">Skráðu þig inn á Retail.</span><span class="sxs-lookup"><span data-stu-id="7f206-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="7f206-153">Notaðu valmyndina til vinstri til að fara í **Einingar \> Fyrirtækisstjórnun \> Uppsetning \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="7f206-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7f206-154">Veldu **Sýna lista**.</span><span class="sxs-lookup"><span data-stu-id="7f206-154">Select **Show list**.</span></span>
1. <span data-ttu-id="7f206-155">Fyrir hvert sniðmát á listanum skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="7f206-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="7f206-156">Í reitinn **Netfang sendanda** slærðu inn netfang sendanda.</span><span class="sxs-lookup"><span data-stu-id="7f206-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="7f206-157">Valfrjálst: Í reitinn **Nafn sendanda** slærðu inn nafnið sem ætti að nota sem nafn sendandans.</span><span class="sxs-lookup"><span data-stu-id="7f206-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="7f206-158">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7f206-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="7f206-159">Sérstilla sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="7f206-159">Customize email templates</span></span>

<span data-ttu-id="7f206-160">Þú gætir viljað aðlaga tölvupóstsniðmátin þannig að þau noti mismunandi myndir.</span><span class="sxs-lookup"><span data-stu-id="7f206-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="7f206-161">Eða þú gætir viljað uppfæra tenglana í sniðmátunum þannig að þeir fari í forskoðunarumhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="7f206-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="7f206-162">Þetta ferli útskýrir hvernig á að hala niður sjálfgefnu sniðmátunum, aðlaga þau og uppfæra sniðmátin í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7f206-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="7f206-163">Í netvafra skaltu hlaða niður [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) á tölvuna þína.</span><span class="sxs-lookup"><span data-stu-id="7f206-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="7f206-164">Þessi skrá inniheldur eftirfarandi HTML skjöl:</span><span class="sxs-lookup"><span data-stu-id="7f206-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="7f206-165">Eining pöntunarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="7f206-165">Order confirmation template</span></span>
    - <span data-ttu-id="7f206-166">Gefa út sniðmát gjafakorts</span><span class="sxs-lookup"><span data-stu-id="7f206-166">Issue gift card template</span></span>
    - <span data-ttu-id="7f206-167">Nýtt pöntunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="7f206-167">New order template</span></span>
    - <span data-ttu-id="7f206-168">Umbúðapöntunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="7f206-168">Pack order template</span></span>
    - <span data-ttu-id="7f206-169">Tiltektarpöntunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="7f206-169">Pick order template</span></span>

1. <span data-ttu-id="7f206-170">Sérsniðið sniðmátin með texta- eða HTML-ritil.</span><span class="sxs-lookup"><span data-stu-id="7f206-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="7f206-171">Sjá lista yfir [studd tákn](#supported-tokens-in-the-email-template) seinna í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="7f206-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="7f206-172">Skráðu þig inn á Retail.</span><span class="sxs-lookup"><span data-stu-id="7f206-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="7f206-173">Notaðu valmyndina til vinstri til að fara í **Einingar \> Fyrirtækisstjórnun \> Uppsetning \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="7f206-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7f206-174">Stækkaðu listann vinstra megin til að sjá öll sniðmát.</span><span class="sxs-lookup"><span data-stu-id="7f206-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="7f206-175">Fylgdu þessum skrefum fyrir hvert sniðmát sem þú vilt aðlaga:</span><span class="sxs-lookup"><span data-stu-id="7f206-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="7f206-176">Veldu sniðmátið á listanum.</span><span class="sxs-lookup"><span data-stu-id="7f206-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="7f206-177">Undir **Innihald tölvupóstskilaboða** velurðu viðeigandi tungumálarútgáfu af listanum.</span><span class="sxs-lookup"><span data-stu-id="7f206-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="7f206-178">(Sjálfgefið tungumál er **en-us**).</span><span class="sxs-lookup"><span data-stu-id="7f206-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="7f206-179">Undir **Efni tölvupóstskilaboða** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7f206-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="7f206-180">Glugginn **Hlaða upp sniðmáti fyrir tölvupóst** birtist.</span><span class="sxs-lookup"><span data-stu-id="7f206-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="7f206-181">Veldu **Fletta** og finndu HTML-skjalið sem hefur sérsniðna innihaldið.</span><span class="sxs-lookup"><span data-stu-id="7f206-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="7f206-182">Veldu **Hlaða upp**.</span><span class="sxs-lookup"><span data-stu-id="7f206-182">Select **Upload**.</span></span> <span data-ttu-id="7f206-183">Sniðmátinu er hlaðið inn í kerfið og forskoðun birtist.</span><span class="sxs-lookup"><span data-stu-id="7f206-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="7f206-184">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7f206-184">Select **OK**.</span></span>
    1. <span data-ttu-id="7f206-185">Valfrjálst: Sérsníða eiginleikann **Efni** í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="7f206-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="7f206-186">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7f206-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="7f206-187">Studd tákn í tölvupóstsniðmátinu</span><span class="sxs-lookup"><span data-stu-id="7f206-187">Supported tokens in the email template</span></span>

<span data-ttu-id="7f206-188">Þegar tölvupóstur er gerður er þessum táknum skipt út fyrir raungildi sem eiga við viðskiptavin og pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="7f206-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="7f206-189">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="7f206-189">Sales order</span></span>

<span data-ttu-id="7f206-190">Eftirfarandi tákn eiga við um heildarsölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="7f206-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="7f206-191">Heiti táknsins</span><span class="sxs-lookup"><span data-stu-id="7f206-191">Name of the token</span></span> | <span data-ttu-id="7f206-192">Tákn</span><span class="sxs-lookup"><span data-stu-id="7f206-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="7f206-193">Pöntunarnúmer</span><span class="sxs-lookup"><span data-stu-id="7f206-193">Order number</span></span>      | <span data-ttu-id="7f206-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="7f206-194">%salesid%</span></span> |
| <span data-ttu-id="7f206-195">Nafn viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="7f206-195">Customer's name</span></span>   | <span data-ttu-id="7f206-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="7f206-196">%customername%</span></span> |
| <span data-ttu-id="7f206-197">Afh.aðsetur</span><span class="sxs-lookup"><span data-stu-id="7f206-197">Delivery address</span></span>  | <span data-ttu-id="7f206-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7f206-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="7f206-199">Póstfang greiðanda</span><span class="sxs-lookup"><span data-stu-id="7f206-199">Billing address</span></span>   | <span data-ttu-id="7f206-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="7f206-200">%customeraddress%</span></span> |
| <span data-ttu-id="7f206-201">Pöntunardagsetning</span><span class="sxs-lookup"><span data-stu-id="7f206-201">Order date</span></span>        | <span data-ttu-id="7f206-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="7f206-202">%shipdate%</span></span> |
| <span data-ttu-id="7f206-203">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="7f206-203">Delivery mode</span></span>     | <span data-ttu-id="7f206-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="7f206-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="7f206-205">Afsláttur</span><span class="sxs-lookup"><span data-stu-id="7f206-205">Discount</span></span>          | <span data-ttu-id="7f206-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="7f206-206">%discount%</span></span> |
| <span data-ttu-id="7f206-207">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="7f206-207">Sales tax</span></span>         | <span data-ttu-id="7f206-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="7f206-208">%tax%</span></span> |
| <span data-ttu-id="7f206-209">Heildarupphæð pöntunar</span><span class="sxs-lookup"><span data-stu-id="7f206-209">Order total</span></span>       | <span data-ttu-id="7f206-210">%total%</span><span class="sxs-lookup"><span data-stu-id="7f206-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="7f206-211">Sölulínur</span><span class="sxs-lookup"><span data-stu-id="7f206-211">Sales line</span></span>

<span data-ttu-id="7f206-212">Eftirfarandi táknum er skipt út með gildum fyrir hverja vöru í röðinni.</span><span class="sxs-lookup"><span data-stu-id="7f206-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="7f206-213">Settu táknið **Vörulisti - byrja** í byrjun HTML-bálksins sem er endurtekinn fyrir hverja vöru og settu táknið **Vörulisti - ljúka** í lok bálksins.</span><span class="sxs-lookup"><span data-stu-id="7f206-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="7f206-214">Heiti táknsins</span><span class="sxs-lookup"><span data-stu-id="7f206-214">Name of the token</span></span>      | <span data-ttu-id="7f206-215">Tákn</span><span class="sxs-lookup"><span data-stu-id="7f206-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="7f206-216">Afurðalisti - hefja</span><span class="sxs-lookup"><span data-stu-id="7f206-216">Product list - start</span></span>   | <span data-ttu-id="7f206-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="7f206-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="7f206-218">Afurðalisti - lok</span><span class="sxs-lookup"><span data-stu-id="7f206-218">Product list - end</span></span>     | <span data-ttu-id="7f206-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="7f206-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="7f206-220">Afurðarnafn</span><span class="sxs-lookup"><span data-stu-id="7f206-220">Product name</span></span>           | <span data-ttu-id="7f206-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="7f206-221">%lineproductname%</span></span> |
| <span data-ttu-id="7f206-222">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7f206-222">Description</span></span>            | <span data-ttu-id="7f206-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="7f206-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="7f206-224">Magn</span><span class="sxs-lookup"><span data-stu-id="7f206-224">Quantity</span></span>               | <span data-ttu-id="7f206-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="7f206-225">%linequantity%</span></span> |
| <span data-ttu-id="7f206-226">Einingaverð línu</span><span class="sxs-lookup"><span data-stu-id="7f206-226">Line unit price</span></span>        | <span data-ttu-id="7f206-227">%lineprice% (staðfesta)</span><span class="sxs-lookup"><span data-stu-id="7f206-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="7f206-228">Heildarfjöldi línuatriða</span><span class="sxs-lookup"><span data-stu-id="7f206-228">line item total</span></span>        | <span data-ttu-id="7f206-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="7f206-229">%linenetamount%</span></span> |
| <span data-ttu-id="7f206-230">línuafsláttur</span><span class="sxs-lookup"><span data-stu-id="7f206-230">line discount</span></span>          | <span data-ttu-id="7f206-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="7f206-231">%linediscount%</span></span> |
| <span data-ttu-id="7f206-232">Sendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="7f206-232">Ship date</span></span>              | <span data-ttu-id="7f206-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="7f206-233">%lineshipdate%</span></span> |
| <span data-ttu-id="7f206-234">Innkaupaaðferð</span><span class="sxs-lookup"><span data-stu-id="7f206-234">Procurement method</span></span>     | <span data-ttu-id="7f206-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="7f206-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="7f206-236">afhendingaraðsetur</span><span class="sxs-lookup"><span data-stu-id="7f206-236">delivery address</span></span>       | <span data-ttu-id="7f206-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7f206-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="7f206-238">Sölueining línunnar</span><span class="sxs-lookup"><span data-stu-id="7f206-238">Sales unit of the line</span></span> | <span data-ttu-id="7f206-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="7f206-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7f206-240">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7f206-240">Additional resources</span></span>

[<span data-ttu-id="7f206-241">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="7f206-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7f206-242">Úthluta Dynamics 365 Commerce forsýningarumhverfi</span><span class="sxs-lookup"><span data-stu-id="7f206-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="7f206-243">Skilgreina Dynamics 365 Commerce forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="7f206-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7f206-244">Dynamics 365 Commerce yfirlitsumhverfi algengra spurninga</span><span class="sxs-lookup"><span data-stu-id="7f206-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7f206-245">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="7f206-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7f206-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="7f206-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7f206-247">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="7f206-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7f206-248">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="7f206-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
