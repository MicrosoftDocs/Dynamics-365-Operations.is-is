---
title: Kröfur um vélbúnaðarþörf fyrir staðbundin umhverfi
description: Þetta efnisatriði tilgreinir kröfur um vélbúnaðarþörf fyrir staðbundin umhverfi.
author: sericks007
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 8fa644f35a086af99cde74fd6a2062f9b59a6ff7
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870265"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="dc2e6-103">Kröfur um vélbúnaðarþörf fyrir staðbundin umhverfi</span><span class="sxs-lookup"><span data-stu-id="dc2e6-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc2e6-104">Áður en byrjað er á ferlinu fyrir vélbúnaðar- og innviðaþörf fyrir staðbundið umhverfi skaltu kynna þér [Kerfiskröfur fyrir uppsetningu í skýi](system-requirements.md) og [Leiðbeiningar um uppsetningu og virkjun](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) til að fá góðan skilning á undirliggjandi innviðum.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements for cloud deployments](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="dc2e6-105">Hugaðu sérstaklega að bestu starfsvenjum kerfisuppsetningar fyrir hámarksafköst.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="dc2e6-106">Þegar þú hefur skoðað fylgiskjölin geturðu hafið það ferli að meta færslutengt og samtíma notandamagn og meta stærðarþörf umhverfisins þíns byggt á meðaltals kjarnaafköstum.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="dc2e6-107">Þættir sem hafa áhrif á stærðarþörf.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-107">Factors that affect sizing</span></span>

<span data-ttu-id="dc2e6-108">Allir þættir sem eru sýndir í eftirfarandi skýringarmynd hafa áhrif á stærðarþörf.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="dc2e6-109">Því ítarlegri upplýsinga sem er safnað, þeim mun nákvæmara er hægt að ákvarða stærðarþörf.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="dc2e6-110">Líklegt er að vélbúnaðarþörf, án stuðningsgagna, sé röng.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="dc2e6-111">Algjörar lágmarkskröfur fyrir nauðsynleg gögn eru hámarks millifærslulína hleðslu á klst.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="dc2e6-112">[![Vélbúnaðarþörf fyrir staðbundin umhverfi](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="dc2e6-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="dc2e6-113">Skoðað frá vinstri til hægri er fyrsti og mikilvægasti þátturinn sem þarf til að meta stærðarþörf nákvæmlega er færslusnið eða færsluframsetning.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="dc2e6-114">Mikilvægt er að finna alltaf hámarks færslumagn á hverja klukkustund.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="dc2e6-115">Ef það eru mörg hámarkstímabil þarf að skilgreina þessi tímabil nákvæmlega.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="dc2e6-116">Um leið og þú skilur álagið sem hefur áhrif á þína innviði þarftu líka að skilja þessa þætti betur:</span><span class="sxs-lookup"><span data-stu-id="dc2e6-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="dc2e6-117">**Færslur** - Venjulega hafa færslur ákveðna toppa yfir daginn/vikuna.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="dc2e6-118">Þetta fer aðallega eftir gerð færslunnar.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="dc2e6-119">Tíma- og kostnaðarfærslur sýna yfirleitt hámarkspunkta einu sinni í hverri viku viku, á meðan sölupantanafærslur koma oft margar saman með samþættingu eða jafnóðum inn yfir daginn.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="dc2e6-120">**Fjöldi samtíma notenda** – Fjöldi samtíma notenda er næstmikilvægasti þátturinn varðandi stærðarþörf.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="dc2e6-121">Þú getur ekki fengið ábyggilegt mat á stærðarþörf byggt á fjölda samtíma notenda, svo ef það eru einu gögnin sem þú hefur skaltu áætla fjöldann, og skoða þetta aftur þegar þú hefur meiri gögn.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="dc2e6-122">Nákvæm skilgreining á samtíma notendum þýðir að:</span><span class="sxs-lookup"><span data-stu-id="dc2e6-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="dc2e6-123">Nefndir notendur eru ekki samtíma notendur.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="dc2e6-124">Samtíma notendur eru alltaf hlutmengi nefndra notenda.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="dc2e6-125">Hámarksvinnuálag skilgreinir hámarks samvinnslu fyrir stærðarþörf.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="dc2e6-126">Skilyrði fyrir samtíma notendur er að notandinn uppfylli öll eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="dc2e6-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="dc2e6-127">Innskráður.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-127">Logged on.</span></span>
    - <span data-ttu-id="dc2e6-128">Vinnur í færslum/fyrirspurnum þegar talning fer fram.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="dc2e6-129">Ekki aðgerðalaus seta.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-129">Not an idle session.</span></span>

- <span data-ttu-id="dc2e6-130">**Gagnasamsetning** – Þetta snýst aðallega um hvernig kerfið þitt er uppsett og skilgreint.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="dc2e6-131">Til dæmis hve marga lögaðila þú hefur, hve mörg atriði, hve mörg uppskriftarstig, og hve flókið öryggiskerfið þitt er.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="dc2e6-132">Hver þessara þátta gæti haft lítil áhrif á afköst, svo hægt er að vega upp á móti þeim snjöllum ákvörðunum hvað varðar innviði.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="dc2e6-133">**Viðbætur** – Sérsnið geta verið einföld eða flókin.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="dc2e6-134">Fjöldi sérsniða og eðli flækjustigs og notkunar hefur mismunandi áhrif á stærð þeirra innviða sem þarf.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="dc2e6-135">Fyrir flóknar sérstillingar er ráðlagt að framkvæma afkastamat til að tryggja að þær séu ekki aðeins prófuð fyrir skilvirkni en einnig til að auka skilning á þörfum innviða.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="dc2e6-136">Þetta er enn mikilvægara þegar viðbætur eru ekki kóðaðar í samræmi við bestu venjur fyrir afköst og kvarðanleika.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="dc2e6-137">**Skýrslugerð og greiningar** – Þessir þættir fela yfirleitt í sér að keyra þungar fyrirspurnir við ýmsa gagnagrunna í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the system.</span></span> <span data-ttu-id="dc2e6-138">Skilningur á og lægri tíðni dýrra skýrslna hjálpar þér að skilja áhrif þeirra.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="dc2e6-139">**Lausnir þriðja aðila** – Þessar lausnir, eins og ISV-lausnir, hafa sömu áhrif og meðmæli og viðbætur.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-environment"></a><span data-ttu-id="dc2e6-140">Stærðir í umhverfinu</span><span class="sxs-lookup"><span data-stu-id="dc2e6-140">Sizing your environment</span></span>

<span data-ttu-id="dc2e6-141">Til að skilja stærðarkröfur þarftu að vita hámarksmagns færslna sem þú þarft að vinna úr.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="dc2e6-142">Flest aukakerfi, eins og Management Reporter eða SSRS, eru ekki eins nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="dc2e6-143">Vegna þess er að mestu einblínt á AOS og SQL Server í þessu skjali.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="dc2e6-144">Almennt víkka reikningslög út og þau ætti að setja upp sem N+1, sem þýðir að ef þrjú AOS eru áætluð er því fjórða bætt við.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="dc2e6-145">Gagnagrunnslagið ætti að vera sett upp sem Alltaf mjög tiltækt.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="dc2e6-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="dc2e6-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="dc2e6-147">Stærðir</span><span class="sxs-lookup"><span data-stu-id="dc2e6-147">Sizing</span></span>

- <span data-ttu-id="dc2e6-148">3000 til 15.000 færslulínur á klst. í hverjum kjarna í DB þjóni.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="dc2e6-149">Dæmigert AOS á móti SQL kjarnahlutfall 3:1 fyrir aðal SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="dc2e6-150">Aukakjarna gæti þurft byggt á valinni grunnstillingu fyrir mikinn tiltækileika.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="dc2e6-151">Vinnsla á aðgerðum sem setja mikið álag á gagnagrunna gæti minnkað þetta í 2:1.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="dc2e6-152">Eftirfarandi þættir hafa áhrif á tilbrigði:</span><span class="sxs-lookup"><span data-stu-id="dc2e6-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="dc2e6-153">Stillingar færibreyta í notkun.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="dc2e6-154">Stig viðbóta.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-154">Levels of extensions.</span></span>
    - <span data-ttu-id="dc2e6-155">Notkun viðbótarvirkni, eins og gagnagrunnsskrár og viðvarana.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="dc2e6-156">Mjög mikil gagnagrunnsskráning dregur enn frekar úr afköstum á klst. í hverjum kjarna undir 3000 línur.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="dc2e6-157">Flækjustig gagnasamsetningar – Einfaldur bókhaldslykill á móti ítarlegum bókhaldslykli hefur áhrif á afköst (svo dæmi sé tekið).</span><span class="sxs-lookup"><span data-stu-id="dc2e6-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="dc2e6-158">Framsetning færslu.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-158">Transaction characterization.</span></span>
    - <span data-ttu-id="dc2e6-159">2 GB til 16 GB minni fyrir hvern kjarna.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="dc2e6-160">Viðbótargagnagrunnar á DB þjóni eins og Management reporter og SSRS gagnagrunnar.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="dc2e6-161">Tímabundið DB = 15% af DB stærð með jafnmörgum skrár og efnislegir örgjörvar.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="dc2e6-162">SAN stærð og afköst byggð á heildarmagni/-notkun samtíma færslna.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="dc2e6-163">Mikill tiltækileiki</span><span class="sxs-lookup"><span data-stu-id="dc2e6-163">High availability</span></span>

<span data-ttu-id="dc2e6-164">Mælt er með að notast alltaf við SQL Server í annaðhvort klasa- eða speglunaruppsetningu.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="dc2e6-165">Annar SQL hnúturinn ætti að hafa sama fjölda kjarna og aðalhnúturinn.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="dc2e6-166">Active Directory samsteypuþjónusta (AD FS)</span><span class="sxs-lookup"><span data-stu-id="dc2e6-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="dc2e6-167">Fyrir AD FS stærðarþörf skal sjá [Fylgiskjöl fyrir afkastagetu þjóns AD FS](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span><span class="sxs-lookup"><span data-stu-id="dc2e6-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="dc2e6-168">[Stærðatöflureiknir](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) er í boði til að áætla fjölda tilvika í þinni virkjun.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-168">A [sizing spreadsheet](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="dc2e6-169">AOS (á netinu og runa)</span><span class="sxs-lookup"><span data-stu-id="dc2e6-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="dc2e6-170">Stærðir</span><span class="sxs-lookup"><span data-stu-id="dc2e6-170">Sizing</span></span>

- <span data-ttu-id="dc2e6-171">Stærðir eftir færslumagni/notkun</span><span class="sxs-lookup"><span data-stu-id="dc2e6-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="dc2e6-172">2000 til 6000 línur í kjarna</span><span class="sxs-lookup"><span data-stu-id="dc2e6-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="dc2e6-173">16 GB fyrir hvert tilvik</span><span class="sxs-lookup"><span data-stu-id="dc2e6-173">16 GB per instance</span></span>
    - <span data-ttu-id="dc2e6-174">Staðlaður kassi - 4 til 24 kjarnar</span><span class="sxs-lookup"><span data-stu-id="dc2e6-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="dc2e6-175">10 til 15 Enterprise notendur í hverjum kjarna</span><span class="sxs-lookup"><span data-stu-id="dc2e6-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="dc2e6-176">15 til 25 Activity notendur í hverjum kjarna</span><span class="sxs-lookup"><span data-stu-id="dc2e6-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="dc2e6-177">25 til 50 Hópmeðlimir í hverjum kjarna</span><span class="sxs-lookup"><span data-stu-id="dc2e6-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="dc2e6-178">Runa</span><span class="sxs-lookup"><span data-stu-id="dc2e6-178">Batch</span></span>

    - <span data-ttu-id="dc2e6-179">1 til 4 runuþræðir í hverjum kjarna</span><span class="sxs-lookup"><span data-stu-id="dc2e6-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="dc2e6-180">Stærð byggð á framsetningu runuglugga</span><span class="sxs-lookup"><span data-stu-id="dc2e6-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="dc2e6-181">Athugaðu að AOS, gagnastjórnun og runa eru á sama hlutverki í Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="dc2e6-182">Þú þarft að stækka fyrir þessi þrjú vinnuálög samanlagt og ekki aðgreina þau eins og í Microsoft Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="dc2e6-183">Sömu breytileikaþættir fyrir SQL þjóna eiga við hér.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="dc2e6-184">Mikill tiltækileiki</span><span class="sxs-lookup"><span data-stu-id="dc2e6-184">High availability</span></span>

- <span data-ttu-id="dc2e6-185">Gakktu úr skugga um að þú hafir að minnsta kosti 1 til 2 fleiri AOS tiltæka en þú telur þig þurfa.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="dc2e6-186">Gakktu úr skugga um að þú hafir að minnsta kosti 3 til 4 sýndarhýsla tiltæka.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="dc2e6-187">Management reporter</span><span class="sxs-lookup"><span data-stu-id="dc2e6-187">Management reporter</span></span>

<span data-ttu-id="dc2e6-188">Í flestum tilvikum, nema þegar notkun er mjög mikil, ættu lágmarkskröfur sem mælt er með þar sem tveir hnútar eru notaðir að virka vel.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="dc2e6-189">Aðeins í tilfellum þar sem nottkun er mikil þarf fleiri en tvo hnúta.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="dc2e6-190">Skalaðu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="dc2e6-191">SQL Server Reporting Services þjónn</span><span class="sxs-lookup"><span data-stu-id="dc2e6-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="dc2e6-192">Í almennri útgáfu er aðeins hægt að virkja einn SSRS hnút.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="dc2e6-193">Fylgstu með SSRS hnútnum þínum við prófun og fjölgaðu tiltækum kjörnum fyrir SSRS eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="dc2e6-194">Gakktu úr skugga um að þú hafir fyrirframgerðan aukahnút tiltækan á sýndarhýsli sem er öðruvísi en SSRS VM.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="dc2e6-195">Þetta er mikilvægt ef upp kemur vandamál með sýndarvél sem hýsir SSRS eða sýndarhýsilinn.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="dc2e6-196">Ef þetta er tilfellið þyrfti að skipta þeim út.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="dc2e6-197">Environment Orchestrator</span><span class="sxs-lookup"><span data-stu-id="dc2e6-197">Environment Orchestrator</span></span>

<span data-ttu-id="dc2e6-198">Orchestrator þjónustan er þjónustan sem hefur umsjón með þinni virkjun og tengdum samskiptum við LCS.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="dc2e6-199">Þessi þjónusta er notuð sem Service Fabric aðalþjónustua og krefst að minnsta kost þriggja VM.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="dc2e6-200">Þessi þjónusta er á sama stað og niðurröðunarþjónusta Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="dc2e6-201">Stærðin ætti að miðast við hámarksálag klasans.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="dc2e6-202">Nánari upplýsingar er að finna í [Skipuleggðu og undirbúðu virkjun á sjálfstæðum Service Fabric klasa](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span><span class="sxs-lookup"><span data-stu-id="dc2e6-202">For more information, see [Plan and prepare your Service Fabric Standalone cluster deployment](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="dc2e6-203">Sýndaruppsetning og ofáskrift</span><span class="sxs-lookup"><span data-stu-id="dc2e6-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="dc2e6-204">Mikilvæg þjónusta eins og AOS ætti að vera hýst á sýndarhýslum sem hafa sérstök tilföng til þess – kjarna, minni og disk.</span><span class="sxs-lookup"><span data-stu-id="dc2e6-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>
