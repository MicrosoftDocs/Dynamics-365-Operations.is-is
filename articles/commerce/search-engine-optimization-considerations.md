---
title: Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt
description: Þetta efni nær yfir sjónarmið leitarvélabestun (SEO) fyrir síðuna þína frá þróun til framleiðslu.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 52a10c754315bfef2a01c593f5fa5366e9054982
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791800"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="1fe2e-103">Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt</span><span class="sxs-lookup"><span data-stu-id="1fe2e-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1fe2e-104">Þetta efni nær yfir sjónarmið leitarvélabestun (SEO) fyrir síðuna þína frá þróun til framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="1fe2e-105">Síða sem er í þróun</span><span class="sxs-lookup"><span data-stu-id="1fe2e-105">A site that is under development</span></span>

<span data-ttu-id="1fe2e-106">Þó að vefsvæði sé í þróun ættu allar vefsíður að vera með **NOINDEX** og **NOFOLLOW** lýsimerki, svo að leitarvélar skrái ekki síðurnar og geymi þróunarútgáfur af síðunni þinni í skyndiminni.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="1fe2e-107">Til að gera þessa stillingu verður þú að bæta við sjálfgefinni lýsimerkjaeiningu við sniðmát vefsíðunnar.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="1fe2e-108">Sjálfgefnir lýsimerkjaeiginleikar verða síðan aðgengilegir í SEO eiginleikahlutanum í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="1fe2e-109">Þú getur notað þessa eiginleika til að stjórna lýsimerkjunum.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="1fe2e-110">Óbundin ræsing svæðis</span><span class="sxs-lookup"><span data-stu-id="1fe2e-110">Soft launch of a site</span></span>

<span data-ttu-id="1fe2e-111">Við „óbundna ræsingu“ er vefsíða gerð aðgengileg fyrir takmarkaðan markhóp eða markað áður en full kynning fer fram.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="1fe2e-112">Ef þú setur óbundna ræsingu á vefsíðuna þína ættir þú að íhuga að hreyfa ekki við lýsimerkjunum **NOINDEX**.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="1fe2e-113">Á þennan hátt hjálpar þú til við að tryggja að óbundin ræsing sé áfram takmörkuð við þann takmarkaða markhóp sem þú vilt ná til.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="1fe2e-114">Vefsvæði sem er í framleiðslu</span><span class="sxs-lookup"><span data-stu-id="1fe2e-114">A site that is in production</span></span>

<span data-ttu-id="1fe2e-115">Þegar vefur er í framleiðslu ættirðu að ganga úr skugga um að allar vefsíðurnar séu réttar merktar.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="1fe2e-116">Microsoft Dynamics 365 Commerce notar upplýsingarnar sem eru færðar inn fyrir síðu til að mynda allar upplýsingar um leitarvélabestun á þeirri síðu.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="1fe2e-117">Eftirfarandi einingar veita þessa virkni: yfirlit yfir flokksíðu, yfirlit yfir listasíðu og yfirlit yfir vörusíðu.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="1fe2e-118">Til að hámarka flokkun leitarvéla notar flutningsramma báðar upplýsingar frá SEO eiginleikunum sem eru settir upp í Dynamics 365 Commerce og einingasértækar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="1fe2e-119">Fyrir vefsvæði sem er í framleiðslu, ættir þú að ganga úr skugga um að robots.txt skráin geri kleift að gera skrá yfir allt vefsvæðið og að hún innihaldi tengla á birt skjal svæðiskorts.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="1fe2e-120">Þú ættir að kveikja á myndunarvirkni svæðiskorts á **Svæðisstillingar \> Vefkort virkjuð**.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="1fe2e-121">Stillingar á síðu SEO fyrir innri forsýningu, takmarkaða markhóp og alla markhópa</span><span class="sxs-lookup"><span data-stu-id="1fe2e-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="1fe2e-122">Vegna þess að Dynamics 365 Commerce styður „það sem þú sérð er það sem þú færð“ sannvottaðar forskoðanir í sjónrænum vefsmið, höfundar geta undirbúið efni síðunnar þeirra án þess að þurfa að hafa áhyggjur af því að upplýsingarnar verða sýnilegar gestum svæðisins.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="1fe2e-123">Ef birta verður síðu en útsetning hennar verður að vera takmörkuð ætti hún að hafa lýsimerkið **NOINDEX**, svo að það verði ekki skráð af leitarvélum.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="1fe2e-124">Þegar síðan er tilbúin fyrir alla markhópa ættu öll grunnlýsigögn SEO að vera til staðar til að hámarka skilvirkni flokkunar leitarvéla.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="1fe2e-125">Að auki ætti að fjarlægja lýsimerkið **NOLIMIT**.</span><span class="sxs-lookup"><span data-stu-id="1fe2e-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fe2e-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1fe2e-126">Additional resources</span></span>

[<span data-ttu-id="1fe2e-127">Stjórna notendum og hlutverkum rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="1fe2e-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="1fe2e-128">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="1fe2e-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="1fe2e-129">Stjórna öryggisreglu fyrir efni (CSP)</span><span class="sxs-lookup"><span data-stu-id="1fe2e-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]