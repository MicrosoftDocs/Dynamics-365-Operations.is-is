---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir í Dynamics 365 Supply Chain Management.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597117"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

Þetta efni verður uppfært þegar nýir fjarlægðir eða úreltir eiginleikar eru skráðir fyrir Dynamics 365 Supply Chain Management.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð.

> [!NOTE]
> Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Eiginleikar sem eru úreltir eða hafa verið fjarlægðir í Supply Chain Management 10.0.11 útgáfa

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Notkun á aðaláætlunarvél fyrir innbyggða Supply Chain Management fyrir dreifingaraðstæður

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Til að auka afköst og draga úr álagi SQL-gagnagrunns við keyrslu aðaláætlunar er verið að skipta út grunnstillingu á Supply Chain Management vél fyrir fínstilling áætlanagerðar. Fínstilling áætlanagerðar gerir kleift að keyra hraða áætlanagerð sem jafnvel er hægt að framkvæma á skrifstofutíma. Þetta gerir skipuleggjendum kleift að bregðast tafarlaust við breytingum á eftirspurn eða áætlunarfæribreytum. |
| **Skipt út fyrir aðra eiginleika?**   | Já, fínstilling áætlanagerðar kemur í stað núverandi aðaláætlunarvélar Supply Chain Management. |
| **Afurðasvæði sem haft er áhrif á**         | Supply Chain Management - Aðaláætlanagerð |
| **Dreifingarvalkostur**              | Aðeins ský. Fínstilling áætlanagerðar er ekki studd með uppsetningu á staðnum. |
| **Staða**                         | Úrelt. Í apríl 2021 verða dreifingaraðstæður ekki lengur studdar með innbyggðri Dynamics 365 Supply Chain Management aðaláætlunarvél. Fyrir dreifingaraðstæður verða viðskiptavinir að nota fínstillingu áætlanagerðar fyrir útreikning aðaláætlunar. Nánari upplýsingar er að finna í [fylgiskjölum fínstillingar áætlanagerðar](https://go.microsoft.com/fwlink/?linkid=2105830). Viðskiptavinir með uppsetningu á staðnum á Dynamics 365 Supply Chain Management geta haldið áfram að nota aðaláætlunarvél Supply Chain Management fyrir dreifingaraðstæður eftir apríl 2021. Ekki verður boðið upp á fleiri umbætur á eiginleikum. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir

Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
