---
title: "Skilgreina kostnaðarstýringu"
description: "Þessi grein lýsir því sem þarf að hafa í huga og ákvörðunum sem þarf að taka í áætlunarferli áður en hægt er að skilgreina kostnaðarstýringu í Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5ac9959a4ee66e52ead5050897403602e407ca10
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="configure-expense-management"></a><span data-ttu-id="5a640-103">Skilgreina kostnaðarstýringu</span><span class="sxs-lookup"><span data-stu-id="5a640-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a640-104">Þetta efnisatriði lýsir því sem þarf að hafa í huga og ákvörðunum sem þarf að taka í áætlunarferli áður en hægt er að skilgreina kostnaðarstýringu í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5a640-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="5a640-105">Í kostnaðarstýringu, er hægt að geyma upplýsingar um greiðslumáta, ferðabeiðnir, kostnaðarskýrslur og stefnur og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="5a640-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="5a640-106">Þar sem margar þeirra ákvarðana sem gerðar eru við að áætla samskipan fyrir kostnaðarstýringu byggjast á stigveldi og fjárhagslegu skipulagi fyrirtækisins, verður að vísa til skipulagningarskjala fyrir þau svæði.</span><span class="sxs-lookup"><span data-stu-id="5a640-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="5a640-107">Kostnaður innan samstæðu</span><span class="sxs-lookup"><span data-stu-id="5a640-107">Intercompany expenses</span></span>

<span data-ttu-id="5a640-108">Þegar kostnaður innan samstæðu er virkjaður, er lögaðilum og starfsmönnum leyft að stofna til kostnaðar fyrir hönd annars lögaðila og innheimta greiðslur frá lögaðila innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5a640-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="5a640-109">Til dæmis lýkur starfsmaður í lögaðila A verkefni fyrir lögaðila B og verkefnið felur í sér ferðatengdan kostnað.</span><span class="sxs-lookup"><span data-stu-id="5a640-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="5a640-110">Ef kostnaður innan samstæðu er virkjaður getur starfsmaðurinn svo skráð kostnaðarskýrslu sem mun bóka kostnaðinn á lögaðila B, og lögaðili A verður að greiða útgjöldin. Ef fyrirtækið hefur ekki marga lögaðila þarf ekki að virkja kostnað innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="5a640-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="5a640-111">**Ákvörðun:** Á að virkja kostnað innan samstæðu?</span><span class="sxs-lookup"><span data-stu-id="5a640-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="5a640-112">Fjármálastjórnun</span><span class="sxs-lookup"><span data-stu-id="5a640-112">Financial management</span></span>

<span data-ttu-id="5a640-113">Kostnaðarstýring er samþætt náið með fjárhagslegar umsjón fyrirtækis þíns.</span><span class="sxs-lookup"><span data-stu-id="5a640-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="5a640-114">Mikið af stillingum fyrir kostnaðarstýringu munu byggjast á ákvörðunum sem teknar voru um fjármál fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5a640-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="5a640-115">Eftirfarandi kaflar lýsa ýmislegum svæðum sem krefjast áætlanagerðar og ákvarðana samkvæmt fjárhagslegum ákvörðunum og leiðbeiningum frá leiðtogateymi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5a640-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="5a640-116">Dagpeningar</span><span class="sxs-lookup"><span data-stu-id="5a640-116">Per diems</span></span>

<span data-ttu-id="5a640-117">Skilgreina verður dagpeningana sem fyrirtækið veitir starfsmanninum.</span><span class="sxs-lookup"><span data-stu-id="5a640-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="5a640-118">Þar sem dagpeningar eru vanalega notaðir til að ná yfir útgjöld, eins og fæði, leiguhúsnæði og annan tilfallandi kostnað, er hægt að stofna reglur fyrir dagpeningaheimildir sem fyrirtækið býður.</span><span class="sxs-lookup"><span data-stu-id="5a640-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="5a640-119">dagpeningataxti getur byggt á árstíma, ferðastað eða hvoru tveggja.</span><span class="sxs-lookup"><span data-stu-id="5a640-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5a640-120">Þegar dagpeningaregla er skilgreind er hægt að tilgreina að prósenta af dagpeningataxta verði haldið eftir ef starfsmaður fær ókeypis fæði eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="5a640-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5a640-121">Einnig er hægt að skilgreina lög af dagpeningataxta til að setja lágmarks- og hámarksfjölda klukkustunda sem hægt er að beita á ferðalög starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="5a640-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="5a640-122">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="5a640-122">**Decisions:**</span></span>

- <span data-ttu-id="5a640-123">Sjálfgefnar reglur fyrir dagpeninga fyrir fyrsta og síðasta daga:</span><span class="sxs-lookup"><span data-stu-id="5a640-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="5a640-124">Hver er lágmarksfjöldi stunda sem starfsmaður getur krafist á dag og fengið dagpeningar fyrir?</span><span class="sxs-lookup"><span data-stu-id="5a640-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="5a640-125">Er lækkun á þeirri upphæð sem er í boði fyrir máltíðir fyrir fyrsta dag og síðasta dag?</span><span class="sxs-lookup"><span data-stu-id="5a640-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="5a640-126">Ef lækkun er til staðar hversu hátt er hlutfall lækkunarinnar?</span><span class="sxs-lookup"><span data-stu-id="5a640-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5a640-127">Er lækkun á þeirri upphæð sem er í boði fyrir hótel fyrir fyrsta dag og síðasta dag?</span><span class="sxs-lookup"><span data-stu-id="5a640-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="5a640-128">Ef lækkun er til staðar hversu hátt er hlutfall lækkunarinnar?</span><span class="sxs-lookup"><span data-stu-id="5a640-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="5a640-129">Er lækkun á þeirri upphæð sem er í boði fyrir annan kostnað sem hlýst á fyrsta og síðasta degi?</span><span class="sxs-lookup"><span data-stu-id="5a640-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="5a640-130">Ef lækkun er til staðar hversu hátt er hlutfall lækkunarinnar?</span><span class="sxs-lookup"><span data-stu-id="5a640-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="5a640-131">Sjálfgefnar reglur fyrir dagpeninga:</span><span class="sxs-lookup"><span data-stu-id="5a640-131">Default per diem rules:</span></span>

    - <span data-ttu-id="5a640-132">Er prósentulækkun á dagpeningaheimild fyrir hverja máltíð, ef máltíðin er t.d. ókeypis?</span><span class="sxs-lookup"><span data-stu-id="5a640-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="5a640-133">Ef lækkun er til staðar hversu há er prósenta lækkunar fyrir hverja máltíð?</span><span class="sxs-lookup"><span data-stu-id="5a640-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="5a640-134">Er lækkun fæðispeninga reiknuð á dag, hverja ferð eða fjölda máltíða á dag?</span><span class="sxs-lookup"><span data-stu-id="5a640-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="5a640-135">Eiga dagpeningaupphæðir að vera sléttaðar á venjulegan hátt eða sléttaðar upp?</span><span class="sxs-lookup"><span data-stu-id="5a640-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="5a640-136">Eru dagpeningar reiknaðir á grundvelli 24 klst. tímabils eða almanaksdags?</span><span class="sxs-lookup"><span data-stu-id="5a640-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="5a640-137">Reglur um dagpeninga samkvæmt staðsetningu:</span><span class="sxs-lookup"><span data-stu-id="5a640-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="5a640-138">Eru dagpeningar breytilegir eftir staðsetningu?</span><span class="sxs-lookup"><span data-stu-id="5a640-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="5a640-139">Hvaða staðsetningar eru innifaldar?</span><span class="sxs-lookup"><span data-stu-id="5a640-139">What locations are included?</span></span>
    - <span data-ttu-id="5a640-140">Ef munur er dagpeningum eftir staðsetningu, fyrir hverja staðsetningu, hvaða prósentutala er veitt fyrir eftirfarandi kostnað:</span><span class="sxs-lookup"><span data-stu-id="5a640-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="5a640-141">Fæði</span><span class="sxs-lookup"><span data-stu-id="5a640-141">Meals</span></span>
        - <span data-ttu-id="5a640-142">Hótel</span><span class="sxs-lookup"><span data-stu-id="5a640-142">Hotel</span></span>
        - <span data-ttu-id="5a640-143">Annar kostnaður</span><span class="sxs-lookup"><span data-stu-id="5a640-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="5a640-144">Útgjaldastýringarbækur og -lyklar</span><span class="sxs-lookup"><span data-stu-id="5a640-144">Expense management journals and accounts</span></span>

<span data-ttu-id="5a640-145">Útgjaldastýring krefst þess að notaðar séu margar færslubækur og lyklar.</span><span class="sxs-lookup"><span data-stu-id="5a640-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="5a640-146">Það verður til dæmis að ákveða hvort sami lykillinn er notaður fyrir fyrirframgreiðslur og ágreining kreditkorts.</span><span class="sxs-lookup"><span data-stu-id="5a640-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="5a640-147">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="5a640-147">**Decisions:**</span></span>

- <span data-ttu-id="5a640-148">Hvaða færslubók á að bóka samþykktar útgjaldaskýrslur í?</span><span class="sxs-lookup"><span data-stu-id="5a640-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="5a640-149">Hvaða lykill er notaður fyrir fyrirframgreiðslur?</span><span class="sxs-lookup"><span data-stu-id="5a640-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="5a640-150">Á að bóka fyrirframgreiðslur strax?</span><span class="sxs-lookup"><span data-stu-id="5a640-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="5a640-151">Greiðslumátar</span><span class="sxs-lookup"><span data-stu-id="5a640-151">Payment methods</span></span>

<span data-ttu-id="5a640-152">Þegar starfsmönnum er leyft að stofna til kostnaðar fyrir hönd fyrirtækisins, verður að skilgreina greiðslumáta sem starfsmönnum er heimilt að nota.</span><span class="sxs-lookup"><span data-stu-id="5a640-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="5a640-153">Til dæmis væri hægt að leyfa starfsmönnum að nota reiðufé eða kreditkort fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5a640-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="5a640-154">Einnig væri hægt að leyfa starfsmönnum að nota persónuleg kreditkort og endurgreiða þeim síðan.</span><span class="sxs-lookup"><span data-stu-id="5a640-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="5a640-155">Gera verður eftirfarandi ákvarðanir fyrir hvern greiðslumáta sem á að leyfa.</span><span class="sxs-lookup"><span data-stu-id="5a640-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="5a640-156">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="5a640-156">**Decisions:**</span></span>

- <span data-ttu-id="5a640-157">Hvaða greiðslumátar eru heimilaðir?</span><span class="sxs-lookup"><span data-stu-id="5a640-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="5a640-158">Hver á útgjöld greiðslumátans?</span><span class="sxs-lookup"><span data-stu-id="5a640-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="5a640-159">Er gerð mótlykils til staðar?</span><span class="sxs-lookup"><span data-stu-id="5a640-159">Is there an offset account type?</span></span> <span data-ttu-id="5a640-160">Ef mótlykilsgerð er til staðar, hver er hún?</span><span class="sxs-lookup"><span data-stu-id="5a640-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="5a640-161">Ef mótlykill er til staðar, hver er lykillinn?</span><span class="sxs-lookup"><span data-stu-id="5a640-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="5a640-162">Ef greiðslumátinn er kreditkort, á einungis að nota greiðslumátann með innfluttum kreditkortafærslum?</span><span class="sxs-lookup"><span data-stu-id="5a640-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="5a640-163">Útgjaldaflokkar og samnýttir flokkar</span><span class="sxs-lookup"><span data-stu-id="5a640-163">Expense categories and shared categories</span></span>

<span data-ttu-id="5a640-164">Þegar starfsmenn stofna kostnaðarskýrslu, verða hver útgjöld sem þeir skrá að vera tengd við útgjaldaflokk.</span><span class="sxs-lookup"><span data-stu-id="5a640-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="5a640-165">Kostnaðartegundir eru afleiddar af samnýttum flokkum sem hægt er að deila með lögaðilum innan fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="5a640-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="5a640-166">Einnig er hægt að samnýta þessar tegundir í verkstjórnun og bókhaldi, allt eftir því hvernig fyrirtækið er skilgreint.</span><span class="sxs-lookup"><span data-stu-id="5a640-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="5a640-167">Samkvæmt grunni skilgreiningar fyrirtækisins og leiðbeiningum frá framkvæmdahópnum þarf að ákvarða hvort aðeins skuli nota flokkana sem eru notaðir í Útgjaldastýringu á Útgjaldastýringu eða hvort samnýta eigi þá milli Verkefnastjórnunar og bókhalds og Útgjaldastýringu.</span><span class="sxs-lookup"><span data-stu-id="5a640-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="5a640-168">Athugaðu að þessar tegundir er hægt að samnýta milli Verks og Kostnaðar eða Verks og Framleiðslu, en ekki á milli Kostnaðar og Framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="5a640-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="5a640-169">Taka verður eftirfarandi ákvarðanir fyrir hverja kostnaðartegund.</span><span class="sxs-lookup"><span data-stu-id="5a640-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="5a640-170">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="5a640-170">**Decisions:**</span></span>

- <span data-ttu-id="5a640-171">Hver er kostnaðarflokkurinn?</span><span class="sxs-lookup"><span data-stu-id="5a640-171">What is the expense category?</span></span> <span data-ttu-id="5a640-172">Dæmi eru flokkar fyrir flug, hótel eða vegalengd.</span><span class="sxs-lookup"><span data-stu-id="5a640-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="5a640-173">Er einnig hægt að nota kostnaðartegundina í Verkefnastjórnun og bókhaldi?</span><span class="sxs-lookup"><span data-stu-id="5a640-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="5a640-174">Hver er kostnaðartegundin?</span><span class="sxs-lookup"><span data-stu-id="5a640-174">What is the expense type?</span></span>
- <span data-ttu-id="5a640-175">Hver er sjálfgefinn greiðslumáti fyrir kostnaðartegunda?</span><span class="sxs-lookup"><span data-stu-id="5a640-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="5a640-176">Þarf að skilgreina kostnað í kostnaðarflokknum?</span><span class="sxs-lookup"><span data-stu-id="5a640-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="5a640-177">Hver er sjálfgefinn lykill fyrir kostnaðartegundina?</span><span class="sxs-lookup"><span data-stu-id="5a640-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="5a640-178">Hver er sjálfgefinn VSK-flokkur vöru fyrir kostnaðartegunda?</span><span class="sxs-lookup"><span data-stu-id="5a640-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="5a640-179">Eru viðbótar greiðslumátar leyfðir fyrir kostnaðartegunda?</span><span class="sxs-lookup"><span data-stu-id="5a640-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="5a640-180">Ef viðbótargreiðslumátar eru heimilaðir, hverjir eru þeir?</span><span class="sxs-lookup"><span data-stu-id="5a640-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="5a640-181">Eru undirtegundir í þessari kostnaðartegund?</span><span class="sxs-lookup"><span data-stu-id="5a640-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="5a640-182">Ef undirflokkar eru til staðar þarf einnig að taka eftirfarandi ákvarðanir:</span><span class="sxs-lookup"><span data-stu-id="5a640-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="5a640-183">Er einhverjum undirtegundum sleppt úr skattendurgreiðslum?</span><span class="sxs-lookup"><span data-stu-id="5a640-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="5a640-184">Hver er VSK-flokkur vöru fyrir undirtegundirnar?</span><span class="sxs-lookup"><span data-stu-id="5a640-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="5a640-185">Ef kostnaðartegundin er einnig notuð í verkstjórnun og bókhaldi, þarf að svara eftirstandandi spurningum.</span><span class="sxs-lookup"><span data-stu-id="5a640-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="5a640-186">Annars skaltu færa þig yfir í næsta kafla.</span><span class="sxs-lookup"><span data-stu-id="5a640-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="5a640-187">Hvaða kostnaðarlyklar verða notaðir fyrir eftirfarandi kkostnað?</span><span class="sxs-lookup"><span data-stu-id="5a640-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="5a640-188">Kostnaður</span><span class="sxs-lookup"><span data-stu-id="5a640-188">Cost</span></span>
    - <span data-ttu-id="5a640-189">Launaskipting</span><span class="sxs-lookup"><span data-stu-id="5a640-189">Payroll allocation</span></span>
    - <span data-ttu-id="5a640-190">VÍV - Kostnaðarverðmæti</span><span class="sxs-lookup"><span data-stu-id="5a640-190">WIP-cost value</span></span>
    - <span data-ttu-id="5a640-191">Kostnaður - Vara</span><span class="sxs-lookup"><span data-stu-id="5a640-191">Cost-item</span></span>
    - <span data-ttu-id="5a640-192">VÍV - Kostnaðarvirði - Vara</span><span class="sxs-lookup"><span data-stu-id="5a640-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="5a640-193">Uppsafnað tap</span><span class="sxs-lookup"><span data-stu-id="5a640-193">Accrued loss</span></span>
    - <span data-ttu-id="5a640-194">VÍV - Uppsafnað tap</span><span class="sxs-lookup"><span data-stu-id="5a640-194">WIP-accrued loss</span></span>

- <span data-ttu-id="5a640-195">Hvaða tekjulyklar verða notaðir fyrir eftirfarandi?</span><span class="sxs-lookup"><span data-stu-id="5a640-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="5a640-196">Reikningsfærðar tekjur</span><span class="sxs-lookup"><span data-stu-id="5a640-196">Invoiced revenue</span></span>
    - <span data-ttu-id="5a640-197">Áfallnar tekjur - Söluverðmæti</span><span class="sxs-lookup"><span data-stu-id="5a640-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="5a640-198">VÍV - söluvirði</span><span class="sxs-lookup"><span data-stu-id="5a640-198">WIP-sales value</span></span>
    - <span data-ttu-id="5a640-199">Áfallnar tekjur - Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="5a640-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="5a640-200">VÍV - Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="5a640-200">WIP-production</span></span>
    - <span data-ttu-id="5a640-201">Áfallnar tekjur - Hagnaður</span><span class="sxs-lookup"><span data-stu-id="5a640-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="5a640-202">VÍV - Hagnaður</span><span class="sxs-lookup"><span data-stu-id="5a640-202">WIP-profit</span></span>
    - <span data-ttu-id="5a640-203">Áfallnar tekjur - Áskrift</span><span class="sxs-lookup"><span data-stu-id="5a640-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="5a640-204">VÍV - Áskrift</span><span class="sxs-lookup"><span data-stu-id="5a640-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="5a640-205">Skattar</span><span class="sxs-lookup"><span data-stu-id="5a640-205">Taxes</span></span>

<span data-ttu-id="5a640-206">Fyrir kostnað sem tengist sköttum verður að ákvarða hvað er tekið með eða virkjað í kostnaðarskýrslum.</span><span class="sxs-lookup"><span data-stu-id="5a640-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="5a640-207">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="5a640-207">**Decisions:**</span></span>

- <span data-ttu-id="5a640-208">Er virðisaukaskattur innifalinn í upphæð kostnaðar?</span><span class="sxs-lookup"><span data-stu-id="5a640-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="5a640-209">Á að virkja skattendurgreiðslur í útgjöldum?</span><span class="sxs-lookup"><span data-stu-id="5a640-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a640-210">Ef þú hefur við áætlun í fjárhag ákveðið að nota bandarískan virðisaukaskatt og reglur neysluskatts er ekki hægt að virkja skattendurgreiðslu á útgjöldum.</span><span class="sxs-lookup"><span data-stu-id="5a640-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="5a640-211">(Til að nota bandarískar söluskatts- og neysluskattareglur skal stilla **Nota skattareglur virðisaukaskatts** valkostinn á **Já**.)</span><span class="sxs-lookup"><span data-stu-id="5a640-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="5a640-212">Reglur</span><span class="sxs-lookup"><span data-stu-id="5a640-212">Policies</span></span>

<span data-ttu-id="5a640-213">Með því að stofna kostnaðarskýrslureglur getur fyrirtækið sparað peninga og tíma þegar starfsmenn stofna til útgjalda fyrir hönd þess.</span><span class="sxs-lookup"><span data-stu-id="5a640-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="5a640-214">Reglur hjálpa til við að tryggja að starfsmenn séu innan fjárhagsáætlunar, veiti allar nauðsynlegar upplýsingar og eyði aðeins fé eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5a640-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="5a640-215">Taka verður eftirfarandi ákvarðanir fyrir hverja kostnaðarreglu og hverja samþykktarreglu kostnaðarskýrslu sem þú stofnar.</span><span class="sxs-lookup"><span data-stu-id="5a640-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="5a640-216">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="5a640-216">**Decisions:**</span></span>

- <span data-ttu-id="5a640-217">Hvert er heiti reglunnar?</span><span class="sxs-lookup"><span data-stu-id="5a640-217">What is the name of the policy?</span></span>
- <span data-ttu-id="5a640-218">Til hvers er kostnaðarreglan?</span><span class="sxs-lookup"><span data-stu-id="5a640-218">What is the expense policy for?</span></span>
- <span data-ttu-id="5a640-219">Ef þú ákvaðst áður að virkja kostnað innan samstæðu, fyrir hvaða fyrirtæki í samstæðunni á þessi regla við?</span><span class="sxs-lookup"><span data-stu-id="5a640-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="5a640-220">Hvenær verður reglan virk?</span><span class="sxs-lookup"><span data-stu-id="5a640-220">When does the policy become effective?</span></span>
- <span data-ttu-id="5a640-221">Hvenær verður úreldist reglan?</span><span class="sxs-lookup"><span data-stu-id="5a640-221">When does the policy expire?</span></span>
- <span data-ttu-id="5a640-222">Hvað er stefnuregla?</span><span class="sxs-lookup"><span data-stu-id="5a640-222">What is the policy rule?</span></span>
- <span data-ttu-id="5a640-223">Hver er útkoma stefnureglunnar?</span><span class="sxs-lookup"><span data-stu-id="5a640-223">What is the outcome of the policy rule?</span></span>

