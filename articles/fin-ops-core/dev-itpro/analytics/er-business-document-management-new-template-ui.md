---
title: Notandaviðmót Microsoft Office-stíls í Stjórnun viðskiptaskjala
description: Í þessu efnisatriði er útskýrt hvernig á að nota nýja notandaviðmótið í eiginleika viðskiptaskjalastjórnunar í ramma rafrænnar skýrslugerðar.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881037"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="45d31-103">Notandaviðmót Microsoft Office-stíls í Stjórnun viðskiptaskjala</span><span class="sxs-lookup"><span data-stu-id="45d31-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45d31-104">Business Document Management leyfir notendum að breyta sniðmátum viðskiptaskjala með Microsoft 365-þjónustu eða viðeigandi Microsoft Office skjáborðsforriti.</span><span class="sxs-lookup"><span data-stu-id="45d31-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="45d31-105">Breytingar gætu innihaldið hönnunarbreytingar eða nýjar dreifingar, eða notendur gætu bætt við frátökutákni til að innihalda viðbótargögn án þess að þurfa að breyta kóðanum.</span><span class="sxs-lookup"><span data-stu-id="45d31-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="45d31-106">Nánari upplýsingar um hvernig á að vinna með skjalastjórnun viðskipta, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="45d31-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="45d31-107">Nýja notendaviðmótið (UI) er skýrara og þægilegra í notkun.</span><span class="sxs-lookup"><span data-stu-id="45d31-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="45d31-108">Svæðið **Viðskiptaskjal** sýnir aðeins sniðmát sem eru í boði fyrir núverandi þjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="45d31-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="45d31-109">Í eldra notandaviðmóti sýndi flipinn **Sniðmát** öll sniðmátin sem voru í boði fyrir alla þjónustuaðila.</span><span class="sxs-lookup"><span data-stu-id="45d31-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="45d31-110">Hann sýndi einnig öll sniðmát sem voru búin til og breytt af öllum notendum í sama hlutverkinu.</span><span class="sxs-lookup"><span data-stu-id="45d31-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="45d31-111">Með hnappinum **Nýtt skjal** er hægt að búa til og breyta sniðmáti í rafrænni skýrslugerð (ER) sniði sem annar veitandi veitir.</span><span class="sxs-lookup"><span data-stu-id="45d31-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="45d31-112">Í dæminu í þessu efni er veitan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45d31-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="45d31-113">Einnig er hægt að stofna sniðmát með því að hlaða upp eigin sniðmáti á Excel sniði.</span><span class="sxs-lookup"><span data-stu-id="45d31-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="45d31-114">Myndbandið [Búa til nýtt viðskiptaskjal með stjórnun viðskiptaskjala](https://youtu.be/gAIYl-mM_pw) (sýnt hér að ofan) er að finna í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er aðgengilegur í YouTube.</span><span class="sxs-lookup"><span data-stu-id="45d31-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="45d31-115">Gerðu nýja skjalið UI í viðskiptaskjalastjórnun tiltækt</span><span class="sxs-lookup"><span data-stu-id="45d31-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="45d31-116">Til að byrja að nota nýja skjalið UI í viðskiptaskjalastjórnun verður þú að kveikja á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Stjórnun eiginleika**.</span><span class="sxs-lookup"><span data-stu-id="45d31-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="45d31-117">Fylgdu þessum skrefum til að kveikja á þessum eiginleika fyrir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="45d31-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="45d31-118">Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Allt**, velurðu eiginleikann **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á listanum.</span><span class="sxs-lookup"><span data-stu-id="45d31-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="45d31-119">Veldu **Virkja núna** til að kveikja á völdum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="45d31-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="45d31-120">Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="45d31-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="45d31-121">Breyta sniðmátum sem eru í eigu annarra veitenda</span><span class="sxs-lookup"><span data-stu-id="45d31-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="45d31-122">Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.</span><span class="sxs-lookup"><span data-stu-id="45d31-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="45d31-124">Í flipanum **Velja** skal velja skjalið til að nota sem sniðmát og síðan velja **Stofna skjal**.</span><span class="sxs-lookup"><span data-stu-id="45d31-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Gluggi viðskiptaskjala](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="45d31-126">Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="45d31-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="45d31-127">Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til.</span><span class="sxs-lookup"><span data-stu-id="45d31-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="45d31-128">Drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda.</span><span class="sxs-lookup"><span data-stu-id="45d31-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="45d31-129">Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.</span><span class="sxs-lookup"><span data-stu-id="45d31-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="45d31-130">Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.</span><span class="sxs-lookup"><span data-stu-id="45d31-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="45d31-131">Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.</span><span class="sxs-lookup"><span data-stu-id="45d31-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="45d31-132">Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.</span><span class="sxs-lookup"><span data-stu-id="45d31-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Gluggi skjalagerðar](./media/BDM_overview_new_template3.png)

<span data-ttu-id="45d31-134">Hnappurinn **Nýtt skjal** er notaður til að búa til og breyta sniðmáti á ER-sniði sem annar veitandi veitir.</span><span class="sxs-lookup"><span data-stu-id="45d31-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="45d31-135">Í þessu dæmi er veitan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45d31-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="45d31-136">Þegar þú velur **Nýtt skjal** geturðu skoðað öll sniðmát sem eru í eigu núverandi og annarra veitenda.</span><span class="sxs-lookup"><span data-stu-id="45d31-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="45d31-137">Eftir að þú velur sniðmátið verður það opnað fyrir breytingar.</span><span class="sxs-lookup"><span data-stu-id="45d31-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="45d31-138">Síðan verður breytt sniðmátið geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.</span><span class="sxs-lookup"><span data-stu-id="45d31-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="45d31-139">Hlaða upp sniðmáti sem notar fyrirliggjandi Excel-snið</span><span class="sxs-lookup"><span data-stu-id="45d31-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="45d31-140">Fylgið þessum skrefum til að veita nauðsynlegar upplýsingar áður en sniðmáti er hlaðið upp.</span><span class="sxs-lookup"><span data-stu-id="45d31-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="45d31-141">Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.</span><span class="sxs-lookup"><span data-stu-id="45d31-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="45d31-143">Á síðunni **Búa til nýtt sniðmát**, í flipanum **Hlaða upp**, í flipanum **Sniðmát**, skal velja **Fletta** til að finna og velja Excel-skrána sem á að nota sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="45d31-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="45d31-144">Í hlutanum **Sniðmát** er sjálfkrafa fyllt inn í reitina **Titill** og **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="45d31-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="45d31-145">Þeir tilgreina heiti og lýsingu á nýrri skilgreiningu rafræns skýrslugerðarsniðs sem er sjálfkrafa búið til.</span><span class="sxs-lookup"><span data-stu-id="45d31-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="45d31-146">Hægt er að breyta þessum reitum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="45d31-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="45d31-147">Í hlutanum **Skjalagerð**, í reitnum **Heiti**, skal tilgreina gerð viðskiptaskjalsins.</span><span class="sxs-lookup"><span data-stu-id="45d31-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="45d31-148">Þetta gildi verður notað til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans).</span><span class="sxs-lookup"><span data-stu-id="45d31-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Sniðmátsflipinn](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="45d31-150">Í flipanum **Gagnaveita**, í flýtiflipanum **Sía**, skal velja **Nota síu**.</span><span class="sxs-lookup"><span data-stu-id="45d31-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="45d31-151">Í hlutanum **Gagnaveita**, er fyllt inn sjálfkrafa í reitinn **Heiti** eða hægt er að velja gildi handvirkt.</span><span class="sxs-lookup"><span data-stu-id="45d31-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="45d31-152">Hægt er að nota síuna til að leita að viðeigandi heiti gagnaveitu eftir heiti, lýsingu, lands-/svæðiskóða og gerð viðskiptaskjals.</span><span class="sxs-lookup"><span data-stu-id="45d31-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Flipi gagnaveitu](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="45d31-154">Flýtiflipinn **Sía** er notuð til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans).</span><span class="sxs-lookup"><span data-stu-id="45d31-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="45d31-155">Hægt er að breyta öllum síureitum til að finna hentugustu gagnaveituna fyrir skjalið sem hlaðið er upp.</span><span class="sxs-lookup"><span data-stu-id="45d31-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="45d31-156">Skilyrðin í flýtiflipanum **Sía** eru notuð sem **EÐA** skilyrði.</span><span class="sxs-lookup"><span data-stu-id="45d31-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="45d31-157">Í flipanum **Vörpun** skal velja **Greina sjálfvirkt**.</span><span class="sxs-lookup"><span data-stu-id="45d31-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="45d31-158">Reiturinn **Skilgreining rótar** er sjálfkrafa fylltur út eða hægt er að velja gildi handvirkt.</span><span class="sxs-lookup"><span data-stu-id="45d31-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="45d31-159">Þessi flipi sýnir endavörpun eininganna úr sniðmátinu og líkaninu.</span><span class="sxs-lookup"><span data-stu-id="45d31-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Vörpunarflipi](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="45d31-161">Vörpunin í hlutanum **Skipulag sniðmáts** notar fulla samsvörun á merkjum eða lýsingum í gagnaveitunni á tungumáli notanda og í heiti hólfs í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="45d31-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="45d31-162">Veljið **Stofna skjal** til að staðfesta að ætlunin sé að stofna sniðmát og hefja breytingarferlið.</span><span class="sxs-lookup"><span data-stu-id="45d31-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="45d31-163">Fyrir frekari upplýsingar, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="45d31-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="45d31-164">Ef ekki er til nein veita í rafrænni skýrslugerð er hægt að búa hana til.</span><span class="sxs-lookup"><span data-stu-id="45d31-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="45d31-165">Ef engin virk veita er til staðar er hægt að velja að virkja eina slíka.</span><span class="sxs-lookup"><span data-stu-id="45d31-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="45d31-166">Til að búa til veitu skal breyta heiti veitunnar í reitnum **Heiti**, uppfæra veffang nýju veitunnar í reitnum **Veffang** og velja **Í lagi** til að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="45d31-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Stofna nýja veitu í BDM](./media/bdm_create_provider.png)
    
- <span data-ttu-id="45d31-168">Til að virkja núverandi veitu skal velja heiti veitunnar í reitnum **Skilgreiningarveita** og velja **Í lagi** til að stilla veituna sem virka.</span><span class="sxs-lookup"><span data-stu-id="45d31-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Virkja veitu í BDM](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="45d31-170">Hvert BDM-sniðmát vísar í veituna sem höfund skilgreiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="45d31-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="45d31-171">Þess vegna þarf að hafa virka veitu fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="45d31-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
