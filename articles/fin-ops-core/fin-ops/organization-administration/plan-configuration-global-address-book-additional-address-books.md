---
title: Skipuleggja altæku aðsetursbókina og aðrar aðsetursbækur
description: Þetta efnisatriði lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a0613b944d0446e339480a71fa890702190ed53
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559966"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="a9bb2-103">Skipuleggja altæku aðsetursbókina og aðrar aðsetursbækur</span><span class="sxs-lookup"><span data-stu-id="a9bb2-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9bb2-104">Þetta efnisatriði lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="a9bb2-105">Sumir af þeim ákvörðunum munu krefjast þess að þú staðfestir þær ákvarðanir sem hafa verið gerðar fyrir önnur svið vörunnar, svo sem stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="a9bb2-106">Altæk aðsetursbók</span><span class="sxs-lookup"><span data-stu-id="a9bb2-106">Global address book</span></span>

<span data-ttu-id="a9bb2-107">Áður en byrjað er að vinna með í altækri aðsetursbók verður að ákvarða sjálfgefin gildi fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="a9bb2-108">Þessi sjálfgildi eru síðan notaðar fyrir allar aðrar aðsetursbækur sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="a9bb2-109">**Ákvarðanir**</span><span class="sxs-lookup"><span data-stu-id="a9bb2-109">**Decisions**</span></span>

- <span data-ttu-id="a9bb2-110">Hvaða röð ætti nöfn að birtast í fyrir aðilafærslur fyrir gerðina **Einstaklingur**?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="a9bb2-111">Til dæmis er ein röð eftirnafn, millinafn fornafn.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="a9bb2-112">Á eyða aðilafærslur úr aðsetursbókinni þegar hlutverk færslu er eytt?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="a9bb2-113">Til dæmis, ef færslu um viðskiptavin er eytt er á einnig að eyða færslu aðila?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="a9bb2-114">Þegar ný færsla er stofnuð á notendum að tilkynna ef tvítekin færsla fannst í altæku aðsetursbókinni?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="a9bb2-115">Á DUNS-númer (Data Universal Numbering System) að fylgja með í upplýsingum aðilafærslu?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="a9bb2-116">Ef duns-númer er innifalin í aðilafærslu þarf að athuga einkvæmni númersins?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="a9bb2-117">Þegar aðilafærsla er stofnuð í altæku aðsetursbókinni á aðilagerð, manneskju eða fyrirtæki að vera sjálfgefin, ?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="a9bb2-118">Hvaða notandahlutverk ætti að hafa aðgang að persónulegum aðsetrum og tengslaupplýsingum fyrir aðilafærslur?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="a9bb2-119">Auka aðsetursbækur</span><span class="sxs-lookup"><span data-stu-id="a9bb2-119">Additional address books</span></span>

<span data-ttu-id="a9bb2-120">Þegar Búið er að stofna altæka aðsetursbók, er hægt að stofna viðbótar aðsetursbækur sem þörf er á, svo sem aðskilda aðsetursbókar fyrir hvert fyrirtæki í þínu samsteypu eða fyrir hverja atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="a9bb2-121">Til dæmis er Fabrikam alþjóðlegt fyrirtæki sem er með mörg fyrirtæki og margar atvinnugreinar.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="a9bb2-122">Fabrikam áformar að stofna aðsetursbók fyrir hverja atvinnugrein.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="a9bb2-123">Fyrir atvinnugreinar sem eru á fleiri en einum stað, eins og viðskipti með loftknúin verkfæri, áformar Fabrikam að stofna aðsetursbók fyrir hverja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="a9bb2-124">Chris, tæknistjóri hjá Fabrikam, hefur stofnað eftirfarandi listi yfir aðsetursbækur sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="a9bb2-125">Þessi listi lýsir einnig aðilafærslum sem hver aðsetursbók verður að hafa.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="a9bb2-126">**Samningar hins opinbera (PubSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum hins opinbera sem Fabrikam býr yfir.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="a9bb2-127">**Samningar almenns vinnumarkaðar (PriSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum almenns vinnumarkaðar sem Fabrikam býr yfir.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="a9bb2-128">**Rafræn Verkfæri (ET)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á rafræna verkfæri, eða verkfæra sem annars tengjast á einhvern hátt rafrænum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="a9bb2-129">**Loftknúin Verkfæri (PTJPN)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="a9bb2-130">**Loftknúin Verkfæri (PTUSA)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-US fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a9bb2-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="a9bb2-131">**Ákvörðun:**</span><span class="sxs-lookup"><span data-stu-id="a9bb2-131">**Decision:**</span></span>

- <span data-ttu-id="a9bb2-132">Hversu margar viðbótar aðsetursbækur muntu stofna?</span><span class="sxs-lookup"><span data-stu-id="a9bb2-132">How many additional address books will you create?</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]