---
title: Tilgreina sérsniðinn geymslustað fyrir skjöl sem eru mynduð
description: Þetta efnisatriði útskýrir hvernig á að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3ea9de81045dfd01ffec2c8a1d98ea2ba4f2c49a
ms.sourcegitcommit: 0e01d3907b70261aee2df3e3ce0dde2f1343a43a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/27/2019
ms.locfileid: "770089"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="82e0e-103">Tilgreina sérsniðinn geymslustað fyrir skjöl sem eru mynduð</span><span class="sxs-lookup"><span data-stu-id="82e0e-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82e0e-104">Forritunarviðmót forritsins (API) fyrir ramma rafrænnar skýrslugerðar gerir þér kleift að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar.</span><span class="sxs-lookup"><span data-stu-id="82e0e-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="82e0e-105">Í þessu efnisatriði er að finna yfirlit aðalverkefnanna sem þarf að klára til að bæta við sérsniðnum geymslustað.</span><span class="sxs-lookup"><span data-stu-id="82e0e-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="82e0e-106">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="82e0e-106">Prerequisites</span></span>

<span data-ttu-id="82e0e-107">Þú verður að setja upp Microsoft Dynamics 365 for Finance and Operations grannfræði sem styður samfellda smíði.</span><span class="sxs-lookup"><span data-stu-id="82e0e-107">You must deploy a Microsoft Dynamics 365 for Finance and Operations topology that supports continuous build.</span></span> <span data-ttu-id="82e0e-108">(Nánari upplýsingar er að finna í [Setja upp grannfræði sem styður samfellda smíði og sjálfvirkni prófunar](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Þú verður að hafa aðgang að þessari grannfræði Finance and Operations fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="82e0e-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this Finance and Operations topology for one of the following roles:</span></span>

- <span data-ttu-id="82e0e-109">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="82e0e-109">Electronic reporting developer</span></span>
- <span data-ttu-id="82e0e-110">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="82e0e-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="82e0e-111">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="82e0e-111">System administrator</span></span>

<span data-ttu-id="82e0e-112">Þú verður einnig að hafa aðgang að þróunarumhverfi fyrir þessa grannfræði Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="82e0e-112">You must also have access to the development environment for this Finance and Operations topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="82e0e-113">Búa til eða flytja inn skilgreiningu fyrir snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="82e0e-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="82e0e-114">Í núverandi grannfræði Finance and Operations, [búa til nýtt snið rafrænnar skýrslugerðar](tasks/er-format-configuration-2016-11.md) til að mynda skjöl sem áformað er að bæta við sérsniðinn geymslustað.</span><span class="sxs-lookup"><span data-stu-id="82e0e-114">In the current Finance and Operations topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="82e0e-115">Annars [flytja núverandi snið rafrænnar skýrslugerðar inn í þessa grannfræði](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="82e0e-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Síða sniðshönnuðar](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="82e0e-117">Snið rafrænnar skýrslugerðar sem þú býrð til eða flytur inn verður að innihalda að minnsta kosti eina af eftirfarandi sniðseiningum:</span><span class="sxs-lookup"><span data-stu-id="82e0e-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="82e0e-118">Skrá</span><span class="sxs-lookup"><span data-stu-id="82e0e-118">File</span></span>
> - <span data-ttu-id="82e0e-119">Mappa</span><span class="sxs-lookup"><span data-stu-id="82e0e-119">Folder</span></span>
> - <span data-ttu-id="82e0e-120">Samruni</span><span class="sxs-lookup"><span data-stu-id="82e0e-120">Merger</span></span>
> - <span data-ttu-id="82e0e-121">Viðhengi</span><span class="sxs-lookup"><span data-stu-id="82e0e-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="82e0e-122">Stofna nýja gerð skjala</span><span class="sxs-lookup"><span data-stu-id="82e0e-122">Create a new document type</span></span>

<span data-ttu-id="82e0e-123">Til að tilgreina hvernig skjöl eru send sem snið rafrænnar skýrslugerðar myndar er nauðsynlegt að skilgreina [Viðtökustaðir rafrænnar skýrslugerðar](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="82e0e-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="82e0e-124">Í sérhverjum viðtökustað rafrænnar skýrslugerðar sem er skilgreindur til að geyma mynduð skjöl sem skrár, þarf að tilgreina gerð skjals fyrir skjalastjórnunarramma.</span><span class="sxs-lookup"><span data-stu-id="82e0e-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="82e0e-125">Mismunandi skjalagerðir er hægt að nota til að senda skjöl sem mismunandi snið rafrænnar skýrslugerðar mynda.</span><span class="sxs-lookup"><span data-stu-id="82e0e-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="82e0e-126">Bæta við nýrri [skjalagerð](../../fin-and-ops/organization-administration/configure-document-management.md) fyrir snið rafrænnar skýrslugerðar sem þú bjóst til eða fluttir inn áður.</span><span class="sxs-lookup"><span data-stu-id="82e0e-126">Add a new [document type](../../fin-and-ops/organization-administration/configure-document-management.md) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="82e0e-127">Í skýringarmyndinni sem fylgir er skjalagerðin **FileX**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="82e0e-128">Til að aðgreina þessa skjalategund frá öðrum skjalategundum skal hafa með tiltekið lykilorð í heitinu.</span><span class="sxs-lookup"><span data-stu-id="82e0e-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="82e0e-129">Til dæmis, í skýringarmyndinni sem fylgir er heitið **(LOCAL) mappa**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="82e0e-130">Í reitnum **Klasi** skal tilgreina **Hengja skrá við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="82e0e-131">Í reitnum **Flokkur** skal tilgreina **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-131">In the **Group** field, specify **File**.</span></span>

![Síðan Gerðir skjala](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="82e0e-133">Gerðir skjala miðast við fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="82e0e-133">Document types are company-specific.</span></span> <span data-ttu-id="82e0e-134">Til að nota snið rafrænnar skýrslugerðar með skilgreindum viðtökustað í mörgum fyrirtækjum verður að skilgreina aðskilda gerð skjals í hverju fyrirtæki fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="82e0e-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="82e0e-135">Yfirfara frumkóða</span><span class="sxs-lookup"><span data-stu-id="82e0e-135">Review source code</span></span>

<span data-ttu-id="82e0e-136">Yfirfara kóða aðferðarinnar **insertFile()** af klasanum **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="82e0e-137">Takið eftir að tilvikið **AttachingFile()** kemur upp á meðan myndaða skráin er hengd við færslu.</span><span class="sxs-lookup"><span data-stu-id="82e0e-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="82e0e-138">Tilvikið **AttachingFile()** kemur upp þegar unnið er úr eftirfarandi viðtökustöðum rafrænnar skýrslugerðar:</span><span class="sxs-lookup"><span data-stu-id="82e0e-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="82e0e-139">**Safnvista** - Þegar þessi viðtökustaður er notaður er búin til ný færsla í töflunni ERFormatMappingRunJobTable fyrir það snið rafrænnar skýrslugerðar sem er keyrt.</span><span class="sxs-lookup"><span data-stu-id="82e0e-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="82e0e-140">Svæðið **Safnvistað** í þessari færslu er stillt á **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="82e0e-141">Ef keyrsla á sniði rafrænnar skýrslugerðar tekst er myndaða skjalið hengt við þessa færslu og tilvikið **AttachingFile()** kemur upp.</span><span class="sxs-lookup"><span data-stu-id="82e0e-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="82e0e-142">Gerð skjals sem er valið í þessum viðtökustað rafrænnar skýrslugerðar ákvarðar geymslustaðinn fyrir viðhengda skrá (Microsoft Azure Geymsla eða Microsoft SharePoint mappa).</span><span class="sxs-lookup"><span data-stu-id="82e0e-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="82e0e-143">**Safnvistun vinnslu** - Þegar þessi viðtökustaður er notaður er búin til ný færsla í töflunni ERFormatMappingRunJobTable fyrir það snið rafrænnar skýrslugerðar sem er keyrt.</span><span class="sxs-lookup"><span data-stu-id="82e0e-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="82e0e-144">Svæðið **Safnvistað** í þessari færslu er stillt á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="82e0e-145">Ef keyrsla á sniði rafrænnar skýrslugerðar tekst er myndaða skjalið hengt við þessa færslu og tilvikið **AttachingFile()** kemur upp.</span><span class="sxs-lookup"><span data-stu-id="82e0e-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="82e0e-146">Gerð skjals sem er skilgreind í færibreytum rafrænnar skýrslugerðar ákvarðar geymslustaðinn fyrir viðhengda skrá (Azure-geymsla eða SharePoint mappa).</span><span class="sxs-lookup"><span data-stu-id="82e0e-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Síða rafrænna skýrslufæribreyta](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="82e0e-148">Skilgreina viðtökustað rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="82e0e-148">Configure an ER destination</span></span>

1. <span data-ttu-id="82e0e-149">Skilgreina safnvistaðan viðtökustað fyrir einn af áðurnefndum þáttum (skrá, mappa, samruni eða viðhengi) í sniði rafrænnar skýrslugerðar sem var búinn til eða fluttur inn.</span><span class="sxs-lookup"><span data-stu-id="82e0e-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="82e0e-150">Til leiðbeiningar skal sjá [Viðtökustaðir rafrænnar skýrslugerðar](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="82e0e-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="82e0e-151">Notaðu gerð skjals sem þú bættir við á undan fyrir skilgreindan viðtökustað.</span><span class="sxs-lookup"><span data-stu-id="82e0e-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="82e0e-152">(Fyrir dæmið í þessu efnisatriði er gerð skjals **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="82e0e-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Svargluggi áfangastaðastillinga](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="82e0e-154">Breyta frumkóða</span><span class="sxs-lookup"><span data-stu-id="82e0e-154">Modify source code</span></span>

1. <span data-ttu-id="82e0e-155">Bæta nýjum klasa við Microsoft Visual Studio verkið og skrifa kóða til að gerast áskrifandi að tilvikinu **AttachingFile()** sem var minnst á hér á undan.</span><span class="sxs-lookup"><span data-stu-id="82e0e-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="82e0e-156">(Nánari upplýsingar um mynstur stækkunarhæfni sem er notað skal sjá [Svara með því að nota EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Til dæmis, í nýja klasanum, skrifa kóða sem framkvæmir eftirfarandi aðgerðir:</span><span class="sxs-lookup"><span data-stu-id="82e0e-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="82e0e-157">Geymið myndaðar skrár í möppu staðbundins skráakerfis á þjóninum sem keyrir AOS-þjónustu.</span><span class="sxs-lookup"><span data-stu-id="82e0e-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="82e0e-158">Geymið aðeins þessar mynduðu skrár þegar nýja skjalagerðin (til dæmis gerðin **FileX** sem er með lykilorðið „(LOCAL)“ í heitinu) er notuð þegar skrá er hengd við færsluna í kladda fyrir vinnsluverk rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="82e0e-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="82e0e-159">Endursmíðaðu verkefnið þitt.</span><span class="sxs-lookup"><span data-stu-id="82e0e-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="82e0e-160">Keyra snið rafrænnar skýrslugerðar var búið til eða flutt inn</span><span class="sxs-lookup"><span data-stu-id="82e0e-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="82e0e-161">Framkvæma snið rafrænnar skýrslugerðar sem var búið til eða flutt inn.</span><span class="sxs-lookup"><span data-stu-id="82e0e-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="82e0e-162">Farðu í **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Vinnslur rafrænnar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="82e0e-163">Finndu skrána sem var búin til fyrir þetta vinnsluverk, og sem hefur myndaða skrá sem viðhengi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="82e0e-164">Kannaðu staðbundna **C:\\0** möppu til að finna sömu mynduðu skrá.</span><span class="sxs-lookup"><span data-stu-id="82e0e-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82e0e-165">Frekari tilföng</span><span class="sxs-lookup"><span data-stu-id="82e0e-165">Additional resources</span></span>

- [<span data-ttu-id="82e0e-166">Viðtökustaðir rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="82e0e-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="82e0e-167">Heimasíða stækkunarhæfni</span><span class="sxs-lookup"><span data-stu-id="82e0e-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)
