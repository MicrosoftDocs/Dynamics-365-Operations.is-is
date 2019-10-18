---
title: Birta síður hlið við hlið með því að nota „Opna í nýjum glugga“-eiginleikann
description: Þessi grein útskýrir hvernig eigi að birta síður hlið við hlið.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180692"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a><span data-ttu-id="37815-103">Birta síður hlið við hlið með því að nota „Opna í nýjum glugga“-eiginleikann</span><span class="sxs-lookup"><span data-stu-id="37815-103">Show pages side by side by using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37815-104">Þessi grein útskýrir hvernig eigi að birta síður hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="37815-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="37815-105">Þú gætir viljað skoða margar síður hlið við hlið til að ljúka verkefnum hratt.</span><span class="sxs-lookup"><span data-stu-id="37815-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="37815-106">Sem dæmi, gæti verið óskað að villuleita eða færa inn línur í fleiri en einni færslubók.</span><span class="sxs-lookup"><span data-stu-id="37815-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="37815-107">Venjulega til að gera þetta þyrfti að fara fram og til baka milli síðunnar sem sýnir lista yfir færslubækur og síðuna sem sýnir línur í tiltekna færslubók.</span><span class="sxs-lookup"><span data-stu-id="37815-107">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="37815-108">Hins vegar **Opna í nýjum glugga** eiginleikinn gerir kleift að sýna þessar síður hlið við hlið þannig að hægt er að framkvæma verkefnunum fljótt.</span><span class="sxs-lookup"><span data-stu-id="37815-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="37815-109">Haldið er áfram með fyrrgreint dæmi hér fyrir ofan þegar verið er að skoða línurnar með því að smella á **Opna í nýjum glugga** tákn.</span><span class="sxs-lookup"><span data-stu-id="37815-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="37815-110">[![tákn til að opna í nýjum glugga](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="37815-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="37815-111">Smella á **Opna í nýjum glugga** táknið opnar línusíðuna í nýja, vafra sem sprettur upp og flettir síðan í upprunalega vafra til baka í sögunni á síðuna sem birti lista yfir færslubækur.</span><span class="sxs-lookup"><span data-stu-id="37815-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="37815-112">Hægt er að birta síðan báðar síðurnar hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="37815-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="37815-113">Þegar búið er að skoðuð færslubók er hægt að breyta valinni færslubók á listasíðu færslubókar, og línusíður í sprettiglugga birta sjálfkrafa línur í nýlega valinnar færslubókar.</span><span class="sxs-lookup"><span data-stu-id="37815-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="37815-114">[![síður birtast hlið við hlið](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="37815-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="37815-115">Gagnvirk tengingu og endurnýjun gerist vegna vensl sem eru til staðar á milli gagna sem hafa tekið Gert öryggisafrit af þessar síður.</span><span class="sxs-lookup"><span data-stu-id="37815-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="37815-116">Ef kerfið er ekki kunnugt um tengsl milli gagna, sprettiglugga mun ekki endurnýjast sjálfkrafa til að bregðast við breytingum í glugganum sem það er upprunnið frá.</span><span class="sxs-lookup"><span data-stu-id="37815-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="37815-117">Sumar síður eru með mörgum yfirlitum eins og hnitanetsyfirlit, hausyfirlit og upplýsingayfirlit.</span><span class="sxs-lookup"><span data-stu-id="37815-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="37815-118">**Opna í nýjum glugga** táknið veldur því að öll síðu opnast í nýjan vafraglugga.</span><span class="sxs-lookup"><span data-stu-id="37815-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="37815-119">Þess vegna er hægt að halda tvö yfirlit yfir sömu síðu hlið við hlið með því að nota **Opna í nýjum glugga** eiginleika.</span><span class="sxs-lookup"><span data-stu-id="37815-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="37815-120">Hins vegar nánast allar slíkar síður hafa flettingarlista sem þú getur notað til að skipta á milli skráa og ná fram svipaðri upplifun.</span><span class="sxs-lookup"><span data-stu-id="37815-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="37815-121">Áður en aðgerðin **Opna í nýjum glugga** er notuð ætti að skilgreina sprettigluggavörn vafrans til að leyfa sprettiglugga úr slóð svæðisins.</span><span class="sxs-lookup"><span data-stu-id="37815-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="37815-122">Sem dæmi, mætti heimila sprettiglugga úr "\*. dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="37815-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="37815-123">**Opna í nýjum glugga** eiginleiki er aðeins tiltækur þegar fleiri en einn síða er opna í glugganum.</span><span class="sxs-lookup"><span data-stu-id="37815-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="37815-124">Einnig sprettiglugga sjálfkrafa lokast þegar engar frekari síður eru opnar (þar er, þegar síðustu síðuna í glugganum er lokað).</span><span class="sxs-lookup"><span data-stu-id="37815-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="37815-125">Kerfið lokar einnig opnum síðum þegar farið er í mismunandi svæði í forritinu.</span><span class="sxs-lookup"><span data-stu-id="37815-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="37815-126">Þess vegna ef sprettuglugga eru opnir og farið er í annað svæði í forritinu, er sprettuglugga sjálfkrafa lokað því síðurnar í þeim gluggum var lokað af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="37815-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="37815-127">Efsta sláin í sprettiglugga birtir upplýsingar um fyrirtækið sem síðuna var opnuð í og er skrifvarin.</span><span class="sxs-lookup"><span data-stu-id="37815-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="37815-128">Sprettigluggar treysta einnig á aðalvafragluggann.</span><span class="sxs-lookup"><span data-stu-id="37815-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="37815-129">Ef aðalglugginn er lokaður eða endurnýjuð, allar opnar sprettuglugga mun verða eingöngu lesaðgangur.</span><span class="sxs-lookup"><span data-stu-id="37815-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="37815-130">Þetta þýðir að er hægt að skoða upplýsingarnar í þessum gluggum, en er ekki hægt að eiga samskipti við þá.</span><span class="sxs-lookup"><span data-stu-id="37815-130">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>
