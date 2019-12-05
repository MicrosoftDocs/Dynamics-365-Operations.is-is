---
title: Skipta mynduðum XML-skrám út frá skráarstærð og efnismagni
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig á að skipta mynduðum skrám út frá stærð og efnismagni.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 804878150f035adc051e89ec6be44457ad58e87e
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771192"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Skipta mynduðum XML-skrám út frá skráarstærð og efnismagni

[!include[banner](../includes/banner.md)]

Hægt er að hanna snið rafrænnar skýrslugerðar til að búa til skjöl á útleið í XML-sniði. Stundum er aðeins hægt að samþykkja þessi skjöl þegar þau uppfylla sérstakar kröfur á borð við hámarksskráarstærð eða hámarksfjölda sumra XML-hnúta. Hægt er að hanna snið rafrænnar skýrslugerðar til að búa til rafræn skjöl sem uppfylla kröfur sem viðtakendur þessara skjala tilgreina.

- Fyrir skráarsniðseininguna er hægt að tilgreina mörk á skráarstærð sem segð rafrænnar skýrslugerðar. Ef farið er yfir tilgreind mörk þegar skýrsla rafrænnar skýrslugerðar er búin til, lýkur rafræn skýrslugerð við að stofna núverandi skrá og heldur síðan áfram við að stofna næstu skrá.
- Fyrir sérhverja XML-sniðseiningu er hægt að tilgreina mörk á fjölda eininga sem segð rafrænnar skýrslugerðar. Ef fjöldi XML-hnúta í skránni sem er búin til fer yfir tilgreind mörk þegar skýrsla rafrænnar skýrslugerðar er keyrð, lýkur rafræna skýrslugerðin við að búa til núverandi skrá og heldur síðan áfram við að stofna næstu skrá.
- Fyrir hvaða XML-sniðseiningarröð er hægt að skilgreina mörk á fjölda undireininga sem segð rafrænnar skýrslugerðar. Ef fjöldi faldaðra XML-hnúta sniðseiningarinnar í mynduðu skránni fer yfir skilgreind mörk þegar skýrsla rafrænnar skýrslugerðar er keyrð, lýkur rafræn skýrslugerð við að búa til núverand skrá og heldur síðan áfram við að stofna næstu skrá.
- Hægt er að merkja hvaða XML-sniðseiningu sem óskiptanlega. Á þennan hátt er hægt að halda földuðum atriðum XML-hnúta sem eru búnir til undir sniðseiningunni í einni myndaðri skrá.

Til viðbótar við að nota sniðseiningar XML-einingar og XML-raðar til að bæta XML-hnútum við mynduðu skrána, er hægt að nota hráa XML-sniðseiningu. Hins vegar eru hnútar sem þú bætir við með því að nota hráa XML-sniðseiningu ekki teknir til greina þegar fjöldi hnúta er reiknaður út til að meta mörk á fjölda eininga.

Ef þú hefur skilgreint viðtökustað skráar fyrir sniðseiningu skráar sem hefur verið skilgreind til að skipta mynduðu úttaki í hvert skipti sem farið er yfir mörkin, er hverju skipti af mynduðu úttaki sent á viðtökustað skilgreindrar skráar sem sjálfstæð skrá. Til að gefa skránum sem eru stofnaðar með því að skipta niður úttakinu einkvæmt heiti verður að skilgreina segð rafrænnar skýrslugerðar fyrir sniðseiningu skráarinnar. Ef gagnagjafi rafrænnar skýrslugerðar af gerðinni númeraröð er tekinn með mun númeraröðin fara stigvaxandi fyrir hvert atriði af skipta úttakinu.

Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeininguna **Skipting XML-skráa rafrænnar skýrslugerðar á grundvelli skáarstærðar eða magni innihaldsefnis** sem er hluti af viðskiptaferlinu **7.5.4.3 Acquire/Develop IT- þjónustu-/lausnarhlutum (10677)** og sem hægt er að hlaða niður frá [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Þessi verkefnaleiðbeining fylgir þér í gegnum ferlið við að grunnstilla snið rafrænnar skýrslugerðar til að skipta mynduðum skrám á grundvelli marka á skráarstærð og magni innihaldsefnis. Til að ljúka verkefnaleiðbeiningunum verður að sækja eftirfarandi skrár:

- [Skilgreining líkans fyrir rafræna skýrslugerð - XmlFilesSplittingModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [Skilgreining sniðs fyrir rafræna skýrslugerð - XmlFilesSplittingFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a>Frekari upplýsingar
[Áfangastaðir rafrænnar skýrslugerðar (ER)](electronic-reporting-destinations.md)

[Formúluhönnuður í rafrænni skýrslugerð (ER)](general-electronic-reporting-formula-designer.md)
