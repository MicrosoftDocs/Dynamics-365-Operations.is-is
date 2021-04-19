---
title: Tafarlaus áfylling
description: Þetta efnisatriði lýsir því hvernig hægt er að nota tafarlausa áfyllingu til að fylla á birgðir þegar staðsetningarleiðbeining tekst ekki úthluta birgðum.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 006160a3f7eada95ebdcdbf6694ee54be439f349
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835655"
---
# <a name="immediate-replenishment"></a><span data-ttu-id="b5921-103">Tafarlaus áfylling</span><span class="sxs-lookup"><span data-stu-id="b5921-103">Immediate replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5921-104">Tafarlaus áfylling gerir þér kleift að fylla á birgðir strax eftir að lína staðsetningarleiðbeiningar tekst ekki að úthluta birgðum.</span><span class="sxs-lookup"><span data-stu-id="b5921-104">Immediate replenishment lets you replenish inventory immediately after a location directive line fails to allocate inventory.</span></span> <span data-ttu-id="b5921-105">Áfyllingin byggist á einni línu í uppsetningu staðsetningarleiðbeiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="b5921-105">The replenishment is based on a single line in the setup of the location directive.</span></span> <span data-ttu-id="b5921-106">Ef birgðir eru ekki á lager í mælieiningunni sem er tilgreind af þeirri línu, á sér stað áfylling á þessari mælieiningu þegar í stað.</span><span class="sxs-lookup"><span data-stu-id="b5921-106">If inventory isn't on hand in the unit of measure that is specified by that line, replenishment of that unit of measure occurs immediately.</span></span>

<span data-ttu-id="b5921-107">Tafarlaus áfylling býður upp á annan valkost við aðferðina þar sem úthlutun birgða byggist á fleiri línum í staðsetningarleiðbeiningunni og þar sem eftirspurnin er tekin saman við lok úthlutunarinnar og fyllt á í mælieiningunni sem tilgreind er af síðustu línunni í staðsetningarleiðbeiningunni.</span><span class="sxs-lookup"><span data-stu-id="b5921-107">Immediate replenishment provides an alternative to the method where the allocation of inventory is based on more lines in the location directive, and where the demand is summed at the end of the allocation and replenished in the unit of measure that is specified by the last line in the location directive.</span></span>

<span data-ttu-id="b5921-108">Ávinningur þess að nota tafarlausa áfyllingu er sá að hægt er að takmarka áfyllingu með sérstökum einingum og magnið er hægt að stjórna til tiltekinna staða.</span><span class="sxs-lookup"><span data-stu-id="b5921-108">The benefits of using immediate replenishment are that replenishment can be limited by specific units and the quantity can be directed to specific locations.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="b5921-109">Sviðsmynd fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="b5921-109">Business scenario</span></span>

<span data-ttu-id="b5921-110">Til dæmis ertu með vöruhús sem hefur aðskilin tiltektarsvæði fyrir „kassann“ og „hverja“ mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="b5921-110">For example, you have a warehouse that has separate picking areas for the "box" and "each" units of measure.</span></span> <span data-ttu-id="b5921-111">Þú vilt fínstilla tiltektarferlið með því að tína eins marga kassa og mögulegt er og síðan tína allt eftirstandandi magn sem er minna en kassi frá „hverju“ svæðinu.</span><span class="sxs-lookup"><span data-stu-id="b5921-111">You want to optimize the picking process by picking as many boxes as possible and then picking any remaining quantity that is less than a box from the "each" area.</span></span>

<span data-ttu-id="b5921-112">Í þessu tilviki er hægt að nota tafarlausa áfyllingu.</span><span class="sxs-lookup"><span data-stu-id="b5921-112">In this case, you can use immediate replenishment.</span></span> <span data-ttu-id="b5921-113">Í staðsetningarleiðbeiningunni er hægt að setja upp tafarlausa áfyllingu fyrir kassa svo eftirspurnaráfylling verði notuð um leið og skortur er á kössum sem hægt er að tína fyrir eftirspurnarmagnið.</span><span class="sxs-lookup"><span data-stu-id="b5921-113">In the location directive, you can set up immediate replenishment for boxes so that demand replenishment is used as soon as there is a shortage of boxes that can be picked for the demand quantity.</span></span> <span data-ttu-id="b5921-114">Með þessum hætti er tiltektarferlið fínstillt þannig að það tiltektin feli í sér eins marga kassa og mögulegt er.</span><span class="sxs-lookup"><span data-stu-id="b5921-114">In this way, you optimize the picking process so that picking includes as many boxes as possible.</span></span> <span data-ttu-id="b5921-115">Tafarlaus áfylling mun búa til áfyllingu á kössunum og eftirspurnin verður send áfram svo að magnið sé tínt í „hverri“ mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="b5921-115">Immediate replenishment will generate replenishment of the boxes, and the demand won't be passed on so that the quantities are picked in the "each" unit of measure.</span></span> <span data-ttu-id="b5921-116">Með öðrum orðum verður aðeins magnið sem á að tína í „hverri“ mælieiningu (það er magn sem er minna en kassi) verður valið úr „hverju“ svæðinu.</span><span class="sxs-lookup"><span data-stu-id="b5921-116">In other words, only the quantities that are supposed to be picked in the "each" unit of measure (that is, quantities that are less than a box) will be picked from the "each" area.</span></span> <span data-ttu-id="b5921-117">Ef skortur er á „kassa“svæðinu getur þú tínt eins marga kassa og mögulegt er af heildareftirspurninni.</span><span class="sxs-lookup"><span data-stu-id="b5921-117">If a shortage occurs in the "box" area, you can pick as many boxes as possible out of the total demand.</span></span> <span data-ttu-id="b5921-118">Eftirstandandi magn verður síðan tínt úr „hverju“ svæði.</span><span class="sxs-lookup"><span data-stu-id="b5921-118">The remaining quantities will then be picked from the "each" area.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="b5921-119">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="b5921-119">Where it applies</span></span>

<span data-ttu-id="b5921-120">Tafarlaus áfylling er notuð við bylgjukeyrslur ef úthlutun mistekst fyrir línu staðsetningarleiðbeiningar sem áfyllingarsniðmát er sett fyrir.</span><span class="sxs-lookup"><span data-stu-id="b5921-120">Immediate replenishment is used during wave execution if allocation fails for a location directive line that a replenishment template is set for.</span></span>

## <a name="set-up-immediate-replenishment"></a><span data-ttu-id="b5921-121">Setja upp tafarlausa áfyllingu</span><span class="sxs-lookup"><span data-stu-id="b5921-121">Set up immediate replenishment</span></span>

- <span data-ttu-id="b5921-122">Farðu í **Vöruhúsakerfi** \> **Uppsetning** \> **Staðsetningarleiðbeiningar** og síðan í flipanum **Línur** á listanum **Sniðmát tafarlausrar áfyllingar** skal velja áfyllingarsniðmát fyrir bylgjueftirspurn.</span><span class="sxs-lookup"><span data-stu-id="b5921-122">Go to **Warehouse management** \> **Setup** \> **Location directives**, and then, on the **Lines** tab, in the **Immediate replenishment template** list, select a replenishment template for wave demand.</span></span>

<span data-ttu-id="b5921-123">Áfyllingarsniðmátinu er beitt ef lína staðsetningarleiðbeiningar tekst ekki að úthluta sérstökum mælieiningum.</span><span class="sxs-lookup"><span data-stu-id="b5921-123">The replenishment template is applied if the location directive line fails to allocate a dedicated unit of measure.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b5921-124">Úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="b5921-124">Troubleshooting</span></span>

<span data-ttu-id="b5921-125">Ef tafarlaus áfylling er valin fyrir línu staðsetningarleiðbeiningar, en engin áfyllingarvinna er búin til þegar þú notar sniðmát eftirspurnaráfyllingar fyrir þá línu staðsetningarleiðbeiningar, verður að rannsaka tvær meginorsakir:</span><span class="sxs-lookup"><span data-stu-id="b5921-125">If immediate replenishment is selected for a location directive line, but no replenishment work is generated when you use demand replenishment templates for that location directive line, two main causes must be investigated:</span></span>

- <span data-ttu-id="b5921-126">Gakktu úr skugga um að sniðmát eftirspurnaráfyllingar sem er notað sé sett upp til að nota rétt staðsetningarsniðmát og vinnusniðmát af gerðinni **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="b5921-126">Make sure that the demand replenishment template that is applied is set up to use the correct location templates and work templates of the **Replenishment** type.</span></span>
- <span data-ttu-id="b5921-127">Gakktu úr skugga um að það sé nóg af birgðum á lager á þeirri staðsetningu sem sniðmát eftirspurnaráfyllingar leitar að birgðum á lager fyrir áfyllingu.</span><span class="sxs-lookup"><span data-stu-id="b5921-127">Make sure that there is enough on-hand inventory at the locations where the demand replenishment template searches for on-hand inventory for replenishment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]