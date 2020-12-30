---
title: Lén í Dynamics 365 Commerce
description: Þetta efnisatriði lýsir því hvernig lén eru afgreidd í Microsoft Dynamics 365 Commerce.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cb2b003168d32d05387bd45796d313736b11a41f
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517356"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="dc1b3-103">Lén í Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="dc1b3-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dc1b3-104">Þetta efnisatriði lýsir því hvernig lén eru afgreidd í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dc1b3-105">Lén eru vefföng sem eru notuð til að fara á Dynamics 365 Commerce-vefsvæði í netvafra.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="dc1b3-106">Þú sérð um stjórnun á léninu þínu með valdri DNS-veitu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="dc1b3-107">Vísað er í lén í gegnum Dynamics 365 Commerce-vefsmið til að samræma hvernig svæði verður opnað þegar það er birt.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="dc1b3-108">Þetta efnisatriði fer yfir hvernig lén eru meðhöndluð og vísað í gegnum feril þróunar og útgáfu Commerce-svæðis.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="dc1b3-109">Úthlutun og studd hýsilheiti</span><span class="sxs-lookup"><span data-stu-id="dc1b3-109">Provisioning and supported host names</span></span>

<span data-ttu-id="dc1b3-110">Þegar verið er að úthluta rafrænu viðskiptaumhverfi í [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), er kassinn **Studd lénsheiti** í úthlutunarskjámynd rafrænna viðskipta notaður til að færa inn lén sem munu tengjast uppsettu viðskiptaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-110">When provisioning an e-commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="dc1b3-111">Þessi lén verða DNS-heiti sem snúa að viðskiptavinum þar sem vefsvæði rafrænna viðskipta verða hýst.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-commerce websites will be hosted.</span></span> <span data-ttu-id="dc1b3-112">Að færa inn lén á þessu stigi setur ekki af stað umferð inn á lénið á Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="dc1b3-113">Umferð fyrir lén verður aðeins vísað á Commerce-endastöð þegar CNAME-færsla DNS er uppfærð til að nota Commerce-endastöðina með léninu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="dc1b3-114">Hægt er að færa mörg lén inn í kassann **Studd hýsilheiti** með því að aðskilja þau með semíkommu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="dc1b3-115">Eftirfarandi mynd sýnir úthlutunarskjámynd rafrænna viðskipta LCS með kassann **Studd lénsheiti** auðkenndan.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-115">The following illustration shows the LCS e-commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![Úthlutunarskjámynd rafrænna viðskipta LCS með kassann **Studd lénsheiti** auðkenndan](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="dc1b3-117">Hægt er að stofna þjónustubeiðni til að bæta öðrum lénum við umhverfi ef úthlutun hefur þegar átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="dc1b3-118">Til að stofna þjónustubeiðni í LCS skaltu í umhverfinu þínu fara í **Stuðningur \> Vandamál varðandi stuðning** og velja **Senda inn tilvik**.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="dc1b3-119">Vefslóðir myndaðar af Commerce</span><span class="sxs-lookup"><span data-stu-id="dc1b3-119">Commerce-generated URLs</span></span>

<span data-ttu-id="dc1b3-120">Þegar rafrænu Dynamics 365 Commerce viðskiptaumhverfi er úthlutað, býr Commerce til vefslóð sem verður vinnuveffangið fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-120">When provisioning a Dynamics 365 Commerce e-commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="dc1b3-121">Vísað er í þessa vefslóð í tengli á rafræna viðskiptasvæðið í LCS þegar búið er að úthluta umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-121">This URL is referenced in the e-commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="dc1b3-122">Vefslóð sem Commerce myndar er á sniðinu `https://<e-commerce tenant name>.commerce.dynamics.com`, þar sem biðlaraheiti rafrænna viðskipta er heitið sem fært er inn í LCS fyrir viðskiptaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-122">A Commerce-generated URL is in the format `https://<e-commerce tenant name>.commerce.dynamics.com`, where the e-commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="dc1b3-123">Einnig er hægt að nota hýsilheiti fyrir framleiðslusvæði í sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="dc1b3-124">Þessi möguleiki er tilvalinn þegar vefsvæði er afritað úr sandkassaumhverfi í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="dc1b3-125">Uppsetning svæðis</span><span class="sxs-lookup"><span data-stu-id="dc1b3-125">Site setup</span></span>

<span data-ttu-id="dc1b3-126">Þegar búið er að úthluta rafrænu viðskiptaumhverfi þarf að setja upp vefsvæðið í Commerce-vefsmið til að tengja vefsvæðið við virku vefslóðina.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-126">After your e-commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="dc1b3-127">Þegar fyrst er sett upp svæði í vefsmið birtist svarglugginn **Setja upp svæðið þitt**.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="dc1b3-128">Eftirfarandi mynd sýnir svargluggann **Setja upp svæðið þitt** fyrir svæði sem heitir „sjálfgefið“ þegar þú ferð inn á svæðið í fyrsta skipti í vefsmiðnum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![**Setja upp svæðið þitt** svargluggi](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="dc1b3-130">Glugginn **Velja lén** gerir þér kleift að tengja eitt af studdu hýsilheitunum, sem gefin er upp fyrir svæðið þitt í LCS, við svæðið þitt í vefsmiðnum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="dc1b3-131">Gluggann **Slóð** er hægt að skilja eftir auðan, eða bæta aukalegum streng við slóðina sem kemur fram í virku vefslóðinni þinni.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="dc1b3-132">Ef glugginn **Slóð** er skilinn eftir auður, tengir það grunnvefslóðina sem Commerce myndar við svæðið sem verið er að setja upp í vefsmiðnum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="dc1b3-133">Slóðir verða að vera einkvæmar fyrir hvert svæðis-/lénapar.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="dc1b3-134">Innan svæðis og léns sem valið er, getur aðeins eitt svæði í umhverfinu notað auðu slóðina eða verið tengt við einkvæman streng slóðar.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="dc1b3-135">Öllum strengjum sem bætt er við reitinn **Slóð** við uppsetningu svæðis verða undirslóðir grunnvefslóðar sem Commerce myndar og notaðar til að komast inn á svæðið í vafra.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="dc1b3-136">Slóðin er einnig þekkt sem **Samsvörun við slóð** þegar rás er bætt við skilgreiningarhlutann **Stillingar svæðis \> Rásir** í vefsmiðnum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="dc1b3-137">Ef þú ert til dæmis með svæði í vefsmiðnum sem heitir „fabrikam“ í biðlaraheiti rafrænna viðskipta „xyz“ og ef þú setur upp svæðið með auðri slóð, þá myndir þú opna birt efni vefsvæðisins í vafra með því að fara beint í grunnvefslóð sem Commerce býr til:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-137">For example, if you have a site in site builder called "fabrikam" in an e-commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="dc1b3-138">Að öðrum kosti, ef þú bættir við slóðinni „fabrikam“ við sömu uppsetningu vefsvæðisins, myndir þú opna birt efni vefsvæðisins í vafra með því að nota eftirfarandi vefslóð:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="dc1b3-139">Síður og vefslóðir</span><span class="sxs-lookup"><span data-stu-id="dc1b3-139">Pages and URLs</span></span>

<span data-ttu-id="dc1b3-140">Þegar búið er að setja upp svæðið með slóð, munu allar vefslóðir sem tengjast síðunum byggja ofan á virku vefslóðinni (Commerce-myndaða vefslóðin eða Commerce-myndaða vefslóðin ásamt slóðinni) fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="dc1b3-141">Að búa til nýja vefslóð í vefsmiðnum (**Vefslóðir /> +Nýtt**) með því að velja síðu í listanum í svarglugganum **Ný vefslóð** og færa inn vefslóðina fyrir þessa síðu mun tengja vefslóðina við völdu síðuna.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="dc1b3-142">Gildi vefslóðarinnar bætist þá við virka vefslóð svæðisins til að opna síðuna og er merkt sem `./<URL path>` í vefslóðarlistanum á síðunni **Vefslóðir** í vefsmiðnum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="dc1b3-143">Eftirfarandi mynd sýnir svargluggann **Ný vefslóð** í vefsmiðnum með auðkennt dæmi um vefslóð.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![**Ný vefslóð** svargluggi í vefsmið](./media/Domains_PageSetup2a.png)

<span data-ttu-id="dc1b3-145">Eftirfarandi mynd sýnir síðuna **Vefslóðir** í vefsmiðnum með auðkenndu dæmi um vefslóð í listanum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![Keyra valkost notendaflæðis í stefnuflæði](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="dc1b3-147">Lén í vefsmiðnum</span><span class="sxs-lookup"><span data-stu-id="dc1b3-147">Domains in site builder</span></span>

<span data-ttu-id="dc1b3-148">Gildi studdra hýsilheita eru í boði til að tengja sem lén þegar svæði er sett upp.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="dc1b3-149">Þegar gildi studds hýsilheitis er valið sem lénið, sérðu vísað í valið lén í gegnum vefsmiðinn.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="dc1b3-150">Þetta lén er aðeins tilvísun innan Commerce-umhverfisins, umferð í rauntíma fyrir þetta lén verður ekki framsent til Dynamics 365 Commerce sem stendur.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dc1b3-151">Þegar unnið er með svæði í vefsmið, ef þú ert með tvö svæði sett upp með tveimur mismunandi lénum, geturðu bætt eigindinni **?domain=** við virku vefslóðina til að opna efni birta vefsvæðisins í vafra.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="dc1b3-152">Til dæmis hefur umhverfi „xyz“ verið úthlutað og tvö svæði hafa verið búin til og tengd í vefsmiðnum: eitt með lénið `www.fabrikam.com` og hitt með lénið `www.constoso.com`.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="dc1b3-153">Hvort svæði var sett upp með auðri slóð.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="dc1b3-154">Síðan var hægt að komast inn á þessi svæði í vafra eins og meðfylgjandi með því að nota eigindina **?domain=**:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="dc1b3-155">Þegar fyrirspurnarstrengur léns er ekki gefinn í umhverfi með mörgum lénum, notar Commerce fyrsta lénið sem gefið er upp.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="dc1b3-156">Til dæmis, ef slóðin „fabrikam“ var gefin upp fyrst við uppsetningu vefsvæðið, væri hægt að nota vefslóðina `https://xyz.commerce.dynamics.com` til að opna efni birta vefsvæðisins fyrir `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="dc1b3-157">Framsend umferð í framleiðslu</span><span class="sxs-lookup"><span data-stu-id="dc1b3-157">Traffic forwarding in production</span></span>

<span data-ttu-id="dc1b3-158">Hægt er að líkja eftir mörgum lénum með því að nota færibreytur fyrir fyrirspurnarstreng léns á endastöð commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="dc1b3-159">En þegar nauðsynlegt er að fara í framleiðslu í rauntíma þarf að framsenda umferðina fyrir sérsniðna lénið á endastöðina `<e-commerce tenant name>.commerce.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="dc1b3-160">Endastöð `<e-commerce tenant name>.commerce.dynamics.com` styður ekki sérsniðin SSL og þarf því setja upp sérsniðin lén með því að nota Front Door-þjónustu eða efnisbirtingarnet (CDN).</span><span class="sxs-lookup"><span data-stu-id="dc1b3-160">The `<e-commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="dc1b3-161">Til að setja upp sérsniðin lén með því að nota Front Door-þjónustu eða CDN, eru tveir möguleikar í boði:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="dc1b3-162">Setjið upp Front Door-þjónustu á borð við Azure til að meðhöndla umferð framvinnslu og tengjast viðskiptaumhverfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="dc1b3-163">Þetta veitir meiri stjórn á léni og vottorðastjórnun og nákvæmari öryggisstefnur.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="dc1b3-164">Notið tilvik Azure Front Door sem Commerce útvegar.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="dc1b3-165">Þetta krefst þess að samhæfa aðgerð við Dynamics 365 Commerce-teymið fyrir sannprófun léns og að fá SSL-vottorð fyrir framleiðslulénið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="dc1b3-166">Frekari upplýsingar um hvernig setja á upp CDN-þjónustu beint má finna í [Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="dc1b3-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="dc1b3-167">Til að nota tilvik Azure Front Door sem Commerce útvegar, þarf að stofna þjónustubeiðni fyrir CDN-uppsetningaraðstoð úr innleiðingarteymi Commerce.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="dc1b3-168">Þú þarft að gefa upp heiti fyrirtækisins, framleiðslulénið, umhverfiskennið og biðlaraheiti rafrænna viðskipta framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-168">You will need to provide your company name, the production domain, environment ID, and production e-commerce tenant name.</span></span> 
- <span data-ttu-id="dc1b3-169">Þú þarft að staðfesta ef þetta er lén sem er til staðar (notað fyrir virkt vefsvæði) eða nýtt lén.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="dc1b3-170">Fyrir nýtt lén er hægt að ná í sannprófun á léni og SSL-vottorð í einu skrefi.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="dc1b3-171">Fyrir lén sem þjónar fyrirliggjandi vefsvæði, er ferli í mörgum skrefum nauðsynlegt til að framkvæma sannprófun léns og fá SSL-vottorð.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="dc1b3-172">Þetta ferli er með þjónustustigssamning sjö virkra daga til að gera lén virkt í rauntíma, því að í því felast mörg skref í ákveðinni röð.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="dc1b3-173">Til að stofna þjónustubeiðni í LCS skaltu í umhverfinu þínu fara í **Stuðningur \> Vandamál varðandi stuðning** og velja **Senda inn tilvik**.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="dc1b3-174">Sérsniðin lén með SSL eru aðeins studd í vinnsluumhverfum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="dc1b3-175">Fyrir önnur umhverfi en vinnsluumhverfi, t.d. sandkassa og samþykkisprófun notanda, skal nota vefslóðina sem Commerce myndar til að opna birt efni í vafra.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="dc1b3-176">Ferli SSL-vottorðs</span><span class="sxs-lookup"><span data-stu-id="dc1b3-176">SSL certificate process</span></span>

<span data-ttu-id="dc1b3-177">Þegar þjónustubeiðni er skráð, mun Commerce-teymið samræma eftirfarandi skref með þér.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="dc1b3-178">Fyrir ný lén:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-178">For new domains:</span></span>
- <span data-ttu-id="dc1b3-179">Commerce-teymið mun setja upp tilvik Azure Front Door (hýst af Commerce).</span><span class="sxs-lookup"><span data-stu-id="dc1b3-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="dc1b3-180">Commerce-teymið útvegar síðan CNAME-færsluna sem bendir á sérsniðna lénið þitt.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="dc1b3-181">Þegar CNAME-færslan hefur verið uppfærð, getur tilvik Azure Front Door sem Commerce hýsir sannprófað eignarhald lénsins og fengið SSL-vottorðið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="dc1b3-182">Fyrir núverandi/virk lén:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-182">For existing/active domains:</span></span>
- <span data-ttu-id="dc1b3-183">Commerce-teymið biður þig um að bæta við `afdverify.<custom-domain>`-CNAME-færslu sem DNS-veita lénsins á að fá.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="dc1b3-184">Þegar því er lokið bætir Commerce-teymið léninu við tilvik Azure Front Door og útvega frekari DNS TXT-færslur sem bæta á við DNS fyrir lénið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="dc1b3-185">Þegar TXT-færslunum er lokið, lýkur Commerce-teymið við uppfærslur Azure Front Door fyrir lénið sem mun setja upp SSL-vottorðið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="dc1b3-186">Apex-lén</span><span class="sxs-lookup"><span data-stu-id="dc1b3-186">Apex domains</span></span>

<span data-ttu-id="dc1b3-187">Tilvik Azure Front Door styður ekki apex-lén (rótarlén sem innihalda ekki undirlén).</span><span class="sxs-lookup"><span data-stu-id="dc1b3-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="dc1b3-188">Apex-lén þurfa IP-tölu til að leysa úr og tilvik Commerce Front Door er til með eingöngu sýndarendastöðvum.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="dc1b3-189">Til að nota apex-lén eru tveir möguleikar í boði:</span><span class="sxs-lookup"><span data-stu-id="dc1b3-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="dc1b3-190">**Valkostur 1** - Notið DNS-veitu til að framsenda apex-lénið á „www“ lén.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="dc1b3-191">Fabrikam.com framsendir til dæmis `www.fabrikam.com` þar sem `www.fabrikam.com` er CNAME-færslan sem bendir á tilvik Azure Front Door sem Commerce hýsir.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="dc1b3-192">**Valkostur 2** - Setjið upp CDN-/front door-tilvik á eigin spýtum til að hýsa apex-lénið.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="dc1b3-193">Ef verið er að nota Azure Front Door þarf einnig að setja upp Azure-DNS í sömu áskriftinni.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="dc1b3-194">Apex-lénið sem hýst er á Azure DNS getur bent á Azure Front Door sem samnefnd færsla.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="dc1b3-195">Þetta er eina hjáleiðin, þar sem apex-lén verða alltaf að benda á IP-tölu.</span><span class="sxs-lookup"><span data-stu-id="dc1b3-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="dc1b3-196">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dc1b3-196">Additional resources</span></span>

  [<span data-ttu-id="dc1b3-197">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="dc1b3-197">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="dc1b3-198">Setja upp netverslunarrás</span><span class="sxs-lookup"><span data-stu-id="dc1b3-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="dc1b3-199">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dc1b3-199">Create an e-commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="dc1b3-200">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="dc1b3-200">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="dc1b3-201">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="dc1b3-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="dc1b3-202">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="dc1b3-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="dc1b3-203">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="dc1b3-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="dc1b3-204">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="dc1b3-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="dc1b3-205">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="dc1b3-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="dc1b3-206">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="dc1b3-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="dc1b3-207">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="dc1b3-207">Enable location-based store detection</span></span>](enable-store-detection.md)
