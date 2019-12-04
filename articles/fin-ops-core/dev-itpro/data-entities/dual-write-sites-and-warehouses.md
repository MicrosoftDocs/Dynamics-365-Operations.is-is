---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu svæðis- og vöruhúsgagna milli Finance and Operations og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770990"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="581e2-103">Innbyggð svæði og vöruhús</span><span class="sxs-lookup"><span data-stu-id="581e2-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="581e2-104">Þetta efni lýsir samþættingu svæðis- og vöruhúsgagna milli Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="581e2-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="581e2-105">Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="581e2-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="581e2-106">Þau eru notuð til að móta aðfangakeðju fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="581e2-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="581e2-107">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="581e2-107">Templates</span></span>

<span data-ttu-id="581e2-108">Með samþættingunni við Common Data Service eru þessi hugtök og allar tengdar upplýsingar fáanleg í Common Data Service með því að nota gagnaeiningar svæðanna og vöruhúsanna í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="581e2-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="581e2-109">Forrit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="581e2-109">Finance and Operations apps</span></span> | <span data-ttu-id="581e2-110">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="581e2-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="581e2-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="581e2-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="581e2-112">Svæði</span><span class="sxs-lookup"><span data-stu-id="581e2-112">Sites</span></span> | <span data-ttu-id="581e2-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="581e2-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="581e2-114">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="581e2-114">Warehouses</span></span> | <span data-ttu-id="581e2-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="581e2-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

