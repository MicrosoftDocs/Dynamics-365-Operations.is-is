---
title: Framkvæma uppfærslur á reikningi vegna skila
description: Þessi virkni styður viðskiptaferla fyrirtækja sem velja að hafa skila- og sölupantanir reikningsfærðar á sama tíma og af sama einstaklingnum.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec803aaa2f750c43a1865c9536730b275e6ef1d4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202142"
---
# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="1c063-103">Framkvæma uppfærslur á reikningi vegna skila</span><span class="sxs-lookup"><span data-stu-id="1c063-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1c063-104">Skilapöntun er gerð af sölupöntun sem merkt er sem skilapöntun.</span><span class="sxs-lookup"><span data-stu-id="1c063-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="1c063-105">Þess vegna er listasíðan **Allar sölupantanir** notuð til að búa til reikninga fyrir skilapantanir í staðinn fyrir skjámyndina **Skilapantanir**.</span><span class="sxs-lookup"><span data-stu-id="1c063-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="1c063-106">Þessi virkni styður viðskiptaferla fyrirtækja sem velja að hafa skila- og sölupantanir reikningsfærðar á sama tíma og af sama einstaklingnum.</span><span class="sxs-lookup"><span data-stu-id="1c063-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="1c063-107">Vegna þess að reikningur fyrir skilavöru er fyrir neikvæðri upphæð er hann kallaður kreditnóta.</span><span class="sxs-lookup"><span data-stu-id="1c063-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="1c063-108">Þegar þú setur upp uppfærslu reiknings fyrir runuvinnslu verður sölupöntunin af gerðinni **Skilapöntun** að hafa stöðu skilalínu sem **Móttekið** sem gefur til kynna að fylgiseðill pöntunarinnar hafi verið uppfærður.</span><span class="sxs-lookup"><span data-stu-id="1c063-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="1c063-109">Bóka reikning fyrir skilapöntun</span><span class="sxs-lookup"><span data-stu-id="1c063-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="1c063-110">Smelltu á **Viðskiptakröfur** \> **Algengt** \> **Sölupantanir** \> **Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="1c063-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="1c063-111">Veldu sölupöntun þar sem **Skilapöntun** birtist í reitnum **Gerð pöntunar**.</span><span class="sxs-lookup"><span data-stu-id="1c063-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="1c063-112">Á aðgerðasvæðinu, á flipanum **Reikningur**, í flokknum **Búa til** skal smella á **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="1c063-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="1c063-113">Á flipanum **Færibreytur** skal velja gátreitinn **Bókun**.</span><span class="sxs-lookup"><span data-stu-id="1c063-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="1c063-114">Skoðaðu upplýsingar í skjámyndinni og gerðu þær breytingar sem eru nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="1c063-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="1c063-115">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1c063-115">Click **OK**.</span></span> <span data-ttu-id="1c063-116">Kreditnótan er bókuð.</span><span class="sxs-lookup"><span data-stu-id="1c063-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c063-117">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1c063-117">See also</span></span>

[<span data-ttu-id="1c063-118">Uppfærslur á fylgiseðli fyrir skil</span><span class="sxs-lookup"><span data-stu-id="1c063-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


