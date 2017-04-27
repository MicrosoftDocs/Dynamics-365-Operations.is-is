---
title: "Sjálfgildi framleiðslupöntunar í framkvæmd framleiðslu"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Sjálfgildi framleiðslupöntunar í framkvæmd framleiðslu

[!include[banner](../includes/banner.md)]




Þú ættir að íhuga vandlega allar stillingar í á **sjálfgildi framleiðslupöntunar** síðuna áður en starfsmenn byrja að gera skráningar fyrir framleiðsluvinnslur. Ef fyrirtækið notar virknina fjölsvæði, viltu kannski setja upp mismunandi sjálfgildi fyrir framleiðslupantanir fyrir hvert svæði. Pantanasjálfgildi fyrir samþættingu við framleiðslustýringar eru settir upp á eftirfarandi flipum á í **sjálfgildi framleiðslupöntunar** síðu:

-   **Almennt** – almenn pantanasjálfgildi fyrir framleiðsluverk í framkvæmd framleiðslu
-   **Hefja** – Pöntunarsjálfgildi sem eru notaðar þegar framleiðsluvinnslur eða aðgerðir eru ræstar.
-   **Aðgerðir** – Pantanasjálfgildi sem er beitt á framleiðsluvinnslur eða aðgerðir og svörun á aðgerðir meðan á framleiðsluferlinu stendur.
-   **Tilkynna sem lokið** - Pantanasjálfgildi sem eru notuð þegar vörur eru tilkynntar sem tilbúnar í síðustu aðgerð framleiðslupöntunar.
-   **Villuleit á magni** – Pantanasjálfgildi fyrir villuleit magns upphafs- og svörunar á framleiðslupantanir.

## <a name="types-of-production-jobs"></a>Gerðir af framleiðsluvinnslum
Á **Aðgerðir** flipa velurðu gerðir af framleiðsluvinnslum sem krefjast skráningar á **starfsskráning** síðu. Yfirleitt gera starfsmenn skráningar á uppsetningarvinnslum og vinnslukenni verks. Hins vegar ef vinnsluröðun er notuð er hægt að velja aðrar vinnslugerðir, eins og flutningsvinnslur, sem starfsmenn verða einnig að gera skráningar á þegar framleiðslupöntun er unnin. **Mikilvægt** Gangið úr skugga um að allar viðeigandi vinnslugerðir séu valdar. Annars gætu vinnslur ekki verið tiltækar fyrir skráningu á í **starfsskráning** síðu. Raðið valinu við valið sem er gert í**Vinnslustjórnun** dálk á **leiðaflokkur** síðu. Ef **Vinnslustjórnun** er valin á leiðaflokki , er vinnslugerð skráð sem tilbúin á framleiðslupöntuninni. Þessi skýrslugerð á sér stað þegar vinnsla er skráð sem lokið í Framleiðslukeyrslu. Þegar allar vinnslugerðir sem **Vinnslustjórnun** er valin fyrir hafa verið tilkynntar sem tilbúnar í aðgerð, mun Framleiðsluframkvæmd einnig tilkynna aðgerðina sem tilbúna. **Athugasemd** Sumar vinnslugerðir er hægt að tilkynna handvirkt í gegnum framleiðslubækur. Veljið í þessu tilfelli **Vinnslustjórnun** fyrir vinnslugerð, en veljið ekki vinnslugerðina til skráningar á í **Aðgerðir** flipanum á í **sjálfgildi framleiðslupöntunar** síðu.

## <a name="bom-consumption-and-picking-list-journals"></a>notkun Uppskriftar og tiltektarlistafærslubækur
Efni er hægt að setja upp þannig að þær eru notaðar annað hvort sjálfvirkt eða handvirkt í framleiðslu. Sjálfvirk notkun er stjórnað af losunarreglu sem sett er upp á í uppskriftarlínum (BOM) og með stillingu í **Sjálfvirk uppskriftanotkun** reit í sjálfgildi framleiðslupöntunar. Sjálfvirka notkuner hægt að setja upp þannig að hún eigi sér stað þegar framleiðslupöntun er hafin eða skráð sem lokið. Einnig er hún getur átt sér stað á stigi vinnslu þegar vinnsla er byrjuð eða lokið.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Stjórn efnisnotkun þegar framleiðslupöntun er ræst

Efnisnotkun við byrjun framleiðslupöntunar er stjórnað af á **Sjálfvirk uppskriftanotkun** á í **Ræsa** flipa. Eftirtalin gildi eru tiltæk:

-   **Losunarregla** – Þegar framleiðslupöntun er hafin er magni af efni sem verður notaðar samkvæmt losunarreglu sem er stillt á uppskriftarlínum framleiðslu. Aðeins efnislínur þar sem losunarregla er stillt á **Ræsa** verður notuð við upphaf framleiðslu.
-   **Alltaf** – Magni af efni sem eru í hlutfalli við ræst magn verður alltaf notað.
-   **Aldrei** – Magn af efni verður aldrei notað.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Stjórna efnisnotkun þegar framleiðslupöntun er ræst eða lokið.

Efnisnotkun við byrjun eða lok framleiðsluverks er stjórnað af á **Sjálfvirk uppskriftanotkun** reit á í **aðgerðir ** flipa. Eftirtalin gildi eru tiltæk:

-   **Losunarregla** – Þegar magn á framleiðsluverki er hafin eða lokið er magni af efni sem verður notaðar samkvæmt losunarreglu sem er stillt á uppskriftarlínum framleiðslu. Aðeins efnislínur þar sem losunarregla er stillt á **Ræsa**  **lokið** verður notuð.
-   **Alltaf** – Magni af efni sem eru í hlutfalli við ræst magn á verki verður alltaf notað.
-   **Aldrei** – Magn af efni verður aldrei notað.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Stjórn efnisnotkun þegar framleiðslupöntun er tilkinn sem lokið.

Efnisnotkun við tilkynna sem lokið ferlið fyrir framleiðslupöntunar er stjórnað af á **Sjálfvirk uppskriftanotkun** á í **tilkynna sem lokið** flipa. Eftirtalin gildi eru tiltæk:

-   **Losunarregla** – Þegar framleiðslupöntun er tilkynnt sem lokið er magni af efni sem verður notaðar samkvæmt losunarreglu sem er stillt á uppskriftarlínum framleiðslu. Aðeins efnislínur þar sem losunarregla er stillt á **lokið** verður notuð.
-   **Alltaf** – Magni af efni sem eru í hlutfalli við magn sem er tilkynnt sem lokið verður alltaf notað.
-   **Aldrei** – Magn af efni verður aldrei notað.





