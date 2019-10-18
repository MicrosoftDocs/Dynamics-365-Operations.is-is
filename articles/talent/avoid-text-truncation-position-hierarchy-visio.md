---
title: Forðist stýfingu á texta í stöðustigveldi og útflutningi í Visio
description: Þetta efnisatriði útskýrir hvernig á að leysa mál þar sem nöfn einstaklinga og stöður eru styttar þegar viðskiptamenn skoða stöðustigveldið í Microsoft Dynamics 365 Talent. Stýfing á texta getur gert það erfitt að taka skjámynd eða prenta stigveldið.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e151818f29ac37ff449daaf1dc02e44b8fb317c3
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008501"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="a17ff-104">Forðist stýfingu á texta í stöðustigveldi og útflutningi í Visio</span><span class="sxs-lookup"><span data-stu-id="a17ff-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a17ff-105">**Úthreyfing**</span><span class="sxs-lookup"><span data-stu-id="a17ff-105">**Issue**</span></span>

<span data-ttu-id="a17ff-106">Þegar viðskiptavinur skoðar stöðustigveldið í Microsoft Dynamics 365 Talent, eru nöfn á einstaklingum og stöðum stytt.</span><span class="sxs-lookup"><span data-stu-id="a17ff-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="a17ff-107">Því getur reynst erfitt að taka skjámynd eða að prenta og dreifa stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="a17ff-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Stöðustigveldi](media/position-h.png)

<span data-ttu-id="a17ff-109">**Orsök**</span><span class="sxs-lookup"><span data-stu-id="a17ff-109">**Cause**</span></span>

<span data-ttu-id="a17ff-110">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="a17ff-110">This behavior is by design.</span></span>

<span data-ttu-id="a17ff-111">**Upplausn**</span><span class="sxs-lookup"><span data-stu-id="a17ff-111">**Resolution**</span></span>

<span data-ttu-id="a17ff-112">Því miður geta notendur ekki breytt stærð textans á auðveldan hátt.</span><span class="sxs-lookup"><span data-stu-id="a17ff-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="a17ff-113">Hins vegar er hægt að flytja stöðustigveldið út úr Talent og flytja það síðan inn í Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="a17ff-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="a17ff-114">Þrátt fyrir að eftirfarandi grein hafi verið skrifuð fyrir Microsoft Dynamics AX 2012, gildir ferlið samt sem áður fyrir Talent: [Flytja út stöðustigveldi í Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="a17ff-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="a17ff-115">Fylgið þessum skrefum til að flytja út í Visio.</span><span class="sxs-lookup"><span data-stu-id="a17ff-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="a17ff-116">Í Talent skal opna listasíðuna **Stöður**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="a17ff-117">Til að bæta frekar upplýsingum við skipurit fyrirtækis skal bæta reitum við listann **Stöður** svo þeir séu tiltækir þegar leiðsagnarforritið er notað síðar í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="a17ff-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="a17ff-118">Í aðgerðasvæðinu skal velja hnappinn **Opna í Microsoft Office** og síðan, undir **Flytja út í Excel**, skal velja **Stöður**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="a17ff-119">Einnig er hægt að ýta á Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="a17ff-119">Alternatively, press Ctrl+T.</span></span>

    ![Flytjið út listasíðuna Stöður í Excel](media/org-admin.png)

3. <span data-ttu-id="a17ff-121">Vistið Excel-skrána sem er flutt út.</span><span class="sxs-lookup"><span data-stu-id="a17ff-121">Save the Excel file that is exported.</span></span>

    ![Flytjið út í svarglugga Excel](media/export-excel.png)

4. <span data-ttu-id="a17ff-123">Í Visio skal velja **Visio - Búa til nýja** og síðan velja sniðmátsflokkinn **Viðskipti**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Ný skýringarmynd](media/new.png)

5. <span data-ttu-id="a17ff-125">Veljið **Leiðsagnarforrit fyrir myndrit fyrirtækis** og síðan **Búa til**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Svargluggi leiðsagnarforrits fyrir myndrit fyrirtækis](media/orgchart-wizard.png)

6. <span data-ttu-id="a17ff-127">Veljið **Upplýsingar sem eru þegar vistaðar í skrá eða gagnagrunni** og veljið síðan **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="a17ff-129">Veljið **Texta, „Org Plus“ (\*.txt) eða Excel-skrá** og veljið síðan **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="a17ff-131">Flettið til að velja útfluttu Excel-skrána sem inniheldur stöðustigveldið og veljið síðan **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="a17ff-133">Stillið reitinn **Heiti** á **Staða**, stillið reitinn **Skýrslur til að** á **Skýrslur til að staðsetja** og veljið síðan **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="a17ff-135">Veljið reitina sem á að sýna á hverjum hnút og veljið síðan **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="a17ff-137">Bætið dálknum **Staða** við listann **Móta gagnareiti** og veljið síðan **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="a17ff-139">Myndir eru ekki í boði eins og er.</span><span class="sxs-lookup"><span data-stu-id="a17ff-139">Pictures aren't currently available.</span></span> <span data-ttu-id="a17ff-140">Á næstu síðu skal því velja **Næsta**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="a17ff-141">Veljið **Ég vil að leiðsagnarforritið raði myndriti fyrirtækisins sjálfkrafa niður á margar síður**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Leiðsagnarforrit fyrir myndrit fyrirtækis 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="a17ff-143">Veljið **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="a17ff-143">Select **Finish**.</span></span>

    <span data-ttu-id="a17ff-144">Ef einhverjar stöður eru ekki í skipulaginu verður notandi beðinn um að bæta þeim við skýringarmyndina.</span><span class="sxs-lookup"><span data-stu-id="a17ff-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="a17ff-145">Skýringarmyndin sem er búin til í Visio birtir hvern yfirmann á aðskildu vinnublaði.</span><span class="sxs-lookup"><span data-stu-id="a17ff-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="a17ff-146">Þegar Visio-skráin er búin til birtir hver hnútur viðeigandi upplýsingar sem byggjast á reitunum sem voru valdir til að hafa með á skýringarmyndinni.</span><span class="sxs-lookup"><span data-stu-id="a17ff-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Stigveldi skýringarmyndar](media/hierarchy.png)

<span data-ttu-id="a17ff-148">**Frekari valkostir**</span><span class="sxs-lookup"><span data-stu-id="a17ff-148">**Additional option**</span></span>

<span data-ttu-id="a17ff-149">Í Talent er hugsanlega líka hægt að nota vinnusvæðið **Fólk** til að skoða stigveldistengdar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a17ff-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
