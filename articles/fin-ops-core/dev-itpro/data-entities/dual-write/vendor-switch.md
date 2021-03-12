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
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744466"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="a662a-103">Skipta á milli lánardrottnahönnunar</span><span class="sxs-lookup"><span data-stu-id="a662a-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="a662a-104">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="a662a-104">Vendor data flow</span></span> 

<span data-ttu-id="a662a-105">Ef þú velur að nota töfluna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og töfluna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="a662a-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="a662a-106">Annars er ekki þörf á þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="a662a-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="a662a-107">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="a662a-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="a662a-108">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="a662a-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="a662a-109">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a662a-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="a662a-110">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="a662a-111">Stofna lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="a662a-112">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="a662a-113">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="a662a-114">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a662a-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="a662a-115">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í reikningstöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="a662a-116">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a662a-116">Then select **OK**.</span></span> <span data-ttu-id="a662a-117">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir töfluna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="a662a-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Stofna lánardrottna í reikningstöflu verkflæðisferlis](media/create_process.png)

2. <span data-ttu-id="a662a-119">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í reikningstöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="a662a-120">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a662a-120">Then select **OK**.</span></span> <span data-ttu-id="a662a-121">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir töfluna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="a662a-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="a662a-122">Stofnaðu verkflæðisferli fyrir töfluna **Reikningur** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í lánardrottnatöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="a662a-123">Stofnaðu verkflæðisferli fyrir töfluna **Reikningur** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í lánardrottnatöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="a662a-124">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="a662a-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="a662a-125">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="a662a-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. <span data-ttu-id="a662a-127">Virkjaðu verkflæðin sem þú stofnaðir fyrir töflurnar **Reikningur** og **Lánardrottinn** til að hefja notkun á töflunni **Reikningur** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="a662a-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="a662a-128">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="a662a-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="a662a-129">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="a662a-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="a662a-130">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a662a-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="a662a-131">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="a662a-132">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="a662a-133">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="a662a-134">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="a662a-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="a662a-135">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a662a-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="a662a-136">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="a662a-137">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a662a-137">Then select **OK**.</span></span> <span data-ttu-id="a662a-138">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir töfluna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="a662a-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="a662a-139">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="a662a-140">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a662a-140">Then select **OK**.</span></span> <span data-ttu-id="a662a-141">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir töfluna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="a662a-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="a662a-142">Stofnaðu verkflæðisferli fyrir töfluna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="a662a-143">Stofnaður verkflæðisferli fyrir töfluna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="a662a-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="a662a-144">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="a662a-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="a662a-145">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="a662a-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="a662a-146">Virkjaðu verkflæðin sem þú stofnaðir í töflunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á töflunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="a662a-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
