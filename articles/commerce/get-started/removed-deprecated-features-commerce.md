---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Commerce
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Commerce.
author: josaw
ms.date: 01/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: f80d1509c7c363e93b83cb47c1b93ab00bf67180
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193469"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Commerce.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!NOTE]
> Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](/dynamics/s-e/). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Commerce 10.0.17 útgáfu

### <a name="full-dataset-generation-interval-is-deprecated"></a>Tímabil myndunar fullbúins gagnasafns er úrelt

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá og með þessari útgáfu, í **Færibreytur viðskiptaverkraðara** í Dynamics 365 Headquarters, er reiturinn **Tímabil myndunar fullbúins gagnasafns í dögum** ekki notaður. Í þessari útgáfu verður reiturinn fjarlægður þannig að ekki er hægt að breyta gildinu. Þetta mun halda áfram sem gildið **0**. |
| **Skipt út fyrir aðra eiginleika?**   | Ekkert |
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
| **Dreifingarvalkostur**              | Allir|
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