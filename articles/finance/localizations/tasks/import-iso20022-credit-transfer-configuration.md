---
title: Flytja inn skilgreiningu ISO20022-kreditfærslu
description: Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu lánardrottins.
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
ms.openlocfilehash: 4a96827bc6e126a7f5de6d67338b5233a65d93c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840914"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="ff6c4-103">Flytja inn skilgreiningu ISO20022-kreditfærslu</span><span class="sxs-lookup"><span data-stu-id="ff6c4-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff6c4-104">Þessi verklýsing sýnir hvernig á að flytja inn skilgreiningu rafrænnar skýrslugerðar fyrir greiðslu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="ff6c4-105">Þýska ISO 20022 snið millifærsla fjármuna er notað sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="ff6c4-106">Hægt að nota þetta ferli fyrir aðrar tiltækt snið fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="ff6c4-107">Þetta verkefni var stofnuð með því að nota sýnigögn fyrirtækisins DEMF en hægt er að nota hvaða sýnigögn fyrirtækis til að ljúka þessu verki.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="ff6c4-108">Þetta er fyrsta af fimm verkefnum sem saman lýsa greiðsluferlinu lánardrottins með því að nota grunnstillingar fyrir rafræna skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ff6c4-109">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="ff6c4-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ff6c4-111">Í lista yfir tiltæka veitandi skilgreininga, veljið Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="ff6c4-112">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-112">Click Set active.</span></span>
4. <span data-ttu-id="ff6c4-113">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-113">Click Repositories.</span></span>
5. <span data-ttu-id="ff6c4-114">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-114">Click Open.</span></span>
6. <span data-ttu-id="ff6c4-115">Smellt er á Sýna síur.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-115">Click Show filters.</span></span>
7. <span data-ttu-id="ff6c4-116">Notið eftirfarandi síur: færðu inn síugildi "ISO20022 millifærsla fjármuna (DE)" á reitnum "heiti skilgreiningar" með því að nota síuvirknitáknið "byrjar á".</span><span class="sxs-lookup"><span data-stu-id="ff6c4-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="ff6c4-117">Einnig má finna skilgreiningu á listanum, veljið það og flytja í innflutningsverkið.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="ff6c4-118">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-118">Click Import.</span></span>
    * <span data-ttu-id="ff6c4-119">Ef hnappurinn Innflutningur er ekki tiltækur, merkir það að þessi skilgreining hefur þegar verið flutt inn.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="ff6c4-120">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="ff6c4-120">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]