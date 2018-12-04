---
title: "Hlutar fjárhagsskýrslu"
description: "Í þessari grein er því lýst hvernig hlutar, eða einingar, skýrsluskiglreiningar eru notaðar í fjárhagsskýrslu. Þessar einingar eru línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar. Í þessari grein er útskýrt hvernig á að skipuleggja og læsa einingum, og hvernig unnið er með einingahópa."
author: aprilolson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 0829c9eb54a8a5ca1f78bfe85de4779e541b945a
ms.contentlocale: is-is
ms.lasthandoff: 08/13/2018

---

# <a name="financial-report-components"></a>Hlutar fjárhagsskýrslu

[!include [banner](../includes/banner.md)]

Í þessari grein er því lýst hvernig hlutar, eða einingar, skýrsluskiglreiningar eru notaðar í fjárhagsskýrslu. Þessar einingar eru línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar. Þetta efnisatriði útskýrir hvernig einingar eru skipulagðar og þeim læst.

Hugmyndin á bak við hönnunarviðmót fyrir fjárhagsskýrslur byggir á því að brjóta upplýsingar niður í smæstu einingar eða grunneiningar, og blanda þeim svo saman eftir þörfum. Því er skýrslusniðið aðskilið fjárhagsgögnum og hægt er að breyta útliti skýrslu án þess að breyta fjárhagsgögnunum í Microsoft Dynamics ERP-kerfinu. Með því að nota þessa nálgun eininga, er hægt að sameina texta, upphæðir og útreikninga til að útbúa skýrslur sem þarf. Að sama skapi auðveldar sveigjanleikinn notendum að skoða aðgerðir út frá mismunandi sjónarhornum og hvetur þannig til skapandi lausna. Hver eining í skýrsluskilgreiningu virkar nokkurn veginn eins og þrívíður töflureiknir, nema að hún er öflugri. Skýrsluskilgreining tilgreinir línuskilgreininguna, dálkskilgreininguna og valfrjálsa skilgreiningu skipurits sem ætti að nota í skýrslunni. Hún hefur einnig að geyma upplýsingar um hvar geyma skal skýrsluna sem er mynduð og hvernig á að sníða hana.

## <a name="building-blocks-of-a-report"></a>Einingar skýrslu

| Eining            | lýsing | Frekari upplýsingar |
|---------------------------|-------------|----------------------|
| Skilgreining línu            | Línuskilgreining tilgreinir lýsandi línur í skýrslu (til dæmis laun eða sölu). Í henni er jafnframt listi yfir hlutagildi eða víddir sem innihalda gildin fyrir hvert línuatriði auk þess sem hún inniheldur línusnið og útreikninga. | [Línuskilgreiningar](row-definitions-financial-reporting.md) |
| Skilgreining dálks         | Dálkskilgreining tilgreinir hvaða tímabil á að nota þegar gögn eru dregin út úr fjárhagsvíddum. Hún inniheldur einnig dálksnið og útreikninga. | [Dálkskilgreiningar](column-definitions-financial-reports.md) |
| Skilgreining skipurits | Skilgreiningu skipurits svipar til hefðbundins skipurits. Hún inniheldur stakar einingar skipurits sem standa fyrir hvern kassa í skipuritinu. Einingarnar geta verið annaðhvort einstaka deildir úr fjárhagsgögnum eða einingar á hærri stigum sem taka saman gögn frá öðrum einingum skipurits. | [Skilgreiningar skipurits](financial-reporting-tree-definitions.md) |
| Skýrsluskilgreining         | Skýrsluskilgreining notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skilgreiningu skipurits til að búa til skýrslu. Hún býður einnig upp á viðbótarvalkosti og stillingar sem hægt er að nota til að sérsníða skýrslu. | [Skýrsluskilgreining](design-financial-report-definitions.md) |

Ef notandi hefur ekki hannað skýrslur áður kann að vera gagnlegt að nota leiðsagnarforritið fyrir skýrslugerð til að stofna skýrsluskilgreiningu á fljótlegan hátt sem hægt er að sérstilla síðar. Ef notandi hefur reynslu af því að hanna skýrslur og kýs meiri sveigjanleika við skýrsluhönnun er hægt að stofna nýja skýrsluskilgreiningu með því að tengja saman nýjar eða fyrirliggjandi einingar. Til þess að geta útbúið vandaðar skýrslur þarf notandi ekki að þekkja til hlítar alla þá valkosti sem standa til boða fyrir skýrsluskilgreiningu. Eftir því sem notandinn öðlast meiri reynslu af skýrsluhönnun getur hann hins vegar bætt við skýrsluskilgreiningarnar til að nýta sér flóknari eiginleika. Þegar stofnuð hefur verið einföld skýrsla er hægt að sérsníða skýrsluskilgreininguna og einingar hennar.

## <a name="organize-the-building-blocks"></a>Einingar skipulagðar
Möppur eru notaðar til að raða einingum í Skýrsluhönnun. Allar möppur eru sérstaklega ætlaðar fyrir tegund eininganna sem þær innihalda. Til dæmis eru allar möppur sem innihalda línuskilgreiningar staðsettar á svæðinu **Línuskilgreiningar** í Report Designer.

### <a name="create-a-folder"></a>Stofna möppu.

1. Veljið tegund einingar sem á að raða í yfirlitssvæðinu í Skýrsluhönnun. Smellið til dæmis á **Línuskilgreiningar** til að raða línuskilgreiningu.
2. Á yfirlitssvæðinu er valin fyrirliggjandi mappa sem nýja mappan verður stofnuð í og síðan er eitt af eftirfarandi skrefum framkvæmt:

    - Hægrismellið á yfirmöppuna og veljið **Ný mappa**.
    - Veljið yfirmöppuna, smellið á **Skrá** og smellið síðan á **Ný mappa**.

3. Þegar nýja mappan birtist er heiti nýju möppunnar slegið inn og svo ýtt á færslulykilinn.

## <a name="lock-a-building-block"></a> Einingu læst
Hægt er að stofna aðgangsorð til að verja og læsa einingu. Þannig er öryggisstigi bætt við skýrsluíhlut án þess að allt kerfið sé tryggt um leið. Aðgangsorð getur hjálpað til við að verja einingarupplýsingar sem eru mikilvægar fyrir skýrsluferli við mánaðarlok. Allir notendur geta læst einingu. Hins vegar hafa aðrir notendur alltaf lesaðgang að læsta hlutanum. Notendur geta opnað, breytt og vistað læsta íhlutinn undir nýju heiti. Notandi með hlutverk stjórnanda getur ávallt fengið aðgang að og breytt læstri einingu.

1. Opnið skýrslueininguna sem á að læsa í Report Designer, svo sem línuskilgreiningu, dálkskilgreiningu, skýrsluskilgreiningu eða skilgreiningu skipurits.
2. Á valmyndinni **Verkfæri** er smellt á **Verkja/taka vörn af**. Einnig er hægt að smella á **Verja/taka vörn af** (lástáknið) á tækjastikunni.
3. Í svarglugganum **Verja** skal slá inn og staðfesta aðgangsorð og smella á **Í lagi**. Lástáknið á tækjastikunni er auðkennt þegar opin eining er læst.

Til að taka lás af læstri einingu skal opna eininguna og smella á táknið **Verja/taka vörn af** á tækjastikunni. Á valmyndinni **Verkfæri** er einnig hægt að smella á **Verkja/taka vörn af**.

## <a name="building-block-groups"></a>Einingahópar

Einingar eru línuskilgreiningarnar, dálkskilgreiningarnar og skipuritsskilgreiningarnar sem stofnaðar eru fyrir skýrslu. Einingahópar eru söfn skilgreininga og víddasamstæða.

### <a name="view-a-building-block-group"></a>Einingahópur skoðaður

Hægt er að skoða allar einingar sem eru tengdir einingahópum. Einnig er hægt að flytja einingahópa inn og út.

1. Á valmyndinni **Fyrirtæki** í Report Designer er smellt á **Einingarhópar**.
2. Í svarglugganum **Einingarhópar** er einingin valin sem á að skoða.
3. Smellið á **Skoða** til að opna svargluggann **Skoða einingarhóp** þar sem hægt er að skoða innihald einingahópsins.
4. Smellið á **Loka** til að loka svargluggunum.

### <a name="export-a-building-block-group"></a>Einingahópur fluttur út

Einnig er hægt að flytja einingahóp út eða tilteknar skýrslueiningar í einingahóp. Hægt er að nota einingahóp sem hefur verið fluttur út sem afrit. Einnig er hægt að afrita gögn sem voru flutt út uppsettra Finance and Operations. Skýrsluhönnun tekur með leturstíl sem vísað er til og víddasamstæður með í einingahópnum.

1. Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Einingarhópar**.
2. Í svarglugganum **Einingarhópar** er valinn einingahópurinn sem á að flytja út og síðan er smellt á **Flytja út**.
3. Smellið á skýrsluskilgreiningarnar í svarglugganum **Flytja út** til að flytja út:

    - Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    - Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út. Haldið inni Ctrl-lyklinum til að velja mörg atriði á flipa.

    > [!NOTE]
    > Þegar valdar eru skýrslur til að flytja út eru einnig valdar tengdar línur, dálkar, skipurit og víddasamstæður.

4. Smellið á **Flytja út** þegar búið er að velja atriði til að flytja út.
5. Í svarglugganum **Vista sem** er valin staðsetningin sem flytja á einingahópinn til.
6. Í reitnum **Skrárheiti** er heiti fyrir skrána fært inn. Report Designer bætir sjálfkrafa við .tdbx skrárendingu.
7. Smelltu á **Vista**. Einingahópurinn er vistaður á staðsetningunni sem var tilgreind.

### <a name="import-a-building-block-group"></a>Einingahópur fluttur inn

Hægt er að flytja inn einingahóp í fyrirliggjandi einingahóp. Allir einingahópar sem fluttir eru inn halda upprunalegum leturstíl sínum sem og tilvísunum í fyrirtæki og taka með sér viðeigandi víddasamstæður.

1. Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Einingarhópar**.
2. Í svarglugganum **Einingarhópar** er valin eining sem á að flytja einingahóp í og síðan er smellt á **Flytja inn**.
3. Í svarglugganum **Opna** er valinn einingahópurinn sem á að flytja inn og síðan er smellt á **Opna**.
4. Smellið á skýrsluskilgreiningarnar í svarglugganum **Flytja inn** til að flytja inn:

    - Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    - Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.

5. Smellið á **Flytja inn** þegar búið er að velja atriði til að flytja inn.

### <a name="undo-a-checkout-of-a-building-block"></a>Útskráning einingar afturkölluð

Þegar eining er opnuð geta aðrir notendur aðeins fengið lesaðgang að þeirri einingu. Stundum gleymir notandi að loka einingu eða slekkur á kerfinu án þess að loka einingunni. Af því leiðir að einingin er útskráð og engir notendur geta opnað hana. Við þessar aðstæður getur stjórnandi fjárhagsskýrslna notað svargluggann **Útskráð atriði** til að skrá inn einingar sem einhver notandi hefur skilið eftir í útskráðri stöðu.

> [!NOTE]
> Aðeins stjórnandi getur skráð inn einingar í svarglugganum **Útskráð atriði**.

1. Á valmyndinni **Verkfæri** í Skýrsluhönnun er smellt á **Útskráð atriði**.
2. Veljið **Sýna vörur frá öllum notendum** í svarglugganum **Útskráð atriði**. Listinn uppfærist og sýnir allar einingar sem hafa verið skráðar út og hvaða notendur það voru sem skráðu þær út.
3. Veljið einingu og smellið síðan á **Afturkalla útskráningu**.
4. Smellið á **Já** til að skrá inn eininguna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Fjárhagsskýrslugerð](financial-reporting-intro.md)

