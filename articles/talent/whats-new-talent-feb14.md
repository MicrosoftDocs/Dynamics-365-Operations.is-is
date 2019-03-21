---
title: Hvað er nýtt eða breytt í Dynamics 365 for Talent (14. febrúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5f96dd60652705de820e0661d417dcaee8143561
ms.sourcegitcommit: 5384200c3e33510c5b3ac31f2b22443e1076251f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/14/2019
ms.locfileid: "390666"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="352ac-103">Hvað er nýtt eða breytt í Dynamics 365 for Talent (14. febrúar 2019)</span><span class="sxs-lookup"><span data-stu-id="352ac-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="352ac-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Talent.</span><span class="sxs-lookup"><span data-stu-id="352ac-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="352ac-105">Breytingar í Attract</span><span class="sxs-lookup"><span data-stu-id="352ac-105">Changes in Attract</span></span>
<span data-ttu-id="352ac-106">Það eru minniháttar villuleiðréttingar með í þessari útgáfu.</span><span class="sxs-lookup"><span data-stu-id="352ac-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="352ac-107">Breytingar á nýliðun</span><span class="sxs-lookup"><span data-stu-id="352ac-107">Changes in Onboarding</span></span>
<span data-ttu-id="352ac-108">Það eru minniháttar villuleiðréttingar með í þessari útgáfu.</span><span class="sxs-lookup"><span data-stu-id="352ac-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="352ac-109">Breytingar í Core HR</span><span class="sxs-lookup"><span data-stu-id="352ac-109">Changes in Core HR</span></span> 
<span data-ttu-id="352ac-110">**Smíði 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="352ac-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="352ac-111">Einingin fyrir föst laun starfsmanns flytur ekki út allar færslur</span><span class="sxs-lookup"><span data-stu-id="352ac-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="352ac-112">Með þessari breytingu mun einingin **Föst laun starfsmanns** núna flytja út allar færslur.</span><span class="sxs-lookup"><span data-stu-id="352ac-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="352ac-113">Eininguna er hægt að nota til að búa til og uppfæra núverandi færslur fyrir föst laun starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="352ac-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="352ac-114">Lokadagur ráðningar tekur ekki tillit til æskilegrar stillingar á tímabelti starfsmanns</span><span class="sxs-lookup"><span data-stu-id="352ac-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="352ac-115">Lokadagar ráðningar taka nú tillit til tímabeltis sem notandi kýs þegar ráðning er búin til eða kláruð hjá fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="352ac-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="352ac-116">Bresk aðsetur birtast í Analytics sem austur-svissnesk aðsetur</span><span class="sxs-lookup"><span data-stu-id="352ac-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="352ac-117">Í þessari útgáfu hefur breyting verið gerð til að leiðrétta skekkju í aðsetrum í **Starfsmannastjórnun**, skýrslunni „Starfsmannafjöldi eftir staðsetningu“.</span><span class="sxs-lookup"><span data-stu-id="352ac-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="352ac-118">Starfslokakóði er ekki fylltur út í stöðuverkefnaskrám starfsmanns þegar stöðunni er lokað</span><span class="sxs-lookup"><span data-stu-id="352ac-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="352ac-119">Breyting hefur verið gerð svo ástæðukóði starfsloka verði sjálfgefinn þegar stöðuverkefni starfsmanns er lokað.</span><span class="sxs-lookup"><span data-stu-id="352ac-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="352ac-120">Ný eining búin til fyrir launastig starfs</span><span class="sxs-lookup"><span data-stu-id="352ac-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="352ac-121">Ný eining fyrir gagnastjórnunarramma (DMF) var búin til.</span><span class="sxs-lookup"><span data-stu-id="352ac-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="352ac-122">Einingin gerir kleift að búa til og uppfæra launastig, markaðsvirði og upplýsingar könnunar fyrir hvert starf sem er skilgreint í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="352ac-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
