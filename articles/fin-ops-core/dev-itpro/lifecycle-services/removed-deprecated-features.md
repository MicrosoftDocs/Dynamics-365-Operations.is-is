---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Lifecycle Services (LCS)
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Microsoft Dynamics Lifecycle Services (LCS).
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e583ec66f24940f44113433042f5e2340cf0f52c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748440"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="847c8-103">Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="847c8-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="847c8-104">Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða úreltir fyrir Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="847c8-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="847c8-105">*Fjarlægður* eiginleiki er ekki lengur tiltækur í þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="847c8-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="847c8-106">*Úreltur* eiginleiki er ekki í virkri þróun og kann að vera fjarlægður úr uppfærslum í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="847c8-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="847c8-107">Þessi listi er veittur svo að þú getir íhugað þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="847c8-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="847c8-108">Október 2019 tilkynningar</span><span class="sxs-lookup"><span data-stu-id="847c8-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="847c8-109">Skýringarmyndir flæðirita í viðskiptaferlavinnslu</span><span class="sxs-lookup"><span data-stu-id="847c8-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="847c8-110"><strong>Ástæða úreldingar/fjarlægingar</strong></span><span class="sxs-lookup"><span data-stu-id="847c8-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="847c8-111">Við erum að afskrifa flæðirit í Viðskiptaferlavinnslu (BPM) vegna þess að eldri hönnun olli litlum notum.</span><span class="sxs-lookup"><span data-stu-id="847c8-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="847c8-112"><strong>Skipt út fyrir aðra eiginleika?</strong></span><span class="sxs-lookup"><span data-stu-id="847c8-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="847c8-113">Nr</span><span class="sxs-lookup"><span data-stu-id="847c8-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="847c8-114"><strong>Svæði sem verða fyrir áhrifum</strong></span><span class="sxs-lookup"><span data-stu-id="847c8-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="847c8-115">Viðskiptaferlavinnsla</span><span class="sxs-lookup"><span data-stu-id="847c8-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="847c8-116"><strong>Staða</strong></span><span class="sxs-lookup"><span data-stu-id="847c8-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="847c8-117">Úrelt: Gert er ráð fyrir að flæðirit skýringarmyndar í BPM verði fjarlægt í febrúar 2020.</span><span class="sxs-lookup"><span data-stu-id="847c8-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="847c8-118">Eftirfarandi aðgerðir verða ekki tiltækar:</span><span class="sxs-lookup"><span data-stu-id="847c8-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="847c8-119">Öll flæðirit verða skrifvarin og ekki hægt að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="847c8-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="847c8-120">Eiginleikar forms sem tengjast flæðiritaraðgerðum verða einnig ekki tiltækir.</span><span class="sxs-lookup"><span data-stu-id="847c8-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="847c8-121">Þessi flæðirit eru bæði með sjálfgefnum flæðiritum sem eru sjálfkrafa mynduð og sérsniðin flæðirit sem er breytt miðað við þessi sjálfgefnu flæðirit.</span><span class="sxs-lookup"><span data-stu-id="847c8-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="847c8-122">Öll stig ferlisins verða skrifvarin og ekki hægt að breyta þeim.</span><span class="sxs-lookup"><span data-stu-id="847c8-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="847c8-123">Eldri eiginleikinn hæfni/gloppugreining verður ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="847c8-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="847c8-124">Þess vegna verður enginn gloppulisti búinn til sjálfkrafa eða fáanlegur til útflutnings.</span><span class="sxs-lookup"><span data-stu-id="847c8-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="847c8-125"><strong>Athugasemd:</strong> Þessi aðgerð hafði áður verið úrelt og skipt út fyrir Microsoft Azure DevOps-samþættingar.</span><span class="sxs-lookup"><span data-stu-id="847c8-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="847c8-126">Útgáfusaga flæðiritsins verður ekki tiltæk.</span><span class="sxs-lookup"><span data-stu-id="847c8-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]