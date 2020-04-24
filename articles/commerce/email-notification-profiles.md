---
title: Setja upp forstillingu tilkynningar í tölvupósti
description: Þetta efnisatriði lýsir því hvernig á að búa til tilkynningar um tölvupóst í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180196"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="1541a-103">Setja upp forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="1541a-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1541a-104">Þetta efnisatriði lýsir því hvernig á að búa til tilkynningar um tölvupóst í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1541a-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1541a-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="1541a-105">Overview</span></span>

<span data-ttu-id="1541a-106">Áður en þú stofnar rásir þarftu að setja upp prófíl til að tryggja að hægt sé að senda tölvupósttilkynningar vegna ýmissa viðburða, svo sem til pöntunar, pöntunarstöðu og greiðslubilun.</span><span class="sxs-lookup"><span data-stu-id="1541a-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="1541a-107">Frekari upplýsingar um hvernig á að skilgreina tölvupóst er að finna í [Stilling og sending tölvupósts](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="1541a-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="1541a-108">Stofna forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="1541a-108">Create an email notification profile</span></span>

<span data-ttu-id="1541a-109">Fylgdu þessum skrefum til að búa til tilkynningar um tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="1541a-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="1541a-110">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.</span><span class="sxs-lookup"><span data-stu-id="1541a-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="1541a-111">Í aðgerðasvæðinu er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="1541a-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="1541a-112">Í reitinn **Tilkynning um tölvupóst** slærðu inn heiti til að bera kennsl á forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="1541a-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="1541a-113">Í reitnum **Lýsing** skal færa inn viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="1541a-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="1541a-114">Stilltu rofann **Virkur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="1541a-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="1541a-115">Stofna sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="1541a-115">Create an email template</span></span>

<span data-ttu-id="1541a-116">Áður en hægt er að búa til tilkynningu í tölvupósti verður þú að búa til tölvupóstsniðmát stofnunar sem inniheldur tölvupóstupplýsingar sendenda og tölvupóstsniðmátið.</span><span class="sxs-lookup"><span data-stu-id="1541a-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="1541a-117">Til að stofna tölvupóstsniðmát, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="1541a-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="1541a-118">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="1541a-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="1541a-119">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="1541a-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1541a-120">Í reitinn **Kenni tölvupósts** slærðu inn kenni til að auðkenna þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="1541a-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="1541a-121">Í reitnum **Nafn sendanda** skal færa inn heiti sendanda.</span><span class="sxs-lookup"><span data-stu-id="1541a-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="1541a-122">Í reitnum **Lýsing tölvupósts** skal færa inn auðskiljanlega lýsingu.</span><span class="sxs-lookup"><span data-stu-id="1541a-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="1541a-123">Í **Netfang sendanda** slærðu inn netfang sendanda.</span><span class="sxs-lookup"><span data-stu-id="1541a-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="1541a-124">Í hlutanum **Almennt** fyllirðu út allar nauðsynlegar upplýsingar (svo sem forgang tölvupósts).</span><span class="sxs-lookup"><span data-stu-id="1541a-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="1541a-125">Stækkaðu hlutann **Efni tölvupóstskilaboða** og veldu **Nýtt** til að búa til sniðmátsinnihald.</span><span class="sxs-lookup"><span data-stu-id="1541a-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="1541a-126">Veldu tungumál fyrir hvern efnislið og gefðu upp efnislínu tölvupóstsins.</span><span class="sxs-lookup"><span data-stu-id="1541a-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="1541a-127">Ef tölvupósturinn verður með meginmál skal passa að hakað sé í reitinn **Hefur meginmál**.</span><span class="sxs-lookup"><span data-stu-id="1541a-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="1541a-128">Í aðgerðaglugganum velurðu **Tölvupóstskeyti** til að gefa upp meginmálssnið tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="1541a-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="1541a-129">Eftirfarandi mynd sýnir nokkur dæmi um sniðmátsstillingar tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="1541a-129">The following image shows some example email template settings.</span></span>

![Stillingar fyrir sniðmát tölvupósts](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="1541a-131">Stofna tilvik fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="1541a-131">Create an email event</span></span>

<span data-ttu-id="1541a-132">Til að stofna tölvupóststilvik, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="1541a-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="1541a-133">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.</span><span class="sxs-lookup"><span data-stu-id="1541a-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="1541a-134">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1541a-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="1541a-135">Velja tölvupóstssniðmát af fellislistanum **Tölvupóstskenni**.</span><span class="sxs-lookup"><span data-stu-id="1541a-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="1541a-136">Veldu viðeigandi **Gerð tilkynningar í tölvupósti** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="1541a-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="1541a-137">Velja skal gátreitinn **Virkt** .</span><span class="sxs-lookup"><span data-stu-id="1541a-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="1541a-138">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="1541a-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="1541a-139">Eftirfarandi mynd sýnir nokkur dæmi um stillingar tilkynningar tilviks.</span><span class="sxs-lookup"><span data-stu-id="1541a-139">The following image shows some example event notification settings.</span></span>

![Tilkynningastillingar tilvika](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="1541a-141">Næstu skref</span><span class="sxs-lookup"><span data-stu-id="1541a-141">Next steps</span></span>

<span data-ttu-id="1541a-142">Áður en þú getur sent tölvupóst verður þú að stilla póstþjónustu póst á útleið og setja upp runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="1541a-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="1541a-143">Nánari upplýsingar er að finna í [Skilgreina og senda tölvupóst](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="1541a-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="1541a-144">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1541a-144">Additional resources</span></span>

[<span data-ttu-id="1541a-145">Skilgreining og sending tölvupósts</span><span class="sxs-lookup"><span data-stu-id="1541a-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1541a-146">Yfirlit rása</span><span class="sxs-lookup"><span data-stu-id="1541a-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1541a-147">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="1541a-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="1541a-148">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="1541a-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
