--- 
title: "Flytja inn ISO20022-beingreiðsluskilgreiningu"
description: "Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ea88fd6edca291db984223413f671eec8935fc9a
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="600d7-103">Flytja inn ISO20022-beingreiðsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="600d7-103">Import ISO20022 direct debit configuration</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="600d7-104">Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="600d7-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="600d7-105">Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="600d7-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="600d7-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="600d7-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="600d7-107">Þetta er fyrsta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="600d7-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="600d7-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="600d7-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="600d7-109">Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.</span><span class="sxs-lookup"><span data-stu-id="600d7-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="600d7-110">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="600d7-110">Click Set active.</span></span>
4. <span data-ttu-id="600d7-111">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="600d7-111">Click Repositories.</span></span>
5. <span data-ttu-id="600d7-112">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="600d7-112">Click Open.</span></span>
6. <span data-ttu-id="600d7-113">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="600d7-113">Click Show filters.</span></span>
7. <span data-ttu-id="600d7-114">Notið eftirfarandi síur: færðu inn síugildi "ISO20022 beingreiðsla (DE)"  á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".</span><span class="sxs-lookup"><span data-stu-id="600d7-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="600d7-115">Einnig má finna skilgreiningu á listanum, veljið það og sleppið þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="600d7-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="600d7-116">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="600d7-116">Click Import.</span></span>
    * <span data-ttu-id="600d7-117">Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="600d7-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="600d7-118">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="600d7-118">Click Yes.</span></span>


