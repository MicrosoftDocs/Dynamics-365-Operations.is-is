---
title: Birgðamerking með fínstillingu áætlanagerðar
description: Þetta efnisatriði inniheldur upplýsingar um valkostina sem eru tiltækir til að merkja birgðir í staðfestum pöntunum þegar fínstilling skipulagningar er notuð.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: dc94ca8b15d626d8ff64f50718d7d2e3e0326144465f3d27787805220842849f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711906"
---
# <a name="inventory-marking-with-planning-optimization"></a>Birgðamerking með fínstillingu áætlanagerðar

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði inniheldur upplýsingar um valkostina sem eru tiltækir til að merkja birgðir í staðfestum pöntunum þegar fínstilling skipulagningar er notuð.

*Merking* er notuð til að tengja framboð og eftirspurn. Slíkt er svipað og *þarfarakning*, sem gefur til kynna hvernig aðaláætlanagerð gerir ráð fyrir því að uppfylla eftirspurn. Frá áætlunarsjónarmiði séð er helsti munurinn sá að merking er varanlegri en þarfarakning.

Merking var tekin í notkun til að styðja við sérstakar kostnaðaraðstæður samkvæmt reglum FIFO- og LIFO-birgðarmatsaðferðanna. Hins vegar er það nú einnig notað fyrir aðstæður sem ekki fela í sér kostnað. Merking milli framboðs og eftirspurnar er valfrjáls og nær varanleg. Notandi getur fjarlægt merkingu handvirkt eða hana má fjarlægja með því að keyra niðurbrot sölupöntunarlínu þar sem valkosturinn **Fjarlægja merkingu** er valinn.

Þarfarakningu er stjórnað af aðaláætlanagerð á meðan á þekju stendur til að tengja eftirspurn við nauðsynleg framboð. Hægt er að uppfæra þarfarakningu fyrir hverja áætlunarkeyrslu til að fínstilla framboðið sem þarf til að uppfylla eftirspurn. Þegar aðaláætlanagerð uppfærir upplýsingar þarfarakningar tekur hún mið af fyrirliggjandi merkingu.

Þarfarakning hefst með því að taka með viðeigandi merkingar, frátekningar á lager og frátekningar í pöntun, í eftirfarandi röð:

1. Merking framboðs og eftirspurnar
1. Frátekningar í birgðum
1. Frátekningar í pöntun

Um leið og áætluð pöntun er staðfest veitir svarglugginn **Staðfesting** svæðið **Uppfæra merki** sem notað er til að stilla valkosti merkisins fyrir pantanirnar sem eru stofnaðar við staðfestingu. Veljið eitt af eftirfarandi gildum:

- **Nei** – Engar birgðir eru merktar.
- **Staðlað** – Birgðamerking er uppfærð í samræmi við jöfnun. Þarfapöntun (þarfir) er merkt gagnvart fullnaðarpöntun (birgðir). Þegar eitthvað magn er eftir í fullnaðarpöntuninni er það ekki merkt og tilvísunarupplýsingarnar eru skildar eftir auðar. Þegar t.d. pöntun á 100 EA er fest við innkaupapöntun fyrir 150 EA verður tilvísunarupplýsingum aðeins úthlutað á sölupöntunina.
- **Útvíkkað** – Bæði þarfapöntun (eftirspurn) og fullnaðarpöntun (framboð) er merkt, burtséð frá því hvort eitthvert magn er eftir í fullnaðarpöntuninni. Þegar t.d. pöntun á 100 EA er fest við innkaupapöntun fyrir 150 EA verður tilvísunarupplýsingum bæði úthlutað á sölupöntunina og innkaupapöntunina.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]