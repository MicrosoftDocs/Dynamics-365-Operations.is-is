---
title: "Hlutar fjárhagsskýrslu"
description: "Í þessari grein er því lýst hvernig hlutar, eða einingar, skýrsluskiglreiningar eru notaðar í fjárhagsskýrslu. Þessar einingar eru línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar. Í þessari grein er útskýrt hvernig á að skipuleggja og læsa einingum, og hvernig unnið er með einingahópa."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5c09b1fc061f95cd78e9f18c2bdf846fdbfc7cf1
ms.contentlocale: is-is
ms.lasthandoff: 06/13/2017

---

# <a name="financial-report-components"></a>Hlutar fjárhagsskýrslu

[!include[banner](../includes/banner.md)]


Í þessari grein er því lýst hvernig hlutar, eða einingar, skýrsluskiglreiningar eru notaðar í fjárhagsskýrslu. Þessar einingar eru línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar. Í þessari grein er útskýrt hvernig á að skipuleggja og læsa einingum, og hvernig unnið er með einingahópa. 

Hugmyndin á bak við hönnunarviðmót fyrir fjárhagsskýrslur byggir á því að brjóta upplýsingar niður í smæstu einingar eða grunneiningar, og blanda þeim svo saman eftir þörfum. Því er skýrslusniðið aðskilið fjárhagsgögnum og hægt er að breyta útliti skýrslu án þess að breyta fjárhagsgögnunum í Microsoft Dynamics ERP-kerfinu. Með því að nota þessa nálgun eininga, er hægt að sameina texta, upphæðir og útreikninga til að útbúa skýrslur sem þarf. Að sama skapi auðveldar sveigjanleikinn notendum að skoða aðgerðir út frá mismunandi sjónarhornum og hvetur þannig til skapandi lausna. Hver eining í skýrsluskilgreiningu virkar nokkurn veginn eins og þrívíður töflureiknir, nema að hún er öflugri. Skýrsluskilgreining tilgreinir línuskilgreininguna, dálkskilgreininguna og valfrjálsa skilgreiningu skipurits sem ætti að nota í skýrslunni. Hún hefur einnig að geyma upplýsingar um hvar geyma skal skýrsluna sem er mynduð og hvernig á að sníða hana. Til að auðvelda endur- og samnýtingu eininga er hægt að stofna einingahóp, sem er safn fyrirliggjandi skýrsluskilgreininga, línuskilgreininga, dálkskilgreininga, skilgreininga skipurita og víddasamstæða sem tengjast fyrirtæki í.

## <a name="building-blocks-of-a-report"></a>Einingar skýrslu
| Eining            | Lýsing                                                                                                                                                                                                                                                                              | Frekari upplýsingar                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Skilgreining línu            | Línuskilgreining tilgreinir lýsandi línur í skýrslu (til dæmis laun eða sölu). Í henni er jafnframt listi yfir hlutagildi eða víddir sem innihalda gildin fyrir hvert línuatriði auk þess sem hún inniheldur línusnið og útreikninga.                                                    | [Línuskilgreiningar](row-definitions-financial-reporting.md)                       |
| Skilgreining dálks         | Dálkskilgreining tilgreinir hvaða tímabil á að nota þegar gögn eru dregin út úr fjárhagsvíddum. Hún inniheldur einnig dálksnið og útreikninga.                                                                                                                                 | [Dálkskilgreiningar](column-definitions-financial-reports.md)         |
| Skilgreining skipurits | Skilgreiningu skipurits svipar til hefðbundins skipurits. Hún inniheldur stakar einingar skipurits sem standa fyrir hvern kassa í skipuritinu. Einingarnar geta verið annaðhvort einstaka deildir úr fjárhagsgögnum eða einingar á hærri stigum sem taka saman gögn frá öðrum einingum skipurits. | [Skilgreiningar skipurits](financial-reporting-tree-definitions.md) |
| Skýrsluskilgreining         | Skýrsluskilgreining notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skilgreiningu skipurits til að búa til skýrslu. Hún býður einnig upp á viðbótarvalkosti og stillingar sem hægt er að nota til að sérsníða skýrslu.                                                                    | [Skýrsluskilgreining](design-financial-report-definitions.md)                  |

Ef notandi hefur ekki hannað skýrslur áður kann að vera gagnlegt að nota leiðsagnarforritið fyrir skýrslugerð til að stofna skýrsluskilgreiningu á fljótlegan hátt sem hægt er að sérstilla síðar. Ef notandi hefur reynslu af því að hanna skýrslur og kýs meiri sveigjanleika við skýrsluhönnun er hægt að stofna nýja skýrsluskilgreiningu með því að tengja saman nýjar eða fyrirliggjandi einingar. Til þess að geta útbúið vandaðar skýrslur þarf notandi ekki að þekkja til hlítar alla þá valkosti sem standa til boða fyrir skýrsluskilgreiningu. Eftir því sem notandinn öðlast meiri reynslu af skýrsluhönnun getur hann hins vegar bætt við skýrsluskilgreiningarnar til að nýta sér flóknari eiginleika. Þegar stofnuð hefur verið einföld skýrsla er hægt að sérsníða skýrsluskilgreininguna og einingar hennar.

## <a name="organize-the-building-blocks"></a>Einingar skipulagðar
Möppur eru notaðar til að raða einingum í Skýrsluhönnun. Allar möppur eru sérstaklega ætlaðar fyrir tegund eininganna sem þær innihalda. Til dæmis eru allar möppur sem innihalda línuskilgreiningar staðsettar á svæðinu **Línuskilgreiningar** í Report Designer.

### <a name="create-a-folder"></a>Stofna möppu.

1.  Veljið tegund einingar sem á að raða í yfirlitssvæðinu í Skýrsluhönnun. Smellið til dæmis á **Línuskilgreiningar** til að raða línuskilgreiningu.
2.  Á yfirlitssvæðinu er valin fyrirliggjandi mappa sem nýja mappan verður stofnuð í og síðan er eitt af eftirfarandi skrefum framkvæmt:
    -   Hægrismellið á yfirmöppuna og veljið **Ný mappa**.
    -   Veljið yfirmöppuna, smellið á **Skrá** og smellið síðan á **Ný mappa**.

3.  Þegar nýja mappan birtist er heiti nýju möppunnar slegið inn og svo ýtt á færslulykilinn.

## <a name="lock-a-building-block"></a> Einingu læst
Hægt er að stofna aðgangsorð til að verja og læsa einingu. Þannig er öryggisstigi bætt við skýrsluíhlut án þess að allt kerfið sé tryggt um leið. Aðgangsorð getur hjálpað til við að verja einingarupplýsingar sem eru mikilvægar fyrir skýrsluferli við mánaðarlok. Allir notendur geta læst einingu. Hins vegar hafa aðrir notendur alltaf lesaðgang að læsta hlutanum. Notendur geta opnað, breytt og vistað læsta íhlutinn undir nýju heiti. Notandi með hlutverk stjórnanda getur ávallt fengið aðgang að og breytt læstri einingu.
1.  Opnið skýrslueininguna sem á að læsa í Report Designer, svo sem línuskilgreiningu, dálkskilgreiningu, skýrsluskilgreiningu eða skilgreiningu skipurits.
2.  Á valmyndinni **Verkfæri** er smellt á **Verkja/taka vörn af**. Einnig er hægt að smella á **Verja/taka vörn af** (lástáknið) á tækjastikunni.
3.  Í svarglugganum **Verja** skal slá inn og staðfesta aðgangsorð og smella á **Í lagi**. Lástáknið á tækjastikunni er auðkennt þegar opin eining er læst.

Til að taka lás af læstri einingu skal opna eininguna og smella á táknið **Verja/taka vörn af** á tækjastikunni. Á valmyndinni **Verkfæri** er einnig hægt að smella á **Verkja/taka vörn af**.

## <a name="building-block-groups"></a>Einingahópar

Einingar eru línuskilgreiningarnar, dálkskilgreiningarnar og skipuritsskilgreiningarnar sem stofnaðar eru fyrir skýrslu. Einingahópar eru söfn skilgreininga og víddasamstæða sem eru tengdar fyrirtæki. Einingahópar geta tengst tilteknu fyrirtæki en nokkur fyrirtæki geta einnig deilt einingahópi. Ef notandi er með fyrirtæki sem hafa mismunandi bókhaldslykla gæti verið gott að nota mismunandi einingahópa fyrir hvert fyrirtæki. Annar möguleiki er að gefa hverri stakri einingu sérstakt heiti sem lýsir því við hvaða fyrirtæki sú eining er samhæf.
### <a name="create-a-building-block-group"></a>Einingahópur stofnaður

1.  Á valmyndinni **Fyrirtæki** í Report Designer er smellt á **Einingarhópar**.
2.  Í svarglugganum **Einingarhópar** er smellt á **Nýtt**.
3.  Færið inn einkvæmt heiti og lýsingu á einingahópnum. Hver reitur má innihalda að hámarki 256 stafi. (Þessi fjöldi inniheldur bil.)
4.  Smellt er á **Í lagi** til að stofna nýjan einingahóp.

### <a name="assign-a-building-block-group"></a>Einingahópi úthlutað

Þegar einingahópur hefur verið stofnaður þarf að úthluta honum til a.m.k. eins fyrirtækis. Því næst er hægt að stofna skýrslu, línu, dálk og skipuritsskilgreiningu og vista í einingahópnum. Loka þarf öllum einingum áður en hægt er að byrja á eftirfarandi ferli.
1.  Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Fyrirtæki**.
2.  Í svarglugganum **Fyrirtæki** skal velja fyrirtæki sem úthluta á einingahópnum til.
3.  Smellið á **Breyta**.
4.  Í svarglugganum **Breyta fyrirtæki** í reitnum **Einingarhópur** skal velja einingahópinn sem úthluta á því fyrirtæki eða smella á **Nýtt** til að stofna nýjan einingahóp.
5.  Smellið á **Í lagi** til að úthluta nýja einingahópnum.
6.  Smellt er á **Loka** til að loka svarglugganum **Fyrirtæki**. Einingahópnum sem valinn var hefur nú verið úthlutað til fyrirtækisins. Nú munu allar línuskilgreiningar, dálkskilgreiningar og svo framvegis sem eru stofnaðar vera hluti einingahópsins sem er úthluta á þetta fyrirtæki. Einnig er hægt að flytja inn .tdbx-skrá eða skýrslu úr öðru kerfi.

### <a name="view-a-building-block-group"></a> Einingahópur skoðaður

Þegar einingahópur hefur verið stofnaður og notaður er hægt að skoða allar einingar sem hafa verið tengdar við hann. Einnig er hægt að flytja einingahóp út eða inn og framkvæma frekara viðhald á einingahópunum.
1.  Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Einingarhópar**.
2.  Í svarglugganum **Einingarhópar** er einingin valin sem á að skoða.
3.  Smellið á **Skoða** til að opna svargluggann **Skoða einingarhóp** þar sem hægt er að skoða innihald einingahópsins.
4.  Smellið á **Loka** til að loka svargluggunum.

### <a name="save-a-building-block-group-under-a-new-name"></a>Einingahópur vistaður undir nýju heiti

Hægt er að vista einingahóp sem þegar er til undir nýju heiti. Síðan má breyta nýja einingahópnum án þess að breyta upprunalega einingahópnum.
1.  Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Einingarhópar**.
2.  Í svarglugganum **Einingarhópar** er valinn einingahópurinn sem á að vista undir nýju heiti.
3.  Smellið á **Vista sem**.
4.  Færið inn nýtt heiti og lýsingu á einingahópnum.
5.  Smelltu á **Í lagi**. Nýi einingahópurinn birtist í svarglugganum **Einingarhópar**.

### <a name="export-a-building-block-group"></a>Einingahópur fluttur út

Einnig er hægt að flytja einingahóp út eða tilteknar skýrslueiningar í einingahóp. Hægt er að nota einingahóp sem hefur verið fluttur út sem afrit. Einnig er hægt að afrita gögn sem voru flutt út milli einingahópa eða uppsettra Finance and Operations. Skýrsluhönnun tekur með leturstíl sem vísað er til og víddasamstæður með í einingahópnum.
1.  Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Einingarhópar**.
2.  Í svarglugganum **Einingarhópar** er valinn einingahópurinn sem á að flytja út og síðan er smellt á **Flytja út**.
3.  Smellið á skýrsluskilgreiningarnar í svarglugganum **Flytja út** til að flytja út:
    -   Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    -   Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út. Haldið inni Ctrl-lyklinum til að velja mörg atriði á flipa. **Athugasemd:** Þegar valdar eru skýrslur til að flytja út eru einnig valdar tengdar línur, dálkar, skipurit og víddasamstæður.

4.  Smellið á **Flytja út** þegar búið er að velja atriði til að flytja út.
5.  Í svarglugganum **Vista sem** er valin staðsetningin sem flytja á einingahópinn til.
6.  Í reitnum **Skrárheiti** er heiti fyrir skrána fært inn. Report Designer bætir sjálfkrafa við .tdbx skrárendingu.
7.  Smelltu á **Vista**. Einingahópurinn er vistaður á staðsetningunni sem var tilgreind.

### <a name="import-a-building-block-group"></a>Einingahópur fluttur inn

Hægt er að flytja einingahóp inn í fyrirliggjandi einingahóp eða stofna nýjan einingahóp fyrir gögnin. Allir einingahópar sem fluttir eru inn halda upprunalegum leturstíl sínum sem og tilvísunum í fyrirtæki og taka með sér viðeigandi víddasamstæður.
1.  Á valmyndinni **Fyrirtæki** í Skýrsluhönnun er smellt á **Einingarhópar**.
2.  Í svarglugganum **Einingarhópar** er valin eining sem á að flytja einingahóp í og síðan er smellt á **Flytja inn**.
3.  Í svarglugganum **Opna** er valinn einingahópurinn sem á að flytja inn og síðan er smellt á **Opna**.
4.  Smellið á skýrsluskilgreiningarnar í svarglugganum **Flytja inn** til að flytja inn:
    -   Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    -   Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.

5.  Smellið á **Flytja inn** þegar búið er að velja atriði til að flytja inn.

### <a name="undo-a-checkout-of-a-building-block"></a>Útskráning einingar afturkölluð

Þegar eining er opnuð geta aðrir notendur aðeins fengið lesaðgang að þeirri einingu. Stundum gleymir notandi að loka einingu eða slekkur á kerfinu án þess að loka einingunni. Af því leiðir að einingin er útskráð og engir notendur geta opnað hana. Við þessar aðstæður getur stjórnandi fjárhagsskýrslna notað svargluggann **Útskráð atriði** til að skrá inn einingar sem einhver notandi hefur skilið eftir í útskráðri stöðu. **Athugasemd:** Aðeins stjórnandi getur skráð inn einingar í svarglugganum **Útskráð atriði**.
1.  Á valmyndinni **Verkfæri** í Skýrsluhönnun er smellt á **Útskráð atriði**.
2.  Veljið **Sýna vörur frá öllum notendum** í svarglugganum **Útskráð atriði**. Listinn uppfærist og sýnir allar einingar sem hafa verið skráðar út og hvaða notendur það voru sem skráðu þær út.
3.  Veljið einingu og smellið síðan á **Afturkalla útskráningu**.
4.  Smellið á **Já** til að skrá inn eininguna.

# <a name="see-also"></a>Sjá einnig

[Fjárhagsskýrslugerð](financial-reporting-intro.md)



