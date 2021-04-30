---
title: Mynda og yfirfara launaaðila
description: Þetta efnisatriði lýsir því hvernig á að mynda og yfirfara launaeiningar.
author: andreabichsel
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6e043498d4e36e38575a16c6475a5edfef51fc6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882007"
---
# <a name="generate-payroll-entities"></a><span data-ttu-id="435bc-103">Mynda launaeiningar</span><span class="sxs-lookup"><span data-stu-id="435bc-103">Generate payroll entities</span></span>

<span data-ttu-id="435bc-104">Notið þessa OData-aðgerð til að mynda einingar sem þarf fyrir launasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="435bc-104">Use this OData function to generate the entities needed for payroll integration.</span></span> <span data-ttu-id="435bc-105">Ef einhverjar breytingar eru gerðar á þessum einingum í Human Resources, t.d. sérstilltum reitum bætt við, verður hægt að kalla aftur á þessa aðgerð til að endurhlaða lýsigögn hverrar einingar.</span><span class="sxs-lookup"><span data-stu-id="435bc-105">If any changes are made to these entities in Human Resources, such as adding custom fields, this function can be called again to refresh the metadata of each entity.</span></span> <span data-ttu-id="435bc-106">Svarið inniheldur auðkenni aðgerðar sem hægt er að fylgjast með þannig að vitað sé hvenær myndunferlinu lýkur.</span><span class="sxs-lookup"><span data-stu-id="435bc-106">The response contains an operation ID that you can monitor so you know when the generation process has completed.</span></span>

<span data-ttu-id="435bc-107">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="435bc-107">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/RefreshHumanResourcesVirtualEntities
```

<span data-ttu-id="435bc-108">**body**</span><span class="sxs-lookup"><span data-stu-id="435bc-108">**body**</span></span>

```json
{
    "PhysicalNames" : ["PayrollEmployeeEntity", "HcmWorkerBaseEntity", "PayrollPositionEntity", "PayrollPositionJobEntity", "PayrollWorkerAddressEntity", "HcmJobDetailEntity", "HcmCompFixedPlanTableEntity", "PayrollFixedCompensationPlanEntity", "HcmEmploymentDetailEntity"]
}
```

<span data-ttu-id="435bc-109">**Svar**</span><span class="sxs-lookup"><span data-stu-id="435bc-109">**Response**</span></span>

```json
{
    "AsyncOperationId": "8b98d338-f939-4c86-9a91-80b76b6ab2ea"
}
```

## <a name="review-payroll-entities"></a><span data-ttu-id="435bc-110">Yfirfara launaeiningar</span><span class="sxs-lookup"><span data-stu-id="435bc-110">Review payroll entities</span></span>

<span data-ttu-id="435bc-111">Notið þetta API til að sækja lista yfir einingarnar sem tekist hefur að mynda og eru tilbúnar til notkunar.</span><span class="sxs-lookup"><span data-stu-id="435bc-111">Use this API to retrieve a list of the entities that have been successfully generated and are ready for use.</span></span>

<span data-ttu-id="435bc-112">**Beiðni**</span><span class="sxs-lookup"><span data-stu-id="435bc-112">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hrvirtualentitycatalogs?$filter=mshr_hasbeengenerated eq true
```

<span data-ttu-id="435bc-113">**Svar**</span><span class="sxs-lookup"><span data-stu-id="435bc-113">**Response**</span></span>

```json
{
      "value": [
        {
            "mshr_physicalname": "PayrollWorkerAddressEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-1c00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmJobDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6400-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmCompFixedPlanTableEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6b00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollEmployeeEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6d00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmEmploymentDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-7e00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollFixedCompensationPlanEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-9300-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmWorkerBaseEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-c000-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollPositionJobEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-e700-005001000000",
            "mshr_refresh": null
        }
    ]
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]