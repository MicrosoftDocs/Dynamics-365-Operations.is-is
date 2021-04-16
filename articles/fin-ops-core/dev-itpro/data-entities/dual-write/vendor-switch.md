---
title: Skipta á milli lánardrottnahönnunar
description: Þetta efni lýsir hvernig skuli skipta á milli samþættingar lánardrottnagagna milli forrita Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750595"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="3c077-103">Skipta á milli lánardrottnahönnunar</span><span class="sxs-lookup"><span data-stu-id="3c077-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="3c077-104">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3c077-104">Vendor data flow</span></span> 

<span data-ttu-id="3c077-105">Ef þú velur að nota töfluna **Lykill** til að geyma lánardrottna af gerðinni **Fyrirtæki** og töfluna **Hafa samband** til að geyma lánardrottna af gerðinni **Einstaklingur** stillirðu eftirfarandi verkflæði.</span><span class="sxs-lookup"><span data-stu-id="3c077-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="3c077-106">Annars er ekki þörf á þessari stillingu.</span><span class="sxs-lookup"><span data-stu-id="3c077-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="3c077-107">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="3c077-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="3c077-108">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="3c077-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="3c077-109">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="3c077-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="3c077-110">Stofna lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="3c077-111">Stofna lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="3c077-112">Uppfæra lánardrottna í reikningstöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="3c077-113">Uppfæra lánardrottna í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="3c077-114">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3c077-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="3c077-115">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í reikningstöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="3c077-116">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3c077-116">Then select **OK**.</span></span> <span data-ttu-id="3c077-117">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir töfluna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="3c077-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Stofna lánardrottna í reikningstöflu verkflæðisferlis](media/create_process.png)

2. <span data-ttu-id="3c077-119">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í reikningstöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="3c077-120">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3c077-120">Then select **OK**.</span></span> <span data-ttu-id="3c077-121">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir töfluna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="3c077-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="3c077-122">Stofnaðu verkflæðisferli fyrir töfluna **Reikningur** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna í lánardrottnatöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="3c077-123">Stofnaðu verkflæðisferli fyrir töfluna **Reikningur** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna í lánardrottnatöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="3c077-124">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="3c077-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="3c077-125">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="3c077-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Hnappurinn Umbreyta í bakgrunnsverkflæði](media/background_workflow.png)

6. <span data-ttu-id="3c077-127">Virkjaðu verkflæðin sem þú stofnaðir fyrir töflurnar **Reikningur** og **Lánardrottinn** til að hefja notkun á töflunni **Reikningur** til að geyma upplýsingar um lánardrottna af gerðinni **Fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="3c077-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="3c077-128">Notaðu stækkaða lánardrottnahönnun fyrir framleiðendur af gerðinni Einstaklingur</span><span class="sxs-lookup"><span data-stu-id="3c077-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="3c077-129">Lausnapakkinn **Dynamics365FinanceExtended** inniheldur eftirfarandi sniðmát verkflæðisferla.</span><span class="sxs-lookup"><span data-stu-id="3c077-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="3c077-130">Þú verður að búa til verkflæði fyrir hvert sniðmát.</span><span class="sxs-lookup"><span data-stu-id="3c077-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="3c077-131">Stofna lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="3c077-132">Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="3c077-133">Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="3c077-134">Uppfæra lánardrottna af gerðinni einstaklingur í lánardrottnatöflu</span><span class="sxs-lookup"><span data-stu-id="3c077-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="3c077-135">Til að stofna nýja verkflæðisferla með ferlissniðmáti verkflæðis fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3c077-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="3c077-136">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="3c077-137">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3c077-137">Then select **OK**.</span></span> <span data-ttu-id="3c077-138">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir töfluna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="3c077-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="3c077-139">Stofnaðu verkflæðisferli fyrir töfluna **Lánardrottinn** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="3c077-140">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3c077-140">Then select **OK**.</span></span> <span data-ttu-id="3c077-141">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir töfluna **Tengiliður**.</span><span class="sxs-lookup"><span data-stu-id="3c077-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="3c077-142">Stofnaðu verkflæðisferli fyrir töfluna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Stofna lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="3c077-143">Stofnaður verkflæðisferli fyrir töfluna **Tengiliður** og veldu sniðmát verkflæðisferlisins **Uppfæra lánardrottna af gerðinni einstaklingur í tengiliðatöflu**.</span><span class="sxs-lookup"><span data-stu-id="3c077-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="3c077-144">Þú getur stillt verkflæði sem annaðhvort rauntíma- eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="3c077-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="3c077-145">Til að stilla verkflæði sem bakgrunnsflæði velurðu **Umbreyta í bakgrunnsverkflæði**.</span><span class="sxs-lookup"><span data-stu-id="3c077-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="3c077-146">Virkjaðu verkflæðin sem þú stofnaðir í töflunum **Tengiliður** og **Lánardrottinn** til að hefja notkun á töflunni **Tengiliður** til að geyma upplýsingar um lánardrottna af gerðinni **Einstaklingur**.</span><span class="sxs-lookup"><span data-stu-id="3c077-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]