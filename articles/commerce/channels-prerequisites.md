---
title: Skilyrði fyrir rásauppsetningu
description: Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0705efac4659f96ebca1c67f6f0ab8d23c99d81e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997701"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="77da9-103">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="77da9-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="77da9-104">Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="77da9-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="77da9-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="77da9-105">Overview</span></span>

<span data-ttu-id="77da9-106">Áður en hægt er að stofna rás í Dynamics 365 Commerce verður nokkrum nauðsynlegum verkum að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="77da9-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="77da9-107">Eftirfarandi listar með forsenduverkum eru skipulagðir eftir gerð rásar.</span><span class="sxs-lookup"><span data-stu-id="77da9-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="77da9-108">Enn er verið að skrifa nokkur skjöl og tenglar verða uppfærðir þegar nýtt efni er birt.</span><span class="sxs-lookup"><span data-stu-id="77da9-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="77da9-109">Frumstilling</span><span class="sxs-lookup"><span data-stu-id="77da9-109">Initialization</span></span>

- [<span data-ttu-id="77da9-110">Frumstilla grunngögn</span><span class="sxs-lookup"><span data-stu-id="77da9-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="77da9-111">Altækar forsendur sem krafist er fyrir allar rásategundir</span><span class="sxs-lookup"><span data-stu-id="77da9-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="77da9-112">Skilgreina og stilla uppbyggingu lögaðila</span><span class="sxs-lookup"><span data-stu-id="77da9-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="77da9-113">Skilgreindu fyrirtækjastigveldið</span><span class="sxs-lookup"><span data-stu-id="77da9-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="77da9-114">Setja upp vöruhús</span><span class="sxs-lookup"><span data-stu-id="77da9-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="77da9-115">Stilla virðisaukaskatt</span><span class="sxs-lookup"><span data-stu-id="77da9-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="77da9-116">Setja upp forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="77da9-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="77da9-117">Setja upp númeraraðir</span><span class="sxs-lookup"><span data-stu-id="77da9-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="77da9-118">Settu upp sjálfgefna viðskiptavini og heimilisfangabók</span><span class="sxs-lookup"><span data-stu-id="77da9-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="77da9-119">Skilyrði fyrir rásum í Retail</span><span class="sxs-lookup"><span data-stu-id="77da9-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="77da9-120">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="77da9-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="77da9-121">Setja upp virknireglu f. smásölu</span><span class="sxs-lookup"><span data-stu-id="77da9-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="77da9-122">Setja upp heimilifangabók starfsmanna</span><span class="sxs-lookup"><span data-stu-id="77da9-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="77da9-123">Setja upp útlit afgreiðsluskjás</span><span class="sxs-lookup"><span data-stu-id="77da9-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="77da9-124">Setja upp vélbúnaðarstöð</span><span class="sxs-lookup"><span data-stu-id="77da9-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="77da9-125">Forsendur rásar símavers</span><span class="sxs-lookup"><span data-stu-id="77da9-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="77da9-126">Færibreytur símavers</span><span class="sxs-lookup"><span data-stu-id="77da9-126">Call center parameters</span></span>
- [<span data-ttu-id="77da9-127">Símaverspöntun og endurgreiðslumátar</span><span class="sxs-lookup"><span data-stu-id="77da9-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="77da9-128">Stillingar afhendingarmáta og gjalda símavers</span><span class="sxs-lookup"><span data-stu-id="77da9-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="77da9-129">Skilyrði netrásar</span><span class="sxs-lookup"><span data-stu-id="77da9-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="77da9-130">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="77da9-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="77da9-131">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="77da9-131">Additional resources</span></span>

[<span data-ttu-id="77da9-132">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="77da9-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="77da9-133">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="77da9-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="77da9-134">Setja upp stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="77da9-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="77da9-135">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="77da9-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="77da9-136">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="77da9-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="77da9-137">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="77da9-137">Set up an online channel</span></span>](channel-setup-online.md)
