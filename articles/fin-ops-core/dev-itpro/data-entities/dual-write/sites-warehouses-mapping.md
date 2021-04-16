---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Dataverse.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750667"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="1271f-103">Samþætt svæði og vöruhús</span><span class="sxs-lookup"><span data-stu-id="1271f-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1271f-104">Þetta efni lýsir samþættingu vefsvæðis- og vöruhússgagna milli Finance and Operations og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="1271f-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="1271f-105">Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1271f-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="1271f-106">Þau eru notuð til að móta aðfangakeðju fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="1271f-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="1271f-107">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="1271f-107">Templates</span></span>

<span data-ttu-id="1271f-108">Með samþættingu við Dataverse eru þessi hugtök og allar tengdar upplýsingar þeirra aðgengilegar í Dataverse með því að nota gagnatöflur fyrir svæði og vöruhús í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="1271f-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="1271f-109">Finance and Operations-smáforrit</span><span class="sxs-lookup"><span data-stu-id="1271f-109">Finance and Operations apps</span></span> | <span data-ttu-id="1271f-110">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="1271f-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="1271f-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="1271f-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="1271f-112">Svæði</span><span class="sxs-lookup"><span data-stu-id="1271f-112">Sites</span></span> | <span data-ttu-id="1271f-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="1271f-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="1271f-114">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="1271f-114">Warehouses</span></span> | <span data-ttu-id="1271f-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="1271f-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]