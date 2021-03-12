---
title: Uppfæra skipan sniðmáts viðskiptaskjals
description: Þetta efnisatriði útskýrir hvernig á að uppfæra skipulag sniðmáts viðskiptaskjals með því að nota eiginleikann stjórnun viðskiptaskjala.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
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
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: cb0188e372b5f6275472cf040d10bb796eed1858
ms.sourcegitcommit: 95d2fc0fa7d17d3a96f7969f12c985b018b4ff94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/12/2020
ms.locfileid: "4728090"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="7817a-103">Uppfæra skipan sniðmáts viðskiptaskjals</span><span class="sxs-lookup"><span data-stu-id="7817a-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7817a-104">Á glugganum **Skipulag sniðmáts** í sniðmátsritlinum [Viðskiptaskjalastjórnun](er-business-document-management.md) er hægt að breyta viðskiptaskjalasniðmáti með því að [bæta við nýjum svæðum](er-bdm-add-field-to-excel-template.md) á sniðmát í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7817a-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="7817a-105">Skipulag sniðmátsins er síðan sjálfkrafa uppfært í Dynamics 365 Finance þannig að það endurspegli breytingarnar sem gerðar voru í glugganum **Skipulag sniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="7817a-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="7817a-106">Einnig er hægt að breyta sniðmáti með því að nota Office 365 neteiginleikann.</span><span class="sxs-lookup"><span data-stu-id="7817a-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="7817a-107">Til dæmis er hægt að bæta við nýju atriði með heiti, t.d. mynd eða lögun, á breytanlega vinnublaðið.</span><span class="sxs-lookup"><span data-stu-id="7817a-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="7817a-108">Í þessu tilviki er skipulag sniðmátsins ekki sjálfkrafa uppfært í Finance og varan sem bætt var við birtist ekki á glugganum **Skipulag sniðmáts**.</span><span class="sxs-lookup"><span data-stu-id="7817a-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="7817a-109">Uppfærið sniðmát handvirkt í Finance með því að velja **Uppfæra skipulag** á síðu sniðmátsritilsins.</span><span class="sxs-lookup"><span data-stu-id="7817a-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="7817a-110">Fyrir frekari upplýsingar um þennan eiginleika skal ljúka eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="7817a-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="7817a-111">Dæmi: Uppfæra skipan sniðmáts viðskiptaskjals</span><span class="sxs-lookup"><span data-stu-id="7817a-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="7817a-112">Þetta dæmi sýnir hvernig kerfisstjóri getur uppfært uppbyggingu sniðmáts viðskiptaskjals í Finance eftir að sniðmátinu er breytt í Office Online.</span><span class="sxs-lookup"><span data-stu-id="7817a-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="7817a-113">Eftirfarandi kaflar útskýra skrefin sem um er að ræða.</span><span class="sxs-lookup"><span data-stu-id="7817a-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="7817a-114">Undirbúa sniðmát viðskiptaskjals fyrir breytingar</span><span class="sxs-lookup"><span data-stu-id="7817a-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="7817a-115">Ljúkið eftirfarandi ferli í [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="7817a-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="7817a-116">Skilgreina færibreytur Rafræn skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="7817a-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="7817a-117">Flytja inn ER-lausnir</span><span class="sxs-lookup"><span data-stu-id="7817a-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="7817a-118">Virkja stjórnun viðskiptaskjala</span><span class="sxs-lookup"><span data-stu-id="7817a-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="7817a-119">Skilgreina færibreytur</span><span class="sxs-lookup"><span data-stu-id="7817a-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="7817a-120">Breyta sniðmáti viðskiptaskjala</span><span class="sxs-lookup"><span data-stu-id="7817a-120">Edit a business document template</span></span>

1. <span data-ttu-id="7817a-121">Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.</span><span class="sxs-lookup"><span data-stu-id="7817a-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="7817a-122">Á síðunni **Búa til nýtt sniðmát** skal velja sniðmátið **Reikningur með frjálsum texta (rafrænt skýrslugerðardæmi)(Excel)**.</span><span class="sxs-lookup"><span data-stu-id="7817a-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="7817a-123">Veljið **Búa til skjal**.</span><span class="sxs-lookup"><span data-stu-id="7817a-123">Select **Create document**.</span></span>
4. <span data-ttu-id="7817a-124">Á svæðinu **Titill** skal slá inn **Dæmi um reikning með frjálsum texta fyrir Litware**.</span><span class="sxs-lookup"><span data-stu-id="7817a-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="7817a-125">Veljið **Í LAGI** til að stofna nýja sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="7817a-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7817a-126">Ef notandinn hefur ekki enn skráð sig inn á Office Online er honum [beint á Office 365 innskráningarsíðuna](er-business-document-management.md#frequently-asked-questions).</span><span class="sxs-lookup"><span data-stu-id="7817a-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="7817a-127">Til að fara aftur í fjármálaumhverfið skal velja hnappinn **Til baka** í vafranum.</span><span class="sxs-lookup"><span data-stu-id="7817a-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="7817a-128">Nýja sniðmátið er opnað fyrir breytingar í Excel Online innbyggðu stýringunni á sniðmátssíðu.</span><span class="sxs-lookup"><span data-stu-id="7817a-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="7817a-129">[![Nota vinnusvæði stjórnunar vinnuskjala til að hefja breytingar á sniðmáti viðskiptaskjals](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="7817a-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="7817a-130">Yfirfara núverandi byggingu breytanlegs sniðmáts</span><span class="sxs-lookup"><span data-stu-id="7817a-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="7817a-131">Í Excel Online, á borðanum, á flipanum **Yfirlit**, í flokknum **Sýna**, skal velja **Hnitalínur**.</span><span class="sxs-lookup"><span data-stu-id="7817a-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="7817a-132">Í breytanlegu sniðmáti skal velja rétthyrninginn fyrir ofan titil sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="7817a-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="7817a-133">Þessi rétthyrningur er mynd sem nefnist **rptHeaderCompLogo**.</span><span class="sxs-lookup"><span data-stu-id="7817a-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="7817a-134">Ef **Skipulag sniðmáts** svæðið er falið , skal velja **Sýna skipulag**.</span><span class="sxs-lookup"><span data-stu-id="7817a-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="7817a-135">Á glugganum **Skipulag sniðmáts** skal stækka **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7817a-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="7817a-136">Takið eftir að, í sniðmátsuppbyggingu í Finance, er **rptHeaderCompLogo**-varan birt sem undireining **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7817a-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="7817a-137">[![Vinnusvæði viðskiptaskjalastjórnunar notað til að yfirfara núverandi uppbyggingu breytanlegs sniðmáts](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="7817a-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="7817a-138">Uppfæra skipan sniðmáts viðskiptaskjals með því að eyða mynd</span><span class="sxs-lookup"><span data-stu-id="7817a-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="7817a-139">Í Excel online, í breytanlegu sniðmáti, skal velja **rptHeaderCompLogo** myndina.</span><span class="sxs-lookup"><span data-stu-id="7817a-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="7817a-140">Fylgdu einu af þessum skrefum til að eyða valinni mynd úr breytanlegu sniðmáti:</span><span class="sxs-lookup"><span data-stu-id="7817a-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="7817a-141">Veljið **DELETE** lykilinn á lyklaborðinu.</span><span class="sxs-lookup"><span data-stu-id="7817a-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="7817a-142">Veljið og haldið fingri (eða hægrismellið) á myndina og veljið síðan **Klippa**.</span><span class="sxs-lookup"><span data-stu-id="7817a-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7817a-143">Atriðið **rptHeaderCompLogo** er enn til staðar í skipulagi sniðmáts í Fjármálum, jafnvel þótt myndin sé ekki lengur innifalin í Excel-sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="7817a-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="7817a-144">Veljið **Uppfæra skipulag** til að samstilla byggingu breytanlegra sniðmáta í Excel og Finance.</span><span class="sxs-lookup"><span data-stu-id="7817a-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="7817a-145">Á glugganum **Skipulag sniðmáts** skal stækka **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7817a-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="7817a-146">Takið eftir því að **rptHeaderCompLogo** varan er ekki lengur með í sniðmátsuppbyggingu í Finance.</span><span class="sxs-lookup"><span data-stu-id="7817a-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="7817a-147">[![Nota vinnusvæði stjórnunar vinnuskjala til að eyða mynd úr sniðmáti viðskiptaskjals](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="7817a-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="7817a-148">Uppfæra skipan sniðmáts viðskiptaskjals með því að bæta við mynd</span><span class="sxs-lookup"><span data-stu-id="7817a-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="7817a-149">Á Excel Online á borða flipans **Setja inn** í flokkinum **Myndskreytingar** skal velja **Mynd**.</span><span class="sxs-lookup"><span data-stu-id="7817a-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="7817a-150">Veldu **Velja skrá**, flettu að myndinni sem þú vilt bæta við, veldu hana og veldu svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7817a-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="7817a-151">Veljið **Setja inn**.</span><span class="sxs-lookup"><span data-stu-id="7817a-151">Select **Insert**.</span></span>
4. <span data-ttu-id="7817a-152">Færðu nýju myndin þar til hún er á réttum stað.</span><span class="sxs-lookup"><span data-stu-id="7817a-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="7817a-153">Sjálfgefið er að Excel gefi myndinni heiti.</span><span class="sxs-lookup"><span data-stu-id="7817a-153">By default, Excel names the picture.</span></span> <span data-ttu-id="7817a-154">Til dæmis gæti það gefið myndinni heitið **Mynd 2**.</span><span class="sxs-lookup"><span data-stu-id="7817a-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="7817a-155">Veljið **Uppfæra skipulag** til að samstilla byggingu breytanlegra sniðmáta í Excel og Finance.</span><span class="sxs-lookup"><span data-stu-id="7817a-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="7817a-156">Á glugganum **Skipulag sniðmáts** skal stækka **Skýrsla \> Reikningur \> rptHeader \> rptHeaderPart1**.</span><span class="sxs-lookup"><span data-stu-id="7817a-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="7817a-157">Takið eftir að nýja myndin er nú tekin með sem vara í sniðmátsuppbyggingu í Finance.</span><span class="sxs-lookup"><span data-stu-id="7817a-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="7817a-158">[![Nota vinnusvæði stjórnunar vinnuskjala til að bæta mynd við sniðmát viðskiptaskjals](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="7817a-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="7817a-159">Tengdir tenglar</span><span class="sxs-lookup"><span data-stu-id="7817a-159">Related links</span></span>

[<span data-ttu-id="7817a-160">Yfirlit yfir rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="7817a-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7817a-161">Yfirlit yfir stjórnun viðskiptaskjala</span><span class="sxs-lookup"><span data-stu-id="7817a-161">Business document management overview</span></span>](er-business-document-management.md)