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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1757a1477e46f71e327bb70cf4780767b7509e55
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568724"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="37647-103">Flytja inn ISO20022-beingreiðsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="37647-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37647-104">Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="37647-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="37647-105">Þessi aðferð notar snið ISO-20022 beingreiðslu sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="37647-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="37647-106">Þetta ferli var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="37647-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="37647-107">Þetta er fyrsta af fimm ferlum sem lýsa greiðsluferlinu viðskiptavinar með grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="37647-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="37647-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="37647-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="37647-109">Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.</span><span class="sxs-lookup"><span data-stu-id="37647-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="37647-110">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="37647-110">Click Set active.</span></span>
4. <span data-ttu-id="37647-111">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="37647-111">Click Repositories.</span></span>
5. <span data-ttu-id="37647-112">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="37647-112">Click Open.</span></span>
6. <span data-ttu-id="37647-113">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="37647-113">Click Show filters.</span></span>
7. <span data-ttu-id="37647-114">Notið eftirfarandi síur: færðu inn síugildi "ISO20022 beingreiðsla (DE)"  á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".</span><span class="sxs-lookup"><span data-stu-id="37647-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="37647-115">Einnig má finna skilgreiningu á listanum, veljið það og sleppið þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="37647-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="37647-116">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="37647-116">Click Import.</span></span>
    * <span data-ttu-id="37647-117">Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="37647-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="37647-118">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="37647-118">Click Yes.</span></span>

