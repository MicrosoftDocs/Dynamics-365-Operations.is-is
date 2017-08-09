---
title: "Setja upp og nota staðbundið umhverfi"
description: "Þetta efnisatriði veitir upplýsingar hvernig eigi að áætla, setja upp og virkja staðbundið umhverfi."
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3e9a2e33d9579769f6808b598f865d75f072c450
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Setja upp og nota staðbundið umhverfi

Þetta skjal lýsir því hvernig eigi að áætla virkjun, setja upp innviði og virkja Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (staðbundið).

## <a name="finance-and-operations-components"></a>Þættir Finance and Operations

Forritið Finance and Operations samanstendur af þremur meginþáttum:

- Þjónn hugbúnaðarhluta (AOS)
- Business Intelligence (BI)
- Financial Reporting/Management Reporter

Þessir þættir byggja á eftirfarandi hugbúnaði:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1, sem hefur eftirfarandi eiginleika:

    - Heildartextavísisleit er virkjuð.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Forritið keyrir ekki ef heildartextaleit er ekki virkjuð.

- SQL Server Management Studio
- Standalone Microsoft Azure Service Fabric
- Windows PowerShell 5.0 eða seinni útgáfa
- Active Directory Federation Services (AD FS) á Windows Server 2016

  Lénsstjórinn verður að vera Windows Server 2012 R2 eða seinni útgáfa með lénvirknistigi 2012 R2, eða meira

  Til að fá nánari upplýsingar um lénvirknistig, sjá: 
  - [Hver eru virknistig Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Að skilja virknistig Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Hlutum Finance and Operations er dreift í gegnum Microsoft Dynamics Lifecycle Services (LCS). Áður en hægt er að nota, þarf að kaupa leyfislykla í gegnum rásina [Enterprise-samningar](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) og setja upp staðbundið verkefni í LCS. Aðeins er hægt hefja virkjun í gegnum LCS. Til að fá nánari upplýsingar um hvernig eigi að setja upp staðbundin verkefni í LCS, sjá [Stofna staðbundið verkefni í Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Sannvottun

Staðbundið forrit virkar með AD FS. Til að vinna með LCS, verður einnig að skilgreina Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance and Operations notar Standalone Service Fabric. Til að fá nánari upplýsingar, sjá [Service Fabric fylgiskjöl](/azure/service-fabric/).

## <a name="infrastructure"></a>Innviðir

Finance and Operations er hannað til að vinna samkvæmt samleitniskipulagi. Í stillingum hugbúnaðarins felast eftirfarandi þættir:

- Standalone Service Fabric klasi sem byggir á Windows Server 2016 sýndarvélum (VMs)
- SQL Server (stuðningur fyrir bæði klasað SQL og Always-On)
- AD FS fyrir sannvottun
- Server Message Block (SMB) útgáfa 3 skráardeiling til geymslu
- Valfrjálst: Microsoft Office Server 2017

Til að fá frekari upplýsingar, sjá [Kerfiskröfur](../get-started/system-requirements.md) og stærðarleiðbeiningar.

### <a name="hardware-layout"></a>Uppsetning vélbúnaðar

Skipuleggðu innviði þína og Service Fabric klasa, á grundvelli ráðlagðrar stærðar í [Vélbúnaðarstærð fyrir staðbundin umhverfi](../get-started/hardware-sizing-on-premises-environments.md). Til að fá nánari upplýsingar um hvernig eigi að skipuleggja Service Fabric klasa [Skipuleggðu og undirbúðu virkjun á sjálfstæðum Service Fabric klasa](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Eftirfarandi tafla sýnir dæmi um uppsetningu vélbúnaðar. Þetta dæmi er notað í þessu efnisatriði til að sýna uppsetninguna.

> [!NOTE]
> Aðalhnútur Service Fabric klasans verður að hafa a.m.k. þrjá hnúta. Í þessu dæmi er **OrchestratorType** skilgreint sem aðalhnútur.

| Tilgangur vélar                                 | Heiti vélar    | IP-tala    |
|-------------------------------------------------|-----------------|---------------|
| Lénsstjóri                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Þjónsskrá                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On klasi                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Biðlari                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric klasi/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric klasi/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric klasi/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric klasi/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric klasi/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric klasi/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric klasi/Management Reporter hnútur | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric klasi/SSRS hnútur                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Uppsetning

### <a name="prerequisites"></a>Frumskilyrði

Áður en þú hefur uppsetningu verður að uppfylla eftirfarandi skilyrði. Uppsetning á þessum forkröfum er ekki til umfjöllunar í þessu skjali.

- Active Directory Domain Services (AD DS) er uppsett og skilgreint í netkerfi þínu.
- AD FS er virkjað.
- SQL Server, SSRS og Management Studio eru uppsett.

### <a name="overview"></a>Yfirlit

Ljúka þarf eftirfarandi skrefum til að setja upp innviði fyrir Finance and Operations.

1. Skipuleggja lénsheiti þitt og DNS-svæði 
2. Skipuleggja og sækja skírteini þín
3. Skipuleggja notendur þína og þjónustureikninga
4. Stofna DNS-svæði og bæta við A-skrám
5. Bæta sýndarvélum við umdæmið
6. Setja upp nauðsynlegan hugbúnað á sýndarvélum
7. Sækja uppsetningarforskriftir frá LCS
8. Lýsa stillingum þínum
9. Setja upp skírteini
10. Setja upp sjálfstæðan Service Fabric klasa
11. Skilgreina LCS tengingar fyrir leigjandann
12. Setja upp skráargeymslu
13. Setja upp SQL Server
14. Skilgreina gagnagrunninn
15. Dulrita skilríki
16. Setja upp SSRS
17. Skilgreina AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>Skipuleggja lénsheiti þitt og DNS-svæði 

Ráðlegt er að nota opinberlega skráð lénsheiti fyrir framleiðsluuppsetningu á AOS. Á þann hátt, er hægt að komast í það utan netkerfis, ef þörf er á utanaðkomandi aðgangi.

Til dæmis, ef lén fyrirtækis þíns er contoso.com, gæti svæðið fyrir Finance and Operations (staðbundið) verið d365ffo.onprem.contoso.com og hýsilsheiti verið eftirfarandi:

- ax.d365ffo.onprem.contoso.com fyrir AOS vélar
- sf.d365ffo.onprem.contoso.com fyrir Service Fabric klasann

### <a name="plan-and-acquire-your-certificates"></a>Skipuleggja og sækja skírteini þín

Secure Sockets Layer (SSL) skírteini eru nauðsynleg til að tryggja að Service Fabric klasi og öll forrit séu virkjuð. Fyrir framleiðslu- og sandkassavinnuálag, er ráðlegt að sótt séu vottorð frá skírteinisútgáfu (CA), eins og [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) eða [GlobalSign](https://www.globalsign.com/en/ssl/). Ef lén þitt er sett upp með [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), getur þú stofnað skírteinin í gegnum AD CS. Hvert skírteini verður að hafa einkalykil sem stofnaður var fyrir lyklaskiptin og það verður að vera hægt að flytja hann út í Personal Information Exchange (.pfx) skrá.

Hægt er að nota sjálfárituð skírteini til prófunar. Til hægðarauka innihalda uppsetningarforskriftirnar forskriftir sem búa til og flytja út sjálfárituð skírteini. Eins og áður hefur komið fram má aðeins nota þessi skírteini til prófunar.

| Málefni                                      | Skýring | Aukaþarfir |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL skírteini                   | Þetta skírteini er notað til að dulrita gögn sem eru send um netkerfi milli SQL Server tilvika og biðlaraforrits. | <p>Lénsheiti skírteinisins verður að samsvara gildu lénsheiti (FQDN) SQL Server tilviksins eða hlustanda.</p><p>Til dæmis, ef SQL hlustandi er hýstur á vélinni DAX7SQLAOSQLA, er DNS-heiti skírteinisins DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Service Fabric Server skírteini            | Þetta skírteini er notað til að tryggja öryggi hnútasamskipta milli Service Fabric hnúta. Þetta skírteini er einnig notað sem netþjónsskírteini sem biðlari sem tengist við klasann fær. | <p>Lénsheiti skírteinisins verður að samsvara DNS-svæðinu þar sem AOS og Service Fabric eru hýst.</p><p>Til dæmis gæti lénsheiti skírteinisins verið \*.onprem.contoso.com or \*.contoso.com.</p><p>Ef þú ert að nota skírteini með algildisstaf á algildisstafurinn aðeins við um eitt stig. Það verður að nota undirlén, aukaefnisheiti (SAN),í skírteininu ef um er að ræða fleiri en eitt stig, eins og \*.contoso.com í dæminu á undan.</p> |
| Service Fabric Client skírteini            | Þetta skírteini er notað af biðlurum til að skoða og stýra Service Fabric klasanum. | |
| Dulritunarskírteini                     | Þetta skírteini er notað til að dulrita viðkvæmar upplýsingar eins og aðgangsorð fyrir SQL Server og aðgangsorð að notendareikningum. | <p>Notkun á skírteinislykli verður að fela í sér gagnadulritun (10) og ætti ekki að fela í sér sannvottun þjóns eða sannvottun biðlara.</p><p>Til að fá nánari upplýsingar, sjá [Stýring á leyndarmálum í Service Fabric forritum](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL skírteini                          | <p>Þetta skírteini er notað sem netþjónsskírteini sem biðlari fyrir AOS vefsvæðið fær. Það er einnig notað til að virkja Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP) skírteini.</p><p>Hægt er að nota Service Fabric Server skírteinið hér ef það er skírteini með algildisstaf.</p> | <p>Lénsheiti skírteinisins verður að samsvara DNS-svæðinu þar sem AOS og Service Fabric eru hýst.</p><p>Til dæmis, gæti lénsheiti skírteinisins verið \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com, or \*.contoso.com.</p><p>Ef þú ert að nota skírteini með algildisstaf á algildisstafurinn aðeins við um eitt stig. Það verður að nota undirlén, SAN,í skírteininu ef um er að ræða fleiri en eitt stig, eins og \*.contoso.com í dæminu á undan.</p> |
| Skírteini fyrir setusannvottun           | Þetta skírteini er notað af AOS til að tryggja öryggi upplýsinga í setu notanda. | Þetta er einnig það skírteini **Skráasvæðisins** sem verður notað við virkjun úr LCS. |
| Skírteini fyrir gagnadulritun og gagnaundirritun | Þessi skírteini verða notuð af AOS til að dulrita viðkvæmar upplýsingar. | |
| Financial Reporting biðlaraskírteini       | Þetta skírteini er notað til að tryggja öryggi samskipta milli Financial Reporting þjónustu og AOS. | |
| Skýrsluskírteini                        | Þetta skírteini er notað til að tryggja öryggi samskipta milli SSRS og AOS. | |
| Skírteini fyrir staðbundinn fulltrúa á svæðinu           | <p>Þetta skírteini er notað til að tryggja öryggi samskipta milli staðbundins fulltrúa sem er hýstur á svæðinu og LCS.</p><p>Þetta skírteini gerir staðbundnum fulltrúa kleift að aðhafast fyrir hönd Azure AD leigjanda þíns og hafa samskipti við LCS í því skyni að skipuleggja og fylgjast með virkjunum.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Skipuleggja notendur þína og þjónustureikninga

Þú verður að stofna nokkra notenda- eða þjónustureikninga svo Finance and Operations (staðbundið) virki. Stofna þarf samsetningu hópstjórnaðra þjónustureikninga (gMSAs), lénsreikninga og SQL reikninga. Eftirfarandi tafla sýnir notendareikninga, tilgang þeirra og dæmi um heiti sem verða notuð í þessu efnisatriði.

| Notandareikningur                                            | Gerð           | Málefni | Notandanafn |
|---------------------------------------------------------|----------------|---------|-----------|
| Þjónustureikningur fyrir Financial Reporting forritið         | gMSA           |         | Contoso\\svc-FRAS$ |
| Þjónustureikningur fyrir Financial Reporting ferlið             | gMSA           |         | Contoso\\svc-FRPS$ |
| Þjónustureikningur fyrir Financial Reporting Click Once Designer | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS þjónustureikningur                                     | gMSA           | Stofna skal þennan notanda fyrir prófanir í framtíðinni. Við mælum með því að AOS sé virkjað þannig að það virki með gMSA í útgáfum í framtíðinni. Með því að stofna þennan notanda við uppsetningu stuðlarðu að hnökralausri yfirfærslu í gMSA. | Contoso\\svc-AXSF$ |
| AOS þjónustureikningur                                     | Lénsreikningur | AOS notar þennan notanda í GA útgáfunni. | Contoso\\AXServiceUser |
| AOS SQL DB kerfisstjóranotandi                                   | SQL-notandi       | Finance and Operations notar þennan notanda til að sannvotta með SQL\*. Þessum notanda verður einnig skipt út af gMSA notandanum í komandi útgáfum. | AXDBAdmin |
| Þjónustureikningur fyrir notkun staðbundins fulltrúa                  | gMSA           | Þessi reikningur er notaður af staðbundnum fulltrúa til að skipuleggja virkjun í mismunandi hnútum. | Contoso\\Svc-LocalAgent$ |

\* The SQL notandanafnið og aðgangsorð fyrir SQL sannvottun eru örugg, þar sem þau eru dulrituð og geymd á skráasvæði.

### <a name="create-dns-zones-and-add-a-records"></a>Stofna DNS-svæði og bæta við A-skrám

DNS er samþætt við AD DS og gerir þér kleift að skipuleggja, stjórna og finna tilföng í netkerfi. Stofna DNS uppflettingasvæði og A-skrár fyrir AOS hýsilsnafnið og Service Fabric klasann. Í þessu dæmi um uppsetningu er heiti DNS-svæðisins d365ffo.onprem.contoso.com og A-skrár/hýsilsnöfn eru eftirfarandi:

- **ax**.d365ffo.onprem.contoso.com fyrir AOS vélar
- **sf**.d365ffo.onprem.contoso.com fyrir Service Fabric klasann

#### <a name="add-a-dns-zone"></a>Bæta við DNS-svæði

Notaðu eftirfarandi aðgerð til að bæta við DNS-svæði.

1. Skráðu þig inn í vél lénsstjóra, smelltu á **Hefja** og ræstu DNS Manager með því að slá inn **dnsmgmt.msc**.
2. Hægrismelltu á heiti lénsstjóra og smelltu á **Nýtt svæði** \> **Næsta**.
3. Veldu **Aðalsvæði**.
4. Hafðu hakað við gátreitinn **Geyma svæðið í Active Directory (eingöngu í boði ef DNS-Þjónn er skrifanlegur lénsstjóri** og smelltu svo á **Næsta**.
5. Veldu **Til allra DNS-þjóna sem keyra á lénsstjórum á þessu léni: Contoso.com** og smelltu svo á **Næsta**.
6. Veldu **Uppflettingasvæði** og smelltu svo á **Næsta**.
7. Sláðu inn heiti svæðis fyrir uppsetningu þína og smelltu svo á **Næsta**. Til dæmis, sláðu inn **d365ffo.onprem.contoso.com**.
8. Veldu **Ekki leyfa kvikar uppfærslur** og smelltu svo á **Næsta**.

#### <a name="set-up-an-a-record-for-aos"></a>Setja upp A-skrá fyrir AOS

Á nýju DNS-svæði, stofnaðu eina A-skrá sem heitir **ax.d365ffo.onprem.contoso.com** fyrir **hvern** Service Fabric klasahnút af gerðinni **AOSNodeType**. Ekki stofna A-skrár fyrir aðrar hnútagerðir.

1. Hægrismelltu á nýja svæðið og smelltu svo á **Nýr hýsill**.
2. Sláðu inn heiti og IP-tölu Service Fabric hnútsins (t.d. 10.179.108.12) og smelltu svo á **Bæta við hýsli**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Setja upp A-skrá fyrir skipuleggjandann

Á nýju DNS-svæði, stofnaðu A-skrá sem heitir **sf.d365ffo.onprem.contoso.com** fyrir **hvern** Service Fabric klasahnút af gerðinni **OrchestratorType**. Ekki stofna A-skrár fyrir aðrar hnútagerðir.

1. Hægrismelltu á nýja svæðið og smelltu svo á **Nýr hýsill**.
2. Sláðu inn heiti og IP-tölu Service Fabric hnútsins (t.d. 10.179.108.15) og smelltu svo á **Bæta við hýsli**.

#### <a name="join-vms-to-the-domain"></a>Bæta sýndarvélum við umdæmið

Bættu hverri sýndarvél við lénið með því að ljúka skrefunum í [Hvernig á að bæta Windows Server 2016 við Active Directory lén](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Einnig er hægt að nota Windows PowerShell forskriftina.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Þegar sýndarvélunum hefur verið bætt við lénið, skaltu bæta AOS þjónustureikningunum (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) við staðbundinn stjórnendahóp. Þú getur skoðað greinina [Bæta meðlimi við staðbundinn hóp](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) til að sjá hvernig á að gera þetta.

#### <a name="disable-user-access-control"></a>Afvirkja stýringu á notandaaðgangi 

Keyrðu eftirfarandi forskrift til að afvirkja stýringu á notandaaðgangi í **hverjum** Service Fabric hnút.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Það verður að endurræsa hnútinn eftir að forskriftinni er lokið á árangursríkan hátt.

#### <a name="add-prerequisite-software-to-vms"></a>Setja upp nauðsynlegan hugbúnað á sýndarvélum

Eftirfarandi tafla útlistar nauðsynlegan hugbúnað sem verður að vera notaður á vélum hverrar hnútagerðar.

> [!NOTE]
> Það verður að endurræsa tölvuna eftir að þættirnir hafa verið settir upp.

| Gerð hnúts | Hluti | Skipun |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC rekill | Sjá [Microsoft ODBC Driver 13.1 fyrir SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework útgáfa 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework útgáfa 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internet Upplýsingaþjónusta (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ Dreifingarútgáfur fyrir Microsoft Visual Studio 2013 | Sjá [Microsoft Visual C++ Dreifingarútgáfur fyrir Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access Database Engine 2010 Dreifingarpakki | Sjá [Microsoft Access Database Engine 2010 Dreifingarpakki](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework útgáfa 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework útgáfa 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 í hamnum **Upprunalegur** | |
| MR        | .NET Framework útgáfa 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework útgáfa 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ Dreifingarútgáfur fyrir Visual Studio 2013 | Sjá [Microsoft Visual C++ Dreifingarútgáfur fyrir Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Sækja uppsetningarforskriftir frá LCS

Boðið er upp á nokkrar forskriftir til að hjálpa til við að bæta upplifun við uppsetningu. Fylgdu þessum skrefum til að sækja uppsetningarforskriftir úr LCS.

1. Skráðu þig inn í LCS (<https://lcs.dynamics.com/v2>).
2. Á mælaborðinu, smelltu á reitinn **Samnýttar eignir**.
3. Smelltu á flipann **Líkan**.
4. Í hnitanetinu, veldu línuna **Dynamics 365 for Operations - forskriftir fyrir staðbundna virkjun**.
5. Smelltu á **Útgáfur** og sæktu nýjustu útgáfu af forskriftunum.

### <a name="describe-your-configuration"></a>Lýsa stillingum þínum

Þessi hluti veitir upplýsingar um forskriftir sem þarf að keyra. Forskriftirnar eru ræddar í þeirri röð sem þarf að keyra þær. Til að keyra forskriftirnar, fylltu inn í sniðmátsskrána á $(downloadPath)\\ConfigTemplate.xml. Skráin ConfigTemplate.xml lýsir Service Fabric klösunum, skírteinunum sem voru notuð til að skilgreina þá og reikningana sem þurfa að fá aðgang að viðeigandi skírteinum. Í dæminu sem hér er að finna eru gildin fyllt út fyrir dæmið um innviði sem er lýst í þessu efnisatriði. Sniðmátsskráin er notuð í næsta hluta.

#### <a name="create-the-domain-account-for-a-service-user"></a>Stofna lénsreikning fyrir þjónustunotanda

Keyrðu eftirfarandi skipun til að stofna notandareikning léns, contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>Stofna gMSAs

1. Breyttu skráasafninu í **$(DownloadPath)** og keyrðu eftirfarandi Windows PowerShell skipun.

    > [!NOTE]
    > Þessi forskrift stofnar ekki notendurna. Þess í stað prentar hún þær skipanir sem verður að keyra handvirkt á vél lénsstjóra.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Afritaðu úttak skipunarinnar í Windows PowerShell glugga. Gakktu úr skugga um að línuskil séu fjarlægð og keyrðu línurnar í vél lénsstjóra Active Directory með því að nota aukin réttindi (hægrismelltu og smelltu svo á **Keyra sem stjórnandi**).
3. Keyrðu eftirfarandi forskrift í vél lénsstjóra Active Directory til að staðfesta að tekist hafi að stofna reikningana. Gakktu úr skugga um að þú keyrir forskriftina eftir að skipt hefur verið um mynstrið sem samsvarar nafnareglu þjónustureikninganna.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Keyrðu forskriftina Export-AddGMSAsONVMScript.ps1 á biðlaravélinni. Þessi forskrift býr til forskriftir sem eru keyrðar á hverri sýndarvél Service Fabric og bætir þeim við möppu sem svarar hverju heiti sýndarvélar.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Stöðva IIS

Notaðu Remote Desktop samskiptaregluna (RDP) til að tengjast hverri Service Fabric sýndarvél og ljúktu við handvirku skrefin í [Ræsa eða stöðva vefþjóninn (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). Einnig er hægt að nota eftirfarandi Windows PowerShell forskrift með því að nota RDP til að tengjast hverri Service Fabric sýndarvél.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS eiginleikinn ætti að vera uppsettur en afvirkjaður þar sem ákveðnir hlutar vörunnar treysta á IIS dlls._

### <a name="install-certificates"></a>Setja upp skírteini

1. Hafir þú fengið skírteinin sem útlistuð voru fyrr í þessu efnisatriði frá gildri skírteinisútgáfu, skaltu fylla inn .pfx skráarnafnið og kennið fyrir skírteinin í skránni ConfigTemplate.xml. Stilltu eigindina **generateSelfSignedCert** á **Rangt** og eigindina **hægt að flytja út** á **Rangt**. Afritaðu .pfx skrárnar í möppuna $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Ef verið er að nota sjálfárituð skírteini (eingöngu til prófunar), keyrðu eftirfarandi forskrift. Til að stofna sjálfárituð skírteini í ConfigTemplate.xml skránni, gakktu úr skugga um að **generateSelfSignedCert** sé stillt á **Rétt** og **hægt að flytja út** sé stillt á **Satt**. Forskriftin uppfærir XML með kenninu fyrir skírteinin.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Flytja út nýja skírteinið með einkalyklinum (.pfx skránni). Notaðu eftirfarandi forskrift til að búa til og keyra útflutningsskipanirnar í Windows PowerShell. .pfx skrárnar verða settar í Certs-möppuna.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Það verður að setja upp skírteinin og þau verða að vera í cert:\\CurrentUser\\My. Það verður að vera hægt að flytja út skírteinin.

    Ef þú ert að nota sjálfárituð skírteini, farðu í næsta hluta. Þú þarft að ekki að ljúka við þessa aðgerð.

4. Eftir að þú hefur flutt út eða afritað .pfx skrárnar í möppuna $(DownloadPath)\\InfrastructureScripts\\Certs, keyrðu eftirfarandi skipanir til að búa til forskriftir sem verða settar í þær möppur sem samsvara sýndarvélunum.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Afritaðu forskriftirnar í hverri möppu í þær sýndarvélar sem samsvara möppuheitinu.
6. Í hverri sýndarvél skaltu keyra eftirfarandi forskriftir í þeirri röð sem þær birtast.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Setja upp sjálfstæðan Service Fabric klasa

1. Keyrðu eftirfarandi skipun til að búa til ClusterConfig.json skrána.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Til að fá nánari upplýsingar, sjá [Skref 1B: Stofna fjölvélaklasa](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Tryggja sjálfstæðan klasa á Windows sem notar X.509 skírteini](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) og [Stofna sjálfstæðan klasa sem keyrir á Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Sæktu [Uppsetningarpakka fyrir sjálfstætt Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) á einn af Service Fabric hnútum þínum. Eftir að zip-skránni er hlaðið niður, opnaðu hana með því að hægrismella á zip-skrána og smelltu svo á **Eiginleikar**. Í svarglugganum, veldu gátreitinn **Opna** neðst hægra megin.
3. Afritaðu zip-skrána í einn af hnútunum í Service Fabric klasanum og afþjappaðu henni.
4. Keyrðu eftirfarandi skipanir til að stofna innleiðareldveggsreglu á tengjum 443 og 445 á öllum hnútum.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Keyrðu eftirfarandi skipanir til að stofna innleiðareldveggsreglu á tengi 80 fyrir SSRS hnútinn eingöngu.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Afritaðu ClusterConfig.json skrá þína í óþjappaða uppsetningarstaðsetningu sjálfstæðs Service Fabric.
7. Farðu í óþjappaða uppsetningarstaðsetningu í Windows PowerShell með því að nota aukin réttindi og keyrðu eftirfarandi skipun til að prófa ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Ef prófunin heppnast, skaltu keyra eftirfarandi skipun til að virkja klasann.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Eftir að klasinn er stofnaður, skaltu opna Service Fabric vafrann á einhverri af biðlaravélunum til að villuleita uppsetninguna:

    1. Settu upp Service Fabric biðlaraskírteinið í CurrentUser\\My ef það er ekki þegar uppsett.
    2. Farðu í **IE stillingar** \> **Samhæfishamur** og hreinsaðu gátreitinn **Birta innri netsetur í samhæfisham**.
    3. Farðu í `https://sf.d365ffo.onprem.contoso.com:19080`, þar sem sf.d365ffo.onprem.contoso.com er hýsilsnafn Service Fabric klasans sem er tilgreindur í svæðinu. Ef DNS nafnaúrlausn er ekki skilgreind, skaltu nota IP-tölu vélarinnar.
    4. Velja biðlaraskírteinið. Síðan **Service Fabric vafri** birtist.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Skilgreina LCS tengingar fyrir leigjandann

Virkjun og þjónusta Finance and Operations er skipulögð í gegnum LCS með því að nota staðbundin fulltrúa á svæðinu. Til að koma á tengingu úr LCS við Finance and Operations leigjandann, verður þú að skilgreina skírteini sem gerir staðbundnum fulltrúa kleift að aðhafast fyrir hönd Azure AD leigjanda þíns (til dæmis Contoso.Onmicrosoft.com).

Notaðu skírteinið fyrir fulltrúa á svæðinu sem þú fékkst frá skírteinisútgáfu eða sjálfáritaða skírteinið sem þú bjóst til með því að nota forskriftir.

Aðeins notendareikningar sem eru með hlutverk altæks kerfisstjóra geta bætt við skírteinum til heimildar í LCS. Að sjálfgefnu verður sá einstaklingur sem skráir sig í Microsoft Office 365 fyrir fyrirtækið, altækur kerfisstjóri fyrir skráasafnið.

> [!NOTE]
> Það verður að skilgreina skírteinið nákvæmlega einu sinni fyrir hvern leigjanda. Öll staðbundin umhverfi geta notað sama skírteinið til að tengjast við LCS.

1. Sæktu og settu upp nýjustu útgáfu af Azure PowerShell á vél biðlara. Til að fá nánari upplýsingar, sjá [Uppsetning og skilgreining Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Skráðu þig inn í [viðskiptavinagátt Azure](https://portal.azure.com) til að staðfesta að þú hafir hlutverkið altækur kerfisstjóri.
3. Keyrðu eftirtaldar forskriftir úr $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Setja upp skráargeymslu

Það verður að setja upp tvær SMB 3.0 skráardeilingar, sem eru tiltækar öllum stundum. Til að fá upplýsingar um hvernig eigi að virkja SMB 3.0, sjá[SMB öryggisendurbætur](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Örugg mállýskunotkun (e. Secure dialect negotiation) getur ekki greint né komið í veg fyrir niðurfærslur úr SMB 2.0 eða 3.0 í SMB 1.0. Vegna þessa, og til að nýta alla möguleika í SMB dulritun er eindregið mælt með því að SMB 1.0 þjónninn sé afvirkjaður.

> [!NOTE]
> Til að tryggja að gögn þín séu varin þegar þau eru á bið í umhverfi þínu, verður að virkja BitLocker Drive Encryption á hverri vél. Til að fá upplýsingar um hvernig eigi að virkja BitLocker, sjá [BitLocker: Hvernig á að virkja á Windows Server 2012 og nýrri](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Skráarsvæði sem geymir notendaskjöl sem er hlaðið upp í AOS (til dæmis, \\\\DAX7SQLAOFILE1\\aos-storage).
- Skráarsvæði sem geymir síðustu nýjustu útgáfu og skilgreiningarskrár til að skipuleggja innleiðingu (til dæmis (t.d. \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Hafðu þessa skráarslóð eins stutta og mögulegt er til að forðast að fara yfir hámarkslengd slóðar á þeim skrám sem verða settar á þetta svæði.

1. Keyrðu eftirfarandi skipun á skráarsvæðisvélinni.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Uppsetning á \\\\DAX7SQLAOFILE1\\aos-storage skráarsvæðinu.

2. Í Server Manager, veldu **Skráar- og geymsluþjónusta** \> **Samnýting**.
3. Smelltu á **Verkefni** \> **Ný samnýting** til að stofna nýja samnýtingu með heitinu **aos-storage**.
4. Veittu heimildir til að **Breyta** fyrir hverja vél í Service Fabric klasanum nema **OrchestratorNodeType**.
5. Veittu heimildir til að **Breyta** fyrir notanda AOS-lénsins (contoso\\AXServiceUser) and the gMSA user (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Settu upp skráarsvæðið \\\\DAX7SQLAOFILE1\\agent.

6. Farðu aftur í Server Manager, veldu **Skráar- og geymsluþjónusta** \> **Samnýting**.
7. Smelltu á **Verkefni** \> **Ný samnýting** til að stofna nýja samnýtingu með heitinu **agent**.
8. Veittu heimildina **Full stýring** fyrir gMSA-notandann fyrir notkun staðbundins fulltrúa (contoso\\svc-LocalAgent$).

### <a name="set-up-sql-server"></a>Setja upp SQL Server

1. Settu upp SQL Server 2016 SP1 með miklum stöðugleika, annaðhvort sem SQL-klasar sem fela í sér Storage Area Network (SAN) eða með Always-On skilgreiningu.  Gakktu úr skugga um að **Database Engine, Reporting Services, Full Text Search** og **Management Tools** séu þegar uppsett.
> [!NOTE]
> Vinsamlegast tryggðu að SQL Always On sé uppsett samkvæmt [Velja upphaflega gagnasamstillingarsíðu (hjálparforrit fyrir Always On-stöðugleikahóp)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) og fylgdu [Að útbúa aukagagnagrunna handvirkt](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Keyrðu SQL-þjónustuna sem lénsnotandi.
3. Fáðu SSL-skírteini frá skírteinisútgáfu til að skilgreina Finance and Operations. Til prófunar getur þú stofnað og notað sjálfáritað skírteini.

**Sjálfáritað skírteini fyrir klösuð SQL-tilvik**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Sjálfárituð skírteini fyrir Always-On SQL-tilvik**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Notaðu skírteinið til að ljúka við skrefin í [Að virkja SSL-dulritun fyrir tilvik SQL Server með því að nota Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) til að skilgreina SSL á SQL Server.
5. Fylgdu þessum skrefum fyrir hvern hnút klasans. Gakktu úr skugga um að þú gerir breytingarnar á óvirkum hnúti og fallir yfir í hann eftir að breytingar hafa verið gerðar.

    1. Flytjið skírteinið í LocalMachine\\My.
    2. Veittu skírteinisheimildir fyrir þjónustureikninginn sem notaður er til að keyra SQL-þjónustuna. Í Microsoft Management Console (MMC), hægrismelltu á skírteinið (certlm.msc) og smelltu svo á **Verkefni** \> **Stjórna einkalyklum**.
    3. Bættu skírteiniskenninu við HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. Í Microsoft SQL Server Configuration Manager, stilltu **Krefjast dulritunar** á **Já**.

6. Flytjið út almenna lykil skírteinisins (.cer-skrána) og settu það upp á öruggri rót hvers Service Fabric hnúts.

### <a name="configure-the-orchestratordata-database"></a>Skilgreina OrchestratorData gagnagrunninn

1.  Stofnaðu tóman gagnagrunn og gefðu honum heitið **OrchestratorData**. Þessi gagnagrunnur er notaður af staðbundnum fulltrúa á svæðinu til að stýra innleiðingum.
2.  Veittu staðbundnum fulltrúa gMSA (svc-LocalAgent$) **db\_owner** heimildir í gagnagrunninum:

    1. Í trénu skal víkka út þjónsheitið, víkka út **Öryggi** \> **Innskráningar** og hægrismella svo og smella á **Ný innskráning**.

        ![Ný innskráningarskipun](./media/OPSetup_01_NewLogin.png)


    2. Flettu upp á þjónustureikningnum **svc-LocalAgent$**. Smelltu á **Staðsetningar** og veldu **Allt skráarsafnið** og smelltu svo á **Hlutagerðir** og veldu **Þjónustureikningur**.

        ![Veldu notanda, þjónustureikning eða svarglugga hóps](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Stilltu **Úthluta þjónushlutverki** á **Almennt**.
    4. Úthlutaðu heimildinni **db\_owner** fyrir gagnagrunnshlutverk til OrchestratorData-gagnagrunnsins.

### <a name="configure-the-finance-and-operations-database"></a>Skilgreina Finance and Operations gagnagrunninn

1. Skráðu þig inn í LCS (<https://lcs.dynamics.com/v2>).
2. Á mælaborðinu, smelltu á reitinn **Samnýttar eignir**.
3. Smelltu á flipann **Líkan**. 
4. Í hnitanetinu skaltu smella á línuna **Dynamics 365 for Operations on-premises, Enterprise edition - sýnigögn** til að sækja þjöppunarskrá.
5. Þjöppunarskrá inniheldur tómar .bak-skrár og .bak-skrár fyrir sýnigögn. Veldu viðeigandi .bak-skrá eftir þínum þörfum. Ef þú þarft til dæmis sýnigögn, endurheimtu þá skrána AxBootstrapDB_Demodata.bak. 
6. Endurheimtu gagnagrunninn Restore the AxBootstrapDB_DemoData.bak.
7. Endurnefndu gagnagrunninn **AXDBRAIN**.
8. Keyrðu eftirfarandi fyrirspurnir á endurheimta gagnagrunninum.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Uppfærðu skrár gagnagrunnsins.

    1. Hægrismelltu á gagnagrunninn og smelltu svo á **Eiginleikar**.
    2. Smelltu á **Skrár** til að breyta skráareiginleikum gagnagrunnsins.
    3. Í reitnum **Upphafleg stærð (MB)**, sláðu inn gildi sem er hærra en 5.120.

        ![Svargluggi gagnagrunnseiginleika](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Fyrir **AXDBBuild\_Data**, stilltu reitinn **Sjálfvirk stækkun/Fullstækka** á **200** megabæt (MB).
    5. Fyrir **AXDBBuild\_Log**, stilltu reitinn **Sjálfvirk stækkun/Fullstækka** á **500** MB.

        ![Breyta svarglugga fyrir Sjálfvirka stækkun](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Stofnaðu nýjan notanda sem hefur virkjaða SQL-sannvottun (axdbadmin).
6. Notaðu upplýsingarnar í eftirfarandi töflu til að varpa notendunum og gagnagrunnshlutverkum.

    | Notandi             | Gerð    | Gagnagrunnshlutverk |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Veittu notandanum svc-AXSF$ user og notanda axdbadmin SQL aðgang að eftirtöldum hlutverkum í tempdb-gagnagrunninum:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Í Management Studio, keyrðu eftirfarandi Transact SQL (T-SQL) skipanir:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Keyrðu eftirfarandi skipun:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Skilgreina gagnagrunn Financial Reporting

1.  Stofnaðu tóman gagnagrunn og gefðu honum heitið **FinancialReporting**.
2.  Notaðu upplýsingarnar í eftirfarandi töflu til að varpa notendunum og gagnagrunnshlutverkum.

    | Notandi             | Gerð | Gagnagrunnshlutverk |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Dulrita skilríki

1. Settu upp dulritunarskírteinið í LocalMachine\\My certificate store á öllum biðlaravélum.
2. Veittu núverandi notanda lesaðgang að einkalykli þessa skírteinis.
3. Stofnaðu Credentials.json-skrána eins og sýnt er hér.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** er dulritað aðgangsorð lénsnotanda fyrir lénsnotanda AOS (contoso\\axserviceuser).
    - **SqlUser** er dulritaður SQL-notandi (axdbadmin) sem hefur aðgang að gagnagrunnum Finance and Operations (AXDBRAIN) og **SqlPassword** er dulritaða SQL-aðgangsorðið.

4. Afritaðu .json-skrána á SMB-skráarsvæðið, \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Uppfærðu Credentials.json-skrána með dulrituðum gildum.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Í Credentials.json, skiptu út **\<encryptedDomainUserPassword\>** með dulritaða lénsaðgangsorðinu.
    2. Skiptu út **\<encryptedSqlUser\>** með dulritaða Finance and Operations SQL-notandanum.
    3. Skiptu út **\<encryptedSqlPassword\>** með Finance and Operations SQL-aðgangsorðinu.
    
### <a name="set-up-ssrs"></a>Setja upp SSRS

1.  Áður en hafist er handa skal ganga úr skugga um að þær forkröfur sem taldar eru upp í upphafi þessa efnisatriðis séu settar upp.
2.  Fylgdu skrefunum til að [Skilgreina SQL Server Reporting Services fyrir staðbundna innleiðingu](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>Skilgreina AD FS

Áður en hægt er að ljúka þessari aðgerð þarf að setja upp AD FS á Windows Server 2016. Til að fá nánari upplýsingar um hvernig eigi að setja upp AD FS, sjá [Handbók fyrir innleiðingu á Windows Server 2016 og Handbók fyrir innleiðingu 2012 R2 AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations krefst viðbótarskilgreinina umfram sjálfgefna og upprunalega skilgreiningu AD FS. Fyrir eftirfarandi skref keyrir Windows PowerShell á vél sem hefur uppsett AD FS hlutverk. Notandareikningurinn verður að hafa nægilegar heimildir til að stjórna AD FS. Til dæmis, verður notandi að hafa reikning lénsstjóra.

1. Skilgreindu AD FS kennimerkið þannig að það samsvari útgefanda merkis AD FS.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Þú ættir að afvirkja Windows Integrated Authentication (WIA) fyrir tengingar innhverfrar sannvottunar nema að þú hafir skilgreint AD FS fyrir blandað umhverfi. Til að fá nánari upplýsingar um hvernig eigi að skilgreina WIA þannig að hægt sé að nota það með AD FS, sjá [Skilgreina vafra til að nota Windows Integrated Authentication (WIA) með AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Við innskráningu verður netfang notandans að vera viðunandi sannvottunarinntak.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Til að AD FS treysti Finance and Operations fyrir sannvottunarsamskiptum, verður að skrá ýmsar hugbúnaðarfærslur í AD FS undir AD FS hugbúnaðarhóp. Til að flýta fyrir uppsetningarferlinu og draga úr villum, getur þú notað eftirfarandi forskriftir fyrir skráningu. Afritaðu forskriftina Publish-ADFSApplicationGroup.ps1 og skráasafnið D365FO-OP á vél sem hefur AD FS hlutverkaþjónustuna uppsetta. Keyrðu svo forskriftina með því að nota notandareikning, eins og stjórnandareikning, sem hefur nægilegar heimildir til að stjórna AD FS. Nánari upplýsingar um hvernig eigi að nota forskriftina má finna í fylgiskjölum sem eru talin upp í forskriftinni. Taktu eftir auðkennum biðalara sem eru tilgreind í úttakinu þar sem þú verður beðin(n) um þessar upplýsingar í LCS á seinni stigum.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

Stjórnborð AD FS ætti að líkjast því sem sést á eftirfarandi skýringarmynd. Til að opna Server Manager, smelltu á **Verkfæri** \> **AD FS-stjórnun** og svo, neðst í trénu vinstra megin, smelltu á **Hugbúnaðarhópar**. Tvísmelltu á hugbúnaðarhópinn til að sjá meiri upplýsingar.

![Eiginleikar hugbúnaðarhóps](./media/OPSetup_05_ApplicatioGroupProperties.png)

Að lokum, til að framkvæma áreiðanleikapróf, vertu viss um að þú hafir aðgang að AD FS OpenID vefslóðinni fyrir skilgreiningu á Service Fabric hnúti af gerðinni **AOSNodeType** með því að fara á `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` í vefvafra. Ef það berast skilaboð um að svæðið sé ekki öruggt, hefur þú ekki sett inn AD FS SSL skírteini þitt í certificate to the Trusted Root Certification Authorities geymsluna. Þessu skrefi er lýst í innleiðingarhandbók AD FS. Ef þú kemst á vefslóðina færðu JavaScript Object Notation (JSON) skrá sem inniheldur AD FS skilgreiningu þína og þú sérð að AD FS vefslóð þín er örugg.

Með þessu er uppsetningu á innviðum lokið. Eftirfarandi hlutar lýsa hvernig eigi að fara í [LCS](https://lcs.dynamics.com) til að setja upp tengi og innleiða Dynamics 365 for Finance and Operations umhverfið.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Skilgreina tengi og setja upp staðbundin fulltrúa á svæðinu

1. Skráðu þig inn í [LCS](https://lcs.dynamics.com/) og opnaðu verkefnið fyrir staðbundna innleiðingu.
2. Í listavalmyndinni, smelltu á **Verkstillingar**.

    ![Skipun fyrir verkstillingar](./media/OPSetup_06_ProjectSettings.png)

3. Smelltu á **Staðbundin tengi**.
4. Smelltu á **Bæta við** til að stofna nýtt tengi.
5. Í flipanum **Uppsetning hýsilskerfis**, sæktu uppsetningarforrit fyrir fulltrúa.

    ![Niðurhalshnappur fyrir uppsetningu fulltrúa í flipanum Uppsetning hýsilkerfis](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Gakktu úr skugga um að þjöppunarskráin sé ekki stöðvuð Hægrismelltu á skrána, smelltu á **Eiginleikar** og veldu svo **Opna**.
7. Afþjappaðu uppsetningarforriti fyrir fulltrúa á einum af Service fabric hnútunum í flipanum **OrchestratorType**.
8. Í flipanum **Skilgreina fulltrúa**, sláðu inn stillingarnar.
9. Vistaðu skilgreininguna og smelltu svo á **Sækja skilgreiningar** til að sækja skrána localagent-config.json configuration.

    ![Sæktu stillingarhnapp í flipanum Skilgreina sölufulltrúa](./media/OPSetup_08_DownloadConfigurations.png)

10. Afritaðu skrána localagent-config.json file á vélina þar sem uppsetningarforrit fyrir fulltrúa er staðsett.
11. Í skipanakvaðningarglugganum, keyrðu eftirfarandi skipun með að fara í möppuna sem inniheldur uppsetningaforritið fyrir fulltrúa.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Notandinn sem keyrir þessa skipun verður að hafa **db\_owner** heimildir í gagnagrunninum OrchestratorData.
    
12. Þegar tekist hefur að setja upp fulltrúa á svæðinu, skaltu fara aftur í staðbundið tengi í LCS.
13. Í flipanum **Villuleita uppsetningu**, smelltu á hnappinn **Skilaboð sölufulltrúa**. Þetta prófar LCS tenginguna við fulltrúa þinn á svæðinu. Þegar tengingu hefur verið komið á lítur síðan út eins og myndin sýnir hér að neðan.

     ![Villuleita fulltrúa](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Virkjaðu Dynamics 365 for Finance and Operations (staðbundið) umhverfið

1. Farðu í staðbundið verkefni þitt í LCS, farðu í **Umhverfi**, **Sandkassi** og smelltu á **Skilgreina**
2. Veldu **Grannfræðiumhverfi** þitt og farðu í gegnum leiðsagnarforritið til að setja virkjun í gang.
3. Fulltrúi á svæðinu tekur við virkjunarbeiðni þinni, setur í gang virkjunina og lætur vita í LCS þegar hann er tilbúinn.

