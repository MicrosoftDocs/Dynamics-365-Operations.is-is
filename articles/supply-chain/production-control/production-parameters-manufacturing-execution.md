---
title: "Færibreytur framleiðslu í framkvæmd framleiðslu"
description: "Þetta efnisatriði veitir upplýsingar um uppsetningu framleiðslufæribreytna í Framkvæmd framleiðslu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a0a28ba5072d55b8133f5458f75befa752a3dcdf
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="production-parameters-in-manufacturing-execution"></a>Færibreytur framleiðslu í framkvæmd framleiðslu

[!INCLUDE [banner](../includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um uppsetningu framleiðslufæribreytna í Framkvæmd framleiðslu.

Einingin **Framkvæmd framleiðslu** er fyrst og fremst ætluð framleiðslufyrirtækjum. Hana er hægt að nota til að skrá tíma og vörunotkun í framleiðsluvinnslum eða verkum. Áður en byrjað er að nota Framkvæmd framleiðslu fyrir vinnuskráningu verður þú að setja upp ýmsar framleiðslufæribreytur sem skilgreina hvernig og hvenær skráningar eru bókaðar á meðan á framleiðsluferli stendur. Stilling á framleiðslufæribreytum hefur áhrif á birgðastjórnun, framleiðslustjórnun og kostnaðarútreikning.

Áður en starfsmenn byrja að gera skráningar fyrir framleiðsluvinnslur ættir þú að skoða vel allar stillingar á síðunni **Færibreytur framleiðslu**. Smelltu á **Framleiðslustýring** &gt; **Uppsetning** &gt; **Framkvæmd framleiðslu** &gt; **Sjálfgildi framleiðslupöntunar**. Ef fyrirtækið notar fjölsvæðisvirknina ættir þú ef til vill að setja upp mismunandi framleiðslufæribreytur fyrir hvert svæði. Færibreytur fyrir samþættingu við eininguna **Framleiðsla** eru stilltar á eftirtöldum flipum á síðunni **Framleiðslufæribreytur**:

- **Almennt** – Almennar færibreytustillingar fyrir vinnsluaðgerðir í Framkvæmd framleiðslu.
- **Ræsa** – Færibreytur sem eru notaðar þegar framleiðsluaðgerðir eru hafnar.
- **Aðgerðir** – Færibreytur sem eru notaðar í framleiðsluaðgerðum og svörun vegna aðgerða á meðan á framleiðsluferlinu stendur.
- **Tilbúið** – Færibreytur sem eru notaðar þegar vörur eru skráðar sem lokið í síðustu aðgerð framleiðslupöntunar.
- **Villuleit í magni** – Færibreytur sem eru notaðar til að villuleita upphafs- og svörunarmagn í framleiðslupöntunum.

## <a name="types-of-production-jobs"></a>Gerðir af framleiðsluvinnslum
Á flipanum **Aðgerðir** velur þú hvaða gerðir af framleiðsluvinnslu krefjast skráningar á síðunni **Vinnsluskráning**.

Yfirleitt gera starfsmenn skráningar á uppsetningarvinnslum og vinnslukenni verks. Ef vinnsluröð er notuð er þó hægt að velja aðrar vinnslugerðir sem starfsmenn verða einnig að gera skráningar á þegar framleiðslupantanir eru unnar. Til dæmis er hægt að krefjast skráningar á flutningsvinnslum.

> [!IMPORTANT]
> Gakktu úr skugga um að þú veljir allar viðeigandi vinnslugerðir. Annars gætu vinnslur ekki verið tiltækar fyrir skráningu á í **starfsskráning** síðu. Val þitt ætti að stemma við valið í dálknum **Vinnslustjórnun** á flipanum **Uppsetning** á síðunni **Leiðahópar** (**Framleiðslustýring** &gt; **Uppsetning** &gt; **Leiðir** &gt; **Leiðahópar**).

Ef **Vinnslustýring** er valin á leiðahóp er þessi vinnslutegund skráð sem lokið í framleiðslupöntuninni þegar vinnsla er skráð sem lokið í Framkvæmd framleiðslu. Þegar allar vinnslugerðir sem **Vinnslustjórnun** er valin fyrir hafa verið skráðar í aðgerð skráir Framkvæmd framleiðslu aðgerðina sem lokið.

> [!NOTE]
> Sumar vinnslugerðir er hægt að skrá handvirkt í gegnum framleiðslubækur. Í þessu tifelli skaltu velja **Vinnslustýring** fyrir vinnslutegundina en ekki velja vinnslutegundina fyrir skráningu á flipanum **Aðgerðir** á síðunni **Færibreytur framleiðslu** í Framkvæmd framleiðslu.

## <a name="bom-consumption-and-picking-list-journals"></a>notkun Uppskriftar og tiltektarlistafærslubækur
Samræmd uppsetning á uppskriftarnotkun er mikilvæg þar sem hún stuðlar að skilvirkri birgðastýringu. Ef færibreytur fyrir uppskriftarnotkun eru til dæmis ekki rétt uppsettar í Framkvæmd framleiðslu geta hráefni verið tekin úr birgðum tvisvar sinnum eða alls ekki.

Á síðunni **Færibreytur framleiðslu** er sjálfvirk uppskriftarnotkun sett upp í þremur áföngum:

- Við upphaf framleiðslu. Settu þetta stig upp á flipanum **Ræsa**.
- Meðan á framleiðsluferlinu stendur þegar aðgerð er lokið. Settu þetta stig upp á flipanum **Aðgerðir**.
- Þegar framleiðslupöntun er skráð sem lokið. Settu þetta stig upp á flipanum **Tilbúið**.

Fyrir hvert stig gerir reiturinn **Sjálfvirk uppskriftanotkun** þér kleift að velja eina af þremur aðferðum við að taka til vörur fyrir framleiðslupöntun:

- **Losunarregla** – Þessi valkostur er notaður í tengslum við valkost sem er skilgreindur fyrir uppskriftina í einingunni **Framleiðsla**. Smelltu á **Framleiðslustýring** &gt; **Sameiginlegt** &gt; **Framleiðslupantanir** &gt; **Allar framleiðslupantanir**. Á síðunni **Allar framleiðslupantanir** skaltu velja framleiðslupöntun á listanum og smella svo á **Uppskrift** í aðgerðarúðunni. Á síðunni **Uppskrift** á flipanum **Uppsetning**, í reitnum **Losunarregla**, skaltu velja einn af eftirfarandi valkostum:

  - **Ræsa**
  - **Ljúka**
  - **Handvirkt**
  - Autt (enginn valkostur er valinn.)
  - **Tiltækt í staðsetningu**

    Sé **Losunarregla** valin Framkvæmd framleiðslu, í reitnum **Sjálfvirk uppskriftanotkun** á flipanum **Ræsa**, eru öll hráefni sem eru stillt á **Ræsa** í uppskriftinni dregin frá birgðum þegar aðgerð er hafin. Valkosturinn **Tiltækt í staðsetningu** er notaður fyrir afurðir sem eru virkjaðar fyrir ítarleg vöruhúsaferli. Sé þessi losunarregla valin er hráefni losað þegar vöruhúsavinnu fyrir hráefnatiltekt er lokið. Hráefni er einnig losað þegar uppskriftarlína sem notast við þessa losunarreglu er losuð í vöruhús og hráefnið er tiltækt í staðsetningu framleiðsluinntaks.

    > [!NOTE]
    > Ef reiturinn **Losunarregla** er valinn á flipanum **Ræsa** í framkvæmd framleiðslu verður þú að velja sömu reglu á flipanum **Operations** eða flipanum **Tilkynna sem lokið**. Þessi krafa hjálpar til við að tryggja að efni sé dregið frá birgðum á uppskriftum sem nota **Lokið** sem losunarreglu á framleiðslupöntuninni. Ef sama losunarregla er ekki valin á flipanum **Aðgerðir** eða flipanum **Tilbúið** gæti hráefnið verið dregið tvisvar frá birgðum.

- **Alltaf** – Ef þessi valkostur er valinn fyrir stig er hráefni alltaf dregið frá birgðum á því stigi. Til dæmis er hráefni fyrir framleiðslu dregið frá þegar framleiðslupöntun er hafin. Þessi stilling krefst þess að **Aldrei** sé valið á flipunum **Aðgerðir** og **Tilbúið**. Þessi krafa hjálpar til við að koma í veg fyrir vörur séu dregnar frá lagerbirgðum tvisvar sinnum.
- **Aldrei** – Ef þessi valkostur er valinn fyrir stig á engin uppskriftarnotkun sér stað á því stigi. Ef þú velur til dæmis **Aldrei** á öllum þremur flipunum (**Ræsa**, **Aðgerðir**, og **Tilbúið**) verður að draga hráefni handvirkt frá lagerbirgðum.

> [!IMPORTANT]
> Skoðaðu uppsetninguna á framleiðslufæribreytum vandlega og gakktu úr skugga um að færibreyturnar sem eru valdar á hinum ýmsu flipum síðunnar **Framleiðslufæribreytur** séu ekki í mótsögn hver við aðra.

Eftirfarandi dæmi sýnir færibreytustillingar sem styðja ýmsar reglur um uppskriftarnotkun. Færibreyturnar eru settar upp á síðunni **Framleiðslufæribreytur** í Framkvæmd framleiðslu.

### <a name="example-1-backflushing-on-operations"></a>Dæmi 1: Biðhreinsun á aðgerðum

Notaðu eftirfarandi stillingar ef tiltektarbækur og uppskriftarvörunotkun myndast þegar vörur eru skráðar sem tilbúnar í aðgerð.

| Flipi                | Svæði                          | Stilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Byrja              | Uppfæra gangsetningu á neti           | **Staða** eða **Staða + magn** |
| Byrja              | Sjálfvirk uppskriftanotkun      | **Aldrei**                           |
| Operations         | Sjálfvirk uppskriftanotkun      | **Alltaf**                          |
| Bóka tilbúið | Sjálfvirk uppskriftanotkun      | **Aldrei**                           |
| Bóka tilbúið | Uppfæra skýrslu um tilbúið á neti | **Staða + magn**               |

### <a name="example-2-backflushing-on-production"></a>Dæmi 2: Biðhreinsun á framleiðslu

Notaðu eftirfarandi stillingar ef tiltektarbækur og uppskriftarvörunotkun myndast þegar vörur eru tilkynntar sem tilbúnar í framleiðslupöntun.

| Flipi                | Svæði                          | Stilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Byrja              | Uppfæra gangsetningu á neti           | **Staða** eða **Staða + magn** |
| Byrja              | Sjálfvirk uppskriftanotkun      | **Aldrei**                           |
| Operations         | Sjálfvirk uppskriftanotkun      | **Aldrei**                           |
| Bóka tilbúið | Sjálfvirk uppskriftanotkun      | **Alltaf**                          |
| Bóka tilbúið | Uppfæra skýrslu um tilbúið á neti | **Staða + magn**               |

### <a name="example-3-flushing-principle"></a>Dæmi 3: Losunarregla

Notaðu eftirfarandi stillingar ef tiltektarbækur og uppskriftarvörunotkun myndast samkvæmt stillingu losunarreglu sem er sett fyrir uppskriftarvörur.

| Flipi                | Svæði                          | Stilling                |
|--------------------|--------------------------------|------------------------|
| Byrja              | Uppfæra gangsetningu á neti           | **Staða + magn**  |
| Byrja              | Sjálfvirk uppskriftanotkun      | **Losunarregla** |
| Operations         | Sjálfvirk uppskriftanotkun      | **Losunarregla** |
| Bóka tilbúið | Sjálfvirk uppskriftanotkun      | **Aldrei**              |
| Bóka tilbúið | Uppfæra skýrslu um tilbúið á neti | **Staða + magn**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Dæmi 4: Hráefni dregið frá við upphaf framleiðslupöntunar

Notaðu eftirfarandi stillingar ef tiltektarbækur og uppskriftarvörunotkun eiga að myndast þegar framleiðsla er hafin.

| Flipi                | Svæði                          | Stilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Byrja              | Uppfæra gangsetningu á neti           | **Staða + magn**               |
| Byrja              | Sjálfvirk uppskriftanotkun      | **Alltaf**                          |
| Operations         | Sjálfvirk uppskriftanotkun      | **Aldrei**                           |
| Bóka tilbúið | Sjálfvirk uppskriftanotkun      | **Aldrei**                           |
| Bóka tilbúið | Uppfæra skýrslu um tilbúið á neti | **Staða** eða **Staða + magn** |

Á grundvelli vals sem er lýst fyrr í þessum hluta eru færslubækur tiltektarlista bókaðar á ýmsum stigum framleiðslupöntunarferlisins:

- Þegar aðgerð er ræst
- Þegar magnsvörun er tilkynnt í aðgerð
- Þegar vörur eru tilkynntar sem tilbúnar í framleiðslupöntun

### <a name="example-5-manual-bom-consumption"></a>Dæmi 5: Handvirk uppskriftanotkun

Hægt er að nota eftirfarandi stillingar ef hráefni eiga alltaf að vera dregnar handvirkt frá lagerbirgðum. Í þessu tilfelli eru færslubækur tiltektarlista ekki bókaðar.


|        Flipi         |             Svæði              |         Stilling         |
|--------------------|--------------------------------|-------------------------|
|       Byrja        |      Uppfæra gangsetningu á neti      | <strong>Staða</strong> |
|       Byrja        |   Sjálfvirk uppskriftanotkun    | <strong>Aldrei</strong>  |
|     Operations     |   Sjálfvirk uppskriftanotkun    | <strong>Aldrei</strong>  |
| Bóka tilbúið |   Sjálfvirk uppskriftanotkun    | <strong>Aldrei</strong>  |
| Bóka tilbúið | Uppfæra skýrslu um tilbúið á neti | <strong>Staða</strong> |


