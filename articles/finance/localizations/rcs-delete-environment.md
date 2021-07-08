---
title: Regulatory Configuration Service (RCS) – Eyða RCS-umhverfi
description: Þetta efnisatriði útskýrir hvernig kerfisstjóri Regulatory Configuration Service (RCS) getur eytt RCS-umhverfi og tengdum gögnum.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295819"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="4db43-103">Regulatory Configuration Service (RCS) – Eyða RCS-umhverfi</span><span class="sxs-lookup"><span data-stu-id="4db43-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4db43-104">Þetta efnisatriði útskýrir hvernig kerfisstjóri Regulatory Configuration Service (RCS) getur eytt RCS-umhverfi og tengdum gögnum.</span><span class="sxs-lookup"><span data-stu-id="4db43-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="4db43-105">Áður en hægt er að klára ferlið í þessu efnisatriði þarf að uppfylla eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="4db43-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="4db43-106">Nauðsynlegt er að vera með hlutverkið **Kerfisstjóri** úthlutað fyrir RCS-umhverfið.</span><span class="sxs-lookup"><span data-stu-id="4db43-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="4db43-107">Hlutverkið **Kerfisstjóri** verður að vera með hlutverkið **RCSDeleteEnvironmentDuty** úthlutað.</span><span class="sxs-lookup"><span data-stu-id="4db43-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="4db43-108">Eyða RCS-umhverfi</span><span class="sxs-lookup"><span data-stu-id="4db43-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="4db43-109">Opnið RCS og veljið vinnusvæðið **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="4db43-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="4db43-110">Í hlutanum **Tengdir tenglar** skal velja **Eyða RCS-umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="4db43-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Eyða tengli RCS-umhverfis í hlutanum um tengda tengla](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="4db43-112">Í svarglugganum sem birtist skal yfirfara skilaboðin um umfang eyðingar á umhverfi.</span><span class="sxs-lookup"><span data-stu-id="4db43-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Skilaboð í svarglugganum Eyða RCS-umhverfi](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="4db43-114">Ekki er hægt að afturkalla eyðingu RCS-umhverfis.</span><span class="sxs-lookup"><span data-stu-id="4db43-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="4db43-115">Aðgerðin eyðir völdu RCS-umhverfi og tengdum gögnum, þar á meðal eiginleikum og grunnstillingum sem eru vistaðar í altækri geymslu.</span><span class="sxs-lookup"><span data-stu-id="4db43-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="4db43-116">Hætt verður að samnýta eiginleika og grunnstillingar sem er deilt með öðrum fyrirtækjum og þeim verður eytt ef þeir eru ekki tengdir við neitt.</span><span class="sxs-lookup"><span data-stu-id="4db43-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="4db43-117">Eiginleikar og grunnstillingar sem eru tengdar öðru verða merktar sem hætt í notkun.</span><span class="sxs-lookup"><span data-stu-id="4db43-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="4db43-118">Í reitnum sem er gefinn upp skal færa inn altækt einkvæmt kennimerki (GUID) fyrir RCS-umhverfið til að staðfesta að það eigi að eyða því.</span><span class="sxs-lookup"><span data-stu-id="4db43-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="4db43-119">GUID umhverfisins er með í skilaboðum um eyðingu.</span><span class="sxs-lookup"><span data-stu-id="4db43-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="4db43-120">Veljið **Eyða umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="4db43-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="4db43-121">RCS-umhverfinu þínu og öllum tengdum gögnum hefur nú verið eytt.</span><span class="sxs-lookup"><span data-stu-id="4db43-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4db43-122">Eftir að RCS-umhverfi er eytt er engin leið til að endurheimta gögnin.</span><span class="sxs-lookup"><span data-stu-id="4db43-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="4db43-123">Hægt er að búa til nýtt RCS-umhverfi á öllum tiltækum RCS-svæðum.</span><span class="sxs-lookup"><span data-stu-id="4db43-123">A new RCS environment can be created in any available RCS region.</span></span>
