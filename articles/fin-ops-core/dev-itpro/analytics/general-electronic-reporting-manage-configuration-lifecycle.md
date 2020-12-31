---
title: Stjórnun á lífsferli grunnstillingar fyrir rafræna skýrslugerð
description: Þetta efnisatriði lýsir hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Microsoft Dynamics 365 Finance-lausnina.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a4741784103817c270c4c7f730753ba59a327d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682624"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="2ee04-103">Stjórnun á lífsferli grunnstillingar fyrir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="2ee04-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ee04-104">Þetta efnisatriði lýsir hvernig á að stjórna lífsferli skilgreininga rafrænnar skýrslugerðar (ER) fyrir Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2ee04-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="2ee04-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="2ee04-105">Overview</span></span>

<span data-ttu-id="2ee04-106">Rafræn skýrslugerð (ER) er kerfi til að styðja lögboðin og landsértæk rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="2ee04-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="2ee04-107">Almennt hefur ER möguleikann á að framkvæma eftirfarandi verkefni fyrir stakt rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="2ee04-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="2ee04-108">Frekari upplýsingar eru í [Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="2ee04-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="2ee04-109">Að hanna sniðmát fyrir rafrænt skjal:</span><span class="sxs-lookup"><span data-stu-id="2ee04-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="2ee04-110">Auðkenna áskilinn uppruna gagna sem má setja fram í þessu fylgiskjali:</span><span class="sxs-lookup"><span data-stu-id="2ee04-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="2ee04-111">Undirliggjandi gögn, t.d. gagnatöflur, gagnaeiningar og flokkar.</span><span class="sxs-lookup"><span data-stu-id="2ee04-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="2ee04-112">Ferlistengdir eiginleikar, t.d. dagsetning og tími keyrslu og tímabelti.</span><span class="sxs-lookup"><span data-stu-id="2ee04-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="2ee04-113">Innsláttarfæribreytur notanda, tilgreindar af notanda á keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="2ee04-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="2ee04-114">Skilgreina þarf nauðsynlegar einingar skjals sem og grannfræði þess til að tilgreina snið endanlegs skjals.</span><span class="sxs-lookup"><span data-stu-id="2ee04-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="2ee04-115">Skilgreina þarf æskilegt flæði gagna frá völdum gagnagjafa til skilgreindra eininga skjals (í gegnum tengingar gagnagjafa við sniðsþætti skjals) og tilgreina rök vinnslustjórnunar.</span><span class="sxs-lookup"><span data-stu-id="2ee04-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="2ee04-116">Gera sniðmát tiltækt þannig að hægt er að nota það í öðrum tilvikum:</span><span class="sxs-lookup"><span data-stu-id="2ee04-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="2ee04-117">Umbreyta sniðmáti skjals sem var stofnað yfir í ER skilgreiningu og flytja afbrigði úr núverandi forritstilviki sem xml-pakka sem hægt er að geyma annaðhvort staðbundið eða í LCS.</span><span class="sxs-lookup"><span data-stu-id="2ee04-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="2ee04-118">Umbreyta skilgreiningu ER í skjalasniðmát forrits.</span><span class="sxs-lookup"><span data-stu-id="2ee04-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="2ee04-119">Flytja inn xml-pakka sem geymdur er annað hvort staðbundið eða í LCS yfir í gildandi tilvik.</span><span class="sxs-lookup"><span data-stu-id="2ee04-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="2ee04-120">Sérsníða sniðmát rafræna skjalsins:</span><span class="sxs-lookup"><span data-stu-id="2ee04-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="2ee04-121">Flytja sniðmát úr LCS yfir í núverandi tilvik sem ER-skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="2ee04-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="2ee04-122">Hanna sérsniðna útgáfu ER skilgreiningar og halda tilvísun í grunnútgáfu hennar.</span><span class="sxs-lookup"><span data-stu-id="2ee04-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="2ee04-123">Samþætta sniðmát við tiltekið viðskiptaferli, þannig að það sé tiltækt í forritinu:</span><span class="sxs-lookup"><span data-stu-id="2ee04-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="2ee04-124">Skilgreina stillingar þannig að forritið byrjar að nota ER-skilgreiningu með því að vísa í þá skilgreiningu í færibreytu sem er í tengslum við vinnslu.</span><span class="sxs-lookup"><span data-stu-id="2ee04-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="2ee04-125">Til dæmis vísa í skilgreiningu rafrænnar skýrslugerðar í tilteknum greiðslumáta fyrir viðskiptaskuldir til að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga.</span><span class="sxs-lookup"><span data-stu-id="2ee04-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="2ee04-126">Nota sniðmát í tilteknu viðskiptaferli:</span><span class="sxs-lookup"><span data-stu-id="2ee04-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="2ee04-127">Keyra skilgreiningu rafrænnar skýrslugerðar í tilteknu viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="2ee04-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="2ee04-128">Til dæmis til að mynda skilaboð rafrænnar greiðslu fyrir úrvinnslu reikninga þegar greiðslumáti sem vísar til skilgreiningar rafrænnar skýrslugerðar er valinn.</span><span class="sxs-lookup"><span data-stu-id="2ee04-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="2ee04-129">Hugtök</span><span class="sxs-lookup"><span data-stu-id="2ee04-129">Concepts</span></span>
<span data-ttu-id="2ee04-130">Eftirfarandi hlutverk og tengdar aðgerðir tengjast lífsferli skilgreiningar rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="2ee04-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="2ee04-131">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="2ee04-131">Role</span></span>                                       | <span data-ttu-id="2ee04-132">Verkþættir</span><span class="sxs-lookup"><span data-stu-id="2ee04-132">Activities</span></span>                                                      | <span data-ttu-id="2ee04-133">lýsing</span><span class="sxs-lookup"><span data-stu-id="2ee04-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="2ee04-134">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="2ee04-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="2ee04-135">Stofna og stjórna íhlutum ER (líkön og snið).</span><span class="sxs-lookup"><span data-stu-id="2ee04-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="2ee04-136">Viðskiptaaðili sem hannar sértæk gagnalíkön rafrænnar skýrslugerðar fyrir tiltekin svið hannar áskilin sniðmát fyrir rafræn skjöl og tengir þau saman á viðeigandi hátt.</span><span class="sxs-lookup"><span data-stu-id="2ee04-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="2ee04-137">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="2ee04-137">Electronic reporting developer</span></span>             | <span data-ttu-id="2ee04-138">Stofnar og stjórnar vörpunum gagnalíkana.</span><span class="sxs-lookup"><span data-stu-id="2ee04-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="2ee04-139">Sérfræðingur sem velur viðeigandi Finance gagnagjafa og tengir þá við lénasértæk ER gagnalíkön.</span><span class="sxs-lookup"><span data-stu-id="2ee04-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="2ee04-140">Yfirmaður bókhalds</span><span class="sxs-lookup"><span data-stu-id="2ee04-140">Accounting supervisor</span></span>                      | <span data-ttu-id="2ee04-141">Skilgreinir stillingar á ferlum sem vísa til ER gervinga.</span><span class="sxs-lookup"><span data-stu-id="2ee04-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="2ee04-142">Til dæmis hlutverkið **Yfirmaður bókhalds** sem leyfir að nota stillingar skilgreiningar rafrænnar skýrslugerðar fyrir tiltekinn greiðslumáta viðskiptaskulda til að geta búið til rafræn greiðsluskilaboð fyrir úrvinnslu reikninga.</span><span class="sxs-lookup"><span data-stu-id="2ee04-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="2ee04-143">Starfsmaður viðskiptaskuldagreiðslna</span><span class="sxs-lookup"><span data-stu-id="2ee04-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="2ee04-144">Notar ER gervinga í tilteknu viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="2ee04-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="2ee04-145">Til dæmis hlutverk **Starfsmanns viðskiptaskuldagreiðslna** sem leyfir að mynda rafræn greiðsluskilaboð fyrir úrvinnslu reikninga, byggt á sniði rafrænnar skýrslugerðar sem er skilgreint fyrir tiltekinn greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="2ee04-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="2ee04-146">Þróunarlífsferill ER skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="2ee04-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="2ee04-147">Af eftirfarandi ER-tengdum ástæðum er mælt með að hanna ER skilgreiningar í þróunarumhverfi sem aðskilið tilvik af Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="2ee04-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="2ee04-148">Notendur í hlutverkum annaðhvort **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** geta breytt stillingum og keyrt þær vegna prófunar.</span><span class="sxs-lookup"><span data-stu-id="2ee04-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="2ee04-149">Það getur valdið köllun eftir aðferðum flokka og töflum sem geta hugsanlega verið skaðleg fyrir viðskiptagögn og árangur af notkun tilviks.</span><span class="sxs-lookup"><span data-stu-id="2ee04-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="2ee04-150">Köllun eftir aðferðum flokka og tafla sem ER gagnagjafa fyrir ER skilgreiningar eru ekki takmarkaðar af aðgangsstað og skráðu efni fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="2ee04-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="2ee04-151">Því geta notendur sem eru í hlutverkum **Þróunaraðila rafrænnar skýrslugerðar** eða **Hagnýts ráðgjafa vegna rafrænnar skýrslugerðar** fengið aðgang að viðkvæmum gögnum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="2ee04-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="2ee04-152">Skilgreiningar rafrænar skýrslugerðar sem eru hannaðar í þróunarumhverfi má hlaða upp í prófunarumhverfi fyrir skilgreiningarmat (rétt samþætting vinnslu, nákvæmni niðurstaða og afköst) og gæðatryggingu, til dæmis réttmæti aðgangsheimilda sem eru knúin af hlutverkum, aðskilnaður á skyldum o.s.frv..</span><span class="sxs-lookup"><span data-stu-id="2ee04-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="2ee04-153">Hægt er að nota eiginleika til að skiptast á skilgreiningum rafrænnar skýrslugerðar í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="2ee04-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="2ee04-154">Loks er hægt að hlaða upp sönnuðum skilgreiningum rafrænnar skýrslugerðar annaðhvort í LCS til að deila með áskrifendum þjónustu eða í framleiðsluumhverfi til innri notkunar, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="2ee04-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![Lífsferill skilgreiningar rafrænnar skýrslugerðar](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="2ee04-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2ee04-156">Additional resources</span></span>

[<span data-ttu-id="2ee04-157">Yfirlit yfir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="2ee04-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
