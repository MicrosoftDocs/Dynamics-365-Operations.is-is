---
title: Úthýsing
description: Þetta efnisatriði aðstoðar þig við að búa til kynningu á úthýsingu framleiðslu í Dynamics 365 Supply Chain Management.
author: christophernread
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 053dff19da6e51d23383d667c340c49f3eff1b27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825183"
---
# <a name="subcontracting"></a><span data-ttu-id="a2e4c-103">Úthýsing</span><span class="sxs-lookup"><span data-stu-id="a2e4c-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2e4c-104">Þetta efnisatriði aðstoðar þig við að búa til kynningu á úthýsingu framleiðslu í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a2e4c-105">Fyrsti hlutinn í þessu efnisatriði lýsir uppsetningu á gögnum.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="a2e4c-106">Annar hlutinn fer með þig í gegnum skref kynningarinnar.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="a2e4c-107">Markhópur</span><span class="sxs-lookup"><span data-stu-id="a2e4c-107">Target audience</span></span>

<span data-ttu-id="a2e4c-108">Í þessu efnisatriði muntu fræðast um uppsetningu úthýsingar í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="a2e4c-109">Þú notar fyrirliggjandi gögn í HQUS-lögaðilanum til að búa til grunnuppsetningu á aðgerðaflæði úthýsingar.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="a2e4c-110">Sýnigögnin í HQUS-lögaðilanum innihalda færibreytur uppsetningar sem hafa verið forstilltar til að styðja við skrefin í kynningunni.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="a2e4c-111">Jafnvel þótt kynningin fjallar um helstu vandamál og áskoranir fyrir mismunandi hlutverk, getur kerfisstjóri lokið henni.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="a2e4c-112">Sýnikennsla</span><span class="sxs-lookup"><span data-stu-id="a2e4c-112">Demo scenario</span></span>

<span data-ttu-id="a2e4c-113">Í HQUS-lögaðilanum eru hágæða hátalarar framleiddir.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="a2e4c-114">Á meðan á framleiðsluferlinu stendur fara hátalararnir í gegnum eftirfarandi þrjár aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="a2e4c-115">**Fyrirfram samsetning** - Hátalaraboxið er sett saman.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="a2e4c-116">Efnið fyrir boxið er tekið til í vöruhúsinu áður en aðgerðin er hafin.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="a2e4c-117">**Húðun** - Eftir að hátalaraboxið hefur verið sett saman verður að húða það.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="a2e4c-118">Lánardrottinn (undirverktaki) lýkur þessari aðgerð.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="a2e4c-119">Fyrirfram samsetta hátalaraboxið er sent til undirverktaka húðunar ásamt tveimur efnisþáttum.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="a2e4c-120">**Ljúka** - Eftir að undirverktakinn hefur húðað fyrirfram samsetta hátalaraboxið er því skilað til HQUS-lögaðila svo hægt sé að ljúka endanlegri samsetningu á hátalaranum.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="a2e4c-121">Eftirfarandi skýringarmynd sýnir aðgerðirnar þrjár og efnisþættina sem voru notaðir.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Aðgerðirnar „Fyrirfram samsetning“, „Húðun“ og „Ljúka“ og efnisþættirnir sem eru notaðir](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="a2e4c-123">Setja upp</span><span class="sxs-lookup"><span data-stu-id="a2e4c-123">Setup</span></span>

<span data-ttu-id="a2e4c-124">Áður en byrjað er á kynningunni þarf að setja upp gögnin.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="a2e4c-125">Setja upp tilbúna afurð</span><span class="sxs-lookup"><span data-stu-id="a2e4c-125">Set up the finished product</span></span>

<span data-ttu-id="a2e4c-126">Þessi aðferð fer með þig í gegnum uppsetningu á losaðir afurð D8100, „Húðað hátalarabox“.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="a2e4c-127">Veldu **Afurðaupplýsingastjórnun \> Afurðir \> Losaðar afurðir** til að opna síðuna **Upplýsingar um losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="a2e4c-128">Í flýtisíureitnum skal slá inn **D8100** til að finna fyrirliggjandi afurð.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Síun á losaðri afurð D8100 á síðunni „Upplýsingar um losaðar afurðir“](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="a2e4c-130">Á aðgerðasvæðinu, í flipanum **Hanna**, skal velja **Leið** til að opna síðuna **Leið**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="a2e4c-131">Síðan **Leið** sýnir átta leiðarútgáfur fyrir losaða afurð D8100.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="a2e4c-132">Átta leiðarútgáfunum er skipt niður á fjórar leiðir á svæði 1 og á svæði 5.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="a2e4c-133">Leið 000400 er notuð fyrir kostnað, leið 00041 er notuð þegar húðunaraðgerðin er innri aðgerð og leið 00042 er notuð þegar húðunaraðgerðin er utanaðkomandi aðgerð.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Átta leiðarútgáfur á leiðarsíðunni](./media/subcontract03_route-page.png)

4. <span data-ttu-id="a2e4c-135">Í efri rúðunni, í hnitanetinu **Útgáfur**, skal velja leiðarútgáfu **00042** fyrir svæði **5**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="a2e4c-136">Í neðri rúðunni, í flipanum **Yfirlit** skal velja aðgerð **20** (**Cbnt Ctsc**) í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Aðgerð 20 fyrir leiðarútgáfu 00042 fyrir svæði 5 er valið](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="a2e4c-138">Veldu flipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-138">Select the **General** tab.</span></span>

    <span data-ttu-id="a2e4c-139">Athugaðu að reiturinn **Leiðargerð** er stilltur á **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="a2e4c-140">Þetta gildi gefur til kynna að aðgerð 20 (Cbnt CtSc) er aðgerð undirverktaka.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Reitur leiðargerðar er stilltur á Lánardrottinn í flipanum Almennt](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="a2e4c-142">Veldu flipann **Tilfangaþarfir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="a2e4c-143">Eiginleikar verða notaðir til að finna viðeigandi tilfang meðan á framleiðsluröðun stendur.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="a2e4c-144">Fyrir aðgerð 20 (Cbnt CtSc), athugaðu að tilfang sem hefur tvenns konar eiginleika, **Húðun** og **Húðuð box**, er krafist.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Eiginleikarnir Húðun og Húðað box á flipa tilfangaþarfa](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="a2e4c-146">Veldu **Viðeigandi tilföng** til að opna svargluggann **Viðeigandi tilföng**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="a2e4c-147">Þrjú tilföng finnast sem samsvara tilfangaþörfum fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="a2e4c-148">Taktu eftir að tilföng 8851 og 8852 eru af gerðinni **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Þrjú viðeigandi tilföng í svarglugganum Viðeigandi tilföng](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="a2e4c-150">Veldu **Í lagi** til að loka svarglugganum **Viðeigandi tilföng** og fara aftur á síðuna **Leið**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="a2e4c-151">Lokaðu síðunni **Leið** til að fara aftur á síðuna **Upplýsingar um losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Upplýsingasíða um losaðar afurðir](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="a2e4c-153">Á aðgerðasvæðinu, í flipanum **Hanna**, skal velja **Uppskriftarútgáfur** til að opna síðuna **Uppskriftarútgáfur**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="a2e4c-154">Síðan **Uppskriftarútgáfur** sýnir fjórar uppskriftarútgáfur fyrir losaða afurð D8100.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="a2e4c-155">Uppskrift 000040 er notuð fyrir kostnað og áætlanagerð, uppskrift 000041 er notuð ef húðunaraðgerðin er gerð innanhúss og uppskriftir 000042 og 000043 eru notaðar ef húðunaraðgerð er úthýst.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="a2e4c-156">Athugaðu að vara S8050 er afurð af vörugerðinni **Þjónusta**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="a2e4c-157">Þessi vara táknar úthýstu vinnuna.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-157">This item represents the subcontracted work.</span></span>

    ![Fjórar uppskriftarútgáfur á útgáfusíðu uppskriftar](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="a2e4c-159">Á flýtiflipanum **Uppskriftarlínur** skal velja **Breyta** til að opna svargluggann **Breyta uppskriftarlínu**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="a2e4c-160">Þegar framleiðslupöntun er búin til og áætluð fyrir losaða afurð D8100 verður innkauppöntun sjálfkrafa búin til fyrir vöru S8050.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="a2e4c-161">Þessi innkaupapöntun verður tengd við framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="a2e4c-162">Til þess að innkaupapantanir verði sjálfkrafa búnar til verður reiturinn **Línugerð** að vera stilltur á **Lánardrottinn** og velja þarf lánardrottnalykil fyrir undirverktakann.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="a2e4c-163">Í þessu tilviki er lánardrottnalykillinn US-801.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="a2e4c-164">Takið eftir að uppskriftarlínan er tengd við húðunaraðgerðina með aðgerðarnúmerinu (í þessu tilviki 20).</span><span class="sxs-lookup"><span data-stu-id="a2e4c-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Breyta svarglugga uppskriftarlínu](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="a2e4c-166">Stofna aðgangsorð fyrir starfsmenn í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="a2e4c-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="a2e4c-167">Þú verður að skilgreina aðgangsorð fyrir starfsmenn í vöruhúsi sem nota handbúnað.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="a2e4c-168">Veldu **Vöruhúsakerfi \> Uppsetning \> Starfsmaður** til að opna síðuna **Verknotendur**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="a2e4c-169">Á flýtiflipanum **Notendur** skal velja línuna fyrir notanda **51**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Verknotendasíða](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="a2e4c-171">Veldu **Endurstilla aðgangsorð**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="a2e4c-172">Í reitunum **Aðgangsorð** og **Staðfesta aðgangsorð** skal slá inn **1**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="a2e4c-173">Veldu **Stilla aðgangsorð**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="a2e4c-174">Kynning skref fyrir skref</span><span class="sxs-lookup"><span data-stu-id="a2e4c-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="a2e4c-175">**Aðstæður og bakgrunnur**</span><span class="sxs-lookup"><span data-stu-id="a2e4c-175">**Scenario and background**</span></span>

<span data-ttu-id="a2e4c-176">Framleiðslupöntun upp á 10 stykki er búin til fyrir afurðina D8100, „Húðað hátalarabox“.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="a2e4c-177">Húðunin á boxinu er úthýst aðgerð sem lánardrottinn US-801, „Perfect Coating Solutions“, gerir.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="a2e4c-178">Framleiðslupöntunin samanstendur af þremur aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-178">The production order consists of three operations.</span></span> <span data-ttu-id="a2e4c-179">Í fyrstu aðgerðinni er boxið fyrirfram samsett sem aðgerð innanhúss.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="a2e4c-180">Efnið fyrir fyrirfram samsetninguna er losað fyrir tiltekt í vöruhúsi hráefna.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="a2e4c-181">Eftir að fyrirfram samsetningu er lokið er fyrirfram samsetta boxið sent til „Perfect Coating Solutions“ ásamt tveimur efnisþáttum sem þarf að nota fyrir húðunaraðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="a2e4c-182">Þegar húðaða boxið er móttekið frá lánardrottni fer það í gegnum endanlega samsetningaraðgerð innanhúss áður en það er tilkynnt sem lokið.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="a2e4c-183">Veldu **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** til að opna síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="a2e4c-184">Á aðgerðasvæðinu skal velja **Ný framleiðslupöntun** til að opna svargluggann **Stofna framleiðslupöntun**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Svarglugginn „Stofna framleiðslupöntun“](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="a2e4c-186">Í svæðið **Vörunúmer** veldu **D8100**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="a2e4c-187">Eftir að þú velur vörunúmer birtast reitir fyrir birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="a2e4c-188">Í reitnum **Litur** er valið **Króm**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="a2e4c-189">Skilaboðagluggi birtist sem spyr hvort ætti að setja inn virkar útgáfur fyrir uppskrift og leið.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Skilaboðagluggi](./media/subcontract13_message-box.png)

5. <span data-ttu-id="a2e4c-191">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-191">Select **Yes**.</span></span> 

    <span data-ttu-id="a2e4c-192">Í svarglugganum **Stofna framleiðslupöntun** eru virku útgáfur uppskriftar og leiðar fyrir afurð D8100 valdar sjálfkrafa í reitunum **Uppskriftarnúmer** og **Leiðarnúmer**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="a2e4c-193">Í þessu tilviki er uppskrift **000040** og leið **000040** valin.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a2e4c-194">Fyrir bæði uppskrift og leið er útgáfa 000040 notuð fyrir kostnað og áætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="a2e4c-195">Í reitnum **Svæði** skal velja **5**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="a2e4c-196">Í reitnum **Vöruhús** skal velja **51**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="a2e4c-197">Í reitunum **Uppskriftarnúmer** og **Leiðarnúmer** skal breyta sjálfkrafa valda gildinu í **000042**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2e4c-198">Fyrir bæði uppskrift og leið er útgáfa 000042 notuð til að úthýsa húðun á boxinu á lánardrottin US-801.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Gildi stillt í svarglugganum „Stofna framleiðslupöntun“](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="a2e4c-200">Veldu **Stofna** til að búa til framleiðslupöntun og fara aftur á síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Ný framleiðslupöntun á síðunni „Allar framleiðslupantanir“](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="a2e4c-202">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun** skal velja **Áætlun** til að opna svargluggann **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Svarglugginn Áætlun](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="a2e4c-204">Veldu **Í lagi** til að staðfesta áætlunina og fara aftur á síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2e4c-205">Þegar framleiðslupöntun er áætluð er innkaupapöntunin fyrir þjónustuvöru S8050 búin til fyrir lánardrottin US-801.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="a2e4c-206">Á aðgerðasvæðinu í flipanum **Framleiðslupöntun** skal velja **Uppskrift** til að opna síðuna **Uppskrift** þar sem hægt er að skoða uppskriftarlínur fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="a2e4c-207">Athugaðu að fyrir þjónustuvöru S8050 er tilvísun í framleiðslupöntunina sem var búin til þegar framleiðslupöntunin var áætluð.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Uppskriftarlínur framleiðslupöntunar á uppskriftarsíðunni](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="a2e4c-209">Lokaðu síðunni **Uppskrift** til að fara aftur á síðuna **Framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="a2e4c-210">Á aðgerðasvæðinu í flipanum **Tímasetja** skal velja **Tímasetja verk** til að opna svargluggann **Vinnsluröðun**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="a2e4c-211">Tilgreindu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a2e4c-211">Specify the following values:</span></span>

    - <span data-ttu-id="a2e4c-212">Í reitnum **Röðunarstefna** er valið **Áfram frá morgundegi**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="a2e4c-213">Stilltu valkostinn **Takmörkuð geta** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Svargluggi vinnsluröðunar](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="a2e4c-215">Veldu **Í lagi** til að loka svarglugganum **Vinnsluröðun** og fara aftur á síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="a2e4c-216">Á aðgerðasvæðinu, í flipanum **Tímasetja** skal velja **Gantt** til að opna síðuna **Gantt-rit - tilfangayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="a2e4c-217">Gantt-ritið veitir sjónrænt yfirlit yfir hvernig framleiðsluverkin eru áætluð á tilföngunum.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="a2e4c-218">Taktu eftir því að utanaðkomandi húðunaraðgerðin samanstendur af þremur verkum: vinnsluverki, flutningsverki og biðtímaverki.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantt-rit á Gantt-ritinu - Yfirlitssíða tilfanga](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="a2e4c-220">Lokaðu síðunni **Gantt-rit - tilfangayfirlit** til að fara aftur á síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="a2e4c-221">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun** skal velja **Losa** til að opna svargluggann **Losa**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Svarglugginn Losa](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="a2e4c-223">Velja skal **Í lagi** til að loka svarglugganum **Losa**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="a2e4c-224">Veldu **Framleiðslustýring \> Reglubundin verkefni \> Losa í vöruhús \> Sjálfvirk losun á uppskriftar- og formúlulínum** til að opna svargluggann **Sjálfvirk losun uppskriftar og formúlulína**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Svarglugginn Sjálfvirk losun uppskriftar og formúlulína](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="a2e4c-226">Veldu **Í lagi** til að keyra Sjálfvirk losun á verki uppskriftar og formúlulína.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="a2e4c-227">Þetta verk losar tiltektarvinnu á hráefnum til vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="a2e4c-228">Veldu **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** til að opna síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="a2e4c-229">Notaðu flýtisíureitinn til að velja framleiðslupöntunina sem þú hefur verið að vinna við.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="a2e4c-230">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Upplýsingar um verk** til að opna síðuna **Verk**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="a2e4c-231">Taktu eftir að síðan sýnir tvö sett af verkum fyrir tiltekt á hráefni.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="a2e4c-232">Fyrra verkið er fyrir efni M8100 og M8101.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="a2e4c-233">Aðgerð 10 notar þessa efnisþætti.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="a2e4c-234">Seinna verkið er fyrir efni M8202 og M8250.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="a2e4c-235">Aðgerð 20 notar þessa efnisþætti, sem er úthýsta aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Tvö sett af verkum fyrir hráefnatiltekt á Verksíðunni](./media/subcontract22_work-page.png)

26. <span data-ttu-id="a2e4c-237">Opnaðu farsímaforrit vöruhúsakerfis til að vinna við vöruhúsaverkið fyrir aðgerð 10.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-237">Start the Warehouse Management mobile app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="a2e4c-238">Veldu **Framleiðslustýring \> Framleiðslupantanir \> Allar framleiðslupantanir** til að opna síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="a2e4c-239">Notaðu flýtisíureitinn til að velja framleiðslupöntunina sem þú hefur verið að vinna við.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="a2e4c-240">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, skal velja **Opna** til að opna svargluggann **Opna**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="a2e4c-241">Í flipanum **Almennt** skal tilgreina eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a2e4c-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="a2e4c-242">Í **Frá aðg. nr.**</span><span class="sxs-lookup"><span data-stu-id="a2e4c-242">In the **From Oper. No.**</span></span> <span data-ttu-id="a2e4c-243">reitur, veljið **10**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-243">field, select **10**.</span></span>
    - <span data-ttu-id="a2e4c-244">Í **Til aðg. nr.**</span><span class="sxs-lookup"><span data-stu-id="a2e4c-244">In the **To Oper. No.**</span></span> <span data-ttu-id="a2e4c-245">reitur, veljið **10**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-245">field, select **10**.</span></span>

    ![Gildi stillt í Almenna flipanum 1](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="a2e4c-247">Veldu **Í lagi** til að loka svarglugganum **Opna** og fara aftur á síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="a2e4c-248">Taktu eftir að staðan á framleiðslupöntuninni er nú **Opin**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="a2e4c-249">Sjálfvirk bókun á færslubók tiltektarlista notar efnin fyrir aðgerð 10.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="a2e4c-250">Sjálfvirk bókun á færslubók leiðarspjalda gerir grein fyrir tímanotkun fyrir aðgerð 10.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="a2e4c-251">Opnaðu farsímaforrit vöruhúsakerfis til að vinna við vöruhúsaverkið fyrir aðgerð 20.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-251">Start the Warehouse Management mobile app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="a2e4c-252">Á aðgerðasvæðinu, í flipanum **Framleiðslupöntun**, skal velja **Opna** til að opna svargluggann **Opna**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="a2e4c-253">Í flipanum **Almennt** skal tilgreina eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a2e4c-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="a2e4c-254">Í **Frá aðg. nr.**</span><span class="sxs-lookup"><span data-stu-id="a2e4c-254">In the **From Oper. No.**</span></span> <span data-ttu-id="a2e4c-255">reitur, veljið **20**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-255">field, select **20**.</span></span>
    - <span data-ttu-id="a2e4c-256">Í **Til aðg. nr.**</span><span class="sxs-lookup"><span data-stu-id="a2e4c-256">In the **To Oper. No.**</span></span> <span data-ttu-id="a2e4c-257">reitur, veljið **20**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-257">field, select **20**.</span></span>
    - <span data-ttu-id="a2e4c-258">Í **Magn** reitinn er fært inn **10**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="a2e4c-259">Stilltu valkostinn **Bóka tiltektarlistann núna** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Gildi stillt í Almenna flipanum 2](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="a2e4c-261">Veldu **Í lagi** til að loka svarglugganum **Opna** og fara aftur á síðuna **Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="a2e4c-262">Tiltektarlisti er búinn til fyrir þau efni sem húðunaraðgerðin og þjónustuvaran notar.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="a2e4c-263">Þjónustuvaran sýnir kostnað á úthýstri aðgerð.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="a2e4c-264">Á aðgerðasvæðinu, í flipanum **Skoða**, skal velja **Tínslulisti** til að opna síðuna **Tínslulisti**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="a2e4c-265">Veldu tínslulistann sem ekki er bókaður og veldu síðan færslubókarnúmerið til að skoða færslubókarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Færslubókarlínur á síðu tínslulista](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="a2e4c-267">Í aðgerðasvæðinu skal velja **Prenta** \> **Skýrsla tínslulista** til að opna svargluggann **Skýrsla tínslulista**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="a2e4c-268">Stilltu valkostinn **Nota útlit fylgiseðils** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Svarglugginn Skýrsla tínslulista](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="a2e4c-270">Veldu **Í lagi** til að búa til skýrslu fyrir **Tínslulista**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="a2e4c-271">Í þessu tilfelli er fylgiseðill lánardrottins prentaður út frá færslubók tiltektarlista framleiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="a2e4c-272">Fylgiseðillinn tilgreinir þau efni sem eru send til lánardrottins sem mun sjá um húðunaraðgerðina.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Skýrsla tiltektarlista](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="a2e4c-274">Lokaðu skýrslunni **Tínslulisti** til að fara aftur á síðuna **Tínslulisti**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="a2e4c-275">Á aðgerðasvæðinu skal velja **Bóka** til að opna svargluggann **Bóka færslubók**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Svarglugginn Bóka færslubók](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="a2e4c-277">Veldu **Í lagi** til að loka svarglugganum **Bóka færslubók**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="a2e4c-278">Opna innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-278">Open the purchase order.</span></span>

    ![Síða innkaupapöntunar](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="a2e4c-280">Á aðgerðasvæðinu, í flipanum **Innkaup**, skal velja **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="a2e4c-281">Veldu **Bóka** til að opna svargluggann **Bóka færslubók**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="a2e4c-282">Veldu **Í lagi** til að loka svarglugganum **Bóka færslubók** og fara aftur á síðuna **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="a2e4c-283">Breyttu einingarverðinu úr **33** í **40**.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-283">Change the unit price from **33** to **40**.</span></span>

    ![Breyting á einingarverði á síðu innkaupapöntunar](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="a2e4c-285">Staðfestu innkaupapöntunina aftur.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="a2e4c-286">Innhreyfingarskjal.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-286">Product receipt.</span></span>

    ![Svarglugginn Bókun innhreyfingarskjals](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="a2e4c-288">Innkaupareikningur.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-288">Purchase invoice.</span></span>
52. <span data-ttu-id="a2e4c-289">Uppfærðu samsvörunarstöðuna.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-289">Update the match status.</span></span>

    ![Reikningssíða lánardrottins](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="a2e4c-291">Bóka sem lokið.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-291">Report as finished.</span></span>

    ![Svarglugginn Bóka sem lokið](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="a2e4c-293">Lok.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-293">End.</span></span>

    ![Svarglugginn Lok](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="a2e4c-295">Kostnaðarsamanburður.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-295">Cost comparison.</span></span>

    ![Gröf kostnaðarsamanburðar](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="a2e4c-297">Vantar uppsetningu í gögnum.</span><span class="sxs-lookup"><span data-stu-id="a2e4c-297">Missing setup in data.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]