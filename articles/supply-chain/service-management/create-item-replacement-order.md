---
title: Stofnun skiptipöntunar vöru
description: Vöruskilapantanir eru yfirleitt stofnaðar eftir að vöru hefur verið skilað eftir skoðun.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0932c34cc6b3604afbea7c8a18620640c00d928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258000"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="5dc0b-103">Stofnun skiptipöntunar vöru</span><span class="sxs-lookup"><span data-stu-id="5dc0b-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5dc0b-104">Vöruskilapantanir eru yfirleitt stofnaðar eftir að vöru hefur verið skilað eftir skoðun.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="5dc0b-105">Hins vegar, ef nauðsynlegt er að skipta út vöru áður en henni hefur verið skilað, eða ef upprunalegu vörunni verður ekki skilað, er hægt að stofna vöruskiptapöntun um leið og búið er að stofna skilapöntun.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="5dc0b-106">Stofna skal skiptipöntun eftir að skilavara hefur verið móttekin</span><span class="sxs-lookup"><span data-stu-id="5dc0b-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="5dc0b-107">Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="5dc0b-108">Búðu til nýtt skilapöntun, eða veldu skilapöntun frá listanum til að opna **Skilapöntun - RMA númer: %1, %2** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="5dc0b-109">Smelltu á **Skilalína** og veldu síðan **Skiptivara**.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="5dc0b-110">Veljið vöruna sem á að skipta út skilavörunni með.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="5dc0b-111">Færa skal inn nákvæma skilgreiningu og smella síðan á **Nota**.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="5dc0b-112">Smelltu á **Fylgiseðill** til að búa til fylgiseðill fyrir skilapöntunina.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="5dc0b-113">Sölupöntun er mynduð fyrir skiptivöruna sem var valin.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="5dc0b-114">Eftir að sölupöntunin er búin til fyrir skilavöruna er sölusamninga sjálfkrafa leitað og ef sölusamningur er fyrir hendi er hann settur á sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="5dc0b-115">Stofna skal skiptipöntun áður en þú móttekur vöru sem verður skilað</span><span class="sxs-lookup"><span data-stu-id="5dc0b-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="5dc0b-116">Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="5dc0b-117">Búðu til nýja skilapöntun, eða veldu skilapöntun af listanum til að opna skjámyndina **Skilapöntun - RMA númer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="5dc0b-118">Smelltu á **Finna sölupöntun** ef þú vilt auðkenna sölupöntun fyrir skilavörunni.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="5dc0b-119">Fylla út í **Finna sölupöntun** skjámynd og smelltu síðan **Í lagi** til að loka skjámynd og fara aftur í **Skilapöntun - RMA númer: %1, %2** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="5dc0b-120">Sölupöntunarlínan fyrir skilavöruna er afrituð í vöruskilapöntunina.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="5dc0b-121">Smelltu á **Skilapöntun** til að opna **Búa til sölupöntun** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="5dc0b-122">Veldu **Afrita skilapöntunarlínur** gátreitinn til að flytja upplýsingar úr skilapöntun sem þú valdir á **Skilapöntun - RMA númer: %1, %2** skjámynd yfir í þessa sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="5dc0b-123">Færa skal inn eða breyta upplýsingum eins og krafist er.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="5dc0b-124">Ef þú tilgreindir sölupöntunina í skrefi 3 og ef sölupöntunarlína fyrir skilavöruna er tengdur sölusamningi verður sjálfkrafa birt auðkenni á gildandi sölusamningi fyrir vöruskilapöntunina í **Sölusamningsauðkenni** reitnum.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="5dc0b-125">Smelltu **Í lagi** til að loka **Búa til sölupöntun** skjámynd og opnaðu **Sölupöntun** skjámynd, þar sem þú getur haldið áfram að slá inn upplýsingar um nýja sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="5dc0b-126">Allar viðeigandi skilapöntunarlínur munu verða afritaðar á nýju sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="5dc0b-127">Ef sölusamningsauðkennið birtist sjálfkrafa í **Sölusamningnsauðkenni** reitnum, þá hefur sölusamningurinn verið tengdur við sölupöntunarhausinn fyrir skilavörupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="5dc0b-128">Ef tiltæk ráðstöfun er til staðar í sölusamningnum sem ekki hefur verið uppfyllt ennþá og sölupöntunin er stofnuð áður en sölusamningurinn rennur út, er mynduð tenging milli sölusamningslínunnar og sölupöntunarlínunnar.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="5dc0b-129">Þess vegna eru upplýsingar úr sölusamningnum, t.d. vöruverð, afritaðar yfir í nýju sölupöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="5dc0b-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]