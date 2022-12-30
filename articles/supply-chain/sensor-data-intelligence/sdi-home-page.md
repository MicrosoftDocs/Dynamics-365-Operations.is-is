---
title: Sensor Data Intelligence heimasíða
description: Í þessari grein er að finna yfirlit yfir Sensor Data Intelligence. Fyrirtæki geta notað þennan eiginleika til að keyra áfram viðskiptaferli í Microsoft Dynamics 365 Supply Chain Management, sem byggir á IoT-merkjum frá vélum og búnaði á framleiðslugólfi.
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
ms.openlocfilehash: ba030364056db8b0524de22aacbc6528ef77813b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689858"
---
# <a name="sensor-data-intelligence-home-page"></a>Sensor Data Intelligence heimasíða

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensor Data Intelligence fyrir Microsoft Dynamics 365 Supply Chain Management gerir fyrirtækjum kleift að reka viðskiptaferli í Supply Chain Management, sem byggir á interenti hlutanna (IoT) merkjum frá vélum og búnaði á framleiðslugólfi. Hann er uppfærð, endurnefnd útgáfa af eiginleikanum *IoT Greind* sem var áður í boði fyrir Supply Chain Management.

Sensor Data Intelligence gerir þér kleift að framkvæma eftirfarandi verk:

- Safna upplýsingum frá vélum og búnaði til að uppfæra teljaragildi viðhalds í Supply Chain Management og keyra spá um viðhald.
- Settu upp lausnina með því að nota einfalt leiðsagnarforrit fyrir innleiðingu í stað þess að setja upp og stilla íhluti handvirkt í Microsoft Dynamics Lifecycle Services (LCS).
- Settu inn hluti í eigin áskrift svo að þú hafir meiri sveigjanleika til að stjórna Azure hlutum.
- Stilla, kvarða og útvíkka lausnina sem viðskiptagrunn sem keyrir á Azure íhlutum. Þeim þáttum er nú stjórnað í þinni eigin áskrift. Þar af leiðandi geturðu sérsniðið þau eins og þarf til að uppfylla sérstakar viðskiptaþarfir þínar.

## <a name="business-scenarios"></a>Sviðsmyndir fyrirtækis

Sensor Data Intelligence opnar á ýmsar aðgerðir sem eru sýndar í tilteknum *aðstæðum* í kerfinu. Allar aðstæður bjóða upp á sérhæfða stillingarvalkosti í kerfinu eins og lýst er í eftirfarandi töflu.

| Aðstæður | Lýsing |
|---|---|
| [Niðurtími eignar](sdi-scenario-asset-downtime.md) | Fylgist nákvæmlega með skilvirkni vélaeigna með því að nota gögn frá skynjara til að fylgjast með niðurtíma véla. |
| [Eignaviðhald](sdi-scenario-asset-maintenance.md) | Lágmarkaðu viðhaldskostnað og lengdu líftíma eigna með því að bæta viðhaldsáætlanir byggðar á skynjaramælingum mikilvægra stjórnstöðva fyrir eignir vélarinnar. |
| [Staða vélar](sdi-scenario-equipment-downtime.md) | Tryggðu skilvirkni í rekstri með því að nota skynjaramælingar til að láta skipuleggjendur vita af vélarbilun og bjóða upp á valkosti til að draga úr hugsanlegum töfum. |
| [Gæði afurðar](sdi-scenario-product-quality.md) | Tryggja skal gæði vörulotna með því að bera saman skynjaramælingar við raunverulega eiginleika hverrar vörulotu, svo sem raka, hitastig eða sérsniðnar gæðamælingar. Kerfið lætur notendur vita þegar frávik eiga sér stað. |
| [Tafir á framleiðslu](sdi-scenario-production-delays.md) | Notaðu skynjaramælingar til að bera saman raunverulegan tíma ferlis við áætlaðan tíma ferlis og láttu umsjónarmenn vita þegar framleiðsla er ekki á áætlun. Þá geta eftirlitsaðilar gripið inn í eftir þörfum til að tryggja hámarks hagkvæmni í rekstri. |

## <a name="architecture"></a>Högun

Á eftirfarandi skipulagsmynd er boðið upp á yfirlit yfir lausnir og íhluti hennar.

![Skipulagsmynd Sensor Data Intelligence.](media/sdi-architecture.png "Skipulagsmynd Sensor Data Intelligence")
