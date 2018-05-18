---
title: "Framleiðslubókun"
description: "Þessi grein gefur upplýsingar um mismunandi tegundir bókana í framleiðsluferlinu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 413bf76b40ec1e6d00322605900a71f163c9396c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="production-posting"></a>Framleiðslubókun

[!include [banner](../includes/banner.md)]

Þessi grein gefur upplýsingar um mismunandi tegundir bókana í framleiðsluferlinu.

Verkþættir framleiðslubókunar fylgja framleiðsluferli sem lýst er í eftirfarandi hlutum.

## <a name="material-consumption"></a>Efnisnotkun
Efni eru skráðar sem notuð í framleiðslu þegar tiltektarlisti framleiðslubókar er bókuð. Þetta ferli myndar úthreyfingarfærslur sem draga frá birgðum á lager. Í færibreytum framleiðslu er hægt að tilgreina hvort gildi hráefna sem eru í vinnslu (verk í vinnslu \[VÍV\]) skuli bókuð í fjárhaginn. Gildi hráefna sem eru í vinnslu (VÍV) er síðan bókuð sérstakan lykil tiltektarlista og sérstakan mótlykil tiltektarlista.

## <a name="time-consumption"></a>Tímanotkun
Tíminn sem starfsmenn nota í framleiðsluvinnslu er skráð í færslubók leiðarspjalds eða vinnsluspjaldsbókinni. Þegar þessar færslubækur eru bókaðar er unnin fjárhagsbókun á sérstakan lykil fyrir tilföng sem eru í vinnslu (VÍV). Þessi bókun sýnir virði tímans sem er varið í framleiðslupöntun. Eftir að framleiðslupöntunin er skráð sem lokið, er vív-lyklar eru jafnaðir.

## <a name="reporting-finished-goods-and-error-quantities"></a>Tilkynni um Fullbúnar vörur og villumagn
Þegar framleiðslupöntun er skráð sem lokið, er magn fullbúinna vara sem var lokið uppfært í Birgðastjórnun í gegnum færslubókina Bóka sem tilbúið. Ef verið er að nota bókhald fyrir verk í vinnslu (VÍV), sem má setja upp í færibreytum framleiðslu, er færslubók fjárhags búin til til að minnka vív-lyklar og auka birgðir fullbúinnar vöru. Færslubók notar staðlaðan kostnað sem er skilgreint fyrir afurðina.

## <a name="ending-the-production-order"></a>Lokið við framleiðslupöntunina
Áður er framleiðslupöntun er lokið er raunkostnaður reiknaður fyrir magnið sem var framleitt. Allur áætlaður kostnaður fyrir efni, vinnu og rekstrarkostnaði er bakfærður og skipt út fyrir raunkostnað. Heildarkostnaðurinn fyrir tilbúna afurð er debetfærður úr innhreyfinglykli birgða og kreditfærður á úthreyfingarlykil afurðar. Ef þú velur **Ljúka vinnslu** gátreitur þegar þú keyrir kostnaðarútreikningur, breytist staða framleiðslupöntunar í **Lokið**. Þessi staða kemur í veg fyrir aukalegan kostnað sé óvart bókaður á lokna framleiðslupöntun. Hægt er að tilgreina að gildi villumagns sem eru skráðar sem loknar við skýrslugerðsem skuli úthluta á gallalausa magnið sem er skráð sem lokið. Einnig er hægt að tilgreina að virðis villumagns eigi að bóka á sérstakan rýrnunarlykil.

## <a name="controlling-the-level-of-ledger-posting"></a>Stýra stigi fjárhagsbókunar
Í **færibreytur framleiðslustýringar**, er hægt að nota í **fjárhagsbókun** svæði til að stilla stig fjárhagsbókunar fyrir framleiðsluferli. Eftirtalin gildi eru tiltæk:

-   **Afurð og tilföng** – Notið fjárhagslykla sem eru settir upp á vöruflokka fyrir hráefni og fullbúnar vörur. VÍV fyrir tímanotkun er sótt úr tilfangi eða tilfangaflokki úr leiðaraðgerðir.
-   **Afurð og flokkur** – Notið fjárhagslykla sem eru settir upp á vöruflokka fyrir hráefni og fullbúnar vörur. VÍV fyrir tímanotkun er sótt úr kostnaðarflokkum sem eru tengdir við leiðaraðgerðir.
-   **Framleiðsluflokkar** – Notið fjárhagslykla sem eru sett upp í framleiðsluflokkum fyrir bæði efni og tímanotkun. Framleiðsluflokkarnir eru tengdir við útgefnar afurðir og afritaðir í framleiðslupantanir þegar þessar pantanir eru stofnaðar. Bókun á framleiðslupantanir  mun svo fylgja framleiðsluflokkum sem eru tengdir við framleiðslupöntunina.

**Athugasemd** Ef staðlaða aðferðin til að reikna út kostnað við tilbúna vöru var notuð, endurspegla lokafærslurnar það. Ef það er mismunur á raunkostnaði og útreiknuðum kostnaði með notkun stöðluðu aðferðarinnar, er mismunurinn bókaður á lykilinn sem sýnir hagnað eða tap.




