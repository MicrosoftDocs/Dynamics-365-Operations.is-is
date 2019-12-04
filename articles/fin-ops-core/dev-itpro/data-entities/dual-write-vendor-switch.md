---
title: Skipta á milli hönnunar lánardrottna
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772365"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="9f58a-102">Skipta á milli hönnunar lánardrottna</span><span class="sxs-lookup"><span data-stu-id="9f58a-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="9f58a-103">Gagnaflæði lánardrottins</span><span class="sxs-lookup"><span data-stu-id="9f58a-103">Vendor data flow</span></span> 

<span data-ttu-id="9f58a-104">Ef þú notar önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt einangra upplýsingar lánardrottins frá viðskiptavinum, notarðu þessa grunn lánardrottinshönnun.</span><span class="sxs-lookup"><span data-stu-id="9f58a-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grunnlánardrottnaflæði](media/dual-write-switch-1.png)
 
<span data-ttu-id="9f58a-106">Ef þú notar önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt halda áfram að nota eininguna **Lykill** til að geyma upplýsingar lánardrottins geturðu notað þessa útvíkkuðu lánardrottinshönnun.</span><span class="sxs-lookup"><span data-stu-id="9f58a-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="9f58a-107">Í þessari hönnun eru stækkaðar upplýsingar um lánardrottinn, eins og staða lánardrottins í bið og lánardrottinssniðs vistaðar í einingunni **lánardrottnar** í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9f58a-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Útvíkkað lánardrottnaflæði](media/dual-write-switch-2.png)
 
<span data-ttu-id="9f58a-109">Fylgdu skrefunum hér að neðan til að nota stækkaða lánardrottnahönnun:</span><span class="sxs-lookup"><span data-stu-id="9f58a-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="9f58a-110">Lausnapakkinn **FramboðChainCommon** inniheldur ferlissniðmát verkflæðis eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="9f58a-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="9f58a-111">![Ferlissniðmát verkflæðis](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="9f58a-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="9f58a-112">Búðu til nýja verkflæðisferla með ferlissniðmáti verkflæðis:</span><span class="sxs-lookup"><span data-stu-id="9f58a-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="9f58a-113">Stofnaðu nýtt verkflæðisferli fyrir eininguna **Lánardrottinn** sem notar ferlissniðmát verkflæðis **Stofna lánardrottna í lykileiningu** og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9f58a-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9f58a-114">Þetta verkflæði annast stofnunaraðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="9f58a-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f58a-115">![Stofna lánardrottna í lykileiningu](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="9f58a-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="9f58a-116">Stofnaðu nýtt verkflæðisferli fyrir eininguna **Lánardrottinn** sem notar ferlissniðmát verkflæðis **Uppfæra lykileiningu** og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="9f58a-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="9f58a-117">Þetta verkflæði annast uppfærsluaðstæður lánardrottins fyrir eininguna **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="9f58a-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f58a-118">![Uppfæra lyklaeiningu](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="9f58a-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="9f58a-119">Stofnaðu ný verkflæðisferli úr sniðmátunum sem voru stofnuð í einingunni **Lyklar**.</span><span class="sxs-lookup"><span data-stu-id="9f58a-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f58a-120">![Stofna lánardrottna í lykileiningu](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="9f58a-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="9f58a-121">![Uppfæra lánardrottnaeiningu](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="9f58a-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="9f58a-122">Þú getur stillt verkflæði sem rauntíma eða bakgrunnsverkflæði út frá þörfum þínum.</span><span class="sxs-lookup"><span data-stu-id="9f58a-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="9f58a-123">![Umbreyta í bakgrunnsverkflæði](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="9f58a-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="9f58a-124">Virkjaðu verkflæðin sem þú stofnaðir í einingunum **Lykill** og **Lánardrottinn** til að hefja notkun á Customer Engagement-einingunni **Lykill** til að geyma upplýsingar lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="9f58a-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
