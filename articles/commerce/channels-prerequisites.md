---
title: Skilyrði fyrir rásauppsetningu
description: Þetta efnisatriði sýnir yfirlit yfir forsendur rásauppsetningar í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800520"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="33707-103">Skilyrði fyrir uppsetningu rásar</span><span class="sxs-lookup"><span data-stu-id="33707-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33707-104">Þetta efnisatriði sýnir yfirlit yfir forsendur rásaruppsetningar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="33707-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="33707-105">Áður en hægt er að stofna rás í Dynamics 365 Commerce verður nokkrum nauðsynlegum verkum að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="33707-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="33707-106">Eftirfarandi listar með forsenduverkum eru skipulagðir eftir gerð rásar.</span><span class="sxs-lookup"><span data-stu-id="33707-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="33707-107">Enn er verið að skrifa nokkur skjöl og tenglar verða uppfærðir þegar nýtt efni er birt.</span><span class="sxs-lookup"><span data-stu-id="33707-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="33707-108">Frumstilling</span><span class="sxs-lookup"><span data-stu-id="33707-108">Initialization</span></span>

- [<span data-ttu-id="33707-109">Frumstilla grunngögn</span><span class="sxs-lookup"><span data-stu-id="33707-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="33707-110">Altækar forsendur sem krafist er fyrir allar rásategundir</span><span class="sxs-lookup"><span data-stu-id="33707-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="33707-111">Skilgreina og stilla uppbyggingu lögaðila</span><span class="sxs-lookup"><span data-stu-id="33707-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="33707-112">Skilgreindu fyrirtækjastigveldið</span><span class="sxs-lookup"><span data-stu-id="33707-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="33707-113">Setja upp vöruhús</span><span class="sxs-lookup"><span data-stu-id="33707-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="33707-114">Stilla virðisaukaskatt</span><span class="sxs-lookup"><span data-stu-id="33707-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="33707-115">Setja upp forstillingu tilkynningar í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="33707-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="33707-116">Setja upp númeraraðir</span><span class="sxs-lookup"><span data-stu-id="33707-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="33707-117">Settu upp sjálfgefna viðskiptavini og heimilisfangabók</span><span class="sxs-lookup"><span data-stu-id="33707-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="33707-118">Skilyrði fyrir rásum í Retail</span><span class="sxs-lookup"><span data-stu-id="33707-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="33707-119">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="33707-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="33707-120">Setja upp virknireglu f. smásölu</span><span class="sxs-lookup"><span data-stu-id="33707-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="33707-121">Setja upp heimilifangabók starfsmanna</span><span class="sxs-lookup"><span data-stu-id="33707-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="33707-122">Setja upp útlit afgreiðsluskjás</span><span class="sxs-lookup"><span data-stu-id="33707-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="33707-123">Setja upp vélbúnaðarstöð</span><span class="sxs-lookup"><span data-stu-id="33707-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="33707-124">Forsendur rásar símavers</span><span class="sxs-lookup"><span data-stu-id="33707-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="33707-125">Færibreytur símavers</span><span class="sxs-lookup"><span data-stu-id="33707-125">Call center parameters</span></span>
- [<span data-ttu-id="33707-126">Símaverspöntun og endurgreiðslumátar</span><span class="sxs-lookup"><span data-stu-id="33707-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="33707-127">Stillingar afhendingarmáta og gjalda símavers</span><span class="sxs-lookup"><span data-stu-id="33707-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="33707-128">Skilyrði netrásar</span><span class="sxs-lookup"><span data-stu-id="33707-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="33707-129">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="33707-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="33707-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="33707-130">Additional resources</span></span>

[<span data-ttu-id="33707-131">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="33707-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="33707-132">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="33707-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="33707-133">Setja upp stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="33707-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="33707-134">Stofna lögaðila</span><span class="sxs-lookup"><span data-stu-id="33707-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="33707-135">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="33707-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="33707-136">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="33707-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
