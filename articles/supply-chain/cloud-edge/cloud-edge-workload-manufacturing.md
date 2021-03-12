---
title: Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra
description: Þetta efnisatriði lýsir því hvernig vinnuálag framkvæmdar framleiðslu starfar með kvörðunareiningum skýja og jaðra.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08c46655d3966ad1433935318c5e60667dd10bb6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967765"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Vinnuálag framleiðslukeyrslu fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Tiltekin virkni fyrirtækisins er ekki studd að fullu í almennu forskoðuninni þegar kvörðunareiningar skýja og jaðra eru notaðar.

Við framkvæmd framleiðslu veita kvörðunareiningar skýja og jaðra eftirfarandi getu, jafnvel þegar kvörðunareiningarnar eru ekki tengdar við miðstöðina:

- Stjórnandi véla og eftirlitsmenn vinnusalar fá aðgang að framleiðsluáætlun.
- Stjórnendur vél geta uppfært áætlunina með því að keyra afmarkað og verk framleiðsluferlis.
- Umsjónarmaður vinnusalar getur breytt starfsáætluninni.
- Starfskraftar geta opnað tíma og viðveru til innstimplunar og útstimplunar á jaðrinum til að tryggja réttan útreikning launa starfsmanna.

Þetta efnisatriði lýsir því hvernig vinnuálag framkvæmdar framleiðslu starfar með kvörðunareiningum skýja og jaðra.

## <a name="the-manufacturing-lifecycle"></a>Stuðningstími framleiðslu

Eins og eftirfarandi skýringarmynd sýnir er stuðningstíma framleiðslu skipt í þrjá áfanga: *Áætlun*, *Keyrslu* og *Lok*.

[![Áfangar framkvæmdar framleiðslu þegar stakt umhverfi er notað](media/mes-phases.png "Áfangar framkvæmdar framleiðslu þegar stakt umhverfi er notað")](media/mes-phases-large.png)

Áfanginn _Áætlun_ felur í sér skilgreiningu afurðar, áætlanagerð, stofnun og áætlun afurðar og losun. Útgáfuskrefið tilgreinir skiptin úr áfanganum _Áætlun_ yfir í áfangann _Keyrsla_. Þegar framleiðslupöntun er losuð verða verk framleiðslupöntunar sýnileg á framleiðslugólfinu og tilbúnar til framkvæmdar.

Þegar framleiðsluverk er merkt sem lokið, færist verkið úr áfanganum _Keyrsla_ yfir í áfangann _Lok_. Í áfanganum _Lok_ fara skráningarnar úr áfanganum *Keyrsla* í gegnum samþykktarverkflæði og eru reiknaðar, samþykktar og fluttar. Á þeim tímapunkti er framleiðslupöntuninni lokið. Þar af leiðandi er myndaður grunnur fyrir laun starfskrafta.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Skipta áfanganum Keyrsla í aðskilið vinnuálag

Eins og sýnt er á eftirfarandi skýringarmynd, þegar notast er við kvörðunareiningar, er áfanganum _Keyrsla_ skipt niður sem aðskilið vinnuálag.

[![Áfangar framkvæmdar framleiðslu þegar kvörðunareiningar eru notaðar](media/mes-phases-workloads.png "Áfangar framkvæmdar framleiðslu þegar kvörðunareiningar eru notaðar")](media/mes-phases-workloads-large.png)

Líkanið færist nú frá stakri uppsetningu yfir í líkan sem er byggt á miðstöðinni og kvörðunareiningunum. Áfangarnir _Áætlun_ og _Lok_ keyra sem aðgerðir bakvinnslu á miðstöðinni og vinnuálag framkvæmdar framleiðslu er keyrð á kvörðunareiningunum. Gögn eru flutt á ósamstilltan hátt á milli miðstöðvarinnar og kvörðunareininganna.

Þegar framleiðslupöntun er losuð í miðstöðinni verða öll gögn sem þarf til að vinna úr framleiðsluverkum flutt yfir í kvörðunareininguna. Þessi gögn fela í sér framleiðslupantanir, framleiðsluleiðir, uppskriftir og afurðir. Gögn sem eru ekki tengd framleiðslupöntun (svo sem óbeinir verkþættir, fjarvistarkóðar og færibreytur framleiðslu) eru einnig flutt frá miðstöðinni yfir í kvörðunareininguna. Gögn sem koma frá miðstöðinni og eru flutt yfir í kvörðunareininguna er að jafnaði einungis hægt að stofna eða uppfæra á miðstöðinni. Ekki er t.d. hægt að stofna nýjan fjarvistakóða eða óbeinan verkþátt á kvörðunareiningu&mdash;sem þeir geta aðeins notað fyrir skráningu. Skráningarnar sem gerðar eru á kvörðunareiningunni við keyrslu eru síðan fluttar í miðstöðina, þar sem unnið er úr samþykki á tíma og viðveru, birgðum og fjárhagslegum uppfærslum.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Verk framkvæmdar framleiðslu sem keyra má á vinnuálagi

Hægt er að keyra eftirfarandi verk framkvæmdar framleiðslu á vinnuálagi þegar kvörðunareiningar eru notaðar:

- Innstimplun, innskráning, útstimplun og fjarvistir
- Ræsa vinnslu
- Sameina vinnslur
- Gera framvinduskýrslu
- Tilkynna rýrnun
- Óbeinn verkþáttur
- Hlé

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Unnið með vinnuálag framkvæmdar framleiðslu í miðstöðinni

Yfirleitt eru áskilin ferli til keyrslu vinnuálags framkvæmdar framleiðslu keyrð sjálfkrafa til að halda miðstöðinni og öllum kvörðunareiningunum samstilltum eins og þörf er á. Þegar þú lendir í vandræðum er hins vegar hægt að ræsa handvirkt vinnslu á hráum skráningum sem mótteknar eru frá vinnuálagi og/eða athuga vinnslukladda hrárrar skráningar.

### <a name="manually-process-raw-registrations"></a>Vinna handvirkt úr hráum skráningum

Runuvinnsla í Supply Chain Management keyrir sjálfkrafa til að vinna úr öllum skráningum sem hafa verið mótteknar úr vinnuálaginu. Þessi vinnsla stofnar nauðsynlegar framleiðslubækur og færslubókarfærslur þegar skráning er unnin fyrir vinnslu sem er lokið á vinnuálaginu.

Þrátt fyrir að vinnslan sé yfirleitt keyrð sjálfkrafa er hægt að keyra hana handvirkt hvenær sem er með því að skrá þig inn á miðstöðina og opna **Framleiðslustýring \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu \> Vinna úr hráum skráningum**.

### <a name="check-the-raw-registration-processing-log"></a>Athugun á vinnslukladda hrárra skráningar

Þegar endurskoða á vinnslukladda skráningar skal skrá sig inn á miðstöðina og opna **Framleiðslustýring \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu \> Vinnslukladdi hrárrar skráningar**. Síðan **Vinnslukladdi hrárrar skráningar** sýnir lista yfir unnar hráar skráningar og stöðu hverrar skráningar fyrir sig.

![Vinnslukladdasíða hrárrar skráningar](media/mes-processing-log.png "Vinnslukladdasíða hrárrar skráningar")

Hægt er að vinna með allar skráningar á listanum með því að velja skráningu og síðan smella á einn af eftirfarandi hnöppum á aðgerðasvæðinu:

- **Vinnsla** – Vinna handvirkt úr valinni skráningu. Þessi aðgerð getur komið sér vel ef vinnslan _Úrvinnsla hrárra skráninga_ var ekki keyrt eða það mistókst.
- **Hætta við** – Hætta við völdu skráninguna.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Unnið með vinnuálag framkvæmdar framleiðslu í kvarðaeiningu

Yfirleitt eru áskilin ferli til keyrslu vinnuálags framkvæmdar framleiðslu keyrð sjálfkrafa til að halda miðstöðinni og öllum kvörðunareiningunum samstilltum eins og þörf er á. Þegar þú lendir í vandræðum getur þú athugað feril pantana sem hefur verið unnið úr í kvörðunareiningu eða keyrt handvirkt vinnsluna _Skilaboðaúrvinnsla framleiðslumiðstöðvar til einingarkvarða_.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Skoða feril framleiðsluvinnslu sem hefur verið unnin á kvörðunareiningu

Þegar endurskoða á framleiðsluvinnslu sem hefur verið unnin á kvörðunareiningu skal skrá sig inn í kvörðunareiningavélina og opna **Framleiðslustýring \> Reglubundin verkefni \> Stjórnun vinnuálags í bakvinnslu \> Vinnsluferill framleiðsluvinnslu**. **Vinnsluferill framleiðsluvinnslu** sýnir vinnsluferil framleiðslupantana í kvörðunareiningunni. Hægt er að vinna í öllum framleiðslupöntunum á listanum með því að velja framleiðslupöntun og smella síðan á einn af eftirfarandi hnöppum á aðgerðasvæði:

- **Vinnsla** – Vinna handvirkt úr valinni framleiðslupöntun.
- **Hætta við** – Hætta við völdu framleiðslupöntunina.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Skilaboðaúrvinnsla framleiðslumiðstöðvar til vinnslu kvörðunareiningar

Vinnslan _Skilaboðaúrvinnsla framleiðslumiðstöðvar til kvörðunareiningar_ vinnur úr gögnum frá miðstöðinni til kvörðunareiningarinnar. Þessi vinnsla hefst sjálfkrafa um leið og vinnuálag framkvæmdar framleiðslu er keyrt. Hins vegar er hægt að keyra slíkt handvirkt hvenær sem er með því að opna **Framleiðslustýringu \> Reglubundin verk \> Stjórnun vinnuálags í bakvinnslu \> Skilaboðaúrvinnsla framleiðslumiðstöðvar til kvörðunareiningar**.
