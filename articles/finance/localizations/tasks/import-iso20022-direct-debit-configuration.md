---
title: Flytja inn ISO20022-beingreiðsluskilgreiningu
description: Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d0358c414af20558e7e5aaadad5d9844f7853bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840890"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="2f9fd-103">Flytja inn ISO20022-beingreiðsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="2f9fd-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f9fd-104">Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="2f9fd-105">Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="2f9fd-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="2f9fd-107">Þetta er fyrsta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="2f9fd-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2f9fd-109">Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="2f9fd-110">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-110">Click Set active.</span></span>
4. <span data-ttu-id="2f9fd-111">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-111">Click Repositories.</span></span>
5. <span data-ttu-id="2f9fd-112">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-112">Click Open.</span></span>
6. <span data-ttu-id="2f9fd-113">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-113">Click Show filters.</span></span>
7. <span data-ttu-id="2f9fd-114">Notið eftirfarandi síur: færðu inn síugildi "ISO20022 beingreiðsla (DE)" á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".</span><span class="sxs-lookup"><span data-stu-id="2f9fd-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="2f9fd-115">Einnig má finna skilgreiningu á listanum, veljið það og sleppið þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="2f9fd-116">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-116">Click Import.</span></span>
    * <span data-ttu-id="2f9fd-117">Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="2f9fd-118">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="2f9fd-118">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]