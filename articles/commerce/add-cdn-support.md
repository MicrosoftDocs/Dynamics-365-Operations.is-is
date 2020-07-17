---
title: Bæta við stuðningi fyrir efnisbirtingarnet (CDN)
description: Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: febef3bcc06dc1b5868a0decebee33d76110c505
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533345"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="dd150-103">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="dd150-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dd150-104">Þetta efnisatriði lýsir því hvernig á að bæta efnisbirtingarnet (CDN) við Microsoft Dynamics 365 Commerce umhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="dd150-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="dd150-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="dd150-105">Overview</span></span>

<span data-ttu-id="dd150-106">Þegar þú setur upp umhverfi rafrænna viðskipta í Dynamics 365 Commerce geturðu stillt það til að virka með CDN-þjónustunni.</span><span class="sxs-lookup"><span data-stu-id="dd150-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="dd150-107">Hægt er að virkja sérsniðið lén þitt í úthlutunarferlinu fyrir umhverfi þitt með rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="dd150-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="dd150-108">Einnig er hægt að nota þjónustubeiðni til að setja hana upp eftir að úthlutunarferlinu er lokið.</span><span class="sxs-lookup"><span data-stu-id="dd150-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="dd150-109">Úthlutunarferlið fyrir umhverfi rafrænna viðskipta býr til hýsingarheiti sem er tengt umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="dd150-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="dd150-110">Þetta hýsingarheiti er með eftirfarandi sniði, þar sem *rafræn viðskipti-leigjanda-heiti* er heiti umhverfisins:</span><span class="sxs-lookup"><span data-stu-id="dd150-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="dd150-111">&lt;rafræn viðskipti-leigjanda-heiti&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="dd150-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="dd150-112">Hýsingarheiti eða endastöð sem er mynduð í úthlutunarferlinu styður aðeins SSL-skírteini (Secure Sockets Layer) fyrir \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="dd150-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="dd150-113">Það styður ekki SSL fyrir sérsniðin lén.</span><span class="sxs-lookup"><span data-stu-id="dd150-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="dd150-114">Þess vegna verður þú að segja upp SSL fyrir sérsniðin lén í CDN og framsenda umferð frá CDN til hýsingarheitsins eða endapunktsins sem Commerce myndaði.</span><span class="sxs-lookup"><span data-stu-id="dd150-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="dd150-115">Að auki er *tölfræðin* (JavaScript eða Cascading Style Sheets \[CSS\]-skrár) frá Commerce sýnd frá þeim endapunkti sem Commerce myndaði (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="dd150-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="dd150-116">Aðeins er hægt að afrita tölfræðina í skyndiminni ef hýsingarheiti eða endapunktur sem Commerce myndaði er sett á bak við CDN.</span><span class="sxs-lookup"><span data-stu-id="dd150-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="dd150-117">Setja upp SSL</span><span class="sxs-lookup"><span data-stu-id="dd150-117">Set up SSL</span></span>

<span data-ttu-id="dd150-118">Til að hjálpa til við að tryggja að SSL sé sett upp og að tölfræði sé vistuð í skyndiminni verður að stilla CDN þannig að það sé tengt við hýsingarheitið sem Commerce myndaði fyrir umhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="dd150-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="dd150-119">Þú verður einnig að vista eftirfarandi mynstur fyrir tölfræði í skyndiminni:</span><span class="sxs-lookup"><span data-stu-id="dd150-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="dd150-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="dd150-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="dd150-121">Eftir að þú hefur úthlutað Commerce-umhverfi þínu á sérsniðna lénið sem er veitt, eða eftir að þú hefur gefið sérsniðna lénið fyrir umhverfi þitt með því að nota þjónustubeiðni, skaltu beina sérsniðna léninu á hýsingarheitið eða endapunktinn sem Commerce myndaði.</span><span class="sxs-lookup"><span data-stu-id="dd150-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="dd150-122">Eins og áður var getið styður myndað hýsingarheiti eða endapunktur aðeins SSL-skírteini fyrir \*.commerce.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="dd150-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="dd150-123">Það styður ekki SSL fyrir sérsniðin lén.</span><span class="sxs-lookup"><span data-stu-id="dd150-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="dd150-124">CDN-þjónusta</span><span class="sxs-lookup"><span data-stu-id="dd150-124">CDN services</span></span>

<span data-ttu-id="dd150-125">Hægt er að nota hvaða CDN-þjónustu sem er með Commerce-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="dd150-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="dd150-126">Hér eru tvö dæmi:</span><span class="sxs-lookup"><span data-stu-id="dd150-126">Here are two examples:</span></span>

- <span data-ttu-id="dd150-127">**Microsoft Azure Útidyraþjónusta** - Azure CDN-lausnin.</span><span class="sxs-lookup"><span data-stu-id="dd150-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="dd150-128">Fyrir frekari upplýsingar um Azure útidyraþjónustu, sjá [Þjónustuskjöl Azure Front Service](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="dd150-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="dd150-129">**Akamai Dynamic Site Accelerator** - Sjá frekari upplýsingar í [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="dd150-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="dd150-130">Uppsetning CDN</span><span class="sxs-lookup"><span data-stu-id="dd150-130">CDN setup</span></span>

<span data-ttu-id="dd150-131">Uppsetningarferli CDN samanstendur af þessum almennu skrefum:</span><span class="sxs-lookup"><span data-stu-id="dd150-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="dd150-132">Bæta við framvinnsluhýsli.</span><span class="sxs-lookup"><span data-stu-id="dd150-132">Add a front-end host.</span></span>
1. <span data-ttu-id="dd150-133">Stilltu bakvinnslusafn.</span><span class="sxs-lookup"><span data-stu-id="dd150-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="dd150-134">Settu upp reglur fyrir beina og skyndiminni.</span><span class="sxs-lookup"><span data-stu-id="dd150-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="dd150-135">Bæta við framvinnsluhýsli</span><span class="sxs-lookup"><span data-stu-id="dd150-135">Add a front-end host</span></span>

<span data-ttu-id="dd150-136">Hægt er að nota hvaða CDN þjónustu sem er, en til dæmis í þessu efni er Azure Front Door Service notað.</span><span class="sxs-lookup"><span data-stu-id="dd150-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="dd150-137">Upplýsingar um hvernig á að setja upp Azure Front Door Service, sjá [Stuttur leiðarvísir: Búðu til útidyr fyrir víðfáanlegt altækt vefforrit](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="dd150-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="dd150-138">Stilla bakvinnslusafn í Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="dd150-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="dd150-139">Til að stilla bakvinnslusafn í Azure Front Door Service skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="dd150-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="dd150-140">Bæta við **&lt;ecom-leigjandi-nafn&gt;.commerce.dynamics.com** í bakvinnslusafn sem sérsniðinn hýsil sem er með tóma fyrirsögn bakvinnsluhýsingar.</span><span class="sxs-lookup"><span data-stu-id="dd150-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="dd150-141">Undir **Heilbrigðiseftirlit**, í reitnum **Slóð**, skaltu slá inn **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="dd150-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="dd150-142">Í reitinn **Millibil (sekúndur)** skaltu slá inn **255**.</span><span class="sxs-lookup"><span data-stu-id="dd150-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="dd150-143">Undir **Álagsjöfnun** skaltu skilja eftir sjálfgefin gildi.</span><span class="sxs-lookup"><span data-stu-id="dd150-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="dd150-144">Eftirfarandi mynd sýnir valmyndina **Bæta við bavinnslusafni** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Bæta við valmynd bakvinnslusafns](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="dd150-146">Settu upp reglur í Azure Front Door Service</span><span class="sxs-lookup"><span data-stu-id="dd150-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="dd150-147">Fylgdu þessum skrefum til að setja upp beinareglu í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="dd150-148">Bæta við beinareglu.</span><span class="sxs-lookup"><span data-stu-id="dd150-148">Add a routing rule.</span></span>
1. <span data-ttu-id="dd150-149">Í reitinn **Heiti** skal færa inn **sjálfgildi**.</span><span class="sxs-lookup"><span data-stu-id="dd150-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="dd150-150">Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="dd150-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="dd150-151">Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="dd150-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="dd150-152">Undir **Mynstur til að passa** skaltu slá inn efri reitinn **/\***.</span><span class="sxs-lookup"><span data-stu-id="dd150-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="dd150-153">Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="dd150-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="dd150-154">Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="dd150-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="dd150-155">Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**.</span><span class="sxs-lookup"><span data-stu-id="dd150-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="dd150-156">Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="dd150-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="dd150-157">Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="dd150-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="dd150-158">Fylgdu þessum skrefum til að setja upp biðminnisreglu í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="dd150-159">Bæta við biðminnisreglu.</span><span class="sxs-lookup"><span data-stu-id="dd150-159">Add a caching rule.</span></span>
1. <span data-ttu-id="dd150-160">Í reitinn **Heiti** skal færa inn **tölfræði**.</span><span class="sxs-lookup"><span data-stu-id="dd150-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="dd150-161">Í reitnum **Samþykkt samskiptaregla** velurðu **HTTP og HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="dd150-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="dd150-162">Í reitnum **Framvinnsluhýslar** skaltu slá inn **dynamics-ecom-tenant-name.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="dd150-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="dd150-163">Undir **Mynstur til að passa**, í efri reitnum, **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="dd150-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="dd150-164">Undir **Upplýsingar um beini** stillirðu valkostinn **Gerð beinis** á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="dd150-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="dd150-165">Í reitnum **Bakvinnslusafn** velurðu **ecom-backend**.</span><span class="sxs-lookup"><span data-stu-id="dd150-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="dd150-166">Í reitahópnum **Samskiptareglur framsendingar** velurðu valkostinn **Jafna beiðni**.</span><span class="sxs-lookup"><span data-stu-id="dd150-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="dd150-167">Stilltu valkostinn **Umrita vefslóð** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="dd150-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="dd150-168">Stilltu valkostinn **Biðminnisvistun** á **Óvirkt**.</span><span class="sxs-lookup"><span data-stu-id="dd150-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="dd150-169">Í reitnum **Skyndiminnishegðun fyrirspurnstrengja** velurðu **Vista hverja einstaka vefslóð í skyndiminni**.</span><span class="sxs-lookup"><span data-stu-id="dd150-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="dd150-170">Í reitahópnum **Breytileg þjöppun** velurðu valkostinn **Virkt**.</span><span class="sxs-lookup"><span data-stu-id="dd150-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="dd150-171">Eftirfarandi mynd sýnir valmyndina **Bæta við reglu** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Bættu við regluglugga](./media/CDN_CachingRule.png)

<span data-ttu-id="dd150-173">Eftir að þessari upphafsstillingu hefur verið komið á, verður þú að bæta sérsniðna léninu við stillingarnar fyrir Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="dd150-174">Til að bæta við sérsniðna léninu (t.d. `www.fabrikam.com`), verður þú að stilla Canonical Name (CNAME) fyrir lénið.</span><span class="sxs-lookup"><span data-stu-id="dd150-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="dd150-175">Eftirfarandi mynd sýnir valmyndina **CNAME grunnstilling** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Valmyndin CNAME grunnstilling](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="dd150-177">Ef lénið sem þú munt nota er þegar virkt og lifandi, hafðu samband við stuðning til að virkja þetta lén með Azure Front Door Service til að setja upp próf.</span><span class="sxs-lookup"><span data-stu-id="dd150-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="dd150-178">Þú getur notað Azure Front Door Service til að stjórna skírteininu, eða þú getur notað þitt eigið skírteini fyrir sérsniðna lénið.</span><span class="sxs-lookup"><span data-stu-id="dd150-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="dd150-179">Eftirfarandi mynd sýnir valmyndina **Sérsniðin lén HTTPS** í Azure Front Door Service.</span><span class="sxs-lookup"><span data-stu-id="dd150-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Sérsniðin lén HTTPS valmynd](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="dd150-181">CDN ætti nú að vera rétt stillt þannig að það sé hægt að nota það með Commerce síðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="dd150-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd150-182">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dd150-182">Additional resources</span></span>

[<span data-ttu-id="dd150-183">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="dd150-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="dd150-184">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dd150-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="dd150-185">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dd150-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="dd150-186">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="dd150-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="dd150-187">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="dd150-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="dd150-188">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="dd150-188">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="dd150-189">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="dd150-189">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="dd150-190">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="dd150-190">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="dd150-191">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="dd150-191">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="dd150-192">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="dd150-192">Enable location-based store detection</span></span>](enable-store-detection.md)
