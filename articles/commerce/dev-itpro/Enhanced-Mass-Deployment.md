---
title: Fjölvirkjun á innsigluðum íhlutum fyrir sjálfsafgreiðslu í Commerce
description: Þetta efni útskýrir hvernig á að nota ramma fyrir sjálfsafgreiðsluíhlutauppsetningarforrit til að setja upp og þjónusta uppsetningar hljóðlaust.
author: jashanno
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 5cb27fd0ea366d12c8bd6ee1cdb0c6d584375862
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2022
ms.locfileid: "8742589"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Fjölvirkjun á innsigluðum íhlutum fyrir sjálfsafgreiðslu í Commerce

[!include [banner](../includes/banner.md)]

Þetta efni á við um innsiglaða ramma, íhlutauppsetningarforrit sem eru gefin út í hverjum mánuði, frá og með útgáfunni 10.0.18, og eru gerð aðgengileg í Samnýtt eignasafn í Microsoft Dynamics Lífsferilsþjónusta (LCS). Athugaðu að fyrstu útgáfur þessara nýju uppsetningarforrita eru merktar sem **(Forskoðun)**. Hins vegar er eini tilgangurinn með þessari tilnefningu að aðgreina nýju uppsetningarforritin á meðan Microsoft ákvarðar hvort það séu einhverjar viðbótarkröfur um virkni til að nota þau. Það þýðir ekki að uppsetningartækin séu ekki gild fyrir framleiðslu. Byggt á útgáfu þessara nýju uppsetningarforrita ætlar Microsoft að afnema gömlu (eldri) uppsetningartækin í eða í kringum október 2023. 

Þetta efnisatriði útskýrir hvernig á að nota nýju uppsetningarforritin til að framkvæma hljóðlausar uppsetningar og þjónustuuppfærslur með skipanalínubreytingum. Þessi rök gera þér kleift að framkvæma fjöldadreifingu á nokkra mismunandi vegu.

> [!NOTE]
> Nýju sjálfsafgreiðslu, lokuðu uppsetningartækin verða ekki aðgengileg í höfuðstöðvunum og er aðeins hægt að hlaða niður í gegnum LCS.

## <a name="delimiters-for-mass-deployment"></a>Afmörkun fyrir fjöldadreifingu

Eftirfarandi tafla sýnir afmörkunina sem hægt er að nota við framkvæmd skipanalínunnar.


| Skiltákn                 | Lýsing |
|---------------------------|-------------|
| --AadTokenIssuerPrefix | Forskeytið fyrir Microsoft Azure Active Directory (Azure AD) táknaútgefanda. |
| --AsyncClientAadClientId | The Azure AD auðkenni viðskiptavinar sem Async Client ætti að nota í samskiptum við höfuðstöðvar. |
| --AsyncClientAppInsightsInstrumentationKey | Async viðskiptavinurinn AppInsights hljóðfæralykill. |
| --AsyncClientCertFullPath | Fullsniðin URN slóð sem notar þumalfingur sem leitarmælikvarða fyrir Async Client Identity vottorðsstaðsetningu sem ætti að nota til að auðkenna með Azure AD fyrir samskipti við höfuðstöðvar. Til dæmis,`store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` er rétt sniðið vefslóð. Gildið **\<MyThumbprint\>** verður skipt út fyrir þumalfingur skírteinisins sem ætti að nota. Ekki nota þessa breytu ásamt **-AsyncClientCertThumbprint** breytu. |
| --AsyncClientCertThumbprint | Þumalfingursmerki Async Client Identity vottorðsins sem ætti að nota til að auðkenna með Azure AD fyrir samskipti við höfuðstöðvar. Þetta þumalfingur verður notað til að leita í **LocalMachine/My Store** staðsetningu og nafn til að finna rétta vottorðið til að nota. Ekki nota þessa breytu ásamt **-AsyncClientCertFullPath** breytu. |
| --ClientAppInsightsInstrumentationKey | Viðskiptavinurinn AppInsights hljóðfæralykill. |
| --CloudPosAppInsightsInstrumentationKey | Cloud POS AppInsights hljóðfæralykill. |
| --Config | Stillingarskráin sem ætti að nota við uppsetningu. Dæmi um skráarheiti er **Contoso.CommerceScaleUnit.xml**. |
| --CposAadClientId | The Azure AD auðkenni viðskiptavinar sem Cloud POS ætti að nota við virkjun tækisins. Þessi færibreyta er ekki nauðsynleg fyrir innleiðingu á staðnum. |
| --Tæki | Auðkenni tækisins, eins og sýnt er á **Tæki** síðu í höfuðstöðvum. |
| --EnvironmentId | Auðkenni umhverfisins. |
| --HardwareStationAppInsightsInstrumentationKey | Vélbúnaðarstöðin AppInsights hljóðfæralykill. |
| --Setja upp | Færibreyta sem tilgreinir hvort íhlutinn sem þetta uppsetningarforrit veitir ætti að vera settur upp. Þessi færibreyta er ekki nauðsynleg. |
| --Setja upp án nettengingar | Fyrir Modern POS tilgreinir þessi færibreyta að ótengdur gagnagrunnur ætti einnig að vera settur upp og stilltur. Nota **-SQLServerName** breytu líka. Annars mun uppsetningarforritið reyna að finna sjálfgefið tilvik sem uppfyllir forsendur. |
| --Höfn | Gáttin sem ætti að vera tengd og notuð af Retail Server sýndarskránni. Ef engin gátt er stillt verður sjálfgefna gáttin, 443, notuð. |
| --Skráðu þig | Auðkenni skrárinnar, eins og sýnt er á **Skrár** síðu í höfuðstöðvum. |
| --RetailServerAadClientId | The Azure AD auðkenni viðskiptavinar sem Retail Server ætti að nota í samskiptum við höfuðstöðvar. |
| --RetailServerAadResourceId | Smásöluþjónninn Azure AD auðkenni forrits tilfangs sem ætti að nota við virkjun tækisins. Þessi færibreyta er ekki nauðsynleg fyrir innleiðingu á staðnum. |
| --RetailServerCertFullPath | Fullsniðin URN slóðin sem notar þumalfingur sem leitarmæligildi smásölumiðlarans auðkennisvottorðs sem ætti að nota til að auðkenna með Azure AD fyrir samskipti við höfuðstöðvar. Til dæmis,`store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` er rétt sniðin vefslóð þar sem gildið **\<MyThumbprint\>** verður skipt út fyrir þumalfingur skírteinisins sem ætti að nota. Ekki nota þessa breytu ásamt **-RetailServerCertThumbprint** breytu. |
| --RetailServerCertThumbprint | Þumalfingursmerki smásölumiðlarans auðkennisvottorðs sem ætti að nota til að auðkenna með Azure AD fyrir samskipti við höfuðstöðvar. Þetta þumalfingur verður notað til að leita í **LocalMachine/My** geyma staðsetningu og nafn til að finna rétta vottorðið til að nota. Ekki nota þessa breytu ásamt **-RetailServerCertFullPath** breytu. |
| --RetailServerURL | Vefslóð smásöluþjónsins sem uppsetningarforritið ætti að nota. (Þessi vefslóð er einnig þekkt sem Commerce Scale Unit\[ CSU\] URL.) Fyrir Modern POS verður þetta gildi notað við virkjun tækisins. |
| --SkipAadCredentialsCheck| Rofi sem gefur til kynna hvort Azure AD Sleppa ætti eftirliti með skilríkjum. Sjálfgefið gildi er **rangt**. |
| --SkipCertCheck | Rofi sem gefur til kynna hvort sleppa eigi forsendum skírteinaprófa. Sjálfgefið gildi er **rangt**. |
| --SkipIisCheck | Rofi sem gefur til kynna hvort sleppa eigi forsendumathugunum Internet Information Services (IIS). Sjálfgefið gildi er **rangt**. |
| --SkipNetFrameworkCheck | Rofi sem gefur til kynna hvort sleppa eigi .NET Framework forsendum. Sjálfgefið gildi er **rangt**. |
| --SkipScaleUnitHealthcheck | Rofi sem gefur til kynna hvort sleppa eigi heilsuskoðun á uppsettum íhlutum. Sjálfgefið gildi er **rangt**. |
| --SkipSChannelCheck | Rofi sem gefur til kynna hvort sleppa ætti forsendumathugunum á öruggum rásum. Sjálfgefið gildi er **rangt**. |
| --SkipSqlFullTextCheck | Rofi sem gefur til kynna hvort sleppa ætti staðfestingu á SQL Server forsendunni sem krefst fullrar textaleitar. Sjálfgefið gildi er **rangt**. |
| --SkipSqlServerCheck | Rofi sem gefur til kynna hvort sleppa ætti SQL Server forkröfuskoðunum. Sjálfgefið gildi er **rangt**. |
| --SqlServerName | SQL Server nafnið. Ef nafnið er ekki tilgreint mun uppsetningarforritið reyna að finna sjálfgefið tilvik. |
| --SslcertFullPath | Fullsniðin URN slóð sem notar þumalfingur sem leitarmælikvarða staðsetningar vottorðsins sem ætti að nota til að dulkóða HTTP umferð í mælikvarðaeininguna. Til dæmis,`store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` er rétt sniðin vefslóð þar sem gildið **\<MyThumbprint\>** verður skipt út fyrir þumalfingur skírteinisins sem ætti að nota. Ekki nota þessa breytu ásamt **-SslCertThumbprint** breytu. |
| --SslCertThumbprint | Þumalfingur af vottorðinu sem ætti að nota til að dulkóða HTTP umferð í mælikvarðaeininguna. Þetta þumalfingur verður notað til að leita í **LocalMachine/My Store** staðsetningu og nafn til að finna rétta vottorðið til að nota. Ekki nota þessa breytu ásamt **-SslCertFullPath** breytu. |
| --StoreSystemAosUrl | Vefslóð höfuðstöðvanna (AOS). |
| --StoreSystemChannel DatabaseId | Auðkenni rásargagnagrunnsins (nafn). |
| --Leigjandi | The Azure AD auðkenni leigjanda. |
| --TransactionServiceAzureAuthority | Viðskiptaþjónustan Azure AD heimild. |
| --TransactionServiceAzureResource | Viðskiptaþjónustan Azure AD auðlind. |
| --TrustSqlServerCertificate | Rofi sem gefur til kynna hvort treysta eigi Server-vottorðinu á meðan verið er að koma á tengingu við SQL Server. Til að koma í veg fyrir öryggisáhættu ætti framleiðsluuppsetning aldrei að gefa upp verðmæti **satt** hér. Sjálfgefið gildi er **rangt**. |
| --Frásögn | Stig skráningar sem beðið er um við uppsetningu. Venjulega ætti ekki að nota þetta gildi. |
| --WindowsPhoneAppInsightsInstrumentationKey | Vélbúnaðarstöðin AppInsights hljóðfæralykill. |

## <a name="general-overview"></a>Almennt yfirlit

Nýja umgjörðin fyrir sjálfsafgreiðslufólk hefur ýmsa eiginleika og endurbætur. Nýja ramminn býr sem stendur aðeins til uppsetningarforrita fyrir nútíma POS, vélbúnaðarstöð og CSU (sjálfhýst). Það er mikilvægt að skilja grunnskipanalínunotkun lokuðu uppsetningarforritanna, sem ætti að líta svipað út og notað er í eftirfarandi dæmi. 
 
```Console
<Component Installer Name>.exe install --<Parameter Name> "<Parameter Information>"
```

Uppsetningarforritið krefst færibreytunnar **setja upp** (eða **fjarlægja** til að fjarlægja uppsetninguna) og allar færibreytur sem eru sérstakar fyrir þá uppsetningu. **Nafn færibreytu** ætti að innihalda allar færibreytur sem eru nauðsynlegar eins og skrá, CSU vefslóð eða upplýsingar um vottorð. **Upplýsingar um færibreytur** ætti að innihalda allar viðbótarupplýsingar um færibreyturnar.

Lokaði ramminn hefur verið búinn til til að gera ráð fyrir eftirfarandi breytingum:
- **Innsiglað** – Nýja uppsetningarramminn skilur algjörlega frá Microsoft-dreifðum grunnþáttauppsetningum frá sérstillingunum sem byggjast á stækkanleika. Sérstillingarnar verða settar upp eftir á en verða síðan óbundnar varðandi uppfærslur (svo að uppfærslur verða aðeins leyfðar fyrir Microsoft grunnhlutann, aðeins fyrir sérstillingarnar, eða fyrir bæði).
- **GUI-laus** - Það er ekki lengur notendaviðmót (UI). Þess í stað er algjörlega skipanalínudrifin keyrsla fyrir hvern íhlutauppsetningarforrit. Þessi breyting er ein af nokkrum lykilbreytingum eða eiginleikum sem eru notaðir til að einbeita sér að nýja uppsetningarrammanum til notkunar með fjöldadreifingu.
- **Dýpri skógarhögg** – Auka uppsetningarskrár gera kleift að sannreyna betur að uppsetningu sé lokið eða bilun, skrefunum sem voru framkvæmd og hvers kyns viðvaranir eða villur sem voru búnar til.
- **Hreinsun** – Í nýja rammanum vinna íhlutauppsetningarforritarnir erfiðara við að viðhalda hreinleika uppsetningarskránna með því að hreinsa allt innihald íhlutamöppunnar áður en þeir setja upp nýrri íhlutina. Þessi hreinsun tryggir að engar skrár séu eftir sem gætu valdið vandræðum og komið í veg fyrir árangursríka uppsetningu.

Þrír íhlutir hafa ekki verið fluttir yfir í nýja rammann: Virtual Peripheral Simulator, Async Server Connector Service (notað fyrir Dynamics AX 2012 R3 stuðning), og rauntíma þjónustuskipti (notað fyrir Dynamics AX 2012 R3 stuðningur).

> [!NOTE]
> Uppsetningartæki eru geymd á staðnum og geymd.  Það er mikilvægt, með tímanum, að stjórna eða eyða uppsetningarforritum sem varðveitt er til að sóa ekki plássi. Mælt er með því að halda núverandi uppsetningarforriti fyrir grunníhluti og hvers kyns viðbótauppsetningarforrit fyrir nýjustu útgáfurnar til að endurheimta frá erfiðum aðstæðum.

## <a name="migration"></a>Flutningur

Flutningur frá gömlu sjálfsafgreiðslu rammahlutauppsetningum yfir í nýju rammahlutauppsetningartæki krefst fjarlægingar á gömlu íhlutunum.

- **Nútíma POS** – Nýja uppsetningarramminn olli því að forritið fékk nýtt auðkenni forritaundirskriftar. Þess vegna þarf fulla fjarlægingu á gömlum íhlutum áður en nýr ramma Modern POS hluti er settur upp. Vegna kröfunnar um fulla fjarlægingu, verður virkjun tækisins aftur krafist. (Þessi endurvirkjun tækis er einu sinni krafa, að því tilskildu að fjarlæging eigi sér ekki stað aftur.)
- **Vélbúnaðarstöð** – Sem IIS vefsíða krefst nýi uppsetningarramminn að grunnmöppuskipulagið sé endurunnið. Þess vegna er þörf á fullri fjarlægingu á gömlum íhlutum áður en nýi rammavélbúnaðarstöðin er settur upp.
- **Commerce Scale Unit (CSU, sjálfhýst)** – Sem röð af IIS vefsíðum krefst nýi uppsetningarramminn að grunnmöppubyggingin sé endurunnin.  Þess vegna þarf fulla fjarlægingu á gömlum íhlutum áður en nýr ramma CSU (sjálfstýrður) íhluturinn er settur upp.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Áður en hafist er handa

Það er mikilvægt að þú fjarlægir gamla, sjálfsafgreiðslu Modern POS íhlutinn. Fyrir frekari upplýsingar, sjá flutningsskref fyrr í þessu efni.

### <a name="examples-of-silent-deployment"></a>Dæmi um hljóðlausa dreifingu

Þessi hluti sýnir dæmi um skipanir sem eru notaðar til að setja upp Modern POS.

#### <a name="silently-install-modern-pos"></a>Settu upp Modern POS hljóðlaust

Eftirfarandi skipun setur hljóðlaust upp (eða uppfærir) Modern POS. Það hefur staðlaða stjórnskipulag sem er notað fyrir hljóðlausa þjónustu á íhlutum sem eru uppsettir. Uppbyggingin notar grunngildi um **&lt; Uppsetningarnafn&gt; .exe**.

Eftirfarandi grunnskipun sýnir tiltæka valkosti ef beðið er um uppsetningu. Það er mjög mælt með því að þessi skipun sé notuð í fyrstu prófun eða notkun uppsetningarforritsins.

```Console
CommerceModernPOS.exe --help install
```

> [!NOTE]
> Stillingarskrá er ekki nauðsynleg fyrir Modern POS. Uppsetningarforritið hefur nú færibreytur (sýndar fyrr í þessu efni) fyrir hin ýmsu gildi sem eru notuð við virkjun tækisins.

Eftirfarandi skipun tilgreinir allar færibreytur sem ætti að nota við virkjun tækisins eftir að Modern POS forritið er sett upp. Þetta dæmi notar **Houston-3** register, sem er algengt gildi í Dynamics 365 Commerce kynningargögn.

```Console
CommerceModernPOS.exe install --Register "Houston-3" --Device "Houston-3" --RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Eftirfarandi skipun tilgreinir færibreyturnar sem ætti að nota til að setja upp og stilla offline gagnagrunninn. SQL Server er tilgreindur ásamt stillingarskránni sem ætti að nota.

```Console
CommerceModernPOS.exe install --InstallOffline --SQLServerName "SQLExpress" --Config "ModernPOS.Houston-3.xml"
```

Þú getur blandað saman þessum hugtökum til að ná þeim uppsetningarárangri sem þú vilt.

## <a name="hardware-station"></a>Vélbúnaðarstöð

### <a name="before-you-begin"></a>Áður en hafist er handa

Það er mikilvægt að þú fjarlægir gamla sjálfsafgreiðslu vélbúnaðarstöðina. Fyrir frekari upplýsingar, sjá flutningsskref fyrr í þessu efni. Það er ekki lengur til sölureikningsupplýsingatól. Þess í stað eru upplýsingar um söluaðilareikninginn settar upp þegar POS flugstöð er pöruð við vélbúnaðarstöðina. Þegar þú prófar þetta uppsetningarforrit í fyrsta skipti er mjög mælt með því að þú keyrir eftirfarandi skipun:

```Console
CommerceHardwareStation.exe --help install
```

### <a name="examples-of-silent-deployment"></a>Dæmi um hljóðlausa dreifingu

Þessi hluti sýnir dæmi um skipanir sem eru notaðar til að setja upp vélbúnaðarstöð.

#### <a name="silently-install-hardware-station"></a>Settu upp vélbúnaðarstöð hljóðlaust

Eftirfarandi skipun setur hljóðlaust upp (eða uppfærir) vélbúnaðarstöð. Það hefur staðlaða skipanabyggingu sem er notuð til að þjónusta íhluti sem eru uppsettir. Uppbyggingin notar grunngildi um **&lt; Uppsetningarnafn&gt; .exe**.

Eftirfarandi grunnskipun keyrir uppsetningarforritið sem hægt er að keyra.

```Console
HardwareStation.exe install --Port 443 --StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" --StoreSystemChannelDatabaseID "Houston" --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Stillingarskrá er ekki nauðsynleg fyrir vélbúnaðarstöð. Uppsetningarforritið hefur nú færibreytur (sýndar fyrr í þessu efni) fyrir hin ýmsu gildi sem þarf.

Eftirfarandi skipun tilgreinir allar færibreytur sem þarf til að sleppa forkröfuprófunum meðan á hefðbundinni uppsetningu stendur. 

> [!NOTE]
> Ekki er mælt með því að sleppa skoðunum án ítarlegra prófana fyrirfram eða í þróunaraðstæðum.

```Console
HardwareStation.exe install --SkipFirewallUpdate --SkipOPOSCheck --SkipVersionCheck --SkipURLCheck --Config "HardwareStation.Houston.xml"
```

Eins og venjan er er algengt að blanda saman þessum hugtökum til að ná þeim uppsetningarárangri sem þú vilt.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (hýsing á eigin vegum)

Þegar þú prófar þetta uppsetningarforrit í fyrsta skipti er mjög mælt með því að þú keyrir eftirfarandi skipun:

```Console
CommerceStoreScaleUnitSetup.exe --help install
```

### <a name="before-you-begin"></a>Áður en hafist er handa

Það er mikilvægt að þú fjarlægir gamla sjálfsafgreiðslu CSU (sjálf-hýst) íhlutinn. Fyrir frekari upplýsingar, sjá flutningsskref fyrr í þessu efni.

### <a name="examples-of-silent-deployment"></a>Dæmi um hljóðlausa dreifingu

Þessi hluti sýnir dæmi um skipanir sem eru notaðar til að setja upp CSU (sjálf-hýst).

#### <a name="silently-install-csu-self-hosted"></a>Settu upp CSU hljóðlaust (sjálfhýst)

Eftirfarandi skipun setur hljóðlaust upp (eða uppfærir) CSU (sjálfhýst). Það hefur staðlaða stjórnskipulag sem er notað fyrir hljóðlausa þjónustu á íhlutum sem eru uppsettir. Uppbyggingin notar grunngildi um **&lt; Uppsetningarnafn&gt; .exe**.

Í samanburði við hina sjálfsþjónustuuppsetningaraðilana er Commerce Scale Unit (CSU) flóknari og krefst frekar mikið magn af viðbótarupplýsingum. Eftirfarandi skipun er lágmarksskipunin (með breytum) sem þarf til að keyra uppsetningarforritið sem hægt er að keyra þegar engin stillingarskrá er til staðar.

```Console
CommerceScaleUnit.exe install --port 446 --SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Stillingarskrá er enn nauðsynleg fyrir CSU (sjálfhýst).

Eftirfarandi skipun er ítarlegri skipun sem keyrir executable skráauppsetningarforritið með nokkrum öðrum breytum.

```Console
CommerceScaleUnit.exe install --Port 446 --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate --Verbosity 0 --Config "Contoso.StoreSystemSetup.xml"
```

Eftirfarandi skipun tilgreinir færibreytur sem þarf til að sleppa forkröfuprófunum meðan á hefðbundinni uppsetningu stendur. 

> [!NOTE]
> Ekki er mælt með því að sleppa skoðunum án ítarlegra prófana fyrirfram eða í þróunaraðstæðum.


```Console
CommerceScaleUnit.exe installer --skipscaleunithealthcheck --skipcertcheck --skipaadcredentialscheck --skipschannelcheck --skipiischeck --skipnetcorebundlecheck --skipsqlservercheck --skipnetframeworkcheck --skipversioncheck --skipurlcheck --Config "Contoso.StoreSystemSetup.xml" --SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" --RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" --AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" --RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" --CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" --RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" --TrustSqlServerCertificate
```

Þú getur blandað saman þessum hugtökum til að ná þeim uppsetningarárangri sem þú vilt.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
