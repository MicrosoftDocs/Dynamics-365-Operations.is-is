---
title: Skipta á milli lánardrottnahönnunar
description: Þetta efni lýsir hvernig skuli skipta á milli samþættingar lánardrottnagagna milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173040"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="98861-103">Skipta á milli lánardrottnahönnunar</span><span class="sxs-lookup"><span data-stu-id="98861-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="98861-104">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="98861-104">Vendor data flow</span></span> 

<span data-ttu-id="98861-105">Ef þú velur að nota eininguna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og eininguna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="98861-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="98861-106">Annars er ekki þörf á þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="98861-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="98861-107">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="98861-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="98861-108">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="98861-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="98861-109">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="98861-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="98861-110">Stofna lánardrottna í lyklaeiningu</span><span class="sxs-lookup"><span data-stu-id="98861-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="98861-111">Stofna lánardrottna í lánardrottnaeiningu</span><span class="sxs-lookup"><span data-stu-id="98861-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="98861-112">Uppfæra lánardrottna í lyklaeiningu</span><span class="sxs-lookup"><span data-stu-id="98861-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="98861-113">Uppfæra lánardrottna í lánardrottnaeiningu</span><span class="sxs-lookup"><span data-stu-id="98861-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="98861-114">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="98861-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="98861-115">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna í lyklaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="98861-116">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="98861-116">Then select **OK**.</span></span> <span data-ttu-id="98861-117">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="98861-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Stofna lánardrottna í verkflæðisferlis lyklaeiningar](media/create_process.png)

2. <span data-ttu-id="98861-119">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna í lyklaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="98861-120">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="98861-120">Then select **OK**.</span></span> <span data-ttu-id="98861-121">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="98861-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="98861-122">Stofnaðu verkflæðisferli fyrir eininguna **Lykill** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="98861-123">Stofnaðu verkflæðisferli fyrir eininguna **Lykill** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="98861-124">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="98861-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="98861-125">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="98861-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. <span data-ttu-id="98861-127">Virkjaðu verkflæðin sem þú stofnaðir fyrir einingarnar **Lykill** og **Lánardrottinn** til að hefja notkun á einingunni **Lykill** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="98861-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="98861-128">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="98861-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="98861-129">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="98861-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="98861-130">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="98861-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="98861-131">Búðu til lánardrottinn af gerðinni Einstaklingur í einingunni Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="98861-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="98861-132">Búðu til lánardrottinn af gerðinni Einstaklingur í einingunni Tengiliður</span><span class="sxs-lookup"><span data-stu-id="98861-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="98861-133">Uppfæra lánardrottinn af gerðinni Einstaklingur í einingunni Tengiliður</span><span class="sxs-lookup"><span data-stu-id="98861-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="98861-134">Uppfæra lánardrottinn af gerðinni Einstaklingur í einingunni Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="98861-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="98861-135">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="98861-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="98861-136">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna af gerðinni Einstaklingur í tengiliðaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="98861-137">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="98861-137">Then select **OK**.</span></span> <span data-ttu-id="98861-138">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="98861-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="98861-139">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna af gerðinni Einstaklingur í tengiliðaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="98861-140">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="98861-140">Then select **OK**.</span></span> <span data-ttu-id="98861-141">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="98861-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="98861-142">Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmátið **Stofna lánardrottna af gerðinni Einstaklingur í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="98861-143">Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmátið **Uppfæra lánardrottna af gerðinni Einstaklingur í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="98861-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="98861-144">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="98861-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="98861-145">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="98861-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="98861-146">Virkjaðu verkflæðin sem þú stofnaðir í einingunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á einingunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="98861-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
