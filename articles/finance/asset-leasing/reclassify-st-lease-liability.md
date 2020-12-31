---
title: Endurflokka skammtímahluta leiguskuldbindingar
description: Þetta efnisatriði útskýrir hvernig á að stofna mánaðarlega færslubókarfærslu til að endurflokka hluta af leiguskuldbindingunni sem skammtíma.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444574"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="edac7-103">Endurflokka skammtímahluta leiguskuldbindingar</span><span class="sxs-lookup"><span data-stu-id="edac7-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edac7-104">Þetta efnisatriði útskýrir hvernig á að stofna mánaðarlega færslubókarfærslu til að endurflokka hluta af leiguskuldbindingunni sem skammtíma.</span><span class="sxs-lookup"><span data-stu-id="edac7-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="edac7-105">Þegar áætlunin sem er valin í runuvinnslunni er **endurflokkun skammtíma leiguskuldbindingar** er færslubókarfærsla stofnuð.</span><span class="sxs-lookup"><span data-stu-id="edac7-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="edac7-106">Þessi færsla er notuð til að bóka núverandi hluta leiguskuldarinnar á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="edac7-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="edac7-107">Á sama tíma er bakfærsla bókuð frá fyrsta degi næsta mánaðar.</span><span class="sxs-lookup"><span data-stu-id="edac7-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="edac7-108">Skammtímahluti leiguskuldbindingar er sýndur í afskriftaráætlun skuldar.</span><span class="sxs-lookup"><span data-stu-id="edac7-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="edac7-109">Þegar færslubókarfærslan er bókuð verður dálkurinn **Endurflokkunarbók skuldar stofnuð** tiltækur og færslubókarkennið er einnig fyllt út í áætluninni.</span><span class="sxs-lookup"><span data-stu-id="edac7-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="edac7-110">Til að stofna og bóka færslu í endurflokkunarbók skammtímaskuldar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="edac7-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="edac7-111">Opnið **Eignarleiga \> Reglubundið \> Stofnun runubókar**.</span><span class="sxs-lookup"><span data-stu-id="edac7-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="edac7-112">Í svarglugganum **Stofnun runubókar**, á svæðinu **Velja áætlun** skal velja **Endurflokkun skuldbindingar skammtímaleigu**.</span><span class="sxs-lookup"><span data-stu-id="edac7-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="edac7-113">Í reitnum **Leigusamningsflokkur** skal velja leigusamningsflokk.</span><span class="sxs-lookup"><span data-stu-id="edac7-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="edac7-114">Einnig er hægt að velja bókarkennið í reitnum **Bókarkenni** .</span><span class="sxs-lookup"><span data-stu-id="edac7-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="edac7-115">Kveikja skal á færibreytunni **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="edac7-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="edac7-116">Einnig er hægt að stofna færsluna en ekki bóka hana með því að hafa slökkt á þessari færibreytu.</span><span class="sxs-lookup"><span data-stu-id="edac7-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="edac7-117">Kveikja skal á færibreytunni **Forskoða fyrir bókun** til að skoða færsluna áður en hún er bókuð.</span><span class="sxs-lookup"><span data-stu-id="edac7-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="edac7-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="edac7-118">Select **OK**.</span></span>
