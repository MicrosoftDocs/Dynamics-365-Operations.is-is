---
title: Hreinsunarvinnsla lagerbirgðafærslna vöruhúsakerfis
description: Þetta efnisatriði lýsir hreinsunarvinnslu á lagerbirgðafærslum, sem eykur afköst kerfisins með því að auðkenna og eyða tengdum en ónauðsynlegum færslum.
author: perlynne
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f6d1f8a4c85c2161d1b79246d437bb3b4d223d1d
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410956"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a><span data-ttu-id="bb3bc-103">Hreinsunarvinnsla lagerbirgðafærslna vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="bb3bc-103">Warehouse management on-hand entries cleanup job</span></span>

<span data-ttu-id="bb3bc-104">Afköst fyrirspurna sem eru notaðar til að reikna lagerbirgðir verður fyrir áhrifum af færslufjöldanum í töflunum sem koma við sögu.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-104">The performance of queries that are used to calculate on-hand inventory is affected by the number of records in the tables that are involved.</span></span> <span data-ttu-id="bb3bc-105">Ein leið til að auka afköst er að draga úr fjölda færslna sem gagnagrunnurinn þarf að hafa í huga.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-105">One way to help improve the performance is to reduce the number of records that the database must consider.</span></span>

<span data-ttu-id="bb3bc-106">Þetta efnisatriði lýsir hreinsunarvinnslu á lagerbirgðafærslum, sem eyðir ónauðsynlegum færslum í töflunum InventSum og WHSInventReserve.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-106">This topic describes the on-hand entries cleanup job, which deletes unneeded records in the InventSum and WHSInventReserve tables.</span></span> <span data-ttu-id="bb3bc-107">Þessar töflur geyma upplýsingar um lager fyrir vörur sem eru virkar fyrir vinnslu vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-107">These tables store on-hand information for items that are enabled for warehouse management processing.</span></span> <span data-ttu-id="bb3bc-108">(Þessar vörur nefnast WHS-vörur.) Eyðing þessara færslna getur stóraukið afköst lagerútreikninga.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-108">(These items are referred to as WHS items.) Deletion of these records can significantly improve the performance of on-hand calculations.</span></span>

## <a name="what-the-cleanup-job-does"></a><span data-ttu-id="bb3bc-109">Hvað gerir hreinsunarvinnslan</span><span class="sxs-lookup"><span data-stu-id="bb3bc-109">What the cleanup job does</span></span>

<span data-ttu-id="bb3bc-110">Hreinsunarvinnsla lagerbirgðafærslna eyðir öllum færslum í töflunum WHSInventReserve og InventSum þar sem öll reitargildi eru *0* (núll).</span><span class="sxs-lookup"><span data-stu-id="bb3bc-110">The on-hand entries cleanup job deletes any records in the WHSInventReserve and InventSum tables where all the field values are *0* (zero).</span></span> <span data-ttu-id="bb3bc-111">Hægt er að eyða þessum færslum vegna þess að þær leggja ekki til upplýsingar um lagerbirgðir.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-111">These records can be deleted because they don't contribute to the on-hand information.</span></span> <span data-ttu-id="bb3bc-112">Vinnslan eyðir aðeins færslum sem eru fyrir neðan stigið **Staðsetning**.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-112">The job deletes only records that are below the **Location** level.</span></span>

<span data-ttu-id="bb3bc-113">Ef neikvæðar efnislegar birgðir eru leyfðar er hugsanlegt að hreinsunarvinnslan geti ekki eytt öllum færslum sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-113">If negative physical inventory is allowed, the cleanup job might not be able to delete all the relevant entries.</span></span> <span data-ttu-id="bb3bc-114">Ástæðan fyrir þessari takmörkun er sú að vinnslan verður að leyfa sérstakar aðstæður þar sem númeraplata er með mörg raðnúmer og eitt þessara raðnúmera er orðið neikvætt.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-114">The reason for this limitation is that the job must allow for a special scenario where a license plate has multiple serial numbers, and one of those serial numbers has become negative.</span></span> <span data-ttu-id="bb3bc-115">Til dæmis verður kerfið með núll á lager á stigi númeraplötu þegar númeraplata er með +1 stk af raðnúmeri 1 og –1 stk af raðnúmeri 2.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-115">For example, the system will have zero on hand at the license plate level when a license plate has +1 pcs of serial number 1 and –1 pcs of serial number 2.</span></span> <span data-ttu-id="bb3bc-116">Við þessar sérstöku aðstæður eyðir vinnslan fyrst á breiddina, þar sem hún reynir fyrst að eyða á lægri stigum.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-116">For this special scenario, the job does a breadth-first deletion, where it tries to delete from lower levels first.</span></span>

## <a name="schedule-and-configure-the-cleanup-job"></a><span data-ttu-id="bb3bc-117">Áætla og skilgreina hreinsunarvinnsluna</span><span class="sxs-lookup"><span data-stu-id="bb3bc-117">Schedule and configure the cleanup job</span></span>

<span data-ttu-id="bb3bc-118">Hreinsunarvinnsla lagerbirgðafærslna er tiltæk í **Birgðastjórnun \> Reglubundin verkefni \> Hreinsun \> Hreinsun lagerbirgðafærslna vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-118">The on-hand entries cleanup job is available at **Inventory management \> Periodic tasks \> Clean up \> Warehouse management on-hand entries cleanup**.</span></span> <span data-ttu-id="bb3bc-119">Notið staðlaðar vinnslustillingar til að stýra umfangi og áætlun fyrir keyrslu vinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-119">Use the standard job settings to control the scope and schedule for running the job.</span></span> <span data-ttu-id="bb3bc-120">Þar að auki eru eftirfarandi stillingar í boði:</span><span class="sxs-lookup"><span data-stu-id="bb3bc-120">In addition, the following settings are provided:</span></span>

- <span data-ttu-id="bb3bc-121">**Eyða ef ekki uppfærðar í þetta marga daga** – Færið inn lágmarksfjölda daga sem vinnslan á að bíða áður en hún eyðir lagerbirgðafærslu sem hefur dottið niður í núll í magni.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-121">**Delete if not updated for this many days** – Enter the minimum number of days that the job should wait before it deletes an on-hand entry that has dropped to zero quantity.</span></span> <span data-ttu-id="bb3bc-122">Notið þessa stillingu til að draga úr hættu á að eyða færslum á lager sem enn er verið að nota.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-122">Use this setting to help reduce the risk of deleting on-hand entries that are still being used.</span></span> <span data-ttu-id="bb3bc-123">Ef hreinsun á að fara fram sem fyrst skal annaðhvort slá inn *0* (núll) eða skilja reitinn eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-123">If you want cleanup to occur as soon as possible, either enter *0* (zero) or leave the field blank.</span></span>
- <span data-ttu-id="bb3bc-124">**Hámarkskeyrslutími (klukkustundir)** - Sláið inn hámarkskeyrslutíma hreinsunarvinnslu, í klukkustundum.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-124">**Maximum execution time (hours)** – Enter the maximum execution time of the cleanup job, in hours.</span></span> <span data-ttu-id="bb3bc-125">Ef vinnslunni er ekki lokið áður en þessi tími rennur út, vistar hún vinnuna sem er lokið fram að þessu og lokar vinnslunni.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-125">If the job isn't completed before this time passes, it will save the work that it has completed so far and then close itself.</span></span> <span data-ttu-id="bb3bc-126">Þessi möguleiki á sérstaklega við um innleiðingar með mikilli birgðanotkun.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-126">This capability is especially relevant for implementations that have high inventory use.</span></span> <span data-ttu-id="bb3bc-127">Í slíkum tilfellum ætti að áætla að keyra vinnsluna á tímum þegar er sem minnst álag á kerfinu.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-127">In these cases, you should schedule the job to run at times when the system load is as light as possible.</span></span> <span data-ttu-id="bb3bc-128">Ef halda á keyrslu runuvinnslunnar áfram þar til hún klárast skal slá inn *0* (núll) eða skilja reitinn eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-128">If you want the batch job to continue to run until it's completed, either enter *0* (zero) or leave the field blank.</span></span> <span data-ttu-id="bb3bc-129">Þessi stilling er aðeins í boði ef tengdur eiginleiki hefur verið [kveikt á í kerfinu](#max-execution-time).</span><span class="sxs-lookup"><span data-stu-id="bb3bc-129">This setting is available only if the related feature has been [turned on in your system](#max-execution-time).</span></span>

<span data-ttu-id="bb3bc-130">Þótt hægt sé að keyra vinnsluna á venjulegum vinnutíma er mælt með því að keyra hana utan vinnustunda.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-130">Although you can run the job during regular business hours, we recommend that you run it outside working hours.</span></span> <span data-ttu-id="bb3bc-131">Þannig er komið í veg fyrir árekstra sem geta átt sér stað ef notandi er að vinna í færslu sem einnig er verið að hreinsa.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-131">In this way, you help prevent conflicts that can occur if a user is working with a record that is also being cleaned up.</span></span>

<span data-ttu-id="bb3bc-132">Ef vinnslan reynir að eyða færslu fyrir vöru á meðan annar notandi er að nota þá færslu, kemur upp sjálfhelduvilla hjá annaðhvort hreinsunarvinnslunni eða notandanum.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-132">If the job tries to delete a record for an item while that record is being used by another user, a deadlock error occurs for either the cleanup job or the user.</span></span>

<span data-ttu-id="bb3bc-133">Þegar vinnslan er í gangi er hún með staðfestingarstærðina 100.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-133">When the job runs, it has a commit size of 100.</span></span> <span data-ttu-id="bb3bc-134">Hún reynir sem sagt að staðfesta eitt skipti fyrir hverjar 100 eyðingar.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-134">In other words, it will try to commit one time for every 100 deletions.</span></span> <span data-ttu-id="bb3bc-135">Hins vegar, vegna þess að sumar eyðingar eru samstæðubyggðar, geta komið upp aðstæður þar sem hægt er að eyða meira en 100 skrám í sömu færslunni.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-135">However, because some deletions are set-based, there might be scenarios where more than 100 records can be deleted in the same transaction.</span></span> <span data-ttu-id="bb3bc-136">Þess vegna geta stigvaxandi læsingar enn átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-136">Therefore, lock escalations can still sometimes occur.</span></span>

## <a name="possible-user-impact"></a><span data-ttu-id="bb3bc-137">Hugsanleg áhrif á notanda</span><span class="sxs-lookup"><span data-stu-id="bb3bc-137">Possible user impact</span></span>

<span data-ttu-id="bb3bc-138">Notendur gætu orðið fyrir áhrifum ef hreinsunarvinnsla lagerbirgðafærslna eyðir öllum færslum fyrir uppgefið stig (t.d. númeraplötustigið).</span><span class="sxs-lookup"><span data-stu-id="bb3bc-138">Users might be affected if the on-hand entries cleanup job deletes all the records for a given level (such as the license plate level).</span></span> <span data-ttu-id="bb3bc-139">Í slíku tilfelli gæti aðgerðin til að sjá að birgðir séu til staðar á lager á númeraplötu ekki virkað sem skyldi vegna þess að viðeigandi lagerbirgðafærslur eru ekki lengur í boði.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-139">In this case, the functionality for seeing that inventory was previously available on hand at a license plate might not work as expected, because the relevant on-hand entries are no longer available.</span></span> <span data-ttu-id="bb3bc-140">(Þessi aðgerð athugar skilyrðið **Magn \<\> 0** í stillingunum **Birting víddar** þegar notendur skoða lagerupplýsingar.) Hins vegar ættu aukin afköst sem hreinsunarvinnslan býður upp á að bæta upp fyrir þetta litla tap í virkni.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-140">(That functionality checks the condition **Quantity \<\> 0** in the **Dimension display** settings when users view on-hand information.) However, the performance improvement that the cleanup job provides should make up for this small loss in functionality.</span></span>

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a><span data-ttu-id="bb3bc-141">Gera stillingu hámarkskeyrslutíma tiltæka</span><span class="sxs-lookup"><span data-stu-id="bb3bc-141">Make the Maximum execution time setting available</span></span>

<span data-ttu-id="bb3bc-142">Sjálfgefið er að stillingin **Hámarkskeyrslutími** sé ekki í boði.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-142">By default, the **Maximum execution time** setting isn't available.</span></span> <span data-ttu-id="bb3bc-143">Ef ætlunin er að nota hann þarf að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á tengdum eiginleika í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="bb3bc-143">If you want to use it, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the related feature in your system.</span></span> <span data-ttu-id="bb3bc-144">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="bb3bc-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bb3bc-145">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="bb3bc-145">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="bb3bc-146">**Heiti eiginleika:** *Hámarkskeyrslutími á hreinsunarvinnslu lagerbirgðafærslna vöruhúsakerfis*</span><span class="sxs-lookup"><span data-stu-id="bb3bc-146">**Feature name:** *Maximum execution time for the warehouse management on-hand entries cleanup job*</span></span>