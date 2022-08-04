---
title: Settu upp beina samþættingu ítalska FatturaPA við SDI
description: Þessi grein veitir upplýsingar sem hjálpa þér að byrja með rafræna reikningagerð fyrir Ítalíu og setja upp beina samþættingu ítalska FatturaPA við Exchange kerfið (SDI).
author: abaryshnikov
ms.date: 07/27/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 363b7b5e3d5abbb990fea8f8ad4d0c1bebf80102
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203170"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Settu upp beina samþættingu ítalska FatturaPA við SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Rafræn reikningagerð fyrir Ítalíu styður ef til vill ekki allar aðgerðir sem eru tiltækar fyrir rafræna reikninga í Microsoft Dynamics 365 Fjármál og Dynamics 365 Supply Chain Management.

Þessi grein veitir upplýsingar sem hjálpa þér að byrja með rafræna reikningagerð fyrir Ítalíu í fjármála- og birgðakeðjustjórnun. Það leiðir þig í gegnum stillingarskrefin sem eru háð landi/svæði í Regulatory Configuration Services (RCS). Þessi skref eru viðbót við þau skref sem lýst er í [Byrjaðu með rafræna reikningagerð](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Forkröfur

Áður en þú lýkur skrefunum í þessari grein verður að uppfylla eftirfarandi forsendur:

- Ljúktu við skrefin í [Byrjaðu með rafræna reikningagerð](e-invoicing-get-started.md).
- Flytja inn **Ítalska FatturaPA (IT)** rafræna innheimtuaðgerð í RCS frá alþjóðlegu geymslunni. Fyrir frekari upplýsingar, sjá [Flytja inn rafrænan reikningseiginleika frá Microsoft stillingarveitunni](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) kafla áðurnefndrar greinar „Byrjað með rafrænum reikningum“.
- Bættu tenglum úr nauðsynlegum vottorðum við þjónustuumhverfið. Nauðsynleg vottorð innihalda stafræna undirskriftarvottorð, vottorðsvottorð (CA) og vottorð viðskiptavina. Fyrir frekari upplýsingar, sjá [Búðu til stafrænt vottorð leyndarmál](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) kafla í greininni „Hefjast handa með rafræna reikningaþjónustu“.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Landssértæk uppsetning fyrir ítalska FatturaPA (IT) rafræna reikningseiginleikann

Ljúktu við eftirfarandi verklagsreglur áður en þú setur uppsetningu forritsins upp í tengda Finance eða Supply Chain Management appið þitt.

Þessi hluti er viðbót við [Landssértæk uppsetning forritsuppsetningar](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) kafla í greininni „Byrjað með rafrænum reikningum“.

### <a name="create-a-new-feature"></a>Búa til nýjan eiginleika

1. Skráðu þig inn í RCS.
2. Í **Rafræn skýrslugerð** vinnurými, í **Stillingarveitur** kafla, merktu stillingarveitu fyrirtækisins sem virkan.
3. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
4. Á **Eiginleikar rafrænna reikninga** síðu, veldu **Bæta við** \> **Byggt á núverandi eiginleika**.
5. Undir **Microsoft stillingarveita**, veldu **Ítalska FatturaPA (IT)** sem grunneiginleika, sláðu inn nafn og veldu síðan **Búðu til eiginleika**.

### <a name="set-up-application-specific-parameters"></a>Setja upp færibreytur tiltekins forrits

1. Á **Eiginleikar rafrænna reikninga** síðu, veldu eiginleikann til að breyta.
2. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
3. Á **Stillingar** flipann, veldu stillingu og veldu síðan **Sértækar breytur fyrir forrit**.
4. Í **Uppflettingar** kafla, vertu viss um að **Listi yfir undirflokka Natura afturábyrgðar** uppfletting er valin.
5. Í **Skilyrði** kafla, veldu **Bæta við**.
6. Bættu við sérstökum skilyrðum fyrir hvern undirflokk sem er skilgreindur í kerfinu og vistaðu síðan breytingarnar þínar.

    > [!NOTE]
    > Í **Nafn** dálki geturðu valið **\* Autt\*** eða **\* Ekki autt\*** staðgengilsgildi í stað tiltekins gildis.

### <a name="configure-a-processing-pipeline-for-export"></a>Stilla vinnsluleiðslu fyrir útflutning

1. Á **Eiginleikar rafrænna reikninga** síðu, veldu eiginleikann til að breyta.
2. Á **Uppsetningar** flipa, veldu **Sölureikningar**, og veldu síðan **Breyta**.
3. Í **Vinnsluleiðsla** kafla, farðu í gegnum aðgerðirnar og stilltu alla nauðsynlega reiti:

    - Fyrir **Skrifaðu undir skjal** aðgerð, í **Nafn skírteinis** reit skal tilgreina stafræna undirskriftarvottorð.
    - Fyrir **Sendu inn** aðgerð, stilltu **URL heimilisfang** og **Skírteini** sviðum. Verðmæti **Skírteini** reiturinn er keðja af vottorðum, það fyrsta er CA-rótarvottorðið (caentrate.cer) og hið síðara er viðskiptavottorðið.

4. Í **Gildisreglur** kafla, farðu í gegnum ákvæðin og skoðaðu eða stilltu nauðsynlega reiti:
    - Skoðaðu **Legal EntityID** ákvæði og uppfærðu með réttu gildi frá lögaðila þínum.

5. Veldu **Staðfesta** til að tryggja að allir nauðsynlegir reiti hafi verið stilltir.
6. Vistaðu breytingarnar og lokaðu síðunni.
7. Á **Uppsetningar** flipa, veldu **Verkreikningar**, og veldu síðan **Breyta**.
8. Endurtaktu skref 3 til 6 fyrir verkreikninga.

### <a name="configure-the-processing-pipeline-for-import"></a>Stilltu vinnsluleiðsluna fyrir innflutning

1. Á **Eiginleikar rafrænna reikninga** síðu, veldu eiginleikann til að breyta.
2. Á **Uppsetningar** flipa, veldu **Flytja inn reikninga**, og veldu síðan **Breyta**.
3. Í **Gagnarás** kafla, á **Færibreytur** flipa, í **Gagnarás** reit, sláðu inn strengsgildi.
4. Á **Gildisreglur** flipanum, stilltu reiti fyrir uppsetninguna. Þú getur notað sjálfgefið **Rás** ákvæði með því að senda gildið sem þú stillir fyrir **Gagnarás** reit í fyrra skrefi í **Gildi** sviði.

    ![Setja upp gildandi reglur.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Veldu **Staðfesta** til að tryggja að allir nauðsynlegir reiti hafi verið stilltir.

### <a name="deploy-the-feature"></a>Settu eiginleikann í notkun

1. Ljúktu við, birtu og dreifðu eiginleikanum í þjónustuumhverfið. Fyrir frekari upplýsingar, sjá [Settu rafræna reikningseiginleikann í þjónustuumhverfi](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) kafla í greininni „Byrjað með rafrænum reikningum“.
2. Dreifðu eiginleikanum í tengda forritið. Fyrir frekari upplýsingar, sjá [Settu rafræna reikningseiginleikann í Tengd forrit](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) kafla í greininni „Byrjað með rafrænum reikningum“.

### <a name="set-up-finance"></a>Settu upp Fjármál

1. Skráðu þig inn í fjármálaumhverfið þitt.
2. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.
3. Veldu **Geymslur** \> **Alþjóðlegt** \> **Opið**.
4. Veldu og flyttu inn **Samhengislíkan viðskiptavinareiknings** og **Innflutningur á reikningi söluaðila (IT)** stillingar.
5. Farið í **Fyrirtækisstjórnun** \> **Uppsetning** \> **Færibreytur rafræns skjals**.
6. Á **Eiginleikar** flipann, finndu og veldu **Ítalskur rafrænn reikningur** eiginleiki og veldu síðan **Virkja** gátreit.
7. Á **Rafræn skjal** flipa skaltu ganga úr skugga um að reitirnir fyrir **Reikningardagbók viðskiptavinar** og **Verkreikningur** eru settar samkvæmt upplýsingum í [Stilltu uppsetningu forritsins](e-invoicing-get-started.md#configure-the-application-setup).

### <a name="set-up-vendor-invoice-import"></a>Settu upp innflutning lánardrottinsreikninga 

1. Í fjármálum, í **Rafræn skýrslugerð** vinnurými, í **Stillingarveitur** kafla, merktu stillingarveitu fyrirtækisins sem virkan.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Veldu **Samhengislíkan viðskiptavinareiknings**, og veldu síðan **Búðu til stillingar**.
4. Veldu **Afleidd af nafni: Samhengi reiknings viðskiptavinar, Microsoft** til að búa til afleidda uppsetningu.
5. Í **Drög** útgáfu, veldu **Hönnuður**.
6. Í **Gagnalíkan** tré, veldu **Korta líkan til gagnagjafa**.
7. Í **Skilgreiningar** tré, veldu **Gagnarás**, og veldu síðan **Hönnuður**.
8. Í **Uppsprettur gagna** tré, stækkaðu **\$ Samhengi\_ Rás** ílát.
9. Í **Gildi** reit, veldu **Breyta**. 
10. Sláðu inn nafn gagnarásarinnar. Nafnið ætti að vera að hámarki 10 stafir. Það ætti að passa við verðmæti **Gagnarás** færibreytu gagnarásarinnar fyrir eiginleikann Rafræn reikningagerð í RCS.
11. Vistaðu breytingarnar þínar og farðu síðan á **Skýrslustillingar** \> **Heill stillingarútgáfa**.
12. Á **Ytri rásir** flipa, í **Rásir** kafla, veldu **Bæta við**.
13. Í **Rás** reit, slá inn **\$ Samhengisrás** gildi.
14. Sláðu inn gildi í **Lýsing** og **Fyrirtæki** sviðum.
15. Í **Samhengi skjala** reit, veldu nýju stillingarnar sem þú fékkst úr **Samhengislíkan viðskiptavinareiknings**. Lýsing vörpunar ætti að vera **Samhengi gagnarásar**.
16. Á **Innflutningsheimildir** flipa, veldu **Bæta við**, og stilltu síðan eftirfarandi gildi:

    - **Nafn:** OutputFile
    - **Nafn gagnaeiningar:** Fyrirsögn lánardrottins reiknings (**Gagnaeining:** VendorInvoiceHeaderEntity)
    - **Líkanskortlagning:** Innflutningur á reikningi söluaðila (IT)

> [!NOTE]
> Ef þú ert með innflutningsreikninga frá mismunandi aðilum geturðu búið til nokkrar ytri rásir og nokkrar afleiddar stillingar sem hafa mismunandi **\$ Samhengisrás** gildi. Til dæmis gætirðu viljað flytja inn reikninga lánardrottins fyrir mismunandi lögaðila.

## <a name="proxy-server-setup"></a>Uppsetning proxy-þjóns

Þessi hluti veitir upplýsingar sem hjálpa þér að setja upp og stilla umboðsþjónustuna fyrir samskipti milli Exchange kerfisins (SDI) og rafrænna reikningsþjónustunnar.

### <a name="create-an-app-registration"></a>Búðu til app skráningu

1. Notaðu eftirfarandi Windows PowerShell skriftu til að búa til sjálfundirritað vottorð fyrir þjónustu-til-þjónustu (S2S) auðkenningu.

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Vistaðu .pfx vottorðaskrána í lyklageymslunni og eyddu síðan staðbundnu afritinu.
3. Skráðu þig inn á [Azure gátt](https://portal.azure.com) sem stjórnandi.
4. Búðu til forritaskráningu fyrir SDI Proxy þjónustuna.

    1. Fara til **App skráningar**, búðu til skráningu og stilltu síðan eftirfarandi gildi fyrir hana:

        - **Nafn:** SDI proxy viðskiptavinur
        - **Studdar tegundir reikninga:** Reikningar í þessari fyrirtækjaskrá eingöngu (einn leigjandi)

    2. Veldu **Skráðu þig**, og veldu síðan forritaskráninguna sem þú varst að búa til.
    3. Fara til **API heimildir**, og veldu **Veittu samþykki stjórnanda**.
    4. Fara til **Vottorð og leyndarmál**, veldu **Hladdu upp vottorði**, og hladdu upp .cer vottorðaskránni fyrir S2S auðkenningu.
    5. Fara til **Enterprise forrit**, og veldu forritið sem þú bjóst til.
    6. Vistaðu **Auðkenni umsóknar** (auðkenni viðskiptavinar) og **Auðkenni hlutar** gildi fyrir appið.
    7. Innheimtuþjónustuteymi verður að veita appinu aðgang að þjónustunni. Sendu gildi eftirfarandi stika til <D365EInvoiceSupport@microsoft.com>:

        - AAD leigjanda auðkenni
        - LCS Umhverfiskenni
        - Kenni umsóknar
        - Kenni hlutar

5. Í RCS skaltu bæta appinu við forritalistann fyrir þjónustuumhverfið þitt.

    1. Fara til **Hnattvæðingareiginleikar** \> **Umhverfi** \> **Rafræn reikningagerð** \> **Þjónustuumhverfi**, og veldu umhverfið þitt.
    2. Í **Umsóknir** kafla, bættu línu við ristina og sláðu inn nafn og hlutakenni appsins.

        ![Bætir forritinu við þjónustuumhverfið.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Veldu **Vista**, og veldu síðan **Birta**.

### <a name="create-an-azure-virtual-machine"></a>Búðu til Azure sýndarvél

1. Í [Azure gátt](https://portal.azure.com), fara til **Sýndarvélar**, og veldu **Búa til nýtt**.
2. Á **Grunnatriði** flipann, veldu áskrift og tilfangahóp. Gildin ættu að vera áskriftar- og auðlindahópurinn þar sem lykilhólfið þitt og Blob-geymslan þín eru staðsett.
3. Veldu svæðið. Þetta gildi ætti að vera svæðið þar sem fjármálaumhverfið þitt er notað.
4. Bættu við notandanafni og lykilorði stjórnanda og vistaðu þau í lyklageymslunni.
5. Í **Veldu höfn á heimleið** reit, veldu **HTTPS (443)** og **RPD (3389)**.

    > [!NOTE]
    > Við mælum með að þú slökktir á **RDP (3389)** höfn þegar kerfið fer í framleiðslu. Þú getur virkjað það aftur ef þú verður að tengjast sýndarvélinni (VM) í bilanaleitarskyni.

    ![Stillir reitina á Basics flipanum til að búa til Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Á **Diskar** flipa, á **Ítarlegri** flýtiflipann, veldu **Notaðu stýrða diska** gátreit. Skildu eftir **Tímabundinn OS diskur** gátreiturinn hreinsaður.

    ![Stillir reitina á flipanum Diskar til að búa til Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Á **Netkerfi** flipann, undir **Opinber IP** reit, veldu **Búa til nýtt**.

    ![Stillir reitina á Networking flipanum til að búa til Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Í **Búðu til opinbera IP tölu** valmynd, í **SKU** reitahópur, veldu **Standard** valmöguleika. Í **Verkefni** reitahópur, veldu **Statískt** valmöguleika.

    ![Að búa til opinbera IP tölu.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Á **Stjórnun** flipann, hreinsaðu **Sjálfvirk lokun** gátreit til að slökkva á sjálfvirkri lokun.
10. Stilltu **Uppfærslur á stýrikerfi gesta** sviði til **Handbók**, og stilltu síðan aðrar reglur.
11. Skoðaðu og búðu til VM.
12. Í nýja VM, farðu til **Sjálfsmynd** \> **Kerfi úthlutað**, og stilltu **Staða** valmöguleika til **Á**.
13. Veittu VM aðgang að lyklageymslunni.

    1. Í lyklahólfinu, farðu til **Aðgangsstýring (IAM)** \> **Hlutverkaúthlutun**.
    2. Veldu **Bæta við hlutverkaúthlutun**, og stilltu síðan eftirfarandi reiti:

        1. Í **Hlutverk** reit, tilgreinið **Key Vault Secrets notandi**.
        2. Í **Úthluta aðgang að** reit, tilgreinið **Sýndarvél**.
        3. Í **Áskrift** reit, tilgreindu áskriftina þína.
        4. Í **Veldu** reit, tilgreindu VM þinn.

    3. Fara til **Aðgangsreglur**.
    4. Veldu **Bæta við aðgangsstefnu**, og stilltu síðan eftirfarandi reiti:

        1. Í **Valinn skólastjóri** reit, veldu VM þinn.
        2. Í **Vottorð** kafla, veldu **Listi** og **Fáðu** heimildir.

14. Í [Azure gátt](https://portal.azure.com), fara til **Opinber IP tölur**, og veldu IP töluna sem var búin til í VM.
15. Fara til **Stillingar**, og stilltu Domain Name System (DNS) nafnið.

### <a name="prepare-the-proxy-service-environment"></a>Undirbúðu umboðsþjónustuumhverfið

Fylgdu þessum skrefum á vélinni þar sem proxy-þjónustan er hýst.

1. Tengstu við VM með því að nota Remote Desktop Connection.
2. Opnaðu skyndikynni fyrir Local Machine Certificate. Fyrir frekari upplýsingar, sjá [Hvernig á að: Skoða vottorð með MMC snap-in](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Flytja inn **caenrate.cer** vottorð fyrir framleiðslu og **CAEntratetest.cer** til að prófa í [Traust rótarvottunaryfirvöld verslun](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** er rótar-CA vottorðið sem var útvegað af yfirvaldinu.)
4. Í Control Panel, opnaðu **Kveiktu eða slökktu á Windows eiginleikum**, eða farðu til **Server Manager** \> **Bættu við hlutverkum og eiginleikum** fyrir stýrikerfi netþjónsins (OS) og kveiktu á Internet Information Services (IIS) eiginleikum:

    - Vefstjórnunarverkfæri
        - IIS stjórnunarhólf
    - World Wide Web Services
        - Eiginleikar forritaþróunar
            - .NET stækkanleiki 4.7 (eða 4.8)
            - ASP
            - ASP.NET 4.7 (eða 4.8)
            - CGI
            - ISAPI viðbætur
            - ISAPI síur
        - Algengar HTTP eiginleikar
            - Sjálfgefið skjal
            - Skráaskoðun
            - HTTP villur
            - Statískt efni
        - Heilsa og greining
            - HTTP skráning
            - Rakning
        - Frammistöðueiginleikar
            - Stöðug efnisþjöppun
        - Öryggi
            - Biðja um síun

    ![Kveikir á IIS eiginleikum.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Settu upp SDI Proxy þjónustuna í IIS

1. Í Microsoft Dynamics Lifecycle Services (LCS), farðu í Samnýtt eignasafn og veldu **Gagnapakki** sem eignategund.
2. Finndu **Rafræn reikningaþjónusta Sdi umboð**, og hlaðið því niður á VM.
3. Stilltu þjónustuna.

    1. Renndu niður **Rafræn reikningaþjónusta Sdi umboð** geymslumöppu sem þú halaðir niður.
    2. Í **src\\ FattureService** möppu, opnaðu **appssettings.json** skrá og stilltu eftirfarandi færibreytur:

        - **KeyVaultUri** – Tilgreindu heimilisfang lykilhólfsins sem geymir viðskiptavottorð fyrir reikningsþjónustuna.
        - **TenantId** – Tilgreindu alþjóðlegt einstakt auðkenni (GUID) leigjanda viðskiptavinarins.
        - **EnvironmentId** – Tilgreindu auðkenni LCS umhverfisins.
        - **ClientId** – Tilgreindu appauðkenni milliþjónustuappsskráningar hjá leigjanda viðskiptavinarins.
        - **ClientCertificateName** – Tilgreindu nafn S2S vottorðsins í lyklahólfinu.
        - **SecurityServiceClientOptions.Endapunktur** – Tilgreindu slóð öryggisþjónustunnar.
        - **SecurityServiceClientOptions.Resource** – Tilgreindu umfangið til að fá táknið fyrir.
        - **InvoicingServiceClientOptions.Endapunktur** – Tilgreindu endapunkt reikningsþjónustunnar. Þetta gildi ætti að vera sama endapunktur og notaður er fyrir RCS og Finance.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Tilgreindu heiti þjónustuumhverfisins. Þetta gildi ætti að vera nafnið á fjármálaumhverfinu þínu.
        - **Tilkynningarmappa** - Tilgreindu möppuna til að vista tilkynningaskrár í.

    3. Í **web.config** skrá, finndu eftirfarandi línu og bættu við þumalfingursmerki proxy-miðlarans.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Þegar kerfið fer í framleiðslu geturðu breytt sumum gildum í web.config skránni til að draga úr magni annálaupplýsinga sem er safnað og spara pláss. Í **\<system.diagnostics\>\<source\>** hnút, breyttu gildinu á **switchValue** til **Mikilvægt, villa**. Fyrir frekari upplýsingar, sjá [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Opnaðu IIS Manager. Í trénu til vinstri, vertu áfram í rótarhnútnum. Til hægri velurðu **Netþjónavottorð**.

    ![Val á þjónustuskírteini í IIS Manager.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Opnaðu valmyndina og veldu **Flytja inn**.
6. Í **Innflutningsvottorð** valmynd, í **Vottorðsskrá (.pfx)** reit, tilgreindu slóð .pfx-skrárinnar fyrir proxy-þjónsvottorðið.

    ![Að tilgreina vottorðsskrá fyrir proxy-þjónustu.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Veldu og haltu inni (eða hægrismelltu) **Síður**, og veldu síðan **Bæta við vefsíðu**.
8. Í **Bæta við vefsíðu** valmynd, í **Heiti vefsvæðis** reit, sláðu inn nafn fyrir síðuna.
9. Í **Líkamleg leið** reit, benda á **src\\ FattureService** möppu.
10. Í **Bindandi gerð** reit, veldu **https**.
11. Í **Nafn gestgjafa** reit, tilgreindu hýsilheitið.
12. Skildu eftir **IP tölu** og **Höfn** reiti stilltir á sjálfgefin gildi.
13. Gakktu úr skugga um að **Krefjast vísbendingar um nafn netþjóns** gátreiturinn er hreinsaður, vegna þess að SDI styður ekki þá tækni.
14. Í **SSL vottorð** reit, veldu vottorð um proxy-miðlara sem þú fluttir inn.
15. Í **Umsóknarlaug** reit, tilgreindu laug fyrir síðuna og skráðu nafn hennar (td, **SdiAppPool**).

    ![Að bæta við vefsíðu.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Eftir að þú hefur lokið við að búa til vefsíðuna skaltu opna valmyndina fyrir **SSL stillingar**.

    ![Að opna valmyndina fyrir SSL stillingar.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Veldu **Krefjast SSL** gátreitinn og síðan í **Viðskiptavinavottorð** reitahópur, veldu **Krefjast** valmöguleika.

    ![Stilla SSL stillingar.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Opið **Skráaskoðun**, og veldu **Virkja**.
19. Farðu í hvaða vafra sem er **serverDNS/TrasmissioneFatture.svc**. Stöðluð síða um þjónustuna verður að birtast.

    ![Athugar þjónustuna í vafra.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Búðu til eftirfarandi möppur til að geyma annála og skrár:

    - **C:\\ Logs\\** - Geymdu annálsskrár hér. Þessar skrár er hægt að skoða af [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\ Skrár\\** – Geymdu allar svarskrárnar hér.

21. Í File Explorer, veittu **NETÞJÓNUSTA** og **IIS AppPool\\ SdiAppPool** (eða **IIS AppPool\\ DefaultAppPool** ef þú ert að nota sjálfgefna laug) aðgang að **Logs** og **Skrár** möppur.

    1. Veldu og haltu inni (eða hægrismelltu) einni af möppunum og veldu síðan **Eiginleikar**.
    2. Í **Eiginleikar** valmynd, á **Öryggi** flipa, veldu **Breyta**.
    3. Bættu notendum við ef þeir eru ekki skráðir.
    4. Endurtaktu skref 1 til 3 fyrir hina möppuna.

    ![Bætir heimildum við þjónustunotandann.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd 

Að virkja **Ítalskur rafrænn reikningur** eiginleiki gæti krafist þess að takmörkuð gögn séu send. Þessi gögn innihalda skattskráningarauðkenni stofnunarinnar. Kerfisstjóri getur virkjað og slökkt á ítalska rafræna reikningseiginleikanum. Til að slökkva á eiginleikanum skaltu fylgja þessum skrefum.

1. Farið í **Fyrirtækisstjórnun** \> **Uppsetning** \> **Færibreytur rafræns skjals**.
2. Á **Eiginleikar** flipann, veldu línurnar sem innihalda **Ítalskur rafrænn reikningur** eiginleiki og veldu síðan **Slökktu núna**.

Gögn sem eru flutt inn úr þessum ytri kerfum inn í þessa Dynamics 365 netþjónustu eru háð okkar [persónuverndaryfirlýsingu](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í hlutanum „Persónuverndartilkynning“ í lands-/svæðissértækum eiginleikum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
