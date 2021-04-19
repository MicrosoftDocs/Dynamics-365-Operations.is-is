---
title: Setja upp forstillingu tilkynningar í tölvupósti
description: Þetta efnisatriði lýsir hvernig á að stofna forstillingu tilkynningar í tölvupósti í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792658"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="23266-103">Setja upp forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="23266-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23266-104">Þetta efnisatriði lýsir hvernig á að stofna forstillingu tilkynningar í tölvupósti í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="23266-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="23266-105">Þegar rásir eru búnar til er hægt að setja upp forstillingu tilkynningar í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="23266-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="23266-106">Á þann hátt er hægt að senda viðskiptavinum tölvupósta vegna ýmissa færslutilvika á borð við stofnun pöntunar, sendingarstöðu pöntunar og greiðsluvillu.</span><span class="sxs-lookup"><span data-stu-id="23266-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="23266-107">Frekari upplýsingar um hvernig á að skilgreina tölvupóst er að finna í [Stilling og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="23266-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="23266-108">Stofna forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="23266-108">Create an email notification profile</span></span>

<span data-ttu-id="23266-109">Fylgdu þessum skrefum til að búa til tilkynningar um tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="23266-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="23266-110">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.</span><span class="sxs-lookup"><span data-stu-id="23266-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="23266-111">Í aðgerðasvæðinu er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="23266-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="23266-112">Í reitinn **Tilkynning um tölvupóst** slærðu inn heiti til að bera kennsl á forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="23266-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="23266-113">Í reitnum **Lýsing** skal færa inn viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="23266-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="23266-114">Stilltu rofann **Virkur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="23266-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="23266-115">Stofna sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="23266-115">Create an email template</span></span>

<span data-ttu-id="23266-116">Áður en hægt er að virkja gerð tölvupóststilkynningar þarf að stofna tölvupóstssniðmát fyrirtækis í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="23266-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="23266-117">Þetta sniðmát skilgreinir viðfangsefni tölvupóstsins, sjálfgefið tungumál hans og meginmál fyrir öll tungumálin sem á að styðja við.</span><span class="sxs-lookup"><span data-stu-id="23266-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="23266-118">Til að stofna tölvupóstsniðmát, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="23266-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="23266-119">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="23266-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="23266-120">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="23266-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="23266-121">Í reitinn **Kenni tölvupósts** slærðu inn kenni til að auðkenna þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="23266-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="23266-122">Í reitnum **Nafn sendanda** skal færa inn heiti sendanda.</span><span class="sxs-lookup"><span data-stu-id="23266-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="23266-123">Í reitnum **Lýsing tölvupósts** skal færa inn auðskiljanlega lýsingu.</span><span class="sxs-lookup"><span data-stu-id="23266-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="23266-124">Í **Netfang sendanda** slærðu inn netfang sendanda.</span><span class="sxs-lookup"><span data-stu-id="23266-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="23266-125">Í hlutanum **Almennt** skal velja sjálfgefið tungumál fyrir sniðmát tölvupóstsins.</span><span class="sxs-lookup"><span data-stu-id="23266-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="23266-126">Sjálfgefið tungumál verður notað þegar ekkert staðbundið sniðmát er til fyrir tilgreint tungumál.</span><span class="sxs-lookup"><span data-stu-id="23266-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="23266-127">Stækkaðu hlutann **Efni tölvupóstskilaboða** og veldu **Nýtt** til að búa til sniðmátsinnihald.</span><span class="sxs-lookup"><span data-stu-id="23266-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="23266-128">Veldu tungumál fyrir hvern efnislið og gefðu upp efnislínu tölvupóstsins.</span><span class="sxs-lookup"><span data-stu-id="23266-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="23266-129">Ef tölvupósturinn verður með meginmál skal passa að hakað sé í reitinn **Hefur meginmál**.</span><span class="sxs-lookup"><span data-stu-id="23266-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="23266-130">Í aðgerðaglugganum velurðu **Tölvupóstskeyti** til að gefa upp meginmálssnið tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="23266-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="23266-131">Eftirfarandi mynd sýnir nokkur dæmi um sniðmátsstillingar tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="23266-131">The following image shows some example email template settings.</span></span>

![Stillingar fyrir sniðmát tölvupósts](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="23266-133">Stofna tilvik fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="23266-133">Create an email event</span></span>

<span data-ttu-id="23266-134">Til að stofna tölvupóststilvik, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="23266-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="23266-135">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.</span><span class="sxs-lookup"><span data-stu-id="23266-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="23266-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="23266-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="23266-137">Velja tölvupóstssniðmát af fellislistanum **Tölvupóstskenni**.</span><span class="sxs-lookup"><span data-stu-id="23266-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="23266-138">Veldu viðeigandi **Gerð tilkynningar í tölvupósti** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="23266-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="23266-139">Velja skal gátreitinn **Virkt** .</span><span class="sxs-lookup"><span data-stu-id="23266-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="23266-140">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="23266-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="23266-141">Eftirfarandi mynd sýnir nokkur dæmi um stillingar tilkynningar tilviks.</span><span class="sxs-lookup"><span data-stu-id="23266-141">The following image shows some example event notification settings.</span></span>

![Tilkynningastillingar tilvika](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="23266-143">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="23266-143">Next steps</span></span>

<span data-ttu-id="23266-144">Áður en þú getur sent tölvupóst verður þú að stilla póstþjónustu póst á útleið og setja upp runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="23266-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="23266-145">Nánari upplýsingar er að finna í [Skilgreina og senda tölvupóst](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="23266-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="23266-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="23266-146">Additional resources</span></span>

[<span data-ttu-id="23266-147">Skilgreining og sending tölvupósts</span><span class="sxs-lookup"><span data-stu-id="23266-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="23266-148">Yfirlit rása</span><span class="sxs-lookup"><span data-stu-id="23266-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="23266-149">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="23266-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="23266-150">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="23266-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
