---
title: Gerðir viðhaldsbeiðna
description: Þetta efni útskýrir hvernig á að setja upp gerðir viðhaldsbeiðna í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790505"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="08e3d-103">Gerðir viðhaldsbeiðna</span><span class="sxs-lookup"><span data-stu-id="08e3d-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="08e3d-104">Gerðir viðhaldsbeiðna eru notaðar til að flokka viðhaldsbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="08e3d-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="08e3d-105">Til dæmis gætir þú verið með tegundir viðhaldsbeiðna sem tengjast fyrirbyggjandi viðhaldi og leiðréttandi viðhaldi.</span><span class="sxs-lookup"><span data-stu-id="08e3d-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="08e3d-106">Eða þú gætir haft sérstaka tegund viðhaldsbeiðni sem er notuð til að stjórna viðgerðum á eignum (viðgerð á geymslu).</span><span class="sxs-lookup"><span data-stu-id="08e3d-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="08e3d-107">Gerð viðhaldsbeiðni skilgreinir tengsl við líftímastöðuhóp fyrir viðhaldsbeiðni (viðhaldslíftímalíkan).</span><span class="sxs-lookup"><span data-stu-id="08e3d-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="08e3d-108">Líftímalíkön viðhaldsbeiðni skilgreina líftímastöður sem hægt er að stilla fyrir viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="08e3d-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="08e3d-109">(Dæmi um lífshringrásarstig viðhalds eru **Stofnað**, **Virkur**, og **Klárað**.)</span><span class="sxs-lookup"><span data-stu-id="08e3d-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="08e3d-110">Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsbeiðnir** \> **Gerðir viðhaldsbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="08e3d-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="08e3d-111">Veldu **Nýtt** til að búa til gerð viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="08e3d-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="08e3d-112">Í reitnum **Gerð viðhaldsbeiðni**, sláðu inn auðkenni fyrir gerð viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="08e3d-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="08e3d-113">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="08e3d-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="08e3d-114">Á flýtiflipanum **Almennt**, í **Líftímalíkan viðhaldsbeiðni**, veldu líkan um líftíma viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="08e3d-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="08e3d-115">Í reitnum **Verkbeiðni** velurðu gerð verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="08e3d-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="08e3d-116">Þegar viðhaldsbeiðni er breytt í verkbeiðni fær verkbeiðnin sjálfkrafa þá gerð verkbeiðni sem tengist gerð viðhaldsbeiðninnar.</span><span class="sxs-lookup"><span data-stu-id="08e3d-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="08e3d-117">Eftirfarandi mynd sýnir dæmi um síðuna **Gerðir viðhaldsbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="08e3d-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Mynd 1](media/07-setup-for-requests.png)
