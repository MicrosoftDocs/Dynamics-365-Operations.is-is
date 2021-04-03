---
title: Bæta við stuðningi fyrir efnisbirtingarnet (CDN)
description: Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582720"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="e8965-103">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="e8965-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8965-104">Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="e8965-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="e8965-105">Þegar búið er að setja upp rafrænt viðskiptaumhverfi í Dynamics 365 Commerce er hægt að skilgreina það til að vinna með CDN-þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="e8965-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="e8965-106">Hægt er að virkja sérsniðið lén meðan á úthlutunarferlinu stendur fyrir rafræna viðskiptaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="e8965-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="e8965-107">Einnig er hægt að nota þjónustubeiðni til að setja hana upp eftir að úthlutunarferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="e8965-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="e8965-108">Úthlutunarferlið fyrir rafræna viðskiptaumhverfið myndar hýsingarheiti sem er tengt við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="e8965-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="e8965-109">Þetta hýsilsheiti er með eftirfarandi sniði, þar sem \<*e-commerce-tenant-name*\> er heiti umhverfisins:</span><span class="sxs-lookup"><span data-stu-id="e8965-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="e8965-110">&lt;rafræn viðskipti-leigjanda-heiti&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="e8965-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="e8965-111">Hýsingarheiti eða endastöð sem er mynduð í úthlutunarferlinu styður aðeins SSL-skírteini (Secure Sockets Layer) fyrir \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="e8965-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="e8965-112">Það styður ekki SSL fyrir sérsniðin lén.</span><span class="sxs-lookup"><span data-stu-id="e8965-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="e8965-113">Þess vegna verður þú að segja upp SSL fyrir sérsniðin lén í CDN og framsenda umferð frá CDN til hýsingarheitsins eða endapunktsins sem Commerce myndaði.</span><span class="sxs-lookup"><span data-stu-id="e8965-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="e8965-114">Að auki er *tölfræðin* (JavaScript eða Cascading Style Sheets \[CSS\]-skrár) frá Commerce sýnd frá þeim endapunkti sem Commerce myndaði (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="e8965-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="e8965-115">Aðeins er hægt að afrita tölfræðina í skyndiminni ef hýsingarheiti eða endapunktur sem Commerce myndaði er sett á bak við CDN.</span><span class="sxs-lookup"><span data-stu-id="e8965-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="e8965-116">Setja upp SSL</span><span class="sxs-lookup"><span data-stu-id="e8965-116">Set up SSL</span></span>

<span data-ttu-id="e8965-117">Til að hjálpa til við að tryggja að SSL sé sett upp og að tölfræði sé vistuð í skyndiminni verður að stilla CDN þannig að það sé tengt við hýsingarheitið sem Commerce myndaði fyrir umhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="e8965-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="e8965-118">Þú verður einnig að vista eftirfarandi mynstur fyrir tölfræði í skyndiminni:</span><span class="sxs-lookup"><span data-stu-id="e8965-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="e8965-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="e8965-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="e8965-120">Eftir að þú hefur úthlutað Commerce-umhverfi þínu á sérsniðna lénið sem er veitt, eða eftir að þú hefur gefið sérsniðna lénið fyrir umhverfi þitt með því að nota þjónustubeiðni, skaltu beina sérsniðna léninu á hýsingarheitið eða endapunktinn sem Commerce myndaði.</span><span class="sxs-lookup"><span data-stu-id="e8965-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="e8965-121">Eins og áður var getið styður myndað hýsingarheiti eða endapunktur aðeins SSL-skírteini fyrir \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="e8965-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="e8965-122">Það styður ekki SSL fyrir sérsniðin lén.</span><span class="sxs-lookup"><span data-stu-id="e8965-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="e8965-123">CDN-þjónusta</span><span class="sxs-lookup"><span data-stu-id="e8965-123">CDN services</span></span>

<span data-ttu-id="e8965-124">Hægt er að nota hvaða CDN-þjónustu sem er með Commerce-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="e8965-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="e8965-125">Hér eru tvö dæmi:</span><span class="sxs-lookup"><span data-stu-id="e8965-125">Here are two examples:</span></span>

- <span data-ttu-id="e8965-126">**Microsoft Azure Útidyraþjónusta** - Azure CDN-lausnin.</span><span class="sxs-lookup"><span data-stu-id="e8965-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="e8965-127">Fyrir frekari upplýsingar um Azure útidyraþjónustu, sjá [Þjónustuskjöl Azure Front Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="e8965-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="e8965-128">**Akamai Dynamic Site Accelerator** - Sjá frekari upplýsingar í [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="e8965-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="e8965-129">Uppsetning CDN</span><span class="sxs-lookup"><span data-stu-id="e8965-129">CDN setup</span></span>

<span data-ttu-id="e8965-130">Uppsetningarferli CDN samanstendur af þessum almennu skrefum:</span><span class="sxs-lookup"><span data-stu-id="e8965-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="e8965-131">Bæta við framvinnsluhýsli.</span><span class="sxs-lookup"><span data-stu-id="e8965-131">Add a front-end host.</span></span>
1. <span data-ttu-id="e8965-132">Skilgreina bakvinnsluhóp.</span><span class="sxs-lookup"><span data-stu-id="e8965-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="e8965-133">Settu upp reglur fyrir beina og skyndiminni.</span><span class="sxs-lookup"><span data-stu-id="e8965-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="e8965-134">Bæta við framvinnsluhýsli</span><span class="sxs-lookup"><span data-stu-id="e8965-134">Add a front-end host</span></span>

<span data-ttu-id="e8965-135">Hægt er að nota hvaða CDN þjónustu sem er, en til dæmis í þessu efni er Azure Front Door Service notað.</span><span class="sxs-lookup"><span data-stu-id="e8965-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="e8965-136">Upplýsingar um hvernig á að setja upp Azure Front Door Service, sjá [Stuttur leiðarvísir: Búðu til útidyr fyrir víðfáanlegt altækt vefforrit](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="e8965-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="e8965-137">Skilgreina bakvinnsluhóp í Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="e8965-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="e8965-138">Til að skilgreina bakvinnsluhóp í Azure Front Door Service skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="e8965-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e8965-139">Bætið **&lt;ecom-leigjanda-heiti&gt;.commerce.dynamics.com** við bakvinnsluhóp sem sérsniðinn hýsil sem er með auðan haus bakvinnsluhýsils.</span><span class="sxs-lookup"><span data-stu-id="e8965-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="e8965-140">Undir **Álagsjöfnun** skaltu skilja eftir sjálfgefin gildi.</span><span class="sxs-lookup"><span data-stu-id="e8965-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="e8965-141">Eftirfarandi mynd sýnir svargluggann **Bæta við bakvinnslu** í Azure Front Door Service með hýsilheiti bakvinnslu slegið inn.</span><span class="sxs-lookup"><span data-stu-id="e8965-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Bæta við valmynd bakvinnslusafns](./media/CDN_BackendPool.png)

<span data-ttu-id="e8965-143">Eftirfarandi mynd sýnir svargluggann **Bæta við bakvinnslu** í Azure Front Door Service með sjálfgefin gildi álagsjöfnunar.</span><span class="sxs-lookup"><span data-stu-id="e8965-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Svarglugginn „Bæta við bakvinnslu“ heldur áfram](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="e8965-145">Settu upp reglur í Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="e8965-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="e8965-146">Fylgdu þessum skrefum til að setja upp beinareglu í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="e8965-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e8965-147">Bæta við beinareglu.</span><span class="sxs-lookup"><span data-stu-id="e8965-147">Add a routing rule.</span></span>
1. <span data-ttu-id="e8965-148">Í reitinn **Heiti** skal færa inn **sjálfgildi**.</span><span class="sxs-lookup"><span data-stu-id="e8965-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="e8965-149">Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="e8965-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="e8965-150">Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="e8965-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="e8965-151">Undir **Mynstur til að passa** skaltu slá inn efri reitinn **/\***.</span><span class="sxs-lookup"><span data-stu-id="e8965-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="e8965-152">Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="e8965-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="e8965-153">Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="e8965-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="e8965-154">Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**.</span><span class="sxs-lookup"><span data-stu-id="e8965-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="e8965-155">Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="e8965-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="e8965-156">Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="e8965-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="e8965-157">Fylgdu þessum skrefum til að setja upp biðminnisreglu í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="e8965-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e8965-158">Bæta við biðminnisreglu.</span><span class="sxs-lookup"><span data-stu-id="e8965-158">Add a caching rule.</span></span>
1. <span data-ttu-id="e8965-159">Í reitinn **Heiti** skal færa inn **tölfræði**.</span><span class="sxs-lookup"><span data-stu-id="e8965-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="e8965-160">Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="e8965-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="e8965-161">Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="e8965-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="e8965-162">Undir **Mynstur til að passa**, í efri reitnum, **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="e8965-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="e8965-163">Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="e8965-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="e8965-164">Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="e8965-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="e8965-165">Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**.</span><span class="sxs-lookup"><span data-stu-id="e8965-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="e8965-166">Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="e8965-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="e8965-167">Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="e8965-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="e8965-168">Í reitnum **Skyndiminnishegðun fyrirspurnstrengja** velurðu **Vista hverja einstaka vefslóð í skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="e8965-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="e8965-169">Í reitahópnum **Breytileg þjöppun** velurðu valkostinn **Virkt**.</span><span class="sxs-lookup"><span data-stu-id="e8965-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="e8965-170">Eftirfarandi mynd sýnir valmyndina **Bæta við reglu** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="e8965-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Bættu við regluglugga](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="e8965-172">Ef lénið sem notað verður er þegar virkt og komið í notkun skal stofna þjónustubeiðni úr reitnum **Stuðningur** í [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) til að fá aðstoð vegna næstu skrefa.</span><span class="sxs-lookup"><span data-stu-id="e8965-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="e8965-173">Frekari upplýsingar er að finna í [Fá stuðning fyrir Finance and Operations-forrit eða Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="e8965-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="e8965-174">Ef lénið er nýtt og er ekki lén sem þegar er komið í virka notkun, er hægt að bæta sérsniðna léninu við skilgreininguna fyrir Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="e8965-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="e8965-175">Þannig getur vefumferð beinst að vefsvæðinu í gegnum tilvik Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="e8965-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="e8965-176">Til að bæta við sérsniðna léninu (t.d. `www.fabrikam.com`), verður þú að stilla Canonical Name (CNAME) fyrir lénið.</span><span class="sxs-lookup"><span data-stu-id="e8965-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="e8965-177">Eftirfarandi mynd sýnir valmyndina **CNAME grunnstilling** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="e8965-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Valmyndin CNAME grunnstilling](./media/CNAME_Configuration.png)

<span data-ttu-id="e8965-179">Þú getur notað Azure Front Door Service til að stjórna skírteininu, eða þú getur notað þitt eigið skírteini fyrir sérsniðna lénið.</span><span class="sxs-lookup"><span data-stu-id="e8965-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="e8965-180">Eftirfarandi mynd sýnir valmyndina **Sérsniðin lén HTTPS** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="e8965-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Sérsniðin lén HTTPS valmynd](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="e8965-182">Ítarlegar leiðbeiningar um hvernig skuli bæta sérsniðnu léni við Azure Front Door er að finna í [Bæta sérsniðnu léni við Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="e8965-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="e8965-183">CDN ætti nú að vera rétt stillt þannig að það sé hægt að nota það með Commerce síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="e8965-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8965-184">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e8965-184">Additional resources</span></span>

[<span data-ttu-id="e8965-185">Valkostir innleiðingar á efnisbirtingarneti</span><span class="sxs-lookup"><span data-stu-id="e8965-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
