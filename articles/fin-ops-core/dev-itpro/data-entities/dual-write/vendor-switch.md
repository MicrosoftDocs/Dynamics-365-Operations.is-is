---
title: Skipta á milli lánardrottnahönnunar
description: Þetta efni lýsir hvernig skuli skipta á milli samþættingar lánardrottnagagna milli forrita Finance and Operations og Dataverse.
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
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685510"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="b9ac7-103">Skipta á milli lánardrottnahönnunar</span><span class="sxs-lookup"><span data-stu-id="b9ac7-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="b9ac7-104">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="b9ac7-104">Vendor data flow</span></span> 

<span data-ttu-id="b9ac7-105">Ef þú velur að nota eininguna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og eininguna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="b9ac7-106">Annars er ekki þörf á þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="b9ac7-107">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="b9ac7-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="b9ac7-108">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="b9ac7-109">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="b9ac7-110">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="b9ac7-111">Stofna lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="b9ac7-112">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="b9ac7-113">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="b9ac7-114">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="b9ac7-115">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í reikningstöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="b9ac7-116">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-116">Then select **OK**.</span></span> <span data-ttu-id="b9ac7-117">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Stofna lánardrottna í reikningstöflu verkflæðisferlis](media/create_process.png)

2. <span data-ttu-id="b9ac7-119">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í reikningstöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="b9ac7-120">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-120">Then select **OK**.</span></span> <span data-ttu-id="b9ac7-121">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="b9ac7-122">Stofnaðu verkflæðisferli fyrir eininguna **Reikningur** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í lánardrottnatöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="b9ac7-123">Stofnaðu verkflæðisferli fyrir eininguna **Reikningur** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í lánardrottnatöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="b9ac7-124">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="b9ac7-125">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. <span data-ttu-id="b9ac7-127">Virkjaðu verkflæðin sem þú stofnaðir fyrir töflurnar **Reikningur** og **Lánardrottinn** til að hefja notkun á einingunni **Reikningur** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="b9ac7-128">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="b9ac7-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="b9ac7-129">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="b9ac7-130">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="b9ac7-131">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="b9ac7-132">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="b9ac7-133">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="b9ac7-134">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="b9ac7-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="b9ac7-135">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="b9ac7-136">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="b9ac7-137">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-137">Then select **OK**.</span></span> <span data-ttu-id="b9ac7-138">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="b9ac7-139">Stofnaðu verkflæðisferli fyrir eininguna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="b9ac7-140">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-140">Then select **OK**.</span></span> <span data-ttu-id="b9ac7-141">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="b9ac7-142">Stofnaðu verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="b9ac7-143">Stofnaður verkflæðisferli fyrir eininguna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="b9ac7-144">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="b9ac7-145">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="b9ac7-146">Virkjaðu verkflæðin sem þú stofnaðir í töflunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á einingunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="b9ac7-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
