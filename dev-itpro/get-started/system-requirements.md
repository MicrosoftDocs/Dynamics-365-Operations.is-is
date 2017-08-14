---
title: "Kerfiskröfur"
description: "Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fyrir staðbundna virkjun og virkjun úr skýinu."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: is-is
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Kerfiskröfur

[!include[banner](../includes/banner.md)]


Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir staðbundna virkjun og virkjun úr skýinu. Áður en hægt er að setja upp Finance and Operations þegar við á, skal staðfesta að kerfi sem unnið er með uppfylli eða fari yfir lágmarkskröfur fyrir net, vélbúnað og hugbúnað.


## <a name="supported-microsoft-office-applications"></a>Studd forrit Microsoft Office
Eftirfarandi Office-forrit eru studd í virkjunum úr skýinu og staðbundnum virkjunum á Finance and Operations.
-   Til að nota Office-innbætur fyrir Microsoft Excel og Word verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Til að skoða skjöl sem eru myndaðar Út í Excel- eða Útflutnings í Word virkni, sem verður að hafa Microsoft Office 2007 eða sett upp síðar.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Kerfiskröfur sem eru sértækar fyrir virkjun úr skýinu
## <a name="network-requirements"></a>Netþarfir
-   Finance and Operations er hannað fyrir netkerfi með 250-300 millisekúndna biðtíma eða minna. Þetta er biðtími vafra biðlara Microsoft Azure gagnamiðstöðvar sem hýsir Dynamics 365 for Finance and Operations. Mælt er með er prófað biðtíma á netinu á <http://www.azurespeed.com>.
-   Bandvíddarkröfur fyrir Finance and Operations fara eftir aðstæðum. Flestar dæmigerðar aðstæður krefjast bandvíddar yfir meira en 50 kílóbætum á sekúndu (KBps). Hins vegar fyrir aðstæður sem hafa miklar farmþarfir, eins og vinnusvæðin eða aðstæður sem fela í sér upp á yfirgripsmikil sérsnið, er mælt með fleiri bandvíddum.

Almennt séð, er Finance and Operations bestuð fyrir Internetið. Fjöldi ferða frá biðlara vafra Azure gagnamiðstöð eru mjög lágar og allt farmur þjöppuð. 

> [!WARNING]
> Ekki skal reikna bandvíddarkröfur úr biðlarastaðsetningu með því að margfalda fjölda notenda með lágmarks bandvíddarkröfum. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Nota sýnisútgáfa af Finance and Operations fyrir viðskiptavini sem hafa áhyggjur af bandvíddaþörf.

## <a name="net-framework-requirements"></a>.NET Framework þarfir
Finance and Operations krefst .NET Framework útgáfu 4.6.2 fyrir eins-smells forrit, eins og skjalaleiðarfulltrúa. Sjá leiðbeiningar með uppsetningu, [Uppsetningu .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Studdir vafrar
Vefforritið getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:


-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva
-   Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad

Farið á vefsvæði hugbúnaðarframleiðandans til að finna nýjustu útgáfu hvers vafra. 

> [!NOTE]
> -   Í prufuútgáfa Króm nafnauka verður sett upp til þess að leyfa screenshot myndir að vera áfram með Verkskráningu og í myndaðri skjöl í Microsoft Word. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Verkflæðisritillinn er ræstur sem ClickOnce-forrit. Aðeins Edge Microsoft og Internet Explorer (á studdri útgáfu af Microsoft Windows) styðja ClickOnce forrit. Verkflæðisritlinum ClickOnce hugbúnaðurinn krefst á 64-bita samhæfar stýrikerfi.
> -   Hönnunarviðmót fyrir fjárhagsskýrslugerð er ræst sem ClickOnce forritsins. Það krefst 64-bita samhæfs stýrikerfis. Ef verið er að nota Króm, verður að setja upp ClickOnce viðauka til að sækja skýrsluhönnuð biðlara. Ef verið er að nota Króm með nafnlausum afhendingarmáta, ganga úr skugga um að ClickOnce viðaukanum verður einnig virkur fyrir nafnlausan ham.
> -   Til að forskoða PDF-skrár er mælt með því að notaðir séu vafrar eins og Microsoft Edge (nýjasta tiltæka útgáfa fyrir almenning) Windows 10 eða Google Chorme (nýjasta tiltæka útgáfa fyrir almenning) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölvu.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Studdir vafrar fyrir sölustað smásöluskýs

Retail Cloud POS getur keyrt í eftirfarandi vöfrum sem keyra á tilgreindum stýrikerfum:

-   Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
-   Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
-   Chrome (síðustu almennu útgáfu) á Windows 10, Windows 8.1 eða Windows 7

## <a name="retail-modern-pos-requirements"></a>Þarfir Retail Modern POS
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Modern POS er 32-bita hugbúnaður en hún mun keyra á x86 og x64 hönnun.
-   Retail Modern POS er aðeins studd í útgáfum Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   Lágmarks studd lausn er 1280 × 1024.
-   Í tölvu sem keyrir Retail Modern POS á verður að uppfylla þær þarfir:
    -   Það verður að hafa, lágmarki tvískiptur kjarnauppsetning gjörva sem keyrir á minna en 2 gigahertz (GHz).
    -   Það verður að hafa, lágmarki 3 gígabæt (GB) af RAM.
    -   Hún verður að hafa aðgang á Internetinu.

## <a name="retail-hardware-station-requirements"></a>Kjarnapakki fyrir Retail Hardware Station.
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Hardware Station er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.
-   Retail Hardware Station er stutt á eftirfarandi stýrikerfum:
    -   Windows 7 Professional, Enterprise og Embedded editions 
    
    > [!NOTE]
    > Windows 7 er eingöngu stutt ef Internet Explorer 11 er uppsett handvirkt í kerfinu.

    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

Tölvan verður að uppfylla alla kerfiskröfur fyrir uppsetningu og notkun eftirfarandi atriða:

-   Internet Upplýsingaþjónusta (IIS)
-   Vélbúnaður þriðja aðila

## <a name="retail-store-scale-unit-requirements"></a>Þarfir fyrir Retail Store Scale Unit
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Retail Store Scale Unit er 32-bita hugbúnaður, en hún mun keyra á x86 og x64 hönnun.
-   Retail Store Scale Unit er stutt á eftirfarandi stýrikerfum:
    -   Windows 7 Professional, Enterprise og Embedded editions
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   4 GB RAM
-   1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

### <a name="recommended-system-requirements"></a>Ráðlagðar kerfisþarfir

-   6 GB RAM
-   2.4 GHz i7 (eða jafngildi) ferðatímabilinu CPU hraða á kjarnauppsetning (Fjórum kjarna ráðlagðar.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

## <a name="connector-requirements"></a>Kröfur um connector
### <a name="supported-operating-systems"></a>Studd stýrikerfi

-   Connector í Microsoft Dynamics AX hefur tvær aðskildar installers á **þjónustu Þjóns Connector Async** og **rauntíma þjónustu fyrir Dynamics AX 2012 R3**.
-   Bæði íhlutir eru 32 bita forrit en keyrir á x86 og x64 architectures.
-   Bæði íhlutir eru studdir stýrikerfi eftirfarandi:
    -   Windows 7 Professional, Enterprise og Embedded editions
    -   Windows 8.1 Update 1 Professional Enterprise og Embedded editions
    -   Windows 10 Pro Enterprise og Enterprise LTSB editions
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Lágmarksþörf kerfis

-   2 GB RAM 4 GB RAM ráðlagt
-   1.6 GHz ferðatímabilinu CPU hraða á kjarnauppsetning (kjarna Tvær eru lágmarks.)
-   Að minnsta kosti 10 GB af lausu rými (gagnagrunnur rásar getur þurft mikið rými.)

## <a name="requirements-for-development-on-local-vms"></a>Kröfur til þróunar á staðbundna VMs
Sjá upplýsingar um þarfir fyrir þróun á staðbundna hýsilsheiti vélar (VMs) [VL keyrslu á verslunarsvæðis](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Kerfiskröfur fyrir staðbundna virkjun

## <a name="network-requirements"></a>Netþarfir
Finance and Operations (staðbundið) virkar ekki í netkerfum sem notast við Internet Protocol Version 4 (IPv4) eða Internet Protocol Version 6 (IPv6). Hafðu netumhverfi í huga þegar þú skipuleggur kerfi þitt og notaðu eftirfarandi leiðbeiningar.

### <a name="network-response-time"></a>Svartími netkerfis
Í eftirfarandi töflu er listi yfir lágmarks netkerfiskröfur fyrir tengingu milli vefvafrans og Application Object Server (AOS) og gagnagrunnsins í staðbundnu kerfi.

| Virði     | Vefvafri í AOS | AOS til gagnagrunns                                            |
|-----------|--------------------|------------------------------------------------------------|
| Bandvídd | 50 KBps á notanda   | 100 MBps                                                   |
| Biðtími   | < 250-300 ms       | < 1 ms (LAN eingöngu). AOS og gagnagrunnurinn verða að vera á sama stað. |

- Finance and Operations (staðbundið) er hannað fyrir netkerfi með 250–300 millisekúndna (ms) biðtíma eða minna. Þessi biðtími er biðtími úr vafra biðlara í gagnamiðstöð sem hýsir Finance and Operations.
- Bandvíddarkröfur fyrir Finance and Operations (staðbundið) fara eftir aðstæðum. Dæmigerðar aðstæður krefjast bandvíddar sem er meiri en 50 kílóbæt á sekúndu (KBps) á milli vafra og Finance and Operations þjóns. Hins vegar, fyrir aðstæður sem hafa miklar gagnaburðarkröfur, eins og vinnusvæði eða aðstæður sem kalla á ítarleg sérsnið, er mælt með meiri bandvídd og það fer eftir notkun.
Virkjanir þar sem AOS og SQL Server Database eru í mismunandi gagnamiðstöðum eru ekki studdar. Gagnagrunnur AOS og SQL Server þurfa að vera á sama stað. Almennt er Finance and Operations bestað til að draga úr umferð frá vafra til þjóns. Fjöldi ferða úr vafra biðlara í gagnamiðstöð er annaðhvort núll eða ein fyrir hver samskipti, og gagnaburður er þjappaður.

> [!WARNING]
> Ekki skal reikna bandvíddarkröfur úr biðlarastaðsetningu með því að margfalda fjölda notenda með lágmarks bandvíddarkröfum. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Mælt er með því að nota raunverulega hermingu í öðru umhverfi en vinnsluumhverfi Finance and Operations sem besta mælikvarða á afkastagetu fyrir þitt tiltekna tilvik. 

### <a name="lan-environments"></a>LAN umhverfi
Í staðarnetsumhverfi (LAN) er Microsoft Remote Desktop í Microsoft Windows Server ekki nauðsynlegt til að tengjast Finance and Operations. Hins vegar gæti það verið nauðsynlegt fyrir þjónustuaðgerðir á þeim sýndarvélum sem mynda þjónsvirkjanir.

### <a name="wan-environments"></a>WAN umhverfi
Í víðssvæðisnetsumhverfi (WAN) er Remote Desktop í Windows Server ekki nauðsynlegt til að tengjast Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Kröfur um tengingu við Internetið
Finance and Operations (staðbundið) krefst ekki tengingar við Internetið úr vinnustöðvum notenda. Hins vegar eru sumir eiginleikar ekki tiltækir án tengingar við Internetið.

| Vafri biðlara | Aðstæður á innra neti án tengingar við Internetið er hluti af hönnuninni fyrir staðbundinn virkjunarkost. Sumir eiginleikar sem krefjast skýjaþjónustu verða ekki tiltækir, eins og söfn fyrir hjálp og leiðbeiningar í LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Þjónn         | AOS eða Service Fabric-lagið verður að geta haft samskipti við LCS. Staðbundinn vafrabiðlari krefst ekki tengingar við Internetið.                                                                                |
| Fjarmæling      | Fjarmælingagögn gætu glatast ef langvarandi truflanir verða á tengingu. Truflanir á tengingum við LCS hafa ekki áhrif á staðbundna virkni forrita.                                                |
| LCS            | Tengingar við LCS eru nauðsynlegar fyrir virkjun, kóðavirkjun og þjónustuaðgerðir.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Flutningur fjarmælingagagna í skýið
Flestar fjarmælingar eru geymdar staðbundið og hægt er að komast í þær með Event Viewer í Microsoft Windows. Lítil undirsamstæða fjarmælingatilvika er flutt í Microsoft fjarmælingapípuna í skýinu til greiningar. Viðskiptavinagögn og auðkennanleg notendagögn eru ekki hluti af fjarmælingum sem sendar eru til Microsoft. Heiti sýndarvéla eru send til Microsoft til að aðstoða við umhverfisstýringu og greiningar úr LCS gáttinni.

## <a name="domain-requirements"></a>Lénskröfur
Hafðu í huga eftirfarandi lénskröfur þegar Finance and Operations (staðbundið) er sett upp:

- Sýndarvélar sem hýsa þætti Finance and Operations (staðbundið) verða að tilheyra Active Directory léni. Active Directory Domain Services (AD DS) verður að vera skilgreint í upprunalegum ham.
- Sýndarvélar sem keyra þætti Finance and Operations (staðbundið) verða að hafa aðgang að hvorri annarri skilgreindum í Active Directory Domain Services. 
- Lénsstjóri verður að keyra á Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>Vélbúnaðarkröfur
Þessi hluti lýsir þeim hugbúnaði sem krafist er svo hægt sé að keyra Finance and Operations (staðbundið).
Raunverulegar hugbúnaðarkröfur geta verið breytilegar, allt eftir kerfisstillingu, gagnasamsetningu og þeim forritum og eiginleikum sem ákveðið er að nota. Hér eru nokkrir af þeim þáttum sem geta haft áhrif á val á viðeigandi vélbúnaði fyrir Finance and Operations (staðbundið):

- Fjöldi færslna á klukkustund.
- Fjöldi samhliða notenda.

## <a name="minimum-infrastructure-requirements"></a>Lágmarkskröfur innviða
Finance and Operations (staðbundið) notar Microsoft Azure Service Fabric til að hýsa AOS, Batch, Data management, Management reporter, og Environment skipulagningu. Microsoft SQL Server Reporting Services (SSRS) er ekki hýst í Service Fabric klasanum.
SQL Server verður að vera sett upp með stöðugri HADRON uppsetningu sem hefur a.m.k. tvo hnúta til vinnslunotkunar.
Eftirfarandi tala sýnir ráðlagðan lágmarksfjölda hnúta í Service Fabric klasa þínum.

[![ráðlagður fjöldi hnúta fyrir Service Fabric klasa](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Kröfur fyrir gjörva og vinnsluminni
Í eftirfarandi töflu er listi yfir fjölda gjörva og magn vinnsluminnis (RAM) sem krafist er fyrir hvert hlutverkanna sem þarf til að keyra þennan virkjunarkost. Til að fá frekari upplýsingar, lestu ráðlagðar lágmarkskröfur fyrir sjálfstæðan Service Fabric standalone klasa, [Skipuleggðu og undirbúðu Service Fabric klasa](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Ef annar Microsoft hugbúnaður er settur upp á sömu tölvu, verður kerfið einnig að uppfylla vélbúnaðarkröfur fyrir þann hugbúnað. Mælt er með því að þú takmarkir önnur þjónsforrit á sömu tölvu og AOS við 1 gígabæt (GB) af RAM.

**Stærðir eftir gerðum hlutverka og grannfræði**

| Grannfræði   | Hlutverk (gerð hnútar)              | Ráðlagðir gjörvakjarnar | Ráðlagt minni (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Framleiðsla | AOS, Data management, Batch   | 8                           | 24                      |
|            | Stjórnunarskýrslugerð           | 4                           | 16                      |
|            | SQL Server Reporting Services þjónn | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| Sandkassi    | AOS, Data management, Batch   | 4                           | 24                      |
|            | Stjórnunarskýrslugerð           | 4                           | 16                      |
|            | SQL Server Reporting Services þjónn | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**Lágmarksstærðarmat fyrir vinnslu- og sandkassavirkjun**\*

| Grannfræði                                  | Hlutverk                          | Fjöldi tilvika |
|-------------------------------------------|-------------------------------|---------------------|
| Framleiðsla                                | AOS (Data management, Batch)  | 3                   |
|                                           | Stjórnunarskýrslugerð           | 2                   |
|                                           | SQL Server Reporting Services þjónn | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Sandkassi                                   | AOS, Data management, Batch   | 2                   |
|                                           | Stjórnunarskýrslugerð           | 1                   |
|                                           | SQL Server Reporting Services þjónn | 1                   |
|                                           | Orchestrator                  | 3                   |
| *Grannfræði fyrir samantektarvinnslu og sandkassa* |                               | 16                  |

\*Verið er að sannprófa þessar tölur af forskoðunarviðskiptavinum okkar og þær gætu breyst eftir endurgjöf frá þeim.

\*\*Orchestrator er skilgreint sem aðalhnútagerð og verður notað til að keyra Service Fabric þjónustu einnig.

**SQL Server bakendi og upphaflegt mat AD**

[![SQL Server bakendi og upphaflegt mat AD](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*Stærðir SQL Server fara mikið eftir vinnuálagi. Til að fá frekari upplýsingar, sjá hlutann [Hugbúnaðarstærðir fyrir staðbundin umhverfi](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Geymsla

- **AOS** - Finance and Operations (staðbundið) mun nota Server Message Block (SMB) 3.0 samnýtingu til að geyma óröðuð gögn. Til að fá frekari upplýsingar, sjá [Storage Spaces Direct í Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Hagkvæmir valkostir:
    - Mjög stöðug solid-state-drive (SSD) uppsetning.
    - Geymslunet (SAN) bestað fyrir OLTP-afköst.
    - Afkastamikil Direct-attached geymsla (DAS) 
- **IOPS fyrir SQL og gagnastjórnun** – Geymslan fyrir bæði gagnastýringu og SQL Server ætti að hafa a.m.k. 2.000 inntaks/úttaksaðgerðir á sekúndu (IOPS). IOPS fyrir vinnslu fer eftir mörgum þáttum. Til að fá frekari upplýsingar, sjá hlutann “Hugbúnaðarstærðir fyrir staðbundin umhverfi”. 
- **IOPS fyrir sýndarvél** – Hver sýndarvél ætti að hafa a.m.k. 100 IOPS fyrir skrifaðgerðir.

## <a name="virtual-host-requirements"></a>Kröfur fyrir sýndarhýsil
Þegar settir eru upp sýndarhýslar fyrir Finance and Operations (staðbundið) umhverfi, sjáðu eftirfarandi leiðbeiningar: [Skipuleggðu og undirbúðu Service Fabric klasa](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) og [Lýsing á Service Fabric klasa](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Hver sýndarklasi ætti að hafa næga kjarna fyrir þá innviði sem verið er að stærðarflokka. Margar ítarlegar skilgreiningar eru mögulegar, þar sem SQL Server er staðsett á efnislegum vélbúnaði en allt annað er sýndartengt. Ef SQL Server er sýndartengdur, ætti undirkerfi disks að vera hraðvirkt SAN eða samsvarandi. Í öllum tilvikum skal gengið úr skugga um að grundvallaruppsetning sýndarhýsils sé stöðug og umfram kröfur. Þegar sýndaruppsetning er notuð skal ekki taka neinar skyndimyndir af sýndarvélum, í neinum tilvikum.

## <a name="software-requirements-for-all-server-computers"></a>Hugbúnaðarkröfur fyrir allar þjónstölvur
Eftirfarandi hugbúnaður verður að vera á tölvu áður en hægt er að setja upp nokkra þætti Finance and Operations (staðbundið):

- Microsoft .NET Framework 4.5.1 eða nýrra
- Service Fabric, til að fá frekari upplýsingar, sjá [Skipuleggðu og undirbúðu Service Fabric klasa](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Studd stýrikerfi þjóna
Í eftirfarandi töflu er listi yfir stýrikerfi þjóna sem eru studd fyrir þætti Finance and Operations.

| Stýrikerfi                                     | Athugasemdir                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter eða Standard | Þessar kröfur eiga við um gagnagrunninn og Service Fabric klasann sem hýsir AOS. |

## <a name="software-requirements-for-database-servers"></a>Hugbúnaðarkröfur fyrir gagnagrunnsþjóna

- Aðeins 64 bita útgáfur af SQL Server 2016 eru studdar.
- Í vinnsluumhverfi, er mælt með að sett sé upp síðasta heildaruppfærsla (CU) fyrir þá útgáfu SQL Server sem verið er að nota.
- Finance and Operations (staðbundið) styður Unicode uppröðun sem gerir ekki greinarmun á hástöfum og lágstöfum, gerir greinarmun á áherslum og gerir ekki greinarmun á breidd. Uppröðunin verður að samsvara Windows-staðli þeirra tölva sem eru að keyra AOS-tilvik. Ef þú ert að setja upp nýja uppsetningu, er mælt með því að þú veljir Windows uppröðun í stað SQL Server uppröðunar. Til að fá frekari upplýsingar um hvernig eigi að velja uppröðun fyrir SQL Server gagnagrunn, sjá [SQL Server fylgiskjöl](/sql/sql-server/sql-server-technical-documentation).
Í eftirfarandi töflu er listi yfir útgáfur SQL Server sem eru studdar fyrir gagnagrunna Finance and Operations. Til að fá frekari upplýsingar, sjá lágmarks vélbúnaðarkröfur fyrir [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Þörf                                                      | Athugasemdir                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition eða Enterprise Edition | Fyrir hugbúnaðarkröfur fyrir SQL Server 2016, sjá [Vélbúnaðar- og hugbúnaðarkröfur fyrir uppsetningu á SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Hugbúnaðarkröfur fyrir biðlaratölvur
Vefforrit Finance and Operations getur keyrt á hvaða tæki sem er með vefvafra sem er HTML5.0-samræmdur. Á meðal samsetninga búnaðar/vafra sem Microsoft hefur staðfest eru:

- Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
- Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
- Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva
- Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Hugbúnaðarkröfur fyrir Active Directory Federation Services 
Active Directory Federation Services (AD FS) á Windows Server 2016

Lénsstjóri verður að vera Windows Server 2012 R2 eða nýrri með lénvirknistigi 2012 R2 eða meira

Til að fá nánari upplýsingar um lénvirknistig, sjá: 
- [Hver eru virknistig Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Að skilja virknistig Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Vélbúnaðar- og hugbúnaðarkröfur fyrir Retail-þætti
Finance and Operations (staðbundið) innifelur ekki Retail-þætti eins og er.

<a name="see-also"></a>Sjá einnig
--------

[Sækja um mat afrit af Dynamics 365 til Fjármála og Aðgerðir Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

