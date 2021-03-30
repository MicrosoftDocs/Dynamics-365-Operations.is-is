---
title: Stofna líkanastigveldi fyrir B2B-fyrirtæki
description: Í þessu efnisatriði er lýst hvernig á að stofna líkanastigveldi fyrirtækis fyrir B2B-fyrirtæki.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 91cb01637faa69bd3c7fefefae69c60cb948510e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211226"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="fcb03-103">Stofna líkanastigveldi fyrir B2B-fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="fcb03-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcb03-104">Í þessu efnisatriði er lýst hvernig á að stofna líkanastigveldi fyrirtækis fyrir B2B-fyrirtæki í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fcb03-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fcb03-105">Í Commerce Headquarters koma einingar viðskiptavina og viðskiptavinastigveldis fram fyrir hönd fyrirtækja viðskiptafélaga.</span><span class="sxs-lookup"><span data-stu-id="fcb03-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="fcb03-106">Fyrirtækið viðskiptafélaga og notendur þess koma fram sem viðskiptavinir og stigveldi viðskiptavina eru notuð til að tengja þessa viðskiptavini hvern við annan.</span><span class="sxs-lookup"><span data-stu-id="fcb03-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="fcb03-107">Þegar beiðni viðskiptafélagi um að tengjast B2B-svæði fyrir rafræn viðskipti er samþykkt eru eftirfarandi aðgerðir framkvæmdar:</span><span class="sxs-lookup"><span data-stu-id="fcb03-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="fcb03-108">Tvær nýjar viðskiptavinafærslur eru stofnaðar í kerfinu: Viðskiptavinafærsla af **Gerð: Fyrirtæki** fyrir fyrirtæki viðskiptafélaga og viðskiptavinafærsla af **Gerð: Einstaklingur** fyrir beiðandann (þ.e. notandi viðskiptafélaga sem sendi inn beiðnina).</span><span class="sxs-lookup"><span data-stu-id="fcb03-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="fcb03-109">Ný stigveldisfærsla viðskiptavinar er stofnuð undir **Viðskiptavinur \> Stigveldi viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="fcb03-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="fcb03-110">Þessi færsla er með eftirfarandi eiginleika í haus:</span><span class="sxs-lookup"><span data-stu-id="fcb03-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="fcb03-111">**Stigveldisauðkenni viðskiptavinar** – Einkvæmt kenni fyrir stigveldi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="fcb03-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="fcb03-112">Þetta kenni notar númeraröð sem er skilgreind í samnýttum viðskiptafæribreytum í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="fcb03-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="fcb03-113">**Heiti** – Fyrirtækisheiti viðskiptafélagans eins og það er tilgreint í innleiðingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="fcb03-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="fcb03-114">**Tilgangur** – Þessi eiginleiki er stilltur á fyrirframskilgreint gildi **B2B-fyrirtæki**.</span><span class="sxs-lookup"><span data-stu-id="fcb03-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="fcb03-115">**Fyrirtæki** – Viðskiptavinakenni viðskiptafélagans.</span><span class="sxs-lookup"><span data-stu-id="fcb03-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="fcb03-116">Hér eru upplýsingarnar um stigveldisfærslu viðskiptavinar:</span><span class="sxs-lookup"><span data-stu-id="fcb03-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="fcb03-117">Viðskiptavinafærsla beiðandans tengist stigveldi viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="fcb03-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="fcb03-118">Stjórnandahlutverkið tengist beiðandanum.</span><span class="sxs-lookup"><span data-stu-id="fcb03-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="fcb03-119">Þegar stjórnandinn bætir fleiri notendum við fyrirtæki viðskiptafélagans á B2B-svæðinu verður ný viðskiptavinafærsla stofnuð fyrir hvern notanda í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="fcb03-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="fcb03-120">Þessari viðskiptavinafærslu er einnig bætt við viðeigandi stigveldi viðskiptavinar fyrir viðskiptafélagann og er með hlutverk „notanda“.</span><span class="sxs-lookup"><span data-stu-id="fcb03-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="fcb03-121">Í flestum tilfellum ættu samsvarandi gildi eiginleika allra viðskiptavinafærslna í stigveldi að passa saman.</span><span class="sxs-lookup"><span data-stu-id="fcb03-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="fcb03-122">Sem dæmi, þar sem allir notendur viðskiptafélaga eiga að fá svipuð verð fyrir afurðir, ætti verðflokkur þeirra og tengdar skilgreiningar að passa saman.</span><span class="sxs-lookup"><span data-stu-id="fcb03-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="fcb03-123">Kerfið framfylgir samt sem áður ekki þessari samsvörun.</span><span class="sxs-lookup"><span data-stu-id="fcb03-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="fcb03-124">Þess vegna eru tilheyrandi notendur Commerce Headquarters ábyrgir fyrir því að tryggja að gildi eiginleika og skilgreiningar passi saman fyrir alla viðskiptavini í tilgreindu stigveldi.</span><span class="sxs-lookup"><span data-stu-id="fcb03-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="fcb03-125">Notendur Commerce Headquarters geta skoðað gildi eiginleikanna fyrir allar færslu viðskiptavina í stigveldinu í tvískiptu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="fcb03-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="fcb03-126">Veljið viðeigandi eiginleika viðskiptavinafærslu með því að velja flipaheitin í fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="fcb03-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="fcb03-127">Notendur geta skoðað og breytt eiginleikagildum í þessu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="fcb03-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="fcb03-128">Að öðrum kosti, ef á að nota öll gildin úr viðskiptavinafærslu stjórnanda í allar færslur viðskiptavina, skal velja **Hnekkja** í upplýsingum um stigveldi viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="fcb03-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcb03-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fcb03-129">Additional resources</span></span>

[<span data-ttu-id="fcb03-130">Setja upp B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="fcb03-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="fcb03-131">Stjórna notendum viðskiptafélaga á B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="fcb03-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="fcb03-132">Skilgreina greiðslumáta viðskiptavinalykils fyrir B2B-svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="fcb03-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="fcb03-133">Stilla takmörk afurðarmagns fyrir rafræn B2B-vefsvæði</span><span class="sxs-lookup"><span data-stu-id="fcb03-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]