---
title: Úrræðaleit fyrir frátekningar í vöruhúsastjórnun
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsafrátektir í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828107"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="fe97a-103">Úrræðaleit fyrir frátekningar í vöruhúsastjórnun</span><span class="sxs-lookup"><span data-stu-id="fe97a-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe97a-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsafrátektir í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fe97a-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="fe97a-105">Fyrir efnisatriði sem tengjast skráningu runu-og raðnúmerum skal skoða [Úrræðaleit fyrir keyrslur vöruhúss og frátekningastigveldi raða](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="fe97a-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="fe97a-106">Ég fæ eftirfarandi villuboð: „Ekki er hægt að fjarlægja frátekningar vegna þess að búið er að stofna vinnu sem byggir á frátekningunum.“</span><span class="sxs-lookup"><span data-stu-id="fe97a-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe97a-107">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fe97a-107">Issue description</span></span>

<span data-ttu-id="fe97a-108">Ekki er hægt að taka frá birgðir á sölulínu, þar sem það er opin vinna á móti línunni.</span><span class="sxs-lookup"><span data-stu-id="fe97a-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe97a-109">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fe97a-109">Issue resolution</span></span>

<span data-ttu-id="fe97a-110">Kanna hvort opin pökkunarhópvinna er til staðar til að koma vörunni úr pökkunarstöð á aðra staðsetningu (t.d. *útskot*).</span><span class="sxs-lookup"><span data-stu-id="fe97a-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="fe97a-111">Farið yfir færslurnar í **Ferilannál vinnustofnunar** og **Upplýsingar um verk** til að ákvarða hvað er efnislega verið að taka frá í birgðum og ljúka því eða eyða vinnu til að losa frátektina.</span><span class="sxs-lookup"><span data-stu-id="fe97a-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="fe97a-112">Ég fæ eftirfarandi villuboð: „Ekki var hægt að uppfæra birgðamagnið %1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2...“</span><span class="sxs-lookup"><span data-stu-id="fe97a-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe97a-113">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fe97a-113">Issue description</span></span>

<span data-ttu-id="fe97a-114">Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir.</span><span class="sxs-lookup"><span data-stu-id="fe97a-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="fe97a-115">Hér er allur texti villuskilaboða:</span><span class="sxs-lookup"><span data-stu-id="fe97a-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="fe97a-116">Ekki var hægt að uppfæra birgðamagnið -%1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2 með málin Stærð=%3, Litur=%4, Viðbætur=%5, Staður=%6, Vöruhús=%7, Staðsetning=%8, Birgðastaða=Tiltækar, Leyfisplata=%9, Lotunúmer=%10 tilvísunarauðkenni %11 á lotukenni %12.</span><span class="sxs-lookup"><span data-stu-id="fe97a-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe97a-117">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fe97a-117">Issue resolution</span></span>

<span data-ttu-id="fe97a-118">Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu.</span><span class="sxs-lookup"><span data-stu-id="fe97a-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="fe97a-119">Til dæmis gætu þessar færslur opnað gæðapantanir, birgðalokunarfærslur eða úttakspantanir.</span><span class="sxs-lookup"><span data-stu-id="fe97a-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="fe97a-120">Ég fæ eftirfarandi villuboð: „Efnislega á lager... Ekki er hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.“</span><span class="sxs-lookup"><span data-stu-id="fe97a-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe97a-121">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="fe97a-121">Issue description</span></span>

<span data-ttu-id="fe97a-122">Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir.</span><span class="sxs-lookup"><span data-stu-id="fe97a-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="fe97a-123">Hér er allur texti villuskilaboða:</span><span class="sxs-lookup"><span data-stu-id="fe97a-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="fe97a-124">Efnislegt lagersvæði =%1, Vöruhús=%2, Birgðastaða =Tiltækt, Rununúmer=%3, Eigandi=%4: %5 er ekki hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.</span><span class="sxs-lookup"><span data-stu-id="fe97a-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe97a-125">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="fe97a-125">Issue resolution</span></span>

<span data-ttu-id="fe97a-126">Þetta vandamál stafar líklega af opinni vinnu.</span><span class="sxs-lookup"><span data-stu-id="fe97a-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="fe97a-127">Annaðhvort skal ljúka vinnu eða taka við án þess að stofna vinnu.</span><span class="sxs-lookup"><span data-stu-id="fe97a-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="fe97a-128">Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu.</span><span class="sxs-lookup"><span data-stu-id="fe97a-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="fe97a-129">Til dæmis gætu þessar færslur verið opnar gæðapantanir, birgðalokunarfærslur eða úttakspantanir.</span><span class="sxs-lookup"><span data-stu-id="fe97a-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
