---
title: "Sýnishorn af rafrænni skýrslugerð ávísanir lánardrottins"
description: "Þetta efni inniheldur almennar upplýsingar um hvernig á að nota sýnishornasnið rafrænnar skýrslugerðar ávísana."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="3c26e-103">Sýnishorn af ávísanasniðum skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="3c26e-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="3c26e-104">Hægt er að nota rafræna skýrslugerð (ER) til að sníða ávísanir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="3c26e-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="3c26e-105">Mörg bankasértæk og ávísanaveitusértæk ávísunarsnið eru í boði á markaðnum.</span><span class="sxs-lookup"><span data-stu-id="3c26e-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="3c26e-106">Sýnishorn af ávísunarsniðum hafa verið höfð með í ávísanagreiðslulíkani í verkfæri geymslustaðurinn ER.</span><span class="sxs-lookup"><span data-stu-id="3c26e-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="3c26e-107">Þessi sýnishorn ávísana eru merkt **Ávísun í miðju (Bandaríkin)** og **Ávísun í efsta stubbi undir (Bandaríkin)**.</span><span class="sxs-lookup"><span data-stu-id="3c26e-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="3c26e-108">Hvað ávísanasnið eru studd eins og stendur?</span><span class="sxs-lookup"><span data-stu-id="3c26e-108">What check formats are currently supported?</span></span>

<span data-ttu-id="3c26e-109">Alltaf skal fara eignasafnið Samnýtt eign í Microsoft Dynamics Lifecycle services (LCS) og skoða núverandi lista yfir tiltækar skrár af eignargerðinni **GER-skilgreining**.</span><span class="sxs-lookup"><span data-stu-id="3c26e-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="3c26e-110">Næsti hluti „Hvað þarf að setja upp?“ veitir tengla í efnisatriði þar sem útskýrt er hvernig búa á til LCS-geymslu svo að hægt sé að fara yfir tiltækar stillingar og flytja inn valdar stillingar.</span><span class="sxs-lookup"><span data-stu-id="3c26e-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="3c26e-111">Microsoft Dynamics 365 til Fjármála og Aðgerðir Enterprise edition, inniheldur sýnishorn af sniði þar sem ávísunin er efst, með tvo kafla greiðslu.</span><span class="sxs-lookup"><span data-stu-id="3c26e-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="3c26e-112">Það felur líka í sér sýnishorn snið þar sem ávísun er í miðju, á milli tveggja greiðsluhluta.</span><span class="sxs-lookup"><span data-stu-id="3c26e-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="3c26e-113">Þessa sýnishornasnið samsvara ávísanasniðum Deluxe viðskipta.</span><span class="sxs-lookup"><span data-stu-id="3c26e-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="3c26e-114">Hvað þarf að setja upp?</span><span class="sxs-lookup"><span data-stu-id="3c26e-114">What do I have to set up?</span></span>

- <span data-ttu-id="3c26e-115">Áður en hægt er að prenta ávísanir með því að nota rafræna skýrslugerð verður a.m.k. ein virk skilgreining ávísunar flutt í stillingar á rafrænum skýrslum.</span><span class="sxs-lookup"><span data-stu-id="3c26e-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="3c26e-116">Hægt er að skoða leiðbeiningar í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)</span><span class="sxs-lookup"><span data-stu-id="3c26e-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="3c26e-117">Þegar stilltar eru ávísanir Lausafjár og stjórnun banka fyrir bankareikninginn skal velja gátreitinn **Almenn rafræn útflutningssnið** og velja síðan viðeigandi ávísunarsnið og útflutning skilgreiningarsniðið.</span><span class="sxs-lookup"><span data-stu-id="3c26e-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="3c26e-118">Einnig þarf að tilgreina fjölda innborgunarseðlalína sem verða prentaðar á greiðslu.</span><span class="sxs-lookup"><span data-stu-id="3c26e-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="3c26e-119">Gangið úr skugga um að taka með hausar raða þegar þessi tala er reiknuð út.</span><span class="sxs-lookup"><span data-stu-id="3c26e-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="3c26e-120">Fyrir tvö sýnishorn ávísunarsniða er ráðlagður línufjöldi fylgiseðils 17.</span><span class="sxs-lookup"><span data-stu-id="3c26e-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="3c26e-121">Hins vegar verður þessi tala breytileg eftir ávísunarbirgðum og prentarareklum.</span><span class="sxs-lookup"><span data-stu-id="3c26e-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="3c26e-122">Ráðlagt er að prenta ávísanaprufu til að villuleita útlit ávísunarinnar.</span><span class="sxs-lookup"><span data-stu-id="3c26e-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="3c26e-123">Til að prenta ávísanaprufu skal velja valkostinn **Prentprufa**.</span><span class="sxs-lookup"><span data-stu-id="3c26e-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="3c26e-124">Sýnishorn ávísanasniða virkar best þegar **Framlegð** er stillt á **Ekkert** í ítarlega prentara eiginleikar fyrir Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="3c26e-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="3c26e-125">Eftir að ávísunarprufan hefur verið mynduð gera breytingar á úttakið í Excel og skilgreina útliti síðu þannig að framlegð allra eru stilltir á **0** (núll).</span><span class="sxs-lookup"><span data-stu-id="3c26e-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="3c26e-126">Berðu saman ávísanaprufuna við ávísanabirgðirnar og lagaðu stillingarnar þangað til að þú ert ánægð(ur) með niðurröðina.</span><span class="sxs-lookup"><span data-stu-id="3c26e-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="3c26e-127">Þegar greiðslur eru myndaðar fyrir skilgreindan bankareikning í greiðslubók verða ávísanirnar prentaðar með sniði sem tilgreint er.</span><span class="sxs-lookup"><span data-stu-id="3c26e-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="3c26e-128">Nánari upplýsingar eru í [Breyta sniði rafrænnar skýrslugerðar](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="3c26e-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

