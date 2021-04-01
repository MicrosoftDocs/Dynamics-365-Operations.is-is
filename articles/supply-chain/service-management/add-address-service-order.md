---
title: Bæta aðsetur við þjónustupöntun
description: Í þessu efnisatriði er útlistað hvernig bæta aðsetur viðskiptavinar í þjónustupöntunina.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b9c6a410acbfebb3a83e753c422dd87dbf52566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205858"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="ecd56-103">Bæta aðsetur við þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="ecd56-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ecd56-104">Í þessu efnisatriði er útlistað hvernig bæta aðsetur viðskiptavinar í þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ecd56-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="ecd56-105">Þegar þjónustupöntun er stofnuð eru aðsetursupplýsingar fluttar frá verkinu sem þjónustupöntunin er tengd við.</span><span class="sxs-lookup"><span data-stu-id="ecd56-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="ecd56-106">Hins vegar er hægt að velja aðra staðsetningu aðsetur sem þegar eru færðir inn í Microsoft Dynamics AX fyrir viðskiptavini, lánardrottna, setur, vöruhús, þjónustupantanir og verk.</span><span class="sxs-lookup"><span data-stu-id="ecd56-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="ecd56-107">Einnig er hægt að búa til nýtt aðsetur.</span><span class="sxs-lookup"><span data-stu-id="ecd56-107">You can also create a new address.</span></span> <span data-ttu-id="ecd56-108">Að sjálfgefnu nýja aðsetrið flutt í verkið.</span><span class="sxs-lookup"><span data-stu-id="ecd56-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="ecd56-109">Hins vegar er hægt að tilgreina a‘ nýja aðsetrið er aðeins viðeigandi fyrir þetta tilvik þjónustu.</span><span class="sxs-lookup"><span data-stu-id="ecd56-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="ecd56-110">Ef það er ekki gert er nýtt aðsetur er ekki flutt í verk.</span><span class="sxs-lookup"><span data-stu-id="ecd56-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="ecd56-111">Búa til aðsetur viðskiptavinar fyrir þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="ecd56-111">Create a customer address for a service order</span></span>

<span data-ttu-id="ecd56-112">Fylgið eftirfarandi skrefum til að bæta við aðsetri þjónustupöntun:</span><span class="sxs-lookup"><span data-stu-id="ecd56-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="ecd56-113">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ecd56-114">Opnaðu þjónustupöntun sem þú vilt að búa til netfang fyrir.</span><span class="sxs-lookup"><span data-stu-id="ecd56-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="ecd56-115">Á **Aðgerðarrúða**, smelltu á **Breyta** og smelltu síðan **Haus skoðun**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="ecd56-116">Á **Heimilisfang** flýtiflipi, smelltu á **Bæta við heimilisfangi**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="ecd56-117">Í **Nýtt heimilisfang** skjámynd, sláðu inn einkvæmt heiti fyrir heimilisfang og fylltu út í reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="ecd56-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="ecd56-118">Ef sama heiti er fært inn sem fyrirliggjandi aðsetur, upplýsingarnar sem færðar eru inn í eftirstandandi reiti mun skrifa yfir upplýsingar um fyrirliggjandi aðsetur.</span><span class="sxs-lookup"><span data-stu-id="ecd56-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="ecd56-119">Smellið á **í lagi** til að afrita nýja aðsetrið á þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ecd56-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="ecd56-120">Aukaaðsetur tilgreint á þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="ecd56-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="ecd56-121">Til að bæta öðru aðsetri við þjónustupöntun, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="ecd56-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="ecd56-122">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ecd56-123">Opnaðu þjónustupöntun sem þú vilt slá inn annað aðsetur fyrir.</span><span class="sxs-lookup"><span data-stu-id="ecd56-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="ecd56-124">Á **Aðgerðarrúða**, smelltu á **Breyta** og smelltu síðan **Haus skoðun**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="ecd56-125">Á **Heimilisfang** flýtiflipi, smelltu á **Annað heimilisfang**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="ecd56-126">Í **Val á heimilisfangi** skjámyndinni, í reitnum **Færslugerð**, veldu **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ecd56-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="ecd56-127">Veljið aðsetur og smellið síðan á **í lagi** að afrita í þjónustupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ecd56-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]