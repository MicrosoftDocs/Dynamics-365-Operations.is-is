---
title: Leiðrétt spá heimiluð
description: Ekki skal samþykkja öll spágögn strax. Þessi grein útskýrir hvernig hægt er að tilgreina tímabilið sem spá er heimiluð fyrir. Hún útskýrir líka hvernig á að heimila spá fyrir tiltekin fyrirtæki og spárlíkön.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de7384e94a4b97cf515bb437ad546a8a5f96aa77
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815227"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="a2cb7-105">Leiðrétt spá heimiluð</span><span class="sxs-lookup"><span data-stu-id="a2cb7-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2cb7-106">Ekki skal samþykkja öll spágögn strax.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="a2cb7-107">Þessi grein útskýrir hvernig hægt er að tilgreina tímabilið sem spá er heimiluð fyrir.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="a2cb7-108">Hún útskýrir líka hvernig á að heimila spá fyrir tiltekin fyrirtæki og spárlíkön.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="a2cb7-109">Ekki skal samþykkja öll spágögn strax.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="a2cb7-110">Hægt er að tilgreina upphafs- og dagsetningar tímabilsins sem spáin er heimiluð fyrir.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="a2cb7-111">Þessi aðgerð gerir það mögulegt að frysta tiltekna ramma.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="a2cb7-112">Upphafs- og lokadagsetningar sem eru tilgreindar verða að samsvara upphafs- og lokadagsetningum ramma sem spáin er mynduð í.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="a2cb7-113">Kerfið setur þessar takmarkanir og leiðréttir sjálfvirkt dagsetningar, ef leiðréttingar er þörf.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="a2cb7-114">Á flipanum **Upplýsingar** á síðunni **Heimild** er hægt að skoða upplýsingar um spána sem síðast var mynduð.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="a2cb7-115">Hægt er að velja þau fyrirtæki og nota spálíkön til að heimila spá fyrir.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="a2cb7-116">Sjálfgefið er að hnitanetið felur í sér öll þau fyrirtæki sem spáreftirspurn hefur verið stofnuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="a2cb7-117">Fyrir hvert fyrirtæki er spárlíkan sem samsvarar gildandi spáráætlun sem sett er upp í færibreytum aðalröðunar fyrirfram fyllt út fyrir hvert fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="a2cb7-118">Hins vegar er hægt að breyta þessu spárlíkani í hvaða spálíkan sem er sem tilheyrir því fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="a2cb7-119">Ef engin gögn um spáreftirspurn voru mynduð fyrir valið fyrirtæki mun viðvörunarboð berast á innflutningstíma.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="a2cb7-120">Mjög mikilvægt er að skilja hvernig gátreiturinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár** virkar.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="a2cb7-121">Ef gerð hafa verið handvirkar leiðréttingar á tölfræðilegri grunnlínuspá eru leiðrétt gildi heimil til notkunar, jafnvel þó að gátreiturinn sé hreinsaður.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="a2cb7-122">Hins vegar er breytingunum fleygt eftir heimildina.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="a2cb7-123">Þess vegna, næst þegar spá er mynduð er sú spá aðeins tölfræðileg spá og ekki með neinar handvirkar hnekkingar, jafnvel þótt **Flytja handvirkar leiðréttingar á eftirspurnarspánni** sé valinn.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="a2cb7-124">Þess vegna er hægt að líta á gátreitinn **Vista handvirkar leiðréttingar á grunnlínu eftirspurnarspár** sem ferli sem gerir kleift að halda eða henda öllum handvirkum breytingum.</span><span class="sxs-lookup"><span data-stu-id="a2cb7-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="a2cb7-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a2cb7-125">Additional resources</span></span>
--------

[<span data-ttu-id="a2cb7-126">Gera handvirkar leiðréttingar á grunnlínuspánni</span><span class="sxs-lookup"><span data-stu-id="a2cb7-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="a2cb7-127">Eftirlit með nákvæmni spár</span><span class="sxs-lookup"><span data-stu-id="a2cb7-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



