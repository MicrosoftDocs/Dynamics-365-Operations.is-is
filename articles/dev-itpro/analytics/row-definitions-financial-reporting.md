---
title: "Línuskilgreiningar í fjárhagsskýrsluhönnuði"
description: "Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu. Línuskilgreiningu er hægt að sameina með dálkaskilgreiningum, skipuritsskilgreiningum og skýrsluskilgreiningum til að stofna einingahóp sem mörg fyrirtæki geta notað."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 06a75889e62cbba6e47a8543cf663868df5ae2e3
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="row-definitions-in-financial-report-designer"></a>Línuskilgreiningar í fjárhagsskýrsluhönnuði

[!include[banner](../includes/banner.md)]


Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu. Línuskilgreiningu er hægt að sameina með dálkaskilgreiningum, skipuritsskilgreiningum og skýrsluskilgreiningum til að stofna einingahóp sem mörg fyrirtæki geta notað.

<a name="create-a-row-definition"></a>Línuskilgreining stofnuð
-----------------------

1.  Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.
2.  Á **Skrá** smellið á **Nýtt** og síðan **Línuskilgreining**. Frekari upplýsingar um innihald hvers hólfs eru í [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Línuskilgreining opnuð
1.  Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.
2.  Tvísmellið á heiti línuskilgreiningarinnar sem á að opna.
3.  Hægrismellið á línuskilgreiningu og veljið **Tengingar** til að skoða allar einingar sem tengjast línuskilgreiningunni.

## <a name="contents-of-a-row-definition"></a>Innihald línuskilgreiningar
Línuskilgreining getur innihaldið allt að 20.000 fjárhagsvíddaarlínur og haft eftirfarandi upplýsingar:

-   Lýsandi texti sem bætir merkingu við skýrsluna með því að stofna hlutafyrirsagnir, línur og bil, s.s. **Reiðufé** eða **Heildartekjur**
-   Tenglar í fjárhagsgögn, sem geta innihaldið víddargildi í Microsoft Dynamics 365 for Finance and Operations **Athugið:** Það er hægt að setja upp línuskilgreiningar til að sækja gögn úr fjárhagsvíddakerfinu í hvert skipti sem skýrslan er mynduð.
-   Samtölur línu og formúlur eru byggð á tengdum fjárhagsgögnum

Yfirleitt inniheldur hver lína í línuskilgreiningu eina af eftirfarandi tegundum upplýsinga:

-   Tilvísanir í fjárhagsvíddarkerfinu
-   Samtölur eða útreikningar sem byggjast á gögnunum
-   Sníða

Tvær leiðir eru til að slá inn upplýsingar í línuskilgreiningu:

-   Færa handvirkt inn upplýsingar um línu í nýju línuskilgreiningunni. Frekari upplýsingar sjá [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).
-   Nota Report Designer til að sækja línuupplýsingar beint úr fjárhagsvíddum. Nánari upplýsingar er að finna í hlutanum "Tengdar línur/formúlur/einingar" í [Breyta reitum skilgreiningar línu](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Víddum bætt við línuskilgreiningu
Vídd er skurðpunktur gagna og gilda. Hægt er að taka saman gögn og gildi í Report Designer. Svo er hægt að flokka og greina færslur nánar. Hægt er að nota svargluggann **Setja inn línur úr víddum** til að bæta mörgum línuskilgreiningum við samtímis. Svarglugginn birtir einn dálk fyrir hverja vídd. Eftirfarandi tafla lýsir upplýsingunum sem hægt er að tilgreina fyrir hverja vídd.

| Valkostur                | Lýsing                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vídd             | Mynstrið sem auðkennir víddina sem bæta á við línuskilgreininguna. Þetta mynstur inniheldur eitt og-merki (&) eða númeratákn (\#) fyrir hverja stöðu í víddunum. Almennt skal nota allar gæsalappir fyrir víddir aðallykils og öll tákn fyrir aðrar víddir. |
| Upphaf víddasviðs | Fyrsta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.                                                                                                                                                                                                                 |
| Lok víddasviðs   | Síðasta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.                                                                                                                                                                                                                  |

Til að bæta víddum við línuskilgreiningu skal fylgja eftirfarandi skrefum.

1.  Report Designer smellt **Línuskilgreiningar**, og opnið síðan línuskilgreiningu til að breyta.
2.  Á valmyndinni **Breyta** er smellt á **Setja inn línur úr víddum**.
3.  Í **Setja inn Línur úr Víddir** í svarglugganum, í **Víddir** línunni skal velja hólfið fyrir víddina sem á að flytja í línuskilgreininguna og smella síðan á **Öll &&&**.
4.  Til að takmarka línuskilgreiningar við ákveðin víddargildi skal slá inn upphafsvíddargildi í **Upphafs víddarsviðs** reitinn og slá svo inn lokavíddargildið í **Lok víddarsviðs** reitinn. Til að hafa öll gildi fyrir valda vídd, skiljið þessum reitum eftir auður. **Athugið:** Algildisstafir (\* eða?) í víddarsviðum skila ekki endilega öllum niðurstöðum sem óskað er, eftir því hvernig ERP gagnagrunnurinn safnar gögnum.
5.  Í **Kóði upphafslínu** svæðið skal tilgreina línukóða fyrir fyrsta víddargildi sem á að bæta við línuskilgreiningu.
6.  Í **Auka stig hverrar línu með** svæðið skal tilgreina bilið á milli samfelldra línukóða. Til dæmis, ef kóði fyrstu línu er 100 og stigvaxandi gildi er 30, hafa fyrstu nýju línurnar kóðana 100 130, 160, 190 og 220. Notið stigvaxandi gildi sem veitir nægt bil fyrir innsetningu nýs sniðs og formúlulínur.
7.  Smelltu á **Í lagi**. Einni línu er bætt við línuskilgreininguna fyrir hvert valið víddargildi.

## <a name="adjust-rounding-in-a-row-definition"></a>Sléttun stillt í línuskilgreiningu
Fyrir efnahagsreikninga þar sem upphæðir eru sléttaðar er ekki víst að samtölur stemmi. Þetta getur t.d. átt sér stað þegar sléttunarvalkosturinn er notaður efnahagsreikningsskýrslu og skýrsluskilgreining tilgreinir einnig sléttun. Hægt er að nota **Sléttunarleiðrétting** valkostinn í línuskilgreiningu til að leiðrétta upphæðir í efnahagsreikningnum. Hægt er að slökkva á sléttun eða breyta henni í flipanum **Stillingar** í skýrsluskilgreiningunni. Eftirfarandi tafla sýnir hvernig upphæðirnar eru sléttaðar. Í þessari töflu eru samtölur línanna 100 og 200 mismunandi þegar kveikt er á sléttun.

| Línukóði | Upphæðir án sléttunar | Upphæð með sléttun að heilum þúsundum |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Samtals    | 7,300                    | 8                                       |

Til að leiðrétta sléttun í efnahagsreikningi skal fylgja eftirfarandi skrefum.

1.  Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.
2.  Á valmyndinni **Breyta** er smellt á **Sléttunarleiðrétting**.
3.  Í svarglugganum **Sléttunarleiðréttingar** eru eftirfarandi gildi færð inn:
    -   **Sléttunarleiðréttingarlína** – Línukóðinn fyrir línuna sem ætti að leiðrétta til að jafna efnahagsreikninginn.
    -   **Samtölulína eigna** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur heildareignir.
    -   **Samtölulína skulda og eigin fjár** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur skuldir og eigið fé samtals.
    -   **Takmörk leiðréttingarupphæðar** – Jákvæð, heiltala sem tilgreinir takmörkun sjálfvirkrar leiðréttingar. Þessi upphæð er borin saman við raungildi raunverulegs sléttunarmismunar.

    **Ábending:** Tengja verður þessa línukóða við fjárhagsgögn notanda. Með öðrum orðum, línan verður að hafa víddargildi í hólfinu **Tengill í fjárhagsvíddir**. **Ekki** vísa til lýsingar (**DESC**), reiknaðrar (**CALC**), eða samtölulínu (**TOT**).

Upphæðir í efnahagsreikningi verða nú jafnaðar jafnt þegar kveikt er á sléttun. **Ábending:** Takmörkun leiðréttingar er beitt út frá valkostinum **Sléttunarnákvæmni** sem er tilgreindur fyrir skýrsluskilgreininguna. Til dæmis, ef að slétta á skýrsluna í þúsundum og færa inn **2** í **Takmörk leiðréttingarupphæðar** reitnum birtist viðvörun þegar gildið í **Sléttunarleiðréttingarlína** reitnum hækkar eða lækkar um meira en 2.000.

## <a name="format-row-and-column-text"></a>Lína og dálktexti sniðin
Breyta má útliti skýrslna með því að breyta leturgerðum og sníða texta. Eftirfarandi hlutar útskýra hvernig á að sníða útliti lína og dálka í skýrslum.

### <a name="manage-font-styles"></a>Vinna með leturstíla

Hægt er að stofna og breyta leturstílum fyrir skýrslu. Svo er hægt að nota þá stíla í skjalinu, eða á tiltekna röð eða dálki í skýrslu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Leturstíll stofnaður</td>
<td><ol>
<li>Á valmyndinni <strong>Snið </strong>í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</li>
<li>Í <strong>Stílar og snið</strong> svarglugganum skal smella á <strong>Nýtt</strong> og færa inn einkvæmt heiti fyrir nýja stílinn.</li>
<li>Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Leturstíl breytt</td>
<td><ol>
<li>Á valmyndinni <strong>Snið </strong>í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</li>
<li>Í <strong>Stílar og snið</strong> svarglugganum skal velja stíl sem á að breyta og smella svo á <strong>Breyta</strong>.</li>
<li>Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Leturstíll notaður</td>
<td><ol>
<li>Í Report Designer, í skilgreiningu eða dálkskilgreining eða í hausum og fótum, skal velja einn eða fleiri reit.</li>
<li>Í listanum <strong>Stíll</strong> á tækjastikunni er valinn leturstíll.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Snið texta í línum

Sniðið sem er tilgreint í línuskilgreiningunni hnekkir öllum sniðum sem eru tilgreind í dálkskilgreiningu og skýrsluskilgreiningu. Hægt er að breyta textasniðinu með því að nota stýringarnar á sniðstikunni. Stýringarnar eru hefðbundnar Microsoft Windows stýringar.

1.  Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2.  Veljið hólfin sem á að sníða. Til að velja fleiri en eitt hólf skal halda Ctrl-lyklinum niðri um leið og hólfin eru valin.
3.  Smellið á tækjastikuhnapp sniðsins sem á að nota. Til að draga t.d. inn línu skal velja línuna og smella á **Auka inndrátt** ![Auka inndrátt](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Auka inndrátt") á tækjastikunni.

### <a name="adjust-columns-while-you-design-reports"></a>Stilling dálka við hönnun skýrslna

Til að auðvelda að skoða dálka sem er unnið er með í línuskilgreiningu er hægt að stilla breidd dálks og fela (minnka) eða sýna dálka á skoðunarsvæðinu. Allar breytingar sem gerðar hafa aðeins áhrif á útliti dálkanna á skjánum. Þær hafa ekki áhrif á snið dálkanna í skýrslum.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Breidd dálks á skoðunarsvæði breytt

1.  Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2.  Á valmyndinni **Snið** skal velja **Dálkbreidd**.
3.  Í svarglugganum **Dálkbreidd** skal slá inn gildi og smella á **Í lagi**. Einnig er hægt að draga hægri brún hauss á dálkreit til að breyta breidd dálksins.

### <a name="hide-columns-in-the-view-pane"></a>Dálkar á skoðunarsvæði faldir

1.  Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2.  Veljið dálk eða dálka sem á að minnka.
3.  Þá er hægrismellt og smellt á **Fela**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Allir faldir dálkar sýndir á skoðunarsvæði

1.  Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.
2.  Hægrismellið á minnkaða dálkinn sem á að birta og smellið á **Sýna**.


<a name="see-also"></a>Sjá einnig
--------

[Fjárhagsskýrslugerð](financial-reporting-intro.md)




