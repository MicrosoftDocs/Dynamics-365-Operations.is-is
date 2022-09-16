---
title: Heimasíða Sensor Data Intelligence
description: Þessi grein veitir yfirlit yfir Sensor Data Intelligence. Stofnanir geta notað þennan eiginleika til að keyra viðskiptaferla í Microsoft Dynamics 365 Supply Chain Management, byggt á Internet of Things (IoT) merkjum frá vélum og búnaði á framleiðslugólfinu.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429007"
---
# <a name="sensor-data-intelligence-home-page"></a>Heimasíða Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Sensor Data Intelligence fyrir Microsoft Dynamics 365 Supply Chain Management gerir stofnunum kleift að keyra viðskiptaferla í Supply Chain Management, byggt á Internet of Things (IoT) merkjum frá vélum og búnaði á framleiðslugólfinu. Það er uppfærð, endurnefnd útgáfa af *IoT Intelligence* eiginleiki sem áður var fáanlegur fyrir Supply Chain Management.

Sensor Data Intelligence gerir þér kleift að framkvæma eftirfarandi verkefni:

- Safnaðu upplýsingum frá vélum og búnaði til að uppfæra teljaragildi viðhaldseigna í Supply Chain Management og keyra forspárviðhald.
- Settu upp lausnina með því að nota einfaldan inngönguhjálp í stað þess að setja upp og stilla íhluti handvirkt í Microsoft Dynamics Lífsferilsþjónusta (LCS).
- Dreifðu íhlutum í þína eigin áskrift, þannig að þú hafir meiri sveigjanleika til að stjórna Azure íhlutum.
- Stilla, skala og framlengja lausnina sem viðskiptarökfræði sem keyrir á Azure íhlutum. Þeim hlutum er nú stjórnað í þinni eigin áskrift. Þess vegna geturðu sérsniðið þau eftir þörfum til að mæta einstökum viðskiptaþörfum þínum.

## <a name="business-scenarios"></a>Viðskiptasviðsmyndir

Sensor Data Intelligence gerir nokkrar gerðir af virkni kleift, sem hver um sig er táknuð með ákveðinni *atburðarás* í kerfinu. Hver atburðarás býður upp á sérhæft sett af stillingarvalkostum í kerfinu, eins og lýst er í eftirfarandi töflu.

| Aðstæður | Lýsing |
|---|---|
| [Niðurtími eignar](sdi-scenario-asset-downtime.md) | Fylgstu nákvæmlega með skilvirkni vélaeigna með því að nota skynjaragögn til að rekja niðurtíma vélarinnar. |
| [Viðhald eigna](sdi-scenario-asset-maintenance.md) | Lágmarka viðhaldskostnað og lengja líftíma eigna með því að bæta viðhaldsáætlanir byggðar á skynjaralestri á mikilvægum stjórnstöðum fyrir vélaeignir. |
| [Staða vélar](sdi-scenario-equipment-downtime.md) | Tryggðu skilvirkni í rekstri með því að nota skynjaralestur til að tilkynna skipuleggjendum um bilanir í vélinni og bjóða upp á möguleika til að draga úr hugsanlegum töfum. |
| [Gæði afurðar](sdi-scenario-product-quality.md) | Tryggðu gæði vörulota með því að bera saman skynjaralestur fyrir raunverulega eiginleika hverrar vörulotu, svo sem raka, hitastig eða sérskilgreindar gæðamælingar. Kerfið mun láta notendur vita þegar frávik eiga sér stað. |
| [Tafir á framleiðslu](sdi-scenario-production-delays.md) | Notaðu skynjaralestur til að bera saman raunverulegan lotutíma við áætlaðan lotutíma og láta yfirmenn vita þegar framleiðsla er ekki á áætlun. Eftirlitsmenn geta síðan gripið inn í eftir þörfum til að tryggja hámarks hagkvæmni í rekstri. |

## <a name="architecture"></a>Högun

Eftirfarandi byggingarskýringarmynd gefur yfirlit yfir lausnina og íhluti hennar.

![Sensor Data Intelligence byggingarlistarmynd.](media/sdi-architecture.png "Sensor Data Intelligence byggingarlistarmynd")
