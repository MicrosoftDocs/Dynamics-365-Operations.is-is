---
title: "Skilgreina Verkflæði línuatriðis"
description: "Þessu efnisatriði útskýrir hvernig skilgreina á verkflæðiseiningu línuatriðis."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1d36ec599250f62c523e8d538a37cada9b223007
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="3a418-103">Skilgreina Verkflæði línuatriðis</span><span class="sxs-lookup"><span data-stu-id="3a418-103">Configure a line-item workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a418-104">Þessu efnisatriði útskýrir hvernig skilgreina á verkflæðiseiningu línuatriðis.</span><span class="sxs-lookup"><span data-stu-id="3a418-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="3a418-105">Til að skilgreina verkflæðiseiningu línuatriðis í verkflæðisritlinum, hægrismellt er á einingu og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu.</span><span class="sxs-lookup"><span data-stu-id="3a418-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3a418-106">Notið síðan eftirfarandi ferli til að stilla eiginleika fyrir verkflæðiseining línuatriðis.</span><span class="sxs-lookup"><span data-stu-id="3a418-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="3a418-107">Nefndu verkflæðiseiningu línuatriðis</span><span class="sxs-lookup"><span data-stu-id="3a418-107">Name the line-item workflow element</span></span>
<span data-ttu-id="3a418-108">Fylgið þessum skrefum til að færa inn heiti á verkflæðin línuatriðis.</span><span class="sxs-lookup"><span data-stu-id="3a418-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="3a418-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="3a418-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="3a418-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir verkflæðiseiningu línuatriðis.</span><span class="sxs-lookup"><span data-stu-id="3a418-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="3a418-111">Tilgreina hvort sama verkflæði er notað til að vinna úr öllum línuatriðum</span><span class="sxs-lookup"><span data-stu-id="3a418-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="3a418-112">Fylgið eftirfarandi skrefum til að tilgreina hvort sama verkflæði er notað til að vinna úr öllum línuatriðum í skjali.</span><span class="sxs-lookup"><span data-stu-id="3a418-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="3a418-113">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="3a418-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="3a418-114">Ef sama verkflæðið vinna öllum línuatriðum á skjal, smelltu þá á **Nota eitt verkflæði fyrir öll línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="3a418-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="3a418-115">Síðan velja verkflæði sem á að nota við vinnslu á línuatriði.</span><span class="sxs-lookup"><span data-stu-id="3a418-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="3a418-116">Ef tiltekið verkflæði á að vinna línuvörur sem uppfylla ákveðin skilyrði, smellið á **Nota verkflæði fyrir hvert línuatriði**.</span><span class="sxs-lookup"><span data-stu-id="3a418-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="3a418-117">Fylgdu síðan þessum skrefum til að tilgreina sett af skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="3a418-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="3a418-118">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="3a418-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="3a418-119">Í töflunni skal velja skilyrði.</span><span class="sxs-lookup"><span data-stu-id="3a418-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="3a418-120">Á **heiti Skilyrðis** flipanum, færið inn heiti fyrir skilyrði sem verið er að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="3a418-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="3a418-121">Smellið á **bæta við skilyrði** til að slá inn skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="3a418-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="3a418-122">Færið inn öll önnur skilyrði sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="3a418-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="3a418-123">Hægt er að sannreyna að skilyrðin sem voru færð inn hafi verið sett upp rétt með því að smella á **prófa**.</span><span class="sxs-lookup"><span data-stu-id="3a418-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="3a418-124">Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu og smelltu svo á **prófa**.</span><span class="sxs-lookup"><span data-stu-id="3a418-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="3a418-125">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="3a418-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="3a418-126">Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.</span><span class="sxs-lookup"><span data-stu-id="3a418-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="3a418-127">Á **Verkflæði** flipanum, veljið verkflæðið velja verkflæði sem á að nota við vinnslu línuatriði sem uppfylla skilyrðasettin sem þú skilgreindir.</span><span class="sxs-lookup"><span data-stu-id="3a418-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





