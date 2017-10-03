---
title: "Skráningarkenni"
description: "Þetta efnisatriði gefur upplýsingar um uppsetningu og notkun skráningarkenna."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 55c25b005e9dc73713f3d4a30eab5148b17c2fec
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017


---

# <a name="registration-ids"></a>Skráningarkenni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði gefur upplýsingar um uppsetningu og notkun skráningarkenna.

Mörg lönd og svæði hafa mismunandi reglur og kröfur um skráningu skráningarnúmera eða auðkenna. Þetta efnisatriði gefur yfirlit yfir nauðsynlegar stillingar og vinnslu studdra skráningargerða fyrir aðila í mismunandi Evrópulöndum/svæðum. Öll lönd/svæði setja sín skilyrði um stuðning við ýmis landsbundin atriði varðandi skráningarnúmer frá opinberum aðilum. Dæmi um skráningarnúmer eru kennitala (SSN), skattnúmer (TIN) og evrópskt VSK-númer (EU VAT ID). Þessi eiginleiki býður upp á sameiginlega umgjörð fyrir öll lönd á öllum svæðum með tilliti til landsbundinna skilyrða í sumum Evrópulöndum. Eftirfarandi kaflar lýsa heildarflæði upplýsinga sem er notað við uppsetningu og vinnslu á skráningarkennum.

## <a name="registration-type-creation"></a>Skráningargerð stofnuð
Áður en hægt er að færa inn skráningarkenni verður að setja upp skráningargerðir fyrir mismunandi tegundir skráningarnúmera sem eiga við. Farðu á síðuna **Fyrirtækisstjórnun** &gt; **Altæk aðsetursbók** &gt; **Skráningargerðir** &gt; **Skráningargerðir** til að stofna og stjórna skráningargerðum fyrir lánardrottna, viðskiptavini, starfsfólk og lögaðila í mismunandi löndum/svæðum.

|Svæði                 |lýsing      |
|------------------------------|----------------------------|                                                                           
| Nafn                | Heiti skráningargerðarinnar. |                                                                           
| lýsing         | Lýsing á skráningargerðinni. |
| Land/svæði      | Einkvæmt auðkenni lands/svæðis.|
| Skattyfirvöld       | Skattyfirvöld sem tengjast skráningargerðinni.|
| Takmarkað við       | Takmörkun sem gildir um skattskráningargerð: Engin, Einstaklingur, Fyrirtæki.|
| Snið              | Villuleitarsnið skráningargerðarinnar.|
| Hægt að uppfæra      | Skilgreinir hvort hægt sé að uppfæra skráningarnúmerið fyrir skráningargerðina eftir að það er fært inn.|
| Einkvæmt              | Skilgreinir hvort skráningarnúmerið fyrir skráningargerðina er einkvæmt. |
| Aðalaðsetur fyrir land | Ef aðili tengist einu eða fleiri aðsetrum í tilteknu landi og skráningarkennið gildir fyrir öll aðsetrin verður að velja eitt aðalaðsetur fyrir landið. Aðeins er hægt að skrá eitt aðalkenni. Skilgreinir hvort aðeins sé hægt að færa skráningarnúmerið inn fyrir aðalaðsetur í landi. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Úthluta skráningargerð til skráningarflokks
Skráningarflokkur er skráningarkenni lands/svæðis sem er samþykkt til nota í tilteknu landi/svæði fyrir skatta, tolla og í öðrum tilgangi. Þessi flokkur skilgreinir villuleitarreglur tiltekins skráningarkennis (m.a. athugun á tölum) og hvort skráningarkennið kemur fram í mismunandi skýrslum. Notaðu síðuna **Fyrirtækisstjórnun** &gt; **Altæk aðsetursbók** &gt; **Skráningargerð** &gt; **Skráningarflokkar** til að úthluta skráningargerð tiltekins lands á studdan skráningarflokk.

| Svæði            | lýsing|
|-----------------------|----------------|
| Skráningargerð     | Skráningargerð í tilteknu landi/svæði.|
| Takmarkað við         | Takmörkun sem gildir um skattskráningargerð: Engin, Einstaklingur, Fyrirtæki.|
| Skráningarflokkur | Einkvæmt skráningarkenni sem er samþykkt til notkunar í landinu. Fullur listi af studdum í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition er hér að neðan. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Slá inn skráningarkenni fyrir færslur altækrar aðsetursbókar

Altæka aðsetursbókin (GAB) í Microsoft Finance and Operations inniheldur samanteknar upplýsingar um aðsetur fyrir viðskiptavini, lánardrottna, tengiliði, viðskipatengsl og lögaðila. Frekari upplýsingar eru í [Yfirlit yfir altæka aðsetursbók](/dynamics365/unified-operations/fin-and-ops/organization-administration/overview-global-address-book). Aðilafærslur í altæku aðsetursbókinni geta innihaldið eina eða fleiri aðsetursfærslur. Þessi aðsetur eru notuð í mismunandi tilgangi, svo sem vegna reikningsgerðar eða afhendingar. Hægt er að setja upp skráningarkenni fyrir upplýsingar um aðsetur fyrir viðskiptavini, lánardrottna, starfsfólk og lögaðila. Finndu aðila (lögaðila, lánardrottinn, viðskiptavin, starfsmann) sem þú vilt slá inn skráningarkenni fyrir og ​​smelltu síðan á **Skráningarkenni** á skjámyndum sem tengjast aðila, lögaðila, lánardrottni, viðskiptavini, starfsmanni til að opna síðuna **Stjórna heimilisföngum**. Á flipanum **Skattskráning** er smellt á **Bæta við** og færðar inn eftirfarandi upplýsingar um skráningarkenni.


|Svæði                |lýsing                                                |
|---------------------|-----------------------------------------------------------|
| Skráningargerð   | Skráningargerð í völdu landi/svæði.     |
| Skráningarnúmer | Skráningarkenni aðila.                                |
| lýsing         | Lýsing á skráningarnúmeri.               |
| Kafli             | Frekari upplýsingar um skráningarnúmerið. |
| Útgáfustofnun      | Yfirvaldið sem gefur út skráningarnúmerið.        |
| Dagsetning útgáfu         | Útgáfudagur skráningarnúmers.              |
| Virkt           | Gildisdagsetning fyrir skráningarnúmerið.           |
| Lok gildistíma          | Lokadagur fyrir skráningarnúmerið.          |

> [!NOTE]
> Hægt er að velja skattundanþágunúmer lögaðila, lánardrottins, viðskiptavinar úr skráningarkennum sem tengjast VSK-númeri og færa inn fyrir aðila.

## <a name="search-for-records-by-registration-id"></a>Leita að færslum eftir skráningarkenni
Leit að aðilafærslum út frá skráningarkenni er í boði á skjámyndum sem tengjast aðila, lögaðila, lánardrottni, viðskiptavini og starfsmanni. Smellt er á **Leit að skráningarkenni** til að opna síðuna **Leitarskilyrði fyrir skráningarkenni**. Tilgreindu leitarskilyrði og smelltu á **Leita**. Kerfið birtir valdar færslur úr altæku aðsetursbókinni og tengdar tegundir aðilafærslu.

## <a name="supported-registration-categories"></a>Studdir skráningarflokkar
Í eftirfarandi töflu er listi yfir studdar skráningargerðir í Finance and Operations. Ef þú þekkir reitina fyrir skráningarkenni í Microsoft Dynamics AX 2012 tengir taflan þessa reiti einnig við skráningarflokkana í Finance and Operations.

| Skráningarflokkur í Finance and Operations         |Land/svæði  | Dynamics AX 2012 liður/svæði|
|---------------------------------------------------------------|---------------------|---------------------------------|
| VSK-númer                                                        | Öll lönd Evrópusambandsins (ESB)|  Skattundanþágunúmer (lagagerð SKATTNÚMER í AX 2012 R3)|
| Kenni fyrirtækis (COID)                                          | Belgía Tékkland Eistland Ungverjaland Lettland Litháen Pólland Sviss | Fyrirtækisnúmer (EnterpriseNumber) skráningarnúmer (RegNum\_W) skráningarnúmer (RegNum\_W) skráningarnúmer (RegNum\_W) skráningarnúmer (RegNum\_W) fyrirtækiskóði (EnterpriseCode) skráningarnúmer (RegNum\_W) UID (lagagerð UID í AX 2012 R3) |
| Kenni útibús                                                     | Belgía            | Númer útibús (BranchNumber)|
| Spisová značka (skráningarnúmer, útgáfustofnun, hluti) | Tékkland     | Innsetningarnúmer (CommercialRegisterInsetNumber) Geymt í fyrirtækjaskrá (CommercialRegister) Hluti af fyrirtækjaskrá (CommercialRegisterSection)|
| Tollakenni viðskiptavinar                                           | Finnland | Tollnúmer viðskiptavinar (CustomsCustomerNumber\_FI)|
| INN                                                           | Rússneska sambandsríkið| INN (lagagerð INN í AX 2012 R3)|
| RRC                                                           | Rússneska sambandsríkið| RRC (lagagerð RRC í AX 2012 R3)|
| OKDP                                                          | Rússneska sambandsríkið| OKDP (lagagerð OKDP í AX 2012 R3)|
| OKPO                                                          | Rússneska sambandsríkið| OKPO (lagagerð OKPO í AX 2012 R3)|
| RCOAD                                                         | Rússneska sambandsríkið| RCOAD (lagagerð RCOAD í AX 2012 R3)|
| OGRN                                                          | Rússneska sambandsríkið| OGRN (lagagerð OGRN í AX 2012 R3) |
| SNILS                                                         | Rússneska sambandsríkið| SNILS (lagagerð SNILS í AX 2012 R3)|
| CIFTS                                                         | Rússneska sambandsríkið| CIFTS (lagagerð CIFTS í AX 2012 R3)|

Frekari upplýsingar um vinnslu skráningarkenna, þar á meðal áskildar forsendur, er að finna í eftirfarandi verkskráningum fyrir VSK-númer í Lifecycle Services (LCS):

-   Setja upp VSK-númer
-   Skráning VSK-númers lánardrottins
-    Leitað að aðila með VSK-kenni





