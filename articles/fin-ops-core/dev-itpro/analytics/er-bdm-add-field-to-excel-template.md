---
title: Bættu nýjum reit við sniðmát viðskiptaskjala í Microsoft Excel
description: Þetta efni veitir upplýsingar um hvernig bæta má nýjum reitum við sniðmát viðskiptaskjala í Microsoft Excel með því að nota viðskiptaskjalastjórnunaraðgerð.
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: fcfbcb021b192cef75d59b0db1796e994f3dc27d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681377"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="de0f2-103">Bættu nýjum reit við sniðmát viðskiptaskjala í Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="de0f2-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="de0f2-104">Þú getur bætt nýjum reitum við sniðmát sem er notað til að búa til viðskiptaskjöl á Microsoft Excel sniði.</span><span class="sxs-lookup"><span data-stu-id="de0f2-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="de0f2-105">Þessum reitum er hægt að bæta við sem frátökurum sem eru notaðir til að fylla mynda skjöl með nauðsynlegum upplýsingum úr forritinu.</span><span class="sxs-lookup"><span data-stu-id="de0f2-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="de0f2-106">Fyrir alla reiti sem þú bætir við geturðu einnig tilgreint bindingu gagnagjafa til að tilgreina hvaða forritsgögn verða færð inn í reitinn þegar sniðmátið er notað til að búa til viðskiptaskjöl.</span><span class="sxs-lookup"><span data-stu-id="de0f2-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="de0f2-107">Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="de0f2-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="de0f2-108">Þetta dæmi sýnir hvernig á að uppfæra sniðmát til að fylla út reitina í skjámyndum textareikninga sem eru búnir til.</span><span class="sxs-lookup"><span data-stu-id="de0f2-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="de0f2-109">Skilgreina stjórnun viðskiptaskjala til að breyta sniðmátum</span><span class="sxs-lookup"><span data-stu-id="de0f2-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="de0f2-110">Vegna þess að viðskiptaskjalastjórnun (BDM) er byggð ofan á rammann [Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md) verður þú að stilla nauðsynlegar færibreytur ER og BDM áður en þú getur byrjað að vinna með BDM.</span><span class="sxs-lookup"><span data-stu-id="de0f2-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="de0f2-111">Skráðu þig inn á Microsoft Dynamics 365 Finance sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="de0f2-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="de0f2-112">Ljúktu eftirfarandi skrefum í dæminu í efninu [Yfirlit yfir viðskiptaskjöl stjórnun](er-business-document-management.md):</span><span class="sxs-lookup"><span data-stu-id="de0f2-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="de0f2-113">Skilgreina færibreytur Rafræn skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="de0f2-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="de0f2-114">Kveiktu á BDM.</span><span class="sxs-lookup"><span data-stu-id="de0f2-114">Turn on BDM.</span></span>

<span data-ttu-id="de0f2-115">Þú getur nú byrjað að nota BDM til að breyta sniðmátum fyrir viðskiptaskjöl.</span><span class="sxs-lookup"><span data-stu-id="de0f2-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="de0f2-116">Flytja inn ER lausnir sem innihalda sniðmát</span><span class="sxs-lookup"><span data-stu-id="de0f2-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="de0f2-117">Dæmið í þessari aðferð notar opinberlega útgefnu ER lausnina.</span><span class="sxs-lookup"><span data-stu-id="de0f2-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="de0f2-118">Þú verður að flytja ER stillingar þessarar lausnar inn í núverandi tilvik þitt af Finance.</span><span class="sxs-lookup"><span data-stu-id="de0f2-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="de0f2-119">Skilgreining ER-sniðs **Ókeypis textareikningur (Excel)** þessarar lausnar inniheldur sniðmát viðskiptaskjala á Excel sniði sem hægt er að breyta með BDM.</span><span class="sxs-lookup"><span data-stu-id="de0f2-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="de0f2-120">Flytja inn nýjustu útgáfuna af þessu ER sniði frá Microsoft Dynamics Lifecycle Service (LCS).</span><span class="sxs-lookup"><span data-stu-id="de0f2-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="de0f2-121">Samsvarandi ER gagnalíkan og skilgreiningar ER-líkanavörpunar verða fluttar inn sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="de0f2-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="de0f2-122">Nánari upplýsingar um hvernig eigi að flytja inn ER-skilgreininga er að finna í [Stjórna líftíma ER-stillinga](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="de0f2-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Síðan LCS samnýtt eignasafn](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="de0f2-124">Breyta sniðmát fyrir ER lausn</span><span class="sxs-lookup"><span data-stu-id="de0f2-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="de0f2-125">Skráðu þig inn sem notandi sem hefur aðgang að vinnusvæðinu **Stjórnun viðskiptaskjala**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="de0f2-126">Opnaðu vinnusvæðið **Stjórnun viðskiptaskjala**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-126">Open the **Business document management** workspace.</span></span>

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="de0f2-128">Í tölfunni velurðu sniðmátið **Ókeypis textareikningur (Excel)**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="de0f2-129">Í hægri glugganum velurðu **Nýtt sniðmát** til að búa til nýtt sniðmát sem byggist á völdu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="de0f2-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="de0f2-130">Í reitinn **Titill** slærðu inn **Ókeypis textareikningur (Excel) Contoso** sem yfirskrift nýja sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="de0f2-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="de0f2-131">Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.</span><span class="sxs-lookup"><span data-stu-id="de0f2-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="de0f2-132">Síðan BDM-sniðmátsritill birtist.</span><span class="sxs-lookup"><span data-stu-id="de0f2-132">The BDM template editor page appears.</span></span> <span data-ttu-id="de0f2-133">Hægt er að nota Microsoft 365 til að breyta völdu sniðmáti á netinu í innbyggðu stýringunni.</span><span class="sxs-lookup"><span data-stu-id="de0f2-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM ritilssíða](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="de0f2-135">Bættu merkimiðanum fyrir nýjan reit við sniðmátið</span><span class="sxs-lookup"><span data-stu-id="de0f2-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="de0f2-136">Á ritstjórasíðu BDM sniðmáts, á Excel borði, á flipanum **Útsýni**, velurðu gátreitina **Fyrirsagnir og hnitanet** fyrir breytilegt Excel sniðmát.</span><span class="sxs-lookup"><span data-stu-id="de0f2-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![Gátreitirnir Fyrirsagnir og hnitanet valdir](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="de0f2-138">Veldu hólf **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="de0f2-139">Á Excel-borðanum, á flipanum **Heim**, velurðu **Sameina og miðja** til að sameina valda reiti í nýjan sameinaðan reit **E8:F8**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="de0f2-140">Í sameinaða reitnum **E8:F8** slærðu inn **Vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="de0f2-141">Veldu sameinaðan reit **E7:F7**, veldu **Sniðmálari** og veldu síðan sameinaðan reit **E8:F8** til að forsníða hann á sama hátt og sameinaða reitinn **E7:F7**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![Nýjum reitamerkimiða bætt við sniðmátið](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="de0f2-143">Sníddu sniðmátið til að taka frá pláss fyrir nýjan reit</span><span class="sxs-lookup"><span data-stu-id="de0f2-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="de0f2-144">Á ritilsíðu BDM sniðmáts velurðu sameinaðan reit **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="de0f2-145">Á Excel-borðanum, á flipanum **Heim**, velurðu **Sameina og miðja** til að sameina valda reiti í nýjan sameinaðan reit **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="de0f2-146">Veldu sameinaðan reit **G7:H7**, veldu **Sniðmálari** og veldu síðan sameinaðan reit **G8:H8** til að forsníða hann á sama hátt og sameinaða reitinn **G7:H7**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![Rými frátekið fyrir nýja reitinn](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="de0f2-148">Í reitinn **Heiti** velurðu **CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="de0f2-149">Svið **CompanyInfo** núverandi Excel sniðmáts geymir alla reitina sem eru notaðir til að fylla haus á myndaða skýrslu með upplýsingum um núverandi fyrirtæki sem seljanda.</span><span class="sxs-lookup"><span data-stu-id="de0f2-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![CompanyInfo svið valið](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="de0f2-151">Bæta nýjum reit við sniðmátið</span><span class="sxs-lookup"><span data-stu-id="de0f2-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="de0f2-152">Á síðunni **Ritill BDM sniðmáts**, í aðgerðarglugganum, velurðu **Sýna snið**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="de0f2-153">Í glugganum **Uppbygging sniðmáts** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de0f2-154">Þú verður að aðlaga hluta sniðmátsins sem þú vilt nota sem nýjan reit.</span><span class="sxs-lookup"><span data-stu-id="de0f2-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="de0f2-155">Þú hefur þegar gert þessa leiðréttingu með því að forsníða sameinaða reitinn **G8:H8**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![Nýjum reit bætt við sniðmátið](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="de0f2-157">Veldu **Excel\Cell** til að bæta við nýjum reit sem reit í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="de0f2-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="de0f2-158">Þú getur valið **Excel\Range** ef þú vilt bæta nýju svið við sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="de0f2-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="de0f2-159">Sviðið sem er slegið inn getur innihaldið marga reiti.</span><span class="sxs-lookup"><span data-stu-id="de0f2-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="de0f2-160">Þú getur bætt þessum reitum við síðar.</span><span class="sxs-lookup"><span data-stu-id="de0f2-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="de0f2-161">Taktu eftir að sniðmátshlutinn **CompanyInfo** er sjálfkrafa valinn í glugganum **Uppbygging sniðmáts** vegna þess að það er heppilegasti foreldrahlutinn í núverandi sniðmátbyggingu fyrir reitinn sem þú ert að bæta við.</span><span class="sxs-lookup"><span data-stu-id="de0f2-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="de0f2-162">Í reitinn **Excel-svið** reit slærðu inn **CompanyURL_Value**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="de0f2-163">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-163">Select **OK**.</span></span>

    ![CompanyURL_Value sviði bætt við sniðmátaskipan](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="de0f2-165">Í glugganum **Uppbygging sniðmáts** velurðu úrfellingarhnappinn (...) og velur síðan **Sýna bindingar**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![Sýna valdar bindingar](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="de0f2-167">Glugginn **Uppbygging sniðmáts** sýnir nú gagnagjafana sem eru fáanlegir á undirliggjandi ER sniði.</span><span class="sxs-lookup"><span data-stu-id="de0f2-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="de0f2-168">Veldu **CompanyInfo_Value** sem reitinn sem þú ætlar að binda við gagnagjafa af undirliggjandi ER sniði.</span><span class="sxs-lookup"><span data-stu-id="de0f2-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="de0f2-169">Í hlutanum **Gagnagjafar** í glugganum **Uppbygging sniðmáts** stækkarðu **Model \> InvoiceBase \> CompanyInfo**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="de0f2-170">Undir **CompanyInfo** velurðu liðinn **WebsiteURI**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![Liðurinn WebsiteURI valið](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="de0f2-172">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-172">Select **Bind**.</span></span>
11. <span data-ttu-id="de0f2-173">Í glugganum **Uppbygging sniðmáts** velurðu **Vista** og lokar síðan ritilssíðu BDM sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="de0f2-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="de0f2-174">Á vinnusvæðinu **Stjórnun viðskiptaskjala** sýnir flipinn **Sniðmát** í hægri glugganum uppfærða sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="de0f2-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="de0f2-175">Í netinu skaltu taka eftir því að reitnum **Staða** fyrir breytt sniðmát hefur verið breytt í **Drög** og að reiturinn **Endurskoðun** er ekki lengur auður.</span><span class="sxs-lookup"><span data-stu-id="de0f2-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="de0f2-176">Þessar breytingar benda til þess að ferlið við að breyta þessu sniðmáti er hafið.</span><span class="sxs-lookup"><span data-stu-id="de0f2-176">These changes indicate that the process of editing this template has been started.</span></span>

![Breytt sniðmát í vinnusvæðinu Stjórnun viðskiptaskjala](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="de0f2-178">Yfirfara fyrirtækjastillingar</span><span class="sxs-lookup"><span data-stu-id="de0f2-178">Review company settings</span></span>

1.  <span data-ttu-id="de0f2-179">Farðu í **Fyrirtækisstjórnun \> Fyrirtæki \> Lögaðilar**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="de0f2-180">Á flýtiflipanum **Upplýsingar um tengiliði** staðfestirðu að vefslóð fyrirtækisins sé slegin inn.</span><span class="sxs-lookup"><span data-stu-id="de0f2-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![Vefslóð fyrirtækisins slegin inn á síðu Lögaðila](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="de0f2-182">Búðu til viðskiptaskjöl til að prófa uppfærða sniðmátið</span><span class="sxs-lookup"><span data-stu-id="de0f2-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="de0f2-183">Í forritinu skal breyta fyrirtækinu í **USMF** og fara í **Viðskiptakröfur \> Reikningar \> Allir textareikningar**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="de0f2-184">Veldu reikninginn **FTI-00000002** og síðan **Prentstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="de0f2-185">Stækkaðu í vinstri glugganum **Eining - viðskiptakröfur \> Skjöl \> Textareikningur**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="de0f2-186">Undir **Textareikningur** velurðu **Upprunalegt skjal** til að tilgreina umfang reikninga til vinnslu.</span><span class="sxs-lookup"><span data-stu-id="de0f2-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="de0f2-187">Í hægri glugganum, í reitnum **Skýrslusnið**, velurðu sniðmátið **Textareikningur (Excel) Contoso** fyrir tilgreint skjalastig.</span><span class="sxs-lookup"><span data-stu-id="de0f2-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![Sniðmátið Textareikningur (Excel) Contoso valið](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="de0f2-189">Ýttu á **Esc** til að loka núverandi síðu.</span><span class="sxs-lookup"><span data-stu-id="de0f2-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="de0f2-190">Veldu **Prenta \> Valið**.</span><span class="sxs-lookup"><span data-stu-id="de0f2-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="de0f2-191">Sæktu skjalið sem myndað var og opnaðu það í Excel.</span><span class="sxs-lookup"><span data-stu-id="de0f2-191">Download the generated document, and open it in Excel.</span></span>

    ![Textareikningur í Excel](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="de0f2-193">Breytta sniðmátið er notað til að mynda skýrslu reiknings með frjálsum texta fyrir valinn hlut.</span><span class="sxs-lookup"><span data-stu-id="de0f2-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="de0f2-194">Til að greina hvernig þessi skýrsla hefur áhrif á breytingarnar sem eru gerðar á sniðmátinu skaltu keyra þessa skýrslu í einni forritslotu strax eftir að þú breytir sniðmátinu í annarri forritslotu.</span><span class="sxs-lookup"><span data-stu-id="de0f2-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="de0f2-195">Skyldir tenglar</span><span class="sxs-lookup"><span data-stu-id="de0f2-195">Related links</span></span>

[<span data-ttu-id="de0f2-196">Yfirlit yfir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="de0f2-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="de0f2-197">Yfirlit yfir stjórnun viðskiptaskjala</span><span class="sxs-lookup"><span data-stu-id="de0f2-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="de0f2-198">Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði</span><span class="sxs-lookup"><span data-stu-id="de0f2-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)
