---
title: Algengar spurningar fyrir Finance and Operations
description: "Þessi grein veitir svör við algengum spurningum um Microsoft Dynamics 365 for Finance and Operations-biðlarann."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 55d4fa4629d203aa888fe6400126a872d2eee000
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="finance-and-operations-client-faq"></a><span data-ttu-id="568b9-103">Algengar spurningar fyrir Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="568b9-103">Finance and Operations client FAQ</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="568b9-104">Þessi grein veitir svör við algengum spurningum um Microsoft Dynamics 365 for Finance and Operations-biðlarann.</span><span class="sxs-lookup"><span data-stu-id="568b9-104">This article provides answers to frequently asked questions about the Microsoft Dynamics 365 for Finance and Operations client.</span></span>

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a><span data-ttu-id="568b9-105">Hvers vegna er táknum ekki hlaðið þegar ég nota Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="568b9-105">Why aren't symbols loaded when I use Finance and Operations?</span></span>
-----------------------------------------------------------------

<span data-ttu-id="568b9-106">Öryggisstillingar í vafranum geta komið í veg fyrir að táknum sé hlaðið rétt.</span><span class="sxs-lookup"><span data-stu-id="568b9-106">The security settings on your browser might prevent the symbols from being loaded correctly.</span></span> <span data-ttu-id="568b9-107">Til að leysa þetta vandamál má reyna eitt af eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="568b9-107">To resolve this issue, try the following steps:</span></span>

-   <span data-ttu-id="568b9-108">Ef þetta vandamál kemur upp í Internet Explorer skal smella á **verkfæri** og síðan í smella á **Netvalkostir**.</span><span class="sxs-lookup"><span data-stu-id="568b9-108">If you're experiencing this issue in Internet Explorer, click **Tools**, and then click **Internet Options**.</span></span>  <span data-ttu-id="568b9-109">Á svarglugganum Netvalkostir, á **Persónuvernd** flipanum, er smellt á **Sérsniðið stig**, og ganga úr skugga um að valkosturinn **Leturgerðaniðurhal** sé valinn.</span><span class="sxs-lookup"><span data-stu-id="568b9-109">In the Internet Options dialog box, on the **Privacy** tab, click **Custom level**, and make sure the **Font download** option is selected.</span></span>
-   <span data-ttu-id="568b9-110">Annars gæti þurft að bæta Finance and Operations svæðinu við lista yfir traust svæði.</span><span class="sxs-lookup"><span data-stu-id="568b9-110">Otherwise, you might have to add the Finance and Operations site to the list of trusted sites.</span></span>

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a><span data-ttu-id="568b9-111">Ég sakna borðans úr Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="568b9-111">I miss the ribbon from Dynamics AX 2012.</span></span> <span data-ttu-id="568b9-112">Get ég haldið flipum Aðgerðarúðu opnum allar tímann?</span><span class="sxs-lookup"><span data-stu-id="568b9-112">Can I keep Action Pane tabs open all the time?</span></span>
<span data-ttu-id="568b9-113">Við ætlum að innleiða þessa aðgerð í fljótlega.</span><span class="sxs-lookup"><span data-stu-id="568b9-113">We are planning to implement this feature soon.</span></span> <span data-ttu-id="568b9-114">Notendur geta síðan valið að halda flipunum í Aðgerðarúðu alltaf opnum.</span><span class="sxs-lookup"><span data-stu-id="568b9-114">Users will then be able to choose to keep the tabs on Action Panes open all the time.</span></span> <span data-ttu-id="568b9-115">Annars verða fliparnir felldir saman þegar ekki er verið að nota þá, til að fá meira pláss á síðunni.</span><span class="sxs-lookup"><span data-stu-id="568b9-115">Otherwise, the tabs will be collapsed when they aren't being used, to gain more screen space for the page.</span></span>

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a><span data-ttu-id="568b9-116">Af hverju sé ég stundum aðrar flýtivalmyndir þegar ég hægrismelli?</span><span class="sxs-lookup"><span data-stu-id="568b9-116">Why do I sometimes see different shortcut menus when I rightclick?</span></span>
<span data-ttu-id="568b9-117">Ef hægrismellt er í breytanlegan reit (eða ef textinn er valinn), birtist flýtivalmynd vafra.</span><span class="sxs-lookup"><span data-stu-id="568b9-117">If you right-click in an editable field (or if text is selected), the browser's shortcut menu is displayed.</span></span> <span data-ttu-id="568b9-118">Þessi valmynd veitir aðgang að skipununum **Klippa**, **Afrit** og **Líma**.</span><span class="sxs-lookup"><span data-stu-id="568b9-118">This menu gives you access to the **Cut**, **Copy**, and **Paste** commands.</span></span> <span data-ttu-id="568b9-119">Ekki er hægt að fella þessar skipanir inn í flýtivalmyndir Finance and Operations þar sem vafrar leyfa ekki forritunaraðgang að klemmuspjaldi kerfisins af öryggisástæðum.</span><span class="sxs-lookup"><span data-stu-id="568b9-119">We can't embed these commands into the Finance and Operations shortcut menus because, for security reasons, browsers don’t allow us to programmatically access the system clipboard.</span></span>

<span data-ttu-id="568b9-120">Ef þú hægrismellir á reitamerki eða gildi skrifvarins eftirlits muntu sjá flýtivalmynd Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="568b9-120">If you right-click a field label or the value of a read-only control, you'll see the Finance and Operations shortcut menu.</span></span>

<span data-ttu-id="568b9-121">Til að auðvelda aðgang að lyklaborði ætlum við að innleiða flýtileiðir lyklaborðs í framtíðinni sem opnar flýtivalmynd Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="568b9-121">To make keyboard access easier, we plan to implement a keyboard shortcut in the future that will open the Finance and Operations shortcut menu.</span></span>

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a><span data-ttu-id="568b9-122">Hvar er virknin Skoða upplýsingar í Finance and Operations?</span><span class="sxs-lookup"><span data-stu-id="568b9-122">Where is the View details functionality in Finance and Operations?</span></span>
<span data-ttu-id="568b9-123">Valkosturinn **Skoða upplýsingar** er tiltækur á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="568b9-123">The **View details** option is available in a couple of ways:</span></span>

-   <span data-ttu-id="568b9-124">Ef stýring hefur getuna **Skoða upplýsingar** og hafi stýringin gildi er gildið birt sem tengill.</span><span class="sxs-lookup"><span data-stu-id="568b9-124">If a control has **View details** capabilities, and if the control has a value, that value is displayed as a hyperlink.</span></span> <span data-ttu-id="568b9-125">Hægt er að smella á tengillinn til að opna síðuna sem inniheldur viðbótarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="568b9-125">You can click the hyperlink to open a page that contains additional details.</span></span>
-   <span data-ttu-id="568b9-126">**Skoða upplýsingar** er einnig valkostur í flýtivalmynd Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="568b9-126">**View details** is also an option on Finance and Operations shortcut menus.</span></span> <span data-ttu-id="568b9-127">Nánari upplýsingar um hvenær flýtivalmyndir Finance and Operations birtast við hægrismell er að finna í fyrri hlutanum.</span><span class="sxs-lookup"><span data-stu-id="568b9-127">For more information about when Finance and Operations shortcut menus are displayed when you right-click, see the previous section.</span></span>





