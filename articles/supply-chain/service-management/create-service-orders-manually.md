---
title: "Stofna þjónustupantanir handvirkt"
description: "Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0cc6b2646929776f4efb20474de6b0fc5c4719c
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-manually"></a><span data-ttu-id="271f7-103">Stofna þjónustupantanir handvirkt</span><span class="sxs-lookup"><span data-stu-id="271f7-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="271f7-104">Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="271f7-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="271f7-105">Einnig er hægt að stofna þjónustupöntun úr verki.</span><span class="sxs-lookup"><span data-stu-id="271f7-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="271f7-106">Þú getur notað sjálfvirk ferli til að búa til þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="271f7-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="271f7-107">Búðu til þjónustupöntun handvirkt út frá þjónustusamningi</span><span class="sxs-lookup"><span data-stu-id="271f7-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="271f7-108">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="271f7-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="271f7-109">Veljið þjónustusamning eða stofnið nýjan þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="271f7-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="271f7-110">Smelltu á flipann **Afhenda** og í **Stofna** hópnum skal smella á **Skipulögð þjónustupantanir** til að opna **Stofna þjónustupantanir** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="271f7-110">Click the **Deliver** tab and in the **Create** group click **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="271f7-111">Stofna þjónustupöntun handvirkt í skjámyndinni Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="271f7-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="271f7-112">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="271f7-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="271f7-113">Styðjið á CTRL+N til að stofna nýja þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="271f7-113">Press Ctrl+N to create a new service order.</span></span>

3.  <span data-ttu-id="271f7-114">Stofnið þjónustupöntunarlínur fyrir þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="271f7-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="271f7-115">Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="271f7-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="271f7-116">Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="271f7-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="271f7-117">Búðu til þjónustupöntun frá verkefni</span><span class="sxs-lookup"><span data-stu-id="271f7-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="271f7-118">Smelltu á **Verkefnastjórnun og bókhald** \> **Almenn** \> **Verkefni** \> **Öll verkefni**.</span><span class="sxs-lookup"><span data-stu-id="271f7-118">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="271f7-119">Í **Verkefni** skjámynd, á **Aðgerðarúðu**, smelltu á **Stjórna** flipann \> smella **Þjónusta** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="271f7-119">In the **Projects** form, on the **Action pane**, click the **Manage** tab \> click **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="271f7-120">Fylgja fyrri aðferð til að búa til þjónustupöntun handvirkt í **þjónustupantanir** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="271f7-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="271f7-121">**Auðkenni verkefnis** reitinn sýnir verkefni tilvísun.</span><span class="sxs-lookup"><span data-stu-id="271f7-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="271f7-122">Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="271f7-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="271f7-123">Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="271f7-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="271f7-124">Búðu til þjónustupöntun út frá sölupöntunarskjámynd</span><span class="sxs-lookup"><span data-stu-id="271f7-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="271f7-125">Þú getur búið til þjónustupöntun út frá **Sölupantanir** skjámynd með því að nota **Stofna nýjan þjónustupöntun sem byggist á sölupöntunar** hjálpinni.</span><span class="sxs-lookup"><span data-stu-id="271f7-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="271f7-126">Smellið á **Sala og markaðssetning** \> **Almennt** \> **Sölupantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="271f7-126">Click **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="271f7-127">Viðeigandi sölupöntun er opnuð.</span><span class="sxs-lookup"><span data-stu-id="271f7-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="271f7-128">Á **Sölupöntun** flipanum smelltu á **Þjónustupöntun** til að hefja **Stofna nýjan þjónustupöntun sem byggist á sölupöntun** hjálpinni.</span><span class="sxs-lookup"><span data-stu-id="271f7-128">On the **Sales order** tab, click **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="271f7-129">Smelltu á **Næsta \>**, og svo ljúka eftirfarandi skrefum á **Veldu samkomulag um þjónustupöntun** síðunni:</span><span class="sxs-lookup"><span data-stu-id="271f7-129">Click **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="271f7-130">Notaðu **þjónustusamningur** reitinn til að velja þjónustusamninginn sem ætti að tengja nýja þjónustupöntunina við.</span><span class="sxs-lookup"><span data-stu-id="271f7-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="271f7-131">Valfrjálst: Notaðu **Auðkenni verkefnis** reitinn til að tengja þessa þjónustupöntun við tiltekið verkefni.</span><span class="sxs-lookup"><span data-stu-id="271f7-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="271f7-132">Smelltu á **Næsta \>** , og svo ljúka eftirfarandi skrefum á **Stofna þjónustupöntun** síðunni:</span><span class="sxs-lookup"><span data-stu-id="271f7-132">Click **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="271f7-133">Sláðu inn dagsetningu og tíma fyrir þjónustusímtalið í reitnum **Valinn þjónustutími** reitinn.</span><span class="sxs-lookup"><span data-stu-id="271f7-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="271f7-134">Valfrjálst: Breyttu textanum í **Lýsing** reitnum.</span><span class="sxs-lookup"><span data-stu-id="271f7-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="271f7-135">Sjálfgefið inniheldur þetta reitur lýsingu á þjónustusamningnum sem þú valdir á fyrri síðunni.</span><span class="sxs-lookup"><span data-stu-id="271f7-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="271f7-136">Í **Ábyrgur** reitinn, velja Kenni starfsmanns sem ber ábyrgð á samningnum, og ef þú veist hvað það er, slá inn Kenni valinn tæknimaður viðskiptavinarins fyrir þjónustusímtali.</span><span class="sxs-lookup"><span data-stu-id="271f7-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="271f7-137">Í **Kenni tengiliðar** reitinn, velja einstakling í fyrirtæki viðskiptavinarins sem ætti að hafa samband við varðandi þessa þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="271f7-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="271f7-138">Smella á **Næsta \>** og smella síðan á **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="271f7-138">Click **Next \>**, and then click **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="271f7-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="271f7-139">See also</span></span>

[<span data-ttu-id="271f7-140">Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="271f7-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="271f7-141">Stofna þjónustupantanir sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="271f7-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="271f7-142">[Stofna þjónustupantanir (klasaskjámynd)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="271f7-142">[Create service orders (class form)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\))</span></span> 

