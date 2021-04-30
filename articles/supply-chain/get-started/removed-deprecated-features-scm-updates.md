---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 785f9055c44110d88b9494b5066647511840b646
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909648"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Þetta efni verður uppfært þegar nýir fjarlægðir eða úreltir eiginleikar eru skráðir fyrir Dynamics 365 Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.

> [!NOTE]
> Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](/dynamics/s-e/). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Supply Chain Management 10.0.18 útgáfa

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations - Vöruhúsaforrit (vöruhúsaforritið)

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá apríl 2021 er *Dynamics 365 for Finance and Operations - Vöruhús* (þetta vöruhúsaforrit) úrelt og það verður ekki stutt eftir apríl 2022. Því er nú skipt út fyrir *Farsímaforrit vöruhúsakerfis*, sem var gefið út í útgáfu 10.0.17 af Supply Chain Management. Nýja forritið kemur í stað þess eldra en notar sama undirliggjandi ramma sem auðveldar flutning. Hægt er að nota forritin hlið við hlið til að notendur geti vanist nýja forritinu.<br><br>Ef leitað er upplýsinga um hvernig eigi að skilgreina gamla farsímaforritið fyrir farsímaforrit vöruhúsakerfis skal skoða [Farsímaforrit vöruhúsakerfi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) og [Setja upp og tengja farsímaforrit vöruhúsakerfis](../warehousing/install-configure-warehouse-management-app.md). |
| **Skipt út fyrir aðra eiginleika?**   | Já, skipt út fyrir nýtt farsímaforrit vöruhúsakerfis. |
| **Afurðasvæði sem haft er áhrif á**         | Supply Chain Management - vöruhúsaforrit |
| **Dreifingarvalkostur**              | Ský og innanhúss |
| **Staða**                         | Úrelt. Vöruhúsaforritið verður stutt vegna villna og öryggismála, en eiginleikar þess verða ekki endurbættir. Eftir að apríl 2022 verður gamla vöruhúsaforritið ekki lengur stutt og viðskiptavinir verða beðnir um að færa sig yfir í nýtt farsímaforrit vöruhúsakerfis. Gamla vöruhúsforritið verður fjarlægt úr Microsoft Store og Google Play.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Supply Chain Management 10.0.15 útgáfa

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 stuðningi við Dynamics 365 hefur verið hætt

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá desember 2020, er Microsoft Internet Explorer 11 stuðningi fyrir allar Dynamics 365 vörur hætt og Internet Explorer 11 verða ekki stutt eftir ágúst 2021.<br><br>Þetta mun hafa áhrif á viðskiptavini sem nota Dynamics 365 vörur sem eru hannaðar til að nota með Internet Explorer 11 viðmóti. Eftir ágúst 2021 er Internet Explorer 11 ekki stutt fyrir þessar Dynamics 365 vörur. |
| **Skipt út fyrir aðra eiginleika?**   | Við mælum með því að viðskiptavinir skipti yfir í Microsoft Edge.|
| **Afurðasvæði sem haft er áhrif á**         | Allar Dynamics 365 vörur |
| **Dreifingarvalkostur**              | Allir|
| **Staða**                         | Úrelt. Internet Explorer 11 verður ekki stutt eftir ágúst 2021.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Notkun á aðaláætlunarvél fyrir innbyggða Supply Chain Management fyrir framleiðsluaðstæður

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Til að auka afköst og draga úr álagi SQL-gagnagrunns við keyrslu aðaláætlunar er verið að skipta út grunnstillingu á Supply Chain Management vél fyrir fínstilling áætlanagerðar. Fínstilling áætlanagerðar gerir kleift að keyra hraða áætlanagerð sem jafnvel er hægt að framkvæma á skrifstofutíma. Þetta gerir skipuleggjendum kleift að bregðast tafarlaust við breytingum á eftirspurn eða áætlunarfæribreytum. |
| **Skipt út fyrir aðra eiginleika?**   | Já, fínstilling áætlanagerðar kemur í stað núverandi aðaláætlunarvélar Supply Chain Management. |
| **Afurðasvæði sem haft er áhrif á**         | Supply Chain Management - Aðaláætlanagerð |
| **Dreifingarvalkostur**              | Aðeins ský. Fínstilling áætlanagerðar er ekki studd með uppsetningu á staðnum. |
| **Staða**                         | Úrelt. Þann 1. apríl 2022 verða framleiðsluaðstæður ekki lengur studdar með innbyggðri Dynamics 365 Supply Chain Management aðaláætlunarvél. Fyrir framleiðsluaðstæður verða viðskiptavinir að nota fínstillingu áætlanagerðar fyrir útreikning aðaláætlunar. Nánari upplýsingar er að finna í [fylgiskjölum fínstillingar áætlanagerðar](../master-planning/planning-optimization/planning-optimization-overview.md). Viðskiptavinir með uppsetningu á staðnum á Dynamics 365 Supply Chain Management geta haldið áfram að nota aðaláætlunarvél Supply Chain Management fyrir framleiðsluaðstæður eftir apríl 2022. Ekki verður boðið upp á fleiri umbætur á eiginleikum. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Supply Chain Management 10.0.11 útgáfa

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Notkun á aðaláætlunarvél fyrir innbyggða Supply Chain Management fyrir dreifingaraðstæður

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Til að auka afköst og draga úr álagi SQL-gagnagrunns við keyrslu aðaláætlunar er verið að skipta út grunnstillingu á Supply Chain Management vél fyrir fínstilling áætlanagerðar. Fínstilling áætlanagerðar gerir kleift að keyra hraða áætlanagerð sem jafnvel er hægt að framkvæma á skrifstofutíma. Þetta gerir skipuleggjendum kleift að bregðast tafarlaust við breytingum á eftirspurn eða áætlunarfæribreytum. |
| **Skipt út fyrir aðra eiginleika?**   | Já, fínstilling áætlanagerðar kemur í stað núverandi aðaláætlunarvélar Supply Chain Management. |
| **Afurðasvæði sem haft er áhrif á**         | Supply Chain Management - Aðaláætlanagerð |
| **Dreifingarvalkostur**              | Aðeins ský. Fínstilling áætlanagerðar er ekki studd með uppsetningu á staðnum. |
| **Staða**                         | Úrelt. Þann 1. apríl 2021 verða dreifingaraðstæður ekki lengur studdar með innbyggðri Dynamics 365 Supply Chain Management aðaláætlunarvél. Fyrir dreifingaraðstæður verða viðskiptavinir að nota fínstillingu áætlanagerðar fyrir útreikning aðaláætlunar. Nánari upplýsingar er að finna í [fylgiskjölum fínstillingar áætlanagerðar](../master-planning/planning-optimization/planning-optimization-overview.md). Viðskiptavinir með uppsetningu á staðnum á Dynamics 365 Supply Chain Management geta haldið áfram að nota aðaláætlunarvél Supply Chain Management fyrir dreifingaraðstæður eftir apríl 2021. Ekki verður boðið upp á fleiri umbætur á eiginleikum. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir

Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]