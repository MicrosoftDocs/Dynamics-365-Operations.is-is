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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902726"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="159eb-103">Skipta á milli lánardrottnahönnunar</span><span class="sxs-lookup"><span data-stu-id="159eb-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="159eb-104">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="159eb-104">Vendor data flow</span></span> 

<span data-ttu-id="159eb-105">Ef þú notar önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt einangra upplýsingar lánardrottins frá viðskiptavinum, notarðu þessa grunn lánardrottinshönnun.</span><span class="sxs-lookup"><span data-stu-id="159eb-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grunnlánardrottnaflæði](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="159eb-107">Ef þú notar önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt halda áfram að nota eininguna **Lykill** til að geyma upplýsingar lánardrottins geturðu notað þessa útvíkkuðu lánardrottinshönnun.</span><span class="sxs-lookup"><span data-stu-id="159eb-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="159eb-108">Í þessari hönnun eru stækkaðar upplýsingar um lánardrottinn, eins og staða lánardrottins í bið og lánardrottinssniðs vistaðar í einingunni **lánardrottnar** í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="159eb-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Útvíkkað lánardrottnaflæði](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="159eb-110">Fylgdu skrefunum hér að neðan til að nota stækkaða lánardrottnahönnun:</span><span class="sxs-lookup"><span data-stu-id="159eb-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="159eb-111">Lausnapakkinn **FramboðChainCommon** inniheldur ferlissniðmát verkflæðis eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="159eb-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="159eb-112">![Ferlissniðmát verkflæðis](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="159eb-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="159eb-113">Búðu til nýja verkflæðisferla með ferlissniðmáti verkflæðis:</span><span class="sxs-lookup"><span data-stu-id="159eb-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="159eb-114">Stofnaðu nýtt verkflæðisferli fyrir eininguna **Lánardrottinn** sem notar ferlissniðmát verkflæðis **Stofna lánardrottna í lykileiningu** og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="159eb-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="159eb-115">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="159eb-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="159eb-116">![Stofna lánardrottna í lykileiningu](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="159eb-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="159eb-117">Stofnaðu nýtt verkflæðisferli fyrir eininguna **Lánardrottinn** sem notar ferlissniðmát verkflæðis **Uppfæra lykileiningu** og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="159eb-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="159eb-118">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="159eb-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="159eb-119">![Uppfæra lyklaeiningu](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="159eb-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="159eb-120">Stofnaðu ný verkflæðisferli úr sniðmátunum sem voru stofnuð í einingunni **Lyklar**.</span><span class="sxs-lookup"><span data-stu-id="159eb-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="159eb-121">![Stofna lánardrottna í lykileiningu](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="159eb-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="159eb-122">![Uppfæra lánardrottnaeiningu](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="159eb-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="159eb-123">Þú getur stillt verkflæði sem rauntíma eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="159eb-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="159eb-124">![Umbreyta í bakgrunnsverkflæði](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="159eb-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="159eb-125">Virkjaðu verkflæðin sem þú stofnaðir í einingunum **Lykill** og **Lánardrottinn** til að hefja notkun á einingunni **Lykill** til að geyma upplýsingar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="159eb-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
