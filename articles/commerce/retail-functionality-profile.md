---
title: Stofna virknireglu fyrir smásölu
description: Þetta efnisatriði lýsir því hvernig á að búa til virkniforstillingar í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413029"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="55658-103">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="55658-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="55658-104">Þetta efnisatriði lýsir því hvernig á að búa til virkniforstillingar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="55658-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="55658-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="55658-105">Overview</span></span>

<span data-ttu-id="55658-106">Forstillingar viðskiptavirkni veita ýmsar stillingar sem notaðar eru fyrir netrásir.</span><span class="sxs-lookup"><span data-stu-id="55658-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="55658-107">Hver rás verður að tilgreina virknireglu.</span><span class="sxs-lookup"><span data-stu-id="55658-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="55658-108">Stofna virkniforstillingu</span><span class="sxs-lookup"><span data-stu-id="55658-108">Create a functionality profile</span></span>

<span data-ttu-id="55658-109">Til að stofna virknireglu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="55658-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="55658-110">Farðu í **Einingar \> Uppsetning rásar \> POS-virknireglur \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="55658-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="55658-111">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="55658-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="55658-112">Í reitinn **Prófíll**, slærðu inn auðkenni fyrir sniðið („FN006” í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="55658-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="55658-113">Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="55658-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="55658-114">Í kaflanum **Almennt**, veldu land fyrir **ISO** landstig.</span><span class="sxs-lookup"><span data-stu-id="55658-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="55658-115">Í kaflanum **Almennt**, breyttu öðrum stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="55658-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="55658-116">Í kaflanum **Almennt**, veldu **Kenni kvittunarforstillingar** fyrir kvittanir í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="55658-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="55658-117">Í kaflanum **Aðgerðir**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="55658-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="55658-118">Í kaflanum **Upphæð**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="55658-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="55658-119">Í kaflanum **Upplýsingakóðar**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="55658-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="55658-120">Í kaflanum **Kvittananúmer**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="55658-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="55658-121">Eftirfarandi mynd sýnir dæmi um virknireglu.</span><span class="sxs-lookup"><span data-stu-id="55658-121">The following image shows an example functionality profile.</span></span>
  
![Virknireglur fyrir forstillingu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="55658-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="55658-123">Additional resources</span></span>

[<span data-ttu-id="55658-124">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="55658-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="55658-125">Stofna nýja aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="55658-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="55658-126">Yfirlit skjáútlits</span><span class="sxs-lookup"><span data-stu-id="55658-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="55658-127">Skilgreina og setja upp Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="55658-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
