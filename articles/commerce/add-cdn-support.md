---
title: Bæta við stuðningi fyrir efnisbirtingarnet (CDN)
description: Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a56f675b1fb43160625101a067c74e9fcf4f714a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797840"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="0ae9b-103">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="0ae9b-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0ae9b-104">Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="0ae9b-105">Þegar búið er að setja upp rafrænt viðskiptaumhverfi í Dynamics 365 Commerce er hægt að skilgreina það til að vinna með CDN-þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="0ae9b-106">Hægt er að virkja sérsniðið lén meðan á úthlutunarferlinu stendur fyrir rafræna viðskiptaumhverfið.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="0ae9b-107">Einnig er hægt að nota þjónustubeiðni til að setja hana upp eftir að úthlutunarferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="0ae9b-108">Úthlutunarferlið fyrir rafræna viðskiptaumhverfið myndar hýsingarheiti sem er tengt við umhverfið.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="0ae9b-109">Þetta hýsilsheiti er með eftirfarandi sniði, þar sem \<*e-commerce-tenant-name*\> er heiti umhverfisins:</span><span class="sxs-lookup"><span data-stu-id="0ae9b-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="0ae9b-110">&lt;rafræn viðskipti-leigjanda-heiti&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="0ae9b-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="0ae9b-111">Hýsingarheiti eða endastöð sem er mynduð í úthlutunarferlinu styður aðeins SSL-skírteini (Secure Sockets Layer) fyrir \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="0ae9b-112">Það styður ekki SSL fyrir sérsniðin lén.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="0ae9b-113">Þess vegna verður þú að segja upp SSL fyrir sérsniðin lén í CDN og framsenda umferð frá CDN til hýsingarheitsins eða endapunktsins sem Commerce myndaði.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="0ae9b-114">Að auki er *tölfræðin* (JavaScript eða Cascading Style Sheets \[CSS\]-skrár) frá Commerce sýnd frá þeim endapunkti sem Commerce myndaði (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="0ae9b-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="0ae9b-115">Aðeins er hægt að afrita tölfræðina í skyndiminni ef hýsingarheiti eða endapunktur sem Commerce myndaði er sett á bak við CDN.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="0ae9b-116">Setja upp SSL</span><span class="sxs-lookup"><span data-stu-id="0ae9b-116">Set up SSL</span></span>

<span data-ttu-id="0ae9b-117">Eftir að þú hefur úthlutað Commerce-umhverfi þínu á sérsniðna lénið sem er veitt, eða eftir að þú hefur gefið sérsniðna lénið fyrir umhverfi þitt með því að nota þjónustubeiðni, þarf að vinna með Commerce nýliðunarteyminu til að áætla DNS breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="0ae9b-118">Eins og áður var getið styður myndað hýsingarheiti eða endapunktur aðeins SSL-skírteini fyrir \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="0ae9b-119">Það styður ekki SSL fyrir sérsniðin lén.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="0ae9b-120">CDN-þjónusta</span><span class="sxs-lookup"><span data-stu-id="0ae9b-120">CDN services</span></span>

<span data-ttu-id="0ae9b-121">Hægt er að nota hvaða CDN-þjónustu sem er með Commerce-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="0ae9b-122">Hér eru tvö dæmi:</span><span class="sxs-lookup"><span data-stu-id="0ae9b-122">Here are two examples:</span></span>

- <span data-ttu-id="0ae9b-123">**Microsoft Azure Útidyraþjónusta** - Azure CDN-lausnin.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="0ae9b-124">Fyrir frekari upplýsingar um Azure útidyraþjónustu, sjá [Þjónustuskjöl Azure Front Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="0ae9b-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="0ae9b-125">**Akamai Dynamic Site Accelerator** - Sjá frekari upplýsingar í [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="0ae9b-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="0ae9b-126">Uppsetning CDN</span><span class="sxs-lookup"><span data-stu-id="0ae9b-126">CDN setup</span></span>

<span data-ttu-id="0ae9b-127">Uppsetningarferli CDN samanstendur af þessum almennu skrefum:</span><span class="sxs-lookup"><span data-stu-id="0ae9b-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="0ae9b-128">Bæta við framvinnsluhýsli.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-128">Add a front-end host.</span></span>
1. <span data-ttu-id="0ae9b-129">Skilgreina bakvinnsluhóp.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="0ae9b-130">Setja upp reglur fyrir leiðir.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="0ae9b-131">Bæta við framvinnsluhýsli</span><span class="sxs-lookup"><span data-stu-id="0ae9b-131">Add a front-end host</span></span>

<span data-ttu-id="0ae9b-132">Hægt er að nota hvaða CDN þjónustu sem er, en til dæmis í þessu efni er Azure Front Door Service notað.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="0ae9b-133">Upplýsingar um hvernig á að setja upp Azure Front Door Service, sjá [Stuttur leiðarvísir: Búðu til útidyr fyrir víðfáanlegt altækt vefforrit](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="0ae9b-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="0ae9b-134">Skilgreina bakvinnsluhóp í Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="0ae9b-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="0ae9b-135">Til að skilgreina bakvinnsluhóp í Azure Front Door Service skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="0ae9b-136">Bætið **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** við bakvinnsluhóp sem sérsniðinn hýsil sem er með bakvinnsluhaus sem er sá sami og **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="0ae9b-137">Undir **Álagsjöfnun** skaltu skilja eftir sjálfgefin gildi.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="0ae9b-138">Óvirkja ástandsskoðun fyrir bakvinnsluhóp.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="0ae9b-139">Eftirfarandi mynd sýnir svargluggann **Bæta við bakvinnslu** í Azure Front Door Service með hýsilheiti bakvinnslu slegið inn.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Bæta við valmynd bakvinnslusafns](./media/CDN_BackendPool.png)

<span data-ttu-id="0ae9b-141">Eftirfarandi mynd sýnir svargluggann **Bæta við bakvinnslu** í Azure Front Door Service með sjálfgefin gildi álagsjöfnunar.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Svarglugginn „Bæta við bakvinnslu“ heldur áfram](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="0ae9b-143">Gangið úr skugga um að **Heilbrigðiseftirlit** þegar eigin Azure Front Door Service er sett upp fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="0ae9b-144">Settu upp reglur í Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="0ae9b-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="0ae9b-145">Fylgdu þessum skrefum til að setja upp beinareglu í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="0ae9b-146">Bæta við beinareglu.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-146">Add a routing rule.</span></span>
1. <span data-ttu-id="0ae9b-147">Í reitinn **Heiti** skal færa inn **sjálfgildi**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="0ae9b-148">Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="0ae9b-149">Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="0ae9b-150">Undir **Mynstur til að passa** skaltu slá inn efri reitinn **/\***.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="0ae9b-151">Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="0ae9b-152">Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="0ae9b-153">Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="0ae9b-154">Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="0ae9b-155">Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="0ae9b-156">Ef lénið sem notað verður er þegar virkt og komið í notkun skal stofna þjónustubeiðni úr reitnum **Stuðningur** í [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) til að fá aðstoð vegna næstu skrefa.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="0ae9b-157">Frekari upplýsingar er að finna í [Fá stuðning fyrir Finance and Operations-forrit eða Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="0ae9b-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="0ae9b-158">Ef lénið er nýtt og er ekki lén sem þegar er komið í virka notkun, er hægt að bæta sérsniðna léninu við skilgreininguna fyrir Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="0ae9b-159">Þannig getur vefumferð beinst að vefsvæðinu í gegnum tilvik Azure Front Door.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="0ae9b-160">Til að bæta við sérsniðna léninu (t.d. `www.fabrikam.com`), verður þú að stilla Canonical Name (CNAME) fyrir lénið.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="0ae9b-161">Eftirfarandi mynd sýnir valmyndina **CNAME grunnstilling** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Valmyndin CNAME grunnstilling](./media/CNAME_Configuration.png)

<span data-ttu-id="0ae9b-163">Þú getur notað Azure Front Door Service til að stjórna skírteininu, eða þú getur notað þitt eigið skírteini fyrir sérsniðna lénið.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="0ae9b-164">Eftirfarandi mynd sýnir valmyndina **Sérsniðin lén HTTPS** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Sérsniðin lén HTTPS valmynd](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="0ae9b-166">Ítarlegar leiðbeiningar um hvernig skuli bæta sérsniðnu léni við Azure Front Door er að finna í [Bæta sérsniðnu léni við Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="0ae9b-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="0ae9b-167">CDN ætti nú að vera rétt stillt þannig að það sé hægt að nota það með Commerce síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="0ae9b-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ae9b-168">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0ae9b-168">Additional resources</span></span>

[<span data-ttu-id="0ae9b-169">Valkostir innleiðingar á efnisbirtingarneti</span><span class="sxs-lookup"><span data-stu-id="0ae9b-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
