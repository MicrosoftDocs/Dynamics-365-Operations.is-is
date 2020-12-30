---
title: Setja upp stigveldi fyrirtækis
description: Þetta efni lýsir því hvernig á að setja upp stigveldi fyrirtækis í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413120"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="f94b4-103">Setja upp stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f94b4-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f94b4-104">Þetta efni lýsir því hvernig á að setja upp stigveldi fyrirtækis í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f94b4-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f94b4-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f94b4-105">Overview</span></span>

<span data-ttu-id="f94b4-106">Áður en þú býrð til rásir þarftu að tryggja að stigveldi fyrirtækis hafi verið sett upp.</span><span class="sxs-lookup"><span data-stu-id="f94b4-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="f94b4-107">Hægt er að nota stigveldi fyrirtækis til að skoða og gefa skýrslu um reksturinn frá ýmsum sjónarhornum.</span><span class="sxs-lookup"><span data-stu-id="f94b4-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="f94b4-108">Til dæmis er hægt að setja upp eitt stigveldi fyrir skattalega-, lagalega- eða lögboðna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f94b4-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="f94b4-109">Hægt að setja upp annað stigveldi til að gefa skýrslu um fjárhagslegar upplýsingar sem ekki er krafist samkvæmt lögum, en sem er notuð við innri skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f94b4-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="f94b4-110">Áður en hægt er að stofna stigveldi fyrirtækis þarf að stofna fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f94b4-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="f94b4-111">Nánari upplýsingar er að finna í [Stofna lögaðila](channels-legal-entities.md) eða [Stofna rekstrareiningar](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f94b4-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="f94b4-112">Frekari upplýsingar er hægt að finna í eftirfarandi efni.</span><span class="sxs-lookup"><span data-stu-id="f94b4-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="f94b4-113">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="f94b4-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="f94b4-114">Skipuleggja stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f94b4-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="f94b4-115">Stofna fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="f94b4-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="f94b4-116">Búa til stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="f94b4-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="f94b4-117">Til að stofna stigveldi fyrirtækis skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f94b4-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f94b4-118">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Stigveldi fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="f94b4-119">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f94b4-120">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f94b4-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="f94b4-121">Í kaflanum **Tilgangur** skal velja **Úthluta tilgangi**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="f94b4-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f94b4-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="f94b4-123">Veljið tilgangur sem úthluta á stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f94b4-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="f94b4-124">Í kaflanum **Úthlutuð stigveldi** skal velja **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="f94b4-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f94b4-125">In the list, mark the selected row.</span></span> <span data-ttu-id="f94b4-126">Finna stigveldið sem var verið að stofna.</span><span class="sxs-lookup"><span data-stu-id="f94b4-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="f94b4-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-127">Select **OK**.</span></span>

<span data-ttu-id="f94b4-128">Eftirfarandi mynd sýnir dæmi um skipulag stigveldis sem er búið til fyrir upphugsaðar verslanir „Adventure Works“.</span><span class="sxs-lookup"><span data-stu-id="f94b4-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Dæmi um stigveldi fyrirtækis](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="f94b4-130">Bæta við fyrirtækjum í stigveldi</span><span class="sxs-lookup"><span data-stu-id="f94b4-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="f94b4-131">Til að bæta fyrirtækjum við í stigveldi skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f94b4-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f94b4-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f94b4-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="f94b4-133">Velja skal þitt stigveldi.</span><span class="sxs-lookup"><span data-stu-id="f94b4-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="f94b4-134">Í aðgerðaglugganum velurðu **Skoða**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="f94b4-135">Bæta við fleiri fyrirtæki eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="f94b4-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="f94b4-136">Til að bæta fyrirtæki við velurðu **Breyta** og velur síðan **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="f94b4-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="f94b4-137">Þegar gerðar eru breytingar er hægt drög að vista og birta breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="f94b4-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="f94b4-138">Eftirfarandi mynd sýnir lögaðila sem er bætt við stigveldisrótina með fjórum kostnaðarmiðstöðvum bætt við fyrir „verslunarmiðstöð“, „sölustöð“, „net“ og „símaþjónustuver“.</span><span class="sxs-lookup"><span data-stu-id="f94b4-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="f94b4-139">Síðan er hægt að bæta við ýmsum smásölu-, síma- og netrásum.</span><span class="sxs-lookup"><span data-stu-id="f94b4-139">Various retail, call center and online channels can then be added to each.</span></span>

![Dæmi um hönnuð stigveldis](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="f94b4-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f94b4-141">Additional resources</span></span>

[<span data-ttu-id="f94b4-142">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="f94b4-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f94b4-143">Skipuleggja fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="f94b4-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f94b4-144">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="f94b4-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="f94b4-145">Stofna rekstrareiningar</span><span class="sxs-lookup"><span data-stu-id="f94b4-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="f94b4-146">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="f94b4-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f94b4-147">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="f94b4-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
