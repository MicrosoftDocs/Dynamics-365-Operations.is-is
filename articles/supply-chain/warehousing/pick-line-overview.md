---
title: Setja upp valmyndaratriði fartækis til að birta yfirlit yfir val á línu
description: Þetta efnisatriði útskýrir hvernig á að skilgreina þegar listi yfir allar vinnulínur verður sýndur starfsmönnum vöruhúss sem eru að vinna úr vöruhúsavinnu í fartæki. Þessi möguleiki getur gagnast starfsmönnum vöruhúss sem þurfa oft að sjá yfirlit yfir tínslulínur í vinnupöntun þannig að þeir geti hagrætt tínsluröðinni.
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6eaba6da313f398c8d30f9a26c959ee971812e21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818873"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="bbdc4-104">Setja upp valmyndaratriði fartækis til að birta yfirlit yfir val á línu</span><span class="sxs-lookup"><span data-stu-id="bbdc4-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbdc4-105">Þetta efnisatriði útskýrir hvernig skilgreina á valkosti sem tengjast yfirliti tiltektarlínu fyrir valmyndaratriði fartækis sem eru notuð til að vinna úr tiltektarvinnu.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="bbdc4-106">Yfirlit tiltektarlínu gerir starfsmönnum vöruhúss kleift að skoða og velja úr lista yfir allar vinnulínur sem tengjast núverandi verki.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="bbdc4-107">Þessi möguleiki getur hjálpað starfsmönnum að hagræða tínsluröðinni.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="bbdc4-108">Þessi eiginleiki býður upp á valmöguleika sem koma í staðinn fyrir hefðbundna hnappinn **Sleppa** sem gerir starfsmönnum kleift að fara á milli línanna eina í einu í ákveðinni röð.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="bbdc4-109">(Hins vegar er valkosturinn til að nota þann hnapp enn tiltækur.)</span><span class="sxs-lookup"><span data-stu-id="bbdc4-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="bbdc4-110">Stjórnendur geta skilgreint hvert valmyndaratriði út af fyrir sig til að stjórna því hvernig, hvenær og hvar farsímaforrit vöruhúsakerfis sýnir yfirlit tínslulína.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-110">Admins can configure each menu item individually to control how, when, and where the Warehouse Management mobile app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="bbdc4-111">Kveikja á eiginleika fyrir yfirlit yfir tiltektarlínu vinnu</span><span class="sxs-lookup"><span data-stu-id="bbdc4-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="bbdc4-112">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="bbdc4-113">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="bbdc4-114">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="bbdc4-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="bbdc4-115">**Eining:** _Vöruhúsakerfi_</span><span class="sxs-lookup"><span data-stu-id="bbdc4-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="bbdc4-116">**Heiti eiginleika:** _Yfirlit yfir tiltektarlínu vinnu_</span><span class="sxs-lookup"><span data-stu-id="bbdc4-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="bbdc4-117">Skilgreina valmyndaratriði til að birta lista yfir allar vinnulínur</span><span class="sxs-lookup"><span data-stu-id="bbdc4-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="bbdc4-118">Til að setja upp valmyndaratriði fartækis til að birta yfirlit yfir tiltektarlínur skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="bbdc4-119">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="bbdc4-120">Veljið eða búið til valmyndaratriði sem tengist tiltektarvinnu og stillið eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="bbdc4-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="bbdc4-121">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="bbdc4-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="bbdc4-122">**Nota fyrirliggjandi vinnu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="bbdc4-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="bbdc4-123">**Stýrt af:** *Notandastýrt* eða *Kerfisstýrt*</span><span class="sxs-lookup"><span data-stu-id="bbdc4-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="bbdc4-124">Frekari upplýsingar um hvernig á að búa til valmyndaratriði og nota ýmsar stillingar sem eru í boði á síðunni **Valmyndaratriði fartækis** er að finna í [Setja upp fartæki fyrir vinnu vöruhúss](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="bbdc4-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="bbdc4-125">Í flýtiflipanum **Almennt** skal skilgreina eiginleikann með því að stilla reitinn **Sýna vinnulínulista** á eitt eftirfarandi gilda:</span><span class="sxs-lookup"><span data-stu-id="bbdc4-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="bbdc4-126">**Sýna aðeins við beiðni** – Starfsmenn geta valið að skoða tínslulínulista með því að velja hnappinn **Fara í** í farsímaforrit vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="bbdc4-127">**Sýna við upphaf hverrar tiltektar** – Starfsmenn sjá listann í hvert sinn sem þeir hefja eða ljúka tiltektarlínu.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="bbdc4-128">Einnig er hægt að skoða listann aftur með því að velja hnappinn **Fara í** í farsímaforriti vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-128">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="bbdc4-129">**Sýna eingöngu við upphaf fyrstu tiltektar** – Starfsmenn sjá listann í hvert sinn sem þeir hefja nýja tiltektarvinnu, en ekki eftir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="bbdc4-130">Einnig er hægt að skoða listann aftur með því að velja hnappinn **Fara í** í farsímaforriti vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-130">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="bbdc4-131">**Sýna aldrei** – Hefðbundni hnappurinn **Sleppa** birtist í farsímaforriti vöruhúsakerfis og slökkt er á skjámyndinni fyrir vinnulínulista.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-131">**Never show** – The standard **Skip** button appears in the Warehouse Management mobile app, and display of the work line list is turned off.</span></span> <span data-ttu-id="bbdc4-132">Hnappurinn **Sleppa** gerir starfsmönnum kleift að fara á milli línanna eina í einu í ákveðinni röð.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="bbdc4-133">Einnig er hægt að fara í gegnum listann eins oft og þarf til, þar til búið er að vinna úr öllum línum.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="bbdc4-134">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="bbdc4-135">Ef reiturinn **Sýna vinnulínulista** er stilltur á eitthvað gildi fyrir utan *Sýna aldrei* verður hnappurinn **Reitalisti** á aðgerðasvæðinu tiltækur.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="bbdc4-136">Veljið **Reitalisti** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="bbdc4-137">Á síðunni **Reitalisti** skal skilgreina upplýsingarnar sem farsímaforrit vöruhúsakerfis sýnir fyrir hverja línu í listanum.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-137">On the **Field list** page, configure the information that the Warehouse Management mobile app shows for each line in the list.</span></span>

    - <span data-ttu-id="bbdc4-138">Reiturinn **Aðalstýring** er alltaf stilltur á *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="bbdc4-139">Hver lína í listanum hefst þar af leiðandi á línunúmeri.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="bbdc4-140">Notið eftirstandandi reitina **Upplýsingasvæði** til að bæta við allt að sjö upplýsingasvæðum til viðbótar eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="bbdc4-141">Í reitnum **Upplýsingasvæði** skal velja heiti vinnulínureits.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="bbdc4-142">Hver lína sýnir svo gildi fyrir þann reit.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="bbdc4-143">Gildin verða sýnd í pöntuninni sem er valin hér.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="bbdc4-144">Hægt er að skilja nokkra af reitunum **Upplýsingasvæði** eftir auða ef ekki reynist þörf á öllum sjö gildunum.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="bbdc4-145">Á aðgerðasvæðinu skal velja **Vista** og síðan loka síðunni **Reitalisti**.</span><span class="sxs-lookup"><span data-stu-id="bbdc4-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]