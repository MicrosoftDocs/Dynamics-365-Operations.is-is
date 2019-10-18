---
title: Yfirlit yfir jákvæða greiðslu
description: Þessi grein veitir upplýsingar um jákvæðar greiðslur, sem eru notaðar til að mynda rafræna lista yfir ávísanir sem eru innleystar í banka.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49fe8369fce599d16134541b1c968727f38ebff9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189638"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="f1e9c-103">Yfirlit yfir jákvæða greiðslu</span><span class="sxs-lookup"><span data-stu-id="f1e9c-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1e9c-104">Þessi grein veitir upplýsingar um jákvæðar greiðslur, sem eru notaðar til að mynda rafræna lista yfir ávísanir sem eru innleystar í banka.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="f1e9c-105">Hægt er að nota jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru innleystar í banka.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="f1e9c-106">Jákvæðar greiðsluskrár geta auðveldð bönkum að koma í veg fyrir ávísanafals.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="f1e9c-107">Þú setur upp jákvæða greiðslu til að mynda rafræna skrá yfir ávísanir í hvert sinn sem ávísanir eru prentaðar.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="f1e9c-108">Þegar ávísun er innleyst í bankanum ber bankinn ávísunina saman við lista yfir ávísanir sem þú hefur sent áður.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="f1e9c-109">Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="f1e9c-110">Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="f1e9c-111">Jákvæð greo‘sæa er einnig þekkt sem SafePay.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="f1e9c-112">Jákvæðu greiðsluskránni geta innihaldið viðkvæmar upplýsingar um greiðsluþegar og upphæðir ávísunar.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="f1e9c-113">Þess vegna skaltu vera viss um að nota viðeigandi öryggisráðstafanir frá þeim tíma sem skrárnar eru myndaðar og þar til þær eru mótteknar í bankanum.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="f1e9c-114">Jákvæðum greiðsluskrám er hlaðið niður í samræmi við leiðbeiningar um niðurhal í vefvafra.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="f1e9c-115">Jákvæð greiðsluskrár eru stofnaðar með því að nota gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="f1e9c-116">Áður en jákvæð greiðsluskrá er mynduð, verður að setja upp umbreytingasnið fyrir XML sem þýðir gögnin yfir á snið sem bankinn getur notað.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="f1e9c-117">Fyrir hvern bankareikning sem á að mynda jákvæðar greiðsluupplýsingar til, verður að úthluta jákvæða greiðslusniðinu.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="f1e9c-118">Eftir að greiðslur eru myndaðar er hægt að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="f1e9c-119">Hins vegar er hægt að mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="f1e9c-120">Eftir að búið er að greiða ávísanir sem eru talin upp í jákvæðu greiðsluskránni berst staðfestingarnúmer frá bankanum.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="f1e9c-121">Síðan er hægt að staðfesta jákvæðu greiðsluskrána í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="f1e9c-122">Ef nauðsynlegt er að breyta jákvæðri greiðsluskrá er hægt að afturkalla hana.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="f1e9c-123">Í þeim tilfellum er svæðið sem gefur til kynna hvort viðkomandi ávísun hefur verið tekin með í jákvæðri greiðsluskrá endurstillt fyrir hverja ávísun í jákvæðu greiðsluskránni.</span><span class="sxs-lookup"><span data-stu-id="f1e9c-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="f1e9c-124">Nánari upplýsingar er að finna í [Setja upp og mynda jákvæða greiðsluskrá launa](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="f1e9c-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>



