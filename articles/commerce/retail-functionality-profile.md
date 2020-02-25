---
title: Stofna virknireglu fyrir smásölu
description: Þetta efnisatriði lýsir því hvernig á að búa til virkniforstillingar smásölu í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002844"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="46735-103">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="46735-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="46735-104">Þetta efnisatriði lýsir því hvernig á að búa til virkniforstillingar smásölu í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="46735-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="46735-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="46735-105">Overview</span></span>

<span data-ttu-id="46735-106">Smásöluvirkni sniðið veitir ýmsar stillingar sem notaðar eru fyrir netrásir.</span><span class="sxs-lookup"><span data-stu-id="46735-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="46735-107">Hver smásölurás verður að tilgreina virknireglu fyrir smásölu.</span><span class="sxs-lookup"><span data-stu-id="46735-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="46735-108">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="46735-108">Create a retail functionality profile</span></span>

<span data-ttu-id="46735-109">Til að stofna virknireglu smásölu, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="46735-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="46735-110">Farðu í **Einingar \> Uppsetning rásar \> POS-virknireglur \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="46735-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="46735-111">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="46735-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="46735-112">Í reitinn **Prófíll**, slærðu inn auðkenni fyrir sniðið („FN006” í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="46735-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="46735-113">Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="46735-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="46735-114">Í kaflanum **Almennt**, veldu land fyrir **ISO** landstig.</span><span class="sxs-lookup"><span data-stu-id="46735-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="46735-115">Í kaflanum **Almennt**, breyttu öðrum stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="46735-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="46735-116">Í kaflanum **Almennt**, veldu **Kenni kvittunarforstillingar** fyrir kvittanir í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="46735-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="46735-117">Í kaflanum **Aðgerðir**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="46735-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="46735-118">Í kaflanum **Upphæð**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="46735-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="46735-119">Í kaflanum **Upplýsingakóðar**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="46735-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="46735-120">Í kaflanum **Kvittananúmer**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="46735-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="46735-121">Eftirfarandi mynd sýnir dæmi um virknireglu smásölu.</span><span class="sxs-lookup"><span data-stu-id="46735-121">The following image shows an example retail functionality profile.</span></span>
  
![Dæmi um virknireglur smásölu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="46735-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="46735-123">Additional resources</span></span>

[<span data-ttu-id="46735-124">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="46735-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="46735-125">Stofna nýja aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="46735-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="46735-126">Yfirlit skjáútlits</span><span class="sxs-lookup"><span data-stu-id="46735-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="46735-127">Skilgreina og setja upp Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="46735-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
