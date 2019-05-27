---
title: Skilgreina lokadag fyrir útgáfu framleiðsluflæðis
description: Til að ljúka gildistíma og vinnslu í útgáfu framleiðsluflæðis á tiltekinni dagsetningu eða til að áætla skipti á virkri útgáfu með nýrri útgáfu, þarf að setja inn lokadag í útgáfunni.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0bde90273f9392a36732ed79afdad2eea8bf86
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573212"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="45e41-103">Skilgreina lokadag fyrir útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="45e41-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45e41-104">Til að ljúka gildistíma og vinnslu í útgáfu framleiðsluflæðis á tiltekinni dagsetningu eða til að áætla skipti á virkri útgáfu með nýrri útgáfu, þarf að setja inn lokadag í útgáfunni.</span><span class="sxs-lookup"><span data-stu-id="45e41-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="45e41-105">Ekki er nauðsynlegt til að afvirkja útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="45e41-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="45e41-106">Setja inn lokadagsetningu til að ljúka útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="45e41-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="45e41-107">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="45e41-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="45e41-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="45e41-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="45e41-109">Veljið framleiðsluflæði sem hefur útgáfu sem er þegar skilgreind.</span><span class="sxs-lookup"><span data-stu-id="45e41-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="45e41-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="45e41-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="45e41-111">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="45e41-111">Click Edit.</span></span>
5. <span data-ttu-id="45e41-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="45e41-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="45e41-113">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="45e41-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="45e41-114">Fyrir lokadagsetningu hefst ný útgáfu ekki eða verður virk.</span><span class="sxs-lookup"><span data-stu-id="45e41-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="45e41-115">Það verður ekki heldur lengur hægt að stofna eða hefja vinnslur fyrir þetta framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="45e41-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="45e41-116">Það verður samt hægt að ljúka vinnslum eftir lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="45e41-116">You can still complete started jobs after the expiration date.</span></span>  

