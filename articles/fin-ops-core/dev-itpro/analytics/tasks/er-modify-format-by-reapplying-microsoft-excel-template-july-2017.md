---
title: Breyta sniðum með því að endurnýta Excel-sniðmát
description: Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, Rafræn skýrslugerð - Hanna grunnstillingu til að mynda skýrslur í OPENXML-sniði.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24eb64679b458d14e30dc5b4365c7305d71cfc4c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754891"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="cdb01-103">Breyta sniðum með því að endurnýta Excel-sniðmát</span><span class="sxs-lookup"><span data-stu-id="cdb01-103">Modify formats by reapplying Excel templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cdb01-104">Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, Rafræn skýrslugerð - Hanna grunnstillingu til að mynda skýrslur í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="cdb01-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="cdb01-105">Þetta ferli útskýrir hvernig skal breyta Rafræn skýrslugerð (ER) grunnstillingu sniðs með því að endurnýta Microsoft Excel sniðmát sem hefur verið breytt.</span><span class="sxs-lookup"><span data-stu-id="cdb01-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="cdb01-106">Í þessu ferli, muntu flytja breytt Excel sniðmát í Rafræn skýrslugerð grunnstillingar sniðs sem hefur verið stofnað fyrir sýnifyrirtækið, Litware, Inc., og síðan búa til rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="cdb01-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="cdb01-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="cdb01-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="cdb01-108">Skrefin er hægt að klára með því að nota GBSI gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="cdb01-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="cdb01-109">Áður en þú byrjar, skal hlaða niður og vista skránna, SampleVendPaymWsReport2.xlsx, sem er á lista í Hjálp efnisatriði, breyta sniði Rafræn skýrslugerð með því að endurnýta Excel sniðmát (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="cdb01-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="cdb01-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="cdb01-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="cdb01-111">Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="cdb01-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="cdb01-112">Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu Stofna skilgreiningarveitu og merkja hana sem virka.</span><span class="sxs-lookup"><span data-stu-id="cdb01-112">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="cdb01-113">Veljið snið Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="cdb01-113">Select the ER format</span></span>
1. <span data-ttu-id="cdb01-114">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="cdb01-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="cdb01-115">Stækkið eða fellið saman „Greiðslulíka“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="cdb01-116">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="cdb01-117">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="cdb01-117">Click Attachments.</span></span>
    * <span data-ttu-id="cdb01-118">Athugið að SampleVendPaymWsReport.xlsx Excel skjalið er nú notað sem sniðmát fyrir greiðslubókarvinnslu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="cdb01-119">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="cdb01-119">Click Open.</span></span>
    * <span data-ttu-id="cdb01-120">Smellið á Opna til að skoða útlit Excel sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="cdb01-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="cdb01-121">Yfirfara sniðmátið</span><span class="sxs-lookup"><span data-stu-id="cdb01-121">Review the template.</span></span> <span data-ttu-id="cdb01-122">Athugið að það inniheldur eins og er eftirfarandi upplýsingar fyrir hverja greiðslulínu: reikningsnúmer lánardrottins, nafn lánardrottins, banki, leiðarnúmer, reikningsnúmer, debet, kredit og gjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="cdb01-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="cdb01-123">Í þessu dæmi, viljum við útvíkka þennan lista með því að bæta upplýsingum við greiðsludagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="cdb01-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="cdb01-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cdb01-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="cdb01-125">Endurnýta nýtt Excel sniðmát í sniði Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="cdb01-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="cdb01-126">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="cdb01-126">Click Designer.</span></span>
    * <span data-ttu-id="cdb01-127">Opnið drög að sniði valinnar Rafræn skýrslugerð til að breyta.</span><span class="sxs-lookup"><span data-stu-id="cdb01-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="cdb01-128">Í aðgerðasvæðinu er smellt á innflutningur.</span><span class="sxs-lookup"><span data-stu-id="cdb01-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="cdb01-129">Smellið á Uppfæra úr Excel</span><span class="sxs-lookup"><span data-stu-id="cdb01-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="cdb01-130">Smellið á „Uppfæra sniðmát“ og veljið svo skrána SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="cdb01-130">Click 'Update template', and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="cdb01-131">Smellið á Uppfæra sniðmát og flettið til að ná í SampleVendPaymWsReport2.xlsx skránna sem var halað niður áður.</span><span class="sxs-lookup"><span data-stu-id="cdb01-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="cdb01-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-132">Click OK.</span></span>
    * <span data-ttu-id="cdb01-133">SampleVendPaymWsReport2.xlsx sniðmátið er virkt.</span><span class="sxs-lookup"><span data-stu-id="cdb01-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="cdb01-134">Skipan sniðs Rafræn skýrslugerð er samstillt við innihald sniðmátsins, hvers einingum er bætt við snið Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="cdb01-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="cdb01-135">Allar einingar sem enn eru til í sniði Rafræn skýrslugerð, en eru ekki innifaldar í sniðinu, eru teknar út úr skilgreiningu sniðsins.</span><span class="sxs-lookup"><span data-stu-id="cdb01-135">Any existing elements in the ER format that aren't included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="cdb01-136">Í trénu skal velja „Excel“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="cdb01-137">Athugið að sniðmátsreiturinn inniheldur nú tilvísun í nýja sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="cdb01-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="cdb01-138">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="cdb01-138">Click Attachments.</span></span>
7. <span data-ttu-id="cdb01-139">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="cdb01-139">Click Open.</span></span>
    * <span data-ttu-id="cdb01-140">Smellið á Opna til til að skoða útlit breytta Excel sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="cdb01-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="cdb01-141">Yfirfara sniðmátið</span><span class="sxs-lookup"><span data-stu-id="cdb01-141">Review the template.</span></span> <span data-ttu-id="cdb01-142">Athugið að nú inniheldur það línu fyrir greiðsludagsetningu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="cdb01-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cdb01-143">Close the page.</span></span>
9. <span data-ttu-id="cdb01-144">Stækkið „Excel“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="cdb01-145">Í tré skal víkka 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="cdb01-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="cdb01-146">Í tré skal velja „Excel\PaymLines\PaymDate“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="cdb01-147">Athugið að sniðið Rafræn skýrslugerð inniheldur nú fleira en eitt atriði.</span><span class="sxs-lookup"><span data-stu-id="cdb01-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="cdb01-148">Hólf, PaymDate, hefur verið bætt við Excel sniðmát.</span><span class="sxs-lookup"><span data-stu-id="cdb01-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="cdb01-149">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="cdb01-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="cdb01-150">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="cdb01-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="cdb01-151">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="cdb01-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="cdb01-152">Veljið 'model\Payments\Transaction date(TransactionDate)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="cdb01-153">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="cdb01-153">Click Bind.</span></span>
    * <span data-ttu-id="cdb01-154">Tilgreindu hvaða gögnum er bætt við nýja hólfið við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="cdb01-155">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-155">Click Save.</span></span>
18. <span data-ttu-id="cdb01-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cdb01-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="cdb01-157">Virkja breytt drög að sniði Rafræn skýrslugerð til notkunar í greiðslubókarvinnslu</span><span class="sxs-lookup"><span data-stu-id="cdb01-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="cdb01-158">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="cdb01-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="cdb01-159">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="cdb01-159">Click User parameters.</span></span>
3. <span data-ttu-id="cdb01-160">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="cdb01-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-161">Click OK.</span></span>
5. <span data-ttu-id="cdb01-162">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="cdb01-162">Click Edit.</span></span>
6. <span data-ttu-id="cdb01-163">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="cdb01-164">Nota breytt drög að sniði Rafræn skýrslugerð fyrir greiðslubókarvinnslu</span><span class="sxs-lookup"><span data-stu-id="cdb01-164">Use the modified draft version of the ER format for payment journal processing</span></span>

<span data-ttu-id="cdb01-165">Fara yfir stofnaðar vinnublað, þar á meðal nýjar upplýsingar um greiðslulínur – greiðsludagsetningu.</span><span class="sxs-lookup"><span data-stu-id="cdb01-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]