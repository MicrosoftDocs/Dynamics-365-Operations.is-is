---
title: Skilgreina skilyrtar ákvöarðanir í verkflæði
description: Notið eftirfarandi ferli til að stilla eiginleika fyrir skilyrt ákvörðun.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a01290b3e2810aa1762f2230e8d01d219d6b10bf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554921"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="b7f44-103">Skilgreina skilyrtar ákvöarðanir í verkflæði</span><span class="sxs-lookup"><span data-stu-id="b7f44-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7f44-104">Notið eftirfarandi ferli til að stilla eiginleika fyrir skilyrt ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="b7f44-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="b7f44-105">Skilyrt ákvörðun er punktur þar sem verkflæði skiptist í tvær greinar.</span><span class="sxs-lookup"><span data-stu-id="b7f44-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="b7f44-106">Til að skilgreina skilyrta ákvörðun í verkflæðisritlinum, hægrismellt er á skilyrt ákvörðun og smellið síðan á **Eiginleika** til að opna **Eiginleika** skjámynd.</span><span class="sxs-lookup"><span data-stu-id="b7f44-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="b7f44-107">Nefndu ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="b7f44-107">Name a decision</span></span>

<span data-ttu-id="b7f44-108">Fylgið þessum skrefum til að færa inn heiti á skilyrta ákvörðun.</span><span class="sxs-lookup"><span data-stu-id="b7f44-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="b7f44-109">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="b7f44-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b7f44-110">Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir skilyrtu ákvörðunina.</span><span class="sxs-lookup"><span data-stu-id="b7f44-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="b7f44-111">Stilla skilyrði</span><span class="sxs-lookup"><span data-stu-id="b7f44-111">Set conditions</span></span>

<span data-ttu-id="b7f44-112">Kerfið ákveður sjálfkrafa hvaða grein á að nota með því að meta sent fylgiskjal til að ákvarða hvort það fullnægi ákveðnum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="b7f44-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="b7f44-113">Í vinstri glugganum, smelltu á **grunnstillingar**.</span><span class="sxs-lookup"><span data-stu-id="b7f44-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="b7f44-114">Smelltu á **Bæta við Aðgerð**.</span><span class="sxs-lookup"><span data-stu-id="b7f44-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="b7f44-115">Færið inn skilyrði.</span><span class="sxs-lookup"><span data-stu-id="b7f44-115">Enter a condition.</span></span>
4. <span data-ttu-id="b7f44-116">Færa inn viðbótarskilyrði ef þess gerist þörf:</span><span class="sxs-lookup"><span data-stu-id="b7f44-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="b7f44-117">Til að sannreyna að skilyrðin sem voru færð hafi verið sett upp rétt, skal ljúka eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="b7f44-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="b7f44-118">Smellið á **Prófun** til að opna **Kanna verkflæðisskilyrði** skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="b7f44-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="b7f44-119">Veljið færslu í svæðinu **Villuleita skilyrði** á skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="b7f44-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="b7f44-120">Smellið á **Prófun**.</span><span class="sxs-lookup"><span data-stu-id="b7f44-120">Click **Test**.</span></span> <span data-ttu-id="b7f44-121">Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú tiltókst.</span><span class="sxs-lookup"><span data-stu-id="b7f44-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="b7f44-122">Smelltu á **Í lagi** eða **Hætta við** til að fara aftur síðuna **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="b7f44-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>
