---
title: Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations og Common Data Service
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
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797299"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="e37f5-103">Framkvæmdapöntun fyrir fyrstu samstillingu Finance and Operations og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e37f5-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="e37f5-104">Áður en þú notar gagnasamþættingu verður þú að búa til fyrstu gögn sem krafist er fyrir viðskiptavini, lánardrottna og tengiliði.</span><span class="sxs-lookup"><span data-stu-id="e37f5-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="e37f5-105">Til dæmis ef þú vilt búa til nýjan lið **Lánardrottnahóp** og stilla **Greiðsluskilmála** hans á **Net30** þá þarftu, áður en þú reynir að stofna liðinn **Lánardrottnahóp** að ganga úr skugga um að **Net30** sé bæði til í Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e37f5-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="e37f5-106">(Í framtíðinni munum við gefa út tvískipta verkvangsaðgerð sem kallast **Upphafssamstilling**. Hún mun gera staka samstillingu gagna milli Finance and Operations og Common Data Service sem hluti af tvískiptu uppsetningunni.)</span><span class="sxs-lookup"><span data-stu-id="e37f5-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="e37f5-107">Ábending: Við gefum út tvískipt kort fyrir öll tilvísunargögn, þ.m.t. **Greiðsluskilmála** (Greiðsluskilmálar).</span><span class="sxs-lookup"><span data-stu-id="e37f5-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="e37f5-108">Ef þú ert nú þegar með upphafsgögnin í einu kerfinu, getur lítil uppfærsluaðgerð á plötunni kallað fram tvískipt skrif á þá skrá.</span><span class="sxs-lookup"><span data-stu-id="e37f5-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="e37f5-109">Þú verður að fylgja eftirfarandi forgangsröð og ganga úr skugga um að upphafsgögnin séu aðgengileg bæði varðandi Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="e37f5-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="e37f5-110">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="e37f5-110">Vendor</span></span>

<span data-ttu-id="e37f5-111">Röð framkvæmdar fyrir lánardrottinn er:</span><span class="sxs-lookup"><span data-stu-id="e37f5-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="e37f5-112">Viðskiptavinur (fyrirtæki)</span><span class="sxs-lookup"><span data-stu-id="e37f5-112">Customer (Organization)</span></span>

<span data-ttu-id="e37f5-113">Röð framkvæmdar fyrir viðskiptavin er:</span><span class="sxs-lookup"><span data-stu-id="e37f5-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="e37f5-114">Tengiliður (Einstaklingur)</span><span class="sxs-lookup"><span data-stu-id="e37f5-114">Contact (Person)</span></span>

<span data-ttu-id="e37f5-115">Röð framkvæmdar fyrir tengilið er:</span><span class="sxs-lookup"><span data-stu-id="e37f5-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
