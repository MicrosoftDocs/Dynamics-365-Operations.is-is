---
title: Skilja svæði fyrir dagsetningu og tíma
description: Fáðu skilning á við hverju má búast við notkun á dagsetningar- og tímareitum í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7e5726f7e4beea1584b9a8e142212531ba1db56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051738"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="ecffb-103">Skilja svæði fyrir dagsetningu og tíma</span><span class="sxs-lookup"><span data-stu-id="ecffb-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ecffb-104">Reitirnir **Dagsetning og tími** eru grundvallarhugtak í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ecffb-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ecffb-105">Mikilvægt er að skilja hvernig vinna á með gögn **Dagsetningu og tíma** í skjámyndum, Dataverse, og ytri upprunum.</span><span class="sxs-lookup"><span data-stu-id="ecffb-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="ecffb-106">Að skilja muninn á gagnagerðum dagsetningar- og tímareita</span><span class="sxs-lookup"><span data-stu-id="ecffb-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="ecffb-107">Reitirnir **Dagsetning og tími** innihalda upplýsingar um tímabelti en reitirnir **Dagsetning** gera það ekki.</span><span class="sxs-lookup"><span data-stu-id="ecffb-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="ecffb-108">Reitirnir **Dagsetning** sýna sömu upplýsingar á hvaða stað sem er.</span><span class="sxs-lookup"><span data-stu-id="ecffb-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="ecffb-109">Þegar þú slærð inn dagsetningu í reitinn **Dagsetning** skrifar Human Resources sömu dagsetninguna í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="ecffb-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="ecffb-110">Þegar gögn eru birt í reitnum **Dagsetning og tími** aðlagar Human Resources dagsetningu og tíma út frá tímabelti notandans sem er stillt í glugganum **Notendastillingar** (**Sameiginlegt > Uppsetning > Notendastillingar**).</span><span class="sxs-lookup"><span data-stu-id="ecffb-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="ecffb-111">Upplýsingar um dagsetningu og tíma sem þú slærð inn í reitinn eru ef til vill ekki þær sömu og upplýsingarnar sem skrifaðar eru í gagnagrunninn.</span><span class="sxs-lookup"><span data-stu-id="ecffb-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="ecffb-112">[![Skjámyndin Notendastillingar](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="ecffb-113">Að öðlast skilning á dagsetninga- og tímareitum</span><span class="sxs-lookup"><span data-stu-id="ecffb-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="ecffb-114">Gögn **Dagsetningar og tíma** sem birtast á skjánum eru ekki þau sömu og gögnin sem eru geymd í gagnagrunninum ef tímabelti notanda er ekki stillt á samræmdan alþjóðlegan tíma (UTC).</span><span class="sxs-lookup"><span data-stu-id="ecffb-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="ecffb-115">Gögn í reitunum **Dagsetning og tími** eru alltaf geymdir sem UTC.</span><span class="sxs-lookup"><span data-stu-id="ecffb-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="ecffb-116">[![UTC í skjámynd starfsmanns](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="ecffb-117">Fáðu öðlast skilning á dagsetninga- og tímareitum í gagnagrunninum</span><span class="sxs-lookup"><span data-stu-id="ecffb-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="ecffb-118">Þegar Human Resources skrifar gildi fyrir **Dagsetningu og tíma** í gagnagrunninn, eru gögnin geymd á UTC.</span><span class="sxs-lookup"><span data-stu-id="ecffb-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="ecffb-119">Þetta gerir notendum kleift að sjá öll gögn í **Dagsetningu og tíma** miðað við tímabeltið sem er skilgreint í notendastillingum þeirra.</span><span class="sxs-lookup"><span data-stu-id="ecffb-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="ecffb-120">Í dæminu hér að ofan er upphafstíminn tímapunktur, ekki ákveðin dagsetning.</span><span class="sxs-lookup"><span data-stu-id="ecffb-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="ecffb-121">Með því að breyta tímabelti innskráða notanda úr GMT +12:00 í GMT UTC, sýnir sama færslan 04/30/2019 12:00:00 í stað 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="ecffb-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="ecffb-122">Í dæminu hér að neðan verður starf starfsmanns 000724 virkt á umleið, óháð tímabelti.</span><span class="sxs-lookup"><span data-stu-id="ecffb-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="ecffb-123">Starfsmaðurinn verður virkur þann 04/30/2019 á GMT-tímabeltinu, sem er það sama og 05/01/2019 á GMT+12:00-tímabeltinu.</span><span class="sxs-lookup"><span data-stu-id="ecffb-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="ecffb-124">Hvort tveggja vísar til sama tímapunkts og ekki til ákveðinnar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="ecffb-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="ecffb-125">[![GMT í skjámynd starfsmanns](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="ecffb-126">Dagsetninga- og tímagögn í gagnastjórnunarramma, Excel, Dataverse og Power BI</span><span class="sxs-lookup"><span data-stu-id="ecffb-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="ecffb-127">Gagnastjórnunarrammi, Excel-innbót, Dataverse og Power BI skýrslugerð eru öll hönnuð til að hafa samskipti við gögn beint á gagnagrunnsstigi.</span><span class="sxs-lookup"><span data-stu-id="ecffb-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="ecffb-128">Þar sem enginn biðlari er til staðar til að stilla gögnin fyrir **Dagsetningu og tíma** á tímabelti notandans, eru öll gildi **Dagsetningar og tíma** á UTC, sem getur valdið misskilningi þegar gögn eru slegin inn eða skoðuð.</span><span class="sxs-lookup"><span data-stu-id="ecffb-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="ecffb-129">Gögn **Dagsetningar og tíma** sem send eru inn í gegnum DMF, Excel eða Dataverse eru álitin vera á UTC af gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="ecffb-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="ecffb-130">Þetta getur valdið nokkrum ruglingi þegar innsent gildi í **Dagsetningu og tíma** birtist ekki eins og búist var við vegna þess að notandi sem skoðar gögnin er ekki með tímabelti notanda stillt á UTC.</span><span class="sxs-lookup"><span data-stu-id="ecffb-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="ecffb-131">Það sama getur gerst á öfugan hátt þegar gögn eru flutt út.</span><span class="sxs-lookup"><span data-stu-id="ecffb-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="ecffb-132">Gögnin **Dagsetning og tími** í útfluttri DMF-einingu geta verið öðruvísi en það sem er sýnt í biðlara Dynamics.</span><span class="sxs-lookup"><span data-stu-id="ecffb-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="ecffb-133">Þegar ytri upprunar eins og DMF eru notaðir til að skoða eða heimila gögn skal hafa í huga að gildin **Dagsetning og tími** eru sjálfgefið stillt á UTC alveg óháð því í hvaða tímabelti tölva notandans er eða hverjar gildandi stillingar á tímabelti notandans eru.</span><span class="sxs-lookup"><span data-stu-id="ecffb-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="ecffb-134">Dæmi um sömu skrá sem birtist á mismunandi afurðasvæðum</span><span class="sxs-lookup"><span data-stu-id="ecffb-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="ecffb-135">**Human Resources með tímabelti notanda stillt á UTC**</span><span class="sxs-lookup"><span data-stu-id="ecffb-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="ecffb-136">[![Skjámynd starfsmanns stillt á UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="ecffb-137">**Human Resources með tímabelti notanda stillt á GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="ecffb-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="ecffb-138">[![Skjámynd starfsmanns stillt á GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="ecffb-139">**Excel í gegnum OData**</span><span class="sxs-lookup"><span data-stu-id="ecffb-139">**Excel Via OData**</span></span>

<span data-ttu-id="ecffb-140">[![Excel í gegnum OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="ecffb-141">**DMF-sviðsetning**</span><span class="sxs-lookup"><span data-stu-id="ecffb-141">**DMF Staging**</span></span>

<span data-ttu-id="ecffb-142">[![DMF-sviðsetning](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="ecffb-143">**Útflutningur á DMF**</span><span class="sxs-lookup"><span data-stu-id="ecffb-143">**DMF Export**</span></span>

<span data-ttu-id="ecffb-144">[![Útflutningur á DMF](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="ecffb-145">**Excel í gegnum Dataverse**</span><span class="sxs-lookup"><span data-stu-id="ecffb-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="ecffb-146">[![Excel í gegnum Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="ecffb-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="ecffb-147">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="ecffb-147">See also</span></span>

[<span data-ttu-id="ecffb-148">Dagsetningar- og tímagögn</span><span class="sxs-lookup"><span data-stu-id="ecffb-148">Date and time data</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="ecffb-149">Valin tímabelti notanda</span><span class="sxs-lookup"><span data-stu-id="ecffb-149">User preferred time zones</span></span>](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]