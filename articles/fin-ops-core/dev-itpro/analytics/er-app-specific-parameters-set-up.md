---
title: Settu upp færibreytur ER sniðs á hvern lögaðila
description: Þetta efni útskýrir hvernig þú getur sett upp færibreytur í snið fyrir rafræna skýrslugerð (ER) á lögaðila.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 9c5884bba494d2dd44f9204667144402a88ddec8
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694339"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="c9e47-103">Settu upp færibreytur ER sniðs á hvern lögaðila</span><span class="sxs-lookup"><span data-stu-id="c9e47-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="c9e47-104">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="c9e47-104">Prerequisites</span></span>

<span data-ttu-id="c9e47-105">Til að ljúka þessum skrefum verðurðu fyrst að klára skrefin í efninu [Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="c9e47-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="c9e47-106">Til að ljúka dæmunum í þessu efni verður þú að hafa aðgang að Microsoft Dynamics 365 Finance (Fjármál) fyrir eitt af eftirfarandi hlutverkum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="c9e47-107">Þróunaraðili rafrænnar skýrslulausnar</span><span class="sxs-lookup"><span data-stu-id="c9e47-107">Electronic reporting developer</span></span>
- <span data-ttu-id="c9e47-108">Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="c9e47-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="c9e47-109">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="c9e47-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="c9e47-110">Flytja inn rafræn skýrslugerð grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="c9e47-110">Import ER configurations</span></span>

1.  <span data-ttu-id="c9e47-111">Skráðu þig inn í umhverfið.</span><span class="sxs-lookup"><span data-stu-id="c9e47-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="c9e47-112">Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="c9e47-113">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="c9e47-114">Flyttu inn í núverandi tilvik af Finance stillingarnar sem þú fluttir út úr Regulatory Configuration Services (RCS) meðan þú varst að ljúka skrefunum í efninu [Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="c9e47-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="c9e47-115">Fylgdu þessum skrefum fyrir hverja stillingu fyrir rafræna skýrslugerð (ER) í eftirfarandi röð: gagnamódel, vörpun líkana og snið.</span><span class="sxs-lookup"><span data-stu-id="c9e47-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="c9e47-116">Veldu **Skipta út \> Hlaða úr XML-skrá**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="c9e47-117">Veljið **Vafra** til að velja skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="c9e47-118">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-118">Select **OK**.</span></span>
    
    <span data-ttu-id="c9e47-119">Eftirfarandi mynd sýnir stillingarnar sem þú verður að hafa þegar þú ert búin/n.</span><span class="sxs-lookup"><span data-stu-id="c9e47-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![Skilgreiningarsíða í ER](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="c9e47-121">Setja upp færibreytur fyrir fyrirtækið DEMF</span><span class="sxs-lookup"><span data-stu-id="c9e47-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="c9e47-122">Þú getur notað ER-rammana til að setja upp sértækar breytur fyrir forrit fyrir ER snið.</span><span class="sxs-lookup"><span data-stu-id="c9e47-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="c9e47-123">Velja skal lögaðilann **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="c9e47-124">Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="c9e47-125">Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="c9e47-127">Á síðunni **Forritsbundnar færibreytur** er hægt að stilla reglurnar fyrir gagnagjafann **Val** í sniðinu **Snið til að læra hvernig á að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="c9e47-128">Ef grunn ER sniðið mun innihalda nokkra gagnagjafa af gerðinni **Uppfletting**, verður þú að velja viðeigandi gagnagjafa á flýtiflipanum **Uppflettingar** áður en þú getur byrjað að stilla reglumengi fyrir gagnagjafann.</span><span class="sxs-lookup"><span data-stu-id="c9e47-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="c9e47-129">Fyrir hvern gagnagjafa er hægt að stilla aðskildar reglur fyrir hverja útgáfu af völdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="c9e47-130">Allt reglumengið fyrir alla uppflettigagnagjafa sem eru fáanlegir í valinni útgáfu af grunn-ER sniði samanstendur af forritssértæku færibreytunum fyrir ER sniðið.</span><span class="sxs-lookup"><span data-stu-id="c9e47-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="c9e47-131">Veldu útgáfu **1.1.1** á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="c9e47-132">Á flýtiflipanum **Skilyrði** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="c9e47-133">Í reitnum **Kóði** í nýju skránni velurðu fellilistaörina til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c9e47-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="c9e47-134">Uppflettan sýnir lista yfir skattakóða fyrir val.</span><span class="sxs-lookup"><span data-stu-id="c9e47-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="c9e47-135">Þessum lista er skilað af gagnagjafanum **Model.Data.Tax** sem hefur verið stilltur á grunn ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="c9e47-136">Vegna þess að þessi gagnagjafi inniheldur reitinn **Heiti** birtist nafn sérhvers skattakóða í leitinni.</span><span class="sxs-lookup"><span data-stu-id="c9e47-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="c9e47-138">Veldu skattakóðann **VAT19** tax code.</span><span class="sxs-lookup"><span data-stu-id="c9e47-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="c9e47-139">Í reitnum **Niðurstöður uppflettinar** í nýju skránni velurðu fellilistaörina til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c9e47-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="c9e47-140">Leitin sýnir lista yfir gildi fyrir TaxationLevel snið upptalningar fyrir val.</span><span class="sxs-lookup"><span data-stu-id="c9e47-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="c9e47-141">Athugaðu að ef þýska er valin sem æskilegt tungumál notandans sem þú ert skráður inn sem, þá verða merkimiðar gildanna í uppflettingu á þýsku, að því tilskildu að þau hafi verið þýdd á grunn ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="c9e47-142">Að auki, ef merkimiði uppflettingargagnaheimildar hefur verið þýddur mun sá merkimiði birtast á æskilegu tungumáli notandans á flipanum **Uppflettingar**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="c9e47-144">Veldu gildið **Regluleg skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="c9e47-145">Með því að bæta við þessa skrá skilgreinirðu eftirfarandi reglu: Alltaf þegar beðið er um **Val** uppflettingu gagnagjafa og skattakóðinn **VSK19** er samþykktur sem frumbreyta verður **Regluleg skattlagning** skilað sem umbeðnu skattlagningarstigi.</span><span class="sxs-lookup"><span data-stu-id="c9e47-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="c9e47-146">Veldu **Bæta við** og fylgdu síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="c9e47-147">Í reitnum **Kóði** velurðu skattakóðann **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="c9e47-148">Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Regluleg skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="c9e47-149">Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="c9e47-150">Í reitnum **Kóði** velurðu skattakóðann **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="c9e47-151">Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Lægri skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="c9e47-152">Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="c9e47-153">Í reitnum **Kóði** velurðu skattakóðann **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="c9e47-154">Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Lægri skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="c9e47-155">Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="c9e47-156">Í reitnum **Kóði** velurðu skattakóðann **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="c9e47-157">Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="c9e47-158">Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="c9e47-159">Í reitnum **Kóði** velurðu skattakóðann **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="c9e47-160">Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="c9e47-161">Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="c9e47-162">Í reitinn **Kóði** velurðu valkostinn **\*Ekki autt\***.</span><span class="sxs-lookup"><span data-stu-id="c9e47-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="c9e47-163">Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Annað**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="c9e47-164">Með því að bæta þessari skrá við skilgreinirðu eftirfarandi reglu: Alltaf þegar skattakóði sem er samþykktur sem frumbreyta uppfyllir engar af áðurnefndum reglum mun gagnagjafi uppflettingar skila **Annað** sem umbeðnu skattlagningarstigi.</span><span class="sxs-lookup"><span data-stu-id="c9e47-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="c9e47-166">Í reitnum **Staða** skal velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="c9e47-167">Þegar þú keyrir ER snið útgáfu sem hefur annaðhvort stöðuna **Lokið** eða **Deilt** verður þetta reglumengi að vera með stöðuna **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="c9e47-168">Annars verður framkvæmd grunn ER sniðsins rofin þegar sniðið reynir að hlaða gögnum úr þessu reglumengi þegar uppflettigagnagjafinn **Val** er keyrður.</span><span class="sxs-lookup"><span data-stu-id="c9e47-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="c9e47-169">Þegar þú keyrir ER snið útgáfu sem hefur stöðuna **Drög** hefur grunn ER sniðið aðgang að þessu reglumengi, óháð stöðu þess.</span><span class="sxs-lookup"><span data-stu-id="c9e47-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="c9e47-170">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-170">Select **Save**.</span></span>
18. <span data-ttu-id="c9e47-171">Lokaðu síðunni **Forritsbundnar færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="c9e47-172">Keyra ER sniðið í DEMF fyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="c9e47-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="c9e47-173">Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="c9e47-174">Í aðgerðarúðunni skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="c9e47-175">Í svarglugganum sem birtist skal smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="c9e47-176">Sæktu yfirlitið sem er búin til og geymdu hana á staðnum.</span><span class="sxs-lookup"><span data-stu-id="c9e47-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="c9e47-177">Taktu eftir því í myndaða uppgjörinu hefur skattakóðinn **InVAT7** verið settur á stigið **Minnkað** og samantektir á skattakóðunum **VSK19** og **InVA19** hafa verið settar á stigið **Reglulegt**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="c9e47-178">Þessi hegðun ræðst af stillingum í reglum sem eru háðir lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="c9e47-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="c9e47-179">Farðu í **Skattur \> Óbeinir skattar \> Virðisaukaskattur \> VSK-kóðar**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="c9e47-180">Veldu skattakóðann **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="c9e47-181">Á aðgerðarrúðunni, á flipanum **VSK-kóði**, í hópnum **Fyrirspurnir**, velurðu **Bókaður virðisaukaskattur** til að skoða upplýsingar um skatthlutfall og beitt skatthlutfall á hvern skattakóða.</span><span class="sxs-lookup"><span data-stu-id="c9e47-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Síðan Bókaður virðisaukaskattur](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="c9e47-183">Lokið síðunni Bókaður virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="c9e47-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="c9e47-184">Setja upp færibreytur fyrir fyrirtækið USMF</span><span class="sxs-lookup"><span data-stu-id="c9e47-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="c9e47-185">Velja skal lögaðilann **USMF**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="c9e47-186">Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="c9e47-187">Í stillingatrénu stækkarðu liðinn **Líkan til að læra færibreytur á köll**, stækkar liðinn **Snið til að læra færibreytur á köll** og velur sniðmátið **Snið til að læra hvernig á að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="c9e47-188">Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="c9e47-189">Veldu útgáfu **1.1.1** á völdu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="c9e47-190">Á flýtiflipanum **Skilyrði** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="c9e47-191">Í reitnum **Kóði** í nýju skránni velurðu fellilistaörina til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c9e47-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="c9e47-192">Núna sýnir uppflettingin lista yfir skattakóða fyrir **USMF** fyrirtækjaskatt fyrir val.</span><span class="sxs-lookup"><span data-stu-id="c9e47-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="c9e47-194">Veldu skattakóðann **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="c9e47-195">Í reitnum **Niðurstaða uppflettingar** í nýju skránni velurðu gildið **Engin skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="c9e47-196">Veldu aftur **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-196">Select **Add** again.</span></span>
11. <span data-ttu-id="c9e47-197">Í reitnum **Kóði** í nýju skránni velurðu valkostinn **\*Ekki autt\***.</span><span class="sxs-lookup"><span data-stu-id="c9e47-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="c9e47-198">Í reitnum **Niðurstaða uppflettingar** í nýju skránni velurðu gildið **Regluleg skattlagning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="c9e47-199">Í reitnum **Staða** skal velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="c9e47-200">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-200">Select **Save**.</span></span>

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="c9e47-202">Lokaðu síðunni **Forritsbundnar færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="c9e47-203">Keyra ER sniðið í USMF fyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="c9e47-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="c9e47-204">Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="c9e47-205">Í aðgerðarúðunni skal velja **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="c9e47-206">Í svarglugganum sem birtist skal smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="c9e47-207">Sæktu yfirlitið sem er búin til og geymdu hana á staðnum.</span><span class="sxs-lookup"><span data-stu-id="c9e47-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="c9e47-208">Taktu eftir því í tilkynningunni að þú hefur nú notað sama ER snið fyrir annan lögaðila en án þess að gera neinar breytingar á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="c9e47-209">Endurnýta færibreytur sem eru háðir lögaðilum</span><span class="sxs-lookup"><span data-stu-id="c9e47-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="c9e47-210">Útflutningsfæribreytur</span><span class="sxs-lookup"><span data-stu-id="c9e47-210">Export parameters</span></span>

1.  <span data-ttu-id="c9e47-211">Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="c9e47-212">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="c9e47-213">Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="c9e47-214">Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="c9e47-215">Veldu útgáfu **1.1.1** á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="c9e47-216">Á Aðgerðasvæðinu skal velja **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="c9e47-217">Sæktu skrána sem er búin til og geymdu hana á staðnum.</span><span class="sxs-lookup"><span data-stu-id="c9e47-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="c9e47-218">Nú er búið að flytja út stillt mengi af forritasértækum breytum sem XML skrá.</span><span class="sxs-lookup"><span data-stu-id="c9e47-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="c9e47-219">Innflutningsfæribreytur</span><span class="sxs-lookup"><span data-stu-id="c9e47-219">Import parameters</span></span>

1.  <span data-ttu-id="c9e47-220">Veldu útgáfu **1.1.2** á ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="c9e47-221">Á Aðgerðasvæðinu skal velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="c9e47-222">Veldu **Já** til að staðfesta að þú viljir hnekkja gildandi forritsbreytum fyrir þessa sniðútgáfu.</span><span class="sxs-lookup"><span data-stu-id="c9e47-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="c9e47-223">Veldu **Fletta** til að finna skrána sem hefur að geyma útfluttar forritsbundnar færibreytur fyrir útgáfu **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="c9e47-224">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-224">Select **OK**.</span></span>

    <span data-ttu-id="c9e47-225">Útgáfa **1.1.2** af ER sniði hefur nú sömu forritssértæku færibreytur og þú stilltir upphaflega fyrir útgáfu **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="c9e47-226">Athugið að forritssértækar færibreytur á ER sniði eru háðar lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="c9e47-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="c9e47-227">Til að endurnýta notendasértæku breyturnar sem voru stilltar fyrir einn lögaðila í öðrum lögaðilum, verður þú að flytja þær út meðan þú ert skráður inn á fyrsta lögaðilinn og flytja þær síðan inn eftir að þú hefur skráð þig inn í hinn lögaðila.</span><span class="sxs-lookup"><span data-stu-id="c9e47-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="c9e47-228">Þú getur líka notað þessa aðferð til að flytja ER-snið sem tengjast sérstökum breytum sem upphaflega voru stilltar í einu tilviki Finance í annað tilvik Finance.</span><span class="sxs-lookup"><span data-stu-id="c9e47-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="c9e47-229">Hafðu í huga að ef þú stillir forritasértækar breytur fyrir eina útgáfu af ER sniði og flytur inn hærri útgáfu af sama sniði í núverandi tilvik Finance, þá verður gildandi forritssértæku breytum ekki beitt fyrir innfluttu útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="c9e47-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="c9e47-230">Hafðu einnig í huga að þegar þú velur skrá til innflutnings er uppbygging forritasértæku færibreytanna í þeirri skrá borin saman við uppbyggingu samsvarandi gagnagjafa af gerðinni **Uppfletting** í ER sniðinu sem er valið til innflutnings.</span><span class="sxs-lookup"><span data-stu-id="c9e47-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="c9e47-231">Innflutningurinn er gerður þegar uppbygging hverrar forritasértækrar færibreytu passar við uppbyggingu samsvarandi gagnagjafa á ER sniði sem er valið til innflutnings.</span><span class="sxs-lookup"><span data-stu-id="c9e47-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="c9e47-232">Ef uppbyggingar passa ekki saman færðu viðvörunarskilaboð sem segja að ekki sé hægt að gera innflutninginn.</span><span class="sxs-lookup"><span data-stu-id="c9e47-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="c9e47-233">Ef þú þvingar framkvæmd á innflutningnum verða núverandi forritasértækar færibreytur fyrir valið ER snið hreinsaðar og það verður að setja þær upp á nýtt.</span><span class="sxs-lookup"><span data-stu-id="c9e47-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="c9e47-234">Samband á milli forritasértækra færibreytna og ER sniðs</span><span class="sxs-lookup"><span data-stu-id="c9e47-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="c9e47-235">Sambandi á milli ER sniðs og forritasértækum færibreyta þess er komið á með tilvikaóháðu sértæku auðkennisnúmeri ER sniðsins.</span><span class="sxs-lookup"><span data-stu-id="c9e47-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="c9e47-236">Þess vegna, þegar þú fjarlægir ER snið úr Finance, eru forritasértæku færibreyturnar sem eru stilltar fyrir ER sniðið geymdar í núverandi tilviki Finance.</span><span class="sxs-lookup"><span data-stu-id="c9e47-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="c9e47-237">Hægt er að fá aðgang að þeim hvenær sem ER-grunnsniðið er flutt aftur inn í þetta tilvik Finance.</span><span class="sxs-lookup"><span data-stu-id="c9e47-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="c9e47-238">Fáðu aðgang að forritasértækum færibreytum með því að nota ER ramma</span><span class="sxs-lookup"><span data-stu-id="c9e47-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="c9e47-239">Í dæminu á undan hefur þú fengið aðgang að forritasértækum færibreytum á ER sniði með því að nota ER ramma.</span><span class="sxs-lookup"><span data-stu-id="c9e47-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="c9e47-240">Þessi aðferð gerir þér ekki kleift að takmarka aðgang að forritasértækum breytum á tilteknu ER sniði.</span><span class="sxs-lookup"><span data-stu-id="c9e47-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="c9e47-241">Fylgdu þessum skrefum ef þú verður að beita slíkum takmörkunum.</span><span class="sxs-lookup"><span data-stu-id="c9e47-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="c9e47-242">Annaðhvort endurnýtirðu núverandi valmyndaratriðið **ERSolutionAppSpecificParametersDesigner** eða útfærir þitt eigið valmyndaratriði **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Síðan Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="c9e47-244">Fylgið einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="c9e47-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="c9e47-245">Búðu til nýjan hnapp fyrir valmyndaratriðið og tengdu hann við samsvarandi skrá úr töflunni **ERSolutionTable** með því að stilla eiginleikann **Gagnagjafi** á **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="c9e47-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Síðan Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="c9e47-247">Búðu til einfaldan hnapp og hnekktu eiginleikanum **Smellt** eins og sýnt er í eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="c9e47-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="c9e47-248">Með því að nota þessa aðferð geturðu tilgreint sérstakt auðkenni lausnar (skilgreint með gildinu **GUID**) til að leyfa aðgang að forritasértækum færibreytum á aðeins tilteknu ER sniði og afrit sem eru afleidd af þeim.</span><span class="sxs-lookup"><span data-stu-id="c9e47-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="c9e47-249">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c9e47-249">Additional resources</span></span>

[<span data-ttu-id="c9e47-250">Formúluhönnuður í rafrænni skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="c9e47-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="c9e47-251">Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila</span><span class="sxs-lookup"><span data-stu-id="c9e47-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
