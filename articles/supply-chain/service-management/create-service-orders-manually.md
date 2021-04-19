---
title: Stofna þjónustupantanir handvirkt
description: Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 486b4a0291ca527e647c9b5a41ff2e65a7820291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817582"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="f562a-103">Stofna þjónustupantanir handvirkt</span><span class="sxs-lookup"><span data-stu-id="f562a-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f562a-104">Þú getur búið til þjónustupantanir handvirkt með því að nota þjónustusamning eða með því að nota **þjónustupantanir** skjámyndina.</span><span class="sxs-lookup"><span data-stu-id="f562a-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="f562a-105">Einnig er hægt að stofna þjónustupöntun úr verki.</span><span class="sxs-lookup"><span data-stu-id="f562a-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="f562a-106">Þú getur notað sjálfvirk ferli til að búa til þjónustupantanir.</span><span class="sxs-lookup"><span data-stu-id="f562a-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="f562a-107">Búðu til þjónustupöntun handvirkt út frá þjónustusamningi</span><span class="sxs-lookup"><span data-stu-id="f562a-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="f562a-108">Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="f562a-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="f562a-109">Veljið þjónustusamning eða stofnið nýjan þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="f562a-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="f562a-110">Veljið **Afhenda** flipann og í **Stofna** hópnum skal velja **Skipulögð þjónustupantanir** til að opna skjámyndina **Stofna þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f562a-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="f562a-111">Stofna þjónustupöntun handvirkt í skjámyndinni Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="f562a-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="f562a-112">Veljið **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f562a-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="f562a-113">Veljið **Nýtt** til að stofna nýja þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="f562a-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="f562a-114">Stofnið þjónustupöntunarlínur fyrir þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="f562a-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="f562a-115">Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="f562a-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="f562a-116">Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="f562a-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="f562a-117">Búðu til þjónustupöntun frá verkefni</span><span class="sxs-lookup"><span data-stu-id="f562a-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="f562a-118">Opnið **Verkefnastjórnun og bókhald** \> **Almennt** \> **Verk** \> **Öll verk**.</span><span class="sxs-lookup"><span data-stu-id="f562a-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="f562a-119">Í **Verkefni** skjámynd, á **Aðgerðasvæði** skal velja **Stjórna** flipann \> velja **Þjónusta** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f562a-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="f562a-120">Fylgja fyrri aðferð til að búa til þjónustupöntun handvirkt í **þjónustupantanir** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="f562a-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="f562a-121">**Auðkenni verkefnis** reitinn sýnir verkefni tilvísun.</span><span class="sxs-lookup"><span data-stu-id="f562a-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="f562a-122">Ef valinn er gátreitur <STRONG>Leyfa án þjónustusamnings</STRONG> í skjámyndinni <STRONG>Færibreytur þjónustustjórnunar</STRONG> getur þú sent færslurnar frá þjónustupöntunarlínunum án þess að tengja þjónustupöntunina við þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="f562a-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="f562a-123">Ef gátreiturinn er hreinsaður verður í það minnsta að tengja þjónustupöntunina, sem var stofnuð handvirkt, við verk áður en þjónustupöntunarlínurnar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="f562a-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="f562a-124">Búðu til þjónustupöntun út frá sölupöntunarskjámynd</span><span class="sxs-lookup"><span data-stu-id="f562a-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="f562a-125">Þú getur búið til þjónustupöntun út frá **Sölupantanir** skjámynd með því að nota **Stofna nýjan þjónustupöntun sem byggist á sölupöntunar** hjálpinni.</span><span class="sxs-lookup"><span data-stu-id="f562a-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="f562a-126">Farðu í **Sala og markaðssetning** \> **Almennt** \> **Sölupantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="f562a-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="f562a-127">Viðeigandi sölupöntun er opnuð.</span><span class="sxs-lookup"><span data-stu-id="f562a-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="f562a-128">Á **Sölupöntun** flipanum skal velja **Þjónustupöntun** til að hefja **Stofna nýjan þjónustupöntun sem byggist á sölupöntun** hjálpinni.</span><span class="sxs-lookup"><span data-stu-id="f562a-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="f562a-129">Veljið **Næsta \>**, og ljúkið svo eftirfarandi skrefum á **Veldu samkomulag um þjónustupöntun** síðunni:</span><span class="sxs-lookup"><span data-stu-id="f562a-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="f562a-130">Notaðu **þjónustusamningur** reitinn til að velja þjónustusamninginn sem ætti að tengja nýja þjónustupöntunina við.</span><span class="sxs-lookup"><span data-stu-id="f562a-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="f562a-131">Valfrjálst: Notaðu **Auðkenni verkefnis** reitinn til að tengja þessa þjónustupöntun við tiltekið verkefni.</span><span class="sxs-lookup"><span data-stu-id="f562a-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="f562a-132">Veljið **Næsta \>**, og ljúkið svo eftirfarandi skrefum á **Stofna þjónustupöntun** síðunni:</span><span class="sxs-lookup"><span data-stu-id="f562a-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="f562a-133">Sláðu inn dagsetningu og tíma fyrir þjónustusímtalið í reitnum **Valinn þjónustutími** reitinn.</span><span class="sxs-lookup"><span data-stu-id="f562a-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="f562a-134">Valfrjálst: Breyttu textanum í **Lýsing** reitnum.</span><span class="sxs-lookup"><span data-stu-id="f562a-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="f562a-135">Sjálfgefið inniheldur þetta reitur lýsingu á þjónustusamningnum sem þú valdir á fyrri síðunni.</span><span class="sxs-lookup"><span data-stu-id="f562a-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="f562a-136">Í **Ábyrgur** reitinn, velja Kenni starfsmanns sem ber ábyrgð á samningnum, og ef þú veist hvað það er, slá inn Kenni valinn tæknimaður viðskiptavinarins fyrir þjónustusímtali.</span><span class="sxs-lookup"><span data-stu-id="f562a-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="f562a-137">Í **Kenni tengiliðar** reitinn, velja einstakling í fyrirtæki viðskiptavinarins sem ætti að hafa samband við varðandi þessa þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="f562a-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="f562a-138">Veljið **Næsta \>** og svo **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="f562a-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="f562a-139">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f562a-139">See also</span></span>

[<span data-ttu-id="f562a-140">Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="f562a-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="f562a-141">Stofna þjónustupantanir sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="f562a-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="f562a-142">[Stofna þjónustupantanir (klasaskjámynd)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="f562a-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]