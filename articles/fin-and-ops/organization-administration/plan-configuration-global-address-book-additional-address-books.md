---
title: "Áætlun fyrir uppsetningu altækrar aðsetursbókar og viðbótar aðsetursbækur"
description: "Þessi grein lýsir álitamálum og ákvörðunum sem þarf að taka í áætlunarferli áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur í Microsoft Dynamics 365 for Finance and Operations. Sumir af þeim ákvörðunum munu krefjast þess að þú staðfestir þær ákvarðanir sem hafa verið gerðar fyrir önnur svið vörunnar, svo sem stigveldi fyrirtækis."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a><span data-ttu-id="aba52-104">Áætlun fyrir uppsetningu altækrar aðsetursbókar og viðbótar aðsetursbækur</span><span class="sxs-lookup"><span data-stu-id="aba52-104">Plan how to configure the global address book and additional address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aba52-105">Þessi grein lýsir álitamálum og ákvörðunum sem þarf að taka í áætlunarferli áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur í Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="aba52-105">This article describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="aba52-106">Sumir af þeim ákvörðunum munu krefjast þess að þú staðfestir þær ákvarðanir sem hafa verið gerðar fyrir önnur svið vörunnar, svo sem stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="aba52-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="aba52-107">Altæk aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="aba52-107">Global address book</span></span>
-------------------

<span data-ttu-id="aba52-108">Áður en byrjað er að vinna með í altækri aðsetursbók verður að ákvarða sjálfgefin gildi fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="aba52-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="aba52-109">Þessi sjálfgildi eru síðan notaðar fyrir allar aðrar aðsetursbækur sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="aba52-109">These default values are then used for any additional address books that you create.</span></span> 

<span data-ttu-id="aba52-110">**Ákvarðanir:**</span><span class="sxs-lookup"><span data-stu-id="aba52-110">**Decisions:**</span></span>

-   <span data-ttu-id="aba52-111">Hvaða röð ætti nöfn að birtast í fyrir aðilafærslur fyrir gerðina **Einstaklingur**?</span><span class="sxs-lookup"><span data-stu-id="aba52-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="aba52-112">Til dæmis er ein röð eftirnafn, millinafn fornafn.</span><span class="sxs-lookup"><span data-stu-id="aba52-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="aba52-113">Á eyða aðilafærslur úr aðsetursbókinni þegar hlutverk færslu er eytt?</span><span class="sxs-lookup"><span data-stu-id="aba52-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="aba52-114">Til dæmis, ef færslu um viðskiptavin er eytt er á einnig að eyða færslu aðila?</span><span class="sxs-lookup"><span data-stu-id="aba52-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="aba52-115">Þegar ný færsla er stofnuð á notendum að tilkynna ef tvítekin færsla fannst í altæku aðsetursbókinni?</span><span class="sxs-lookup"><span data-stu-id="aba52-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="aba52-116">Á að fylgja DUNS-númer (Data Universal Numbering System-númer) með í upplýsingum aðilafærslu?</span><span class="sxs-lookup"><span data-stu-id="aba52-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="aba52-117">Ef duns-númer er innifalin í aðilafærslu þarf að athuga einkvæmni númersins?</span><span class="sxs-lookup"><span data-stu-id="aba52-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="aba52-118">Þegar aðilafærsla er stofnuð í altæku aðsetursbókinni á aðilagerð, manneskju eða fyrirtæki að vera sjálfgefin, ?</span><span class="sxs-lookup"><span data-stu-id="aba52-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="aba52-119">Hvaða notandahlutverk ætti að hafa aðgang að persónulegum aðsetrum og tengslaupplýsingum fyrir aðilafærslur?</span><span class="sxs-lookup"><span data-stu-id="aba52-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="aba52-120">Auka aðsetursbækur</span><span class="sxs-lookup"><span data-stu-id="aba52-120">Additional address books</span></span>
<span data-ttu-id="aba52-121">Þegar Búið er að stofna altæka aðsetursbók, er hægt að stofna viðbótar aðsetursbækur sem þörf er á, svo sem aðskilda aðsetursbókar fyrir hvert fyrirtæki í þínu samsteypu eða fyrir hverja atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="aba52-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="aba52-122">Til dæmis er Fabrikam alþjóðlegt fyrirtæki sem er með mörg fyrirtæki og margar atvinnugreinar.</span><span class="sxs-lookup"><span data-stu-id="aba52-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="aba52-123">Fabrikam áformar að stofna aðsetursbók fyrir hverja atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="aba52-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="aba52-124">Fyrir atvinnugreinar sem eru á fleiri en einum stað, eins og viðskipti með loftknúin verkfæri, áformar Fabrikam að stofna aðsetursbók fyrir hverja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="aba52-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="aba52-125">Chris, tæknistjóri hjá Fabrikam, hefur stofnað eftirfarandi listi yfir aðsetursbækur sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="aba52-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="aba52-126">Þessi listi lýsir einnig aðilafærslur sem hver aðsetursbók verður að hafa.</span><span class="sxs-lookup"><span data-stu-id="aba52-126">This list also also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="aba52-127">**Samningar hins opinbera (PubSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum hins opinbera sem Fabrikam býr yfir.</span><span class="sxs-lookup"><span data-stu-id="aba52-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="aba52-128">**Samningar almenns vinnumarkaðar (PriSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum almenns vinnumarkaðar sem Fabrikam býr yfir.</span><span class="sxs-lookup"><span data-stu-id="aba52-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="aba52-129">**Rafræn Verkfæri (ET)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á rafræna verkfæri, eða verkfæra sem annars tengjast á einhvern hátt rafrænum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="aba52-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="aba52-130">**Loftknúin Verkfæri (PTJPN)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="aba52-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="aba52-131">**Loftknúin Verkfæri (PTUSA)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-US fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="aba52-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="aba52-132">**Ákvörðun:**</span><span class="sxs-lookup"><span data-stu-id="aba52-132">**Decision:**</span></span>

-   <span data-ttu-id="aba52-133">Hversu margar viðbótar aðsetursbækur muntu stofna?</span><span class="sxs-lookup"><span data-stu-id="aba52-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="aba52-134">Öryggi Aðsetursbókar</span><span class="sxs-lookup"><span data-stu-id="aba52-134">Address book security</span></span>

<span data-ttu-id="aba52-135">Hægt er að stofna aðsetursbækur hvenær sem er, og einnig er hægt að stilla öryggisfæribreytur fyrir aðsetursbækurnar hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="aba52-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="aba52-136">Ekki þarf að setja öryggisréttindi fyrir aðsetursbók, en það er ekki gert geta alla starfsmenn í fyrirtækinu þínu skoða allar færslur allra aðila sem eru í aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="aba52-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="aba52-137">Hægt er að setja upp öryggisréttindi fyrir aðilafærslu í gegnum aðsetursbækur.</span><span class="sxs-lookup"><span data-stu-id="aba52-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="aba52-138">Öryggisréttindi á grundvölluð á teymi.</span><span class="sxs-lookup"><span data-stu-id="aba52-138">Security privileges are based on teams.</span></span> <span data-ttu-id="aba52-139">Þessi nálgun tryggir að aðeins starfsmenn sem eru úthlutaðar teymi sem hefur aðgang að aðsetursbók geta skoðað færslur aðila í þeirri aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="aba52-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="aba52-140">Þú verður að velja hópa sem hefur aðgang að hverju aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="aba52-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="aba52-141">Fyrir hverja aðsetursbók hægt er að setja öryggisréttindi sem heimila eða hafna aðgang fyrir tilteknum teymi.</span><span class="sxs-lookup"><span data-stu-id="aba52-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="aba52-142">Þegar er hóp er veittur réttindi fyrir aðgang að aðsetursbók, geta allir hópmeðlimum skoða færslurnar í aðsetursbók.</span><span class="sxs-lookup"><span data-stu-id="aba52-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="aba52-143">Þegar er hóp er ekki veittur aðgangur fyrir aðgang að aðsetursbók, geta hópmeðlimir ekki skoða færslurnar í aðsetursbók eða efni hennar.</span><span class="sxs-lookup"><span data-stu-id="aba52-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> 

<span data-ttu-id="aba52-144">**Ákvörðun:**</span><span class="sxs-lookup"><span data-stu-id="aba52-144">**Decision:**</span></span>

-   <span data-ttu-id="aba52-145">Hvaða teymi ætti að hafa aðgang að hverju nýja aðsetursbók sem verður stofnað?</span><span class="sxs-lookup"><span data-stu-id="aba52-145">Which teams should have access to each new address book that you will create?</span></span>





