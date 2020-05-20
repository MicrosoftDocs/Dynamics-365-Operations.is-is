---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í Dynamics 365 Supply Chain Management.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331249"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="ae5b3-103">Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="ae5b3-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae5b3-104">Þetta efni verður uppfært þegar nýir fjarlægðir eða úreltir eiginleikar eru skráðir fyrir Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="ae5b3-105">*Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="ae5b3-106">*Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="ae5b3-107">Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="ae5b3-108">Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="ae5b3-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="ae5b3-109">Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="ae5b3-110">Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Supply Chain Management 10.0.11 útgáfa</span><span class="sxs-lookup"><span data-stu-id="ae5b3-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="ae5b3-111">Notkun á aðaláætlunarvél fyrir innbyggða Supply Chain Management fyrir dreifingaraðstæður</span><span class="sxs-lookup"><span data-stu-id="ae5b3-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ae5b3-112">**Ástæða úreldingar/fjarlægingar**</span><span class="sxs-lookup"><span data-stu-id="ae5b3-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ae5b3-113">Til að auka afköst og draga úr álagi SQL-gagnagrunns við keyrslu aðaláætlunar er verið að skipta út grunnstillingu á Supply Chain Management vél fyrir fínstilling áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="ae5b3-114">Fínstilling áætlanagerðar gerir kleift að keyra hraða áætlanagerð sem jafnvel er hægt að framkvæma á skrifstofutíma.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="ae5b3-115">Þetta gerir skipuleggjendum kleift að bregðast tafarlaust við breytingum á eftirspurn eða áætlunarfæribreytum.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="ae5b3-116">**Skipt út fyrir aðra eiginleika?**</span><span class="sxs-lookup"><span data-stu-id="ae5b3-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ae5b3-117">Já, fínstilling áætlanagerðar kemur í stað núverandi aðaláætlunarvélar Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="ae5b3-118">**Afurðasvæði sem haft er áhrif á**</span><span class="sxs-lookup"><span data-stu-id="ae5b3-118">**Product areas affected**</span></span>         | <span data-ttu-id="ae5b3-119">Supply Chain Management - Aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="ae5b3-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="ae5b3-120">**Dreifingarvalkostur**</span><span class="sxs-lookup"><span data-stu-id="ae5b3-120">**Deployment option**</span></span>              | <span data-ttu-id="ae5b3-121">Aðeins ský.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-121">Cloud only.</span></span> <span data-ttu-id="ae5b3-122">Fínstilling áætlanagerðar er ekki studd með uppsetningu á staðnum.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="ae5b3-123">**Staða**</span><span class="sxs-lookup"><span data-stu-id="ae5b3-123">**Status**</span></span>                         | <span data-ttu-id="ae5b3-124">Úrelt.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-124">Deprecated.</span></span> <span data-ttu-id="ae5b3-125">Í apríl 2021 verða dreifingaraðstæður ekki lengur studdar með innbyggðri Dynamics 365 Supply Chain Management aðaláætlunarvél.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="ae5b3-126">Fyrir dreifingaraðstæður verða viðskiptavinir að nota fínstillingu áætlanagerðar fyrir útreikning aðaláætlunar.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="ae5b3-127">Nánari upplýsingar er að finna í [fylgiskjölum fínstillingar áætlanagerðar](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="ae5b3-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="ae5b3-128">Viðskiptavinir með uppsetningu á staðnum á Dynamics 365 Supply Chain Management geta haldið áfram að nota aðaláætlunarvél Supply Chain Management fyrir dreifingaraðstæður eftir apríl 2021.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="ae5b3-129">Ekki verður boðið upp á fleiri umbætur á eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="ae5b3-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="ae5b3-130">Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir</span><span class="sxs-lookup"><span data-stu-id="ae5b3-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="ae5b3-131">Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="ae5b3-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
