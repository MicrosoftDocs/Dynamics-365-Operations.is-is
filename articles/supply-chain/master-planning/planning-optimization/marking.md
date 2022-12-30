---
title: Birgðamerking
description: Þessi grein inniheldur upplýsingar um valkostina sem eru tiltækir til að merkja birgðir í staðfestum pöntunum.
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
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740578"
---
# <a name="inventory-marking"></a>Birgðamerking

[!include [banner](../../includes/banner.md)]

Þessi grein inniheldur upplýsingar um valkostina sem eru tiltækir til að merkja birgðir í staðfestum pöntunum.

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
- *Staðlað eitt stig* – Merking fyrir eitt stig notuð. Merking fyrir eitt stig merkir aðeins aðalvöruna, ekki íhluti uppskrift þess (BOM). Því er hægt að halda íhlutum til úthlutunar fyrir framleiðslupantanir breytilegum eftir staðfestingu. Merking fyrir eitt stig gerir kerfinu kleift að fínstilla fyrir breytingar á eftirspurn á síðustu stundu. Í *hefðbundinni* eins stigs merkingu eru þarfapantanir merktar gegn fullnaðarpöntunum þeirra en fullnaðarpantanir eru ekki merktar ef þær hafa eftirstandandi magn.
- *Eitt stig framlengt* – Merking fyrir eitt stig notuð. Í *framlengdri* eins stigs merkingu eru þarfapantanir merktar gegn fullnaðarpöntunum þeirra, og fullnaðarpantanir eru alltaf merktar, burtséð frá því hvort eitthvert magn er eftir.

Til að stilla sjálfgefinn merkingarvalkost fyrir kerfið skal fara í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**. Síðan skal í flipanum **Stöðluð uppfærsla** stilla reitinn **Uppfæra merkingu** á æskilegan valkost.

> [!NOTE]
> Valkostirnir *Staðlað eitt stig* og *Stækkað eitt stig* eru aðeins í boði ef eiginleikinn *Sjálfvirkt framboð með „framleiða eftir pöntun“* er virkjaður í kerfinu. Frekari upplýsingar um þennan eiginleika og hvernig á að virkja hann má finna í [Sjálfvirkt framboð með „framleiða eftir pöntun](../make-to-order-supply-automation.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
