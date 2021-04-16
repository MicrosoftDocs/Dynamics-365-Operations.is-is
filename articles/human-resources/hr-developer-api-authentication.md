---
title: Sannvottun
description: Þessi grein veitir yfirlitsupplýsingar um hvernig eigi að auðkenna Microsoft Dynamics 365 Human Resources forritunarviðmót gagnaforrits (API).
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3dffe1db98ba39fde2229e69bc70bdbf113ff6ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793682"
---
# <a name="authentication"></a>Sannvottun

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þessi grein veitir yfirlitsupplýsingar um hvernig eigi að auðkenna Microsoft Dynamics 365 Human Resources forritunarviðmót gagnaforrits (API).

## <a name="overview"></a>Yfirlit

Gögn API fyrir Human Resources er innleiðing OData. Nánari upplýsingar er að finna í [Open Data Protocol (OData)](../fin-ops-core/dev-itpro/data-entities/odata.md).

Forritið þitt verður að staðfesta sem viðurkenndur kallari áður en API mun þjónusta beiðnir úr forritinu.

## <a name="fundamentals"></a>Undirstöðuatriði

Til að kalla í gagnaforritið verður forritið að fá aðgangsmerki frá Microsoft kennivettvangi. Aðgangstáknið inniheldur upplýsingar um forritið þitt og leyfið sem það þarf til að hringja í úrræði í Human Resources.

### <a name="access-token"></a>Aðgangsmerki

Aðgangstákn sem gefin eru út af Microsoft auðkenningarpallinum eru base64-kóðuð JavaScript Object Notation (JSON) Web Tokens (JWTs). Þau innihalda upplýsingar (fullyrðingar) sem gögnaskil API (og önnur forritaskil á vefnum sem eru tryggð af Microsoft kennivettvangi) nota til að staðfesta kallara og ganga úr skugga um að kallari hafi réttar heimildir til að framkvæma aðgerðina sem hann óskar eftir. Meðan á símtölum stendur geturðu meðhöndlað aðgangsmerki sem ógegnsætt. Þú ættir alltaf að senda aðgangsmerki yfir örugga rás, svo sem Transport Layer Security (TLS) og Hypertext Transfer Protocol Secure (HTTPS).

Hér er dæmi um aðgangsmerki sem er gefið út af Microsoft kennivettvangi.

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

Til að kalla í gagnaforritið festirðu aðgangstáknið sem handhafa auðkenni við heimildarhaus í HTTP beiðninni þinni. Eftirfarandi er dæmi.

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Skráðu nýtt forrit með Azure-gáttinni

1. Skráðu þig inn á [Microsoft Azure vefsíðunni](https://portal.azure.com) með vinnu- eða skólareikningi, eða persónulegum Microsoft reikningi.

2. Ef reikningurinn þinn veitir þér aðgang að fleiri en einum leigjanda skaltu velja reikninginn þinn í efra hægra horninu og stilla vefgáttina á Azure Active Directory (Azure AD) leigjandi sem þú vilt.

3. Veldu vinstri gluggann **Azure Active Directory** þjónustu og veldu síðan **Forritaskráningar \> Ný skráning**.

4. Þegar **Skrá forrit** síðan birtist skaltu slá inn skráningarupplýsingar forritsins:

    - **Heiti**: Sláðu inn þýðingarmikið heiti forrits sem verður sýnt notendum forritsins.
    - **Studdar tegundir reikninga**: Veldu tegundir reikninga sem forritið þitt ætti að styðja.

        | Studdar reikningsgerðir | Lýsing |
        |-------------------------|-------------|
        | Reikningar í þessari skipulagaskrá eingöngu | Veldu þennan valkost ef þú ert að byggja upp atvinnugreinaforrit. Þessi valkostur er ekki tiltækur nema þú sért að skrá forritið í möppu.<p>Þessi möguleiki er kortlagður **Azure AD aðeins einn leigjandi**.</p><p>Þessi valkostur er sjálfgefinn valkostur nema þú sért að skrá forritið utan möppu. Í því tilfelli er sjálfgefinn valkostur **Azure AD margra leigjenda og persónulegra Microsoft reikninga**.</p> |
        | Reikningar í þessari skipulagaskrá | Veldu þennan valkost til að miða á alla viðskiptavini fyrirtækja og mennta.<p>Þessi möguleiki er kortlagður **Azure AD aðeins margir leigjendur**.</p><p>Ef þú skráðir forritið sem **Azure AD aðeins einn leigjandi**, þú getur notað **Auðkenning** blað til að uppfæra það til **Azure AD aðeins fjöl leigjandi** og síðan aftur til **Azure AD aðeins einn leigjandi**.</p> |
        | Reikningar í hvaða skipulagsskrá og persónulegum Microsoft reikningum | Veldu þennan valkost til að miða á breiðasta hóp viðskiptavina.<p>Þessum valkosti er varpað á **Azure AD margra leigjenda og persónulegra Microsoft reikninga**.</p><p>Ef þú skráðir forritið sem **Azure AD margra leigjenda og persónulegra Microsoft reikninga**, þú getur ekki breytt þessari stillingu í notendaviðmóti (UI). Í staðinn verður þú að nota ritstjóra forritsins til að breyta studdum tegundum reikninga.</p> |

    - **Beina URI (valfrjálst)** - Veldu gerð forritsins sem þú ert að byggja: **vefur** eða **Opinber viðskiptavinur (farsími og skrifborð)**. Sláðu síðan inn beina URI (eða svara URL) fyrir forritið.

        - Fyrir vefforrit, gefðu grunnslóð forritsins. Til dæmis, `http://localhost:31544` gæti verið slóðin fyrir vefforrit sem keyrir á vélinni þinni. Notendur nota síðan þessa slóð til að skrá sig inn á forrit á vefbiðlara.
        - Gefðu URI það fyrir opinbera viðskiptavini Azure AD notar til að skila svarbréfum. Sláðu inn gildi sem er sérstaklega við forritið þitt, svo sem `myapp://auth`.

        Til að sjá ákveðin dæmi fyrir vefforrit eða innfædd forrit, sjáðu skyndistyrki í [Microsoft vettvangur (áður Azure Active Directory fyrir forritara)](https://docs.microsoft.com/azure/active-directory/develop/#quickstarts).

5. Undir **API leyfi**, veldu **Bæta við leyfi**. Síðan, á **Forritaskil sem samtökin mín nota** flipann, leitaðu að **Dynamics 365 Human Resources**, og bæta við **user\_impersonation** leyfi fyrir forritinu þínu. Auðkenni umsóknar um Human Resources er f9be0c49-aa22-4ec6-911a-c5da515226ff. Notaðu þetta auðkenni til að tryggja að þú hafir valið rétt forrit.

6. Veldu **Skrá**.

   [![Að skrá nýtt forrit í Azure gáttina](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD úthlutar einstöku auðkenni forrits (viðskiptavinakennara) í forritið þitt og fer með þig í forritið **Yfirlit** síðu fyrir forritið þitt. Til að bæta við fleiri möguleikum í forritið þitt geturðu valið aðra stillingarvalkosti, svo sem valkosti fyrir vörumerki og fyrir skírteini og leyndarmál.

## <a name="retrieving-an-access-token"></a>Sækir aðgangsmerki

Sérkenni þess hvernig þú sækir aðgangsmerki til að hringja í API fyrir mannauðsgögn fer eftir því hvaða tækni þú notar til að þróa viðskiptavinaforrit þitt. Þú gætir til dæmis verið það [prófanir með þriðja aðila gagnsemi](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (eins og Postman), þróa C # stjórnborðsforrit eða vefþjónustu eða smíða javascript / TypeScript biðlara.

Dæmi um C# biðlaraforrit:
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

Þegar þú hefur sótt aðgangsmerki muntu fara framhjá tákninu í heimildarhausnum sem handhafatákn með hverri beiðni sem þú sendir til gagna API eins og lýst er hér að ofan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]