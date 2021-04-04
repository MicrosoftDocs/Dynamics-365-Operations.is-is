---
title: Stofna virknireglu fyrir smásölu
description: Þetta efnisatriði lýsir hvernig á að stofna virknireglu í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478309"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="0655a-103">Stofna virknireglu fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="0655a-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0655a-104">Þetta efnisatriði lýsir hvernig á að stofna virknireglu í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0655a-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0655a-105">Forstillingar viðskiptavirkni veita ýmsar stillingar sem notaðar eru fyrir netrásir.</span><span class="sxs-lookup"><span data-stu-id="0655a-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="0655a-106">Hver rás verður að tilgreina virknireglu.</span><span class="sxs-lookup"><span data-stu-id="0655a-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="0655a-107">Stofna virkniforstillingu</span><span class="sxs-lookup"><span data-stu-id="0655a-107">Create a functionality profile</span></span>

<span data-ttu-id="0655a-108">Til að stofna virknireglu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0655a-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="0655a-109">Farðu í **Einingar \> Uppsetning rásar \> POS-virknireglur \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="0655a-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="0655a-110">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="0655a-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="0655a-111">Í reitinn **Prófíll**, slærðu inn auðkenni fyrir sniðið („FN006” í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="0655a-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="0655a-112">Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="0655a-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="0655a-113">Í kaflanum **Almennt**, veldu land fyrir **ISO** landstig.</span><span class="sxs-lookup"><span data-stu-id="0655a-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="0655a-114">Í kaflanum **Almennt**, breyttu öðrum stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0655a-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="0655a-115">Í kaflanum **Almennt**, veldu **Kenni kvittunarforstillingar** fyrir kvittanir í tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="0655a-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="0655a-116">Í kaflanum **Aðgerðir**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0655a-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="0655a-117">Í kaflanum **Upphæð**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0655a-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="0655a-118">Í kaflanum **Upplýsingakóðar**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0655a-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="0655a-119">Í kaflanum **Kvittananúmer**, breyttu stillingum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0655a-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="0655a-120">Eftirfarandi mynd sýnir dæmi um virknireglu.</span><span class="sxs-lookup"><span data-stu-id="0655a-120">The following image shows an example functionality profile.</span></span>
  
![Virknireglur fyrir forstillingu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="0655a-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0655a-122">Additional resources</span></span>

[<span data-ttu-id="0655a-123">Upplýsingakóðar og upplýsingakóðaflokkar</span><span class="sxs-lookup"><span data-stu-id="0655a-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="0655a-124">Stofna nýja aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="0655a-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="0655a-125">Yfirlit skjáútlits</span><span class="sxs-lookup"><span data-stu-id="0655a-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="0655a-126">Skilgreina og setja upp Retail Hardware Station</span><span class="sxs-lookup"><span data-stu-id="0655a-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
