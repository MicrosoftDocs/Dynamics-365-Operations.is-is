---
title: "Skráningarkenni"
description: "Þetta efni veitir upplýsingar um uppsetningu og notkun skráningu Kenni."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 32cd09975861083b8940368ed53ae16e89bcd748
ms.lasthandoff: 03/31/2017


---

# <a name="registration-ids"></a>Skráningarkenni

Þetta efni veitir upplýsingar um uppsetningu og notkun skráningu Kenni.

Mörg lönd og svæði hafa mismunandi reglum og kröfum fyrir skráningu skráningarnúmer eða Kenni. Þetta efnisatriði gefur yfirlit yfir stillingar sem þarf og úrvinnslu studd skráningargerðum aðila í aðra Evrópska löndum/svæðum. Öll lönd/svæði hafa þarfir þeirra til að styðja mismunandi landsbundnar aðgerðir sem tengjast skráningarnúmer útvegar skrifstofur mismunandi stöðu. Skráningarnúmer meðal, kennitala (SSN), auðkennisnúmer skatts (TIN) og Evrópska VSK kenni ESB VSK. Eiginleikinn veitir sameinuðum ramma fyrir öll lönd í öllum taki í lykli landsbundnar þarfir evrópskra sumum svæðum. Eftirfarandi kaflar lýsa upplýsinga sem er notað fyrir uppsetningu og vinnslu Kenni skráningu heildarflæðið.

## <a name="registration-type-creation"></a>Stofnun gerð skráningar
Áður en hægt er að færa inn Kenni skráningu, verður að setja upp gerðir skráningu mismunandi gerðir af skráningarnúmer hverja aðila er settur fyrir. Fara í **fyrirtækisstjórnun**&gt;**Altækrar aðsetursbókar**&gt;**skráningargerðum**&gt;**skráningargerðum** síðu til að stofna og stjórna skráningargerðum fyrir lánardrottna, viðskiptavini, starfsmenn og lögaðila í mismunandi löndum/svæðum.

|Svæði                 |lýsing      |
|------------------------------|----------------------------|                                                                           
| Nafn                | Heiti á gerð skráningar. |                                                                           
| lýsing         | Lýsing á gerð skráningar. |
| Land/svæði      | Einkvæmt auðkenni lands/svæðis.|
| Skattyfirvöld       | Skattyfirvaldið sem er tengd gerð skráningar.|
| Takmarkað við       | Gerð takmörkunarlista við skattskráningargerðarinnar: Ekkert, Aðili, Fyrirtæki.|
| Snið              | Snið villuleit fyrir þá gerð skráningar.|
| Hægt að uppfæra      | Skilgreinir hvort hægt er að uppfæra skráningarnúmerið fyrir gerð skráningar eftir að hún er færð inn.|
| Einkvæmt              | Skilgreinir hvort er einkvæmt númer fyrir gerð skráningar. |
| Aðalaðsetur fyrir land | Ef aðili er tengd við eina eða fleiri aðsetur sérstaklega land og Kenni skráningu gildir fyrir allar þessar aðsetur, þarf að tilnefna eitt netfang sem aðalaðsetur fyrir land. Aðeins er hægt að skrá einn Kenni sem aðalaðsetur. Skilgreinir hvort hægt er að færa inn skráningarnúmer aðeins fyrir aðalaðsetur fyrir aukaaðsetur lands. |

## <a name="assign-a-registration-type-to-a-registration-category"></a>Úthluta gerð færslubókarskráningar skráningu tegund
Tegund skráningu er kenni lands/svæðis skráningu samþykkt til að nota sérstaklega land/svæði fyrir skatta, tollar og öðrum tilgangi. Þessi tegund skilgreinir villuleitarreglur Kenni tiltekna skráning (þar á meðal vartölur o. s. frv.) og Kenni meðtalningu skráningu mismunandi skýrslur. Notið síðan **fyrirtækisstjórnun**&gt;**Altækrar aðsetursbókar**&gt;**skráningargerðum**&gt;**Skráningu tegundir** til að úthluta tegund studd skráningu skráningargerð tilteknu landi.

| Svæði            | lýsing|
|-----------------------|----------------|
| Skráningargerð     | Skráning gerð sérstaklega land/svæði.|
| Takmarkað við         | Gerð takmörkunarlista við skattskráningargerðarinnar: Ekkert, Aðili, Fyrirtæki.|
| Skráningarflokkur | Skráning einkvæmt kenni samþykkt til að nota í lands. Full lista yfir studd í AX7.1 tegundir er hér að neðan. |

## <a name="enter-registration-ids-for-global-address-book-records"></a>Færið inn Kenni skráningu fyrir færslur í Altæka aðsetursbók
Altæka vistfangabókin (GAB) í Microsoft Dynamics 365 aðgerða inniheldur upplýsingar um sameinaða aðsetur fyrir viðskiptavini, lánardrottna, tengiliði, viðskiptasambönd og lögaðila. Nánari upplýsingar eru í [altækrar aðsetursbókar yfirlit](/dynamics365/operations/organization-administration/overview-global-address-book). Færslur aðila sem eru geymdar í altæku aðsetursbókinni getur innihaldið einn eða fleiri færslum. Þessi aðsetur eru notuð í mismunandi tilgangi, svo sem vegna reikningsgerðar eða afhendingar. Hægt er að setja upp Kenni skráningu fyrir aðsetursupplýsingar fyrir viðskiptavini, lánardrottna, starfsmenn og lögaðila. Finna skrá aðila (lögaðila, lánardrottinn, viðskiptavinur, starfsmanns) sem óskað er að færa inn Kenni afgreiðslukassa, og smellið síðan á **Skráning Kenni** í skjámyndum sem tengjast aðila lögaðila, lánardrottinn, viðskiptavinur, starfsmanns til að opna í **Stjórna aðsetrum** síðu. Á við **vsk-skráningu** flipanum, smellið **Bæta**, og færa inn eftirfarandi upplýsingar um kenni skráningu.

|Svæði                |lýsing                                                |
|---------------------|-----------------------------------------------------------|
| Skráningargerð   | Gerð skráningar valið land/svæði.     |
| Skráningarnúmer | Kenni aðila skráningu                                |
| lýsing         | Lýsing á skráningarnúmer.               |
| Kafli             | Frekari upplýsingar um skráningarnúmer. |
| Útgáfustofnun      | Yfirvald sem gaf út númerið skráningu.        |
| Dagsetning útgáfu         | Dagsetning útgáfu fyrir skráningarnúmer.              |
| Virkt           | Gildisdagsetning skráningarnúmer.           |
| Lok gildistíma          | Lokadagur fyrir skráningu.          |

> [!NOTE]
> Skattur skattundanþágunúmer lögaðila, lánardrottinn, viðskiptavinur er hægt að velja úr skráning Kenni tengdar VSK-Kenni og færa inn aðilans.

## <a name="search-for-records-by-registration-id"></a>Leita að færslum með Auðkenni skráningar
Leita að aðilafærslu skráning Kenni er tiltækur í skjámyndunum sem tengjast aðila lögaðila, lánardrottinn, viðskiptavinur og starfsmaður á grundvelli. Smellið á **leit Skráningu** til að opna í **leitarskilyrði Skráningu Kenni** síðu. Tilgreinið leitarskilyrði og smellið á **Finna**. Kerfið verður að birta valdar færslur úr altækrar aðsetursbókar og tengdar gerðir aðilafærslu.

## <a name="supported-registration-categories"></a>Studd skráningu tegundir
Í eftirfarandi töflu er listi yfir gerðir skráningu studd í Dynamics 365 fyrir Aðgerðir. Ef þú verið góðum við reiti Microsoft Dynamics AX 2012 skráningar Kennum, varpar í þessari töflu einnig þessum svæðum til 365 Dynamics fyrir skráningu tegundir Aðgerða.

| 365 dynamics fyrir Skráningu Aðgerðir tegund         |Land/svæði  | Dynamics AX 2012 hugtak/svæði|
|---------------------------------------------------------------|---------------------|---------------------------------|
| VSK-númer                                                        | Allar af Innan Evrópusambandsins (ESB) landa|  Skattundanþágunúmer (lagagerð Skattkenni í AX2012 R3)|
| Kenni fyrirtækis (COID)                                          | Tékkland Belgíu Estonia Ungverjaland Latvia Lithuania Pólland Sviss | Númer (EnterpriseNumber) Skráningu fyrirtækisnúmer (RegNum\_V) skráningarnúmer (RegNum\_V) skráningarnúmer (RegNum\_V) skráningarnúmer (RegNum\_V) skráningarnúmer Enterprise-kóði (EnterpriseCode) (RegNum\_V) UID (lagagerð einkvæmt Auðkenni í AX2012 R3) |
| Kenni útibús                                                     | Belgía            | Útibúsnúmer (BranchNumber)|
| Spisová značka (skráningarnúmer, Útgáfustofnun, Hluta) | Tékkland     | Númer (CommercialRegisterInsetNumber) Kept inset á heildarsöluverðmæti skrá (CommercialRegister) Hluta afgreiðslukassa heildarsöluverðmæti (CommercialRegisterSection)|
| Tollakenni viðskiptavinar                                           | Finnland | Tollnúmer viðskiptavinar (CustomsCustomerNumber\_FI)|
| INN                                                           | Rússneska sambandsríkið| INN (lagagerð INN í AX2012 R3)|
| RRC                                                           | Rússneska sambandsríkið| RRC (lagagerð RRC í AX2012 R3)|
| OKDP                                                          | Rússneska sambandsríkið| OKDP (lagagerð OKDP í AX2012 R3)|
| OKPO                                                          | Rússneska sambandsríkið| OKPO (lagagerð OKPO í AX2012 R3)|
| RCOAD                                                         | Rússneska sambandsríkið| RCOAD (lagagerð RCOAD í AX2012 R3)|
| OGRN                                                          | Rússneska sambandsríkið| OGRN (lagagerð OGRN í AX2012 R3) |
| SNILS                                                         | Rússneska sambandsríkið| SNILS (lagagerð SNILS í AX2012 R3)|
| CIFTS                                                         | Rússneska sambandsríkið| CIFTS (lagagerð CIFTS í AX2012 R3)|

Nánari upplýsingar um skráningu Kenni vinnslu, þar á meðal nauðsynlegt skilyrði í eftirfarandi verkskráningu fyrir Auðkenni VSK í Lifecycle Services (LCS):

-   Setja upp VSK-númer
-   Kenni VSK-skráningu lánardrottins
-    Leitað að aðila með VSK-kenni



