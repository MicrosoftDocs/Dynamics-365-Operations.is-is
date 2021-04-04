---
title: Fyrirtækishugtak í Dataverse
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 189d1b8a68f8457d32d656fefeb6cc2a332a3b22
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560250"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="b9b8b-103">Fyrirtækishugtak í Dataverse</span><span class="sxs-lookup"><span data-stu-id="b9b8b-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="b9b8b-104">Í Finance and Operations er hugtakið a *fyrirtæki* bæði lögleg smíð og viðskiptasmíð.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="b9b8b-105">Það er einnig öryggis- og sýnileikamörk fyrir gögn.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="b9b8b-106">Notendur vinna alltaf í samhengi við eitt fyrirtæki og flest gögnin eru röndótt af fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="b9b8b-107">Dataverse er ekki með sambærilegt hugtak.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="b9b8b-108">Næsta hugtakið er *rekstrareining*, sem er fyrst og fremst öryggis- og sýnileikamörk fyrir notendagögn.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="b9b8b-109">Þetta hugtak hefur ekki sömu lagalegu eða viðskiptalegu afleiðingar og hugtakið fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="b9b8b-110">Vegna þess að rekstrareining og fyrirtæki eru ekki sambærileg hugtök er ekki mögulegt að þvinga kortlagningu á milli þeirra (1: 1) í þeim tilgangi að samþætta Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="b9b8b-111">Hins vegar, vegna þess að notendur verða að sjá sömu línur í forritinu og Dataverse, hefur Microsoft kynnt til leiks nýja töflu í Dataverse sem nefnist cdm\_Fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="b9b8b-112">Þessi tafla jafngildir fyrirtækjatöflunni í forritinu.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="b9b8b-113">Til að tryggja að sömu línur sjáist í forriti og nýju Dataverse er mælt með eftirfarandi uppsetningu gagna í Dataverse:</span><span class="sxs-lookup"><span data-stu-id="b9b8b-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="b9b8b-114">Fyrir hverja Finance and Operations -fyrirtækislínu sem er virk fyrir tvöfalda skráningu er tengd cdm\_fyrirtækjalína búin til.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="b9b8b-115">Þegar cdm\_fyrirtækislína er búin til og virkjuð fyrir tvöfalda skráningu er sjálfgefin viðskiptaeining stofnuð með sama heiti.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="b9b8b-116">Þó að sjálfgefið teymi sé sjálfkrafa búið til fyrir þá rekstrareiningu er rekstrareiningin ekki notuð.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="b9b8b-117">Sérstakt eigendateymi er búið til sem hefur sama nafn.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="b9b8b-118">Það er líka tengt rekstrareiningunni.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="b9b8b-119">Sjálfgefið er að eigandi allra lína sem eru búnar til og tvöfalt skráðar á Dataverse sé stilltur á hópinn „DW-eigandi“ sem er tengdur við tengda viðskiptaeiningu.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="b9b8b-120">Eftirfarandi skýringarmynd sýnir dæmi um þessa gagnauppsetningu í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Uppsetning gagna í Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="b9b8b-122">Í þessari grunnstillingu eru færslur sem tengjast USMF fyrirtækinu í eigu teymis sem tengist USMF rekstrareiningunni í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="b9b8b-123">Því geta notendur sem hafa aðgang að viðskiptaeiningunni í gegnum öryggishlutverk sem er stillt á sýnileika viðskiptaeiningarstigs nú séð línurnar.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="b9b8b-124">Eftirfarandi dæmi sýnir hvernig hægt er að nota teymi til að veita réttan aðgang að þessum línum.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="b9b8b-125">Hlutverkinu „Sölustjóri“ er úthlutað til meðlima „USMF sölu“ teymisins.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="b9b8b-126">Notendur sem eru með hlutverkið „sölustjóri“ hafa aðgang að öllum lyklalínum sem eru hluti af sömu viðskiptaeiningu og notendurnir eru meðlimir í.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="b9b8b-127">"USMF Sales" teymið er tengt við USMF viðskiptadeildina sem áður var nefnd.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="b9b8b-128">Þess vegna geta meðlimir í "USMF sölu" teyminu séð hvaða reikning sem er í eigu "USMF DW" notandans, sem hefði komið frá USMF fyrirtækjatöflunni í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Hvernig hægt er að nota teymi](media/dual-write-company-2.png)

<span data-ttu-id="b9b8b-130">Eins og myndin hér að ofan sýnir er þessi 1:1 kortlagning milli rekstrareiningar, fyrirtækis og teymis aðeins upphafspunktur.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="b9b8b-131">Í þessu dæmi er ný „eining“ í Evrópu búin til handvirkt í Dataverse sem yfireining bæði fyrir DEMF og ESMF.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="b9b8b-132">Þessi nýja rótarviðskiptaeining er ekki skyld tvöföldum skrifum.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="b9b8b-133">Hins vegar er hægt að nota hana til að veita meðlimum „EUR Sales“ teymisins aðgang að reikningsgögnum bæði í DEMF og ESMF með því að stilla sýnileika gagna á **Yfir-/undir-BU** í tilheyrandi öryggishlutverki.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="b9b8b-134">Lokaumfjöllunarefnið er hvernig tvöföld skráning ákvarðar hvaða eigendahóp hún á að úthluta línum á.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="b9b8b-135">Hegðuninni er stjórnað af töflunni **Sjálfgefið eigendateymi** í cdm\_Fyrirtæki línunni.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="b9b8b-136">Þegar cdm\_fyrirtækjalína er virkjuð fyrir tvískrif býr viðbót sjálfkrafa til tengda viðskiptaeiningu og eigendateymi (ef það er ekki þegar til) og stillum dálkinn **Sjálfgefið eigendateymi**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="b9b8b-137">Stjórnandi getur breytt þessum dálki í annað gildi.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="b9b8b-138">Stjórnandi getur þó ekki hreinsað dálkinn svo framarlega sem taflan er virk fyrir tvöfalda skráningu.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="b9b8b-139">![Sjálfgefinn dálkur eigendahóps](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="b9b8b-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="b9b8b-140">Fyrirtækjaskrár og ræsibönd</span><span class="sxs-lookup"><span data-stu-id="b9b8b-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="b9b8b-141">Dataverse-samþætting færir fyrirtækjajöfnun með því að nota auðkenni fyrirtækisins til að randa gögn.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="b9b8b-142">Eins og eftirfarandi mynd sýnir eru allar fyrirtækistöflur útvíkkaðar þannig til að þær séu með margt-í-eitt (N:1) vensl við töfluna cdm\_Fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="b9b8b-143">![N:1 vensl milli fyrirtækjasértakrar töflunnar og töflunnar cdm_Company](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="b9b8b-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="b9b8b-144">Gildi lína verður skrifvarið eftir að fyrirtæki hefur verið bætt við og það vistað.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="b9b8b-145">Þess vegna ættu notendur að gæta þess að þeir velja rétt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="b9b8b-146">Aðeins línur sem eru með fyrirtækisgögn eru hæfar fyrir tvöfalda skráningu milli forrits og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="b9b8b-147">Fyrir núverandi gögn Dataverse mun stjórnandaleidd ræsibandareynsla brátt verða tiltæk.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="b9b8b-148">Heiti fyrirtækis sem er sjálfkrafa fyllt út í forritum fyrir viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="b9b8b-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="b9b8b-149">Ýmsar leiðir eru til að fylla út sjálfkrafa Fyrirtækisheitið í forritum fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="b9b8b-150">Ef notandi er kerfisstjóri er hægt að stilla sjálfgefið fyrirtæki með því að fara í **Ítarlegar stillingar > Kerfi > Öryggi > notendur**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="b9b8b-151">Opnaðu skjámyndina **Notandi** og í **Upplýsingar um stofnun/fyrirtæki** hlutanum skaltu stilla gildið **Fyrirtækið á sjálfgefin á skjámyndum**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Velja sjálfgefið fyrirtæki í upplýsingahluta fyrirtækis.":::

+ <span data-ttu-id="b9b8b-153">Ef þú hefur **skrifheimild** fyrir **SystemUser** töfluna fyrir stig **Viðskiptaeiningar**, getur þú breytt sjálfgefna fyrirtækinu í hvaða skjámynd sem er með því að velja fyrirtæki úr fellivalmynd **Fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Breyta heiti fyrirtækisins á nýjum lykli.":::

+ <span data-ttu-id="b9b8b-155">Ef þú hefur **Skrifheimild** fyrir gögn í fleiri en einu fyrirtæki, geturðu breytt sjálfgefna fyrirtækinu með því að velja línu sem tilheyrir öðru fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Að velja línu breytir sjálfgefna fyrirtækinu.":::

+ <span data-ttu-id="b9b8b-157">Ef þú sérð um kerfisstillingar eða ert kerfisstjóri og þú vilt fylla út fyrirtækisgögn sjálfkrafa í sérsniðinni skjámynd, geturðu valið [skjámyndatilvik](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="b9b8b-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="b9b8b-158">Bættu við JavaScript tilvísun á **msdyn_/DefaultCompany.js** og nota eftirfarandi tilvik.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="b9b8b-159">Hægt er að nota hvaða tilbúnu skjámynd sem er, t.d. skjámyndina **Lykill**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="b9b8b-160">**OnLoad** tilvik fyrir skjámyndina: Stillið dálkinn **defaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="b9b8b-161">**OnChange** tilvik fyrir dálkinn **Fyrirtæki**: Stillið dálkinn **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="b9b8b-162">Nota síun sem byggir á samhengi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="b9b8b-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="b9b8b-163">Til að nota síun sem byggir á samhengi fyrirtækisins í sérsniðnum skjámyndum eða í sérsniðnum uppflettidálkum sem bætt hefur verið við staðlaðar skjámyndir, skal opna skjámyndina og nota hlutann **Síun á tengdum færslum** til að nota fyrirtækissíuna.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="b9b8b-164">Þetta verður að stilla fyrir hvern uppflettidálk sem krefst síunar sem byggir á undirliggjandi fyrirtæki fyrir uppgefna röð.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="b9b8b-165">Stillingin er sýnd fyrir **Lykil** á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="b9b8b-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Nota samhengi fyrirtækis":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]