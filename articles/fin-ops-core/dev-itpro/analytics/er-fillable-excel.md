---
title: Hanna skilgreiningu fyrir myndun skjala á Excel-sniði
description: Þetta efnisatriði veitir upplýsingar um hvernig á að hanna snið rafrænnar skýrslugerðar til að fylla út Excel-sniðmát og stofna Excel-skjöl á útleið.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375814"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="56e4c-103">Hanna skilgreiningu fyrir myndun skjala á Excel-sniði</span><span class="sxs-lookup"><span data-stu-id="56e4c-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="56e4c-104">Hægt er að hanna skilgreiningu [rafræns skýrslugerðarsniðs (ER)](general-electronic-reporting.md) sem er með [sniðsþátt](general-electronic-reporting.md#FormatComponentOutbound) rafrænnar skýrslugerðar sem hægt er að skilgreina til að mynda skjal á útleið á Microsoft Excel-vinnubókarsniði.</span><span class="sxs-lookup"><span data-stu-id="56e4c-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="56e4c-105">Nota verður tiltekna sniðsþætti rafrænnar skýrslugerðar í þessum tilgangi.</span><span class="sxs-lookup"><span data-stu-id="56e4c-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="56e4c-106">Til að læra meira um þennan eiginleika skal fylgja skrefunum í efnisatriði [Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="56e4c-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="56e4c-107">Bæta við nýju sniði rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="56e4c-107">Add a new ER format</span></span>

<span data-ttu-id="56e4c-108">Þegar skilgreiningu nýs sniðs rafrænnar skýrslugerðar er bætt við til að mynda skjal á útleið á Excel-vinnubókarsniði verður annaðhvort að velja **Excel**-gildið fyrir eigindina **Sniðsgerð** fyrir sniðið eða hafa eigindina **Sniðsgerð** auða.</span><span class="sxs-lookup"><span data-stu-id="56e4c-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="56e4c-109">Ef **Excel** er valið er hægt að skilgreina sniðið til að mynda skjal á útleið aðeins á Excel-sniði.</span><span class="sxs-lookup"><span data-stu-id="56e4c-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="56e4c-110">Ef eigindin er höfð auð er hægt að skilgreina sniðið til að mynda skjal á útleið á hvaða því sniði sem rafræna skýrslugerðin styður.</span><span class="sxs-lookup"><span data-stu-id="56e4c-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="56e4c-111">Til að skilgreina sniðsþátt rafrænnar skýrslugerðar skal velja **Hönnuður** á aðgerðasvæðinu og opna sniðsþátt rafrænnar skýrslugerðar fyrir breytingar í aðgerðarhönnuði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Skilgreiningasíða](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="56e4c-113">Excel-skrárþáttur</span><span class="sxs-lookup"><span data-stu-id="56e4c-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="56e4c-114">Handvirk færsla</span><span class="sxs-lookup"><span data-stu-id="56e4c-114">Manual entry</span></span>

<span data-ttu-id="56e4c-115">Bæta þarf þætti **Excel\\-skráar** við skilgreint snið rafrænnar skýrslugerðar til að mynda skjal á útleið á Excel-sniði.</span><span class="sxs-lookup"><span data-stu-id="56e4c-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\skráarþáttur](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="56e4c-117">Til að tilgreina útlit skjals á útleið skal hengja Excel-vinnubók með .xlsx skrárendingu við þátt **Excel\\-skrárinnar** sem sniðmát fyrir skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="56e4c-118">Þegar sniðmát er handvirkt hengt við þarf að nota [gerð skjals](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) sem hefur verið skilgreind í þeim tilgangi í [færibreytum rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="56e4c-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Viðhengi bætt við Excel\skráarþátt](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="56e4c-120">Til að tilgreina hvernig viðhengt sniðmát er fyllt út þegar skilgreint snið rafrænnar skýrslugerðar er keyrt þarf að bæta við földuðum þáttum **vinnublaðs**, **sviðs** og **hólfs** í þætti **Excel\\-skráar**.</span><span class="sxs-lookup"><span data-stu-id="56e4c-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="56e4c-121">Hver faldaður þáttur þarf að vera tengdur við Excel-vöru.</span><span class="sxs-lookup"><span data-stu-id="56e4c-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="56e4c-122">Sniðmátsinnflutningur</span><span class="sxs-lookup"><span data-stu-id="56e4c-122">Template import</span></span>

<span data-ttu-id="56e4c-123">Hægt er að velja **Flytja inn úr Excel** á flipanum **Innflutningur** á aðgerðasvæðinu til að flytja nýtt sniðmát inn í autt snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="56e4c-124">Í þessu dæmi er þáttur **Excel\\-skráar** stofnaður sjálfkrafa og innflutta sniðmátið verður hengt við hann.</span><span class="sxs-lookup"><span data-stu-id="56e4c-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="56e4c-125">Allir nauðsynlegir þættir rafrænnar skýrslugerðar verða einnig stofnaðir sjálfkrafa, samkvæmt lista yfir greindar Excel-vörur.</span><span class="sxs-lookup"><span data-stu-id="56e4c-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Val á „Flytja inn úr Excel“](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="56e4c-127">Ef stofna á valfrjálsa einingu fyrir **Vinnublað** á breytanlegu sniði rafrænnar skýrslugerðar þarf að stilla valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="56e4c-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="56e4c-128">Vinnublaðsþáttur</span><span class="sxs-lookup"><span data-stu-id="56e4c-128">Sheet component</span></span>

<span data-ttu-id="56e4c-129">Þátturinn **Vinnublað** gefur til kynna vinnublað viðhengdu Excel-vinnubókarinnar sem þarf að fylla út.</span><span class="sxs-lookup"><span data-stu-id="56e4c-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="56e4c-130">Heiti vinnublaðs í Excel-sniðmáti er skilgreint í eiginleikanum **Vinnublað** fyrir þennan þátt.</span><span class="sxs-lookup"><span data-stu-id="56e4c-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="56e4c-131">Þessi þáttur er valfrjáls fyrir Excel-vinnubækur sem innihalda eitt vinnublað.</span><span class="sxs-lookup"><span data-stu-id="56e4c-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="56e4c-132">Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Vinnublað** til að tilgreina hvort setja þurfi þátt í myndað skjal:</span><span class="sxs-lookup"><span data-stu-id="56e4c-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="56e4c-133">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi vinnublað sett í myndaða skjalið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="56e4c-134">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu mun myndaða skjalið ekki innihalda vinnublað.</span><span class="sxs-lookup"><span data-stu-id="56e4c-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Dæmi um vinnublaðsþátt](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="56e4c-136">Sviðsþáttur</span><span class="sxs-lookup"><span data-stu-id="56e4c-136">Range component</span></span>

<span data-ttu-id="56e4c-137">Þátturinn **Svið** gefur til kynna Excel-svið sem þessi þáttur rafrænnar skýrslugerðar þarf að stýra.</span><span class="sxs-lookup"><span data-stu-id="56e4c-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="56e4c-138">Heiti sviðsins er skilgreint í eiginleikanum **Excel-svið** fyrir þennan þátt.</span><span class="sxs-lookup"><span data-stu-id="56e4c-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="56e4c-139">Eiginleikinn **Eftirlíkingarátt** tilgreinir hvort og hvernig svið verður endurtekið í mynduðu skjali:</span><span class="sxs-lookup"><span data-stu-id="56e4c-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="56e4c-140">Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Engin eftirlíking** verður viðeigandi Excel-svið ekki endurtekið í myndaða skjalinu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="56e4c-141">Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Lóðrétt** verður viðeigandi Excel-svið endurtekið í myndaða skjalinu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="56e4c-142">Hvert endurtekið svið er sett undir upprunalega sviðið í Excel-sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="56e4c-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="56e4c-143">Fjöldi endurtekninga er skilgreindur af fjölda færslna í gagnagjafa af gerðinni **Færslulisti** sem er bundin þessum þætti rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="56e4c-144">Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Lárétt** verður viðeigandi Excel-svið endurtekið í myndaða skjalinu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="56e4c-145">Hvert endurtekið svið er sett til hægri við upprunalega sviðið í Excel-sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="56e4c-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="56e4c-146">Fjöldi endurtekninga er skilgreindur af fjölda færslna í gagnagjafa af gerðinni **Færslulisti** sem er bundin þessum þætti rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="56e4c-147">Frekari upplýsingar um lárétta eftirlíkingu er að hægt að nálgast með því að fylgja skrefunum í [Nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum](tasks/er-horizontal-1.md).</span><span class="sxs-lookup"><span data-stu-id="56e4c-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="56e4c-148">Þátturinn **Svið** getur verið með aðra faldaða þætti rafrænnar skýrslugerðar sem eru notaðir til að færa inn gildi í viðeigandi Excel-svið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="56e4c-149">Ef þáttur í flokknum **Texti** er notaður til að færa inn gildi er gildið fært inn í Excel-svið sem textagildi.</span><span class="sxs-lookup"><span data-stu-id="56e4c-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56e4c-150">Notið þetta mynstur til að sníða innfærð gildi út frá landsstaðlinum sem er skilgreindur í forritinu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="56e4c-151">Ef þátturinn **Hólf** í flokknum **Excel** er notaður til að færa inn gildi er gildið fært inn í Excel-svið sem gildi gagnagerðar sem er skilgreind af bindingum viðkomandi **Hólf**-þáttar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**).</span><span class="sxs-lookup"><span data-stu-id="56e4c-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="56e4c-152">Notið þetta mynstur til að virkja Excel-forritið til að sníða innfærð gildi út frá landsstaðli tölvunnar sem opnar skjal á útleið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="56e4c-153">Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Svið** til að tilgreina hvort setja þurfi þátt í myndað skjal:</span><span class="sxs-lookup"><span data-stu-id="56e4c-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="56e4c-154">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi svið sett í myndaða skjalið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="56e4c-155">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu, og ef þetta svið stendur ekki fyrir allar línur eða dálka, verður viðeigandi svið ekki fyllt út í mynduðu skjalið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="56e4c-156">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu, og ef þetta svið stendur fyrir allar línur eða dálka, mun myndaða skjalið innihalda þessar línur og dálka sem faldar línur og falda dálka.</span><span class="sxs-lookup"><span data-stu-id="56e4c-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="56e4c-157">Þáttur hólfs</span><span class="sxs-lookup"><span data-stu-id="56e4c-157">Cell component</span></span>

<span data-ttu-id="56e4c-158">Þátturinn **Hólf** er notaður til að fylla út Excel-hólf, form og myndir.</span><span class="sxs-lookup"><span data-stu-id="56e4c-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="56e4c-159">Til að gefa til kynna Excel-hlut sem þarf að fylla út með þættinum **Hólf** fyrir rafræna skýrslugerð þarf að tilgreina heiti þess hlutar í eiginleikanum **Excel-svið** fyrir þáttinn **Hólf**.</span><span class="sxs-lookup"><span data-stu-id="56e4c-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="56e4c-160">Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Hólf** til að tilgreina hvort fylla þurfi hlutinn út í mynduðu skjali:</span><span class="sxs-lookup"><span data-stu-id="56e4c-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="56e4c-161">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi hlutur settur í myndaða skjalið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="56e4c-162">Binding fyrir þennan **Hólf**-þátt tilgreinir gildi sem er sett í viðeigandi hlut.</span><span class="sxs-lookup"><span data-stu-id="56e4c-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="56e4c-163">Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu verður viðeigandi hlutur ekki fylltur út í myndaða skjalinu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="56e4c-164">Þegar þátturinn **Hólf** er skilgreindur á að færa inn gildi í hólf er hægt að binda hann við gagnagjafa sem skilar gildi frumstæðrar gagnagerðar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**).</span><span class="sxs-lookup"><span data-stu-id="56e4c-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="56e4c-165">Í þessu tilviki er gildið fært inn í hólfið sem gildi sömu gagnagerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="56e4c-166">Þegar þátturinn **Hólf** er skilgreindur á að færa inn gildi í Excel-form er hægt að binda hann við gagnagjafa sem skilar gildi frumstæðrar gagnagerðar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**).</span><span class="sxs-lookup"><span data-stu-id="56e4c-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="56e4c-167">Í þessu tilviki er gildið fært inn í Excel-formið sem texti á því formi.</span><span class="sxs-lookup"><span data-stu-id="56e4c-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="56e4c-168">Fyrir gildi gagnagerða sem eru ekki **Strengur** er sjálfkrafa breytt í texta.</span><span class="sxs-lookup"><span data-stu-id="56e4c-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="56e4c-169">Hægt er að skilgreina þáttinn **Hólf** til að fylla aðeins út form í tilvikum þar sem eiginleiki formtexta er studdur.</span><span class="sxs-lookup"><span data-stu-id="56e4c-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="56e4c-170">Þegar þátturinn **Hólf** er skilgreindur á að færa inn gildi í Excel-mynd er hægt að binda hann við gagnagjafa sem skilar gildi gagnagerðarinnar **Geymsla** sem stendur fyrir mynd á tvíundarsniði.</span><span class="sxs-lookup"><span data-stu-id="56e4c-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="56e4c-171">Í þessu tilviki er gildið slegið inn í Excel-mynd sem mynd.</span><span class="sxs-lookup"><span data-stu-id="56e4c-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="56e4c-172">Sérhver Excel-mynd og -form er talin vera fest á efra horni til vinstri við tiltekið Excel-hólf eða -svið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="56e4c-173">Ef ætlunin er að endurtaka Excel-mynd eða -form þarf að skilgreina hólfið eða sviðið sem það er fest við sem endurtekið hólf eða svið.</span><span class="sxs-lookup"><span data-stu-id="56e4c-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="56e4c-174">Frekari upplýsingar um hvernig á að fella inn myndir og form eru í [Fella inn myndir og form í skjöl sem búin eru til með rafrænni skýrslugerð](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="56e4c-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="56e4c-175">Síðuskilaþáttur</span><span class="sxs-lookup"><span data-stu-id="56e4c-175">Page break component</span></span>

<span data-ttu-id="56e4c-176">Þátturinn **PageBreak** þvingar Excel til að byrja nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="56e4c-177">Ekki þarf að nota þennan þátt þegar nota á sjálfgefið blaðsíðutal Excel en mælt er að hann sé notaður þegar Excel á að fylgja viðkomandi sniði rafrænnar skýrslugerðar við blaðsíðutal.</span><span class="sxs-lookup"><span data-stu-id="56e4c-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="56e4c-178">Breyta sniði rafrænnar skýrslugerðar sem bætt er við</span><span class="sxs-lookup"><span data-stu-id="56e4c-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="56e4c-179">Uppfæra sniðmát</span><span class="sxs-lookup"><span data-stu-id="56e4c-179">Update a template</span></span>

<span data-ttu-id="56e4c-180">Hægt er að velja **Uppfæra úr Excel** á flipanum **Innflutningur** á aðgerðasvæðinu til að flytja uppfært sniðmát inn í breytanlegt snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="56e4c-181">Á meðan á þessu stendur er sniðmáti af valinni einingu **Excel\\skrá** skipt út fyrir nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="56e4c-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="56e4c-182">Efni breytanlegs sniðs rafrænnar skýrslugerðar verður samstillt við efni með uppfærðs sniðmáts rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="56e4c-183">Nýr sniðsþáttur rafrænnar skýrslugerðar verður sjálfkrafa stofnaður fyrir hvert Excel-heiti ef sniðsþáttur rafrænnar skýrslugerðar finnst ekki í breytanlega sniðinu.</span><span class="sxs-lookup"><span data-stu-id="56e4c-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="56e4c-184">Öllum sniðsþáttum rafrænnar skýrslugerðar verður eytt úr breytanlegu sniði rafrænnar skýrslugerðar ef viðeigandi Excel-heiti finnst ekki fyrir það.</span><span class="sxs-lookup"><span data-stu-id="56e4c-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="56e4c-185">Stilla þarf valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já** ef stofna á valfrjálsa **Skjal** einingu á breytanlegu sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="56e4c-186">Ef breytanlegu sniði rafrænnar skýrslugerðar, var upphaflega í einingunum **Vinnublað** er mælt með því að stilla valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já** þegar flutt er inn uppfært sniðmát.</span><span class="sxs-lookup"><span data-stu-id="56e4c-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="56e4c-187">Að öðrum kosti verða allar faldaðar einingar upprunalegu einingarinnar **Vinnublað** búnar til frá grunni.</span><span class="sxs-lookup"><span data-stu-id="56e4c-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="56e4c-188">Af þeim ástæðum glatast allar bindingar endurstofnaðra sniðseininga í uppfærðu sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56e4c-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Valkosturinn „Stofna sniðseiningu Excel-vinnublaðs“ í svarglugganum Uppfæra úr Excel](./media/er-excel-format-update-template.png)

<span data-ttu-id="56e4c-190">Til að fá frekari upplýsingar um þennan eiginleika skal fylgja skrefunum í [Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát](modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="56e4c-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="56e4c-191">Villuleita snið rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="56e4c-191">Validate an ER format</span></span>

<span data-ttu-id="56e4c-192">Þegar snið rafrænnar skýrslugerðar sem hægt er að breyta er sannprófað er samræmisathugun framkvæmd til að ganga úr skugga um að Excel-heitið sé til staðar í Excel-sniðmátinu sem er í notkun.</span><span class="sxs-lookup"><span data-stu-id="56e4c-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="56e4c-193">Þú munt fá tilkynningu ef ósamræmi kemur upp.</span><span class="sxs-lookup"><span data-stu-id="56e4c-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="56e4c-194">Boðið er upp á valkost til að lagfæra sum vandamál sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="56e4c-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Staðfestingarvilluboð](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a><span data-ttu-id="56e4c-196">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="56e4c-196">Additional resources</span></span>

[<span data-ttu-id="56e4c-197">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="56e4c-197">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="56e4c-198">Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði</span><span class="sxs-lookup"><span data-stu-id="56e4c-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="56e4c-199">Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát</span><span class="sxs-lookup"><span data-stu-id="56e4c-199">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="56e4c-200">Nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum</span><span class="sxs-lookup"><span data-stu-id="56e4c-200">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="56e4c-201">Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER</span><span class="sxs-lookup"><span data-stu-id="56e4c-201">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="56e4c-202">Skilgreina rafræna skýrslugerð (ER) til að draga gögn inn í Power BI</span><span class="sxs-lookup"><span data-stu-id="56e4c-202">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)