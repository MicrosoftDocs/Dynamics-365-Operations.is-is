---
title: Um tengsl þjónustuhluta
description: Þetta efnisatriði lýsir hvernig á að stofna tengsl þjónustuhlutar í þjónustusamningi og þjónustupöntun.
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
ms.openlocfilehash: 344037026399792d6da5777abbde8c9d0d9178f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817630"
---
# <a name="create-service-object-relations"></a><span data-ttu-id="0fb91-103">Um tengsl þjónustuhluta</span><span class="sxs-lookup"><span data-stu-id="0fb91-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0fb91-104">Þetta efnisatriði lýsir hvernig á að stofna tengsl þjónustuhlutar í þjónustusamningi og þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="0fb91-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="0fb91-105">Þegar þú býrð til þjónustuhlutvensl tengirðu þjónustuhlutinn við þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="0fb91-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="0fb91-106">Þegar beiðnir þjónustu viðskiptavinar fyrir vöru sem þjónustuhlut, hægt er að velja þá þjónustuhlutar af lista yfir tengsl þjónustuhluta.</span><span class="sxs-lookup"><span data-stu-id="0fb91-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="0fb91-107">Stofna tengsl þjónustuhlutar fyrir þjónustusamning</span><span class="sxs-lookup"><span data-stu-id="0fb91-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="0fb91-108">Fylgið eftirfarandi skrefum til að stofna þjónustuhlutatengsl fyrir þjónustusamning:</span><span class="sxs-lookup"><span data-stu-id="0fb91-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="0fb91-109">Smellið á **Þjónustustjórnun** \> **Almennt** \> **Þjónustusamningar** \> **þjónustusamningar**.</span><span class="sxs-lookup"><span data-stu-id="0fb91-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="0fb91-110">Í **Þjónustusamningar** listanum, velja núverandi þjónustusamning eða smella á **Nýtt** til að búa til nýjan þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="0fb91-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="0fb91-111">Í **þjónustusamningar** skjámynd í **Aðgerðarúða** á flipanum **Þjónustusamningur** í **Tengsl** flokknum, skal smella á **Þjónustuhlutir**.</span><span class="sxs-lookup"><span data-stu-id="0fb91-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="0fb91-112">Í **Þjónustuhlutir** skjámynd, smelltu **Nýtt**, og veldu síðan þjónustuhlut fyrir þessa þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="0fb91-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="0fb91-113">Til að úthluta sniðmátaruppskrift (BOM) til þjónustusamningsins, smelltu á **Aðgerðir** og veldu síðan **Hengja við sniðmát BOM**.</span><span class="sxs-lookup"><span data-stu-id="0fb91-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="0fb91-114">Í **Velja sniðmát BOM** skjámynd, í **Sniðmát BOM** reit, velja sniðmát.</span><span class="sxs-lookup"><span data-stu-id="0fb91-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="0fb91-115">Stofna tengsl þjónustuhlutar í þjónustupöntun</span><span class="sxs-lookup"><span data-stu-id="0fb91-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="0fb91-116">Fylgið eftirfarandi skrefum til að stofna tengsl þjónustuhlutar í þjónustupöntun:</span><span class="sxs-lookup"><span data-stu-id="0fb91-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="0fb91-117">Smelltu á **Þjónustustjórnun** \> **Almennt** \> **Þjónustupantanir** \> **Þjónustupantanir**.</span><span class="sxs-lookup"><span data-stu-id="0fb91-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="0fb91-118">Í **þjónustupantanir** listanum, velja núverandi þjónustupöntun, eða búa til nýja þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="0fb91-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="0fb91-119">Í **þjónustupantanir** skjámynd á **Aðgerðarúða**, á flipanum **Þjónustupöntun**, í flokknum **Tengsl** skal velja **Þjónustuhlutir**.</span><span class="sxs-lookup"><span data-stu-id="0fb91-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="0fb91-120">Í **Þjónustuhlutir** skjámynd, smelltu **Nýtt**, og veldu síðan þjónustuhlutur fyrir þessa þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="0fb91-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="0fb91-121">Til að úthluta sniðmát BOM til þjónustusamninginn, smelltu á **Aðgerðir** og veldu síðan **Hengja við sniðmát BOM**.</span><span class="sxs-lookup"><span data-stu-id="0fb91-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="0fb91-122">Í **Velja sniðmát BOM** skjámynd, í **Sniðmát BOM** reit, velja sniðmát.</span><span class="sxs-lookup"><span data-stu-id="0fb91-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="0fb91-123">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="0fb91-123">See also</span></span>

[<span data-ttu-id="0fb91-124">Yfirlit yfir þjónustuhluti</span><span class="sxs-lookup"><span data-stu-id="0fb91-124">Service objects overview</span></span>](service-objects.md)

[<span data-ttu-id="0fb91-125">Tengsl þjónustuhluta</span><span class="sxs-lookup"><span data-stu-id="0fb91-125">Service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="0fb91-126">Sniðmátsuppskriftir</span><span class="sxs-lookup"><span data-stu-id="0fb91-126">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]