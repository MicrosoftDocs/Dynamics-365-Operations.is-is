---
title: Flytja inn ISO20022-beingreiðsluskilgreiningu
description: Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eee00021f49ac0110d7bde07faba8095348e1b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185751"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="87d5c-103">Flytja inn ISO20022-beingreiðsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="87d5c-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87d5c-104">Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="87d5c-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="87d5c-105">Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="87d5c-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="87d5c-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="87d5c-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="87d5c-107">Þetta er fyrsta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="87d5c-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="87d5c-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="87d5c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="87d5c-109">Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87d5c-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="87d5c-110">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="87d5c-110">Click Set active.</span></span>
4. <span data-ttu-id="87d5c-111">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="87d5c-111">Click Repositories.</span></span>
5. <span data-ttu-id="87d5c-112">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="87d5c-112">Click Open.</span></span>
6. <span data-ttu-id="87d5c-113">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="87d5c-113">Click Show filters.</span></span>
7. <span data-ttu-id="87d5c-114">Notið eftirfarandi síur: færðu inn síugildi "ISO20022 beingreiðsla (DE)" á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".</span><span class="sxs-lookup"><span data-stu-id="87d5c-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="87d5c-115">Einnig má finna skilgreiningu á listanum, veljið það og sleppið þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="87d5c-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="87d5c-116">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="87d5c-116">Click Import.</span></span>
    * <span data-ttu-id="87d5c-117">Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="87d5c-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="87d5c-118">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="87d5c-118">Click Yes.</span></span>

