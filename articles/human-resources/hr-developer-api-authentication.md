---
title: Sannvottun
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 025feca31eed8649bc319a1e1a1b6d1af3ddb128
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009460"
---
# <a name="authentication"></a><span data-ttu-id="ad57f-102">Sannvottun</span><span class="sxs-lookup"><span data-stu-id="ad57f-102">Authentication</span></span>

<span data-ttu-id="ad57f-103">Þessi grein veitir yfirlitsupplýsingar um hvernig eigi að auðkenna Microsoft Dynamics 365 Human Resources forritunarviðmót gagnaforrits (API).</span><span class="sxs-lookup"><span data-stu-id="ad57f-103">This article provides overview information about how to authenticate with the Microsoft Dynamics 365 Human Resources data application programming interface (API).</span></span>

## <a name="overview"></a><span data-ttu-id="ad57f-104">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ad57f-104">Overview</span></span>

<span data-ttu-id="ad57f-105">Gögn API fyrir Human Resources er innleiðing OData.</span><span class="sxs-lookup"><span data-stu-id="ad57f-105">The data API for Human Resources is an OData implementation.</span></span> <span data-ttu-id="ad57f-106">Nánari upplýsingar er að finna í [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span><span class="sxs-lookup"><span data-stu-id="ad57f-106">For more information, see [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).</span></span>

<span data-ttu-id="ad57f-107">Forritið þitt verður að staðfesta sem viðurkenndur kallari áður en API mun þjónusta beiðnir úr forritinu.</span><span class="sxs-lookup"><span data-stu-id="ad57f-107">Your application must authenticate as an authorized caller before the API will service requests from your application.</span></span>

## <a name="fundamentals"></a><span data-ttu-id="ad57f-108">Undirstöðuatriði</span><span class="sxs-lookup"><span data-stu-id="ad57f-108">Fundamentals</span></span>

<span data-ttu-id="ad57f-109">Til að kalla í gagnaforritið verður forritið að fá aðgangsmerki frá Microsoft kennivettvangi.</span><span class="sxs-lookup"><span data-stu-id="ad57f-109">To call the data API, your application must acquire an access token from the Microsoft identity platform.</span></span> <span data-ttu-id="ad57f-110">Aðgangstáknið inniheldur upplýsingar um forritið þitt og leyfið sem það þarf til að hringja í úrræði í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ad57f-110">The access token contains information about your application and the permission that it has to call resources in Human Resources.</span></span>

### <a name="access-token"></a><span data-ttu-id="ad57f-111">Aðgangsmerki</span><span class="sxs-lookup"><span data-stu-id="ad57f-111">Access token</span></span>

<span data-ttu-id="ad57f-112">Aðgangstákn sem gefin eru út af Microsoft auðkenningarpallinum eru base64-kóðuð JavaScript Object Notation (JSON) Web Tokens (JWTs).</span><span class="sxs-lookup"><span data-stu-id="ad57f-112">Access tokens issued by the Microsoft identity platform are base64–encoded JavaScript Object Notation (JSON) Web Tokens (JWTs).</span></span> <span data-ttu-id="ad57f-113">Þau innihalda upplýsingar (fullyrðingar) sem gögnaskil API (og önnur forritaskil á vefnum sem eru tryggð af Microsoft kennivettvangi) nota til að staðfesta kallara og ganga úr skugga um að kallari hafi réttar heimildir til að framkvæma aðgerðina sem hann óskar eftir.</span><span class="sxs-lookup"><span data-stu-id="ad57f-113">They contain information (claims) that the data API (and other web APIs that are secured by the Microsoft identity platform) use to validate the caller and make sure that the caller has the correct permissions to perform the operation they're requesting.</span></span> <span data-ttu-id="ad57f-114">Meðan á símtölum stendur geturðu meðhöndlað aðgangsmerki sem ógegnsætt.</span><span class="sxs-lookup"><span data-stu-id="ad57f-114">During calls, you can treat access tokens as opaque.</span></span> <span data-ttu-id="ad57f-115">Þú ættir alltaf að senda aðgangsmerki yfir örugga rás, svo sem Transport Layer Security (TLS) og Hypertext Transfer Protocol Secure (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="ad57f-115">You should always transmit access tokens over a secure channel, such as Transport Layer Security (TLS) and Hypertext Transfer Protocol Secure (HTTPS).</span></span>

<span data-ttu-id="ad57f-116">Hér er dæmi um aðgangsmerki sem er gefið út af Microsoft kennivettvangi.</span><span class="sxs-lookup"><span data-stu-id="ad57f-116">Here is an example of an access token that is issued by the Microsoft identity platform.</span></span>

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

<span data-ttu-id="ad57f-117">Til að kalla í gagnaforritið festirðu aðgangstáknið sem handhafa auðkenni við heimildarhaus í HTTP beiðninni þinni.</span><span class="sxs-lookup"><span data-stu-id="ad57f-117">To call the data API, you attach the access token as a bearer token to the authorization header in your HTTP request.</span></span> <span data-ttu-id="ad57f-118">Eftirfarandi er dæmi.</span><span class="sxs-lookup"><span data-stu-id="ad57f-118">Here is an example.</span></span>

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a><span data-ttu-id="ad57f-119">Skráðu nýtt forrit með Azure-gáttinni</span><span class="sxs-lookup"><span data-stu-id="ad57f-119">Register a new application by using the Azure portal</span></span>

1. <span data-ttu-id="ad57f-120">Skráðu þig inn á [Microsoft Azure vefsíðunni](https://portal.azure.com) með vinnu- eða skólareikningi, eða persónulegum Microsoft reikningi.</span><span class="sxs-lookup"><span data-stu-id="ad57f-120">Sign in to the [Microsoft Azure portal](https://portal.azure.com) with a work or school account, or a personal Microsoft account.</span></span>

2. <span data-ttu-id="ad57f-121">Ef reikningurinn þinn veitir þér aðgang að fleiri en einum leigjanda skaltu velja reikninginn þinn í efra hægra horninu og stilla vefgáttina á Azure Active Directory (Azure AD) leigjandi sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="ad57f-121">If your account gives you access to more than one tenant, select your account in the upper-right corner, and set your portal session to the Azure Active Directory (Azure AD) tenant that you want.</span></span>

3. <span data-ttu-id="ad57f-122">Veldu vinstri gluggann **Azure Active Directory** þjónustu og veldu síðan **Forritaskráningar \> Ný skráning**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-122">In the left pane, select the **Azure Active Directory** service, and then select **App registrations \> New registration**.</span></span>

4. <span data-ttu-id="ad57f-123">Þegar **Skrá forrit** síðan birtist skaltu slá inn skráningarupplýsingar forritsins:</span><span class="sxs-lookup"><span data-stu-id="ad57f-123">When the **Register an application** page appears, enter your application's registration information:</span></span>

    - <span data-ttu-id="ad57f-124">**Heiti**: Sláðu inn þýðingarmikið heiti forrits sem verður sýnt notendum forritsins.</span><span class="sxs-lookup"><span data-stu-id="ad57f-124">**Name**: Enter a meaningful application name that will be shown to users of the app.</span></span>
    - <span data-ttu-id="ad57f-125">**Studdar tegundir reikninga**: Veldu tegundir reikninga sem forritið þitt ætti að styðja.</span><span class="sxs-lookup"><span data-stu-id="ad57f-125">**Supported account types**: Select the types of accounts that your app should support.</span></span>

        | <span data-ttu-id="ad57f-126">Studdar reikningsgerðir</span><span class="sxs-lookup"><span data-stu-id="ad57f-126">Supported account types</span></span> | <span data-ttu-id="ad57f-127">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ad57f-127">Description</span></span> |
        |-------------------------|-------------|
        | <span data-ttu-id="ad57f-128">Reikningar í þessari skipulagaskrá eingöngu</span><span class="sxs-lookup"><span data-stu-id="ad57f-128">Accounts in this organizational directory only</span></span> | <span data-ttu-id="ad57f-129">Veldu þennan valkost ef þú ert að byggja upp atvinnugreinaforrit.</span><span class="sxs-lookup"><span data-stu-id="ad57f-129">Select this option if you're building a line-of-business app.</span></span> <span data-ttu-id="ad57f-130">Þessi valkostur er ekki tiltækur nema þú sért að skrá forritið í möppu.</span><span class="sxs-lookup"><span data-stu-id="ad57f-130">This option isn't available unless you're registering the app in a directory.</span></span><p><span data-ttu-id="ad57f-131">Þessi möguleiki er kortlagður **Azure AD aðeins einn leigjandi**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-131">This option is mapped to **Azure AD only single-tenant**.</span></span></p><p><span data-ttu-id="ad57f-132">Þessi valkostur er sjálfgefinn valkostur nema þú sért að skrá forritið utan möppu.</span><span class="sxs-lookup"><span data-stu-id="ad57f-132">This option is the default option unless you're registering the app outside a directory.</span></span> <span data-ttu-id="ad57f-133">Í því tilfelli er sjálfgefinn valkostur **Azure AD margra leigjenda og persónulegra Microsoft reikninga**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-133">In that case, the default option is **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p> |
        | <span data-ttu-id="ad57f-134">Reikningar í þessari skipulagaskrá</span><span class="sxs-lookup"><span data-stu-id="ad57f-134">Accounts in any organizational directory</span></span> | <span data-ttu-id="ad57f-135">Veldu þennan valkost til að miða á alla viðskiptavini fyrirtækja og mennta.</span><span class="sxs-lookup"><span data-stu-id="ad57f-135">Select this option to target all business and educational customers.</span></span><p><span data-ttu-id="ad57f-136">Þessi möguleiki er kortlagður **Azure AD aðeins margir leigjendur**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-136">This option is mapped to **Azure AD only multi-tenant**.</span></span></p><p><span data-ttu-id="ad57f-137">Ef þú skráðir forritið sem **Azure AD aðeins einn leigjandi**, þú getur notað **Auðkenning** blað til að uppfæra það til **Azure AD aðeins fjöl leigjandi** og síðan aftur til **Azure AD aðeins einn leigjandi**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-137">If you registered the app as **Azure AD only single-tenant**, you can use the **Authentication** blade to update it to **Azure AD only multi-tenant** and then back to **Azure AD only single-tenant**.</span></span></p> |
        | <span data-ttu-id="ad57f-138">Reikningar í hvaða skipulagsskrá og persónulegum Microsoft reikningum</span><span class="sxs-lookup"><span data-stu-id="ad57f-138">Accounts in any organizational directory and personal Microsoft accounts</span></span> | <span data-ttu-id="ad57f-139">Veldu þennan valkost til að miða á breiðasta hóp viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="ad57f-139">Select this option to target the widest set of customers.</span></span><p><span data-ttu-id="ad57f-140">Þessum valkosti er varpað á **Azure AD margra leigjenda og persónulegra Microsoft reikninga**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-140">This option is mapped to **Azure AD multi-tenant and personal Microsoft accounts**.</span></span></p><p><span data-ttu-id="ad57f-141">Ef þú skráðir forritið sem **Azure AD margra leigjenda og persónulegra Microsoft reikninga**, þú getur ekki breytt þessari stillingu í notendaviðmóti (UI).</span><span class="sxs-lookup"><span data-stu-id="ad57f-141">If you registered the app as **Azure AD multi-tenant and personal Microsoft accounts**, you can't change this setting in the user interface (UI).</span></span> <span data-ttu-id="ad57f-142">Í staðinn verður þú að nota ritstjóra forritsins til að breyta studdum tegundum reikninga.</span><span class="sxs-lookup"><span data-stu-id="ad57f-142">Instead, you must use the application manifest editor to change the supported account types.</span></span></p> |

    - <span data-ttu-id="ad57f-143">**Beina URI (valfrjálst)** - Veldu gerð forritsins sem þú ert að byggja: **vefur** eða **Opinber viðskiptavinur (farsími og skrifborð)**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-143">**Redirect URI (optional)** – Select the type of app that you're building: **Web** or **Public client (mobile & desktop)**.</span></span> <span data-ttu-id="ad57f-144">Sláðu síðan inn beina URI (eða svara URL) fyrir forritið.</span><span class="sxs-lookup"><span data-stu-id="ad57f-144">Then enter the redirect URI (or reply URL) for the app.</span></span>

        - <span data-ttu-id="ad57f-145">Fyrir vefforrit, gefðu grunnslóð forritsins.</span><span class="sxs-lookup"><span data-stu-id="ad57f-145">For web apps, provide the base URL of the app.</span></span> <span data-ttu-id="ad57f-146">Til dæmis, `http://localhost:31544` gæti verið slóðin fyrir vefforrit sem keyrir á vélinni þinni.</span><span class="sxs-lookup"><span data-stu-id="ad57f-146">For example, `http://localhost:31544` might be the URL for a web app that runs on your local machine.</span></span> <span data-ttu-id="ad57f-147">Notendur nota síðan þessa slóð til að skrá sig inn á forrit á vefbiðlara.</span><span class="sxs-lookup"><span data-stu-id="ad57f-147">Users then use this URL to sign in to a web client app.</span></span>
        - <span data-ttu-id="ad57f-148">Gefðu URI það fyrir opinbera viðskiptavini Azure AD notar til að skila svarbréfum.</span><span class="sxs-lookup"><span data-stu-id="ad57f-148">For public client apps, provide the URI that Azure AD uses to return token responses.</span></span> <span data-ttu-id="ad57f-149">Sláðu inn gildi sem er sérstaklega við forritið þitt, svo sem `myapp://auth`.</span><span class="sxs-lookup"><span data-stu-id="ad57f-149">Enter a value that is specific to your app, such as `myapp://auth`.</span></span>

        <span data-ttu-id="ad57f-150">Til að sjá ákveðin dæmi fyrir vefforrit eða innfædd forrit, sjáðu skyndistyrki í [Microsoft vettvangur (áður Azure Active Directory fyrir forritara)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span><span class="sxs-lookup"><span data-stu-id="ad57f-150">To see specific examples for web apps or native apps, see the quickstarts in [Microsoft identity platform (formerly Azure Active Directory for developers)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).</span></span>

5. <span data-ttu-id="ad57f-151">Undir **API leyfi**, veldu **Bæta við leyfi**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-151">Under **API permissions**, select **Add a permission**.</span></span> <span data-ttu-id="ad57f-152">Síðan, á **Forritaskil sem samtökin mín nota** flipann, leitaðu að **Dynamics 365 Human Resources**, og bæta við **user\_impersonation** leyfi fyrir forritinu þínu.</span><span class="sxs-lookup"><span data-stu-id="ad57f-152">Then, on the **APIs my organization uses** tab, search for **Dynamics 365 Human Resources**, and add the **user\_impersonation** permission to your app.</span></span> <span data-ttu-id="ad57f-153">Auðkenni umsóknar um Human Resources er f9be0c49-aa22-4ec6-911a-c5da515226ff.</span><span class="sxs-lookup"><span data-stu-id="ad57f-153">The Application ID for Human Resources is f9be0c49-aa22-4ec6-911a-c5da515226ff.</span></span> <span data-ttu-id="ad57f-154">Notaðu þetta auðkenni til að tryggja að þú hafir valið rétt forrit.</span><span class="sxs-lookup"><span data-stu-id="ad57f-154">Use this ID to ensure you have chosen the correct application.</span></span>

6. <span data-ttu-id="ad57f-155">Veldu **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="ad57f-155">Select **Register**.</span></span>

   <span data-ttu-id="ad57f-156">[![Að skrá nýtt forrit í Azure gáttina](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ad57f-156">[![Registering a new app in the Azure portal](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)</span></span>

<span data-ttu-id="ad57f-157">Azure AD úthlutar einstöku auðkenni forrits (viðskiptavinakennara) í forritið þitt og fer með þig í forritið **Yfirlit** síðu fyrir forritið þitt.</span><span class="sxs-lookup"><span data-stu-id="ad57f-157">Azure AD assigns a unique application ID (client ID) to your app, and takes you to the **Overview** page for your app.</span></span> <span data-ttu-id="ad57f-158">Til að bæta við fleiri möguleikum í forritið þitt geturðu valið aðra stillingarvalkosti, svo sem valkosti fyrir vörumerki og fyrir skírteini og leyndarmál.</span><span class="sxs-lookup"><span data-stu-id="ad57f-158">To add more capabilities to your app, you can select other configuration options, such as options for branding and for certificates and secrets.</span></span>

## <a name="retrieving-an-access-token"></a><span data-ttu-id="ad57f-159">Sækir aðgangsmerki</span><span class="sxs-lookup"><span data-stu-id="ad57f-159">Retrieving an access token</span></span>

<span data-ttu-id="ad57f-160">Sérkenni þess hvernig þú sækir aðgangsmerki til að hringja í API fyrir mannauðsgögn fer eftir því hvaða tækni þú notar til að þróa viðskiptavinaforrit þitt.</span><span class="sxs-lookup"><span data-stu-id="ad57f-160">The specifics of how you retrieve an access token for calling the Human Resources data API will depend on what technologies you're using to develop your client application.</span></span> <span data-ttu-id="ad57f-161">Þú gætir til dæmis verið það [prófanir með þriðja aðila gagnsemi](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (eins og Postman), þróa C # stjórnborðsforrit eða vefþjónustu eða smíða javascript / TypeScript biðlara.</span><span class="sxs-lookup"><span data-stu-id="ad57f-161">For example, you might be [testing with a third party utility](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (such as Postman), developing a C# console application or web service, or building a javascript/TypeScript client.</span></span>

<span data-ttu-id="ad57f-162">Dæmi um C# biðlaraforrit:</span><span class="sxs-lookup"><span data-stu-id="ad57f-162">Example C# client application:</span></span>
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

<span data-ttu-id="ad57f-163">Þegar þú hefur sótt aðgangsmerki muntu fara framhjá tákninu í heimildarhausnum sem handhafatákn með hverri beiðni sem þú sendir til gagna API eins og lýst er hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="ad57f-163">Once you've retrieved an access token, you'll pass the token in the Authorization header as a bearer token with each request you send to the data API, as described above.</span></span>
