---
title: Afturkalla þjónustupantanir
description: Þú getur hætt við þjónustupöntun eða þjónustupöntunarlínu frá þjónustupöntuninni sjálfri, eða þú getur hætt við margar þjónustupantanir með því að keyra reglubundna vinnslu.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546595"
---
# <a name="cancel-service-orders"></a><span data-ttu-id="643ce-103">Afturkalla þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="643ce-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="643ce-104">Þú getur hætt við þjónustupöntun eða þjónustupöntunarlínu frá þjónustupöntuninni sjálfri, eða þú getur hætt við margar þjónustupantanir með því að keyra reglubundna vinnslu.</span><span class="sxs-lookup"><span data-stu-id="643ce-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="643ce-105">Ekki er hægt að hætta við þjónustupantanir ef stig þjónustupöntunarinnar leyfir ekki að hætta við, ef þjónustupöntunin er með vörukröfur eða ef þjónustupöntunin hefur þegar verið bókuð.</span><span class="sxs-lookup"><span data-stu-id="643ce-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="643ce-106">Hætta við þjónustupöntun í skjámyndinni Þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="643ce-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="643ce-107">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="643ce-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="643ce-108">Veldu þjónustupöntunina og smelltu svo á **Hætta við pöntun** á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="643ce-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="643ce-109">Hætta við þjónustupöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="643ce-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="643ce-110">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="643ce-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="643ce-111">Tvísmella á þjónustupöntunina sem inniheldur línuna sem þú vilt hætta við.</span><span class="sxs-lookup"><span data-stu-id="643ce-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="643ce-112">Veldu þjónustupöntunarlínuna sem þú vilt hætta við og smelltu síðan á **Hætta við pöntunarlínu** til að breyta stöðu línunnar í **Hætt við**.</span><span class="sxs-lookup"><span data-stu-id="643ce-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="643ce-113">Til að snúa við afturköllun þjónustupöntunarlínu og breyta stöðunni aftur í <STRONG>Stofnuð</STRONG>, smelltu á <STRONG>Afnema afturköllun</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="643ce-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="643ce-114">Afturkalla margar þjónustupantanir</span><span class="sxs-lookup"><span data-stu-id="643ce-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="643ce-115">Smelltu á **Þjónustukerfi** \> **Reglubundið** \> **þjónustupantanir** \> **Hætta við þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="643ce-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="643ce-116">Smelltu á hnappinn **Velja**.</span><span class="sxs-lookup"><span data-stu-id="643ce-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="643ce-117">Í **Fyrirspurn** skjámynd, í **Skilyrði** dálknum, veldu þær þjónustupantanir sem þú vilt hætta við.</span><span class="sxs-lookup"><span data-stu-id="643ce-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="643ce-118">Smelltu á **Í lagi** til að loka **Fyrirspurn** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="643ce-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="643ce-119">Veldu gátreitinn **Sýna upplýsingaskrá** til að búa til Upplýsingaskrá sem sýnir þjónustupantanir sem hætt hefur verið við.</span><span class="sxs-lookup"><span data-stu-id="643ce-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="643ce-120">Veldu gátreitinn **Afnema afturköllun** ef þú vilt snúa við stöðunni **Hætta við** á þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="643ce-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="643ce-121">Smellið á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="643ce-121">Click **OK**.</span></span>

<span data-ttu-id="643ce-122">Annaðhvort er búið að hætta við völdu þjónustupantanirnar eða vinnslustöðu þeirra **Hætta við** hefur verið snúið aftur til **Í vinnslu** .</span><span class="sxs-lookup"><span data-stu-id="643ce-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="643ce-123">Ef þú velur <STRONG>Afnema afturköllun</STRONG> gátreitinn, er þjónustupantanir með vinnslustöðu <STRONG>Hætt við</STRONG> snúið við og ekki er hætt við þjónustupantanir með vinnslustöðu <STRONG>Í vinnslu</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="643ce-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  


