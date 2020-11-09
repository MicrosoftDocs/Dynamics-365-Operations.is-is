---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Common Data Service.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: d5c2030160f6025c9de63b2c29215364f5f87e6f
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997625"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="b1aa0-103">Samþætt svæði og vöruhús</span><span class="sxs-lookup"><span data-stu-id="b1aa0-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b1aa0-104">Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="b1aa0-105">Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="b1aa0-106">Þau eru notuð til að móta aðfangakeðju fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="b1aa0-107">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="b1aa0-107">Templates</span></span>

<span data-ttu-id="b1aa0-108">Með samþættingunni við Common Data Service eru þessi hugtök og allar tengdar upplýsingar fáanleg í Common Data Service með því að nota gagnaeiningar svæðanna og vöruhúsanna í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="b1aa0-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="b1aa0-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="b1aa0-109">Finance and Operations apps</span></span> | <span data-ttu-id="b1aa0-110">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="b1aa0-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="b1aa0-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b1aa0-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="b1aa0-112">Svæði</span><span class="sxs-lookup"><span data-stu-id="b1aa0-112">Sites</span></span> | <span data-ttu-id="b1aa0-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="b1aa0-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="b1aa0-114">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="b1aa0-114">Warehouses</span></span> | <span data-ttu-id="b1aa0-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="b1aa0-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]

