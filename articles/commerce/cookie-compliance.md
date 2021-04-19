---
title: Kökusamræmi
description: Þetta efnisatriði lýsir atriðum fyrir reglufylgni fyrir kökur og sjálfgefnum reglum sem teknar eru með í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 08/31/2020
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
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796028"
---
# <a name="cookie-compliance"></a><span data-ttu-id="091cd-103">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="091cd-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="091cd-104">Þetta efnisatriði lýsir atriðum fyrir reglufylgni fyrir kökur og sjálfgefnum reglum sem teknar eru með í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="091cd-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="091cd-105">Persónuvernd er mikilvægur þáttur þegar rekja á tækni sem hefur áhrif á viðskiptavini rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="091cd-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="091cd-106">Vegna staðla um samræmi við friðhelgi einkalífs, svo sem Almennu persónuverndarreglugerðina (GDPR) í Evrópusambandinu (ESB), verður að hafa í huga rafræn viðmiðunarreglur varðandi friðhelgi einkalífs fyrir alla vefi sem eru virkir í dag.</span><span class="sxs-lookup"><span data-stu-id="091cd-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="091cd-107">Vegna þess að mörg svæði rafrænna viðskipta eru sjálfgefið aðgengileg á heimsvísu er mikilvægt að þú hafir farið yfir staðla viðmiðunar fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="091cd-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="091cd-108">Til að læra meira um grundvallarreglurnar sem Microsoft notar fyrir samræmi við vafrakökur skaltu fara á [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="091cd-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="091cd-109">Á þeirri síðu geturðu einnig fengið frekari upplýsingar um svæði þar sem farið er eftir lögum og persónuvernd.</span><span class="sxs-lookup"><span data-stu-id="091cd-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="091cd-110">Eftirfarandi tafla sýnir núverandi tilvísunarlista yfir smákökur settur inn af Dynamics 365 Commerce vefsvæðum.</span><span class="sxs-lookup"><span data-stu-id="091cd-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="091cd-111">Heiti köku</span><span class="sxs-lookup"><span data-stu-id="091cd-111">Cookie name</span></span>                               | <span data-ttu-id="091cd-112">Notkun</span><span class="sxs-lookup"><span data-stu-id="091cd-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="091cd-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="091cd-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="091cd-114">Geymið sannvottunarköku Microsoft Azure Active Directory (Azure AD) fyrir staka innskráningu (SSO).</span><span class="sxs-lookup"><span data-stu-id="091cd-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="091cd-115">Geymir dulkóðaðar aðalupplýsingar notanda (nafn, eftirnafn, netfang).</span><span class="sxs-lookup"><span data-stu-id="091cd-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="091cd-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="091cd-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="091cd-117">Geymið auðkenni körfu sem notað er til að sækja lista yfir vörur sem bætt er við körfutilvik.</span><span class="sxs-lookup"><span data-stu-id="091cd-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="091cd-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="091cd-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="091cd-119">Samþykktarrakning á reglufylgni köku.</span><span class="sxs-lookup"><span data-stu-id="091cd-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="091cd-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="091cd-120">ai_session</span></span>                                  | <span data-ttu-id="091cd-121">Greinir hversu margar lotur notandavirkni hafa tekið með ákveðnar síður og eiginleika forritsins.</span><span class="sxs-lookup"><span data-stu-id="091cd-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="091cd-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="091cd-122">ai_user</span></span>                                     | <span data-ttu-id="091cd-123">Greinir hversu margir notuðu forritið og eiginleika þess.</span><span class="sxs-lookup"><span data-stu-id="091cd-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="091cd-124">Notendur eru taldir með nafnlausum auðkennum.</span><span class="sxs-lookup"><span data-stu-id="091cd-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="091cd-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="091cd-125">b2cru</span></span>                                       | <span data-ttu-id="091cd-126">Geymir gagnvirkt framsenda vefslóð.</span><span class="sxs-lookup"><span data-stu-id="091cd-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="091cd-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="091cd-127">JSESSIONID</span></span>                                  | <span data-ttu-id="091cd-128">Notað af greiðslutengli Adyen til að vista notandalotu.</span><span class="sxs-lookup"><span data-stu-id="091cd-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="091cd-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="091cd-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="091cd-130">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="091cd-130">Authentication</span></span>                                               |
| <span data-ttu-id="091cd-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="091cd-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="091cd-132">Notað til að viðhalda stöðu beiðninnar.</span><span class="sxs-lookup"><span data-stu-id="091cd-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="091cd-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="091cd-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="091cd-134">Merki fyrirspurnafölsunar á milli svæða (CRSF) notað til að verjast CRSF.</span><span class="sxs-lookup"><span data-stu-id="091cd-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="091cd-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="091cd-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="091cd-136">Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar.</span><span class="sxs-lookup"><span data-stu-id="091cd-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="091cd-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="091cd-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="091cd-138">Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar.</span><span class="sxs-lookup"><span data-stu-id="091cd-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="091cd-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="091cd-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="091cd-140">Notað til að vísa beiðnum til viðeigandi þjónustutilviks framleiðslusannvottunar.</span><span class="sxs-lookup"><span data-stu-id="091cd-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="091cd-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="091cd-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="091cd-142">Notað til að viðhalda SSO-lotunni.</span><span class="sxs-lookup"><span data-stu-id="091cd-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="091cd-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="091cd-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="091cd-144">Notað til að rekja færslur (fjöldi opinna flipa sem sannvottar vefsvæði viðskipta við neytanda (B2C)), þar með talið núverandi færslu.</span><span class="sxs-lookup"><span data-stu-id="091cd-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="091cd-145">Samþykki fyrir kökur á svæði notanda á vefsvæði e-Commerce</span><span class="sxs-lookup"><span data-stu-id="091cd-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="091cd-146">Ef eiginleiki einingu rafrænna viðskipta notar köku sem ekki er nauðsynleg þarf að sækja samþykki notanda áður en kakan er rakin.</span><span class="sxs-lookup"><span data-stu-id="091cd-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="091cd-147">Til að leyfa notendum vefsvæðis að veita samþykki fyrir kökur á svæði rafrænna viðskipta verður höfundur síðu að bæta við og grunnstilla samþykkiseining köku í hauseiningu síðu til að tryggja að beðið sé um samþykki og það móttekið.</span><span class="sxs-lookup"><span data-stu-id="091cd-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="091cd-148">Gefa þarf notendasamþykki vefsvæðis áður en hægt er að nota eiginleika eða einingu án nauðsynlegrar köku á síðu svæðis.</span><span class="sxs-lookup"><span data-stu-id="091cd-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="091cd-149">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="091cd-149">Additional resources</span></span>

[<span data-ttu-id="091cd-150">Aðgengiseiginleikar og -geta</span><span class="sxs-lookup"><span data-stu-id="091cd-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="091cd-151">Yfirlit yfir reglufylgni</span><span class="sxs-lookup"><span data-stu-id="091cd-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="091cd-152">Bæta við persónuverndarstefnusíðu</span><span class="sxs-lookup"><span data-stu-id="091cd-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="091cd-153">Skipta um notandakenni sem tengjast röktum efnisbreytingum</span><span class="sxs-lookup"><span data-stu-id="091cd-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="091cd-154">Eining kökusamþykkis</span><span class="sxs-lookup"><span data-stu-id="091cd-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="091cd-155">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="091cd-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
