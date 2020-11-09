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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997553"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="1bd2d-103">Skipta á milli lánardrottnahönnunar</span><span class="sxs-lookup"><span data-stu-id="1bd2d-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="1bd2d-104">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="1bd2d-104">Vendor data flow</span></span> 

<span data-ttu-id="1bd2d-105">Ef þú velur að nota eininguna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og eininguna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="1bd2d-106">Annars er ekki þörf á þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="1bd2d-107">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="1bd2d-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="1bd2d-108">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="1bd2d-109">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="1bd2d-110">Stofna lánardrottna í lyklaeiningu</span><span class="sxs-lookup"><span data-stu-id="1bd2d-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="1bd2d-111">Stofna lánardrottna í lánardrottnaeiningu</span><span class="sxs-lookup"><span data-stu-id="1bd2d-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="1bd2d-112">Uppfæra lánardrottna í lyklaeiningu</span><span class="sxs-lookup"><span data-stu-id="1bd2d-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="1bd2d-113">Uppfæra lánardrottna í lánardrottnaeiningu</span><span class="sxs-lookup"><span data-stu-id="1bd2d-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="1bd2d-114">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="1bd2d-115">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna í lyklaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="1bd2d-116">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-116">Then select **OK**.</span></span> <span data-ttu-id="1bd2d-117">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Stofna lánardrottna í verkflæðisferlis lyklaeiningar](media/create_process.png)

2. <span data-ttu-id="1bd2d-119">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna í lyklaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="1bd2d-120">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-120">Then select **OK**.</span></span> <span data-ttu-id="1bd2d-121">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="1bd2d-122">Stofnaðu verkflæðisferli fyrir eininguna **Lykill** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="1bd2d-123">Stofnaðu verkflæðisferli fyrir eininguna **Lykill** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="1bd2d-124">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="1bd2d-125">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. <span data-ttu-id="1bd2d-127">Virkjaðu verkflæðin sem þú stofnaðir fyrir einingarnar **Lykill** og **Lánardrottinn** til að hefja notkun á einingunni **Lykill** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="1bd2d-128">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="1bd2d-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="1bd2d-129">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="1bd2d-130">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="1bd2d-131">Búðu til lánardrottinn af gerðinni Einstaklingur í einingunni Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="1bd2d-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="1bd2d-132">Búðu til lánardrottinn af gerðinni Einstaklingur í einingunni Tengiliður</span><span class="sxs-lookup"><span data-stu-id="1bd2d-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="1bd2d-133">Uppfæra lánardrottinn af gerðinni Einstaklingur í einingunni Tengiliður</span><span class="sxs-lookup"><span data-stu-id="1bd2d-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="1bd2d-134">Uppfæra lánardrottinn af gerðinni Einstaklingur í einingunni Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="1bd2d-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="1bd2d-135">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="1bd2d-136">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Stofna lánardrottna af gerðinni Einstaklingur í tengiliðaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="1bd2d-137">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-137">Then select **OK**.</span></span> <span data-ttu-id="1bd2d-138">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="1bd2d-139">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu ferlissniðmát verkflæðis **Uppfæra lánardrottna af gerðinni Einstaklingur í tengiliðaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="1bd2d-140">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-140">Then select **OK**.</span></span> <span data-ttu-id="1bd2d-141">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="1bd2d-142">Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmátið **Stofna lánardrottna af gerðinni Einstaklingur í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="1bd2d-143">Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmátið **Uppfæra lánardrottna af gerðinni Einstaklingur í lánardrottnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="1bd2d-144">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="1bd2d-145">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="1bd2d-146">Virkjaðu verkflæðin sem þú stofnaðir í einingunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á einingunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="1bd2d-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
