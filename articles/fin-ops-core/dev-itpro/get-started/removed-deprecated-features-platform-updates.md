---
title: Eiginleikar verkvangs sem hafa verið fjarlægðir eða eru úreltir
description: Þessi grein lýsir eiginleikum sem hafa verið fjarlægðir, eða sem fyrirhugað er að fjarlægja í vettvangsuppfærslum á fjármála- og rekstraröppum.
author: sericks007
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7d74efe7aa4f3a30c116253d647b9d7bec3b508d
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785100"
---
# <a name="removed-or-deprecated-platform-features"></a>Eiginleikar verkvangs sem hafa verið fjarlægðir eða eru úreltir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir eiginleikum sem hafa verið fjarlægðir, eða sem fyrirhugað er að fjarlægja í vettvangsuppfærslum á fjármála- og rekstraröppum.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

Ítarlegar upplýsingar um hluti í fjármála- og rekstraröppum er að finna í [Tæknilegar tilvísunarskýrslur](/dynamics/s-e/global/axtechrefrep_61). Þú getur borið saman mismunandi útgáfur þessara skýrslna til að fræðast um hluti sem hafa breyst eða verið fjarlægðir í hverri útgáfu af fjármála- og rekstrarforritum.

## <a name="feature-deprecation-effective-august-2022"></a>Eiginleikar felldir út frá og með ágúst 2022

### <a name="lifecycle-services-lcs-features-deprecated-in-august-2022"></a>Eiginleikar Lifecycle Services (LCS) voru úreltir í ágúst 2022

Sem hluti af [One Dynamics One Platform](/dynamics365-release-plan/2022wave2/finance-operations/finance-operations-crossapp-capabilities/one-dynamics-one-platform) vinnu, eru eftirfarandi LCS eiginleikar úreltir.

| Heiti eiginleika | Notað með AX 2012? | Notað með fjármála- og rekstraröppum? | Skipt út fyrir aðra eiginleika? |
|--------------|--------------------|----------------------------------------|------------------------------|
| Tilkynningar | Já | Já | Já: Borðar eru til á einstökum verkefna- og umhverfissíðum fyrir tilkynningar. |
| Skilgreiningastjórnun | Já | Nr. | Nr. |
| Hrun og sorpgreining | Já | Nr. | Nr. |
| Athugasemdir og gallar | Já | Já | Nr. |
| Áskriftin | Já | Já | Nr. |
| Office 365 | Já | Já | Já:Azure Active Directory eða Microsoft admin vefgátt. |
| Áhrifagreining | Nr. | Já | Nr. |
| Mat á heildarhagræn áhrif | Nr. | Já | Nr. |
| Þjónustubeiðnir | Nr. | Já | Já: [Sjálfsafgreiðslur](../deployment/infrastructure-stack.md) |
| Samþætting SharePoint | Já | Já | Nr. |
| Skilgreininga- og gagnastjórnun | Nr. | Já | Nr. |
| Ferlisgagnapakkar | Nr. | Já | Já: [Data Import Export Framework (DIXF)](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job) |
| Uppfærsla á umhverfi | Nr. | Já | Já: [Ein útgáfa](../lifecycle-services/oneversion-overview.md) þjónustuuppfærslur eru fáanlegar. |
| Vélbúnaðaráætlun | Já | Nr. | Nr. |
| Stærð leyfis | Já | Nr. | Nr. |
| Notkunarupplýsingar | Já | Nr. | Nr. |
| Sérstillingargreining | Já | Nr. | Nr. |
| Kerfisgreiningar | Já | Já | Nr. |
| Viðskiptaferlismódel Visio stjórnun | Já | Já | Nr. |
| AX 2012 skýjaumhverfisstjórnun | Já | Nr. | Nr. |
| RDFE Azure tengi | Já | Já | Nr. |
| AX 2012 útgáfur | Já | Nr. | Nr. |
| Vinnuhlutir geymdir í LCS geymslu | Já | Já | Nr. |
| Beiðnir um bráðabót | Já | Já | Nr. |


### <a name="transport-layer-security-tls-rsa-cipher-suites"></a>Transport Layer Security (TLS) RSA dulmálssvítur

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að fjarlægja eftirfarandi lista yfir dulmálssvítur til að vera í samræmi við núverandi öryggisreglur okkar.<br><br>TLS_RSA_WITH_AES_256_GCM_SHA384<br>TLS_RSA_WITH_AES_128_GCM_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA256<br>TLS_RSA_WITH_AES_128_CBC_SHA256<br>TLS_RSA_WITH_AES_256_CBC_SHA<br>TLS_RSA_WITH_AES_256_CBC_SHA  |
| **Skipt út fyrir aðra eiginleika?**   | Frá og með 31. janúar 2023 geta viðskiptavinir aðeins notað okkar [staðlaðar dulmálssvítur](/power-platform/admin/server-cipher-tls-requirements). Þessi breyting hefur áhrif á viðskiptavini þína og netþjóna sem hafa samskipti við netþjóna okkar, til dæmis getur hún haft áhrif á samþættingar þriðja aðila sem eru ekki í samræmi við staðlaða dulmálssvíturnar okkar. |
| **Afurðasvæði sem haft er áhrif á**         | Forrit fyrir Finance and Operations |
| **Dreifingarvalkostur**              | Skýdreifing |
| **Staða**                         | Úrelt. Viðskiptavinir verða að uppfæra netþjóna sína fyrir 31. janúar 2023. Fyrir frekari upplýsingar um uppsetningu TLS Cipher Suite röð, sjá [Stjórna flutningslagaöryggi (TLS)](/windows-server/security/tls/manage-tls).  |


## <a name="feature-deprecation-effective-june-2022"></a>Afskrift eiginleiki gildir í júní 2022

### <a name="finance-and-operations-dynamics-365-mobile-application-and-mobile-platform"></a>Fjármál og rekstur (Dynamics 365) farsímaforrit og farsímavettvangur 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að afnema fjármál og rekstrar (Dynamics 365) farsímaforritið og vettvanginn til að sameinast í einn farsímavettvang, sem er Power Apps. |
| **Skipt út fyrir aðra eiginleika?**   | Já, hægt er að byggja upp farsímaupplifun yfir fjármál og rekstrarforritsgögn með Power Platform samþættingu. Sjáðu [bloggfærsla](https://cloudblogs.microsoft.com/dynamics365/it/2022/06/03/finance-and-operations-dynamics-365-mobile-app-to-be-deprecated/) og [Að byggja upp farsímaupplifun](../power-platform/build-mobile-experiences.md) fyrir frekari upplýsingar. |
| **Afurðasvæði sem haft er áhrif á**         | Forrit fyrir Finance and Operations |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt. Lokadagsetning stuðnings er miðuð við október 2024. |


## <a name="platform-updates-for-version-10029-of-finance-and-operations-apps"></a>Uppfærslur á vettvangi fyrir útgáfu 10.0.29 af fjármála- og rekstrarforritum

### <a name="panorama-tab-style"></a>Víðmyndarflipastíll

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Síður sem fletta lárétt samræmast gamaldags útlitsmynstri sem hefur þekkt notagildi og aðgengisvandamál.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei, en aðrir flipastílar eru enn fáanlegir. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt. |


## <a name="feature-deprecation-effective-april-2022"></a>Afskrift eiginleiki gildir í apríl 2022

### <a name="xml-url-resolution-in-data-management"></a>XML URL upplausn í gagnastjórnun 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að fjarlægja stuðning við upplausn XML vefslóða þar sem þetta hefur verið skilgreint sem hugsanlegt öryggisveiki. Þetta þýðir að ytri tilföng sem tengjast XML skrám verða ekki lengur leyst.  |
| **Skipt út fyrir aðra eiginleika?**   | Nr. |
| **Afurðasvæði sem haft er áhrif á**         | Forrit fyrir Finance and Operations |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt. |

## <a name="feature-deprecation-effective-march-14-2022"></a>Afskrift eiginleiki gildir 14. mars 2022

### <a name="xslt-scripting-in-data-management"></a>XSLT forskriftir í gagnastjórnun

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stuðningur við XSLT forskriftir í gagnastjórnun er úreltur til að bæta öryggi og gagnavernd innan fjármála- og rekstrarforrita.  |
| **Skipt út fyrir aðra eiginleika?**   | Nr. Viðskiptavinir og ISVs ættu að íhuga að endurútfæra lausnir sínar byggðar á X++ tungumáli, í stað XSLT forskrifta. |
| **Afurðasvæði sem haft er áhrif á**         | Forrit fyrir Finance and Operations |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt <br><br>**Undantekning:** Viðskiptavinir sem eru að nota XLST forskriftir. Þeir geta haldið áfram að nota það þar til þeir uppfæra í útgáfu 10.0.30 eða síðar. Fyrir eldri útgáfur mun undantekningin renna út 31. janúar 2023. Viðskiptavinir með þessa undantekningu hafa fengið tilkynningu í skilaboðamiðstöðinni sem er tiltæk í Microsoft 365 Stjórnunarmiðstöð. |

## <a name="feature-removal-effective-october-2021"></a>Fjarlæging eiginleika tekur gildi í október 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-skýrslur í Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Allar aðgerðir og eftirfylgni verður framkvæmd innanhúss af verkvangnum í gegnum sjálfvirkni. Þetta krefst engrar handvirkrar íhlutunar.|
| **Skipt út fyrir aðra eiginleika?**   | Já, nú er til sjálfvirkt kerfi, sem gerir þessa möguleika úrelta. |
| **Afurðasvæði sem haft er áhrif á**         | SQL skýrslur: Núverandi DTU, núverandi DTU-upplýsingar, Fá upplýsingar um lás, Listi yfir núverandi áætlunarleiðbeiningar, Fá lista yfir fyrirspurnarauðkenni, Fá SQL fyrirspurnaráætlun fyrir ákveðið auðkenni áætlunar, Fá fyrirspurnaráætlanir og framkvæmdarstöðu, Fá takmörkunarstillingar, Fá biðtölfræði, Skrá yfir dýrustu fyrirspurnirnar |
| **Dreifingarvalkostur**              | Uppsetning í skýinu: hefur áhrif á framleiðsluumhverfi sem Microsoft stjórnar og lag 2 til lags 5 í sandkassaumhverfum. |
| **Staða**                         | Fjarlægt |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-aðgerðir í LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að úrelda nokkrar SQL-aðgerðir í LCS. Allar aðgerðir og eftirfylgni verður framkvæmd innanhúss af verkvangnum í gegnum sjálfvirkni. Þetta krefst engrar handvirkrar íhlutunar. |
| **Skipt út fyrir aðra eiginleika?**   | Já, nú er til sjálfvirkt kerfi, sem gerir þessa möguleika úrelta. |
| **Afurðasvæði sem haft er áhrif á**         | SQL aðgerðir: Búa til leiðarvísi til að þvinga fram auðkenni áætlunar, Búa til leiðarvísi til að bæta við töfluvísbendingum, Fjarlægja leiðarvísi áætlunar, Kveikja/slökkva á læsingum á síðum og aukningu á læsingum, Uppfæra talnagögn á töflu, Endurbyggja vísi, Búa til vísi |
| **Dreifingarvalkostur**              | Uppsetning í skýinu: hefur áhrif á framleiðsluumhverfi sem Microsoft stjórnar og lag 2 til lags 5 í sandkassaumhverfum. |
| **Staða**                         | Fjarlægt |


## <a name="feature-deprecation-effective-october-2021"></a>Úrelding eiginleika tekur gildi í október 2021

### <a name="show-related-document-attachments-feature"></a>Eiginleikinn „Sýna tengd skjalaviðhengi“

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eiginleikinn skilaði óvæntum niðurstöðum. |
| **Skipt út fyrir aðra eiginleika?**   | Nr. Allar frekari áætlanir varðandi þessa virkni verða tilkynntar í gegnum hefðbundna útgáfutímabilið okkar. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari - Upplifun skjalaviðhengis |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt  |

## <a name="platform-updates-for-version-10023-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.23 af fjármála- og rekstrarforritum

### <a name="ondbsynchronize-event"></a>OnDBSynchronize-tilvik

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin stýring er til að framvkæma þetta tilvik. |
| **Skipt út fyrir aðra eiginleika?**   | Já, færa núverandi aðferðir sem eru áskrifendur að **OnDBSynchronize** atburður í SysSetup aukinn bekk. |
| **Afurðasvæði sem haft er áhrif á**         | Gagnagrunnssamstilling |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt. Fyrirhugaður lokadagur er í október 2022. |


### <a name="systemnotificationsmanageraddnotification-api"></a>SystemNotificationsManager.AddNotification API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Microsoft þarf viðbótarfæribreytur þegar tilkynningum er bætt við. |
| **Skipt út fyrir aðra eiginleika?**   | Já, API **SystemNotificationsManager.AddSystemNotification()**. Þetta API krefst þess að þú stillir sérstaklega ExpirationDateTime og RuleID fyrir myndaðar tilkynningar. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt. Fyrirhugaður lokadagur er í apríl 2023. |

## <a name="platform-updates-for-version-10021-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.21 af fjármála- og rekstrarforritum

### <a name="skype-for-business-online-support"></a>Stuðningur við Skype for Business Online

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skype for Business Online hefur verið tekið úr umferð. Frekari upplýsingar er að finna í [Þjónusta Skype for Business Online hefur verið tekin úr umferð](https://techcommunity.microsoft.com/t5/microsoft-teams-blog/the-skype-for-business-online-service-has-retired/ba-p/2596601). |
| **Skipt út fyrir aðra eiginleika?**   | Ekki sem stendur. En við gætum hugsanlega bætt virkni Teams við í framtíðinni.|
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt. Slökkt hefur verið á stillingunni **Skype virkjað** frá og með útgáfu 10.0.21. Stefnt er að því að fjarlægja þessa stillingu í apríl 2022, en eiginleikinn mun hinsvegar hætta að virka þegar Skype-teymið slekkur á þjónustunni. |
 
## <a name="feature-deprecation-effective-august-2021"></a>Eiginleikar felldir út frá og með ágúst 2021

### <a name="microsoft-azure-sql-reports-in-lifecycle-services-lcs"></a>Microsoft Azure SQL-skýrslur í Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Allar aðgerðir og eftirfylgni verður framkvæmd innanhúss af verkvangnum í gegnum sjálfvirkni. Þetta krefst engrar handvirkrar íhlutunar.|
| **Skipt út fyrir aðra eiginleika?**   | Já, nú er til sjálfvirkt kerfi, sem gerir þessa möguleika úrelta. |
| **Afurðasvæði sem haft er áhrif á**         | SQL skýrslur: Núverandi DTU, núverandi DTU-upplýsingar, Fá upplýsingar um lás, Listi yfir núverandi áætlunarleiðbeiningar, Fá lista yfir fyrirspurnarauðkenni, Fá SQL fyrirspurnaráætlun fyrir ákveðið auðkenni áætlunar, Fá fyrirspurnaráætlanir og framkvæmdarstöðu, Fá takmörkunarstillingar, Fá biðtölfræði, Skrá yfir dýrustu fyrirspurnirnar |
| **Dreifingarvalkostur**              | Uppsetning í skýinu: hefur áhrif á framleiðsluumhverfi sem Microsoft stjórnar og lag 2 til lags 5 í sandkassaumhverfum. |
| **Staða**                         | Úrelt: Fyrirhugaður lokadagur er í október 2021. |

### <a name="azure-sql-actions-in-lcs"></a>Azure SQL-aðgerðir í LCS

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að úrelda nokkrar SQL-aðgerðir í LCS. Allar aðgerðir og eftirfylgni verður framkvæmd innanhúss af verkvangnum í gegnum sjálfvirkni. Þetta krefst engrar handvirkrar íhlutunar. |
| **Skipt út fyrir aðra eiginleika?**   | Já, nú er til sjálfvirkt kerfi, sem gerir þessa möguleika úrelta. |
| **Afurðasvæði sem haft er áhrif á**         | SQL aðgerðir: Búa til leiðarvísi til að þvinga fram auðkenni áætlunar, Búa til leiðarvísi til að bæta við töfluvísbendingum, Fjarlægja leiðarvísi áætlunar, Kveikja/slökkva á læsingum á síðum og aukningu á læsingum, Uppfæra talnagögn á töflu, Endurbyggja vísi, Búa til vísi |
| **Dreifingarvalkostur**              | Uppsetning í skýinu: hefur áhrif á framleiðsluumhverfi sem Microsoft stjórnar og lag 2 til lags 5 í sandkassaumhverfum. |
| **Staða**                         | Úrelt: Fyrirhugaður lokadagur er í október 2021. |

## <a name="feature-deprecation-effective-may-2021"></a>Tilkynning um úreldingu eiginleika tekur gildi í maí 2021

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Globalization portal í Lifecycle Services (LCS)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að afnema Globalization gáttina í LCS þar sem þessi eiginleiki hefur komið í stað annarrar LCS-byggðrar þjónustu. |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika er skipt út fyrir LCS [Vandamálaleit](../lifecycle-services/issue-search-lcs.md) og [Innsendingarþjónustu vegna lögboðinnar viðvörunar Dynamics](../lcs-solutions/submit-localization-alerts.md). |
| **Afurðasvæði sem haft er áhrif á**         | Staðfæringargátt í LCS|
| **Dreifingarvalkostur**              | Uppsetning skýs |
| **Staða**                         | Úrelt: Fyrirhugaður lokadagur er í maí 2022. |


## <a name="feature-removed-effective-january-28-2021"></a>Eiginleiki fjarlægður frá og með 28. janúar 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Runuvinnsla fyrir endurröðun SQL-atriðaskráar

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þessi eiginleiki hefur verið fjarlægður til þess að draga úr rekstrar-, eftirlits- og viðhaldskostnaði við stjórnun atriðaskráar eftir viðskiptavini. |
| **Skipt út fyrir aðra eiginleika?**   | Héðan í frá mun Microsoft-þjónusta sjá um stjórnun atriðaskráar. Þetta gerist samfellt án þess að hafa áhrif á vinnuálag notanda. |
| **Afurðasvæði sem haft er áhrif á**         | Forrit fyrir Finance and Operations|
| **Dreifingarvalkostur**              | Uppsetning í skýinu - hefur áhrif á framleiðsluumhverfi sem Microsoft stjórnar og lag 2 til lags 5 í sandkassaumhverfum. |
| **Staða**                         | Þessi eiginleiki hefur verið fjarlægður. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.17 af fjármála- og rekstrarforritum


### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Til að styðja við nýjustu útgáfur af Visual Studio þarf að gera nokkrar breytingar á viðbótum X++ fyrir Visual Studio. Þessar breytingar samhæfast ekki Visual Studio 2015. |
| **Skipt út fyrir aðra eiginleika?**   | Visual Studio 2017 kemur í stað Visual Studio 2015 sem uppsett og áskild útgáfa. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Við uppfærslu verða fyrri verkfæri X++ fjarlægð úr Visual Studio 2015 og uppfærðu verkfærin verða ekki sett upp í Visual Studio 2015. Hýst smíði verður ekki fyrir áhrifum. Fyrir sýndarvélar smíðar þarf sölukeðja smíðar (skilgreining smíðar) að vera uppfærð handvirkt til að breyta tengslum úr MSBuild 14.0 (Visual Studio 2015) í MSBuild 15.0 (Visual Studio 2017) eins og lýst er í [Uppfæra eldri sölukeðju í Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Notandapersóna notanda 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Notandapersóna notanda sem birtist hægra megin á yfirlitsstikunni var sótt með API úr yfirskriftarstýringu Dynamics 365 sem hefur verið úreld. |
| **Skipt út fyrir aðra eiginleika?**   | Notendur munu sjá upphafsstafi sína í hring á yfirlitsstikunni í staðinn. Þetta er sýnt á sama hátt og í þróunarvélum. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með útgáfu 10.0.17 |

### <a name="enterprise-portal-ep-deprecation"></a>Úrelding Enterprise Portal  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lýsigagnagripirnir sem tengjast Dynamics AX 2012 Enterprise Portal (EP) hefur verið úrelt, þar sem EP var aldrei stutt í fjármála- og rekstraröppunum. |
| **Skipt út fyrir aðra eiginleika?**   | Nr. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Áætlað er að allur EP-kóði verði fjarlægður í október 2021 útgáfu. |

## <a name="deprecation-effective-december-2020"></a>Afskrift gildir í desember 2020

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 stuðningi við Dynamics 365 hefur verið hætt

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Gildir í desember 2020, Microsoft Internet Explorer 11 stuðningur fyrir allar Dynamics 365 vörur og Dynamics Lifecycle Services (LCS) er úreltur og Internet Explorer 11 verður ekki stutt eftir ágúst 2021.<br><br>Þetta mun hafa áhrif á viðskiptavini sem nota Dynamics 365 vörur og LCS sem eru hannaðar til að nota í gegnum Internet Explorer 11 tengi. Eftir ágúst 2021,Internet Explorer 11 verður ekki stutt fyrir slíkar Dynamics 365 vörur og LCS. |
| **Skipt út fyrir aðra eiginleika?**   | Við mælum með því að viðskiptavinir skipti yfir í Microsoft Edge.|
| **Afurðasvæði sem haft er áhrif á**         | Allar Dynamics 365 vörur og LCS |
| **Dreifingarvalkostur**              | Allir|
| **Staða**                         | Úrelt: Internet Explorer 11 verður ekki stutt eftir ágúst 2021.|

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.15 af fjármála- og rekstrarforritum

### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio -viðbót til að nota flýtileiðréttingar

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bráðabætur lýsigagna eru ekki lengur studdar með uppfærsluþjónustum [One Version](../../fin-ops/get-started/one-version.md) sem kynntar voru í júlí 2018 með útgáfu 8.1. |
| **Skipt út fyrir aðra eiginleika?**   | Stakar bráðabætur lýsigagna eru ekki í boði fyrir studdar útgáfur. Uppsafnaðar gæðauppfærslur eru notaðar í staðinn. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio viðbætur |
| **Dreifingarvalkostur**              | Sýndarvélar þróunar |
| **Staða**                         | Með útgáfu 10.0.15 er viðbótin ekki lengur með í Visual Studio-verkfærum. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.14 af fjármála- og rekstrarforritum

### <a name="online-users-page"></a>Síða nettengds notanda 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta er eldri síða sem var byggð á fyrri uppsetningu biðlara/þjóns. Upplýsingarnar á þessari síðu eru ekki alltaf réttar, sem getur verið ruglingsleg og villandi. |
| **Skipt út fyrir aðra eiginleika?**   | Við munum birta nýja síðu í síðari uppfærslu.|
| **Afurðasvæði sem haft er áhrif á**         | Kerfisstjórnun |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Frá október 2021 verður þetta fjarlægt.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.13 af fjármála- og rekstrarforritum


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Sérstilltur kóði skilgreindur í eiginleikum SSRS-skýrslu 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Almennt býður sérstilltur kóðir upp á takmarkaðan ávinning og þarf á sama tíma umtalsverða tilfangagetu og útreikning fyrir stuðning. Sérstilltur kóði er fyrst og fremst notaður af skýrsluhöfundum til að kalla á opinberar aðferðir úr samsetningu sérstilltra kóða. Skýjaþjónustan styður hinsvegar ekki tilvísanir í sérstilltar samsetningar fyrir SSR-skýrslur. |
| **Skipt út fyrir aðra eiginleika?**   | Skýrsluhöfundar geta valið að halda áfram að vísa í almenn .NET API fyrir útreiknings-, umreiknings- og sniðsaðgerðir úr hvers kyns textareitasegð. Frekari upplýsingar eru í [Bæta kóða við skýrslu (SSRS)](/sql/reporting-services/report-design/add-code-to-a-report-ssrs).  |
| **Afurðasvæði sem haft er áhrif á**         | Undirsafn af skýrsluhönnunum forrits skilgreind í RDL sem inniheldur sérstilltan kóða. |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Í útgáfu 10.0.13 byrjar þýðandinn að gefa út viðvörun vegna tilvika þar sem sérstilltur kóði greinist í SSRS-skýrsluskilgreiningu. Til að lagfæra vandamálið skal opna skilgreiningu skýrsluhönnunar og fjarlægja alla sérstillta kóðaggervinga. Þessari viðvörun verður skipt út fyrir þýðingarvillu í framtíðaruppfærslu.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Uppfærsla á þremur jQuery-þáttasöfnum 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Verið er að uppfæra þrjú jQuery-þáttasöfn í tengslum við öryggisuppfærslur og uppfærslu upplýsinga.   
| **Skipt út fyrir aðra eiginleika?**   | Eftirfarandi söfn eru uppfærð: jQuery (að útgáfu 3.5.0 frá útgáfu 2.1.4), jQuery UI (að útgáfu 1.12.1 frá útgáfu 1.11.4), jQuery qTip (að útgáfu 3.0.3 frá útgáfu 2.2.1). jQuery hefur birt leiðbeiningar um flutninga á netinu.  |
| **Afurðasvæði sem haft er áhrif á**         | Stækkanlegt stjórntæki, sérsniðinn JavaScript-kóði sem nýtir API sem er búið að úrelda eða fjarlægja |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Með útgáfu 10.0.13/uppfærslu 37 geta viðskiptavinir fært nýjustu söfnin með því að virkja eiginleikann „Uppfæra þrjú jQuery-þáttasöfn“. Áskilið verður að flytja nýju söfnin með útgáfunni í apríl 2021 til að bjóða upp á tíma fyrir flutning viðeigandi API.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Fyrirliggjandi hnitanetsstýring/forceLegacyGrid() API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Verið er að skipta út núverandi hnitanetsstýringu fyrir nýju hnitanetsstýringuna. |
| **Skipt út fyrir aðra eiginleika?**   | [Ný hnitanetsstýring](../..//fin-ops/get-started/grid-capabilities.md) |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Í útgáfu 10.0.13 er nýja hnitanetsstýringin almennt í boði og viðskiptavinir geta kveikt á þessum eiginleika ef þeir vilja. Nýja netstýringin verður sjálfgefið sett á í útgáfu fyrir október 2021 og er stefnt að því að hún verði áskilin í apríl 2022. Þegar nýja hnitanetsstýringin verður áskilin verður **forceLegacyGrid()** API ekki lengur virt. |

### <a name="personalization-without-saved-views"></a>Sérstillingar án vistaðra yfirlita 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Undirkerfi sérstillinga hefur verið yfirfarið með eiginleikanum fyrir vistuð yfirlit þannig að afköstin verði betri og boðið verður upp á fleiri möguleika. |
| **Skipt út fyrir aðra eiginleika?**   | Vistuð yfirlit |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Í útgáfu 10.0.13/verkvangsuppfærslu 37 er eiginleiki vistaðra yfirlita almennt í boði og viðskiptavinir geta kveikt á honum ef þeir vilja. Eiginleiki vistaðra yfirlita verður áskilinn í útgáfu í október 2021. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.12 af fjármála- og rekstrarforritum

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Viðbætur í hnitaneti eða hópstýringarsniði sem innihalda ógildar reitartilvísanir

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Gagnaflokkseiginleikinn í hnitaneti eða hópstýringum er notaður til að birta sjálfkrafa alla reiti reitahópsins. Hnitanet eða hópstýring sem bætt var við með viðbót getur innihaldið reiti sem eru ekki lengur skilgreindir í reitahópnum eða það gætu verið reitir sem vantar sem eru skilgreindir í reitahópnum. Þetta getur valdið ósamkvæmri hegðun á keyrslutíma. Palluppfærslur fyrir útgáfu 10.0.12 af fjármála- og rekstrarforritum flokka þetta mál nú sem þýðanda *viðvörun*. Til að laga þetta vandamál skal opna snið viðbótar og vista hana.
| **Skipt út fyrir aðra eiginleika?**   | Þýðingarviðvörunin verður skipt út fyrir þýðingarvillu í framtíðaruppfærslu. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Viðvörun um þýðanda er kynnt í vettvangsuppfærslum fyrir útgáfu 10.0.12 af fjármála- og rekstraröppum. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Palluppfærslur fyrir útgáfu 10.0.11 af fjármála- og rekstrarforritum

### <a name="explicit-safe-lists-for-self-service-environments"></a>Öruggir listar fyrir sjálfsafgreiðsluumhverfi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ferlið við að færa IP-tölur yfir á undanþágulista hefur breyst. Sjálfsafgreiðsla styður ekki lengur undanþágulista IP-talna. |
| **Skipt út fyrir aðra eiginleika?**   | Nánari upplýsingar er að finna í [Skilgreining Azure Active Directory Skilyrðisbundinn aðgangur](/appcenter/general/configuring-aad-conditional-access).|
| **Afurðasvæði sem haft er áhrif á**         | Öryggi |
| **Dreifingarvalkostur**              | Ský |
| **Staða**                         | Úrelt: Þessi eiginleiki er að fullu úreltur fyrir uppsetningar sjálfsafgreiðslu. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Til að styðja við nýjustu útgáfur af Visual Studio þarf að gera nokkrar breytingar á viðbótum X++ fyrir Visual Studio. Þessar breytingar samhæfast ekki Visual Studio 2015. |
| **Skipt út fyrir aðra eiginleika?**   | Visual Studio 2017 kemur í stað Visual Studio 2015 sem uppsett og áskild útgáfa. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Sýndarvélar virkjaðar í útgáfu 10.0.13 (verkvangsuppfærsla 37) eða nýrri innihalda Visual Studio 2017. Útgáfa 10.0.16 (verkvangsuppfærsla 40) er nýjasta útgáfa með stuðningi fyrir Visual Studio 2015. Ekki er hægt að uppfæra sýndarvélar með aðeins Visual Studio 2015 í útgáfu 10.0.17 (verkvangsuppfærsla 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Reitahópar sem innihalda ógilda tilvísanareiti

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Reitahópar í skilgreiningum á lýsigögnum töflu geta innihaldið reitatilvísanir sem eru ekki gildar. Ef þessi reitahópar eru uppsettir geta þeir valdið keyrsluvillu í Financial Reporting og Microsoft SQL Server Reporting Services (SSRS). Uppfærsla pallsins 23 kynnti þýðanda *viðvörun* sem gerði kleift að taka á þessu lýsigagnavandamáli. Palluppfærslur fyrir útgáfu 10.0.11 af fjármála- og rekstrarforritum flokka þetta mál sem þýðanda *villa*.<p>Til að laga þetta vandamál skal fylgja þessum skrefum.</p><ol><li>Fjarlægja ógilda tilvísunarreitinn úr skilgreiningu töflureitahópsins.</li><li>Endurþýða.</li><li>Gakktu úr skugga um að tekið sé á öllum villum.</li></ol> |
| **Skipt út fyrir aðra eiginleika?**   | Þessi þýðingarvilla kemur í staðinn fyrir viðvörun þýðandans.  |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Þjálfaraviðvörunin er þýðandavilla í vettvangsuppfærslum fyrir útgáfu 10.0.11 af fjármála- og rekstrarforritum. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV leyfi búin til með því að nota endamerkja reikniritið SHA1

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ferlið til að búa til óháð leyfi fyrir hugbúnaðarframleiðanda (ISV) hefur breyst. Fyrir frekari upplýsingar, sjá [Óháð leyfi fyrir hugbúnaðarsöluaðila (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Skipt út fyrir aðra eiginleika?**   | Já. Notaðu Windows PowerShell til að búa til leyfi. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Afskrifað: ISV leyfi sem voru búin til með því að nota endamerkja reiknirit SHA1. Þessi reiknirit voru háð vottorðum sem voru búin til með því að nota gagnaforritið MakeCert og sú veita hefur verið úrelt.<br><br>Afskrifað: Notkun SHA1 í öryggisskyni eða endamerkja tilgangi. SHA1 hættir að virka snemma árs 2021. Þess vegna ætti það ekki að nota það lengur.<br><br>Fjarlægt: Stuðningur við flutningslagöryggi (TLS) 1.0 og TLS 1.1 komandi eða sendar beiðnir. |

## <a name="platform-update-32"></a>Update 32 fyrir verkvang

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Gluggi fyrir breytingu á verkflæðisbeiðni inniheldur ekki lengur fellivalmynd fyrir val á notendum

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta var öryggisatriði vegna þess að beiðni um breytingar var hægt að senda í ógáti til notanda. Þetta var einnig nothæfismál vegna þess að það neyddi notandann til að ákvarða hver upphafsmaður verkflæðisins var og velja þá handvirkt.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei |
| **Afurðasvæði sem haft er áhrif á**         | Verkflæði |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Listi notendavalsins var fjarlægður úr valmyndinni um breytingu á beiðni í uppfærslu á verkvangi 32. Beiðnir um breytingu verða sjálfkrafa sendar til höfundar eins og til er ætlast. Fyrir frekari upplýsingar um þessa virkni, sjá [Verkþættir í samþykktarferli verkflæðis](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Innfelldir boratenglar eru ekki lengur studdir í skjöluðum skjölum sem gefin eru af þjónustunni í skýinu 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vefslóðir sem eru felldar inn í skjöl sem þjónustan veitir geta innihaldið viðkvæm viðskiptagögn. Við erum að fjarlægja stuðning við innbyggða boratengla í skjölum sem öryggisráðstöfun til að vernda gögn viðskiptavinarins frekar. Notendur munu einnig njóta góðs af bættum árangri meðan þeir framleiða skjöl gagnvirkt vegna þessarar breytinga.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei |
| **Afurðasvæði sem haft er áhrif á**         | Skýrslugerð |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Þessi aðgerð er virkur tekinn úr þjónustunni.<br><br>Nútíma viðskiptavinurinn býður upp á fjölmarga möguleika til að framleiða áhorf sem innihalda tengla sem myndast sjálfkrafa til að aðstoða við siglingar forritsins. Mælt er með pagineruðum gögnum sem þjónustan veitir vegna utanaðkomandi samskipta sem eru send, geymd og geymd og prentuð fyrir viðtakendur. Við höfum bætt reynsluna af því að forskoða skjöl beint í vafranum, sem býður upp á beinan aðgang að prenturum á staðnum. Fyrir frekari upplýsingar, sjá [Forskoða PDF skjöl með innbyggðri skoðun](../analytics/preview-pdf-documents.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir
Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../migration-upgrade/deprecated-features.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

