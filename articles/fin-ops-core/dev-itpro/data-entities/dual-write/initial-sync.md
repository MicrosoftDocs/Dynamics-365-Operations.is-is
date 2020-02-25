---
title: Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations forrit og Common Data Service
description: Þetta efni tilgreinir röð samstillingarinnar sem þú verður að fylgja til að búa til upphafsgögnin.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019840"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="5b1fb-103">Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations forrit og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5b1fb-103">Execution order for initial synchronization of Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="5b1fb-104">Áður en þú notar gagnasamþættingu verður þú að búa til fyrstu gögn sem krafist er fyrir viðskiptavini, lánardrottna og tengiliði.</span><span class="sxs-lookup"><span data-stu-id="5b1fb-104">Before you use data integration, you must create the initial data that is required for customers, vendors, and contacts.</span></span> <span data-ttu-id="5b1fb-105">Til dæmis viltu búa til nýtjan lið **Lánardrottnahóp** og stillir gildið **Greiðsluskilmála** á **Net30**.</span><span class="sxs-lookup"><span data-stu-id="5b1fb-105">For example, you want to create a new **Vendor group** item and set its **Terms of Payment** value to **Net30**.</span></span> <span data-ttu-id="5b1fb-106">Í þessu tilfelli, áður en þú reynir að búa til liðinn **Lánardrottnahóp** verður þú að ganga úr skugga um að **Net30** sé til í bæði forritinu og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5b1fb-106">In this case, before you try to create the **Vendor group** item, you must make sure that **Net30** exists in both the application and Common Data Service.</span></span> <span data-ttu-id="5b1fb-107">(Í framtíðinni mun Microsoft gefa út tvískipta verkvangsaðgerð sem kallast Upphafssamstilling. Þessi aðgerð mun gera staka samstillingu gagna milli forritsins og Common Data Service sem hluti af tvískiptu uppsetningunni.)</span><span class="sxs-lookup"><span data-stu-id="5b1fb-107">(In the future, Microsoft will release dual-write platform functionality that is named Initial Sync. This functionality will do a one-time data synchronization between the application and Common Data Service as part of the dual-write setup.)</span></span>

> [!TIP]
> <span data-ttu-id="5b1fb-108">Microsoft er að gefa út tvískipt kort fyrir öll tilvísunargögn, þ.m.t. **Greiðsluskilmála** (Greiðsluskilmálar).</span><span class="sxs-lookup"><span data-stu-id="5b1fb-108">Microsoft is releasing a dual-write map for all reference data, including **Terms of Payment** (payment terms).</span></span> <span data-ttu-id="5b1fb-109">Ef þú ert nú þegar með upphafsgögnin í einu kerfinu, getur lítil uppfærsluaðgerð á plötunni kallað fram tvískipt skrif á þá skrá.</span><span class="sxs-lookup"><span data-stu-id="5b1fb-109">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span>

<span data-ttu-id="5b1fb-110">Þú verður að fylgja eftirfarandi forgangsröð og ganga úr skugga um að upphafsgögnin séu aðgengileg í forritinu og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5b1fb-110">You must follow the following order of precedence and make sure that the initial data is available in the application and Common Data Service.</span></span>

## <a name="vendor"></a><span data-ttu-id="5b1fb-111">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="5b1fb-111">Vendor</span></span>

<span data-ttu-id="5b1fb-112">Hér er röð framkvæmdar fyrir eininguna **Lánardrottinn**:</span><span class="sxs-lookup"><span data-stu-id="5b1fb-112">Here is the order of execution for the **Vendor** entity:</span></span>

1. <span data-ttu-id="5b1fb-113">Lánardrottnaflokkur</span><span class="sxs-lookup"><span data-stu-id="5b1fb-113">Vendor group</span></span>

    1. <span data-ttu-id="5b1fb-114">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="5b1fb-114">Terms of payment</span></span>

        1. <span data-ttu-id="5b1fb-115">Greiðsludagur og línur</span><span class="sxs-lookup"><span data-stu-id="5b1fb-115">Payment day and lines</span></span>
        2. <span data-ttu-id="5b1fb-116">Greiðsluáætlun</span><span class="sxs-lookup"><span data-stu-id="5b1fb-116">Payment schedule</span></span>

2. <span data-ttu-id="5b1fb-117">Greiðsluháttur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="5b1fb-117">Vendor payment method</span></span>

## <a name="customer-organization"></a><span data-ttu-id="5b1fb-118">Viðskiptavinur (fyrirtæki)</span><span class="sxs-lookup"><span data-stu-id="5b1fb-118">Customer (Organization)</span></span>

<span data-ttu-id="5b1fb-119">Hér er röð framkvæmdar fyrir eininguna **Viðskiptavinur**:</span><span class="sxs-lookup"><span data-stu-id="5b1fb-119">Here is the order of execution for the **Customer** entity:</span></span>

1. <span data-ttu-id="5b1fb-120">Flokkur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="5b1fb-120">Customer group</span></span>

    1. <span data-ttu-id="5b1fb-121">Greiðsluskilmálar</span><span class="sxs-lookup"><span data-stu-id="5b1fb-121">Terms of payment</span></span>

        1. <span data-ttu-id="5b1fb-122">Greiðsludagur og línur</span><span class="sxs-lookup"><span data-stu-id="5b1fb-122">Payment day and lines</span></span>
        2. <span data-ttu-id="5b1fb-123">Greiðsla</span><span class="sxs-lookup"><span data-stu-id="5b1fb-123">Payment</span></span> 

2. <span data-ttu-id="5b1fb-124">Greiðslumáti viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="5b1fb-124">Customer payment method</span></span>

## <a name="contact-person"></a><span data-ttu-id="5b1fb-125">Tengiliður (Einstaklingur)</span><span class="sxs-lookup"><span data-stu-id="5b1fb-125">Contact (Person)</span></span>

<span data-ttu-id="5b1fb-126">Hér er röð framkvæmdar fyrir eininguna **Tengiliður**:</span><span class="sxs-lookup"><span data-stu-id="5b1fb-126">Here is the order of execution for the **Contact** entity:</span></span>

1. <span data-ttu-id="5b1fb-127">Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="5b1fb-127">Customer</span></span>
2. <span data-ttu-id="5b1fb-128">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="5b1fb-128">Vendor</span></span>
