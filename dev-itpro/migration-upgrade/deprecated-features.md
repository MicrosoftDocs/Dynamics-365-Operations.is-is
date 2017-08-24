---
title: "Úreltir eiginleikar"
description: "Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir."
author: sericks007
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform, UnifiedOperations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: HT
ms.sourcegitcommit: 404a6e767036542b0e6ccd84c2dd841d4a602b87
ms.openlocfilehash: 671210a8d69282864ca4188abd360eefa819ae72
ms.contentlocale: is-is
ms.lasthandoff: 08/02/2017

---

# <a name="deprecated-features"></a>Úreltir eiginleikar

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða áætlað er að fjarlægja úr Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfu.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update-with-platform-update-8"></a>Eiginleikar hafa verið úreltar í Dynamics 365 for Finance and Operations, Enterprise edition júlí 2017 með uppfærslu verkvangs 8

### <a name="warehouse-mobile-devices-portal"></a>Gátt fyrir fartæki vöruhúss

Vöruhús fjarskiptatæki portal (WMDP) var sjálfstæður þáttur sem var gert ráð fyrir verslunarsvæðis á sjálfnýtingu. Þessi íhlutur er ekki lengur studdur í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Upprunalegt smáforrit sem bætir notandaupplifunina hefur komið í stað virkni WMDP. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Ástæða afskrifta**       | Afrituð virkni.                        |
| **Skipt út fyrir aðra eiginleika?** | Já. Þessari aðgerð hefur verið skipt út fyrir Finance and Operations - Warehousing. Sjá frekari upplýsingar um uppsetningu og forkröfur [sett Upp og skilgreina Microsoft Dynamics 365 til Finance and Operations - Warehousing](/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Kerfi sem verða fyrir áhrifum**             | Vöruhúsastjórnun, flutningsstjórnun |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Jöfnunarregla ítarlegrar afstemmingar banka fyrir handvirka jöfnun

Jöfnunarregla var notuð til að velja og merkja bankaskjal við handvirka jöfnun skjala í afstemmingarvinnublaðinu

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Takmörkuð notkun.                                                                         |
| **Skipt út fyrir aðra eiginleika?** | Nei. Síunarskilyrði dálka ætti að nota til að finna skjöl fyrir afstemmingu. |
| **Kerfi sem verða fyrir áhrifum**             | Reiðufjár- og bankastjórnun                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8 spjaldtölvuforrit

Windows 8 spjaldtölvuforrit veittu aðgerðir fyrir kostnaðarfærslu og -samþykkt.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Finance and Operations er samhæft við spjaldtölvur. Spjaldtölvuforrita er ekki lengur þörf. |
| **Skipt út fyrir aðra eiginleika?** | Nei.                                                                                      |
| **Kerfi sem verða fyrir áhrifum**             | Útgjaldastýring                                                                       |


## <a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Eiginleikar hafa verið úreltar í Dynamics 365 for Operations 1611 með uppfærslu verkvangs 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-greiðslusnið fyrir Spán

Consejo Superior Bancario-greiðslusnið notuð til að senda greiðsluskrár til banka fyrir viðskiptavina- og lánardrottnagreiðslur. Innihald þessara sniða er ákveðið af Asociación Española de Banca. Það tekur á Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                  |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 millifærsla fjármuna og snið beingreiðslu fyrir Spán |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur, viðskiptaskuldir                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Flutningar bankagreiðslur fyrir Litháen

Greiðsluflutningar banka eru prentaðar og myndaðar með útflutningssnið millifærslu greiðslu (LT) fyrir og skýrslum. Litháíska markaðinn hóf að nota LITAS, sameinuðum rafræna bankakerfinu, 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                    |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Litháen |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering greiðslusnið fyrir Noreg

Greiðslusnið BBS Direkte Remittering innihalda útflutning innheimtu fyrir greiðsla viðskiptavinar (beingreiðsla) og innflutning svarskilaboða.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                                                                                                        |
| **Skipt út fyrir aðra eiginleika?** | Greiðslusnið viðskiptavinar AvtaleGiro fyrir noregs má nota til að mynda skilaboð beingreiðslu. Innflutningur svarskilaboða verða innleidd í síðari útgáfum. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur, viðskiptaskuldir                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Bókhaldslykill fyrir Spán

Þessa verkfæris er notaður þegar bókhaldslyklum á Spáni krefst meiriháttar breytingar. Notendur geta flytja nýja bókhaldslykla í Microsoft Excel eða textasnið og einnig er hægt að flytja inn fjárhagsskýrslur.

|                              |                |
|------------------------------|----------------|
| **Ástæða afskrifta**       | Takmörkuð notkun  |
| **Skipt út fyrir aðra eiginleika?** | Ekkert             |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagur |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 greiðslusnið fyrir Belgíu

Eldra belgískt Greiðslusnið fyrir innheimtu (beingreiðsla).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Ástæða afskrifta**      | Þau greiðslusnið eru ekki lengur notaður.                  |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO 20022 beingreiðslusnið fyrir Belgíu. |
| **Kerfi sem verða fyrir áhrifum**            | Viðskiptakröfur                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG greiðslusnið fyrir Sviss

DTA/EZAG snið eru samþætta í ESR-kerfinu því þeau geta borið áfram tilvísunarnúmer. Þar sem Tilvísunarnúmer eru ekki tilskilinn, má nota sniðin til að vinna allar lánardrottnagreiðslur. Þessara sniða eru notaður af fyrirtækjum sem hafa á bankareikning í staðsetningu annars staðar en “Postfinance”.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                      |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Sviss |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB greiðslusnið fyrir Austurríki

EDIFACT-DIRDEB Greiðslusnið innheimtu (beingreiðsla).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                  |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO 20022 beingreiðslusnið fyrir Austurríki. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                    |

### <a name="edivat-for-belgium"></a>EDIVAT fyrir Belgíu

EDIVAT er úreltum Belgískar staðal fyrir rafræna skattskýrslu sent með öruggum pósti. Microsoft Dynamics AX 2012 heldur áfram skrifvarið lausn til að virkja aðgang að söguleg gögn.

|                              |                                      |
|------------------------------|--------------------------------------|
| **Ástæða afskrifta**       | Þau eiginleiki eru ekki lengur notaður. |
| **Skipt út fyrir aðra eiginleika?** | Ekkert                                   |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagur                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>innflutningssnið greiðslu eGiro EDIFACT fyrir Noreg

eGiro byggir á alþjóðlegum staðli Sameinuðu þjóðanna EDIFACT CREMUL, (Multiple Credit Advice Message), notaður fyrir sjálfvirka bókun á greiðslum viðskiptavina. Í Microsoft Dynamics AX er eGiro er innleitt sem innflutningssnið greiðslu viðskiptavinar.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?** | Nei. Snið verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                                                       |

### <a name="external-inventory-for-poland"></a>Ytri birgðir fyrir Pólland

Sönnun um að vörur teknar frá lánardrottni fyrir sölur án kaupa. Vörur sem er meðhöndla í ytri birgðir hafa ekki áhrif á staðalaðar birgðir, og má seldar og síðan keypt sjálfkrafa. Ferlið stofnar raunverulegum birgðahreyfingar.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| **Ástæða afskrifta**       | Skipt út fyrir aðra eiginleika                     |
| **Skipt út fyrir aðra eiginleika?** | Já, kjarnaaðgerðir vörusendingar á Innleið |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir, birgðastjórnun          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Myndun fjárhagsskýrslna fyrir austur-Evrópa

Verkfæri er notað til að setja upp gagnasöfnun fyrir bókhald og skattaskýrslur og flytja út gögn í sniðmát skýrslu XLS og DOC.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Takmörkuð notkun                                                                            |
| **Skipt út fyrir aðra eiginleika?** | Nei. Forritið verður skipt út af skilgreiningar Rafræna skýrslugerð í framtíðinni. |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagskerfi                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Flytja inn greiðslufærslur viðskiptavinar fyrir Finnland

Hægt er að velja innflutningssnið fyrir finnskar greiðslur sem flytur inn greiðslufærslur viðskiptavinar úr ytri skrá frá bankanum.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?** | Nei. Snið verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Innflutningur greiðslufærsla í færslubók fjárhags fyrir Finnland

Sniðið sem er tiltekið fyrir Finnland er notað til að flytja inn bókhaldsfærslur í fjárhag.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?** | Nei. Snið verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Samþætting við Isabel samstillt (CIS) fyrir Belgíu

Isabel er ramma fyrir rafræn bankaviðskipti í Evrópu og de-facto staðall í Belgíu.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Hætt hefur verið samþætting við Isabel-biðlara.                                                                |
| **Skipt út fyrir aðra eiginleika?** | Nei. Greiðslusnið sem eru ekki lengur notaður er skipt fyrir ISO20022 greiðslusnið millifærsla fjármuna fyrir Belgíu. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Breytingar á bókhaldslykill og bókhaldsreglur fyrir Spán

Þessir eiginleikar eru notaðir fyrir Breytingar á bókhaldslykill og bókhaldsreglur fyrir Spán Það varpar lyklum til að aðstoða við að umbreyta gamla bókhaldslykilinn í nýja bókhaldslykil og ber saman fyrra fjárhagsárið með nýja fjárhagsárið, jafnvel þó þær voru bókaðar á mismunandi lykilnúmer.

|                              |                |
|------------------------------|----------------|
| **Ástæða afskrifta**       | Takmörkuð notkun  |
| **Skipt út fyrir aðra eiginleika?** | Ekkert             |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagur |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Greiðslusnið lánardrottins Pagamento Fornittori

Eldri Ítölsk greiðslusnið fyrir millifærsla fjármuna.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                  |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Ítalía |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                       |

### <a name="payment-export-formats-for-estonia"></a>Greiðsluútflutningssnið fyrir Eistland

Telehansa og Teleservice-snið notuð til að flytja út greiðslu banka.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Ástæða afskrifta**      | Þau greiðslusnið eru ekki lengur notaður.                  |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Eistland |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                         |

### <a name="payment-file-archive-for-norway"></a>Greiðsluskrársafn fyrir Noreg

Þegar greiðsluskrár eru myndaðar, geymir í skráasafn sjálfkrafa allar skrár sem eru stofnaðar, jafnvel skrár sem voru áður skrifuð eða lesa.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| **Ástæða afskrifta**       | Skipt út fyrir aðra eiginleika                                        |
| **Skipt út fyrir aðra eiginleika?** | Já, Safnvistaðar vinnslur í Rafrænni skýrslugerð                            |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur, viðskiptaskuldir, fyrirtækisstjórnun |

### <a name="payment-import-formats-for-estonia"></a>Greiðsluinnflutningssnið fyrir Eistland

Telehansa og TeleTeenus-snið notuð til að flytja inn greiðslu banka.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                                    |
| **Skipt út fyrir aðra eiginleika?** | Nei. Sniðum verður skipt út af ISO 20022 innflutningssniði fyrir yfirlit í síðari útgáfum. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                                                        |

### <a name="performance-management-goal-workflow"></a>Verkflæði markmiðs frammistöðustjórnunar

Frammistöðustjórnun inniheldur markmiðastjórnun og samþættingu við yfirferðir frammistöðu.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Frammistöðustjórnun var endurhönnuð og blaðsíðufjöldi var minnkað til að einfalda ferlið.                 |
| **Skipt út fyrir aðra eiginleika?** | Nei. Markmið eru sýnileg stjórnendum gegnum gátt fyrir Sjálfsafgreiðsla stjórnanda og hægt er að breyta og skoða af stjórnanda. |
| **Kerfi sem verða fyrir áhrifum**             | Mannauðsstjórnun                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot og Postgirot Utland greiðslusnið fyrir Svíþjóð

Postgirot og Postgirot Utland greiðslusnið fyrir Svíþjóð

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                 |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Svíþjóð |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                        |

### <a name="radio-frequency-identifier"></a>Rafmerki

Rafmerki (RFID) er gagnasöfnunartækni sem notar Rafræn tög til að geyma auðkennisgögn og no-line-of-sight requirement reader til að grípa auðkenni gögn.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?** | Ekkert                                            |
| **Kerfi sem verða fyrir áhrifum**             | Birgðir                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Skýrsla um opinbera tölusetningu reikninga í Lettlandi.

Lettneskt löggjöf veitir tilteknar reglur um hvernig sölureikninga skulu númeraðir. Eiginleikinn leyfir þér að úthluta tilteknum númer á sölureikninga, byggt á notanda eða notendaflokk. Síðan er hægt að mynda skýrslu eða xml-skrá. Einnig er hægt að prenta skýrslu um reikningsnúmera sem eru notaðar.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Í opinber tölusetning reikninga þarf ekki lengur að halda við. Skýrslu um notuð reikningsnúmer er ekki lengur þörf. |
| **Skipt út fyrir aðra eiginleika?** | Ekkert                                                                                                                       |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Setja upp nöfn stjórnanda og aðalbókari fyrirtækis fyrir Litháen

Nöfn stjórnanda og aðalbókari fyrirtækis má tilgreina í upplýsingar um fyrirtækið og notaðar í útprentunum mismunandi staðbundna skýrslu.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Ástæða afskrifta**       | Skipt út fyrir aðra eiginleika                                     |
| **Skipt út fyrir aðra eiginleika?** | Já, er hægt að nota uppsetningu embættismanna í sama tilgangi.   |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir, viðskiptakröfur, reiðufjár- og bankastjórnunar |

### <a name="telepay-payment-formats-for-norway"></a>Telepay greiðslusnið fyrir Noreg

Greiðslusnið Telepay innihalda útflutning greiðsla lánardrottins (millifærsla fjármuna) og innheimtubréf (beingreiðsla) til viðskiptavina.

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                                                        |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna og greiðslusnið viðskiptavinar AvtaleGiro fyrir Svíþjóð |
| **Kerfi sem verða fyrir áhrifum**            | Viðskiptakröfur, viðskiptaskuldir                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Útflutningssnið lánardrottnagreiðslu fyrir Finnland

Tvö snið fyrir útflutning á greiðslum eru tiltækar fyrir Finnland. LM02 (FI) er notuð fyrir innanlandsgreiðslur og LUM2 (FI) er notað fyrir erlendar greiðslur.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Ástæða afskrifta**       | Þau greiðslusnið eru ekki lengur notaður.                  |
| **Skipt út fyrir aðra eiginleika?** | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Finnland |
| **Kerfi sem verða fyrir áhrifum**            | Viðskiptaskuldir                                         |

### <a name="workflow-for-creating-goals"></a>Verkflæði til að stofna markmið

Verkflæði til að stjórna stofnun starfsmannamarkmiða er eitt af nokkrum verkflæði sem voru tiltæk til að auðvelda skipulag fyrir ferlið við frammistöðustjórnun.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Frammistöðustjórnun hefur verið algerlega endurhönnuð í Microsoft Dynamics 365 for Finance and Operations.                                                                                                                                                                                                                                        |
| **Skipt út fyrir aðra eiginleika?** | Endurhannaður Eiginleiki frammistöðustjórnunar gefur meiri stjórn yfir markmið, mælingar sem notaðar eru til að rekja framvindu, og að hengja við frekari gögn. Markmið má geyma sem sniðmát og síðan endurnotuð. Þessi eiginleiki getur hjálpað við að setja upp viðbótar markmið fyrir starfsmennina fljótlegri hátt. |
| **Kerfi sem verða fyrir áhrifum**            | Mannauðsstjórnun                                                                                                                                                                                                                                                                                                               |

## <a name="features-that-have-been-deprecated-in-dynamics-ax-70-releases"></a>Aðgerðir sem hafa verið úreltar í Dynamics AX 7.0 útgáfum

### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Möguleika á að hætta við breytingar á reikningi lánardrottins

|                              |                         |
|------------------------------|-------------------------|
| **Ástæða afskrifta**       | Bætt frammistaða. |
| **Skipt út fyrir aðra eiginleika?** | Nei                      |
| **Kerfi sem verða fyrir áhrifum**            | Viðskiptaskuldir        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF AxD og AxBC samþættingar

Í samþættingarramma Kerfa (AIF), er hægt að skiptast á gögnum við ytri kerfi gegnum viðskiptagrunninn með viðskiptagrunn sem er sem þjónustu. Dynamics AX felur í sér þjónustu sem byggir á skjölum og .NET Business Connector (AxBC). Skjal er stofnað með notkun XML. XML inniheldur hausupplýsingar sem bætt er við til að stofna *skilaboð* sem hægt er að flytja inn eða út úr Dynamics AX. Dæmi um skjöl fela í sér sölupantanir og innkaupapantanir. Hins vegar getur skjal staðið fyrir nánast hvaða einingu sem er, eins og viðskiptavin. Þjónustur sem byggir á skjölum nota **Axd &lt;*Skjal*&gt;** klasar.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Ekki tókst að laga uppbyggingu AIF og AxDs að skýjaþjónustu. Upp komu afkastavandamálí tengslum við fjöldainnflutning.                                                                               |
| **Skipt út fyrir aðra eiginleika?** | Í þessari útgáfu Dynamics AX, er þessi eiginleiki skipt út fyrir Gagnaramma Innflutnings og Útflutnings sem styður endurtekna fjöldaafritun innflutnings og útflutnings. Mælt er með því að raunverulegar töflur sé notað AxBC. |
| **Kerfi sem verða fyrir áhrifum**             | AxD AxBC og AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Uppskriftir án uppskriftaútgáfa

Þegar á skilgreiningarlykill **uppskriftaútgáfur** var gerður óvirkur voru uppskriftarútgáfur falin í öllum skjámyndum og kerfið þvingaði fram 1:1 vensl milli útgefnar afurðir og Uppskrifta. Skilgreiningarlykillinn **Uppskriftaútgáfur** má ekki vera óvirkur í þessari útgáfu af Dynamics AX.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Ástæða afskrifta**      | Notkun skilgreiningarlykils til að stjórna uppskriftaútgáfur lagast ekki að skýjaumhverfi. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                      |
| **Kerfi sem verða fyrir áhrifum**            | Upplýsingar um afurðarstjórnun, Birgðastjórnun                                    |

### <a name="brazilian-bordero"></a>Brazilian Bordero

Tiltekin greiðsluhátt fyrir Brasilískt fyrirtæki

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Stuðning fyrir greiðsluaðferð Brasilískt Bordero Hefur verið lagðar af úr Brasilískt staðfærslu |
| **Skipt út fyrir aðra eiginleika?** | Ekkert                                                                                                    |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brasilískt Sintegra yfirlit

Alríkisskattframtal fyrir ICMS-skatt

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þetta yfirlit á ekki lengur við sum Brasilískt ríki.                                                     |
| **Skipt út fyrir aðra eiginleika?** | Nei. Notendur geta notað verkfærið Almennan Rafræna skýrslugerð til að skilgreina uppgjör ef nauðsynlegt við tilteknar aðstæður. |
| **Kerfi sem verða fyrir áhrifum**             | Skattabækur                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilísk SCAN viðbúnaðarstilling fyrir NF-e

(SCAN) aðstæður viðbúnaðar er notað til að mynda, flytja út og inn stöðu á Nota Fiscal eletrônica (NF-e) þegar aðstæður Secretaria da Fazenda (SEFAZ) er ekki tiltækt.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Viðbúnaðarháttur er á ekki lengur við í öllum brasilískum ríkjum |
| **Skipt út fyrir aðra eiginleika?** | Ekkert                                                                          |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur                                                         |

### <a name="business-analyzer"></a>Viðskiptagreining

Þessi fartækjaforrit leyfa notendum að yfirfara lykil viðskiptaviðmið.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika.                                                                                                      |
| **Skipt út fyrir aðra eiginleika?** | Fylgjast með fjárhagslegri frammistöðu efnispakki fyrir Microsoft Power BI mun innihalda lykil viðskiptaviðmiða sem voru áður tiltæk í Viðskiptagreiningu. |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagur                                                                                                                                                |

### <a name="business-statistics"></a>Viðskiptatalnagögn

Uppsetning fyrirspurnir um viðskiptatalnagögn sem geta auðveldað greiningu á afköstum í fyrirtækinu

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Eldri nálgun á viðskiptagreind (BI), Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?** | Ný Lausnir fyrir BI fyrir þessa útgáfu af Dynamics AX.                                      |
| **Kerfi sem verða fyrir áhrifum**             | Innkaup og uppruni, viðskiptaskuldir, sala og markaðssetning, viðskiptakröfur         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Breyta virkni dagsetningu skjals í færslubókarsamþykkt reiknings

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun                                                               |
| **Skipt út fyrir aðra eiginleika?** | Já. Hægt er að breyta dagsetningu skjals á bókuðum lánardrottnafærslu. |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03 greiðslusnið fyrir holland

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Snið gildir ekki lengur í Hollandi, þar sem því hefur verið skipt út fyrir SEPA-virkni. |
| **Skipt út fyrir aðra eiginleika?** | SEPA greiðsluútflutningur                                                                                       |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                        |

### <a name="compliance-center"></a>Samræmismiðstöð

Samræmismiðstöðinni var Enterprise Portal-setur til að hafa umsjón með kröfum um fylgiskjöl fyrir vegna samræmis við framtaksverkefni í tengslum við Sarbanes Oxley lög.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Of lítil notkun viðskiptavina. Microsoft SharePoint inniheldur sömu getu sem voru tiltæk í Samræmismiðstöð. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                                                     |
| **Kerfi sem verða fyrir áhrifum**             | Samræmi og innra eftirlit                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Tengill fyrir Microsoft Dynamics

Þessa verkfæris var notuð til að samþætta lykilgögn úr Microsoft Dynamics CRM í Microsoft Dynamics ERP forritin.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| **Ástæða afskrifta**       | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika. |
| **Skipt út fyrir aðra eiginleika?** | Dynamics Integrator                                      |
| **Kerfi sem verða fyrir áhrifum**             | Tengill fyrir Microsoft Dynamics                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Geymslueining og fjölvídd á lager

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Afrituð virkni                                                                                                                                         |
| **Skipt út fyrir aðra eiginleika?** | Já. Síðan AX 2012 hefur þessi virkni verið skipt út fyrir eiginleikasetti sameinuðum runupöntunum. Þetta eiginleikasett er með samantekið yfirlit á lager. |
| **Kerfi sem verða fyrir áhrifum**             | Stjórnun á upplýsingum um afurðir, framleiðslustýring, Birgðastjórnun, Sölu og markaðssetning                                                                   |

### <a name="cue-group-metadata"></a>Bunkaflokkar Lýsigagna

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Bunkaflokkar voru notaðar til að birta eina eða fleiri bunka í svæði Upplýsingakassa . Takmörkuð geta til að meðtaka hlutina einnig komu upp vandamál hvað varðar afköst, vegna þess að breyting á skrá í yfirskjámyndar orsökuðu að ein fyrirspurnin varð til fyrir bunka í bunkaflokknum. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                                                                                                                                                            |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Bunka Lýsigögn

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Bunka lýsigögn hafa verið takmarkað til að telja eða taka saman upplýsingar.                                                                                                                                                                                   |
| **Skipt út fyrir aðra eiginleika?** | Reitar Lýsigögn var kynnt til sögunnar til að veita sveigjanlegri fyrir líkön. Til dæmis, er hægt að breyta gildandi talningar, flettingum og afkastavísar (KPI). Reitar Lýsigögn Talningar er bein útskipting bunka lýsigagna. |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Danskt ávísunarsnið

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Stuðningur við danskt snið ávísana hefur verið lagður af og skýrslan hefur verið fjarlægð úr DK staðfærslu. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                                                      |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                     |

### <a name="data-partitions"></a>Deildaskiptingar gagna

Gögn deildaskiptingar veita röklegt aðskilnaðinn gagna í gagnagrunn Microsoft Dynamics AX.

|   |   |
|---|---|
| **Ástæða afskrifta**       | Gögn deildaskiptingar voru kynnt í Microsoft Dynamics AX 2012 R2 til að virkja einangrun gagna. Í almennum aðstæðum, er Fyrirtæki með dótturfyrirtæki og gögn úr eitt dótturfyrirtæki ætti ekki að vera sýnileg fyrir aðra dótturfyrirtæki, jafnvel þótt bæði dótturfyrirtækjum er stjórnað af sömu tæknideild. Hins vegar var þörf á aukalegar forskriftir og sameiginlegur kostnaður í forritinu til að stofna nýja deildaskiptingar og færa inn í þær gög, og afrita deildaskiptingar gagna. Í skýið, þar sem við höfum aðgang að verkvangur sem þjónusta (PaaS) gagnagrunnsþjónustu (Microsoft Azure SQL Gagnagrunnur), er mikið áhrifaríkara að nota í gagnagrunninn sem einangrunargeymi en að framkvæma einangrunina í forritinu. Óháð því hvort deildarskipging gagna er krafist fyrir dótturfyrirtæki, fyrir marga leigjendur, eða einfaldlega fyrir kvörðun, trúum við því að aðstæður megi meðhöndla betur með mörgum gagnagrunnum eða mörgum tilvikum Dynamics AX. |
| **Skipt út fyrir aðra eiginleika?** | deildaskipting gagna verður skipt út fyrir stuðning við margar gagnagrunna eða Dynamics AX tilvik í framtíðarútgáfum.    |
| **Kerfi sem verða fyrir áhrifum**             | Allir  |

### <a name="database-and-file-share-storage-for-attachments"></a>Gagnagrunnur og geymsla fyrir samnýttar skár fyrir viðhengi
Microsoft Dynamics AX 2012 leyfð geymsla viðhengja í gagnagrunninum og samnýttum skrám. Báðir valkostirnir eru ekki lengur studdir.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Ástæða afskrifta**       | Geymsla samnýttra skráa er ekki lengur studd því umhverfi í skýi geta ekki átt samskipti við staðbundnar samnýttar skrár. Gagnagrunnsgeymsla hefur verið gerð úrelt og í staðinn er komin Azure Blob geymsla. Azure Blob geymsla er sambærileg við geymslu í gagnagrunninum, þar sem aðeins er hægt að fá aðgang að skjölum í gegnum biðlaraskjámyndir Dynamics 365 for Finance and Operations. Þessu fylgir sá viðbótarkostur að bjóða upp á geymslu sem hefur ekki neikvæð áhrif á afköst gagnagrunnsins. Blob geymsla er sjálfgefið geymslukerfi fyrir Skjalastjórnum og virkar tafarlaust. |
| **Skipt út fyrir aðra eiginleika?** | Gagnagrunnsgeymsla hefur verið gerð úrelt og í staðinn er komin Azure Blob geymsla.       |
| **Kerfi sem verða fyrir áhrifum**             | Allir                   |

### <a name="delimitation"></a>Afmörkun

|                              |                                        |
|------------------------------|----------------------------------------|
| **Ástæða afskrifta**       | Engin Notkun á þessari virkni fannst. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                     |
| **Kerfi sem verða fyrir áhrifum**             | Tími og viðvera                    |

### <a name="desktop-client"></a>Fjartengingarforrit

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Dynamics AX biðlarann Hefur verið endurhönnuð til að auka notkunargetu yfir marga vettvanga og tæki.                      |
| **Skipt út fyrir aðra eiginleika?** | Nýr vefbiðlari er byggð á lýsigögnum skjáborðsmyndar og forritunarlíkans sem hefur verið breytt til að veita ríkulegan vefvettvang. |
| **Kerfi sem verða fyrir áhrifum**             | Allir lyklar                                                                                                                                    |

### <a name="direct-database-connection"></a>Bein gagnagrunnstenging

Í Dynamics AX 2012 R3, getur Retail Modern POS tengst beint í Channel DB á svipaðan hátt og við Enterprise POS. Það var auk staðlaðar samskiptaaðferðar Retail Modern POS sem átti samskipti í gegnum Retail-þjón.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Bein gagnagrunns tengingarnar krefst minna öryggis samskiptareglu og var fyrst og fremst notuð til að ná hæsta stig afköst. Vegna frammistöðu og öryggi endurbætur sem hafa orðið í Dynamics 365 fyrir Finance and Operations, býr aðgerðin nú til fleiri vandamál en lausnir. |
| **Skipt út fyrir aðra eiginleika?** | Nei. Aðeins stöðluðum Retail-þjónn samskipti eru studd núna.    |
| **Kerfi sem verða fyrir áhrifum**             | Channel DB/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Hollenska SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Almenn virkni er nú notaðar í stað staðfært virkni.                                                                                                                                                                 |
| **Skipt út fyrir aðra eiginleika?** | Já, þessum eiginleika hefur verið skipt út af ítarlega virkni fyrir bankaafstemmingu. |
| **Kerfi sem verða fyrir áhrifum**             | Allir                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL fyrir Þýskaland)

Þessi virkni veitti úttak fyrir eXtensible Business Reporting Language (XBRL) sem er sérstaklega ætlað fyrir Þýska eBilanz-flokkunina.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Of lítil notkun viðskiptavina.                                                                                                                                                 |
| **Skipt út fyrir aðra eiginleika?** | Þessum eiginleika hefur ekki verið skipt út fyrir annan eiginleika, en marga sérhæfða XBRL-pakka sem veita ríkulega xbrl-virkni eru tiltækar fyrir Þýsk markaði. |
| **Kerfi sem verða fyrir áhrifum**             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Enterprise Portal biðlari

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Eins biðlaravettvangur hefur verið stofnað.                                                                                            |
| **Skipt út fyrir aðra eiginleika?** | Nýr vefbiðlari er byggð á lýsigögnum skjáborðsmyndar og forritunarlíkans sem hefur verið breytt til að veita ríkulegan vefvettvang. |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                                    |

### <a name="environmental-sustainability"></a>Sjálfbær þróun

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun viðskiptavina og takmörkuðum eiginleikum.       |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                 |
| **Kerfi sem verða fyrir áhrifum**             | Samræmi og innra eftirlit, viðskiptaskuldir |

### <a name="form-activex-and-managed-host-controls"></a>Skjámynd ActiveX og stjórntæki hýsils með umsjón

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Skjámynd ActiveX og stjórntæki hýsils með umsjón byggjast á afskrifaða fjartengiforritinu.                                                                                                             |
| **Skipt út fyrir aðra eiginleika?** | Umfangsmikill Rammi fjárhagsáætlunarstýringar styður uppbyggingu nýja stýringar sem er byggt á HTML, CSS og JavaScript og er fyrsta flokks stýring í Microsoft Visual Studio Tooling umhverfinu. |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Mynda fyrirframkvittanir með runu

Myndun fyrirframkvittunar er ekki hægt að gera með því að nota runu en samt er hægt að gera af notanda.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Engin skjámynd er til staðar til að staðfesta og birta fyrirframkvittunarskrá sem verður til þegar hún er mynduð með því að nota runuvinnslu. |
| **Skipt út fyrir aðra eiginleika?** | Enn er hægt að mynda fyrirframkvittanir og notandi hefur stjórn á staðsetningunni þar sem skráin er vistuð.   |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir, viðskiptakröfur, reiðufjár- og bankastjórnunar                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Þýska DTAUS útflutningur og greiðslu og innflutningur lyklayfirlits (samtölur og færslur)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Snið gildir ekki lengur í Þýskalandi, þar sem því hefur verið skipt út fyrir virkni sameiginlegs evrópsks greiðslusvæðis (SEPA).                                                                                                                                                                 |
| **Skipt út fyrir aðra eiginleika?** | Já, þessum eiginleika hefur verið skipt út af greiðsluútflutningur SEPA og ítarlega virkni fyrir bankaafstemming fyrir innflutning reikningsyfirlita. |
| **Kerfi sem verða fyrir áhrifum**             | Allir                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Þýska dtazv greiðslusnið

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Snið gildir ekki lengur í þýskalandi, þar sem því hefur verið skipt út fyrir SEPA-virkni. |
| **Skipt út fyrir aðra eiginleika?** | SEPA greiðsluútflutningur                                                                               |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                |

### <a name="german-mt940-import"></a>Flytja inn Þýska MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Almenn virkni er nú notaðar í stað staðfært virkni.                                                                                                                                                                 |
| **Skipt út fyrir aðra eiginleika?** | Já, þessum eiginleika hefur verið skipt út af ítarlega virkni fyrir bankaafstemmingu. |
| **Kerfi sem verða fyrir áhrifum**             | Allir                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Þýskur XML ESB-sölulisti

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Xml-snið fyrir þýska skýrslugerð esb-Sölulista er ekki studd lengur. Hægt er að nota aðeins ELMA5 Snið textaskrár til að senda skýrslu esb-Sölulista til þýska skattstjórans. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                                                                                                                 |
| **Kerfi sem verða fyrir áhrifum**             | Skattur                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS-skýrslur

Skýrslur sem innihalda eftirfarandi valmyndaratriði hafa verið fjarlægð: **Samantekt á prófjöfnuði**, **Ítarlegur prófjöfnuður**, **Bókhaldslykil**, **Endurskoðunarslóð**, **Stöður**, og **stöðulisti**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Skýrslur fyrir Microsoft SQL Server Reporting Services (SSRS) hefur verið skipt út fyrir eiginleika Management Reporter og sjálfgefnar skýrslur. |
| **Skipt út fyrir aðra eiginleika?** | Management Reporter (merktur **fjárhagsskýrslugerð** í þessari útgáfu af Dynamics AX)                                                  |
| **Kerfi sem verða fyrir áhrifum**            | Fjárhagur                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart og FormPart lýsigögn

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | InfoPart og FormPart lýsigögn virkja stofnun upplýsingareita fyrir tvo mismunandi biðlara.                                                                                                                                    |
| **Skipt út fyrir aðra eiginleika?** | InfoPart lýsigögn sem var einfaldaður skilgreining skjámyndar, er breytt í Skjámynd með uppfærsluverkfærum. FormPart lýsigögn sem vísaí Skjámynd, er skipt út fyrir beinni tilvísun sem er stofnað af uppfærsluverkfærum. |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Listasíða Aðallykils

Listi yfir lykla fyrir lögaðilann og tengdar stöðuupplýsingar

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Upplýsingar um Stöðu er tiltæk á í **prófjöfnuð** listasíðu eftir lykils og víddar.                                                                                      |
| **Skipt út fyrir aðra eiginleika?** | **Aðallyklar** inniheldur sömu lista með lyklum sem listasíðu **aðallykils** innihélt . Sýn hnitanets í **aðallykla** sýnir einnig enn minni, yfirlit í hnitaneti . |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagur                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malasíu og Singapúr sjóðstreymiskýrsla banka

Þessi eiginleiki gefur notanda kost á að Prenta sjóðstreymisskýrslu sem sýnir færslur og upplýsingar sjóðinnstreymis og útstreymis fyrir tilteknar dagsetningar á völdum bankareikningum.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Hægt er að fá sömu upplýsingar úr fyrirspurn Um bankafærslu. |
| **Skipt út fyrir aðra eiginleika?** | Fyrirspurn Um bankafærslu.                                            |
| **Kerfi sem verða fyrir áhrifum**             | Reiðufjár- og bankastjórnun                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Mexíkóskur CFD rafrænn reikningur

Þessi eiginleiki virkjaði myndun Mexíkósk rafræna reikninga með því að nota aðferðina Comprobante Fiscal Digital (CFD), þar sem fyrirtækið skrifar undir reikninginn með því að biðja um viðkomandi heimild frá yfirvalda. Þessi eiginleiki veitir einnig mánaðarleg skýrsla sem inniheldur alla rafræna reikninga sem voru gefnir út á tímabilinu.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Aðferð er ekki lengur gild. Myndun rafrænna reikninga með því að nota aðferðina CFD var afskrifuð af skattyfirvöldum og skipt út fyrir Comprobante Fiscal Digital a través de Internet (CFDI) -aðferð, þar sem undirritun er framvísað til þriðja aðila þjónustuaðila (PAC). Mánaðarleg skýrsla hefur verið fjarlægt og fyrirspurnarvalkostur gerir notendum kleift að spyrjast fyrir um sögulegar færslur. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                                                                                                                                                                                                                                                                                                                                        |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptakröfur, verk                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexíkó innleyst og óinnleystur VSK

Microsoft Dynamics AX 2012 vann úr óinnleysta virðisaukaskattinum (VSK) með því að nota aðgerðir sem eru sérstaklega notaðar fyrir Mexíkó fyrir "óinnleystan skatt."

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Afrituð virkni                                                                                             |
| **Skipt út fyrir aðra eiginleika?** | Já, þessari virkni hefur verið skipt út fyrir virkni staðlaðs skilyrts söluskatts sem Core veitir. |
| **Kerfi sem verða fyrir áhrifum**             | Skattur                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-samþætting

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Aðgerðinni hefur verið skipt út fyrir samþættingu Microsoft Exchange Server. |
| **Skipt út fyrir aðra eiginleika?** | Já                                                                            |
| **Kerfi sem verða fyrir áhrifum**             | Sala og markaðssetning                                                            |

### <a name="payroll-information-in-human-resources"></a>Launaupplýsingar í Mannauði

Mannauður, launaupplýsingar

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þessi aðgerð hefur verið skipt fyrir síðurnar Laun og Mannauður.                                                                                                                                                                                                                                              |
| **Skipt út fyrir aðra eiginleika?** | **Fríðindi**, **Tekjur**, og aðrar tengdar síður sem voru áður í BNA Laun hafa verið endurskilgreind, og eru nú hluti kjarnauppsetning Mannauðs til að styðja við ytri launavinnslu. Þessi virkni er opnuð með því að nota **Mannauður 1** &gt; **Laun** skilgreiningarlykillinn. |
| **Kerfi sem verða fyrir áhrifum**             | Mannauður, Laun                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Einka lokun á færslubókum birgða- og vöruhúsastjórnunar

Færslubók birgða og vöruhúss hafa ekki lengur möguleikann á að merkja færslubók sem einka fyrir valinn notanda. Aðeins ferlið við lokun færslubóka sem einka fyrir notendaflokka og lokunar við breytingar er studd.

|                              |                                        |
|------------------------------|----------------------------------------|
| **Ástæða afskrifta**       | Engin Notkun á þessari virkni fannst. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                     |
| **Kerfi sem verða fyrir áhrifum**             | Birgðastjórnun                   |

### <a name="product-builder"></a>Vörusamsetning

Vörusamsetning (Product builder) var notaður til að setja saman á lifandi hátt vörur úr sölupöntun, innkaupapöntun, framleiðslupöntun, sölutilboð, verktilboð eða vöruþörf. Samkvæmt vörulíkani sem var með líkanabreytum gat notandinn velja gildi til að uppfylla kröfur viðskiptavinar og sækja einkvæmt afurðarafbrigði sem höfðu Uppskrift og leið.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Product builder birti X ++ kóða til að endanotenda og er ekki studdur í þessari útgáfu af Dynamics AX. Það hefur verið fjarlægð til að koma í veg fyrir tvíteknar viðhaldsvinnu á kóðagrunnum sem skarast. |
| **Skipt út fyrir aðra eiginleika?** | Afurðarafbrigði                                                                                                                                                                                   |
| **Kerfi sem verða fyrir áhrifum**             | Stjórnun á upplýsingum um afurðir, Sölu og markaðssetningu                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Endurnefna afurðarvídd

Þessi eiginleiki leyfði þér að breyta heiti á einn af þremur staðlaða afurðarvíddum (stærð, lit eða stíl) í nafn sem hentaði betur þínu fyrirtæki. Endurnefning innifalið allar merki þar sem nöfn afurðarvídda voru notuð.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Þessi útgáfu af Dynamics AX styður ekki merkingabreytingar á keyrslutíma. |
| **Skipt út fyrir aðra eiginleika?** | Ekkert                                                                            |
| **Kerfi sem verða fyrir áhrifum**             | Afurðaupplýsingastjórnun                                                |

### <a name="retail-server-connectivity-using-http"></a>Tengigeta Retail-þjóns athuguð

Í Dynamics AX 2012 R3, gæti Retail-þjónn virkað með HTTP samskiptaaðferðar (ekki-öryggisvörðum). Þetta var til viðbótar við stöðluð samskipti með HTTPS.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Vegna nýrra öryggisþarfa, aðeins öryggisvörðum samskipti með TLS 1,2 (eða ofan, sé það til staðar) er nú studd. Sjálfsafgreiðslu uppsetningarforritið mun sjálfkrafa skilgreina tölvunni þessu samskiptaaðferðar. |
| **Skipt út fyrir aðra eiginleika?** | Nei. Aðeins stöðluðum HTTPS samskipti eru studd núna.                                                                           |
| **Kerfi sem verða fyrir áhrifum**             | Retail-þjónn                                                |

### <a name="role-center-pages"></a>Hlutverkamiðstöðvarsíður

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Síður hlutverkamiðstöðvar voru byggðar á afskrifuðum Enterprise Portal verkvangi, sem hefur verið skipt út fyrir nýtt vefbiðlaravettvang í þessari útgáfu af Dynamics AX. |
| **Skipt út fyrir aðra eiginleika?** | Nýtt skjámyndarmynstur Vinnusvæðis veitir notendum hönnun sem er vinnslumiðuð og veitir auðveldan aðgang að almennum verkum innan þessu ferli.                       |
| **Kerfi sem verða fyrir áhrifum**             | Allt                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Skattaumdæmi

|                              |                                              |
|------------------------------|----------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                           |
| **Kerfi sem verða fyrir áhrifum**             | Bandarískur virðisaukaskattur                                 |

### <a name="shipping-carrier-interface"></a>Viðmót farmflytjanda

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Afrituð virkni                                                                                                                         |
| **Skipt út fyrir aðra eiginleika?** | Já, þessum eiginleika hefur verið skipt út að hluta af flutningsstjórnun en hefur enn ekki verið skipt út af vöruhúsakerfi (WMS I). |
| **Kerfi sem verða fyrir áhrifum**             | Sala og markaðssetning, Birgðastjórnun                                                                                                       |

### <a name="sites-services"></a>Svæðaþjónusta

Sites Services gerir þér kleift að búa til vefsíður sem framlengja viðskiptaferlum þínum til internetsins án stuðnings við upplýsingatækni.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Grunngerð Microsoft Azure sem notað er í Dynamics AX hefur nýja getu sem hægt er að nota í staðinn (til dæmis Azure setur). |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                                                                                                       |
| **Kerfi sem verða fyrir áhrifum**             | Ráðningaferli í mannuði, málastjórnun, Tilboðsbeiðnir, skráning Lánardrottins                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS stefna eftirspurnarspár

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Hönnun á eiginleikanum getur ekki verið studd í nýrri skýjahögun. |
| **Skipt út fyrir aðra eiginleika?** | Azure Machine Learning stefna eftirspurnarspár                           |
| **Kerfi sem verða fyrir áhrifum**             | Áætlun                                                                     |

### <a name="travel-requisitions"></a>Ferðabeiðnir

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun og flestar aðgerðir voru til staðar í Enterprise Portal. |
| **Skipt út fyrir aðra eiginleika?** | Nei                                                              |
| **Kerfi sem verða fyrir áhrifum**             | Útgjaldastýring                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Reikningahópur lánardrottins án bókunarupplýsinga

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun. Aðgerðinni hefur verið skipt út af reikningabók sem hefur virknina verkflæði. |
| **Skipt út fyrir aðra eiginleika?** | Verkflæðigeta reikningsbókar.                                                           |
| **Kerfi sem verða fyrir áhrifum**             | Viðskiptaskuldir                                                                                        |

### <a name="virtual-company-accounts"></a>Sýndarreikningsskil

Sýndarfyrirtækjaeiginleiki er ekki lengur studd í Dynamics AX. Eiginleikinn sýndarfyrirtæki gerði notendum mögulegt að setja upp töflur sem mátti deila með hóp fyrirtækja. Fyrir lýsingu á aðgerðinni sjá [reikningsskil og sýndarreikningsskil](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Eiginleikinn vinnur með því að flokka töflur í söfn sem tilheyra sýndarfyrirtæki, sem eru hópar af fyrirliggjandi "raunverulegum" fyrirtæki. Fyrirspurnir eru stofnaðar svo að öll fyrirtæki í sýndarfyrirtækinu hafi aðgang að gögnum í töflum tengdra töflusafna.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><b>Ástæða afskrifta</b></td>
<td><ul>
<li>Sýndarfyrirtæki verður að vera uppsett áður en gögn eru geymd í töflum. Að bæta sýndarfyrirtæki eftirá við yfir fyrirliggjandi framkvæmd er mjög erfitt.</li>
<li>Þar sem hefur verið svo mikið um stöðlun gagna í gildandi útgáfu af Dynamics AX, er orðið mjög erfitt að vita hvað skuli bæta við töflusöfn. Til dæmis er erfitt að vita hvaða töflum eigi að deila. Allar töflur sem vísað er til úr töflum sem eru í sýndarfyrirtæki verður að bæta við. Vegna Stöðlun Tafla verða jafnvel einfalt aðalgögn sem er dreift yfir margar töflur að vera hluti af sýndarfyrirtækinu. Öll mistök sem gerð eru hér munu valda virknivandamálum.</li>
<li>Þegar tafla er hluti af sýndarfyrirtæki, tapar það upplýsingar um uppruna gagnanna, og aðeins sýndarfyrirtæki er skráð.</li>
</ul></td>
</tr>
<tr class="even">
<td><b>Skipt út fyrir aðra eiginleika?</b></td>
<td>Altækar töflur er hægt að nota til að gera töflur aðgengilegar frá öllum fyrirtækjum. Það er engin útskipting sem stendur.</td>
</tr>
<tr class="odd">
<td><b>Kerfi sem verða fyrir áhrifum</b></td>
<td>Ekki tiltækt</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Vöruhúsakerfi II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Vöruhúsakerfi II-lausn (WMS II) sem var tiltækt í virkni tvíteknu kerfiseininga **Birgðastjórnunar** sem er í **vöruhúsakerfinu** sem var gefin út í Microsoft Dynamics AX 2012 R3.                                                                         |
| **Skipt út fyrir aðra eiginleika?** | **Vöruhúsakerfinu** sem var gefið út í AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 og Dynamics AX 2012 R3 CU9 kemur í stað virkni vöruhúsakerfis II. Nýja kerfið hefur fleiri ítarlegar aðgerðir og sveigjanlegri vöruhúsakerfisferli en vöruhúsakerfi II. |
| **Kerfi sem verða fyrir áhrifum**             | Birgðastjórnun, sölu og markaðssetningu, innkaup og uppruni                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Áminningar starfsmanna í mannauði

Mannauður, launaupplýsingar

|                              |                 |
|------------------------------|-----------------|
| **Ástæða afskrifta**       | Lítil notkun       |
| **Skipt út fyrir aðra eiginleika?** | Nei              |
| **Kerfi sem verða fyrir áhrifum**             | Mannauður |

### <a name="workplanner"></a>Vinnuáætlun

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Lítil notkun                                                                                                                                                            |
| **Skipt út fyrir aðra eiginleika?** | Nei, en **Forstillingarvensl** síðu sem er opnuð á **forstillingarflokks** síðu, styður sömu viðskiptaaðstæður og í hinu úrelta **vinnuáætlun** síðu. |
| **Kerfi sem verða fyrir áhrifum**             | Tími og viðvera                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ fjárhagsskýrslur

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| **Ástæða afskrifta**       | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika.                                    |
| **Skipt út fyrir aðra eiginleika?** | Management Reporter (merktur **fjárhagsskýrslugerð** í þessari útgáfu af Dynamics AX) |
| **Kerfi sem verða fyrir áhrifum**             | Fjárhagur                                                                              |


