---
title: Grunnstilla færibreytur leyfis og fjarvista
description: Skilgreindu færibreytur Human Resources fyrir leyfi og fjarvistir í Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009393"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="08b20-103">Grunnstilla færibreytur leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="08b20-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="08b20-104">Áður en þú setur upp áætlanir um leyfi og fjarvistir í Dynamics 365 Human Resources, það er góð hugmynd að staðfesta stillingar fyrir allar skyldar færibreytur Human Resources, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="08b20-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="08b20-105">Númeraröð fyrir leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="08b20-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="08b20-106">Stillingar á Family and Medical Leave Act (lög um leyfi vegna fjölskyldu eða veikinda)</span><span class="sxs-lookup"><span data-stu-id="08b20-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="08b20-107">Stillingar fyrir sjálfsafgreiðslu starfsmanna vegna orlofs- og fjarverubeiðna</span><span class="sxs-lookup"><span data-stu-id="08b20-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="08b20-108">Færibreytur leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="08b20-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="08b20-109">Skoða og breyta færibreytum Human Resources</span><span class="sxs-lookup"><span data-stu-id="08b20-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="08b20-110">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="08b20-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="08b20-111">Undir **Skipulag**, veldu **Færirbreytur Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="08b20-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="08b20-112">Á **Númeraraðir** flipann, staðfestu **Númeraröð kóða** fyrir **Skildu eftir skilríki** og breyta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="08b20-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="08b20-113">Þessi stilling ákvarðar röðina sem notuð er til að úthluta sjálfkrafa skilríkjum til að skilja eftir beiðnir.</span><span class="sxs-lookup"><span data-stu-id="08b20-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="08b20-114">Á **FMLA** flipanum, staðfestu FMLA stillingarnar og breyttu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="08b20-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="08b20-115">Á **Sjálfsafgreiðsla starfsmanna** flipann, tilgreinir hvort stjórnendur geti slegið inn leyfi og fjarvistarbeiðnir fyrir hönd starfsmanna sinna.</span><span class="sxs-lookup"><span data-stu-id="08b20-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="08b20-116">Á **Leyfi og fjarvera** flipanum, staðfestu stillingarnar og breyttu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="08b20-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="08b20-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="08b20-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="08b20-118">Skilgreina færibreytur dagatals</span><span class="sxs-lookup"><span data-stu-id="08b20-118">Configure calendar parameters</span></span>

<span data-ttu-id="08b20-119">Ef þú hefur virkjað forskoðunareiginleikann Leyfi og fjarvistir, verður þú að stilla viðbótarstika.</span><span class="sxs-lookup"><span data-stu-id="08b20-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="08b20-120">Fyrir forskoðunarútgáfu þann 3. febrúar 2020 er aðeins **Beiðni um orlof** virkjaðar.</span><span class="sxs-lookup"><span data-stu-id="08b20-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="08b20-121">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="08b20-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="08b20-122">Undir **Skipulag**, veldu **Færirbreytur Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="08b20-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="08b20-123">Á **Dagatal** flipanum, skal breyta stillingu dagatals eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="08b20-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="08b20-124">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="08b20-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="08b20-125">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="08b20-125">See also</span></span>

- [<span data-ttu-id="08b20-126">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="08b20-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
