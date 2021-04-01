---
title: Bakfæra breytingar í sendingartöflunni
description: Þetta efnisatriði lýsir hvernig á að bakfæra óvistuðum breytingum sem gerðar eru á sendingarspjaldinu.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef7312243cf7e9b890456fbeeeefb85728b4b5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219246"
---
# <a name="reverse-changes-in-a-dispatch-board"></a><span data-ttu-id="dc3dd-103">Bakfæra breytingar í sendingartöflunni</span><span class="sxs-lookup"><span data-stu-id="dc3dd-103">Reverse changes in a dispatch board</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dc3dd-104">Þetta efnisatriði lýsir hvernig á að bakfæra óvistuðum breytingum sem gerðar eru á sendingarspjaldinu.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-104">This topic describes how to reverse unsaved modifications that you make in a dispatch board.</span></span> <span data-ttu-id="dc3dd-105">Til dæmis er úthluta starfsmanni þjónustuverkþátt vista upplýsingar og síðan síðar er ákveðið að úthluta mismunandi starfsmanns á þjónustuverkþátt.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-105">For example, you assign a worker to a service activity, save the information, and then later decide to assign a different worker to the service activity.</span></span> <span data-ttu-id="dc3dd-106">Breyta starfsmanni í sendingartöflunni, og síðan áður en breyting er vistuð, læra starfsmanns sem er úthlutað á sama hátt er ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-106">You modify the worker in the dispatch board, and then, before saving the change, learn that the worker just assigned is not available.</span></span> <span data-ttu-id="dc3dd-107">Ekki er hægt að bakfæra óvistaðar breytingar þannig að upprunalegum starfsmanni er endurúthlutað til þjónustupöntuninarinnar.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-107">You can reverse the unsaved modification so that the original worker is reassigned to the service order.</span></span>

<span data-ttu-id="dc3dd-108">Fylgið eftirfarandi skrefum til að bakfæra óvistaðar breytingar á sendingarspjaldinu:</span><span class="sxs-lookup"><span data-stu-id="dc3dd-108">Use the following steps to reverse unsaved changes in a dispatch board:</span></span>

1.  <span data-ttu-id="dc3dd-109">Smelltu á **Þjónustustjórnun** \> **Reglubundið** \> **Sendingartafla**.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-109">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>

2.  <span data-ttu-id="dc3dd-110">Í skjámyndinni **Sendingartafla** skal slá inn viðeigandi upplýsingar í reitinn og síðan smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-110">In the **Dispatch board** form, enter relevant information in the fields, and then click **OK**.</span></span> 

3.  <span data-ttu-id="dc3dd-111">Til að bakfæra nýjustu breytingu sem er ekki vistuð, skal smella á **Afturkalla**.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-111">To reverse the most recent change that is not saved, click **Undo**.</span></span>

4.  <span data-ttu-id="dc3dd-112">Til að bakfæra röð breytinga sem ekki eru vistaðar skal halda áfram að smella á **Afturkalla** þar til allar breytingar sem þú vilt fleygja hafa verið bakfærðar.</span><span class="sxs-lookup"><span data-stu-id="dc3dd-112">To reverse a series of changes that are not saved, continue clicking **Undo** until each change that you want to discard is reversed.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc3dd-113">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="dc3dd-113">See also</span></span>

[<span data-ttu-id="dc3dd-114">Sendingartafla</span><span class="sxs-lookup"><span data-stu-id="dc3dd-114">Dispatch board</span></span>](dispatch-board.md)

[<span data-ttu-id="dc3dd-115">Þjónustuverkþættir</span><span class="sxs-lookup"><span data-stu-id="dc3dd-115">Service activities</span></span>](service-activities.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]