---
title: Vinna með dagsetningu og tíma í Microsoft Dynamics 365 for Talent
description: Fáðu skilning á við hverju má búast við notkun á dagsetningar- og tímareitum í Microsoft Dynamics 365 for Talent. Fáðu betri yfirsýn yfir við hverju má búast við samskipti við dagsetningar- og tímagögn í skjámynd í Dynamics 365 for Talent, ytri uppruna, eða Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4c652992272ed1a5aecbb4c78f0d11f077149d1
ms.sourcegitcommit: 46bded82aa072adfedcf443629c2adc69f512c09
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/26/2019
ms.locfileid: "1791214"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="7ccdc-104">Dagsetninga- og tímareitir í Talent</span><span class="sxs-lookup"><span data-stu-id="7ccdc-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7ccdc-105">Reitirnir **Dagsetning og tími** eru grundvallarhugtak í Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-105">**Date and Time** fields are a fundamental concept in Dynamics 365 for Talent.</span></span> <span data-ttu-id="7ccdc-106">Mikilvægt er að öðlast skilning hvernig á að vinna með gögn í **Dagsetningu og tíma** í skjámynd í Dynamics 365, Common Data Serviceog ytri uppruna.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="7ccdc-107">Að skilja muninn á gagnagerðum dagsetningar- og tímareita</span><span class="sxs-lookup"><span data-stu-id="7ccdc-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="7ccdc-108">Reitirnir **Dagsetning og tími** innihalda upplýsingar um tímabelti en reitirnir **Dagsetning** gera það ekki.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="7ccdc-109">Reitirnir **Dagsetning** sýna sömu upplýsingar á hvaða stað sem er.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="7ccdc-110">Þegar þú slærð inn dagsetningu í reitinn **Dagsetning** skrifar Talent sömu dagsetninguna í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="7ccdc-111">Þegar gögn eru birt í reitnum **Dagsetning og tími** aðlagar Talent dagsetningu og tíma út frá tímabelti notandans sem er stillt í glugganum **Notendastillingar** (**Sameiginlegt > Uppsetning > Notendastillingar**).</span><span class="sxs-lookup"><span data-stu-id="7ccdc-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="7ccdc-112">Upplýsingar um dagsetningu og tíma sem þú slærð inn í reitinn eru ef til vill ekki þær sömu og upplýsingarnar sem skrifaðar eru í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="7ccdc-113">[![Skjámyndin Notendastillingar](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="7ccdc-114">Að öðlast skilning á dagsetninga- og tímareitum</span><span class="sxs-lookup"><span data-stu-id="7ccdc-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="7ccdc-115">Þegar gögn eru færð inn í reitinn **Dagsetning og tími** eru gögnin sem birtast á skjánum ekki þau sömu og gögnin sem eru geymd í gagnagrunninum ef tímabelti notandans er ekki stillt á samhæfðan alþjóðlegan tíma (UTC).</span><span class="sxs-lookup"><span data-stu-id="7ccdc-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="7ccdc-116">Gögn í reitunum **Dagsetning og tími** eru alltaf geymdir sem UTC.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="7ccdc-117">[![Skjámyndin Starfskraftur](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="7ccdc-118">Fáðu öðlast skilning á dagsetninga- og tímareitum í gagnagrunninum</span><span class="sxs-lookup"><span data-stu-id="7ccdc-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="7ccdc-119">Þegar Talent skrifar gildi **Dagsetningar og tíma** í gagnagrunninum geymir það gögnin í UTC.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="7ccdc-120">Þetta gerir notendum kleift að sjá öll gögn í **Dagsetningu og tíma** miðað við tímabeltið sem er skilgreint í notendastillingum þeirra.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="7ccdc-121">Í dæminu hér að ofan er upphafstíminn tímapunktur, ekki ákveðin dagsetning.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="7ccdc-122">Með því að breyta tímabelti notandans sem er skráður inn frá GMT +12: 00 í GMT UTC sýnir sama skráin og var stofnuð 04/30/2019 12:00:00 í staðinn 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="7ccdc-123">Í dæminu hér að neðan verður starf starfsmanns 000724 virkt á umleið, óháð tímabelti.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="7ccdc-124">Starfsmaðurinn verður virkur þann 04/30/2019 á GMT-tímabeltinu, sem er það sama og 05/01/2019 á GMT+12:00-tímabeltinu.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="7ccdc-125">Hvort tveggja vísar til sama tímapunkts og ekki til ákveðinnar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="7ccdc-126">[![Skjámyndin Starfskraftur](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="7ccdc-127">Dagsetninga- og tímagögn í gagnastjórnunarramma, Excel, Common Data Service og Power BI</span><span class="sxs-lookup"><span data-stu-id="7ccdc-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="7ccdc-128">Gagnastjórnunarrammi, Excel-innbót, Common Data Service og Power BI skýrslugerð eru öll hönnuð til að hafa samskipti við gögn beint á gagnagrunnsstigi.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="7ccdc-129">Þar sem það er enginn viðskiptavinur til að aðlagast gögnunum **Dagsetning og tími** á tímabelti notandans eru öll gildi **Dagsetningar og tíma** í UTC, sem getur leitt til rangra forsendna þegar gögn eru slegin inn eða skoðuð.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="7ccdc-130">Gagnagrunnurinn gerir ráð fyrir að gögn í **Dagsetningum og tíma** sem eru lögð fram í gegnum DMF, Excel eða Common Data Service séu í UTC.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="7ccdc-131">Þetta getur valdið nokkrum ruglingi þegar innsent gildi í **Dagsetningu og tíma** birtist ekki eins og búist var við vegna þess að notandi sem skoðar gögnin er ekki með tímabelti notanda stillt á UTC.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="7ccdc-132">Það sama getur gerst á öfugan hátt þegar gögn eru flutt út.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="7ccdc-133">Gögnin **Dagsetning og tími** í útfluttu DMF-einingunni geta verið önnur en það sem birtist í Dynamics biðlaranum.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="7ccdc-134">Þegar þú notar utanaðkomandi heimildir eins og DMF til að skoða eða skrifa gögn er mikilvægt að hafa í huga að gildin í **Dagsetningu og tíma** teljast sjálfkrafa vera í UTC óháð tímabelti í tölvu notandans eða núverandi tímabeltisstillingum hans.</span><span class="sxs-lookup"><span data-stu-id="7ccdc-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="7ccdc-135">Dæmi um sömu skrá sem birtist á mismunandi afurðasvæðum</span><span class="sxs-lookup"><span data-stu-id="7ccdc-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="7ccdc-136">**Talent með tímabelti notanda stillt á UTC**</span><span class="sxs-lookup"><span data-stu-id="7ccdc-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="7ccdc-137">[![Skjámyndin Starfskraftur](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="7ccdc-138">**Talent með tímabelti notanda stillt á GMT + 12:00**</span><span class="sxs-lookup"><span data-stu-id="7ccdc-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="7ccdc-139">[![Skjámyndin Starfskraftur](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="7ccdc-140">**Excel í gegnum OData**</span><span class="sxs-lookup"><span data-stu-id="7ccdc-140">**Excel Via OData**</span></span>

<span data-ttu-id="7ccdc-141">[![Excel í gegnum OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="7ccdc-142">**DMF-sviðsetning**</span><span class="sxs-lookup"><span data-stu-id="7ccdc-142">**DMF Staging**</span></span>

<span data-ttu-id="7ccdc-143">[![DMF-sviðsetning](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="7ccdc-144">**Útflutningur á DMF**</span><span class="sxs-lookup"><span data-stu-id="7ccdc-144">**DMF Export**</span></span>

<span data-ttu-id="7ccdc-145">[![DMF-sviðsetning](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="7ccdc-146">**Excel í gegnum Common Data Service**</span><span class="sxs-lookup"><span data-stu-id="7ccdc-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="7ccdc-147">[![Excel í gegnum Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="7ccdc-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="7ccdc-148">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="7ccdc-148">See also</span></span>

[<span data-ttu-id="7ccdc-149">Dagsetningar- og tímagögn</span><span class="sxs-lookup"><span data-stu-id="7ccdc-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="7ccdc-150">Valin tímabelti notanda</span><span class="sxs-lookup"><span data-stu-id="7ccdc-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
