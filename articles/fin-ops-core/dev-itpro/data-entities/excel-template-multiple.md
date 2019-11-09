---
title: Flytja inn gögn frá Excel-gagnaeiningasniðmátum sem eru með mörgum vinnublöðum
description: Þetta efnisatriði lýsir því hvernig skal flytja gögn með því að nota Excel gagnaeiningasniðmát inn í Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: e27b657d3d38ace158bcf4481d1445195147816b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181957"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="a514b-103">Flytja inn gögn frá Excel-gagnaeiningasniðmátum sem eru með mörgum vinnublöðum</span><span class="sxs-lookup"><span data-stu-id="a514b-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a514b-104">Gagnastjórnun í forritinu styður sem byggjast á sniðmátum Microsoft Excel fyrir gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="a514b-104">Data management in the application supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="a514b-105">Þessi sniðmát geta innihaldið einn eða fleiri vinnublöð.</span><span class="sxs-lookup"><span data-stu-id="a514b-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="a514b-106">Sniðmát með mörgum vinnublöðum eru oft notaðar þegar auðvelt er að stýra gögnum í einni skrá og flytja hana inn í margar gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="a514b-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="a514b-107">Dæmi um þetta væri svæði og vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a514b-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="a514b-108">Hlaða upp skrá einu sinni og varpa henni til allra eininga</span><span class="sxs-lookup"><span data-stu-id="a514b-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="a514b-109">Við skulum taka dæmi þar sem ein Excel-skrá með vinnublöðum sem kallast **Svæði** og **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="a514b-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="a514b-110">Til að setja upp gagnainnflutningsverkið myndir þú nýskrá fyrstu gagnaeininguna, **Svæði** og síðan hlaða upp skránni.</span><span class="sxs-lookup"><span data-stu-id="a514b-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="a514b-111">Þú munt geta valið **Svæði** sem vinnublaðið sem verður notað fyrir þessa einingu.</span><span class="sxs-lookup"><span data-stu-id="a514b-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="a514b-112">Ef þú skráir til viðbótar aðra einingu **Vöruhús** án þess að fara úr **Bæta við skrá** skráarsniðinu, þá mun vinnublaðsleitin leyfa þér að velja vinnublaðið **Vöruhús** án þess að þurfa að hlaða skránni upp aftur.</span><span class="sxs-lookup"><span data-stu-id="a514b-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="a514b-113">Eina ástæðan fyrir því að hlaða inn nýjum skrá væri ef **Vöruhús** gögnin voru í annarri skrá.</span><span class="sxs-lookup"><span data-stu-id="a514b-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Mörg vinnublöð](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="a514b-115">Festa vinnublað til einingarvörpunar</span><span class="sxs-lookup"><span data-stu-id="a514b-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="a514b-116">Vörpun vinnublaðsins til gagnaeiningar í innflutningsverkinu er hægt að festa frá hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="a514b-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="a514b-117">**Vinnublað** dálkurinn í hnitanetinu sýnir vinnublaðið úr skránni sem var varpað.</span><span class="sxs-lookup"><span data-stu-id="a514b-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="a514b-118">Þú getur valið annað vinnublað úr fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="a514b-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="a514b-119">Ef valið vinnublað er þegar varpað í einingu í gagnaverkinu biður kerfið þig um að staðfesta breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="a514b-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="a514b-120">Við mælum með að þú festir allar varpanir í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="a514b-120">We recommend that you fix all mappings in the grid.</span></span>

![Uppfæra vörpun vinnublaðs](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="a514b-122">Endurvarpa á nýja skrá</span><span class="sxs-lookup"><span data-stu-id="a514b-122">Re-map to a new file</span></span>

<span data-ttu-id="a514b-123">Í tilfellum þar sem ný útgáfa af sömu skrá eða algjörri nýju skrá verður að hlaða upp fyrir fyrirliggjandi einingar í gagnaverki, verður þú að nota **Bæta við skrá** upplifuninni og bæta einingunum við aftur eins og verið væri að setja þær inn í fyrsta sinn.</span><span class="sxs-lookup"><span data-stu-id="a514b-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="a514b-124">Kerfið mun staðfesta að þú viljir skrifa yfir fyrirliggjandi einingar í gagnaverkinu áður en haldið er áfram.</span><span class="sxs-lookup"><span data-stu-id="a514b-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="a514b-125">Einingar sem ekki er bætt við aftur (eða skrifað yfir) munu áfram halda fyrri vörpunum úr fyrri skrá.</span><span class="sxs-lookup"><span data-stu-id="a514b-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="a514b-126">Hlaða upp skrá með því að nota Keyra verk</span><span class="sxs-lookup"><span data-stu-id="a514b-126">Upload a file using Run project</span></span>

<span data-ttu-id="a514b-127">Þú getur hlaðið upp Excel-skrá meðan þú notar **Keyra verk** valmöguleikann til að framkvæma innflutningsverk.</span><span class="sxs-lookup"><span data-stu-id="a514b-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="a514b-128">Þú verður að gæta þess að hlaða aðeins upp skrám sem eru með sömu vinnublaði og fyrirliggjandi varpanir á gagnaeiningarnar í gagnaverkinu.</span><span class="sxs-lookup"><span data-stu-id="a514b-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="a514b-129">Ef vinnublað er ekki að finna í skránni sem nýlega var hlaðið upp, birtir kerfið villu og stoppar innflutning.</span><span class="sxs-lookup"><span data-stu-id="a514b-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="a514b-130">Ef breyta verður vörpunin á vinnublaðið fyrir einingu, þá verður að uppfæra varpanirnar í gagnaverkinu fyrst innan frá gagnaverkinu, áður en þú notar skrána í **Keyra verk** upplifuninni.</span><span class="sxs-lookup"><span data-stu-id="a514b-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>