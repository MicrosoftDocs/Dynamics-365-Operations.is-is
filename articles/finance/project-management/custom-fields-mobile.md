---
title: Innleiða sérstillta reiti fyrir Microsoft Dynamics 365 Project Timesheet-farsímaforritið í iOS og Android
description: Þetta efnisatriði býður upp á algeng mynstur til að nota viðbætur til að innleiða sérstillta reiti.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: c0c578ca44919671b67daeea51a9ec7687f755c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773646"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="f3210-103">Innleiða sérstillta reiti fyrir Microsoft Dynamics 365 Project Timesheet-farsímaforritið í iOS og Android</span><span class="sxs-lookup"><span data-stu-id="f3210-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3210-104">Þetta efnisatriði býður upp á algeng mynstur til að nota viðbætur til að innleiða sérstillta reiti.</span><span class="sxs-lookup"><span data-stu-id="f3210-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="f3210-105">Fjallað er um eftirfarandi efnisatriði:</span><span class="sxs-lookup"><span data-stu-id="f3210-105">The following topics are covered:</span></span>

- <span data-ttu-id="f3210-106">Hinar ýmsu gagnagerðir sem rammi sérstillts reits styður</span><span class="sxs-lookup"><span data-stu-id="f3210-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="f3210-107">Hvernig á að sýna skrifvarða eða breytanlega reiti í færslum vinnukorts og vista gildi sem notandi hefur bætt við í gagnagrunninn</span><span class="sxs-lookup"><span data-stu-id="f3210-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="f3210-108">Hvernig á að sýna skrifvarða reiti í haus vinnukortsins</span><span class="sxs-lookup"><span data-stu-id="f3210-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="f3210-109">Hvernig á að samþætta annan sérstilltan viðskiptagrunn til að færa inn sjálfgildi í reitina og gera frekari villuleit</span><span class="sxs-lookup"><span data-stu-id="f3210-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="f3210-110">Notendahópur</span><span class="sxs-lookup"><span data-stu-id="f3210-110">Audience</span></span>

<span data-ttu-id="f3210-111">Þetta efnisatriði er ætlað þróunaraðilum sem eru að samþætta sérstillta reiti sína við Microsoft Dynamics 365 Project Timesheet-farsímaforritið sem er í boði fyrir Apple iOS og Google Android.</span><span class="sxs-lookup"><span data-stu-id="f3210-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="f3210-112">Gert er ráð fyrir að lesendur séu kunnugir X++ þróun og virkni vinnukorts fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="f3210-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="f3210-113">Gagnasamningur - TSTimesheetCustomField X++ klasi</span><span class="sxs-lookup"><span data-stu-id="f3210-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="f3210-114">Klasinn **TSTimesheetCustomField** er X++ gagnasamningsklasinn sem veitir upplýsingar um sérstilltan reit fyrir virkni vinnukorts.</span><span class="sxs-lookup"><span data-stu-id="f3210-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="f3210-115">Listar yfir hluti sérstillts reits eru bæði fluttir yfir í TSTimesheetDetails gagnasamning og TSTimesheetEntry gagnasamning til að sýna sérstillta reiti í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="f3210-116">**TSTimesheetDetails** Síðuhaus vinnukortasamnings.</span><span class="sxs-lookup"><span data-stu-id="f3210-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="f3210-117">**TSTimesheetEntry** - Færsla vinnukortasamnings.</span><span class="sxs-lookup"><span data-stu-id="f3210-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="f3210-118">Flokkar þessara hluta sem eru með sömu verkupplýsingarnar og gildið **timesheetLineRecId** gera línu.</span><span class="sxs-lookup"><span data-stu-id="f3210-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="f3210-119">fieldBaseType (gerðir)</span><span class="sxs-lookup"><span data-stu-id="f3210-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="f3210-120">Eiginleikinn **FieldBaseType** í hlutnum **TsTimesheetCustom** ákvarðar gerð reitsins sem birtist í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="f3210-121">Eftirfarandi gildin fyrir **Gerðir** sem eru studdar.</span><span class="sxs-lookup"><span data-stu-id="f3210-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="f3210-122">Gildi gerða</span><span class="sxs-lookup"><span data-stu-id="f3210-122">Types value</span></span> | <span data-ttu-id="f3210-123">Gerð</span><span class="sxs-lookup"><span data-stu-id="f3210-123">Type</span></span>              | <span data-ttu-id="f3210-124">Athugasemdir</span><span class="sxs-lookup"><span data-stu-id="f3210-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="f3210-125">0</span><span class="sxs-lookup"><span data-stu-id="f3210-125">0</span></span>           | <span data-ttu-id="f3210-126">Strengur (og fasttexti)</span><span class="sxs-lookup"><span data-stu-id="f3210-126">String (and Enum)</span></span> | <span data-ttu-id="f3210-127">Reitinn birtist sem textareitur.</span><span class="sxs-lookup"><span data-stu-id="f3210-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="f3210-128">1</span><span class="sxs-lookup"><span data-stu-id="f3210-128">1</span></span>           | <span data-ttu-id="f3210-129">Heiltala</span><span class="sxs-lookup"><span data-stu-id="f3210-129">Integer</span></span>           | <span data-ttu-id="f3210-130">Gildi er sýnt sem tala án aukastafa.</span><span class="sxs-lookup"><span data-stu-id="f3210-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="f3210-131">2</span><span class="sxs-lookup"><span data-stu-id="f3210-131">2</span></span>           | <span data-ttu-id="f3210-132">Rauntala</span><span class="sxs-lookup"><span data-stu-id="f3210-132">Real</span></span>              | <span data-ttu-id="f3210-133">Gildi er sýnt sem tala með aukastafi.</span><span class="sxs-lookup"><span data-stu-id="f3210-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="f3210-134">Til að sýna raunverulegt gildi sem gjaldmiðil í forritinu skal nota eiginleikann **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="f3210-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="f3210-135">Hægt er að nota eiginleikann **numberOfDecimals** til að stilla fjölda aukastafa sem á að sýna.</span><span class="sxs-lookup"><span data-stu-id="f3210-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="f3210-136">3</span><span class="sxs-lookup"><span data-stu-id="f3210-136">3</span></span>           | <span data-ttu-id="f3210-137">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="f3210-137">Date</span></span>              | <span data-ttu-id="f3210-138">Dagsetningarsnið eru ákvörðuð af stillingunum **Dagsetningar-, tíma- og númerasnið** sem notandi velur og eru tilgreind undir **Kjörstilling fyrir tungumál og land/svæði** í **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="f3210-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="f3210-139">4</span><span class="sxs-lookup"><span data-stu-id="f3210-139">4</span></span>           | <span data-ttu-id="f3210-140">Boole</span><span class="sxs-lookup"><span data-stu-id="f3210-140">Boolean</span></span>           | |
| <span data-ttu-id="f3210-141">15</span><span class="sxs-lookup"><span data-stu-id="f3210-141">15</span></span>          | <span data-ttu-id="f3210-142">GUID</span><span class="sxs-lookup"><span data-stu-id="f3210-142">GUID</span></span>              | |
| <span data-ttu-id="f3210-143">16</span><span class="sxs-lookup"><span data-stu-id="f3210-143">16</span></span>          | <span data-ttu-id="f3210-144">Int64</span><span class="sxs-lookup"><span data-stu-id="f3210-144">Int64</span></span>             | |

- <span data-ttu-id="f3210-145">Ef eiginleikinn **stringOptions** er ekki gefinn upp í hlutnum **TSTimesheetCustomField** er notandanum útvegaður reitur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="f3210-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="f3210-146">Hægt er að nota eiginleikann **stringLength** til að stilla hámarkslengd á streng sem notendur geta fært inn.</span><span class="sxs-lookup"><span data-stu-id="f3210-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="f3210-147">Ef boðið er upp á eiginleikann **stringOptions** í hlutnum **TSTimesheetCustomField** eru þessar listaeiningar einu gildin sem notendur geta valið með því að nota valhnappa (valhringi).</span><span class="sxs-lookup"><span data-stu-id="f3210-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="f3210-148">Í þessu tilviki getur strengjareiturinn virkað sem fasttextagildi gagngert fyrir færslu notanda.</span><span class="sxs-lookup"><span data-stu-id="f3210-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="f3210-149">Til að vista gildið í gagnagrunninum sem fasttexta skal varpa strengjagildinu handvirkt aftur í fasttextagildið áður en vistað er í gagnagrunninn með því að nota boðleið (sjá kaflann „Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslu úr forritinu aftur í gagnagrunninn“ seinna í þessu efnisatriði til að sjá dæmi).</span><span class="sxs-lookup"><span data-stu-id="f3210-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="f3210-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="f3210-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="f3210-151">Hægt er að nota þennan eiginleika til að sníða raunveruleg gildi sem gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="f3210-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="f3210-152">Þessi nálgun á eingöngu við þegar gildið **fieldBaseType** er **Raunverulegt**.</span><span class="sxs-lookup"><span data-stu-id="f3210-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="f3210-153">**TSCustomFieldExtendedType:None** - Ekkert snið er notað.</span><span class="sxs-lookup"><span data-stu-id="f3210-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="f3210-154">**TSCustomFieldExtendedType::Gjaldmiðill** - Sníða gildið sem gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="f3210-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="f3210-155">Þegar snið gjaldmiðils er virkt er hægt að nota reitinnn **stringValue** til að flytja gjaldmiðilskóðann áfram sem á að birtast í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="f3210-156">Gildið er skrifvarið gildi.</span><span class="sxs-lookup"><span data-stu-id="f3210-156">The value is a read-only value.</span></span>

    <span data-ttu-id="f3210-157">Reiturinn **realValue** inniheldur peningaupphæðina sem á að vista í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="f3210-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="f3210-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="f3210-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="f3210-159">Hægt er að nota þennan eiginleika til að tilgreina hvar sérstillti reiturinn á að birtast í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="f3210-160">**TSCustomFieldSection::Haus** - Reiturinn birtist í hlutanum **Skoða frekari upplýsingar** í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="f3210-161">Þessir reitir eru alltaf skrifvarðir.</span><span class="sxs-lookup"><span data-stu-id="f3210-161">These fields are always read-only.</span></span>
- <span data-ttu-id="f3210-162">**TSCustomFieldSection::Lína** - Reiturinn birtist á eftir öllum tilbúnum reitarlínum í vinnukortafærslum.</span><span class="sxs-lookup"><span data-stu-id="f3210-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="f3210-163">Þessir reitir geta verið annaðhvort breytilegir eða skrifvarðir.</span><span class="sxs-lookup"><span data-stu-id="f3210-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="f3210-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="f3210-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="f3210-165">Þessi eiginleiki ber kennsl á reitinn þegar gildi sem forritið veitir eru vistuð aftur í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="f3210-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="f3210-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="f3210-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="f3210-167">Þessi eiginleiki ber kennsl á reitinn þegar gildi sem forritið veitir eru vistuð aftur í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="f3210-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="f3210-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="f3210-168">isEditable (NoYes)</span></span>

<span data-ttu-id="f3210-169">Stillið þennan eiginleika á **Já** til að tilgreina að reiturinn í hlutanum fyrir vinnukortafærslur eigi að vera breytanlegur fyrir notanda.</span><span class="sxs-lookup"><span data-stu-id="f3210-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="f3210-170">Stillið eiginleikann á **Nei** til að gera reitinn skrifvarinn.</span><span class="sxs-lookup"><span data-stu-id="f3210-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="f3210-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="f3210-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="f3210-172">Stillið þennan eiginleika á **Já** til að tilgreina að reiturinn í hlutanum fyrir vinnukortafærslur eigi að vera áskilinn.</span><span class="sxs-lookup"><span data-stu-id="f3210-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="f3210-173">merki (str)</span><span class="sxs-lookup"><span data-stu-id="f3210-173">label (str)</span></span>

<span data-ttu-id="f3210-174">Þessi eiginleiki tilgreinir merkið sem er sýnt við hliðina á reitnum í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="f3210-175">stringOptions (listi yfir strengi)</span><span class="sxs-lookup"><span data-stu-id="f3210-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="f3210-176">Þessi eiginleiki er eingöngu tiltækur þegar **fieldBaseType** er stillt á **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="f3210-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="f3210-177">Ef **stringOptions** er stillt eru strengjagildin sem hægt er að velja í gegnum valhnappa (valhringi) tilgreind af strengjunum í listanum.</span><span class="sxs-lookup"><span data-stu-id="f3210-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="f3210-178">Ef engar strengir eru gefnir upp er innsláttur á frjálsum texta í strengjareitnum leyfður (sjá hlutann „Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslur úr forritinu aftur í gagnagrunninn“ seinna í þessu efnisatriði til að sjá dæmi).</span><span class="sxs-lookup"><span data-stu-id="f3210-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="f3210-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="f3210-179">stringLength (int)</span></span>

<span data-ttu-id="f3210-180">Þessi eiginleiki tilgreinir hámarkslengd fyrir strengjareit.</span><span class="sxs-lookup"><span data-stu-id="f3210-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="f3210-181">Hann er eingöngu tiltækur þegar **fieldBaseType** er stillt á **Strengur**.</span><span class="sxs-lookup"><span data-stu-id="f3210-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="f3210-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="f3210-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="f3210-183">Þessi eiginleiki tilgreinir fjölda aukastafa sem eru sýndir í raunverulegum reit.</span><span class="sxs-lookup"><span data-stu-id="f3210-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="f3210-184">Hann er eingöngu tiltækur þegar **fieldBaseType** er stillt á **Raunverulegur**.</span><span class="sxs-lookup"><span data-stu-id="f3210-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="f3210-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="f3210-185">orderSequence (int)</span></span>

<span data-ttu-id="f3210-186">Þessi eiginleiki stýrir röðinni á sérstilltu reitunum þegar þeir birtast í forritinu þegar fleiri en einn sérstilltur reitur er tilgreindur.</span><span class="sxs-lookup"><span data-stu-id="f3210-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="f3210-187">Reitir með lægri tölu eru sýndir fyrst.</span><span class="sxs-lookup"><span data-stu-id="f3210-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="f3210-188">booleanValue (boole-gildi)</span><span class="sxs-lookup"><span data-stu-id="f3210-188">booleanValue (boolean)</span></span>

<span data-ttu-id="f3210-189">Fyrir reiti af gerðinni **Boole-gildi** færir þessi eiginleiki boole-gildi reitsins á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="f3210-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="f3210-190">guidValue (guid)</span></span>

<span data-ttu-id="f3210-191">Fyrir reiti af gerðinni **GUID** færir þessi eiginleiki gildi fyrir reit alþjóðlegs einkvæms kennimerkis (GUID) á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="f3210-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="f3210-192">int64Value (int64)</span></span>

<span data-ttu-id="f3210-193">Fyrir reiti af gerðinni **Int64** færir þessi eiginleiki int64-gildi reitsins á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="f3210-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="f3210-194">intValue (int)</span></span>

<span data-ttu-id="f3210-195">Fyrir reiti af gerðinni **Int** færir þessi eiginleiki int-gildi reitsins á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="f3210-196">realValue (raunverulegt)</span><span class="sxs-lookup"><span data-stu-id="f3210-196">realValue (real)</span></span>

<span data-ttu-id="f3210-197">Fyrir reiti af gerðinni **Raunverulegt** færir þessi eiginleiki raunverulegt gildi reitsins á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="f3210-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="f3210-198">stringValue (str)</span></span>

<span data-ttu-id="f3210-199">Fyrir reiti af gerðinni **Strengur** færir þessi eiginleiki strengjagildi reitsins á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="f3210-200">Hann er einnig notaður fyrir reiti af gerðinni **Raunverulegur** sem eru sniðnir sem gjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="f3210-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="f3210-201">Fyrir þessa reiti er eiginleikinn notaður til að flytja gjaldmiðilskóða áfram í forritið.</span><span class="sxs-lookup"><span data-stu-id="f3210-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="f3210-202">dateValue (dagsetning)</span><span class="sxs-lookup"><span data-stu-id="f3210-202">dateValue (date)</span></span>

<span data-ttu-id="f3210-203">Fyrir reiti af gerðinni **Dagsetning** færir þessi eiginleiki dagsetningargildi reitsins á milli þjónsins og forritsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="f3210-204">Sýnið og vistið sérstilltan reit í hlutanum fyrir vinnukortafærslu</span><span class="sxs-lookup"><span data-stu-id="f3210-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="f3210-205">Hér fyrir neðan er skjámynd úr farsímaforritinu af stofnun vinnukortafærslu.</span><span class="sxs-lookup"><span data-stu-id="f3210-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="f3210-206">Hún sýnir tilbúnu reitina og sérstilltan reit í hlutanum „Tímafærsla“ sem kallast „Prófunarstrengur“ með fasttextagildi sem „Annar valkostur“ nú þegar stilltan.</span><span class="sxs-lookup"><span data-stu-id="f3210-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Sérstilltur reitur prófunarstrengs í forritinu](media/timesheet-entry.jpg)



<span data-ttu-id="f3210-208">Hér að neðan er skjámynd úr farsímaforriti notandans sem velur einn af valmöguleikum fasttexta sem eru í boði fyrir sérstillta reitinn „Prófunarstrengur“.</span><span class="sxs-lookup"><span data-stu-id="f3210-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="f3210-209">Valkostirnir tveir eru „Fyrsti valkostur“ og „Annar valkostur“ sýndir sem valhringir.</span><span class="sxs-lookup"><span data-stu-id="f3210-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="f3210-210">Annar valkosturinn er valinn.</span><span class="sxs-lookup"><span data-stu-id="f3210-210">The second option is currently selected.</span></span>

![Valhnappar (valhringir) fyrir sérstilltan reit prófunarstrengs](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="f3210-212">Stækka TSTimesheetLine-töfluna svo hún sé með sérstilltan reit</span><span class="sxs-lookup"><span data-stu-id="f3210-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="f3210-213">Í dæmigerðum tilfellum er líklegt að gögnin fyrir sérsniðin reit í hlutanum fyrir vinnukortafærslu verði vistuð í TSTimesheetLine-töflunni.</span><span class="sxs-lookup"><span data-stu-id="f3210-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="f3210-214">Hinsvegar er hægt að nota aðrar töflur ef hægt er að sækja gögnin á grunni TSTimesheetTrans-færslu sem er gefin upp, eða ef hún er ekki með tiltekið færslusamhengi (t.d. ef reiturinn er stilltur sem skrifvarinn í færibreytum verksins).</span><span class="sxs-lookup"><span data-stu-id="f3210-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="f3210-215">Athugið að sérstilltu reitirnir eru ekki með nein öryggisafrit af færslum gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="f3210-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="f3210-216">Hægt er að mynda þá gagnvirkt á grunni X++ rökfræði.</span><span class="sxs-lookup"><span data-stu-id="f3210-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="f3210-217">Þessi nálgun getur reynst gagnleg í skrifvörðum aðstæðum (sjá hlutann „Nota boðleið í TSTimesheetDetails-klasanum, buildCustomFieldListForHeader-aðferðina til að fylla út í upplýsingar vinnukorts“ til að sjá dæmi um gagnvirka myndun á gildum sérstillts reits.)</span><span class="sxs-lookup"><span data-stu-id="f3210-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="f3210-218">Hér að neðan er skjámynd úr Visual Studio af hugbúnaðarhlutatrénu.</span><span class="sxs-lookup"><span data-stu-id="f3210-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="f3210-219">Hún sýnir viðbót af TSTimesheetLine-töflunni með TestLineString-töflunni bættri við sem sérstilltur reitur.</span><span class="sxs-lookup"><span data-stu-id="f3210-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Strengjalína](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="f3210-221">Notið boðleið í buildCustomFieldList-aðferðinni fyrir TSTimesheetSettings-klasann til að sýna reit í hluta vinnukortafærslunnar</span><span class="sxs-lookup"><span data-stu-id="f3210-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="f3210-222">Þessi kóði stýrir skjástillingum fyrir reitinn í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="f3210-223">Hann stýrir t.d. gerð reitsins, merkinu, hvort reiturinn sé áskilinn, og í hvaða hluta reiturinn birtist.</span><span class="sxs-lookup"><span data-stu-id="f3210-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="f3210-224">Eftirfarandi dæmi sýnir strengjareit í tímafærslum.</span><span class="sxs-lookup"><span data-stu-id="f3210-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="f3210-225">Þessi reitur hefur tvo valmöguleika, **Fyrsti valkostur** og **Annar valkostur**, sem eru í boði í gegnum valhnappa (valhringi).</span><span class="sxs-lookup"><span data-stu-id="f3210-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="f3210-226">Reiturinn í forritinu tengist reitnum **TestLineString** sem er bætt við TSTimesheetLine-töfluna.</span><span class="sxs-lookup"><span data-stu-id="f3210-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="f3210-227">Athugið notkun á aðferðinni **TSTimesheetCustomField::newFromMetadata()** til að einfalda frumstillingu á eiginleikum sérstillts reits: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="f3210-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="f3210-228">Einnig er hægt að stilla þessar færibreytur handvirkt eins og hentar.</span><span class="sxs-lookup"><span data-stu-id="f3210-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="f3210-229">Nota boðleið í buildCustomFieldListForEntry-aðferðinni fyrir TSTimesheetEntry-klasann til að færa gildi inn í tímafærslu</span><span class="sxs-lookup"><span data-stu-id="f3210-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="f3210-230">Aðferðin **buildCustomFieldListForEntry** er notuð til að færa gildi í vistuðu vinnukortslínunum inn í farsímaforritið.</span><span class="sxs-lookup"><span data-stu-id="f3210-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="f3210-231">Hún tekur TSTimesheetTrans-færslu sem færibreytu.</span><span class="sxs-lookup"><span data-stu-id="f3210-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="f3210-232">Reiti úr þeirri færslu er hægt að nota til að setja inn gildið fyrir sérstilltan reit í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="f3210-233">Nota boðleið í TSTimesheetEntryService-klasanum til að vista vinnukortafærslur úr forritinu aftur í gagnagrunninn</span><span class="sxs-lookup"><span data-stu-id="f3210-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="f3210-234">Til að vista sérstilltan reit aftur í gagnagrunninn við dæmigerða notkun, þarf að víkka út margar aðferðir:</span><span class="sxs-lookup"><span data-stu-id="f3210-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="f3210-235">Aðferðin **timesheetLineNeedsUpdating** er notuð til að ákvarða hvort notandinn hafi breytt línufærslunni í forritinu og verði að vista hana í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="f3210-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="f3210-236">Ef afköst eru ekki áhyggjuefni er hægt að einfalda þessa aðferð svo hún skili alltaf **satt**.</span><span class="sxs-lookup"><span data-stu-id="f3210-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="f3210-237">Aðferðirnar **populateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** er hægt að stækka svo þær færi gildi inn í færslu gagnagrunns TSTimesheetLine úr færslu TSTimesheetEntry-gagnasamnings sem gefin er upp.</span><span class="sxs-lookup"><span data-stu-id="f3210-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="f3210-238">Takið eftir í eftirfarandi dæmi hvernig vörpun milli gagnagrunnsreits og færslureits er gerð handvirkt með X++ kóða.</span><span class="sxs-lookup"><span data-stu-id="f3210-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="f3210-239">Einnig er hægt að stækka aðferðina **populateTimesheetWeekFromEntry** ef sérstilltur reitur sem er varpað í hlutinn **TSTimesheetEntry** verður að skrifa til baka til gagnagrunnstöflunnar TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="f3210-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="f3210-240">Eftirfarandi dæmi vistar gildið **firstOption** eða **secondOption** sem notandinn velur í gagnagrunninn sem óunnið strengjagildi.</span><span class="sxs-lookup"><span data-stu-id="f3210-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="f3210-241">Ef gagnagrunnsreiturinn er reitur af gerðinni **Fasttexti** er hægt að varpa þessum gildum handvirkt í fasttextagildi og síðan vista þau í fasttextareit í gagnagrunnstöflunni.</span><span class="sxs-lookup"><span data-stu-id="f3210-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="f3210-242">Sýna sérstilltan reit í hluta vinnukortahauss</span><span class="sxs-lookup"><span data-stu-id="f3210-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="f3210-243">Hér fyrir neðan er skjámynd úr farsímaforritinu af notanda að skoða vinnukort.</span><span class="sxs-lookup"><span data-stu-id="f3210-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="f3210-244">Hnappurinn „Frekari upplýsingar“ hefur verið valinn efst í hægra horninu til að sýna valkostinn „Skoða frekari upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="f3210-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Skipun fyrir að skoða frekari upplýsingar](media/show-more.png)

<span data-ttu-id="f3210-246">Hér fyrir neðan er skjámynd úr farsímaforritinu sem sýnir „Meira“ hlutann í vinnukorti.</span><span class="sxs-lookup"><span data-stu-id="f3210-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="f3210-247">Sérstilltur reitur sem kallast „Nýtingarhlutfall á þessu vinnukorti (reiknaður sérstilltur reitur)“ hefur verið bætt við í haus vinnukortsins.</span><span class="sxs-lookup"><span data-stu-id="f3210-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="f3210-248">Skrifvarið gildi upp á „0,667“ er stillt fyrir sérstillta reitinn.</span><span class="sxs-lookup"><span data-stu-id="f3210-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Meira](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="f3210-250">Stækka TSTimesheetTable-töfluna svo hún sé með sérstilltan reit</span><span class="sxs-lookup"><span data-stu-id="f3210-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="f3210-251">Í dæmigerðum tilfellum er líklegt að gögnin fyrir sérsniðinn reit í hausnum verði sótt úr TSTimesheetHeader-töflunni.</span><span class="sxs-lookup"><span data-stu-id="f3210-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="f3210-252">Hinsvegar er hægt að nota aðrar töflur ef hægt er að sækja gögnin á grunni TSTimesheetTable-færslu sem er gefin upp, eða ef hún er ekki með tiltekið færslusamhengi (t.d. ef reiturinn er stilltur sem skrifvarinn í færibreytum verksins).</span><span class="sxs-lookup"><span data-stu-id="f3210-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="f3210-253">Athugið að sérstilltu reitirnir eru ekki með nein öryggisafrit af færslum gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="f3210-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="f3210-254">Hægt er að mynda þá gagnvirkt á grunni X++ rökfræði.</span><span class="sxs-lookup"><span data-stu-id="f3210-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="f3210-255">Dæmið sem fylgir sýnir þessa nálgun.</span><span class="sxs-lookup"><span data-stu-id="f3210-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="f3210-256">Reitir í hausnum eru alltaf skrifvarðir í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="f3210-257">Nota boðleið í buildCustomFieldList-aðferðinni fyrir TSTimesheetSettings-klasann til að sýna reit í hausnum</span><span class="sxs-lookup"><span data-stu-id="f3210-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="f3210-258">Þessi kóði stýrir skjástillingum fyrir reitinn í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="f3210-259">Hann stýrir t.d. gerð reitsins, merkinu, hvort reiturinn sé áskilinn, og í hvaða hluta reiturinn birtist.</span><span class="sxs-lookup"><span data-stu-id="f3210-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="f3210-260">Eftirfarandi dæmi sýnir reiknað gildi í hausnum í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="f3210-261">Nota boðleið fyrir aðferðina buildCustomFieldListForHeader í TSTimesheetDetails-klasanum til að fylla út upplýsingar um vinnukort</span><span class="sxs-lookup"><span data-stu-id="f3210-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="f3210-262">Aðferðin **buildCustomFieldListForHeader** er notuð til að fylla út upplýsingar vinnukortahauss í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="f3210-263">Hún notar TSTimesheetTable-færslu sem færibreytu.</span><span class="sxs-lookup"><span data-stu-id="f3210-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="f3210-264">Reiti úr þeirri færslu er hægt að nota til að setja inn gildið fyrir sérstilltan reit í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="f3210-265">Eftirfarandi dæmi les ekki nein gildi úr gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="f3210-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="f3210-266">Þess í stað notar það X++ reikniaðgerðir til að búa til reiknað gildi sem síðan er sýnt í forritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="f3210-267">Aðrir möguleikar á stillingum/stækkunarhæfni</span><span class="sxs-lookup"><span data-stu-id="f3210-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="f3210-268">Bæta við frekari villuleit fyrir forritið</span><span class="sxs-lookup"><span data-stu-id="f3210-268">Adding additional validation for the app</span></span>

<span data-ttu-id="f3210-269">Núverandi reikniaðgerðir fyrir virkni vinnukorts á gagnagrunnsstigi virka enn eins og venjulega.</span><span class="sxs-lookup"><span data-stu-id="f3210-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="f3210-270">Til að trufla málalyktir á aðgerðum vistunar og innsendingar og sýna tiltekin villuboð er hægt að bæta **sýna villu („skilaboð til notanda“)** við kóðann í gegnum viðbót boðleiðar.</span><span class="sxs-lookup"><span data-stu-id="f3210-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="f3210-271">Hér eru þrjú dæmi um gagnlegar aðferðir fyrir stækkanleika:</span><span class="sxs-lookup"><span data-stu-id="f3210-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="f3210-272">Ef **validateWrite** í TSTimesheetLine-töflunni skilar **rangt** við vistun á aðgerð fyrir vinnukortslínu birtast villuboð í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="f3210-273">Ef **validateSubmit** í TSTimesheetTable-töflunni skilar **rangt** við innsendingu á vinnukorti í forritinu fær notandinn villuboð.</span><span class="sxs-lookup"><span data-stu-id="f3210-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="f3210-274">Reikniaðgerð sem fyllir út reiti (t.d. **Línueiginleiki**) þegar aðferðin **setja inn** stendur yfir í TSTimesheetLine-töflunni mun halda áfram að keyra.</span><span class="sxs-lookup"><span data-stu-id="f3210-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="f3210-275">Fela og merkja tilbúna reiti sem skrifvarða í gegnum grunnstillingu</span><span class="sxs-lookup"><span data-stu-id="f3210-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="f3210-276">Úr færibreytum verka er hægt að gera tilbúna reiti skrifvarða eða fela þá í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="f3210-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="f3210-277">Stillið valmöguleikana í hlutanum **Vinnukort farsíma** í flipanum **Vinnukort** á síðunni **Verkefnastjórnun og bókhaldsfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="f3210-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Færibreytur verka](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="f3210-279">Breyting á verkþáttum sem hægt er að velja í gegnum viðbætur</span><span class="sxs-lookup"><span data-stu-id="f3210-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="f3210-280">Verkþættirnir sem hægt er að velja fyrir verk eru fylltir út í gegnum aðferðirnar **getActivitiesForProject()** og **getActivityQuery()** í klasanum **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="f3210-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="f3210-281">Hægt er að nota boðleið til að breyta þessari hegðun til að passa við rekstraraðstæður þínar fyrir verkþættina sem hægt er að velja fyrir tiltekið verk.</span><span class="sxs-lookup"><span data-stu-id="f3210-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="f3210-282">Færa sjálfgefna verktegund inn í vinnukortafærslur</span><span class="sxs-lookup"><span data-stu-id="f3210-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="f3210-283">Færsla á sjálfgefinni verktegund inn í vinnukortafærslur gerist á þremur stigum.</span><span class="sxs-lookup"><span data-stu-id="f3210-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="f3210-284">Hægt er að nota boðleið til að víkka út hegðunina á hvaða stigi sem er eða þeim öllum til að ná fram æskilegri hegðun.</span><span class="sxs-lookup"><span data-stu-id="f3210-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="f3210-285">Eftirfarandi stigveldi er notað:</span><span class="sxs-lookup"><span data-stu-id="f3210-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="f3210-286">Forritið reynir að setja inn sjálfgefna tegund úr tilföngum verks.</span><span class="sxs-lookup"><span data-stu-id="f3210-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="f3210-287">Þessi sjálfgefna tegund er stillt í aðferðunum **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** í klasanum **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="f3210-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="f3210-288">Ef ekki er boðið upp á sjálfgefna tegund á stigi verktilfanga reynir forritið að sækja það úr verkþættinum.</span><span class="sxs-lookup"><span data-stu-id="f3210-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="f3210-289">Þessi sjálfgefna tegund er stillt í aðferðinni **getActivitiesForProject** í klasanum **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="f3210-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="f3210-290">Ef ekki er boðið upp á sjálfgefna tegund á stigi verkþáttar er náð í sjálfgefnu tegundina úr færibreytum verks.</span><span class="sxs-lookup"><span data-stu-id="f3210-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="f3210-291">Þessi sjálfgefna tegund er stillt í aðferðinni **fáProjectDetailsbyRule** í klasanum **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="f3210-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
