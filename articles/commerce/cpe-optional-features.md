---
title: Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi
description: Þetta efnisatriði útskýrir hvernig á að grunnstilla valfrjálsa eiginleika Microsoft Dynamics 365 Commerce matsumhverfis.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: def99a34404357e28501de5ccf11c6130d53f34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213819"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="ec40a-103">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ec40a-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec40a-104">Þetta efnisatriði útskýrir hvernig á að grunnstilla valfrjálsa eiginleika Microsoft Dynamics 365 Commerce matsumhverfis.</span><span class="sxs-lookup"><span data-stu-id="ec40a-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ec40a-105">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="ec40a-105">Prerequisites</span></span>

<span data-ttu-id="ec40a-106">Ef þú vilt meta viðskipti tölvupóstsaðgerða verður að uppfylla eftirfarandi forsendur:</span><span class="sxs-lookup"><span data-stu-id="ec40a-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="ec40a-107">Þú ert með tiltækan tölvupóstþjón (Simple Mail Transfer Protocol \[SMTP\] Server) sem hægt er að nota úr Microsoft Azure áskriftinni þar sem þú úthlutaði matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="ec40a-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="ec40a-108">Þú ert með gilt lénsheiti (FQDN)/IP-tölu netþjónsins, SMTP-gáttarnúmer og staðfestingu upplýsingar tiltækar.</span><span class="sxs-lookup"><span data-stu-id="ec40a-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="ec40a-109">Stilla bak myndarinnar</span><span class="sxs-lookup"><span data-stu-id="ec40a-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="ec40a-110">Finndu grunnvefslóð miðla</span><span class="sxs-lookup"><span data-stu-id="ec40a-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="ec40a-111">Áður en þú getur klárað þessa aðferð verður þú að klára skrefin í [Settu upp síðuna þína í Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="ec40a-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="ec40a-112">Skráðu þig inn á Commerce-vefsmið með því að nota slóðina sem þú skráðir þegar þú ræstir e-Commerce á meðan úthlutun stóð (sjá [Frumstilla rafræn viðskipti](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="ec40a-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="ec40a-113">Opnið svæðið **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="ec40a-114">Á valmyndinni til vinstri skal velja **Efnissafn**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="ec40a-115">Veldu einhverja staka myndeign.</span><span class="sxs-lookup"><span data-stu-id="ec40a-115">Select any single image asset.</span></span>
1. <span data-ttu-id="ec40a-116">Í eiginleikaeftirlitinu til hægri skaltu finna eiginleikann **Opinber vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="ec40a-117">Gildið er vefslóð.</span><span class="sxs-lookup"><span data-stu-id="ec40a-117">The value is a URL.</span></span> <span data-ttu-id="ec40a-118">Eftirfarandi er dæmi:</span><span class="sxs-lookup"><span data-stu-id="ec40a-118">Here is an example:</span></span>

    <span data-ttu-id="ec40a-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="ec40a-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="ec40a-120">Skiptu út síðasta auðkenni í slóðinni (**MA1nQC** í dæminu hér að undan) með strengnum **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="ec40a-121">Svona lítur vefslóðarsýnishornið út þegar þessi breyting er gerð:</span><span class="sxs-lookup"><span data-stu-id="ec40a-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="ec40a-122">Þessi slóð er grunnvefslóð miðla þinna.</span><span class="sxs-lookup"><span data-stu-id="ec40a-122">This URL is your media base URL.</span></span> <span data-ttu-id="ec40a-123">Skrifaðu það hjá þér.</span><span class="sxs-lookup"><span data-stu-id="ec40a-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="ec40a-124">Uppfærðu grunnvefslóð miðla</span><span class="sxs-lookup"><span data-stu-id="ec40a-124">Update the media base URL</span></span>

1. <span data-ttu-id="ec40a-125">Skráðu þig inn á Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ec40a-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="ec40a-126">Notaðu valmyndina til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Rásaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="ec40a-127">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-127">Select **Edit**.</span></span>
1. <span data-ttu-id="ec40a-128">Undir **Forstillingareiginleikum** skiptirðu út gildinu fyrir eiginleikann **Grunnvefslóð miðlaþjóns** með þeirri grunnvefslóð miðla sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="ec40a-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="ec40a-129">Veldu rásina sem kallast **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="ec40a-130">Undir **Forstillingareiginleikar** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="ec40a-131">Veldu fyrir eignina sem var bætt við **Grunnvefslóð miðlaþjóns** sem eiginleikalykill.</span><span class="sxs-lookup"><span data-stu-id="ec40a-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="ec40a-132">Sem eiginleikagildi skaltu slá inn grunnvefslóð miðla sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="ec40a-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="ec40a-133">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="ec40a-134">Stilla og prófa póstþjóninn</span><span class="sxs-lookup"><span data-stu-id="ec40a-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="ec40a-135">SMTP-miðlarinn eða tölvupóstþjónustan sem þú slærð inn hér verða að vera aðgengileg innan Azure áskriftarinnar sem þú notar fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="ec40a-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="ec40a-136">Skráðu þig inn á Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ec40a-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="ec40a-137">Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Færibreytur tölvupósts**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="ec40a-138">Á flipanum **SMTP-stillingar**, í reitnum **Þjónn fyrir sendan póst**, slærðu inn FQDN eða IP-tölu SMTP-netþjónsins eða tölvupóstþjónustunnar.</span><span class="sxs-lookup"><span data-stu-id="ec40a-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="ec40a-139">Í reitnum **SMTP-númer tengis** slærðu inn númer tengisins.</span><span class="sxs-lookup"><span data-stu-id="ec40a-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="ec40a-140">(Ef þú ert ekki að nota Secure Sockets Layer \[SSL\] er sjálfgefið númer tengis **25**.)</span><span class="sxs-lookup"><span data-stu-id="ec40a-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="ec40a-141">Ef staðfesting er nauðsynleg skal slá inn gildi í reitina **Notandanafn** og **Lykilorð**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="ec40a-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-142">Select **Save**.</span></span>
1. <span data-ttu-id="ec40a-143">Veldu **Endurnýja**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="ec40a-144">Á flipanum **Prufupóstur**, í reitnum **Tölvupóstveita**, velurðu **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="ec40a-145">Í reitinn **Senda til** slærðu inn netfangið sem prufupóstfangið skal afhent á.</span><span class="sxs-lookup"><span data-stu-id="ec40a-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="ec40a-146">Veldu **Senda prufupóst**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="ec40a-147">Stilla tölvupóstsniðmát</span><span class="sxs-lookup"><span data-stu-id="ec40a-147">Configure email templates</span></span>

<span data-ttu-id="ec40a-148">Uppfæra verður tölvupóstsniðmátið fyrir hvert færslutilvik sem þú vilt senda tölvupóst með gildu netfangi sendanda.</span><span class="sxs-lookup"><span data-stu-id="ec40a-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="ec40a-149">Skráðu þig inn á Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ec40a-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="ec40a-150">Notaðu valmyndina hér til vinstri til að fara í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="ec40a-151">Veldu **Sýna lista**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-151">Select **Show list**.</span></span>
1. <span data-ttu-id="ec40a-152">Fyrir hvert sniðmát á listanum skal fylgja eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="ec40a-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="ec40a-153">Í reitinn **Netfang sendanda** slærðu inn netfang sendanda.</span><span class="sxs-lookup"><span data-stu-id="ec40a-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="ec40a-154">Valfrjálst: Í reitinn **Nafn sendanda** slærðu inn nafnið sem ætti að nota sem nafn sendandans.</span><span class="sxs-lookup"><span data-stu-id="ec40a-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="ec40a-155">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="ec40a-156">Sérstilla sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="ec40a-156">Customize email templates</span></span>

<span data-ttu-id="ec40a-157">Þú gætir viljað aðlaga tölvupóstsniðmátin þannig að þau noti mismunandi myndir.</span><span class="sxs-lookup"><span data-stu-id="ec40a-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="ec40a-158">Eða þú gætir viljað uppfæra tengla í sniðmátunum þannig að þeir vísi í matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="ec40a-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="ec40a-159">Þetta ferli útskýrir hvernig á að hala niður sjálfgefnu sniðmátunum, aðlaga þau og uppfæra sniðmátin í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ec40a-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="ec40a-160">Í vefvafra skal sækja upp [ Microsoft Dynamics 365 Commerce Evaluation sjálfgefin zip-skrá fyrir tölvupóstsniðmát](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) í staðbundnu tölvunni.</span><span class="sxs-lookup"><span data-stu-id="ec40a-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="ec40a-161">Þessi skrá inniheldur eftirfarandi HTML skjöl:</span><span class="sxs-lookup"><span data-stu-id="ec40a-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="ec40a-162">Eining pöntunarsniðmáts</span><span class="sxs-lookup"><span data-stu-id="ec40a-162">Order confirmation template</span></span>
    - <span data-ttu-id="ec40a-163">Gefa út sniðmát gjafakorts</span><span class="sxs-lookup"><span data-stu-id="ec40a-163">Issue gift card template</span></span>
    - <span data-ttu-id="ec40a-164">Nýtt pöntunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="ec40a-164">New order template</span></span>
    - <span data-ttu-id="ec40a-165">Umbúðapöntunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="ec40a-165">Pack order template</span></span>
    - <span data-ttu-id="ec40a-166">Tiltektarpöntunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="ec40a-166">Pick order template</span></span>

1. <span data-ttu-id="ec40a-167">Sérsniðið sniðmátin með texta- eða HTML-ritil.</span><span class="sxs-lookup"><span data-stu-id="ec40a-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="ec40a-168">Sjá lista yfir [studd tákn](#supported-tokens-in-the-email-template) seinna í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="ec40a-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="ec40a-169">Innskráning í Commerce.</span><span class="sxs-lookup"><span data-stu-id="ec40a-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="ec40a-170">Notaðu valmyndina til vinstri til að fara í **Einingar \> Fyrirtækisstjórnun \> Uppsetning \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="ec40a-171">Stækkaðu listann vinstra megin til að sjá öll sniðmát.</span><span class="sxs-lookup"><span data-stu-id="ec40a-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="ec40a-172">Fylgdu þessum skrefum fyrir hvert sniðmát sem þú vilt aðlaga:</span><span class="sxs-lookup"><span data-stu-id="ec40a-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="ec40a-173">Veldu sniðmátið á listanum.</span><span class="sxs-lookup"><span data-stu-id="ec40a-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="ec40a-174">Undir **Innihald tölvupóstskilaboða** velurðu viðeigandi tungumálarútgáfu af listanum.</span><span class="sxs-lookup"><span data-stu-id="ec40a-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="ec40a-175">(Sjálfgefið tungumál er **en-us**).</span><span class="sxs-lookup"><span data-stu-id="ec40a-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="ec40a-176">Undir **Efni tölvupóstskilaboða** velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="ec40a-177">Glugginn **Hlaða upp sniðmáti fyrir tölvupóst** birtist.</span><span class="sxs-lookup"><span data-stu-id="ec40a-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="ec40a-178">Veldu **Fletta** og finndu HTML-skjalið sem hefur sérsniðna innihaldið.</span><span class="sxs-lookup"><span data-stu-id="ec40a-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="ec40a-179">Veldu **Hlaða upp**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-179">Select **Upload**.</span></span> <span data-ttu-id="ec40a-180">Sniðmátinu er hlaðið inn í kerfið og forskoðun birtist.</span><span class="sxs-lookup"><span data-stu-id="ec40a-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="ec40a-181">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-181">Select **OK**.</span></span>
    1. <span data-ttu-id="ec40a-182">Valfrjálst: Sérsníða eiginleikann **Efni** í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="ec40a-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="ec40a-183">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ec40a-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="ec40a-184">Studd tákn í tölvupóstsniðmátinu</span><span class="sxs-lookup"><span data-stu-id="ec40a-184">Supported tokens in the email template</span></span>

<span data-ttu-id="ec40a-185">Þegar tölvupóstur er gerður er þessum táknum skipt út fyrir raungildi sem eiga við viðskiptavin og pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ec40a-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="ec40a-186">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ec40a-186">Sales order</span></span>

<span data-ttu-id="ec40a-187">Eftirfarandi tákn eiga við um heildarsölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ec40a-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="ec40a-188">Heiti táknsins</span><span class="sxs-lookup"><span data-stu-id="ec40a-188">Name of the token</span></span> | <span data-ttu-id="ec40a-189">Merki</span><span class="sxs-lookup"><span data-stu-id="ec40a-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="ec40a-190">Pöntunarnúmer</span><span class="sxs-lookup"><span data-stu-id="ec40a-190">Order number</span></span>      | <span data-ttu-id="ec40a-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="ec40a-191">%salesid%</span></span> |
| <span data-ttu-id="ec40a-192">Nafn viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="ec40a-192">Customer's name</span></span>   | <span data-ttu-id="ec40a-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="ec40a-193">%customername%</span></span> |
| <span data-ttu-id="ec40a-194">Afh.aðsetur</span><span class="sxs-lookup"><span data-stu-id="ec40a-194">Delivery address</span></span>  | <span data-ttu-id="ec40a-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="ec40a-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="ec40a-196">Póstfang greiðanda</span><span class="sxs-lookup"><span data-stu-id="ec40a-196">Billing address</span></span>   | <span data-ttu-id="ec40a-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="ec40a-197">%customeraddress%</span></span> |
| <span data-ttu-id="ec40a-198">Pöntunardagsetning</span><span class="sxs-lookup"><span data-stu-id="ec40a-198">Order date</span></span>        | <span data-ttu-id="ec40a-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="ec40a-199">%shipdate%</span></span> |
| <span data-ttu-id="ec40a-200">Afhendingarmáti</span><span class="sxs-lookup"><span data-stu-id="ec40a-200">Delivery mode</span></span>     | <span data-ttu-id="ec40a-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="ec40a-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="ec40a-202">Afsláttur</span><span class="sxs-lookup"><span data-stu-id="ec40a-202">Discount</span></span>          | <span data-ttu-id="ec40a-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="ec40a-203">%discount%</span></span> |
| <span data-ttu-id="ec40a-204">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="ec40a-204">Sales tax</span></span>         | <span data-ttu-id="ec40a-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="ec40a-205">%tax%</span></span> |
| <span data-ttu-id="ec40a-206">Heildarupphæð pöntunar</span><span class="sxs-lookup"><span data-stu-id="ec40a-206">Order total</span></span>       | <span data-ttu-id="ec40a-207">%total%</span><span class="sxs-lookup"><span data-stu-id="ec40a-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="ec40a-208">Sölulína</span><span class="sxs-lookup"><span data-stu-id="ec40a-208">Sales line</span></span>

<span data-ttu-id="ec40a-209">Eftirfarandi táknum er skipt út með gildum fyrir hverja vöru í röðinni.</span><span class="sxs-lookup"><span data-stu-id="ec40a-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="ec40a-210">Settu táknið **Vörulisti - byrja** í byrjun HTML-bálksins sem er endurtekinn fyrir hverja vöru og settu táknið **Vörulisti - ljúka** í lok bálksins.</span><span class="sxs-lookup"><span data-stu-id="ec40a-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="ec40a-211">Heiti táknsins</span><span class="sxs-lookup"><span data-stu-id="ec40a-211">Name of the token</span></span>      | <span data-ttu-id="ec40a-212">Merki</span><span class="sxs-lookup"><span data-stu-id="ec40a-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="ec40a-213">Afurðalisti - hefja</span><span class="sxs-lookup"><span data-stu-id="ec40a-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="ec40a-214">Afurðalisti - lok</span><span class="sxs-lookup"><span data-stu-id="ec40a-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="ec40a-215">Afurðarnafn</span><span class="sxs-lookup"><span data-stu-id="ec40a-215">Product name</span></span>           | <span data-ttu-id="ec40a-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="ec40a-216">%lineproductname%</span></span> |
| <span data-ttu-id="ec40a-217">lýsing</span><span class="sxs-lookup"><span data-stu-id="ec40a-217">Description</span></span>            | <span data-ttu-id="ec40a-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="ec40a-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="ec40a-219">Magn</span><span class="sxs-lookup"><span data-stu-id="ec40a-219">Quantity</span></span>               | <span data-ttu-id="ec40a-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="ec40a-220">%linequantity%</span></span> |
| <span data-ttu-id="ec40a-221">Einingaverð línu</span><span class="sxs-lookup"><span data-stu-id="ec40a-221">Line unit price</span></span>        | <span data-ttu-id="ec40a-222">%lineprice% (staðfesta)</span><span class="sxs-lookup"><span data-stu-id="ec40a-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="ec40a-223">Heildarfjöldi línuatriða</span><span class="sxs-lookup"><span data-stu-id="ec40a-223">line item total</span></span>        | <span data-ttu-id="ec40a-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="ec40a-224">%linenetamount%</span></span> |
| <span data-ttu-id="ec40a-225">línuafsláttur</span><span class="sxs-lookup"><span data-stu-id="ec40a-225">line discount</span></span>          | <span data-ttu-id="ec40a-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="ec40a-226">%linediscount%</span></span> |
| <span data-ttu-id="ec40a-227">Sendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="ec40a-227">Ship date</span></span>              | <span data-ttu-id="ec40a-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="ec40a-228">%lineshipdate%</span></span> |
| <span data-ttu-id="ec40a-229">Innkaupaaðferð</span><span class="sxs-lookup"><span data-stu-id="ec40a-229">Procurement method</span></span>     | <span data-ttu-id="ec40a-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="ec40a-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="ec40a-231">afhendingaraðsetur</span><span class="sxs-lookup"><span data-stu-id="ec40a-231">delivery address</span></span>       | <span data-ttu-id="ec40a-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="ec40a-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="ec40a-233">Sölueining línunnar</span><span class="sxs-lookup"><span data-stu-id="ec40a-233">Sales unit of the line</span></span> | <span data-ttu-id="ec40a-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="ec40a-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ec40a-235">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ec40a-235">Additional resources</span></span>

[<span data-ttu-id="ec40a-236">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="ec40a-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ec40a-237">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ec40a-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="ec40a-238">Stilla Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ec40a-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="ec40a-239">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ec40a-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="ec40a-240">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="ec40a-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ec40a-241">Microsoft Dynamics Lifecycle Services (LSC)</span><span class="sxs-lookup"><span data-stu-id="ec40a-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ec40a-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ec40a-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ec40a-243">Microsoft Azure-gátt</span><span class="sxs-lookup"><span data-stu-id="ec40a-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ec40a-244">Dynamics 365 Commerce vefsvæði</span><span class="sxs-lookup"><span data-stu-id="ec40a-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]