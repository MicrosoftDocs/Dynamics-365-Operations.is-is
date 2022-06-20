---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Commerce
description: Þessi grein lýsir eiginleikum sem hafa verið fjarlægðir, eða sem fyrirhugað er að fjarlægja úr Dynamics 365 Commerce.
author: josaw
ms.date: 04/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 2725ff2b8bfbaadbca1bc070e32cee7c5d2754be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910525"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Þessi grein lýsir eiginleikum sem hafa verið fjarlægðir, eða sem fyrirhugað er að fjarlægja úr Dynamics 365 Commerce.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!NOTE]
> Ítarlegar upplýsingar um hluti í Finance and Operations öppum er að finna í [Tæknilegar tilvísunarskýrslur](/dynamics/s-e/). Þú getur borið saman mismunandi útgáfur þessara skýrslna til að fræðast um hluti sem hafa breyst eða verið fjarlægðir í hverri útgáfu af Finance and Operations forritum.

## <a name="features-removed-or-deprecated-in-the-commerce-10025-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.25 útgáfu

### <a name="modern-point-of-sale-mpos"></a>Nútíma sölustaður (MPOS)

Modern Point of Sale (MPOS) forritið verður úrelt í útgáfu Commerce útgáfu 10.0.25 og skipt út fyrir Store Commerce appið.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Forrit í verslun eru hornsteinn þess Dynamics 365 Commerce allsherjarútboð. Við gerum stöðugt nýsköpun til að bjóða upp á nútímalega og snjalla verslunarupplifun og til að nútímavæða lausnina okkar enn frekar erum við að setja út nýjar breytingar sem munu verulega bæta upplýsingatæknirekstur og notendaupplifun með núverandi forritum okkar í verslunum á Windows. Nýja Store Commerce forritið er tækniuppfærsla á núverandi MPOS. Það veitir betri afköst, áreiðanleika og langtímastuðning á Windows pallinum og útilokar þörfina á að endurpakka forritinu með hverri uppfærslu. |
| **Skipt út fyrir aðra eiginleika?**   |  [Store Commerce](../dev-itpro/store-commerce.md) |
| **Afurðasvæði sem haft er áhrif á**         | Nútíma sölustaður |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá og með útgáfu Commerce útgáfu 10.0.25 verður MPOS uppsetningarforritið sem sent er í gegnum LCS sýndarvélarnar (VMs) fjarlægt í október 2023. |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.21 útgáfu

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Stilling meðhöndlunar afslátta sem skarast í færibreytum Commerce

Stillingin **Meðhöndlun afslátta sem skarast** á síðunni **Færibreytur Commerce** er gerð úreld í Commerce-útgáfu 10.0.21. Í framhaldinu mun verðlagningarkerfi Commerce nota eitt algrím til að ákvarða bestu samsetningu afslátta sem skarast.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | <p>Stillingin **Meðhöndlun afslátta sem skarast** í færibreytum Commerce stýrir því hvernig verðlagningarkerfi Commerce leitar að og ákveður bestu samsetningu afslátta sem skarast. Það býður upp á þrjá valkosti eins og er:<p><ul><li> **Bestu afköst** – Þessi valkostur notar algrím ítarlegra leiðsagnarreglna og aðferðina [Röðun jaðarvirðis](../optimal-combination-overlapping-discounts.md) til að forgangsraða, leggja mat á og skera úr um bestu samsetningu afsláttar með fljótlegum hætti.</li><li>**Jafnaður útreikningur** – Í núverandi kóðakerfi virkar þessi valkostur eins og valkosturinn **Bestu afköst**. Því er þetta í raun tvískiptur valkostur.</li><li>**Tæmandi útreikningur** – Þessi valkostur notar gamalt algrím sem fer gegnum allar mögulegar samsetningar afsláttar í verðútreikningnum. Fyrir pantanir sem eru með stórar línur og mikið magn gæti þessi valkostur valdið afkastavandamálum.</li></ul><p>Til að einfalda stillingar, bæta afköst og draga úr atvikum af völdum gamla algrímsins munum við fjarlægja að fullu stillinguna **Meðhöndlun afslátta sem skarast** og uppfæra innri reiknireglu verðlagningarkerfis Commerce þannig að það noti nú aðeins ítarlegt algrím (þ.e. algrímið að baki valmöguleikanum **Bestu afköst**).</p> |
| **Skipt út fyrir aðra eiginleika?**   | Nr. Við mælum með því að fyrirtæki sem nota valkostinn **Jafnaður útreikningur** eða **Tæmandi útreikningur** skipti yfir í valkostinn **Bestu afköst** áður en þessi eiginleiki er fjarlægður. |
| **Afurðasvæði sem haft er áhrif á**         | Verðlagning og afslættir |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Frá og með útgáfu 10.0.21 mun stillingin **Meðhöndlun afslátta sem skarast** verða fjarlægð úr færibreytum Commerce í október 2022. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Retail SDK dreift með því að nota Lifecycle Services

Retail SDK er sent í Lifecycle Services (LCS). Þessi dreifingarmáti er úreltur í útgáfu 10.0.21. Í framhaldinu verða tilvísunarpakkar fyrir Retail SDK, söfn og sýnishorn birt í opinberum geymslum á GitHub.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Retail SDK er sent í LCS. LCS-ferlið tekur nokkrar klukkustundir og það þarf að endurtaka ferlið fyrir hverja uppfærslu. Í framhaldinu verða tilvísunarpakkar fyrir Retail SDK, söfn og sýnishorn birt í opinberum geymslum á GitHub. Auðvelt er að nota dæmi viðbóta og tilvísunarpakka og uppfærslurnar taka aðeins nokkrar mínútur. |
| **Skipt út fyrir aðra eiginleika?**   |  [Sækja sýnishorn Retail SDK og tilvísunarpakka úr GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Afurðasvæði sem haft er áhrif á**         | Retail SDK |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Frá og með útgáfu 10.0.21 verður SDK sem er sent með sýndarvélum LCS fjarlægt í október 2023. |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Virkjanlegur pakki smásölu og sameinuð uppsetningarforrit sölustaðar, vélbúnaðarstöðvar og Cloud Scale Unit

Virkjanlegir pakkar smásölu myndaðir með Retail SDK MSBuild eru úreltir í 10.0.21. Í framhaldinu skaltu nota Cloud Scale Unit (CSU) pakkann fyrir viðbætur Cloud Scale Unit (Commerce Runtime, gagnagrunn rásar, Headless Commerce API, greiðslur og sölustað í skýi). Notaðu eingöngu uppsetningarforrit vegna stækkunar fyrir sölustað, vélbúnaðarstöð og sjálfhýst Cloud Scale Unit.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Virkjanlegur pakki smásölu er sameinaður pakki sem inniheldur heilt safn af stækkunarpökkum og uppsetningarforritum. Þessi sameinaði pakki gerir uppsetninguna flókna þar sem CSU-viðbætur fara í Cloud Scale Unit og uppsetningarforrit eru notuð í verslunum. Uppsetningarforritin fela í sér viðbótina og grunnafurðina, sem gerir uppfærslurnar erfiðar. Við hverja uppfærslu þarf að sameina kóða og búa til pakka. Til að einfalda þetta ferli eru stækkunarpakkarnir nú aðskildir í hluta fyrir einfaldari uppsetningu og stjórnun. Með nýju aðferðinni eru viðbætur og uppsetningarforrit grunnafurðar aðskilið og er hægt að þjónusta og uppfæra sjálfstætt án kóðasamruna eða endurpökkunar.|
| **Skipt út fyrir aðra eiginleika?**   | CSU-viðbætur, uppsetningarforrit sölustaðarviðbótar, uppsetningarforrit vegna stækkunar vélbúnaðarstöðvar |
| **Afurðasvæði sem haft er áhrif á**         | Dynamics 365 Commerce viðbót og uppsetning |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Frá og með útgáfu 10.0.21 verður stuðningur við að setja upp RetailDeployablePackage í LCS fjarlægður í október 2022. |

Frekari upplýsingar má finna á

+ [Búa til aðskilinn pakka fyrir Commerce Cloud Scale Unit (SCU)](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Stofna viðbótarpakka Modern POS](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Samþætta POS við nýjan vélbúnað](../dev-itpro/hardware-device-extension.md)
+ Dæmi um kóða
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS, CSU og vélbúnaðarstöð](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln og CloudPos.sln í Retail SDK

Þróun POS viðbóta með ModernPos.sln, CloudPos.sln, POS.Extension.csproj og POS möppunni er úrelt í útgáfu 10.0.21. Í framhaldinu skaltu nota sjálfstæða SDK-pökkun fyrir POS fyrir viðbætur við POS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Í eldri útgáfum af Retail SDK, ef það eru POS-viðbætur, þarf kóðasamruna og endurpökkun til að uppfæra nýjustu útgáfu af POS. Samruni kóðans var tímafrekt uppfærsluferli og það þurfti að halda utan um allt Retail SDK í gagnageymslunni. Þú þurftir einnig að safna saman kjarnaverkum POS.App. Með því að nota sjálfstæða pökkunarlíkanið þarftu aðeins að halda utan um viðbótina þína. Það er jafn auðvelt að uppfæra í nýjustu útgáfuna af POS-viðbót eins og að uppfæra þá útgáfu af NuGet pakkanum sem verkið þitt notar. Hægt er að setja upp viðbætur sjálfstætt og þjónustur nota uppsetningarforrit viðbótarinnar. Hægt er að setja upp grunn POS og halda utan um hann sjálfstætt og ekki þarf kóðasamruna eða endurpökkun með grunnuppsetningarforritinu eða kóða. |
| **Skipt út fyrir aðra eiginleika?**   | [Sjálfstæð pökkun SDK fyrir POS](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Afurðasvæði sem haft er áhrif á**         | Dynamics 365 Commerce POS-viðbót og uppsetning |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Frá og með útgáfu 10.0.21 verður stuðningur við sameinaða POS-pakka og viðbótarlíkan með ModernPos.Sln, CloudPOs.sln og Pos.Extensons.csproj í Retail SDK fjarlægður í október 2023. |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.17 útgáfu

### <a name="full-dataset-generation-interval-is-deprecated"></a>Tímabil myndunar fullbúins gagnasafns er úrelt

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá og með þessari útgáfu, í **Færibreytur viðskiptaverkraðara** í Dynamics 365 Headquarters, er reiturinn **Tímabil myndunar fullbúins gagnasafns í dögum** ekki notaður. Í þessari útgáfu verður reiturinn fjarlægður þannig að ekki er hægt að breyta gildinu. Þetta mun halda áfram sem gildið **0**. |
| **Skipt út fyrir aðra eiginleika?**   | Nei |
| **Afurðasvæði sem haft er áhrif á**         | Dynamics 365 Commerce |
| **Dreifingarvalkostur**              | Allir|
| **Staða**                         | Úrelt. Ekki skal nota þennan reit eða breyta gildinu í honum.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.15 útgáfu

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 stuðningi við Dynamics 365 hefur verið hætt

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá desember 2020, er Microsoft Internet Explorer 11 stuðningi fyrir allar Dynamics 365 vörur hætt og Internet Explorer 11 verða ekki stutt eftir ágúst 2021.<br><br>Þetta mun hafa áhrif á viðskiptavini sem nota Dynamics 365 vörur sem eru hannaðar til að nota með Internet Explorer 11 viðmóti. Eftir ágúst 2021 er Internet Explorer 11 ekki stutt fyrir þessar Dynamics 365 vörur. |
| **Skipt út fyrir aðra eiginleika?**   | Við mælum með því að viðskiptavinir skipti yfir í Microsoft Edge.|
| **Afurðasvæði sem haft er áhrif á**         | Allar Dynamics 365 vörur |
| **Dreifingarvalkostur**              | Öll|
| **Staða**                         | Úrelt. Internet Explorer 11 verður ekki stutt eftir ágúst 2021.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.11 útgáfu
### <a name="data-action-hooks"></a>Krókar gagnaaðgerða
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Krókar gagnaaðgerða hafa verið teknir úr umferð vegna afkastatengdra vandamála. |
| **Skipt út fyrir aðra eiginleika?**   | Mælt er með notkun [gagnaaðgerðahnekkinga](../e-commerce-extensibility/data-action-overrides.md) í staðinn þegar breyta þarf viðskiptagrunni í gagnaaðgerðarlagi.|
| **Afurðasvæði sem haft er áhrif á**         | Gagnaaðgerðir stækkunarhæfni rafrænna viðskipta |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: frá og með útgáfu 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Retail SDK-stuðningur fyrir Visual Studio 2015, msbuild 14,0 og Retail SDK\tilvísunarsöfn og verkfæri
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Retail SDK-stuðningi fyrir Visual Studio 2015 hefur verið hætt og uppfærður í support VS 2017, msbuild 15,0 og öll tilvísunarsöfn og Commerce staðgengilsverkfæri í möppunni RetailSDK\References möppunni færðar í NuGet pakka til að einfalda líkanið og SDK uppfærsluferlið.|
| **Skipt út fyrir aðra eiginleika?**   | Við mælum með því að fylgja upplýsingum í [Flytja Retail SDK úr Visual Studio 2015 í Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) til að uppfæra kerfið. |
| **Afurðasvæði sem haft er áhrif á**         | Viðbætur SDK-smásöluþjóns |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: frá og með útgáfu 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Viðbótar smásöluþjóns með IEdmModelExtender and CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Viðbót smásöluþjóns með IEdmModelExtender og CommerceController hefur verið úrelt til að veita einfaldara viðbótarlíkan. Nýja innleiðingin mun aðeins hafa stýriklasa án frekari útfærslu á IEdmModelExtender innleiðingu. Þetta kemur einnig í þörf fyrir tiltekna OData-útgáfu (ef OData-útgáfan er uppfærð getur það skemmt viðbætur.) |
| **Skipt út fyrir aðra eiginleika?**   |  Mælt er með því að nota nafnaukalíkan fyrir IController-klasa með því að flytja inn NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakkann. |
| **Afurðasvæði sem haft er áhrif á**         | Viðbætur smásöluþjóns |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: frá og með útgáfu 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Viðbót vélbúnaðarstöðvar með IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Viðbót vélbúnaðarstöðvar með IHardwareStationController eru úrelt til að veita einfaldara viðaukalíkan. Nýja innleiðingin er aðeins með IController-klasanum án frekari klasaútfærslu og til að koma í veg fyrir tengsl við söfn vélbúnaðarstöðva, fyrri viðbót þurfti áður að vísa í mörg söfn.) |
| **Skipt út fyrir aðra eiginleika?**   | Mælt er með því að nota nafnaukalíkan IController-klasa með því að flytja inn NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) pakkann. |
| **Afurðasvæði sem haft er áhrif á**         | Viðbætur vélbúnaðarstöðvar |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: frá og með útgáfu 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.10 útgáfu
### <a name="pos-operation-803---picking-and-receiving"></a>POS-aðgerð 803 - Tiltekt og móttaka
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Tiltektar- og móttökuaðgerðir verða úreltar vegna endurhönnunar. |
| **Skipt út fyrir aðra eiginleika?**   | Já. Þeim er skipt út fyrir tvær nýjar sölustaðaaðgerðir: aðgerð á innleið (804) og aðgerð á útleið (805).|
| **Afurðasvæði sem haft er áhrif á**         | Sölustaður (POS) forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá og með útgáfu 10.0.10 verða eiginleikar tiltektar-og móttökuaðgerða ekki lengur uppfærðir. Aðeins alvarlegar villuleiðréttingar verða gerðar fyrir þessa aðgerð í síðari útgáfum. Allir viðskiptavinir eru hvattir til að fara í nýja [Aðgerðir á innleið](../pos-inbound-inventory-operation.md) og [Aðgerðir á útleið](../pos-outbound-inventory-operation.md), sem halda áfram að vera hluti af langtímastefnu okkar fyrir vöruna. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.7 útgáfa
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Forritaskil Commerce GetProductAvailabilities og GetAvailableInventoryNearby
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ný forritaskil hafa verið búin til og koma í stað GetProductAvailabilities GetAvailableInventoryNearby. |
| **Skipt út fyrir aðra eiginleika?**   | Já: Þeim er skipt út fyrir forritaskilin GetEstimatedAvailabilty og GetEstimatedProductWarehouseAvailability. |
| **Afurðasvæði sem haft er áhrif á**         | SDK-forrit rafrænna viðskipta |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá og með útgáfu 10.0.7 verða ekki lengur fjárfest í GetProductAvailabilities og GetAvailableInventoryNearby. Fyrirtæki sem nota þessi API í innleiðingu rafrænna viðskipta ættu að skipta yfir í GetEstimatedAvailabilty og GetEstimatedProductWarehouseAvailability API og virkja [Eiginleika fínstillts útreiknings vöruframboðs](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir
Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
