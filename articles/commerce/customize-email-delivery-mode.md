---
title: Sérstilla tölvupósta vegna færslna eftir afhendingarmáta
description: Þetta efnisatriði lýsir því hvernig setja á upp sérsniðin sniðmát fyrir tölvupóst fyrir tilteknar tilkynningagerðir og afhendingarmáta í Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: faf5fba70bf9297727464e6046806696ab725001
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594972"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="70874-103">Sérstilla tölvupósta vegna færslna eftir afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="70874-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="70874-104">Þetta efnisatriði lýsir því hvernig setja á upp sérsniðin sniðmát fyrir tölvupóst fyrir tilteknar tilkynningagerðir og afhendingarmáta í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="70874-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="70874-105">Nú er hægt að sérstilla tölvupóst færslna fyrir samsetningu tilkynningagerðar (til dæmis, **Pöntun stofnuð**, **Pöntun pakkað** eða **Pöntun reikningsfærð**) og afhendingarmáta (til dæmis yfir nótt, sótt í verslun eða sótt fyrir utan verslun).</span><span class="sxs-lookup"><span data-stu-id="70874-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="70874-106">Sérsniðinn tölvupóstur færslna gerir söluaðilum kleift að leyfa viðskiptavinum sínum að panta með afgreiðsluupplifun sem er sérsniðin að afhendingarmáta pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="70874-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="70874-107">Hægt er t.d. að sérsníða tilvikið „pöntun pakkað“ til að veita leiðbeiningar um afhendingu fyrir utan verslun fyrir viðskiptavini sem velja að sækja fyrir utan verslun.</span><span class="sxs-lookup"><span data-stu-id="70874-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="70874-108">Einnig getur tilvikið veitt upplýsingar um farmflytjanda og afhendingarupplýsingar fyrir viðskiptavini sem velja að fá pöntunina sína senda.</span><span class="sxs-lookup"><span data-stu-id="70874-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="70874-109">Til að nota virkni fyrir sérstilltan tölvupóst fyrir færslur verður fyrst að kveikja á **Sérsniðin sniðmát fyrir tölvupóst færslna** með því að opna **Vinnusvæði \> Eiginleikastjórnun** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="70874-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="70874-110">Hægt er að sérsníða tölvupóst eftir afhendingarmáta fyrir eftirfarandi tilkynningagerðir:</span><span class="sxs-lookup"><span data-stu-id="70874-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="70874-111">**Afturköllun pöntunar** – Þessi tilkynning með tölvupósti er ný af nálinni.</span><span class="sxs-lookup"><span data-stu-id="70874-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="70874-112">**Pöntun búin til**</span><span class="sxs-lookup"><span data-stu-id="70874-112">**Order created**</span></span>
- <span data-ttu-id="70874-113">**Pöntun staðfest**</span><span class="sxs-lookup"><span data-stu-id="70874-113">**Order confirmed**</span></span>
- <span data-ttu-id="70874-114">**Pöntun reikningsfærð** – Þessi tilkynning með tölvupósti er ný af nálinni.</span><span class="sxs-lookup"><span data-stu-id="70874-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="70874-115">Hægt er að nota hana í staðinn fyrir tilkynningargerðina **Pöntun send** sem sendir tilkynningu vegna allra reikningsatvika afhendingarmátann sent (ekki sótt, borið út né afhent rafrænt).</span><span class="sxs-lookup"><span data-stu-id="70874-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="70874-116">**Pöntun tekin til**</span><span class="sxs-lookup"><span data-stu-id="70874-116">**Order picked**</span></span>
- <span data-ttu-id="70874-117">**Pöntun pakkað**</span><span class="sxs-lookup"><span data-stu-id="70874-117">**Order packed**</span></span>
- <span data-ttu-id="70874-118">**Pöntun tilbúin til afhendingar** – Aðeins er hægt að sérsníða þessa tilkynningagerð eftir afhendingarmáta ef kveikt er á eiginleikanum **Stuðningur fyrir margar afhendingarmáta**.</span><span class="sxs-lookup"><span data-stu-id="70874-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="70874-119">Í slíku tilviki hefur þessi tilkynningargerð svipaða virkni og tilkynningargerðin **Pöntun pakkað**.</span><span class="sxs-lookup"><span data-stu-id="70874-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="70874-120">**Greiðsla mistókst**</span><span class="sxs-lookup"><span data-stu-id="70874-120">**Payment failed**</span></span>
- <span data-ttu-id="70874-121">**Skiptipöntun stofnuð**</span><span class="sxs-lookup"><span data-stu-id="70874-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="70874-122">Skilgreina sniðmát fyrir tölvupóst fyrir tiltekna afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="70874-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="70874-123">Þegar þetta ferli fer fram er gert ráð fyrir því að þú hafir þegar stofnað ný, sérsniðin sniðmát fyrir tölvupóst og bætt þeim við síðuna **Sniðmát fyrir tölvupóst fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="70874-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="70874-124">Frekari upplýsingar um hvernig á að búa til og hlaða upp sniðmátum fyrir tölvupóst er að finna í [Stofna sniðmát fyrir tölvupóst fyrir færslutilvik](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="70874-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="70874-125">Fylgdu eftirfarandi skrefum til að skilgreina sniðmát fyrir tölvupóst fyrir tiltekna afhendingarmáta í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="70874-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="70874-126">Opnaðu **Forstilling tilkynningar í tölvupósti fyrir Commerce**.</span><span class="sxs-lookup"><span data-stu-id="70874-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="70874-127">Fyrir neðan **Tilkynningastillingar smásölutilvika** skaltu velja núverandi tilkynningargerð.</span><span class="sxs-lookup"><span data-stu-id="70874-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="70874-128">Á meðan tilkynningagerð er enn valin skal velja **Skilgreina afhendingarmáta**.</span><span class="sxs-lookup"><span data-stu-id="70874-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="70874-129">Í svarglugganum **Afhendingarmátar** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="70874-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="70874-130">Í nýju línunni í svæðinu **Afhendingarmáti** skal velja afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="70874-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="70874-131">Í svæðinu **Kenni tölvupósts** skal velja sniðmát fyrir tölvupóst sem skal varpa á afhendingarmátann.</span><span class="sxs-lookup"><span data-stu-id="70874-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="70874-132">Velja skal gátreitinn **Virkt** .</span><span class="sxs-lookup"><span data-stu-id="70874-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="70874-133">Endurtakið skref 4 til 7 til að bæta við fleiri afhendingarmátum.</span><span class="sxs-lookup"><span data-stu-id="70874-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="70874-134">Þegar þessu er lokið skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="70874-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="70874-135">Þegar fleiri en einn afhendingarmáti er til staðar á milli lína í sölupöntun verður sjálfgefið sniðmát notað.</span><span class="sxs-lookup"><span data-stu-id="70874-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="70874-136">Sjálfgefið sniðmát er sniðmátið sem er varpað er á tilkynningagerðina á síðunni **Forstilling tilkynningar í tölvupósti fyrir Commerce**.</span><span class="sxs-lookup"><span data-stu-id="70874-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="70874-137">Þegar sölupöntun er með afhendingarmáta sem hefur ekki verið skilgreindur fyrir sérsniðið sniðmát fyrir tölvupóst, verður sjálfgefna sniðmátið fyrir tölvupóst notað.</span><span class="sxs-lookup"><span data-stu-id="70874-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70874-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="70874-138">Additional resources</span></span>

[<span data-ttu-id="70874-139">Stofna símaverspantanir</span><span class="sxs-lookup"><span data-stu-id="70874-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="70874-140">Breyta afhendingarmáta á sölustað</span><span class="sxs-lookup"><span data-stu-id="70874-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)
