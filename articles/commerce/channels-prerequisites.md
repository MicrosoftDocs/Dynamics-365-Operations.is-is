---
title: Skilyrði fyrir rásauppsetningu
description: Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002290"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="6ffb2-103">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="6ffb2-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ffb2-104">Þetta efni birtir yfirlit yfir forsendur fyrir uppsetningu rása í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6ffb2-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6ffb2-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6ffb2-105">Overview</span></span>

<span data-ttu-id="6ffb2-106">Áður en hægt er að stofna rás í Dynamics 365 Commerce verður nokkrum nauðsynlegum verkum að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="6ffb2-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="6ffb2-107">Eftirfarandi listar með forsenduverkum eru skipulagðir eftir gerð rásar.</span><span class="sxs-lookup"><span data-stu-id="6ffb2-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="6ffb2-108">Enn er verið að skrifa nokkur skjöl og tenglar verða uppfærðir þegar nýtt efni er birt.</span><span class="sxs-lookup"><span data-stu-id="6ffb2-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="6ffb2-109">Frumstilling</span><span class="sxs-lookup"><span data-stu-id="6ffb2-109">Initialization</span></span>

- [<span data-ttu-id="6ffb2-110">Frumstilla grunngögn</span><span class="sxs-lookup"><span data-stu-id="6ffb2-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="6ffb2-111">Altækar forsendur sem krafist er fyrir allar rásategundir</span><span class="sxs-lookup"><span data-stu-id="6ffb2-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="6ffb2-112">Skilgreina og stilla uppbyggingu lögaðila</span><span class="sxs-lookup"><span data-stu-id="6ffb2-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="6ffb2-113">Skilgreindu fyrirtækjastigveldið</span><span class="sxs-lookup"><span data-stu-id="6ffb2-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="6ffb2-114">Setja upp vöruhús</span><span class="sxs-lookup"><span data-stu-id="6ffb2-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="6ffb2-115">Stilla virðisaukaskatt</span><span class="sxs-lookup"><span data-stu-id="6ffb2-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6ffb2-116">Setja upp forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="6ffb2-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="6ffb2-117">Setja upp númeraraðir</span><span class="sxs-lookup"><span data-stu-id="6ffb2-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6ffb2-118">Settu upp sjálfgefna viðskiptavini og heimilisfangabók</span><span class="sxs-lookup"><span data-stu-id="6ffb2-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="6ffb2-119">Skilyrði fyrir rásum í Retail</span><span class="sxs-lookup"><span data-stu-id="6ffb2-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="6ffb2-120">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="6ffb2-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6ffb2-121">Setja upp virknireglu f. smásölu</span><span class="sxs-lookup"><span data-stu-id="6ffb2-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="6ffb2-122">Setja upp heimilifangabók starfsmanna</span><span class="sxs-lookup"><span data-stu-id="6ffb2-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="6ffb2-123">Setja upp útlit afgreiðsluskjás</span><span class="sxs-lookup"><span data-stu-id="6ffb2-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6ffb2-124">Setja upp vélbúnaðarstöð</span><span class="sxs-lookup"><span data-stu-id="6ffb2-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="6ffb2-125">Forsendur rásar símavers</span><span class="sxs-lookup"><span data-stu-id="6ffb2-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="6ffb2-126">Færibreytur símavers</span><span class="sxs-lookup"><span data-stu-id="6ffb2-126">Call center parameters</span></span>
- <span data-ttu-id="6ffb2-127">Endurgreiðslumátar símavers</span><span class="sxs-lookup"><span data-stu-id="6ffb2-127">Call center refund methods</span></span>
- <span data-ttu-id="6ffb2-128">Leigugerð</span><span class="sxs-lookup"><span data-stu-id="6ffb2-128">Rental types</span></span>
- <span data-ttu-id="6ffb2-129">Greiðsluþjónustur</span><span class="sxs-lookup"><span data-stu-id="6ffb2-129">Payment services</span></span>
- <span data-ttu-id="6ffb2-130">Biðkóðar pantana</span><span class="sxs-lookup"><span data-stu-id="6ffb2-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="6ffb2-131">Skilyrði fyrir netrásum</span><span class="sxs-lookup"><span data-stu-id="6ffb2-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="6ffb2-132">Stofna virknireglu fyrir netverslun.</span><span class="sxs-lookup"><span data-stu-id="6ffb2-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="6ffb2-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6ffb2-133">Additional resources</span></span>

[<span data-ttu-id="6ffb2-134">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="6ffb2-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6ffb2-135">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="6ffb2-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6ffb2-136">Setja upp stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="6ffb2-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="6ffb2-137">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="6ffb2-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="6ffb2-138">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="6ffb2-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6ffb2-139">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="6ffb2-139">Set up an online channel</span></span>](channel-setup-online.md)
