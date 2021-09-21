---
title: Aðaláætlanagerð áætlar meira en tiltæka afkastagetu
description: Aðaláætlanagerð virðist ekki taka mið af takmörkunum afkastagetu og áætlar meira en tiltæk afkastageta
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476674"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Aðaláætlanagerð áætlar meira en tiltæka afkastagetu

## <a name="symptoms"></a>Einkenni

Aðaláætlanagerð virðist ekki taka mið af takmörkunum afkastagetu og áætlar meira en tiltæk afkastageta.

Þegar aðgerðaröðun er notuð þar sem takmörkuð afkastageta er til staðar og leiðin tilgreinir blöndu af kröfum bæði tilfangaflokks og einstakra tilfanga er möguleiki á ofbókun vegna aðferðarinnar sem algrím notar til að villuleita árekstra í afkastagetu. Þessi ofbókun getur átt sér stað þegar hjálpartæki eru notuð til að keyra aðaláætlanagerð. Líklegra er að slíkt hendi þegar mörg verk með hlutfallslega stutta keyrslu eru til staðar.

## <a name="resolution"></a>Lausn

Þegar nauðsynlegt að engin ofbókun eigi sér stað við aðgerðaröðun er hægt að gera áætlanahluta aðaláætlanagerðarinnar að stökum þræði með því að kveikja á valkostinum **Nákvæm takmörkuð geta fyrir aðgerðaröðun** á síðunni **Færibreytur aðaláætlanagerðar**. Þessi valkostur er ekki tiltækur sjálfgefið. Þú verður að bæta henni handvirkt við síðuna með því að nota sérstillingar. Þegar þessi valkostur er notaður verður áætlanagerð keyrð hægar því samhliða keyrsla er ekki til staðar.
