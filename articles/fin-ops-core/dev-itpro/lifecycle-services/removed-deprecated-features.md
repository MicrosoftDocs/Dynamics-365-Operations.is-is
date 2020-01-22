---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Lifecycle Services (LCS)
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Microsoft Dynamics Lifecycle Services (LCS).
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885456"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="81af6-103">Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="81af6-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="81af6-104">Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða úreltir fyrir Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="81af6-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="81af6-105">*Fjarlægður* eiginleiki er ekki lengur tiltækur í þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="81af6-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="81af6-106">*Úreltur* eiginleiki er ekki í virkri þróun og kann að vera fjarlægður úr uppfærslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="81af6-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="81af6-107">Þessi listi er veittur svo að þú getir íhugað þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="81af6-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="81af6-108">Október 2019 tilkynningar</span><span class="sxs-lookup"><span data-stu-id="81af6-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="81af6-109">Skýringarmyndir flæðirita í viðskiptaferlavinnslu</span><span class="sxs-lookup"><span data-stu-id="81af6-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="81af6-110"><strong>Ástæða úreldingar/fjarlægingar</strong></span><span class="sxs-lookup"><span data-stu-id="81af6-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="81af6-111">Við erum að afskrifa flæðirit í Viðskiptaferlavinnslu (BPM) vegna þess að eldri hönnun olli litlum notum.</span><span class="sxs-lookup"><span data-stu-id="81af6-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81af6-112"><strong>Skipt út fyrir aðra eiginleika?</strong></span><span class="sxs-lookup"><span data-stu-id="81af6-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="81af6-113">Nr</span><span class="sxs-lookup"><span data-stu-id="81af6-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81af6-114"><strong>Svæði sem verða fyrir áhrifum</strong></span><span class="sxs-lookup"><span data-stu-id="81af6-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="81af6-115">Viðskiptaferlavinnsla</span><span class="sxs-lookup"><span data-stu-id="81af6-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81af6-116"><strong>Staða</strong></span><span class="sxs-lookup"><span data-stu-id="81af6-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="81af6-117">Úrelt: Gert er ráð fyrir að flæðirit skýringarmyndar í BPM verði fjarlægt í byrjun febrúar 2020.</span><span class="sxs-lookup"><span data-stu-id="81af6-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed by early February 2020.</span></span> <span data-ttu-id="81af6-118">Eftirfarandi virkni verður fjarlægð:</span><span class="sxs-lookup"><span data-stu-id="81af6-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="81af6-119">Núverandi flæðirit verða ekki tiltæk til að skoða eða breyta.</span><span class="sxs-lookup"><span data-stu-id="81af6-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="81af6-120">Formeiginleikarnir sem tengjast virkni flæðirita verða heldur ekki tiltækir, vegna þess að allur flipinn <strong>Flæðirit</strong> verður fjarlægður.</span><span class="sxs-lookup"><span data-stu-id="81af6-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="81af6-121">Þessi flæðirit eru bæði með sjálfgefnum flæðiritum sem eru sjálfkrafa mynduð og sérsniðin flæðirit sem er breytt miðað við þessi sjálfgefnu flæðirit.</span><span class="sxs-lookup"><span data-stu-id="81af6-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="81af6-122">Eldri eiginleikinn hæfni/gloppugreining verður ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="81af6-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="81af6-123">Þess vegna verður enginn gloppulisti búinn til sjálfkrafa eða fáanlegur til útflutnings.</span><span class="sxs-lookup"><span data-stu-id="81af6-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="81af6-124"><strong>Athugasemd:</strong> Þessi aðgerð hafði áður verið úrelt og skipt út fyrir Microsoft Azure DevOps-samþættingar.</span><span class="sxs-lookup"><span data-stu-id="81af6-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="81af6-125">Útgáfusaga flæðiritsins verður ekki tiltæk.</span><span class="sxs-lookup"><span data-stu-id="81af6-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
