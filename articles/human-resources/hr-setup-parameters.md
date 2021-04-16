---
title: Grunnstilla færibreytur Human Resources
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp fyrirtækjaháðar færibreytur í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 74bdf891ffa7a9d875e23cf46aeee1dbaf86db48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802408"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="11188-103">Grunnstilla færibreytur Human Resources</span><span class="sxs-lookup"><span data-stu-id="11188-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="11188-104">Stillingar fyrir sumar færibreytur Mannauðs eru eins milli fyrirtækja, á meðan stillingar annara færibreyta eru bundnar tilteknu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="11188-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="11188-105">Í þessu efnisatriði er útskýrt hvernig á að setja upp færibreytur fyrir mannauð.</span><span class="sxs-lookup"><span data-stu-id="11188-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="11188-106">Tvær síður eru notaðar til að setja upp færibreytur mannauðs.</span><span class="sxs-lookup"><span data-stu-id="11188-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="11188-107">Fyrir Færibreytur sem fyrirtæki samnýta, notarðu **samnýttar færibreytur fyrir mannauð** síðu.</span><span class="sxs-lookup"><span data-stu-id="11188-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="11188-108">Fyrir færibreytur sem eru bundin tilteknu fyrirtæki (með öðrum orðum, stillingar eiga við um eitt fyrirtæki), notarðu **færibreytum mannauðs** síðu.</span><span class="sxs-lookup"><span data-stu-id="11188-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Opna Færibreytur mannauðs](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="11188-110">Á **færibreytur Mannauðs** síða, er stillingum deild á sex flipa:</span><span class="sxs-lookup"><span data-stu-id="11188-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="11188-111">**Almennt**</span><span class="sxs-lookup"><span data-stu-id="11188-111">**General**</span></span>
- <span data-ttu-id="11188-112">**Ráðning** (Þessi flipi er ekki tekinn með í Dynamics 365 Human Resources)</span><span class="sxs-lookup"><span data-stu-id="11188-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="11188-113">**Laun**</span><span class="sxs-lookup"><span data-stu-id="11188-113">**Compensation**</span></span>
- <span data-ttu-id="11188-114">**Númeraraðir**</span><span class="sxs-lookup"><span data-stu-id="11188-114">**Number sequences**</span></span>
- <span data-ttu-id="11188-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="11188-115">**FMLA**</span></span>
- <span data-ttu-id="11188-116">**Sjálfsafgreiðsla starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="11188-116">**Employee self service**</span></span>
- <span data-ttu-id="11188-117">**Sjálfsafgreiðsla stjórnanda**</span><span class="sxs-lookup"><span data-stu-id="11188-117">**Manager self service**</span></span>
- <span data-ttu-id="11188-118">**Fríðindastjórnun**</span><span class="sxs-lookup"><span data-stu-id="11188-118">**Benefits management**</span></span>
- <span data-ttu-id="11188-119">**Leyfi og fjarvera**</span><span class="sxs-lookup"><span data-stu-id="11188-119">**Leave and absence**</span></span>
- <span data-ttu-id="11188-120">**Greiðsluhættir**</span><span class="sxs-lookup"><span data-stu-id="11188-120">**Payment methods**</span></span>

<span data-ttu-id="11188-121">Hver flipi inniheldur upplýsingar sem tengjast einu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="11188-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="11188-122">Almennt</span><span class="sxs-lookup"><span data-stu-id="11188-122">General</span></span>

<span data-ttu-id="11188-123">Stillingar á í **Almennt** flipanum skilgreina útlit hvers upplýsinga um fjarvistir, meiðsla og veikinda og nýráðningar.</span><span class="sxs-lookup"><span data-stu-id="11188-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="11188-124">Stillingar á þessum flipa skilgreina einnig sumar sjálfgefnar færslur sem birtast meðfram vinnu.</span><span class="sxs-lookup"><span data-stu-id="11188-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="11188-125">Þessi flipi gerir þér kelift að:</span><span class="sxs-lookup"><span data-stu-id="11188-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="11188-126">Veljið lit til að hafa á opnum fjarvistafærslum</span><span class="sxs-lookup"><span data-stu-id="11188-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="11188-127">Tilgreinið stílblað sem nota á fyrir skýrslur</span><span class="sxs-lookup"><span data-stu-id="11188-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="11188-128">Virkja samþættingu milli þjálfunarnámskeiða og fjarvistaskráningar</span><span class="sxs-lookup"><span data-stu-id="11188-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="11188-129">Veljið fjarvistarkóðann sem er notaður til að hafa stjórna þessari samþættingu.</span><span class="sxs-lookup"><span data-stu-id="11188-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="11188-130">Tilgreinið hversu lengi á að geyma tilfelli meiðsla og veikinda.</span><span class="sxs-lookup"><span data-stu-id="11188-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="11188-131">Tilgreinið sjálfgefna auðkennisnúmerið sem birtist þegar nýr starfskraftur er ráðinn.</span><span class="sxs-lookup"><span data-stu-id="11188-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Almennt](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="11188-133">Ráðning</span><span class="sxs-lookup"><span data-stu-id="11188-133">Recruitment</span></span>

<span data-ttu-id="11188-134">Stillingarnar í flipanum **Ráðning** skilgreina skjalagerðir sem eru notaðar fyrir samskipti sem send eru sjálfkrafa til umsækjenda.</span><span class="sxs-lookup"><span data-stu-id="11188-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="11188-135">Einnig er hægt að tilgreina ráðningarverk sem er notað fyrir lánardrottinsumsækjendur.</span><span class="sxs-lookup"><span data-stu-id="11188-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="11188-136">Tímabilið sem er skilgreint fyrir aldursgreiningu ráðningarverks ákvarðar ráðningarverk sem eru innifalin í reitnum **Aldursgreiningarverk** á vinnusvæðinu **Umsjón með ráðningum**.</span><span class="sxs-lookup"><span data-stu-id="11188-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="11188-137">Tímabilið sem er skilgreint fyrir viðvörun lokafrests umsóknar er notað til að birta ráðningarverk sem eru að nálgast skilafrest sinn á í **skilafrestur umsóknar nálgast** reit í **Ráðningarverk** vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="11188-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="11188-138">Frekari upplýsingar um ráðningar er að finna í [Ráða umsækjendur](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="11188-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="11188-139">Laun</span><span class="sxs-lookup"><span data-stu-id="11188-139">Compensation</span></span>

<span data-ttu-id="11188-140">Í Dynamics 365 Finance skilgreina stillingar á **Laun** flipanum hvort notendur verða staðfesta að þeir vilji að vista upplýsingar fyrir fast eða breytilegt launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="11188-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="11188-141">Ef **Virkja villuleit vistunar** er valið þegar notendur loka síðu sem tengist launum þar sem spurt er hvort þeir vilji vista færsluna.</span><span class="sxs-lookup"><span data-stu-id="11188-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="11188-142">Sumar síður í lausnastjórnun leyfa ekki notendum að eyða upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="11188-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="11188-143">Með því að senda kvaðningu til notenda til að staðfesta að þeir vilja að vista upplýsingar, gætirðu takmarkað magn upplýsinga sem er vistað en ekki er hægt að eyða síðar.</span><span class="sxs-lookup"><span data-stu-id="11188-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="11188-144">Ef **Virkja vistun villuleitar** er hreinsað vistast færslur um leið, hugsanlega áður en notandinn er tilbúinn.</span><span class="sxs-lookup"><span data-stu-id="11188-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="11188-145">Ef frammistöðustjórnun er notuð leyfir flipinn **Laun** einnig að velja matslíkan til að nota í staðinn fyrir líkanið sem er úthlutað á launafyrirkomulag þegar frammistaða er metin.</span><span class="sxs-lookup"><span data-stu-id="11188-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="11188-146">Í Human Resources er hægt að nota flipann **Laun** til að velja að takmarka aðgang að launafyrirkomulagi og til að stilla sjálfgefinn gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="11188-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="11188-147">Frekari upplýsingar um laun er að finna í [Yfirlit launafyrirkomulags](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11188-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Flipinn Laun](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="11188-149">Númeraraðir</span><span class="sxs-lookup"><span data-stu-id="11188-149">Number sequences</span></span>

<span data-ttu-id="11188-150">Stillingarnar í flipanum **Númeraröð** ákvarða raðirnar sem verða notuð til að úthluta auðkennum sjálfkrafa á atriði í Human Resources, t.d.:</span><span class="sxs-lookup"><span data-stu-id="11188-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="11188-151">Hugbúnaður</span><span class="sxs-lookup"><span data-stu-id="11188-151">Applications</span></span>
- <span data-ttu-id="11188-152">Fjarvistaskráningar</span><span class="sxs-lookup"><span data-stu-id="11188-152">Absence registrations</span></span>
- <span data-ttu-id="11188-153">Niðurstöður launavinnslu</span><span class="sxs-lookup"><span data-stu-id="11188-153">Compensation process results</span></span>
- <span data-ttu-id="11188-154">Málsnúmer</span><span class="sxs-lookup"><span data-stu-id="11188-154">Case numbers</span></span>
- <span data-ttu-id="11188-155">Námskeið</span><span class="sxs-lookup"><span data-stu-id="11188-155">Courses</span></span>
- <span data-ttu-id="11188-156">Dagskrá námskeiðs</span><span class="sxs-lookup"><span data-stu-id="11188-156">Course agendas</span></span>

<span data-ttu-id="11188-157">Til að vinna með tilvísanir númeraraða og kóða skal nota **Númeraraðir** listasíðu (valið er **fyrirtækisstjórnun > Númeraraðir > Númeraraðir**).</span><span class="sxs-lookup"><span data-stu-id="11188-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="11188-158">Frekari upplýsingar er að finna í [Yfirlit númeraraða](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span><span class="sxs-lookup"><span data-stu-id="11188-158">For more information, see [Number sequences overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/human-resources/toc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="11188-159">Fjölda stunda sem er unnið má ekki fara yfir 1,250 og lengd ráðningar má ekki fara yfir 12 mánuði.</span><span class="sxs-lookup"><span data-stu-id="11188-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="11188-160">Þessi hámarksgildi eru samkvæmt alríkislögum í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="11188-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Flipinn Númeraraðir](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="11188-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="11188-162">FMLA</span></span>

<span data-ttu-id="11188-163">Í flipanum FMLA eru FMLA-hæfiskröfur og vinnustundir FMLA-réttinda.</span><span class="sxs-lookup"><span data-stu-id="11188-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="11188-164">Frekari upplýsingar eru í [Grunnstilla færibreytur leyfis og fjarvista](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="11188-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA-flipi](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="11188-166">Sjálfsafgreiðsla starfsmanns</span><span class="sxs-lookup"><span data-stu-id="11188-166">Employee self service</span></span>

<span data-ttu-id="11188-167">Stillingarnar í flipanum **Sjálfsafgreiðsla starfsmanns** hafa áhrif á það hvernig sjálfsafgreiðsla starfsmanns birtist starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="11188-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="11188-168">Á þessum flipa er hægt að:</span><span class="sxs-lookup"><span data-stu-id="11188-168">On this tab, you can:</span></span>

- <span data-ttu-id="11188-169">Færið inn heiti á vinnusvæði fyrir sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="11188-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="11188-170">Veljið hvaða upplýsingar yfirmaður getur fært inn fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="11188-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="11188-171">Bæta við gagnlegum tenglum fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="11188-171">Add useful links for employees</span></span>
- <span data-ttu-id="11188-172">Takmarkið getu starfsmanni til að bæta við eða breyta tengiliðaupplýsingum fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="11188-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="11188-173">Frekari upplýsingar er að finna [Við uppsetningu runuvinnslunnar](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="11188-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="11188-174">Frekari upplýsingar um uppsetningu á sjálfsafgreiðslu starfsmanna er að finna í [Yfirlit yfir sjálfsafgreiðslu starfsmanns og stjórnanda](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11188-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Sjálfsafgreiðsluflipi starfsmanns](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="11188-176">Sjálfsafgreiðsla stjórnanda</span><span class="sxs-lookup"><span data-stu-id="11188-176">Manager self service</span></span>

<span data-ttu-id="11188-177">Stillingar í flipanum **Sjálfsafgreiðsla starfsmanns** hafa áhrif á hvað stjórnendur sjá í sjálfsafgreiðslu stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="11188-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="11188-178">Í þessum flipa er hægt að skilgreina eftirfarandi valkosti:</span><span class="sxs-lookup"><span data-stu-id="11188-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="11188-179">Svið fyrir færslur sem eru að renna út</span><span class="sxs-lookup"><span data-stu-id="11188-179">The range for expiring records</span></span>
- <span data-ttu-id="11188-180">Stjórnendur upplýsinga geta skoðað færslur sem eru að renna út</span><span class="sxs-lookup"><span data-stu-id="11188-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="11188-181">Hvort stjórnendur geta skoðað opnar stöður fyrir stækkaðar skýrslur</span><span class="sxs-lookup"><span data-stu-id="11188-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="11188-182">Yfirlit starfskrafta sem eru að hætta</span><span class="sxs-lookup"><span data-stu-id="11188-182">Views of exiting workers</span></span>
- <span data-ttu-id="11188-183">Gagnlegir tenglar fyrir stjórnendur</span><span class="sxs-lookup"><span data-stu-id="11188-183">Useful links for managers</span></span>

<span data-ttu-id="11188-184">Frekari upplýsingar um uppsetningu á sjálfsafgreiðslu stjórnanda er að finna í [Yfirlit yfir sjálfsafgreiðslu starfsmanns og stjórnanda](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11188-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Sjálfsafgreiðsluflipi stjórnanda](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="11188-186">Fríðindastjórnun</span><span class="sxs-lookup"><span data-stu-id="11188-186">Benefits management</span></span>

<span data-ttu-id="11188-187">Í flipa fríðindastjórnunar er hægt að skilgreina valkosti tölvupósts fyrir fríðindastjórnun.</span><span class="sxs-lookup"><span data-stu-id="11188-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="11188-188">Frekari upplýsingar um uppsetningu og notkun fríðindastjórnunar er að finna í [Yfirlit fríðindastjórnunar](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11188-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Fríðindastjórnunarflipi](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="11188-190">Leyfi og fjarvera</span><span class="sxs-lookup"><span data-stu-id="11188-190">Leave and absence</span></span>

<span data-ttu-id="11188-191">Upplýsingar um uppsetningu og notkun leyfa og fjarvista er að finna í [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11188-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="11188-192">Greiðsluhættir</span><span class="sxs-lookup"><span data-stu-id="11188-192">Payment methods</span></span>

<span data-ttu-id="11188-193">Í flipanum **Greiðslumátar** er hægt að velja greiðslumátana sem fyrirtækið styður.</span><span class="sxs-lookup"><span data-stu-id="11188-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="11188-194">Frekari upplýsingar um skilgreiningu launa er að finna í [Yfirlit launafyrirkomulags](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11188-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Flipi Greiðsluhátta](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]