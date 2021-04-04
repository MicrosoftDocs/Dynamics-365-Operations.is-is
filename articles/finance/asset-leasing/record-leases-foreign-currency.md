---
title: Skrá leigusamninga í erlendum gjaldmiðlum
description: Þetta efnisatriði útskýrir hvernig á að skrá leigusamninga í gjaldmiðlum öðrum en bókhalds- eða skýrslugjaldmiðli.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fd4d04ae7e89b8ce41ed745c643b8e736484789d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241491"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="a97a9-103">Skrá leigusamninga í erlendum gjaldmiðlum</span><span class="sxs-lookup"><span data-stu-id="a97a9-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a97a9-104">Reikningar eignarleiga fyrir leigusamninga sem eru í gjaldmiðlum öðrum en bókhaldsgjaldmiðlinum eða skýrslugjaldmiðlinum eru stofnaðir á síðunni **Fjárhagsuppsetning**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="a97a9-105">Allir leigusamningar ættu að vera færðir inn í færslugjaldmiðil þeirra.</span><span class="sxs-lookup"><span data-stu-id="a97a9-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="a97a9-106">Með öðrum orðum ætti að færa þær inn í gjaldmiðlinum sem er tilgreindur í leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="a97a9-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="a97a9-107">Þetta efnisatriði útskýrir hvernig á að skrá leigusamninga í gjaldmiðlum öðrum en bókhalds- eða skýrslugjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="a97a9-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="a97a9-108">Ef verið er að færa inn leigusamning í erlendum gjaldmiðli er afnotaréttur af eign (ROU) afskrifaður bæði í bókhaldsgjaldmiðli og skýrslugjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="a97a9-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="a97a9-109">Þessir gjaldmiðlar eru skilgreindir á síðunni **Fjárhagsuppsetning**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="a97a9-110">Þessi hegðun er einnig notuð í eignum.</span><span class="sxs-lookup"><span data-stu-id="a97a9-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="a97a9-111">Þegar búið er að stofna leigusamning í erlendum gjaldmiðli skal velja færslugjaldmiðil í reitnum **Gjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="a97a9-112">Gengi bókhaldsgjaldmiðilsins er sjálfgefið gildi í reitnum **Bókhaldsgjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="a97a9-113">Gengi skýrslugjaldmiðils er sjálfgefið gildi í reitnum **Gengi skýrslugjaldmiðils**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="a97a9-114">Þessi gengi voru virk á upphafsdegi leigunnar.</span><span class="sxs-lookup"><span data-stu-id="a97a9-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="a97a9-115">Reitirnir **Gengi bókhaldsgjaldmiðils** og **Gengi skýrslugjaldmiðils** eru í flýtiflipanum **Upplýsingar um fjárhag og skýrslugjaldmiðil** á síðunni **Upplýsingar um leigu**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="a97a9-116">Veljið gátreitinn **Fast gengi** til að hnekkja genginu sem var fært inn sjálfkrafa og færið síðan inn nýja gengið.</span><span class="sxs-lookup"><span data-stu-id="a97a9-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="a97a9-117">Í öðrum reitum skal færa inn upplýsingar sem eru nauðsynlegar fyrir leiguna og síðan skal velja **Stofna áætlanir**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="a97a9-118">Á nýju síðunni **Upplýsingar um leigu** skal velja **Bækur**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="a97a9-119">Á síðunni **Leigubók** á flipanum **Upplýsingar um fjárhag og skýrslugjaldmiðil** skal staðfesta gildi reitanna **Bókhaldsgjaldmiðill upphaflegs afnotaréttar af eign** og **Skýrslugjaldmiðill afnotaréttar af eign**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="a97a9-120">Hver þessara reita sýnir stöðu afnotaréttar af eign í samsvarandi gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="a97a9-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="a97a9-121">Þessir reitir eru uppfærðir þegar fjárhagsupplýsingum er breytt.</span><span class="sxs-lookup"><span data-stu-id="a97a9-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="a97a9-122">Veljið **Stofna áætlanir** áður en greiðsluáætlun er staðfest.</span><span class="sxs-lookup"><span data-stu-id="a97a9-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="a97a9-123">Upphaflega bókarfærslan skráir afnotarétt af eign sem notar gengi gjaldmiðla sem er skráð á leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="a97a9-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="a97a9-124">Bókarfærslan inniheldur einnig gildi fyrir reitina **Bókhaldsgjaldmiðill upphaflegs afnotaréttar af eign** og **Skýrslugjaldmiðill upphaflegs afnotaréttar af eign**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="a97a9-125">Síðari mælingar fyrir leigusamninga í erlendum gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="a97a9-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="a97a9-126">Afskriftaráætlunin sýnir áætlaðar kostnaðarupphæðir afskrifta í skýrslugjaldmiðlinum, bókhaldsgjaldmiðlinum og færslugjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="a97a9-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="a97a9-127">Til að skoða stöðu afnotaréttar af eign og afskriftarupphæðir í annaðhvort skýrslugjaldmiðlinum eða bókhaldsgjaldmiðlinum skal opna **Afskriftaráætlun eignar** og velja gátreitinn **Sýna upphæðir bókhaldsgjaldmiðils** eða **Sýna skýrslugjaldmiðilsupphæðir**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="a97a9-128">Þegar stofnaðar eru kostnaðarfærslur afskrifta á móti leigusamningum sem eru gerðir upp í erlendum gjaldmiðli notar færslan gengið sem er skráð á leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="a97a9-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="a97a9-129">Þar eru einnig notuð gildi **bókhaldsgjaldmiðils upphaflegs afnotaréttar af eign** og **skýrslugjaldmiðils upphaflegs afnotaréttar af eign**.</span><span class="sxs-lookup"><span data-stu-id="a97a9-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="a97a9-130">Hægt er að reikna út heildarupphæð afskrifta með því að nota örlítið annað gengi, þannig að afnotaréttur af eign sé að fullu afskrifaður bæði í bókhaldsgjaldmiðlinum og skýrslugjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="a97a9-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="a97a9-131">Ef leigusamningurinn hefur verið endurflokkaður sem **Frestaðar leigugreiðslur** hreinsar kerfið sjálfkrafa gengi bókhalds-og skýrslugjaldmiðla, ef það hefur þegar verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="a97a9-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]