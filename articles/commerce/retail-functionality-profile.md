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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a53fc77a7d457534428929bd431175be7cf450f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979648"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="fe499-103">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="fe499-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fe499-104">Þetta efnisatriði lýsir því hvernig á að búa til virkniforstillingar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe499-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fe499-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="fe499-105">Overview</span></span>

<span data-ttu-id="fe499-106">Forstillingar viðskiptavirkni veita ýmsar stillingar sem notaðar eru fyrir netrásir.</span><span class="sxs-lookup"><span data-stu-id="fe499-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="fe499-107">Hver rás verður að tilgreina virknireglu.</span><span class="sxs-lookup"><span data-stu-id="fe499-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="fe499-108">Stofna virkniforstillingu</span><span class="sxs-lookup"><span data-stu-id="fe499-108">Create a functionality profile</span></span>

<span data-ttu-id="fe499-109">Til að stofna virknireglu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="fe499-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="fe499-110">Farðu í **Einingar \> Uppsetning rásar \> POS-virknireglur \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="fe499-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="fe499-111">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="fe499-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe499-112">Í reitinn **Prófíll**, slærðu inn auðkenni fyrir sniðið („FN006” í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="fe499-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="fe499-113">Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="fe499-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="fe499-114">Í kaflanum **Almennt**, veldu land fyrir **ISO** landstig.</span><span class="sxs-lookup"><span data-stu-id="fe499-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="fe499-115">Í kaflanum **Almennt**, breyttu öðrum stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="fe499-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="fe499-116">Í kaflanum **Almennt**, veldu **Kenni kvittunarforstillingar** fyrir kvittanir í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="fe499-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="fe499-117">Í kaflanum **Aðgerðir**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="fe499-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="fe499-118">Í kaflanum **Upphæð**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="fe499-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="fe499-119">Í kaflanum **Upplýsingakóðar**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="fe499-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="fe499-120">Í kaflanum **Kvittananúmer**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="fe499-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="fe499-121">Eftirfarandi mynd sýnir dæmi um virknireglu.</span><span class="sxs-lookup"><span data-stu-id="fe499-121">The following image shows an example functionality profile.</span></span>
  
![Virknireglur fyrir forstillingu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="fe499-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fe499-123">Additional resources</span></span>

[<span data-ttu-id="fe499-124">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="fe499-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="fe499-125">Stofna nýja aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="fe499-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="fe499-126">Yfirlit skjáútlits</span><span class="sxs-lookup"><span data-stu-id="fe499-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="fe499-127">Skilgreina og setja upp Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="fe499-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
