---
title: "Kerfiskröfur fyrir staðbundna virkjun"
description: "Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir nýtingu innanhúss."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: is-is
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Kerfiskröfur fyrir staðbundna virkjun

[!include[banner](../includes/banner.md)]

Í þessu efnisatriði er listi yfir kerfiskröfur fyrir núverandi útgáfu Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, fyrir nýtingu innanhúss. Áður en Finance and Operations er sett upp skal, þegar viðeigandi, tryggja að kerfið sem verið er að vinna með uppfylli eða fari fram úr lágmarks kröfum um net, vél- og hugbúnað.

## <a name="network-requirements"></a>Netþarfir
Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (innanhúss) getur starfað á netkerfi sem notar Internet Protocol Version 4 (IPv4) eða Internet Protocol Version 6 (IPv6). Kynntu þér netkerfisumhverfið þegar þú skipuleggur kerfið þitt og fylgdu eftirfarandi leiðbeiningum.

### <a name="network-response-time"></a>Svartími netkerfis
Í eftirfarandi töflu er listi yfir lágmarks netkerfiskröfur fyrir tengingu milli vefvafrans og Application Object Server (AOS) og gagnagrunnsins í staðbundnu kerfi.

| Virði     | Vefvafri í AOS                      | AOS til gagnagrunns |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Bandvídd | 50 kílóbæti á sekúndu (KBps) á notanda | 100 megabæti á sekúndu (MBps) |
| Biðtími   | Minni en 250–300 millisekúndur (ms)     | Minna en 1 ms (staðbundið svæði net [LAN] einungis). AOS og gagnagrunnurinn verða að vera sam-staðsett. |

- Finance and Operations (staðbundið) er hannað fyrir netkerfi með 250–300 millisekúndna (ms) biðtíma eða minna. Þetta er biðtími frá vafra biðlara til gagnamiðstöðvar sem hýsir Finance and Operations.
- Bandvíddarkröfur fyrir Finance and Operations (staðbundið) fara eftir aðstæðum. Dæmigerðar aðstæður krefjast bandvíddar sem er meira en 50 kílóbæti á sekúndu (KBps) á milli vafrans og Finance and Operations netþjónsins. Hins vegar fyrir aðstæður sem hafa miklar farmþarfir, eins og aðstæður sem fela í sér vinnusvæði eða yfirgripsmikil sérsnið, er mælt með meiri bandvídd. Tiltekið magn bandvíddar fer eftir notkun.

Innleiðing þar sem AOS og Microsoft SQL Server gagnagrunnar eru hýstir í mismunandi gagnamiðstöð er ekki studd. AOS og SQL Server gagnagrunnar verða að vera sam-staðsettir. 

Almennt er Finance and Operations bestað til að draga úr umferð frá vafra til þjóns. Fjöldi ferða fram og til baka frá biðlara vafra til gagnamiðstöðvar er annað hvort núll eða einn fyrir hvert tilvik notendasamskipta, og allt farmur þjöppuð.

> [!WARNING]
> Ekki reikna þarfir bandvídd frá staðsetningu biðlara með því að margfalda notendur eftir þörfum lágmarksbandvíddar. Samtímanotkun á tiltekinni staðsetningu er mjög erfitt að reikna út. Við mælum með að þú notir raunverulega hermun á móti prufu-umhverfi Finance and Operations sem helsta mælikvarðann á afköst fyrir þitt einstaka tilfelli. 

### <a name="lan-environments"></a>LAN umhverfi
Í LAN umhverfi, er Microsoft fjartengt skjáborð í Microsoft Windows netþjóni ekki krafist til að geta tengst við Finance and Operations. Fjartengds skjáborðs gæti samt sem áður verið krafist til að þjónusta aðgerðir á sýndarvélum (VM) sem mynda innleiðingar þjónsins.

### <a name="wan-environments"></a>WAN umhverfi
Í breitt svæði netkerfi (WAN) umhverfi, er fjartengt skjáborð í Windows netþjóni ekki krafist til að geta tengst við Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Kröfur um tengingu við Internetið
Finance and Operations (innanhúss) krefst ekki nettengingar frá vinnustöðvum notanda. Sumir eiginleikar eru hins vegar ekki studdir ef engin tenging er við Internetið.

|                    |   |
|--------------------|---|
| **Vafri biðlara** | Innra net aðstæður án nettengingar er skipulag punktur fyrir valkostinn um nýtingu innanhúss. Sumir eiginleikar sem krefjast þjónustu skýs eru ekki í boði, eins og Hjálp og Verkefnaleiðbeiningasafn í Microsoft Dynamics Lifecycle Services (LCS). |
| **Þjónn**         | AOS eða Microsoft Azure Service Fabric reinin verður að geta talað við LCS. Vaframiðaður biðlari innanhúss þarf ekki á nettengingu að halda. |
| **Fjarmæling**      | Fjarmælingagögn gætu glatast ef langvarandi truflanir verða á tengingu. Truflanir á tengingum við LCS hafa ekki áhrif á virkni forrita innanhúss. |
| **LCS**            | Tengingar við LCS eru nauðsynlegar fyrir virkjun, kóðavirkjun og þjónustuaðgerðir. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Flutningur fjarmælingagagna í skýið
Mest af fjarmælingargögnum er geymt á staðnum og eru aðgengileg með því að nota Event Viewer í Microsoft Windows. Lítil undirsamstæða fjarmælingatilvika er flutt í Microsoft fjarmælingapípuna í skýinu til greiningar. Viðskiptamannagögn og notanda-auðkennileg gögn eru ekki hluti af fjarmælingargögnum sem eru send til Microsoft. Heiti sýndarvéla eru send til Microsoft til að aðstoða við umhverfisstjórnun og greiningar frá LCS gáttinni.

## <a name="domain-requirements"></a>Lénskröfur
Hafðu í huga eftirfarandi lénskröfur þegar Finance and Operations (staðbundið) er sett upp:

- Sýndarvélar sem hýsa Finance and Operations (innanhúss) þætti verða að tilheyra Virku skráasafni lén. Active Directory Domain Services (AD DS) verður að vera skilgreint í upprunalegum ham.
- Sýndarvélar sem keyra Finance and Operations (innanhúss) þætti verða að hafa aðgang að hverri annarri. Þessi aðgangur er grunnstilltur í AD DS. 
- Lénsstýringin verður að vera Microsoft Windows Server 2012 R2 eða nýrri, og virknistig lénsins verður að vera 2012 R2 eða meira.

## <a name="hardware-requirements"></a>Vélbúnaðarkröfur
Þessi grein lýsir vélbúnaðinum sem er krafist til að nota Finance and Operations (innanhúss).

Hinar raunverulegu kröfur vélbúnaðarins eru breytilegar, það fer eftir grunnstillingum kerfisins, gagnasamsetningunni, og forritunum og eiginleikunum sem þú ákveður að nota. Hér eru nokkrir af þeim þáttum sem geta haft áhrif á val á viðeigandi vélbúnaði fyrir Finance and Operations (innanhúss):

- Fjöldi færslna á hverri klukkustund
- Fjöldi samhliða notenda

## <a name="minimum-infrastructure-requirements"></a>Lágmarkskröfur innviða
Finance and Operations (innanhúss) notar Service Fabric til að hýsa AOS,  Batch, Data management, Management reporter, og Environment orchestrator þjónustuna. 

SQL Server vertður að hafa háan tiltækileika HADRON uppsetningu sem hefur a.m.k. tvo hnúta fyrir framleiðslunotkun.

Eftirfarandi myndskýring sýnir lágmarksfjölda hnúta sem er mælt er með fyrir Service Fabric klasann þinn.

[![Lágmarksfjölda hnúta sem er mælt er með fyrir Service Fabric klasann](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Kröfur fyrir gjörva og vinnsluminni
Á eftirfarandi töflum eru listar yfir fjölda örgjörva og magn vinnsluminnis (RAM) sem er krafist fyrir öll þau hlutverk sem eru nauðsynleg til að keyra þennan nýtingarkost. Frekari upplýsingar, sjá ráðlagðar lágmarkskröfur fyrir Service Fabric stakan klasa í [Undirbúa Service Fabric klasann](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Ef annar Microsoft hugbúnaður er settur upp á sömu tölvu, verður kerfið einnig að uppfylla vélbúnaðarkröfur fyrir þann hugbúnað. Ef annar netþjónahugbúnaður er til staðar á sömu tölvu og AOS, ráðleggjum við þér að takmarka þann hugbúnað við 1 gígabæti af RAM.

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

**Lágmarksstærðarmat fyrir vinnslu- og sandkassavirkjun\***

| Grannfræði                                        | Hlutverk                          | Fjöldi tilvika |
|-------------------------------------------------|-------------------------------|---------------------|
| Framleiðsla                                      | AOS (Data management, Batch)  | 3                   |
|                                                 | Stjórnunarskýrslugerð           | 2                   |
|                                                 | SQL Server Reporting Services þjónn | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| Sandkassi                                         | AOS, Data management, Batch   | 2                   |
|                                                 | Stjórnunarskýrslugerð           | 1                   |
|                                                 | SQL Server Reporting Services þjónn | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *Samantekt fyrir framleiðslu og afmörkun grannfræði* |                               | *16*                |

\* Verið er að staðfesta númerin í þessari töflu, af viðskiptavinum í forskoðun og þau gætu því verið leiðrétt út frá athugasemdum þessara viðskiptavina.

\*\* Orchestrator er útnefndur sem aðal hnútategundin og verður líka notaður til að keyra Service Fabric þjónustuna.

**Upphafsáætlanir fyrir bak SQL Server og AD DS**

<table>
<thead>
<tr>
<th></th>
<th>Hlutverk</th>
<th>VM/tilvik</th>
<th>Kjarnar</th>
<th>Heildarkjarnar</th>
<th>Minni á hvert tilvik (GB)</th>
<th>Heildarminni (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Samnýttir Innviðir</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Skrá þjónn/geymsla svæði netkerfi/Mjög tiltæk geymsla</td>
<td colspan="5"><p>Bak geymslan verður að vera byggð á storkudrifi (SSD) á keyrslutími geymslunet (SAN).</p>
<p>Stærð og ílag/frálag aðgerðir á hverja sekúndu (IOPS) afköst byggist á stærð vinnuálags.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Samantekt á Samnýttir Innviðir</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*Stærðir SQL Server fara mikið eftir vinnuálagi. Frekari upplýsingar, sjá [Vélbúnaðarþörf fyrir staðbundin umhverfi](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Geymsla

- **AOS** – Finance and Operations (innanhúss) notar Þjónn skilaboðaloku (SMB) 3.0 deila til geyma óskipulögð gögn. Til að fá frekari upplýsingar, sjá [Storage Spaces Direct í Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Eftirfarandi kostir eru í boði:

    - Mjög tiltækt SSD uppsetning
    - SAN sem er bestað fyrir OLTP vinnslu
    - Stórvirk beintengd geymsla (DAS) 

- **SQL Server og gagnastjórnun IOPS** – Geymsla fyrir bæði gagnastjórnun og SQL þjón ætti að hafa a.m.k. 2.000 IOPS. IOPS fyrir vinnslu fer eftir mörgum þáttum. Frekari upplýsingar, sjá [Vélbúnaðarþörf fyrir staðbundin umhverfi](hardware-sizing-on-premises-environments.md).
- **Sýndarvél IOPS** – Hver sýndarvél ætti að hafa a.m.k. 100 skrifa IOPS.

## <a name="virtual-host-requirements"></a>Kröfur fyrir sýndarhýsil
Þegar þú setur upp sýndarvefþjóna fyrir Finance and Operations (innanhúss) umhverfi, skal skoða leiðbeiningar í [Undirbúa Service Fabric klasann](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) og [Lýsing á service fabric klasa](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Hver sýndarklasi ætti að hafa næga kjarna fyrir þá innviði sem verið er að stærðarflokka. Margar ítarlegar skilgreiningar eru mögulegar, þar sem SQL Server er staðsett á efnislegum vélbúnaði en allt annað er sýndartengt. Ef SQL Server er sýndartengdur, ætti undirkerfi disks að vera hraðvirkt SAN eða samsvarandi. Í öllum tilvikum skal gengið úr skugga um að grundvallaruppsetning sýndarhýsils sé stöðug og umfram kröfur. Þegar sýndaruppsetning er notuð skal ekki taka neinar skyndimyndir af sýndarvélum, í neinum tilvikum.

## <a name="software-requirements-for-all-server-computers"></a>Hugbúnaðarkröfur fyrir allar þjónstölvur
Eftirfarandi hugbúnaður verður að vera á tölvu áður en hægt er að setja upp nokkra þætti Finance and Operations (staðbundið):

- Microsoft .NET Framework útgáfa 4.5.1 eða nýrri
- Þjónustuefni

Frekari upplýsingar, sjá [Undirbúa Service Fabric klasann](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Studd stýrikerfi þjóna
Í eftirfarandi töflu er listi yfir stýrikerfi þjóna sem eru studd fyrir þætti Finance and Operations.

| Stýrikerfi                                     | Athugasemdir |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter eða Standard | Þessar kröfur eiga við um gagnagrunninn og Service Fabric klasann sem hýsir AOS. |

## <a name="software-requirements-for-database-servers"></a>Hugbúnaðarkröfur fyrir gagnagrunnsþjóna

- Aðeins 64 bita útgáfur af SQL Server 2016 eru studdar.
- Í vinnsluumhverfi, er mælt með að sett sé upp síðasta heildaruppfærsla (CU) fyrir þá útgáfu SQL Server sem verið er að nota.
- Finance and Operations (staðbundið) styður Unicode uppröðun sem gerir ekki greinarmun á hástöfum og lágstöfum, gerir greinarmun á áherslum og gerir ekki greinarmun á breidd. Uppröðunin verður að samsvara Windows-staðli þeirra tölva sem eru að keyra AOS-tilvik. Ef þú ert að setja upp nýja uppsetningu, er mælt með því að þú veljir Windows uppröðun í stað SQL Server uppröðunar. Til að fá frekari upplýsingar um hvernig eigi að velja uppröðun fyrir SQL Server gagnagrunn, sjá [SQL Server fylgiskjöl](/sql/sql-server/sql-server-technical-documentation).

Í eftirfarandi töflu er listi yfir útgáfur SQL Server sem eru studdar fyrir gagnagrunna Finance and Operations. Til að fá frekari upplýsingar, sjá lágmarks vélbúnaðarkröfur fyrir [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Þörf                                                      | Athugasemdir |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition eða Enterprise Edition | Fyrir hugbúnaðarkröfur fyrir SQL Server 2016, sjá [Vélbúnaðar- og hugbúnaðarkröfur fyrir uppsetningu á SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Hugbúnaðarkröfur fyrir Þjónn hugbúnaðarhluta (AOS) 
- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Hugbúnaðurkröfur fyrir skýrsluþjón (BI)
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Hugbúnaðarkröfur fyrir biðlaratölvur
Finance and Operations vefforritið er hægt að keyra á öllum tækjum sem hefur HTML 5.0-heldan vafra. Hér eru sumar af þeim sérstöku samsetningum af tækjum/vöfrum sem Microsoft hefur staðfest:

- Microsoft Edge (nýjasta almenna útgáfa) á Windows-10
- Internet Explorer 11 á Windows 10, Windows 8.1 eða Windows 7
- Google Chrome (nýjasta almenna útgáfa) á Windows 10, Windows 8.1, Windows 8, Windows 7 eða Google Nexus 10 spjaldtölva
- Apple Safari (nýjasta almenna útgáfa) á Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eða Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Hugbúnaðarkröfur fyrir Active Directory Federation Services 
Active Directory Samsteypuþjónusta (AD FS) á Windows þjóni 2016 er krafist.

Lénsstýringin verður að vera Microsoft Windows þjónn 2012 R2 eða nýrri, og virknistig lénsins verður að vera 2012 R2 eða meira. Frekari upplýsingar um virknistig léna, er að finna á eftirfarandi síðum:

- [Hver eru virknistig Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Að skilja virknistig Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Studd forrit Microsoft Office
Eftirfarandi forrit Microsoft Office eru studd í skýi og innanhúsnýtingu Finance and Operations:

-   Til að nota innbætur fyrir Microsoft Excel og Word verður Microsoft Office 2016 fyrir Windows eða Mac að vera uppsett. Sjá frekari upplýsingar um þarfir útgáfu [Office samþættingu úrræðaleit](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Til að skoða skjöl sem eru myndaðar Út í Excel- eða Útflutnings í Word virkni, sem verður að hafa Microsoft Office 2007 eða sett upp síðar.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Vélbúnaðar- og hugbúnaðarkröfur fyrir Retail-þætti
Eins og er eru Retail-þættir ekki innifaldir í Finance and Operations (Innanhúss).

