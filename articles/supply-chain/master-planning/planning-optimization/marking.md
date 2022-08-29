---
title: Birgðamerking með fínstillingu áætlunargerðar
description: Þessi grein veitir upplýsingar um valkostina sem eru tiltækir til að merkja birgðahald í staðfestum pöntunum þegar þú notar áætlanagerð fínstillingu.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 55c83cdbc144f194fe80e8281a35ec7ff43d551e
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219938"
---
# <a name="inventory-marking-with-planning-optimization"></a>Birgðamerking með fínstillingu áætlunargerðar

[!include [banner](../../includes/banner.md)]

Þessi grein veitir upplýsingar um valkostina sem eru tiltækir til að merkja birgðahald í staðfestum pöntunum þegar þú notar áætlanagerð fínstillingu.

*Merking* er notuð til að tengja framboð og eftirspurn. Slíkt er svipað og *þarfarakning*, sem gefur til kynna hvernig aðaláætlanagerð gerir ráð fyrir því að uppfylla eftirspurn. Frá áætlunarsjónarmiði séð er helsti munurinn sá að merking er varanlegri en þarfarakning.

Merking var tekin í notkun til að styðja við sérstakar kostnaðaraðstæður samkvæmt reglum FIFO- og LIFO-birgðarmatsaðferðanna. Hins vegar er það nú einnig notað fyrir aðstæður sem ekki fela í sér kostnað. Merking milli framboðs og eftirspurnar er valfrjáls og nær varanleg. Notandi getur fjarlægt merkingu handvirkt eða hana má fjarlægja með því að keyra niðurbrot sölupöntunarlínu þar sem valkosturinn **Fjarlægja merkingu** er valinn.

Þarfarakningu er stjórnað af aðaláætlanagerð á meðan á þekju stendur til að tengja eftirspurn við nauðsynleg framboð. Hægt er að uppfæra þarfarakningu fyrir hverja áætlunarkeyrslu til að fínstilla framboðið sem þarf til að uppfylla eftirspurn. Þegar aðaláætlanagerð uppfærir upplýsingar þarfarakningar tekur hún mið af fyrirliggjandi merkingu.

Þarfarakning hefst með því að taka með viðeigandi merkingar, frátekningar á lager og frátekningar í pöntun, í eftirfarandi röð:

1. Merking framboðs og eftirspurnar
1. Frátekningar í birgðum
1. Frátekningar í pöntun

Um leið og áætluð pöntun er staðfest veitir svarglugginn **Staðfesting** svæðið **Uppfæra merki** sem notað er til að stilla valkosti merkisins fyrir pantanirnar sem eru stofnaðar við staðfestingu. Veljið eitt af eftirfarandi gildum:

- *Nei* – Engar birgðir eru merktar.
- *Staðlað* – Birgðamerking er uppfærð í samræmi við jöfnun. Þarfapöntun (þarfir) er merkt gagnvart fullnaðarpöntun (birgðir). Þegar eitthvað magn er eftir í fullnaðarpöntuninni er það ekki merkt og tilvísunarupplýsingarnar eru skildar eftir auðar. Þegar t.d. pöntun á 100 EA er fest við innkaupapöntun fyrir 150 EA verður tilvísunarupplýsingum aðeins úthlutað á sölupöntunina.
- *Útvíkkað* – Bæði þarfapöntun (eftirspurn) og fullnaðarpöntun (framboð) er merkt, burtséð frá því hvort eitthvert magn er eftir í fullnaðarpöntuninni. Þegar t.d. pöntun á 100 EA er fest við innkaupapöntun fyrir 150 EA verður tilvísunarupplýsingum bæði úthlutað á sölupöntunina og innkaupapöntunina.
- *Staðall á einu stigi* – Einstigs merking er notuð. Einþreps merking merkir aðeins aðalhlutinn, ekki efnisskrá (BOM) íhluti hans. Þess vegna er hægt að halda íhlutaúthlutun fyrir framleiðslupantanir sveigjanlegan eftir styrkingu. Eins stigs merking gerir kerfinu kleift að hagræða fyrir breytingar á eftirspurn á síðustu stundu. Í *staðall* eins stigs merking, kröfupantanir eru merktar við uppfyllingarpantanir þeirra, en uppfyllingarpantanir eru ekki merktar ef þær hafa eftirstandandi magn.
- *Einhæð stækkuð* – Einstigs merking er notuð. Í *framlengdur* eins stigs merking, kröfupantanir eru merktar við uppfyllingarpantanir þeirra og uppfyllingarpantanir eru alltaf merktar, óháð því hvort eitthvað magn er eftir.

Til að stilla sjálfgefna merkingarvalkost fyrir kerfið þitt skaltu fara á **Aðalskipulag \> Uppsetning \> Aðalskipulagsbreytur**. Síðan, á **Hefðbundin uppfærsla** flipann, stilltu **Uppfæra merkingu** reit í valinn valkost.

> [!NOTE]
> The *Staðall á einu stigi* og *Einhæð stækkuð* valkostir eru aðeins í boði ef *Sjálfvirkni framboðs eftir pöntun* eiginleiki er virkur á kerfinu þínu. Fyrir frekari upplýsingar um þennan eiginleika og hvernig á að virkja hann, sjá [Sjálfvirkni framboðs eftir pöntun](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
