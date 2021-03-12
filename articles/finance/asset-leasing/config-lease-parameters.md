---
title: Skilgreina færibreytur leigusamninga (forskoðun)
description: Þetta efnisatriði lýsir skilgreiningarstillingum fyrir Eignaleigu, svo sem öryggisupplýsingum og bókhaldsstillingum.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ff0aa5fd0b78814dfa5bb00d6d5ef2984c566d14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971404"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="20755-103">Skilgreina færibreytur leigu</span><span class="sxs-lookup"><span data-stu-id="20755-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20755-104">Nokkrar skilgreiningarstillingar hafa áhrif á það hvernig Eignarleiga virkar.</span><span class="sxs-lookup"><span data-stu-id="20755-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="20755-105">Þessar stillingar innihalda færslubókarnöfn, almennar færibreytur og stillingar bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="20755-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="20755-106">Opnið **Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="20755-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="20755-107">Á flipanum **Leigusamningar** skal velja flipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="20755-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="20755-108">**Heimila Handvirk flokkun hnekking** færibreyta ákvarðar hvort hægt sé að hnekkja flokkun leigusamninga áður en greiðsluáætlun er staðfest.</span><span class="sxs-lookup"><span data-stu-id="20755-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="20755-109">**Runueining yfir allt** færibreytan ákvarðar hvort hægt er að bóka á aðra lögaðila frá núverandi lögaðila.</span><span class="sxs-lookup"><span data-stu-id="20755-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="20755-110">Ef kveikt er á þessari færibreytu er hægt að stofna bókarfærslu fyrir lögaðilana sem notandinn hefur aðgang að.</span><span class="sxs-lookup"><span data-stu-id="20755-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="20755-111">Stilla **leyfa eyðingu á staðfestum leigusamningum** valkostur á **Já** til að heimila leigusamninga sem eru með staðfestar greiðsluáætlanir sem á að eyða.</span><span class="sxs-lookup"><span data-stu-id="20755-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="20755-112">Ekki er hægt að eyða leigusamningum ef bókaðar eða óbókaðar færslur eru tengdar þeim, óháð hvernig þessi valkostur er stilltur.</span><span class="sxs-lookup"><span data-stu-id="20755-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="20755-113">Ekki er hægt að endurheimta leiguskrá eftir að henni hefur verið eytt.</span><span class="sxs-lookup"><span data-stu-id="20755-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="20755-114">Ef færslum fyrir eyddan leigusamning er hlaðið upp, annaðhvort handvirkt eða með gagnaeiningum, eru hlaðnar upplýsingar meðhöndlaðar sem nýjar, ekki sem uppfærslur á fyrirliggjandi leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="20755-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="20755-115">Ef þessi valkostur er stilltur á **Já**, og breytingagerð bókarinnar er **valkostur A eða B fyrir uppsafnaða endurnýjun**, stillir kerfið reitinn **vextir á nýju lánsfé** við gildi **vextir á nýju lánsfé við umbreytingu** reitinn í **bókaruppsetning** síða.</span><span class="sxs-lookup"><span data-stu-id="20755-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="20755-116">Ef þessi valkostur er stilltur á **Nei** er taxtinn á höfuð leigusamningsins stilltur á gildi **vextir á nýju lánsfé** á síðunni **bókarupplýsingar**, óháð umbreytingargerð á bókinni.</span><span class="sxs-lookup"><span data-stu-id="20755-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="20755-117">Stilla valkostinn **útgáfu Leyfa bakfærslur afskrifta í lokaðri bók** á **Já** til að leyfa að hægt sé að bakfæra afskriftarkostnaðarfærslur.</span><span class="sxs-lookup"><span data-stu-id="20755-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="20755-118">Hægt er að bakfæra kostnaðarfærslur jafnvel þegar bókaútgáfan er lokuð.</span><span class="sxs-lookup"><span data-stu-id="20755-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="20755-119">Mælt er með því að þessi valkostur sé stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="20755-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="20755-120">Stillingin fyrir þennan valkost er notuð sem staðfesting og stjórnun til að koma í veg fyrir að lokuð bókaútgáfa sé óvart afskrifuð.</span><span class="sxs-lookup"><span data-stu-id="20755-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="20755-121">Með því að stilla valkostinn á **Nei** er hjálpað við að halda bókuðu nettóvirði og útreikningum á afskriftum í framtíðinni réttum.</span><span class="sxs-lookup"><span data-stu-id="20755-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
