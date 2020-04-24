---
title: Stofna verkbeiðnir úr viðhaldsbeiðnum
description: Þetta efni útskýrir hvernig á að stofna verkbeiðni úr viðhaldsbeiðni í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205208"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="ff0b1-103">Stofna verkbeiðnir úr viðhaldsbeiðnum</span><span class="sxs-lookup"><span data-stu-id="ff0b1-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="ff0b1-104">Eftir að þú hefur búið til viðhaldsbeiðnir geturðu auðveldlega umbreytt þeim í vinnupantanir.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="ff0b1-105">Þetta efni lýsir skjótustu leiðinni til að vinna með viðhaldsbeiðnir, uppfæra nokkrar viðhaldsbeiðnir á sama tíma og búa síðan til vinnupöntun fyrir nokkrar viðhaldsbeiðnir á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="ff0b1-106">Á síðunni **Virkar viðhaldsbeiðnir** eða **Mínar viðhaldsbeiðnir á virkri staðsetningu** geturðu líka unnið með eina viðhaldsbeiðni í einu og umbreytt einni viðhaldsbeiðni í vinnupöntun.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="ff0b1-107">Sérhver viðhaldsbeiðni getur tengst aðeins einni verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="ff0b1-108">Hins vegar geta margar viðhaldsbeiðnir verið með í einni verkbeiðni, jafnvel þó að viðhaldsbeiðnirnar hafi mismunandi eignir.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="ff0b1-109">Veldu **Eignastýring** \> **Sameiginlegt** \> **viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="ff0b1-110">Áður en þú getur búið til verkbeiðni úr viðhaldsbeiðnum, verðurðu að velja, að lágmarki, tegund viðhalds fyrir viðhaldsbeiðnir, og einnig afbrigði og viðskipti af viðhaldsvinnu, ef þessar upplýsingar eru viðeigandi.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="ff0b1-111">Í netskjánum geturðu auðveldlega uppfært upplýsingar vegna viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="ff0b1-112">Þegar þú ert tilbúinn að búa til verkbeiðni skaltu velja viðhaldsbeiðnirnar sem á að hafa í henni.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="ff0b1-113">Ef þú velur nokkrar viðhaldsbeiðnir til að umbreyta í verkbeiðni, verða bæði reiturinn **Eignir** og reiturinn **Gerð viðhaldsverks** að vera stilltir áður en þú stofnar verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="ff0b1-114">Ef þú velur eina viðhaldsbeiðni til að umbreyta í verkbeiðni, verður aðeins reiturinn **Eignir** verður að vera stilltur áður en þú stofnar verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="ff0b1-115">Hins vegar, þegar þú býrð til verkbeiðnina, getur þú valið viðhaldsverkefna gerð (og tengt viðhaldstegundarafbrigði og viðskipti, ef þessar upplýsingar eru viðeigandi) í valmyndinni **Búðu til vinnu röð**.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="ff0b1-116">Veldu **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-116">Select **Work order**.</span></span>
5. <span data-ttu-id="ff0b1-117">Í valmyndinni **Stofna verkbeiðni** stillirðu reitina og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="ff0b1-118">Skilaboðastika gæti tilkynnt þér að ný verkbeiðni hafi verið búin til.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="ff0b1-119">Að auki, þegar þú býrð til verkbeiðni sem er byggð á viðhaldsbeiðni, ef eignin sem er tengd viðhaldsbeiðninni er innifalin í ábyrgðarsamningi, tilkynnir skilaboðastikan þér um ábyrgðarsamninginn.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="ff0b1-120">Veldu **Eignastýring** \> **Sameiginlegt** \> **Verkbeiðni** \> **Allar verkbeiðnir**, og opnaðu nýju vinnupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ff0b1-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Opna nýja vinnupöntun](media/05-manage-maintenance-requests.png)

