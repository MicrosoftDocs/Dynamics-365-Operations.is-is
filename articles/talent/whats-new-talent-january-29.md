---
title: Nýjungar eða breytingar í Dynamics 365 Talent (31. janúar 2019)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
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
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690053"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="f7d5b-103">Nýjungar eða breytingar í Dynamics 365 Talent (31. janúar 2019)</span><span class="sxs-lookup"><span data-stu-id="f7d5b-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="f7d5b-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="f7d5b-105">**Smíði 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="f7d5b-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="f7d5b-106">Breytingar á Core HR</span><span class="sxs-lookup"><span data-stu-id="f7d5b-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="f7d5b-107">Frítími sem tekin er af leyfi tengiliðaspjalds tekur ekki tillit til dagsetninga leyfisáætlunar</span><span class="sxs-lookup"><span data-stu-id="f7d5b-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="f7d5b-108">Fyrir leyfisáætlanir sem ekki keyra ekki á almanaksári birtir **Tekið** spjaldið núna frítíma sem hefur verið tekinn á áætlanamiðuðu leyfisári.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-108">For leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="f7d5b-109">Til dæmis, ef leyfisár fyrirtækis er frá 1. júní til og með 30. maí og starfsmaður hefur tekið 3 daga í frí í desember, birtast 3 dagar þann 15. janúar á spjaldinu **Tekið**.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken three days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="f7d5b-110">Uppsafnaðar upphæðir passa ekki við lag dagsetningagrunns</span><span class="sxs-lookup"><span data-stu-id="f7d5b-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="f7d5b-111">Nýjum möguleikum hefur verið bætt við leyfi og fjarvistir (færibreyturnar **Mannauður**) til að gera viðskiptavinum kleift að ákvarða hvenær dagsetning fyrir starfsaldur starfsmanns í mánuðum tekur gildi.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="f7d5b-112">Fyrir sum fyrirtæki er dagsetningin í lok mánaðar, en fyrir önnur kann dagsetningin að vera við upphaf næsta mánaðar.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="f7d5b-113">Til dæmis getur eitt fyrirtæki veitt frítíma 31. desember á meðan annað fyrirtæki kann að veita frítíma 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="f7d5b-114">Þessi valkostur leyfir þér að velja hvenær umbunin á að eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="f7d5b-115">Aðgerðir starfsmannaráðningar eru fastar í stöðunni „Verkflæði lokið“.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="f7d5b-116">Breytingar hafa verið gerðar til að leiðrétta vandamál þar sem lítill fjöldi verkflæða kláraðist með stöðuna „Verkflæði lokið“.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="f7d5b-117">Ný verkflæði ætti nú að færa yfir í stöðuna „Lokið“ þegar verkflæðið klárast.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="f7d5b-118">Öll verkflæði með stöðuna lokið verða færð yfir í villustöðu til að leyfa uppfærslu og fjarlægingu ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f7d5b-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
