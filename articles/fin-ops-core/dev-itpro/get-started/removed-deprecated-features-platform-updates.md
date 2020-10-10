---
title: Fjarlægðir eða úreltir eiginleikar verkvangs
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í verkvangsuppfærslum á forritum Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0b78401f4c1cf289247cd2d600f097ecdf6a712c
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819890"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjarlægðir eða úreltir eiginleikar verkvangs

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í verkvangsuppfærslum á forritum Finance and Operations.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir útgáfu 10.0.14 á forritum Finance and Operations

> [!NOTE]
> Útgáfa 10.0.14 er forútgáfa. Innihald og virkni geta tekið breytingum. Frekari upplýsingar um forútgáfur er að finna í hlutanum [Framboð þjónustuuppfærslu](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/public-preview-releases).


### <a name="online-users-page"></a>Síða nettengds notanda 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta er eldri síða sem var byggð á fyrri uppsetningu biðlara/þjóns. Upplýsingarnar á þessari síðu eru ekki alltaf réttar, sem getur verið ruglingsleg og villandi. |
| **Skipt út fyrir aðra eiginleika?**   | Við munum birta nýja síðu í síðari uppfærslu.|
| **Afurðasvæði sem haft er áhrif á**         | Kerfisstjórnun |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Frá október 2021 verður þetta fjarlægt.   |

## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir útgáfu 10.0.13 á forritum Finance and Operations


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Sérstilltur kóði skilgreindur í eiginleikum SSRS-skýrslu 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Almennt býður sérstilltur kóðir upp á takmarkaðan ávinning og þarf á sama tíma umtalsverða tilfangagetu og útreikning fyrir stuðning. Sérstilltur kóði er fyrst og fremst notaður af skýrsluhöfundum til að kalla á opinberar aðferðir úr samsetningu sérstilltra kóða. Skýjaþjónustan styður hinsvegar ekki tilvísanir í sérstilltar samsetningar fyrir SSR-skýrslur. |
| **Skipt út fyrir aðra eiginleika?**   | Skýrsluhöfundar geta valið að halda áfram að vísa í almenn .NET API fyrir útreiknings-, umreiknings- og sniðsaðgerðir úr hvers kyns textareitasegð. Frekari upplýsingar eru í [Bæta kóða við skýrslu (SSRS)](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Afurðasvæði sem haft er áhrif á**         | Undirsafn af skýrsluhönnunum forrits skilgreind í RDL sem inniheldur sérstilltan kóða. |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Í útgáfu 10.0.13 byrjar þýðandinn að gefa út viðvörun vegna tilvika þar sem sérstilltur kóði greinist í SSRS-skýrsluskilgreiningu. Til að lagfæra vandamálið skal opna skilgreiningu skýrsluhönnunar og fjarlægja alla sérstillta kóðaggervinga. Þessari viðvörun verður skipt út fyrir þýðingarvillu í framtíðaruppfærslu.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Uppfærsla á þremur jQuery-þáttasöfnum 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Verið er að uppfæra þrjú jQuery-þáttasöfn í tengslum við öryggisuppfærslur og uppfærslu upplýsinga.   
| **Skipt út fyrir aðra eiginleika?**   | Eftirfarandi söfn eru uppfærð: jQuery (að útgáfu 3.5.0 frá útgáfu 2.1.4), jQuery UI (að útgáfu 1.12.1 frá útgáfu 1.11.4), jQuery qTip (að útgáfu 3.0.3 frá útgáfu 2.2.1). jQuery hefur birt leiðbeiningar um flutninga á netinu.  |
| **Afurðasvæði sem haft er áhrif á**         | Stækkanlegt stjórntæki, sérsniðinn JavaScript-kóði sem nýtir API sem er búið að úrelda eða fjarlægja |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Með útgáfu 10.0.13/uppfærslu 37 geta viðskiptavinir fært nýjustu söfnin með því að virkja eiginleikann „Uppfæra þrjú jQuery-þáttasöfn“. Áskilið verður að flytja nýju söfnin með útgáfunni í apríl 2021 til að bjóða upp á tíma fyrir flutning viðeigandi API.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Fyrirliggjandi hnitanetsstýring/forceLegacyGrid() API

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Verið er að skipta út núverandi hnitanetsstýringu fyrir nýju hnitanetsstýringuna. |
| **Skipt út fyrir aðra eiginleika?**   | [Ný hnitanetsstýring](../..//fin-ops/get-started/grid-capabilities.md) |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Í útgáfu 10.0.13 er nýja hnitanetsstýringin almennt í boði og viðskiptavinir geta kveikt á þessum eiginleika ef þeir vilja. Nýja hnitanetsstýringin verða áskilin í útgáfu í október 2021. Þegar nýja hnitanetsstýringin verður áskilin verður **forceLegacyGrid()** API ekki lengur virt. |

### <a name="personalization-without-saved-views"></a>Sérstillingar án vistaðra yfirlita 

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Undirkerfi sérstillinga hefur verið yfirfarið með eiginleikanum fyrir vistuð yfirlit þannig að afköstin verði betri og boðið verður upp á fleiri möguleika. |
| **Skipt út fyrir aðra eiginleika?**   | Vistuð yfirlit |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Í útgáfu 10.0.13/verkvangsuppfærslu 37 er eiginleiki vistaðra yfirlita almennt í boði og viðskiptavinir geta kveikt á honum ef þeir vilja. Eiginleiki vistaðra yfirlita verður áskilinn í útgáfu í október 2021. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir útgáfu 10.0.12 á forritum Finance and Operations

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Viðbætur í hnitaneti eða hópstýringarsniði sem innihalda ógildar reitartilvísanir

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Gagnaflokkseiginleikinn í hnitaneti eða hópstýringum er notaður til að birta sjálfkrafa alla reiti reitahópsins. Hnitanet eða hópstýring sem bætt var við með viðbót getur innihaldið reiti sem eru ekki lengur skilgreindir í reitahópnum eða það gætu verið reitir sem vantar sem eru skilgreindir í reitahópnum. Þetta getur valdið ósamkvæmri hegðun á keyrslutíma. Verkvangsuppfærslur fyrir útgáfu 10.0.12 af Finance and Operations-forritum flokka nú þetta vandamál sem þýðingar *viðvörun*. Til að laga þetta vandamál skal opna snið viðbótar og vista hana.
| **Skipt út fyrir aðra eiginleika?**   | Þýðingarviðvörunin verður skipt út fyrir þýðingarvillu í framtíðaruppfærslu. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Þýðingarvilla er kynnt í verkvangsuppfærslum fyrir útgáfu 10.0.12 á forritum Finance and Operations. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Verkvangsuppfærslur fyrir útgáfu 10.0.11 á forritum Finance and Operations

### <a name="explicit-safe-lists-for-self-service-environments"></a>Öruggir listar fyrir sjálfsafgreiðsluumhverfi

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ferlið við að færa IP-tölur yfir á undanþágulista hefur breyst. Sjálfsafgreiðsla styður ekki lengur undanþágulista IP-talna. |
| **Skipt út fyrir aðra eiginleika?**   | Nánari upplýsingar er að finna í [Skilgreining Azure Active Directory Skilyrðisbundinn aðgangur](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Afurðasvæði sem haft er áhrif á**         | Öryggi |
| **Dreifingarvalkostur**              | Ský |
| **Staða**                         | **Úrelt:** Þessi eiginleiki er að fullu úreltur fyrir uppsetningar sjálfsafgreiðslu. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Til að styðja við nýjustu útgáfur af Visual Studio þarf að gera nokkrar breytingar á viðbótum X++ fyrir Visual Studio. Þessar breytingar samhæfast ekki Visual Studio 2015. |
| **Skipt út fyrir aðra eiginleika?**   | Visual Studio 2017 kemur í stað Visual Studio 2015 sem uppsett og áskild útgáfa. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Þegar framboð nýrra sýndarvéla með Visual Studio 2017 er tilkynnt verða núverandi sýndarvélar með aðeins Visual Studio 2015 að vera settar upp aftur á útgáfutímabili 1 fyrir árið 2021. |

### <a name="field-groups-containing-invalid-field-references"></a>Reitahópar sem innihalda ógilda tilvísanareiti

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Reitahópar í skilgreiningum á lýsigögnum töflu geta innihaldið reitatilvísanir sem eru ekki gildar. Ef þessi reitahópar eru uppsettir geta þeir valdið keyrsluvillu í Financial Reporting og Microsoft SQL Server Reporting Services (SSRS). Uppfærsla pallsins 23 kynnti þýðanda *viðvörun* sem gerði kleift að taka á þessu lýsigagnavandamáli. Verkvangsuppfærslur fyrir útgáfu 10.0.11 á forritum Finance and Operations flokka þetta mál sem þýðanda *villa*.<p>Til að laga þetta vandamál skal fylgja þessum skrefum.</p><ol><li>Fjarlægja ógilda tilvísunarreitinn úr skilgreiningu töflureitahópsins.</li><li>Endurþýða.</li><li>Gakktu úr skugga um að tekið sé á öllum villum.</li></ol> |
| **Skipt út fyrir aðra eiginleika?**   | Þessi þýðingarvilla kemur í staðinn fyrir viðvörun þýðandans.  |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | **Úrelt:** Viðvörunin er þýðingartímavilla í framtíðinni með uppfærslum á verkvangi fyrir útgáfu 10.0.11 af Finance and Operations forritum. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>ISV leyfi búin til með því að nota endamerkja reikniritið SHA1

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ferlið til að búa til óháð leyfi fyrir hugbúnaðarframleiðanda (ISV) hefur breyst. Fyrir frekari upplýsingar, sjá [Óháð leyfi fyrir hugbúnaðarsöluaðila (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Skipt út fyrir aðra eiginleika?**   | Já. Notaðu Windows PowerShell til að búa til leyfi. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | <strong>Afskrifað:</strong> ISV leyfi sem voru búin til með því að nota endamerkja reiknirit SHA1. Þessi reiknirit voru háð vottorðum sem voru búin til með því að nota gagnaforritið MakeCert og sú veita hefur verið úrelt.<p><strong>Afskrifað:</strong> Notkun SHA1 í öryggisskyni eða endamerkja tilgangi. SHA1 hættir að virka snemma árs 2021. Þess vegna ætti það ekki að nota það lengur.<p><strong>Fjarlægt:</strong> Stuðningur við flutningslagöryggi (TLS) 1.0 og TLS 1.1 komandi eða sendar beiðnir. |

## <a name="platform-update-32"></a>Update 32 fyrir verkvang

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Gluggi fyrir breytingu á verkflæðisbeiðni inniheldur ekki lengur fellivalmynd fyrir val á notendum
|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta var öryggisatriði vegna þess að beiðni um breytingar var hægt að senda í ógáti til notanda. Þetta var einnig nothæfismál vegna þess að það neyddi notandann til að ákvarða hver upphafsmaður verkflæðisins var og velja þá handvirkt.  |
| **Skipt út fyrir aðra eiginleika?**   | Nr |
| **Afurðasvæði sem haft er áhrif á**         | Verkflæði |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Listi notendavalsins var fjarlægður úr valmyndinni um breytingu á beiðni í uppfærslu á verkvangi 32. Beiðnir um breytingu verða sjálfkrafa sendar til höfundar eins og til er ætlast. Fyrir frekari upplýsingar um þessa virkni, sjá [Verkþættir í samþykktarferli verkflæðis](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Innfelldir boratenglar eru ekki lengur studdir í skjöluðum skjölum sem gefin eru af þjónustunni í skýinu 
|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vefslóðir sem eru felldar inn í skjöl sem þjónustan veitir geta innihaldið viðkvæm viðskiptagögn. Við erum að fjarlægja stuðning við innbyggða boratengla í skjölum sem öryggisráðstöfun til að vernda gögn viðskiptavinarins frekar. Notendur munu einnig njóta góðs af bættum árangri meðan þeir framleiða skjöl gagnvirkt vegna þessarar breytinga.  |
| **Skipt út fyrir aðra eiginleika?**   | Ekkert |
| **Afurðasvæði sem haft er áhrif á**         | Skýrslugerð |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Þessi aðgerð er virkur tekinn úr þjónustunni.<br><br>Nútíma viðskiptavinurinn býður upp á fjölmarga möguleika til að framleiða áhorf sem innihalda tengla sem myndast sjálfkrafa til að aðstoða við siglingar forritsins. Mælt er með pagineruðum gögnum sem þjónustan veitir vegna utanaðkomandi samskipta sem eru send, geymd og geymd og prentuð fyrir viðtakendur. Við höfum bætt reynsluna af því að forskoða skjöl beint í vafranum, sem býður upp á beinan aðgang að prenturum á staðnum. Fyrir frekari upplýsingar, sjá [Forskoða PDF skjöl með innbyggðri skoðun](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir
Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../migration-upgrade/deprecated-features.md).

