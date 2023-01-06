---
title: Setja upp beina samþættingu á ítölsku FatturaPA við SDI
description: Í þessari grein er að finna upplýsingar sem hjálpa til við að komast af stað með rafræna reikningsfærslu fyrir Ítalíu og setja upp beina samþættingu á ítölsku FatturaPA með Exchange System (SDI).
author: gionoder
ms.date: 01/15/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: e050d3896b2ba10433e166995d6fc405996cf0b2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267157"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Setja upp beina samþættingu á ítölsku FatturaPA við SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Rafræn reikningsfærsla fyrir Ítalíu styður eins og er hugsanlega ekki allar aðgerðir sem eru í boði fyrir rafræna reikningsfærslu í Microsoft Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Í þessar grein er að finna upplýsingar sem hjálpa til við að byrja að nota rafræna reikningsfærslu fyrir Ítalíu í Finance and Supply Chain Management. Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi/svæði fyrir sig í Regulatory Configuration Services (RCS) og Finance. Þessi skref eru viðbót við skrefin sem lýst er í [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að klára skrefin í þessari grein þarf að uppfylla eftirfarandi skilyrði:

- Ljúkið skrefunum í [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)
- Flytja skal rafræna reikningsfærslueiginleikann **Ítalskt FatturaPA (IT)** inn í RCS úr altækri geymslu. Frekari upplýsingar er að finna í hlutanum [Flytja inn eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) í áðurnefndri greininni „Hafist handa með rafrænar reikningsfærslur“.
- Bættu tenglum úr nauðsynlegum vottorðum við þjónustuumhverfið. Áskilin vottorð fela í sér vottorð stafrænnar undirskriftar, vottorð yfirvalda og vottorð biðlara. Frekari upplýsingar eru í hlutanum [Búa til leynilykil stafræns vottorðs](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) í greininni „Hafist handa með stjórnun þjónustu rafrænna reikninga“.

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Landsbundnar stillingar fyrir rafrænan reikningsfærslueiginleika ítalsks FatturaPA (IT)

Ljúkið eftirfarandi ferlum áður en uppsetning forritsins er tengd við forritið Finance eða Supply Chain Management.

Þessi hluti tengist hlutanum [Landsháð grunnstilling á uppsetningu forrits](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) í greininni „Hafist handa með rafrænar reikningsfærslur“.

### <a name="create-a-new-feature"></a>Búa til nýjan eiginleika

1. Skráðu þig inn í RCS.
2. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Skilgreiningarveitur**, skal merkja skilgreiningarveitu fyrirtækisins sem virka.
3. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
4. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Bæta við** \> **Byggt á fyrirliggjandi eiginleika**.
5. Undir **Skilgreiningarveitu Microsoft** skal velja **Ítalskt FatturaPA (IT)** sem grunneiginleika, færa inn heiti og síðan velja **Stofna eiginleika**.

### <a name="set-up-application-specific-parameters"></a>Setja upp færibreytur tiltekins forrits

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikann sem á að breyta.
2. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
3. Í flipanum **Grunnstillingar** skal velja grunnstillingu og síðan velja **Færibreytur tiltekins forrits**.
4. Í hlutanum **Uppflettingar** skal ganga úr skugga um að uppflettingin **Listi yfir Natura undirflokka bakfærslugjalda** sé valin.
5. Í hlutanum **Skilyrði** skal velja **Bæta við**.
6. Bættu við sérstökum skilyrðum fyrir hvern undirflokk sem er skilgreindur í kerfinu og vistaðu síðanbreytingarnar.

    > [!NOTE]
    > Í dálknum **heiti** er hægt að velja **\*Autt\*** eða **\*Ekki autt\*** í staðinn fyrir tiltekið gildi.

### <a name="configure-a-processing-pipeline-for-export"></a>Skilgreina vinnslukeðju fyrir útflutning

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikann sem á að breyta.
2. Á flipanum **Uppsetningar** skal velja **Sölureikningar** og síðan velja **Breyta**.
3. Í hlutanum **Úrvinnsla sölukeðju** skal fara í gegnum aðgerðirnar og stilla alla áskilda reiti:

    - Fyrir aðgerðina **Undirrita skjal**, í reitnum **Heiti vottorðs** skal tilgreina vottorð stafrænnar undirskriftar.
    - Fyrir aðgerðina **Senda inn** skal stilla reitina **Vefslóð** og **Vottorð**. Gildið fyrir reitinn **Vottorð** er vottorðakeðja, það fyrsta er vottorð rótarvottunaraðila (caentrate.cer) og það næsta er vottorð biðlara.

4. Í hlutanum **Gildissviðsreglur** skal fara í gegnum ákvæði og yfirfara eða stilla áskilda reiti:
    - Farðu yfir **LegalEntityID** ákvæðið og uppfærðu með réttu gildi úr lögaðilanum

5. Veldu **Staðfesta** til að ganga úr skugga um að allir nauðsynlegir reitir hafi verið stilltir.
6. Vistaðu breytingarnar og lokaðu síðunni.
7. Á flipanum **Uppsetningar** skal velja **Verkreikningar** og síðan velja **Breyta**.
8. Endurtakið skref 3 til 6 fyrir verkreikninga.

### <a name="configure-the-processing-pipeline-for-import"></a>Skilgreina vinnslukeðju fyrir innflutning

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikann sem á að breyta.
2. Á flipanum **Uppsetningar** skal velja **Flytja inn reikninga** og síðan velja **Breyta**.
3. Í hlutanum **Gagnarás**, á flipanum **Færibreytur**, á svæðinu **Gagnarás**, skal færa inn strenggildi.
4. Í flipanum **Gildissviðsreglur** skal stilla reitina fyrir uppsetninguna. Þú getur notað sjálfgefið ákvæði **Rásar** með því að flytja gildið sem þú stilltir fyrir reitinn **Gagnarás** úr fyrra skrefi í reitinn **Gildi**.

    ![Uppsetning gildissviðsreglna.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Veldu **Staðfesta** til að ganga úr skugga um að allir nauðsynlegir reitir hafi verið stilltir.

### <a name="deploy-the-feature"></a>Nota eiginleikann

1. Ljúktu við, gefðu út og settu upp eiginleikann í þjónustuumhverfinu. Frekari upplýsingar er að finna í hlutanum [Nota eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) í greininni „Hafist handa með rafrænar reikningsfærslur“.
2. Settu upp eiginleikann í tengda forritið. Frekari upplýsingar er að finna í hlutanum [Nota eiginleika rafrænnar reikningsfærslu í tengt forrit](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) í greininni „Hafist handa með rafrænar reikningsfærslur“.

### <a name="set-up-finance"></a>Uppsetning Finance

1. Skráðu þig inn á þitt Finance-umhverfi.
2. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.
3. Veljið **Gagnageymslur** \> **Altækt** \> **Opna**.
4. Veldu og flyttu inn grunnstillingarnar **Samhengislíkan viðskiptavinareiknings** og **Innflutningur lánardrottnareiknings (IT)**.
5. Farið í **Fyrirtækisstjórnun** \> **Uppsetning** \> **Færibreytur rafræns skjals**.
6. Í flipanum **Eiginleikar** skal finna og velja eiginleikann **Ítalskur rafrænn reikningur** og síðan velja gátreitinn **Virkja**.
7. Í flipanum **Rafrænt skjal** skal ganga úr skugga um reitirnir fyrir **Reikningabók viðskiptavinar** og **Verkreikningur** séu stilltir samkvæmt upplýsingunum í [Skilgreina uppsetningu forrits](e-invoicing-get-started.md#configure-the-application-setup).

### <a name="set-up-vendor-invoice-import"></a>Setja upp innflutning á reikningi lánardrottins 

1. Í fjármálum, á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Skilgreiningarveitur**, skal merkja skilgreiningarveitu fyrirtækisins sem virka.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Veljið **Samhengislíkan viðskiptavinareiknings** og svo **Stofna skilgreiningu**.
4. Veldu **Leiða af heiti: Reikningssamhengi viðskiptavinar, Microsoft** til að búa til afleidda grunnstillingu.
5. Í útgáfunni **Drög** skal velja **Hönnuður**.
6. Í trénu **Gagnalíkan** skal velja **Varpa líkani á gagnagjafa**.
7. Í trénu **Skilgreining** skal velja **DataChannel** og síðan **Hönnuður**.
8. Í trénu **Gagnagjafar** skal stækka geymsluna **\$Samhengi\_Rás**.
9. Á svæðinu **Gildi** skal velja **Breyta**. 
10. Sláið inn heiti gagnarásarinnar. Heitið má mest vera 10 stafir. Það ætti að samsvara gildinu á færibreytunni **Gagnarás** fyrir gagnarásina fyrir eiginleika rafrænnar reikningsfærslu í RCS.
11. Vistaðu breytingarnar og opnaðu svo **Skýrsluskilgreiningar** \> **Heildstæð útgáfa grunnstillingar**.
12. Á flipanum **Ytri rásir**, í hlutanum **Rásir**, skal velja **Bæta við**.
13. Á svæðinu **Rás** skal færa inn **\$Samhengisrás**.
14. Færið inn gildi í reitina **Lýsing** og **Fyrirtæki**.
15. Á svæðinu **Samhengi skjals** skal velja nýja skilgreiningu sem fengin er úr **Samhengislíkan viðskiptavinareiknings**. Lýsing vörpunar ætti að vera **Samhengi gagnarásar**.
16. Í flipanum **Flytja inn uppruna** skal velja **Bæta við** og síðan stilla eftirfarandi gildi:

    - **Heiti:** OutputFile
    - **Heiti gagnaeiningar:** Reikningshaus lánardrottins (**Gagnaeining:** VendorInvoiceHeaderEntity)
    - **Líkanavörpun:** Innflutningur reiknings lánardrottins (IT)

> [!NOTE]
> Ef þú hefur flutt inn lánardrottnareikninga úr mismunandi upprunum er hægt að búa til nokkrar ytri rásir og nokkrar afleiddar grunnstillingar sem eru með mismunandi gildi í **\$Samhengisrás**. Til dæmis gætir þú flutt inn lánardrottnareikninga fyrir mismunandi lögaðila.

## <a name="proxy-server-setup"></a>Uppsetning staðgengilsþjóns

Þessi hluti veitir upplýsingar sem hjálpa til við að setja upp og grunnstilla staðgengilsþjóninn fyrir samskipti milli Exchange-kerfis (SDI) og rafrænnar reikningsfærsluþjónustu.

### <a name="create-an-app-registration"></a>Búa til forritsskráningu

1. Notaðu eftirfarandi Windows PowerShell-forskrift til að búa til sjálfundirritað vottorð fyrir sannvottun á milli þjónusta (S2S).

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

2. Vistaðu .pfx vottorðaskrána í lyklageymslu og eyddu síðan staðbundnu afriti.
3. Skráðu þig inn sem stjórnandi á [Azure-gáttinni](https://portal.azure.com).
4. Stofnaðu forritsskráningu fyrir SDI-staðgengilsþjónustu.

    1. Farðu í **Forritsskráningar**, stofnaðu skráningu og stilltu síðan eftirfarandi gildi fyrir hana:

        - **Heiti:** SDI-staðgengilsbiðlari
        - **Studdar lyklagerðir:** Lyklar aðeins í þessu skráasafni fyrirtækis (stakur leigjandi)

    2. Veldu **Skrá** og veldu síðan forritsskráninguna sem þú varst að búa til.
    3. Farðu í **API-heimildir** og veldu **Veita samþykki kerfisstjóra**.
    4. Opnaðu **Vottorð og leynilyklar**, veldu **Hlaða upp vottorði** og hladdu upp .cer vottorðaskránni fyrir S2S-sannvottun.
    5. Farðu í **Forrit fyrir fyrirtæki** og veldu forritið sem þú varst að búa til.
    6. Vistaðu gildin fyrir **Forritsauðkennið** (biðlarakenni) og **Hlutarkenni** fyrir forritið.
    7. Þjónustuteymi reikningsfærslu verður að veita forritinu aðgang að þjónustunni. Senda gildi eftirfarandi færibreyta til <D365EInvoiceSupport@microsoft.com>:

        - AAD-leigjandakenni
        - Auðkenni LCS-umhverfis
        - Kenni umsóknar
        - Kenni hlutar

5. Í RCS skaltu bæta forritinu við forritalistann fyrir þjónustuumhverfið þitt.

    1. Farðu í **Altækir eiginleikar** \> **Umhverfi** \> **Rafræn reikningsfærsla** \> **Þjónustuumhverfi** og veldu umhverfið þitt.
    2. Í hlutanum **Forrit** skal bæta línu við hnitanetið og slá inn heiti og hlutarkenni forritisins.

        ![Að bæta forritinu við þjónustuumhverfið.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Veljið **Vista** og síðan **Birta**.

### <a name="create-an-azure-virtual-machine"></a>Stofna Azure-sýndarvél

1. Í [Azure-gáttinni](https://portal.azure.com) skal opna **Sýndarvélar** og velja **Búa til nýja**.
2. Í flipanum **Grunnatriði** skal velja áskriftina og tilfangaflokkinn. Gildin ættu að vera áskriftin og tilfangaflokkurinn þar sem lyklageymslan og Blob-geymslan eru staðsett.
3. Veljið svæði. Þetta gildi ætti að vera svæðið þar sem fjármálaumhverfið þitt er sett upp.
4. Bættu við notandanafni og aðgangsorði stjórnanda og vistaðu þau í lyklageymslunni.
5. Í reitnum **Velja inntengi** skjal velja **HTTPS (443)** og **RPD (3389)**.

    > [!NOTE]
    > Mælt er með því að slökkva á **RDP (3389)** tenginu þegar kerfið fer í framleiðslu. Þú getur virkjað það aftur ef þú verður að tengjast sýndarvélinni fyrir úrræðaleit.

    ![Að stilla reitina í grunnflipanum til að búa til Azure-sýndarvél.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Í flipanum **Diskar**, í flýtiflipanum **Ítarlegt**, skal velja gátreitinn **Nota stýrða diska**. Skildu gátreitinn **Skammvinnan disk stýrikerfis** eftir auðan.

    ![Að stilla reitina í diskafliðanum til að búa til Azure-sýndarvél.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Í flipanum **Netkerfi**, undir reitnum **Opnar IP-tölur** skal velja **Búa til nýtt**.

    ![Að stilla reitina í flipa netkerfis til að búa til Azure-sýndarvél.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. Í svarglugganum **Búa til opinbera IP-tölu**, í reitahópnum **BHE**, skal velja valkostinn **Staðlað**. Í reitarhópnum **Úthlutun** skal velja valkostinn **Fast**.

    ![Almenn IP-tala stofnuð.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Í flipanum **Stjórnun** skal hreina gátreitinn **Sjálfvirkur frágangur** til að gera sjálfvirkan frágang óvirkan.
10. Stilltu reitinn **Uppfærslur gestastýrikerfis** á **Handvirkt** og stilltu síðan aðrar reglur.
11. Farið yfir og búið til sýndarvél.
12. Í nýju sýndarvélinni skal fara í **Auðkenni** \> **Úthlutað kerfi** og stilla valkostinn **Staða** á **Kveikt**.
13. Veittu sýndarvélinni aðgang að lyklageymslunni.

    1. Í lyklageymslunni skal fara í **Aðgangsstýring (IAM)** \> **Úthlutanir hlutverka**.
    2. Veljið **Bæta við hlutverki** og stillið svo eftirfarandi svæði:

        1. Í reitnum **Hlutverk** skal tilgreina **Notanda leynilykla í lyklageymslu**.
        2. Í reitnum **Úthluta aðgangi til** skal tilgreina **Sýndarvél**.
        3. Í reitnum **Áskrift** skaltu tilgreina áskriftina þína.
        4. Tilgreinið sýndarvél notanda á svæðinu **Velja**.

    3. Opnið **Aðgangsreglur**.
    4. Veljið **Bæta við aðgangsreglu** og stillið svo eftirfarandi svæði:

        1. Á svæðinu **Valinn aðalreikningur** skal velja sýndarvél.
        2. Í hlutanum **Vottorð** skal velja heimildirnar **Listi** og **Sækja**.

14. Í [Azure-gáttinni](https://portal.azure.com) skal fara í **Opinberar IP-tölur** og velja IP-töluna sem var búin til í sýndarvélinni.
15. Farðu í **Grunnstilling** og stilltu heiti lénsheitakerfisins (DNS).

### <a name="prepare-the-proxy-service-environment"></a>Undirbúa staðgengilsþjónustuumhverfi

Fylgdu þessum skrefum í vélinni þar sem staðgengilsþjónninn er hýstur.

1. Tengstu við sýndarvélina með tengingu við fjartengt skjáborð.
2. Opnaðu íbót vottorðs staðbundinnar vélar. Frekar upplýsingar er að finna í [Hvernig á að skoða vottorð með MMC-íbótinni](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Flyttu **caentrate.cer** vottorð fyrir framleiðslu og **CAEntratetest.cer** fyrir prófun inn í [Verslun Trusted Root Certification Authorities](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** er rótarvottunaraðili sem yfirvöld buðu upp á.)
4. Á stjórnborðinu skaltu opna **Kveikja eða slökkva á eiginleikum Windows** eða fara í **Server Manager** \> **Bæta við hlutverkum og eiginleikum** fyrir stýrikerfi þjónsins og kveikja á eiginleikum IIS:

    - Vefstjórnunarverkfæri
        - IIS-stjórnborð
    - Veraldarvefsþjónusta
        - Eiginleikar fyrir þróun forrita
            - .NET Extensibility 4.7 (eða 4.8)
            - ASP
            - ASP.NET 4.7 (eða 4.8)
            - Tölvugrafík
            - ISAPI-viðbætur
            - ISAPI-síur
        - Almennir HTTP-eiginleikar
            - Sjálfgefið skjal
            - Flett í skráasafni
            - HTTP-villur
            - Fast efni
        - Ástand og greiningar
            - HTTP-skráning
            - Rakning
        - Afkastaeiginleikir
            - Þjöppun á föstu efni
        - Öryggi
            - Beiðnisíun

    ![Kveikt á IIS-eiginleikum.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Setja upp SDI-staðgengilsþjónustu í IIS

1. Í Microsoft Dynamics Lifecycle Services (LCS) skaltu fara í samnýtta eignasafnið og velja **Gagnapakka** sem eignagerðina.
2. Finndu **Rafræn reikningsfærsluþjónustu Sdi Proxy** og hladdu henni niður í sýndarvélina.
3. Skilgreinið þjónustuna.

    1. Afþjappaðu safnvistunarmöppunni **Rafræn reikningsfærsluþjónusta Sdi Proxy** sem þú varst að sækja.
    2. Í möppunni **src\\FattureService** skaltu opna skrána **appsettings.json** og stilla eftirfarandi færibreytur:

        - **KeyVaultUri** – Tilgreindu aðsetur lyklageymslunnar sem geymir biðlaravottorðið fyrir reikningsfærsluþjónustuna.
        - **TenantId** – Tilgreinið altækt einkvæmt kennimerki (GUID) leigjanda viðskiptavinar.
        - **EnvironmentId** – Tilgreindu auðkenni LCS-umhverfis.
        - **ClientId** – Tilgreindu forritskenni fyrir forritsskráningu millibilsþjónustu í leigjanda viðskiptavinar.
        - **ClientCertificateName** – Tilgreindu heiti S2S-vottorðsins í lyklageymslunni.
        - **SecurityServiceClientOptions.Endpoint** – Tilgreindu vefslóð öryggisþjónustunnar.
        - **SecurityServiceClientOptions.Resource** – Tilgreindu umfangið til að fá lyklana.
        - **InvoicingServiceClientOptions.Endpoint** – Tilgreindu endastöðu reikningsfærsluþjónustunnar. Þetta gildi ætti að vera sama endastöð og var notuð fyrir RCS og Finance.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Tilgreinið heiti þjónustuumhverfisins. Þetta gildi ætti að vera heiti Finance-umhverfisins.
        - **NotificationsFolder** – Tilgreindu möppuna til að vista tilkynningaskrár á innleið í.

    3. Í skránni **web.config** skal finna eftirfarandi línu og bæta við fingrafari á vottorði staðgengilsþjónsins.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Þegar kerfið fer í framleiðslu er hægt að breyta nokkrum gildum í web.config-skránni til að draga úr magni kladdaupplýsingar sem er safnað og hjálpa til við að spara pláss á diski. Í hnútnum **\<system.diagnostics\>\<source\>** skal breyta gildinu á **switchValue** í **Critical,Error**. Frekari upplýsingar er að finna í [MS Þjónusturakningaskoðun](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Opnið IIS Manager. Í trénu vinstra megin skal halda sig í rótarhnútnum. Hægra megin skal velja **Vottorð þjóns**.

    ![Val á þjónustuvottorði í IIS Manager.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Opnið valmyndina og veljið **Flytja inn**.
6. Í svarglugganum **Flytja inn vottorð** í reitnum **Vottorðsskrá (.pfx)** skal tilgreina slóð .pfx-skráar fyrir vottorð staðgengilsþjónsins.

    ![Tilgreinir vottorðaskrá staðgengilsþjónsins.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Veldu og haltu inni (eða hægrismelltu á) **Svæði** og veldu síðan **Bæta við vefsvæði**.
8. Í svarglugganum **Bæta vefsvæði við**, á svæðinu **Heiti vefsvæðis**, skal færa inn heiti vefsvæðisins.
9. Í reitnum **Efnisleg slóð** skal benda á möppuna **src\\FattureService**.
10. Á svæðinu **Bindingargerð** skal velja **https**.
11. Í reitnum **Heiti hýsils** skal tilgreina hýsilheitið.
12. Skildu reitina **IP-tala** og **Tengi** eftir á sjálfgefnum gildum.
13. Gakktu úr skugga um að gátreiturinn **Krefjast vísbendingar um heiti þjóns** sé hreinsaður því að SDI styður ekki tæknina.
14. Í reitnum **SSL-vottorð** skal velja vottorð staðgengilsþjóns sem var fluttur inn.
15. Í reitnum **Hugbúnaðarhópur** skal tilgreina hóp fyrir svæðið og skrá hjá sér heiti hans (t.d. **SdiAppPool**).

    ![Vefsvæði bætt við.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Þegar þú hefur lokið við að búa til vefsvæðið skaltu opna valmyndina fyrir **SSL-stillingar**.

    ![Opnar valmyndina fyrir SSL-stillingar.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Veldu gátreitinn **Krefjast SSL** og síðan í reitahópnum **Vottorð biðlara** skal velja valkostinn **Krefast**.

    ![Skilgreining SSL-stillinga.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Opnið **Flett í skráasafni** og veljið **Virkja**.
19. Í hvaða vafra sem er skaltu fara í **serverDNS/TrasmissioneFatture.svc**. Stöðluð síða um þjónustuna verður að birtast.

    ![Þjónustan athuguð í vafra.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Búðu til eftirfarandi möppru til að geyma kladda og skrár:

    - **C:\\Kladdar\\** – Vistið kladdaskrár hér. Hægt er að skoða þessar skrár með [MS Þjónustrakningarskoðara](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\Skrár\\** – Vistið allar svarskrárnar hér.

21. Í skráavafranum skaltu veita **NETKERFISÞJÓNUSTU** og **IIS AppPool\\SdiAppPool** (eða **IIS AppPool\\DefaultAppPool** ef þú ert að nota sjálfgefinn hóp) aðgang að möppum **Kladda** og **Skráa**.

    1. Veljið og haldið inni á (eða hægrismellið á) einni möppunni og veljið síðan **Eiginleikar**.
    2. Í svarglugganum **Eiginleikar**, í flipanum **Öryggi**, skal velja **Breyta**.
    3. Bætið notendum við ef þeir eru ekki skráðir.
    4. Endurtakið skref 1 til 3 fyrir hina möppuna.

    ![Heimildum bætt við notanda þjónustunnar.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd 

Ef eiginleikanum **Ítalskur rafrænn reikningur** er virkjaður gæti þurft að senda takmarkað magn af gögnum. Þessi gögn innihalda skattaskráningarauðkenni stofnunar/fyrirtækis. Stjórnandi getur gert eiginleika ítalskra rafrænna reikninga virkan og óvirkan. Fylgið eftirfarandi skrefum til að slökkva á eiginleikanum.

1. Farið í **Fyrirtækisstjórnun** \> **Uppsetning** \> **Færibreytur rafræns skjals**.
2. Í flipanum **Eiginleikar** skal velja línurnar sem innihalda eiginleikann **Ítalskur rafrænn reikningur** og síðan velja **Gera óvirkt núna**.

Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í hlutanum „Persónuverndartilkynning“ í fylgiskjölum um eiginleika fyrir viðkomandi land/svæði.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
