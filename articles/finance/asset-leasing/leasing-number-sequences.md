---
title: Úthluta númeraröðum
description: Þetta efnisatriði útskýrir hvernig á að búa til númeraraðir fyrir kenni leigusamnings. Það útskýrir einnig hvernig á að búa til einkvæm kenni sem eru notuð í endurmatsferli vísitölu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3e89fb7616aff323d5815918a37e1fccf9b7f578
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207256"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="eb142-104">Úthluta númeraröðum</span><span class="sxs-lookup"><span data-stu-id="eb142-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="eb142-105">Þetta efnisatriði útskýrir hvernig á að búa til númeraraðir fyrir kenni leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="eb142-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="eb142-106">Það útskýrir einnig hvernig á að búa til einkvæm kenni sem eru notuð í endurmatsferli vísitölu.</span><span class="sxs-lookup"><span data-stu-id="eb142-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="eb142-107">Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="eb142-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="eb142-108">Veljið hliðarflipann **Númeraraðir**.</span><span class="sxs-lookup"><span data-stu-id="eb142-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="eb142-109">Veljið **Númeraraðir** á hliðarstikunni.</span><span class="sxs-lookup"><span data-stu-id="eb142-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="eb142-110">Velja númeraröð fyrir tilvísun **Leigukenni**.</span><span class="sxs-lookup"><span data-stu-id="eb142-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="eb142-111">Þessi númeraröð verður notuð til að mynda einkvæmt kenni fyrir hvern leigusamning fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="eb142-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="eb142-112">Velja númeraröð fyrir tilvísun **Vinnslukennis**.</span><span class="sxs-lookup"><span data-stu-id="eb142-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="eb142-113">Þessi númeraröð verður notuð til að mynda einkvæmt kenni fyrir hvert endurmatsferli vísitölu.</span><span class="sxs-lookup"><span data-stu-id="eb142-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="eb142-114">Velja númeraröð fyrir tilvísun **Auðkenni riftunartillögu**.</span><span class="sxs-lookup"><span data-stu-id="eb142-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="eb142-115">Þessi númeraröð verður notuð til að mynda einkvæmt kenni fyrir hverja tillögu að riftun.</span><span class="sxs-lookup"><span data-stu-id="eb142-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]