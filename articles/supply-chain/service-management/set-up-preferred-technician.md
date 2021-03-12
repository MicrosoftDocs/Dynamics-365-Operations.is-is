---
title: Uppsetning æskilegs tæknimanns
description: Hægt er að velja hvaða starfsmann sem æskilegan tæknimann fyrir þjónustusamning eða þjónustupöntun.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a06ec39bd0552faf7961ae75ff393f0b8edac2eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991741"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="19b7a-103">Uppsetning æskilegs tæknimanns</span><span class="sxs-lookup"><span data-stu-id="19b7a-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="19b7a-104">Hægt er að velja hvaða starfsmann sem æskilegan tæknimann fyrir þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="19b7a-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="19b7a-105">Hins vegar er góð hugmynd að bæta starfsmanninum í viðeigandi sendingarhóp þannig að starfsmaðurinn sé tekinn með í **Sendingartöflunni**.</span><span class="sxs-lookup"><span data-stu-id="19b7a-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="19b7a-106">Úthluta starfsmanni við sendingarhóp</span><span class="sxs-lookup"><span data-stu-id="19b7a-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="19b7a-107">Smellt er á **Mannauður** \> **Algengt** \> **Starfsmenn** \> **Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="19b7a-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="19b7a-108">Tvísmella á starfsmann til að opna upplýsingasíðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="19b7a-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="19b7a-109">Í **Aðgerðasvæði** er smellt á **Uppsetning** \>**Sendingarhópur** til að opna skjámyndina **Senda starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="19b7a-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="19b7a-110">Í reitnum **Sendingarhópur** skal velja hópinn sem starfsmaðurinn á að tilheyra.</span><span class="sxs-lookup"><span data-stu-id="19b7a-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="19b7a-111">Úthluta þjónustusamningi æskilegan tæknimann</span><span class="sxs-lookup"><span data-stu-id="19b7a-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="19b7a-112">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="19b7a-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="19b7a-113">Tvísmella á þjónustusamning til að opna upplýsingaskjámynd.</span><span class="sxs-lookup"><span data-stu-id="19b7a-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="19b7a-114">Á flipanum **Almennt** skal velja reitinn **Æskilegur tæknimaður** og síðan velja meðlim viðeigandi sendingarhóps sem æskilegan tæknimann fyrir þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="19b7a-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="19b7a-115">Úthluta þjónustupöntun æskilegan tæknimann</span><span class="sxs-lookup"><span data-stu-id="19b7a-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="19b7a-116">Smelltu á **Þjónustustjórnun** \> **Reglubundið** \> **Sendingartafla**.</span><span class="sxs-lookup"><span data-stu-id="19b7a-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="19b7a-117">Í skjámyndinni <STRONG>Sendingartafla</STRONG> skal tilgreina dagsetningarsvið fyrir sendingarverkþætti sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="19b7a-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="19b7a-118">Einnig skal tilgreina hvort birta eigi lokaða verkþætti og hvort takmarka eigi lista sendingarverkþátta við hópa sem notandinn tilheyrir eða hefur heimild til að hafa eftirlit með</span><span class="sxs-lookup"><span data-stu-id="19b7a-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="19b7a-119">Smellið á <STRONG>Í lagi</STRONG> til að opna <STRONG>Sendingartöflu</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="19b7a-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="19b7a-120">Veljið þá línu þjónustuverkþáttar sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="19b7a-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="19b7a-121">Á flipanum **Tengt** skal nota listann **Starfsmenn** til að skipa meðlim viðeigandi sendingarhóps sem æskilegan tæknimann fyrir þjónustusímtalið.</span><span class="sxs-lookup"><span data-stu-id="19b7a-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="19b7a-122">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="19b7a-122">See also</span></span>

[<span data-ttu-id="19b7a-123">Yfirlit yfir þróaða og innleidda þjónustusamninga</span><span class="sxs-lookup"><span data-stu-id="19b7a-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="19b7a-124">Stofna þjónustupantanir handvirkt</span><span class="sxs-lookup"><span data-stu-id="19b7a-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="19b7a-125">[Þjónustusamningar (skjámynd)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="19b7a-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  


