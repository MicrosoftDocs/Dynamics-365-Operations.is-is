---
title: Setja upp forstillingu tilkynningar í tölvupósti
description: Þetta efnisatriði lýsir því hvernig á að búa til tilkynningar um tölvupóst í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 320f21916a5f451ebf4f21e0075017a121ba6d6a
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057615"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="5e618-103">Setja upp forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="5e618-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5e618-104">Þetta efnisatriði lýsir því hvernig á að búa til tilkynningar um tölvupóst í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e618-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5e618-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5e618-105">Overview</span></span>

<span data-ttu-id="5e618-106">Áður en þú stofnar rásir þarftu að setja upp prófíl til að tryggja að hægt sé að senda tölvupósttilkynningar vegna ýmissa viðburða, svo sem til pöntunar, pöntunarstöðu og greiðslubilun.</span><span class="sxs-lookup"><span data-stu-id="5e618-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="5e618-107">Frekari upplýsingar um hvernig á að skilgreina tölvupóst er að finna í [Stilling og sending tölvupósts](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span><span class="sxs-lookup"><span data-stu-id="5e618-107">For additional email configuration information, see [Configure and send email](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="5e618-108">Stofna forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="5e618-108">Create an email notification profile</span></span>

<span data-ttu-id="5e618-109">Fylgdu þessum skrefum til að búa til tilkynningar um tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="5e618-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="5e618-110">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.</span><span class="sxs-lookup"><span data-stu-id="5e618-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="5e618-111">Í aðgerðasvæðinu er smellt á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5e618-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="5e618-112">Í reitinn **Tilkynning um tölvupóst** slærðu inn heiti til að bera kennsl á forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="5e618-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="5e618-113">Í reitnum **Lýsing** skal færa inn viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="5e618-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="5e618-114">Stilltu rofann **Virkur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="5e618-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="5e618-115">Stofna sniðmát fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="5e618-115">Create an email template</span></span>

<span data-ttu-id="5e618-116">Áður en hægt er að búa til tilkynningu í tölvupósti verður þú að búa til tölvupóstsniðmát stofnunar sem inniheldur tölvupóstupplýsingar sendenda og tölvupóstsniðmátið.</span><span class="sxs-lookup"><span data-stu-id="5e618-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="5e618-117">Til að stofna tölvupóstsniðmát, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="5e618-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="5e618-118">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Færibreytur \> Sniðmát tölvupósts fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="5e618-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="5e618-119">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5e618-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5e618-120">Í reitinn **Kenni tölvupósts** slærðu inn kenni til að auðkenna þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="5e618-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="5e618-121">Í reitnum **Nafn sendanda** skal færa inn heiti sendanda.</span><span class="sxs-lookup"><span data-stu-id="5e618-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="5e618-122">Í reitnum **Lýsing tölvupósts** skal færa inn auðskiljanlega lýsingu.</span><span class="sxs-lookup"><span data-stu-id="5e618-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="5e618-123">Í **Netfang sendanda** slærðu inn netfang sendanda.</span><span class="sxs-lookup"><span data-stu-id="5e618-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="5e618-124">Í hlutanum **Almennt** fyllirðu út allar nauðsynlegar upplýsingar (svo sem forgang tölvupósts).</span><span class="sxs-lookup"><span data-stu-id="5e618-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="5e618-125">Stækkaðu hlutann **Efni tölvupóstskilaboða** og veldu **Nýtt** til að búa til sniðmátsinnihald.</span><span class="sxs-lookup"><span data-stu-id="5e618-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="5e618-126">Veldu tungumál fyrir hvern efnislið og gefðu upp efnislínu tölvupóstsins.</span><span class="sxs-lookup"><span data-stu-id="5e618-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="5e618-127">Ef tölvupósturinn verður með meginmál skal passa að hakað sé í reitinn **Hefur meginmál**.</span><span class="sxs-lookup"><span data-stu-id="5e618-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="5e618-128">Í aðgerðaglugganum velurðu **Tölvupóstskeyti** til að gefa upp meginmálssnið tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="5e618-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="5e618-129">Eftirfarandi mynd sýnir nokkur dæmi um sniðmátsstillingar tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="5e618-129">The following image shows some example email template settings.</span></span>

![Stillingar fyrir sniðmát tölvupósts](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="5e618-131">Stofna tilvik fyrir tölvupóst</span><span class="sxs-lookup"><span data-stu-id="5e618-131">Create an email event</span></span>

<span data-ttu-id="5e618-132">Til að stofna tölvupóststilvik, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="5e618-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="5e618-133">Í skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Uppsetning höfuðstöðva \> Forstilling tilkynningar í tölvupósti í Commerce**.</span><span class="sxs-lookup"><span data-stu-id="5e618-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="5e618-134">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5e618-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="5e618-135">Velja tölvupóstssniðmát af fellislistanum **Tölvupóstskenni**.</span><span class="sxs-lookup"><span data-stu-id="5e618-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="5e618-136">Veldu viðeigandi **Gerð tilkynningar í tölvupósti** af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="5e618-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="5e618-137">Velja skal gátreitinn **Virkt** .</span><span class="sxs-lookup"><span data-stu-id="5e618-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="5e618-138">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="5e618-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5e618-139">Eftirfarandi mynd sýnir nokkur dæmi um stillingar tilkynningar tilviks.</span><span class="sxs-lookup"><span data-stu-id="5e618-139">The following image shows some example event notification settings.</span></span>

![Tilkynningastillingar tilvika](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="5e618-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5e618-141">Additional resources</span></span>

[<span data-ttu-id="5e618-142">Skilgreining og sending tölvupósts</span><span class="sxs-lookup"><span data-stu-id="5e618-142">Configure and send email</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-email)

[<span data-ttu-id="5e618-143">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="5e618-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5e618-144">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="5e618-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5e618-145">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="5e618-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
