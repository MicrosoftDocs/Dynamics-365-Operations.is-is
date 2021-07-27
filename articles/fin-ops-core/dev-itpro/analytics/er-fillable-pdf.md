---
title: Hanna skilgreiningar rafrænnar skýrslugerðar til að fylla inn í PDF-sniðmát
description: Þetta efnisatriði veitir upplýsingar um hvernig á að hanna snið rafrænnar skýrslugerðar til að fylla út PDF-sniðmát.
author: NickSelin
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 63994a4583e27b0197b9fc42c622f6c0e42c84ee
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355419"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a>Hanna skilgreiningar rafrænnar skýrslugerðar til að fylla inn í PDF-sniðmát

[!include[banner](../includes/banner.md)]

Ferlin í þessu efnisatriði eru dæmi sem sýna hvernig notandi í annaðhvort hlutverkinu **Kerfisstjóri** eða **Þróunaraðili rafrænnar skýrslugerðar** getur skilgreint snið rafrænnar skýrslugerðar sem býr til skýrslur sem PDF-skrár með því að nota útfyllanleg PDF-skjöl sem skýrslusniðmát. Hægt er að framkvæma þessi skref í hvaða fyrirtæki af Dynamics 365 Finance eða regluskilgreiningarþjónustu.

## <a name="prerequisites"></a>Forkröfur

Áður en hafist er handa verður einn af eftirfarandi aðgangsgerðum að vera fyrir hendi, háð þjónustunni sem er notuð til að ljúka ferlunum í þessu efnisatriði:

- Aðgangur að Finance fyrir eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgangi RCS fyrir eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

Einnig þarf að ljúka ferlinu [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

Að lokum skal hlaða niður eftirfarandi skrám.

| Lýsing á efni                       | Skrárnafn                                     |
|-------------------------------------------|-----------------------------------------------|
| Sniðmát fyrir fyrstu síðu skýrslunnar | [IntrastatReportTemplate1.pdf](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| Sniðmát fyrir aðrar síður skýrslunnar    | [IntrastatReportTemplate2.pdf](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| Sýnishorn af sniði rafrænnar skýrslugerðar - PDF                          | [Intrastat-skýrsla (PDF).útgáfa.1.1.xlm](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| Sýnishorn af sniði rafrænnar skýrslugerðar - Excel                          | [Intrastat (innflutt úr Excel).útgáfa.1.1.xml](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| Sýnishorn af gagnasafni                            | [Sýnishorn af intrastat-gögnum.xlsx](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a>Hanna skilgreiningu sniðs

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir

1. Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.
2. Gakktu úr skugga um að **Litware, Inc.** sé tiltækur og merkt sem virk.
3. Í reitnum fyrir þjónustuveitu **Microsoft** skal velja **Geymslur**.

    > [!NOTE]
    > Ef geymsla af gerðinni **LCS** er þegar til skal sleppa eftirstandandi skrefum í þessu ferli.

4. Veljið **Bæta við**.
5. Í fellilista svarglugga, í reitahópnum **Gerð skilgreiningageymslu**, skal velja valkostinn **LCS**.
6. Veljið **Stofna geymslu**.
7. Veljið **Í lagi**.

### <a name="get-the-model-configurations-provided-by-microsoft"></a>Sækja skilgreiningar líkana sem Microsoft útvegar

1. Vinsta megin á síðunni **Skilgreiningageymslur** skal velja hnappinn **Sýna síur** (trektartáknið).
2. Bætið við síu fyrir gildi af **LCS** í reitnum **Gerð** og notið virknitáknið **byrjar á**.
3. Veljið **Bæta við**.
4. Veljið **Opna**.
5. Í trénu skal velja **Intrastat-líkan**.
6. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1**.

    > [!NOTE]
    > Ef hnappurinn **Flytja inn** í flýtiflipanum **Útgáfur** er ekki tiltækur skal sleppa skrefunum sem eftir eru í þessu ferli.

7. Velja **Innflutningur**.
8. Veljið **Já** til að staðfesta innflutning á valdri útgáfu af skilgreiningalíkaninu **Intrastat-líkan**.

### <a name="create-a-new-format-configuration"></a>Stofna nýja skilgreiningu á sniði

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.
2. Í trénu skal velja **Intrastat-líkan**.
3. Veljið **Stofna skilgreiningu**.

    > [!NOTE]
    > Ef hnappurinn **Stofna skilgreiningu** er ekki tiltækur þarf að kveikja á hönnunarstillingu á síðunni **Færibreytur rafrænnar skýrslugerðar** sem hægt er að opna úr vinnusvæðinu **Rafræn skýrslugerð**.

4. Í fellilista svarglugga, í reitahópnum **Nýr**, skal velja valkostinn **Snið byggir á Intrastat-gagnalíkani**.
5. Í reitnum **Heiti** skal færa inn **Intrastat-skýrsla (PDF)**.
6. Í reitinn **Lýsing** skal færa inn **Intrastat-skýrsla á PDF-sniði**.

    > [!NOTE]
    > Virkt skilgreiningarveitu er sjálfkrafa færð inn. Þessa veitu mun geta unnið með þessa skilgreiningu. Þótt aðrar þjónustuveitur geti notað þessa skilgreiningu geta þeir ekki unnið með hana.

7. Valfrjálst: Í reitnum **Gerð sniðs** er hægt að velja tiltekið snið rafræns skjals. Ef valið er **PDF**, á hönnunartíma, mun hönnuður ER Operations eingöngu bjóða upp á sniðseiningar sem eiga eingöngu við um skjöl sem eru mynduð á PDF-sniði (**PDF\Skrá**, **PDF\PDF Merger**, o.s.frv.). Ef þessi reitur er skilinn eftir auður verða snið rafræns skjals tilgreint á hönnunartíma í hönnuði ER Operations þegar fyrstu sniðseiningu er bætt við. Ef til að mynda **Excel/Skrá** er bætt við sem fyrstu sniðseiningu mun hönnuður ER Operations eingögnu bjóða upp á sniðseiningarnar sem eiga eingöngu við skjöl sem eru mynduð á Excel-sniði (**Excel\Hólf**, **Excel\Bil**, o.s.frv.). snið.
8. Veljið **Stofna skilgreiningu**.

Nýtt snið rafrænnar skýrslugerðar er stofnað. Hægt er að nota útgáfudrög þessarar skilgreiningar til að geyma sniðshluta rafrænnar skýrslugerðar sem er hannaður til að mynda rafræn skjöl á PDF-sniði.

### <a name="design-the-format-of-an-electronic-document"></a>Hannið snið fyrir rafrænt skjal

Næst, í skilgreiningu á sniði rafrænnar skýrslugerðar sem var stofnað, þarf að hanna snið rafrænnar skýrslugerðar sem myndar skýrsluna **Intrastat-stýring** á PDF-sniði. Fyrsta síða þessarar skýrslu verður að sýna samantekt skýrslunnar og upplýsingar um færslur erlendra viðskipta sem gefin er skýrsla um. Hinar síðurnar verða að sýna eingöngu upplýsingar um færslur erlendra viðskipta sem gefin er skýrsla um. Vegna þess að síður skýrslunnar sem eru búnar til verða að vera með mismunandi útlit, tvö mismunandi sniðmát á PDF-sniði verða notuð í sniði rafrænnar skýrslugerðar.

Í hvaða PDF-lesara sem er skal opna PDF-sniðmátin sem voru sótt. Athugið að hvert sniðmát inniheldur marga reiti sem verður að fylla út. Í hverju sniðmáti eru upplýsingar um færslur erlendra viðskipta birtar sem 42 línum, sem hver hefur níu reiti. Línunúmerið birtist við endann á öllum reitarheitum (t.d. **Dagsetning 1**...**Dagsetning 42** og **Vara 1**...**Vara 42**).

Eftirfarandi skýringarmynd sýnir PDF-sniðmátið fyrir fyrstu síðu skýrslunnar.

![Sniðmát 1.](media/rcs-ger-filloutpdf-template1.png)

Eftirfarandi skýringarmynd sýnir PDF-sniðmátið fyrir aðrar síður skýrslunnar.

![Sniðmát 2.](media/rcs-ger-filloutpdf-template2.png)

1. Á síðunni **Skilgreiningar** skal velja **Hönnuður**.
2. Veljið **Bæta við rót**.
3. Í fellilista svarglugga, í trénu, skal velja **PDF \> PDF Merger**.

    Þegar einingin **PDF Merger** er valin sem rótareining sniðsins verða öll PDF-skjöl sem eru mynduð á keyrslutíma sameinuð í eitt lokaskjal í PDF. Ef eingöngu þarf eitt PDF-sniðmát til að búa til öll nauðsynleg skjöl með því að nota snið rafrænnar skýrslugerðar sem er hannað, er hægt að velja **PDF-skrá** sem rótareininguna.

4. Í reitinn **Heiti** skal færa inn **Frálag**.
5. Í reitnum **Tungumálastillingar** skal velja **Kjörstilling notanda**. Skýrslan verður búin til á kjörtungumáli notandans sem keyrir hana.
6. Í reitnum **Kjörstillingar menningar** skal velja **Kjörstilling notanda**. Gildi og dagsetningar sem koma fram á síðum skýrslunnar verða á sniði samkvæmt kjörstaðsetningu notandans sem keyrir skýrsluna.
7. Veljið **Í lagi**.
8. Í aðgerðarúðunni, í flipanum **Flytja inn**, skal velja **Flytja inn úr PDF**.

    Þegar útfyllanlegt PDF-skjal er flutt inn sem sniðmát fyrir þetta snið rafrænnar skýrslugerðar eru allar nauðsynlegar sniðseiningar rafrænnar skýrslugerðar (einingarnar **PDF-skrá**, **Reitahópur** og **Reitur**) búnar til sjálfkrafa í sniðinu sem er hannað samkvæmt skipulagi PDF-skjalsins sem er flutt inn.

9. Veljið **Fletta**. Flettið og veljið skrána **IntrastatReportTemplate1.pdf** sem var sótt áður sem forsenda.
10. Veljið **Í lagi**.

    Valdri skrá er hlaðið inn og reiturinn **Sniðmát** í svarglugganum **Flytja inn úr PDF** er fylltur út.

11. Stillið valkostinn **Reitahópar** á **Já**. Ef valið PDF-skjal inniheldur einhverja reitahópur verða þeir notaðir til að flokka sniðseiningar rafrænnar skýrslugerðar sem eru búnar til. **Reitarhópur** sniðseining verður búin til í þessum tilgangi.

    Ef þessi valkostur er stilltur á **Nei** verða nauðsynlegar sniðseiningar rafrænnar skýrslugerðar búnar til sem flatur listi yfir einingar sem eru faldaðar undir sniðseiningunni **PDF-skrá** sem er búin til.

12. Veldu **Í lagi**.

    ![Flytja inn úr svarglugga PDF.](media/rcs-ger-filloutpdf-importtemplate.png)

13. Í trénu skal víkka út **Frálag**.

    Takið eftir að hlutinn **PDF-skrá** hefur verið búinn til sjálfkrafa til að stjórna stofnun á fyrstu síðu skýrslunnar sem er mynduð á keyrslutíma.

14. Í trénu skal víkka út **Frálag \> PDF-skrá**.

    Takið eftir að skipulagður listi yfir sniðseiningar hefur verið búinn til sjálfkrafa í þessu sniði rafrænnar skýrslugerðar samkvæmt skipulagi á útfyllanlegu PDF-skjali sem var flutt inn áður.

15. Í trénu skal velja **Frálag \> PDF-skrá**.
16. Í reitinn **Heiti** skal færa inn **Síða 1**.

    Þessi sniðseining verður notuð til að búa til fyrstu síðu skýrslunnar **Intrastat-stýring**. Þessi síða sýnir samantekt skýrslunnar og upplýsingar um færslur erlendra viðskipta.

    Ef reiturinn **Tungumálastillingar** er skilinn eftir auður mun stillingin **Tungumálastillingar** í yfireiningunni **PDF Merger** ákvarða tungumál skýrslunnar sem er búin til með því að nota þessa sniðseiningu. Hægt er að velja annað gildi til að hnekkja stillingu yfireiningar.

    Ef reiturinn **Kjörstillingar menningar** er skilinn eftir auður mun stillingin **Kjörstillingar menningar** í yfireiningunni **PDF Merger** ákvarða landsstaðal skýrslunnar sem er búin til með því að nota þessa sniðseiningu. Landsstaðallinn ákvarðar snið á gildum og dagsetningum á síðum skýrslunnar. Hægt er að velja annað gildi til að hnekkja stillingu yfireiningar.

17. Í aðgerðarúðunni skal velja flipann **Flytja inn**. Takið eftir að hnappurinn **Uppfæra úr PDF** er nú í boði fyrir valda sniðseiningu, **PDF-skrá**.

    Þú getur notað þennan hnapp til að flytja inn uppfært PDF sniðmát í breytt snið. Þegar uppfærða PDF-sniðmátið er flutt inn verður lista yfir sniðseiningar breytt í samræmi:

    - Fyrir alla nýja reiti í uppfærða PDF-sniðmátinu eru nýjar sniðseiningar búnar til í breyttu sniði rafrænnar skýrslugerðar.
    - Ef uppfærða PDF-sniðmátið inniheldur ekki lengur reiti sem samsvara einhverjum fyrirliggjandi sniðseiningum í breyttu sniði rafrænnar skýrslugerðar, er þessum sniðseiningum eytt úr sniði rafrænnar skýrslugerðar.

18. Í flipanum **Snið** skal velja **Viðhengi**.

    Takið eftir því að innflutta PDF-skjalið er hengt við breytt snið rafrænnar skýrslugerðar.

    ![Forskoðun PDF-viðhengis.](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. Haldið áfram að hanna þetta snið með því að flytja inn næsta PDF-sniðmát, bæta við nauðsynlegum bindingum við gagnagjafa og svo framvegis.
20. Veljið **Vista**.
21. Lokið síðunni.
22. Veljið **Eyða**.
23. Velja skal **Já**.

Til að fá frekari upplýsingar um **PDF Merger**, **PDF-skrá**, **Reitarhópur** og **Reitur** er hægt að nota sniðseiningar til að búa til skjöl á PDF-sniði, hægt er að flytja inn og greina sýnishorn af sniði rafrænnar skýrslugerðar.

### <a name="import-the-format-configuration"></a>Flytja inn skilgreiningu sniðs

Næst skal flytja inn sýnishornið af sniði rafrænnar skýrslugerðar sem var sótt áður til að búa til skýrsluna **Intrastat-stýring** á PDF-sniði. Fyrsta síða skýrslunnar verður að sýna samantekt skýrslunnar og upplýsingar um færslur erlendra viðskipta sem gefin er skýrsla um. Hinar síðurnar verða að sýna eingöngu upplýsingar um færslur erlendra viðskipta sem gefin er skýrsla um.

1. Á síðunni **Skilgreiningar** skal velja **Skipta út \> Hlaða úr XML-skrá**.
2. Veljið **Fletta**. Flettið að og veljið skrána **Intrastat-skýrsla (PDF).útgáfa.1.1.xlm** sem var sótt áður sem forsenda.
3. Veljið **Í lagi**.

## <a name="analyze-the-format-configuration"></a>Greina skilgreiningu sniðs

### <a name="format-layout"></a>Útlit sniðs

1. Á síðunni **Skilgreiningar**, í trénu, skal velja **Intrastat-líkan \> Intrastat-skýrsla (PDF)**.
2. Veljið **Hönnuður**.
3. Veljið **Sýna upplýsingar**.
4. Í trénu skal víkka út **Frálag: PDF Merger**.

    Takið eftir að þetta snið rafrænnar skýrslugerðar inniheldur tvær einingar af **PDF-skrá**, sem hver um sig notar mismunandi PDF-sniðmát. Eitt sniðmátið er nota til að búa til fyrstu síðu skýrslunnar á PDF-sniði og hitt sniðmátið er notað til að búa til hinar síðurnar.

5. Í trénu skal víkka út **Frálag: PDF Merger \> Síða 1: PDF-skrá (IntrastatReportTemplate1)**.
6. Í trénu skal víkka út **Frálag: PDF Merger \> Síða N: PDF-skrá (IntrastatReportTemplate2)**.

    Athugið að innihald PDF-sniðmátanna tveggja er ólíkt, sem gerir að verkum að skipan faldaðra sniðseininga fyrir tvær einingarnar **PDF-skrá** er einnig ólík.

### <a name="format-mapping"></a>Sniðsvörpun

1. Á síðunni **Sniðshönnuður** skal velja flipann **Vörpun**.
2. Í trénu skal víkka út **Síðuvíxl \> Síður**.

    ![Síða formúluhönnuðar þar sem líkanstré er víkkað út.](media/rcs-ger-filloutpdf-reviewformat.png)

    Athugið eftirfarandi upplýsingar:

    - Sniðseiningin **Frálag \> Síða 1** af gerðinni **PDF-skrá** er ekki bundin neinum gagnagjafa og segðin **Virkjað** fyrir þessa sniðseiningu er tóm. Þar af leiðandi, við keyrslutíma, verður PDF-sniðmátið **IntrastatReportTemplate1** fyllt út aðeins einu sinni þegar stakt PDF-skjal er búið til.
    - Sniðseiningin **Frálag \> Síða N** af gerðinni **PDF-skrá** er bundin gagnagjafanum **Paging.PageN** af gerðinni **Færslulisti** og segðin **Virkjað** fyrir þessa sniðseiningu er tóm. Þar af leiðandi, við keyrslutíma, verður PDF-sniðmátið **IntrastatReportTemplate2** fyllt út fyrir hverja færslu af færslulistanum þegar stakt PDF-skjal er búið til.
    - Vegna þess að sniðseiningarnar **Síða 1: PDF-skrá** og **Síða N: PDF-skrá** eru undireiningar sniðseiningarinnar **Frálag: PDF Merger**, eru öll útfyllt PDF-skjöl sameinuð í eitt lokaskjal á PDF-sniði.
    - Gagnaveiturnar **Paging.Page1** og **Paging.PageN** eru skilgreindar sem síur af færslum úr gagnaveitunni **Paging.Pages**. Þessi gagnaveita er skilgreind til að skipta öllu safninu af færslum erlendra viðskipta niður í runur. Hver runa inniheldur allt að 42 færslur. Eftirfarandi segð rafrænnar skýrslugerðar er notuð til að skipta færslunum niður í runur:

        SPLITLIST(Totals.CommodityRecord,42)

    - Gagnagjafinn **Paging.Pages** inniheldur eininguna **Paging.Pages.Enumerated** sem skilar upplýsingum um hverja færslu sem er hluti af runu. Þessar upplýsingar innihalda röð færslunnar í núverandi runu (reiturinn **Paging.Pages.Enumerated.Number**). Reiturinn **Paging.Pages.Enumerated.Number** er notaður í segðinni **Heiti** fyrir sniðseiningarnar **PDF-skrá** til að gagnvirkt mynda heiti reits sem byggist á færslunúmeri í runu. Reitarheitið sem er búið til er síðan notað til að fylla út í réttan PDF-reit í PDF-sniðmátinu sem er notað.
    - Sniðseiningin **Frálag \> Síða N \> Upplýsingar 2** af gerðinni **PDF-flokkur** er bundin gagnagjafanum **Paging.PageN.Enumerated** (eða **\@.Enumerated** ef skoðunarstillingin **Afstæð slóð** er notuð) af gerðinni **Færslulisti**. Þar af leiðandi, við keyrslutíma, verða földuðu einingarnar í þessum PDF-flokki fylltar út fyrir hverja færslu úr bundna færslulistanum. Á þennan hátt eru stakar PDF-línur búnar til þegar fyrir hverja N-tu færslu af 42 færslum úr listanum **Paging.PageN.Enumerated** eru PDF-reitir fylltir út: Dagsetning N, Átt N, Vara N, o.s.frv. Þar af leiðir, hvað þetta varðar, svipar hegðun sniðseiningarinnar **Reitarhópur** til hegðunar á sniðseiningunum **XML \> Röð** og **Texti \> Röð**.

3. Í trénu skal víkka út **Frálag \> Síða N \> Upplýsingar2**.
4. Í trénu skal víkka út **Frálag \> Síða N \> Upplýsingar2 \> PageFooter**.

    Takið eftir að eigindin **Heiti** fyrir þessa sniðseiningu er skilgreind sem **PageFooter**. Takið einnig eftir að segðin **Heiti** fyrir sniðseininguna er tóm.

5. Í trénu skal víkka út **Frálag \> Síða N \> Upplýsingar2 \> Leiðrétting 1**.

    Takið eftir að eigindin **Heiti** fyrir þessa sniðseiningu er skilgreind sem **Leiðrétting 1**. Takið einnig eftir að segðin **Heiti** fyrir sniðseininguna er skilgreind sem **Paging.FldName(„Correction“,\@.Number)**.

![Sniðshönnuður þar sem vörpun er valin.](media/rcs-ger-filloutpdf-reviewformat2.png)

Takið eftir því að sniðseiningin **Reitur** er notuð til að fylla út stakan reit af útfyllanlegu PDF-skjali sem er skilgreint sem sniðmát af yfireiningu sniðseiningarinnar **PDF-skrá**. Binding sniðseiningarinnar **PDF-skrá** eða földuðum einingum hennar, ef hún er með faldaðar einingar, tilgreinir gildið sem er fært inn í samsvarandi PDF-reiti. Hægt er að nota mismunandi eiginleika sniðseiningarinnar **Reitur** til að tilgreina hvaða PDF-reit er fylltur út af stakri sniðseiningu:

- Í flipanum **Snið**, eigindin **Heiti** fyrir sniðseininguna
- Í flipanum **Vörpun**, segðin **Heiti** fyrir sniðseininguna

Vegna þess að báðir eiginleikarnir eru valkvæðir fyrir sniðseininguna **Reitur**, eru eftirfarandi reglur notaðar til að tilgreina PDF-markreit:

- Ef eigindin **Heiti** er tóm og segðin **Heiti** skilar auðum streng á keyrslutíma, er undantekningu beitt á keyrslutíma til að láta notanda vita að PDF-reiturinn finnst ekki í PDF-sniðmátinu sem er notað til að fylla út í PDF-skjalið.
- Ef eigindin **Heiti** er skilgreind og segðin **Heiti** er tóm, er PDF-reiturinn fylltur út sem er með sama heiti og eigindin **Heiti** fyrir sniðseininguna.
- Ef eigindin **Heiti** er skilgreind og segðin **Heiti** er skilgreind, er PDF-reiturinn fylltur út sem er með sama heiti og gildið sem segðin **Heiti** skilar fyrir sniðseininguna.

> [!NOTE]
> Hægt er að fylla út PDF-gátreit sem valinn á eftirfarandi hátt:
>
> - Þegar samsvarandi sniðseiningin **Reitur** er bundin við reit gagnagjafar af gagnagerðinni **Boolean** sem er með gildið **Satt**
> - Þegar samsvarandi sniðseiningin **Reitur** inniheldur faldaða sniðseiningu **Strengur** sem er bundin við reit gagnagjafa sem er með textagildi **1**, **Satt** eða **Já**

## <a name="run-the-format-configuration"></a>Keyra skilgreiningu sniðs

### <a name="import-the-format-configuration"></a>Flytja inn skilgreiningu sniðs

Næst verður hlaðið inn sýnishorninu **Intrastat (flutt inn úr Excel)** fyrir snið rafrænnar skýrslugerðar. Þetta snið er hannað til að þátta Microsoft Excel-vinnubók sem notandi valdi, sem líkir eftir færslum erlendra viðskipta.

1. Á síðunni **Skilgreiningar** skal velja **Skipta út \> Hlaða úr XML-skrá**.
2. Veljið **Fletta**. Flettið að og veljið skrána **Intrastat (innflutt úr Excel).útgáfa.1.1.xml** sem var sótt áður sem forsenda.
3. Veljið **Í lagi**.
4. Í trénu skal velja **Intrastat-líkan \> Intrastat (flutt inn úr Excel)**.
5. Veljið **Breyta**.
6. Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.

    > [!NOTE]
    > Ef valkosturinn **Sjálfgefið fyrir líkanavörpun** var áður stilltur á **Já** fyrir skilgreininguna **Intrastat-líkan** eða aðra skilgreiningu sem er földuð undir skilgreiningunni **Intrastat-líkan** skal stilla valkostinn á **Nei**.

    Þegar valkosturinn **Sjálfgefið fyrir líkanavörpun** er stilltur á **Já** er innflutta sniðið **Intrastat (flytja inn úr Excel)** fyrir rafræna skýrslugerð úthlutað sem sjálfgefinn gagnagjafi fyrir sniðsskilgreininguna **Intrastat-skýrsla (PDF)**. Síðan, þegar sniðsskilgreiningin **Intrastat-skýrsla (PDF)** er keyrð, mun innihald Excel-vinnubókar sem er þáttað af sniðinu **Intrastat (flutt inn úr Excel)** fyrir rafræna skýrslugerð líkja eftir færslum erlendra viðskipta sem þarf að gefa skýrslu um. Eftirfarandi skýringarmynd sýnir dæmi um Excel-vinnubók.

    ![Excel-vinnubók með sýnigögn.](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a>Keyra skilgreiningu sniðs

1. Á síðunni **Skilgreiningar**, í trénu, skal velja **Intrastat-líkan \> Intrastat-skýrsla (PDF)**.
2. Veljið **Keyra**.
3. Veljið **Fletta**. Flettið og veljið skrána **Intrastat sýnigögn.xlsx** sem var sótt áður sem forsenda.
4. Veljið **Í lagi**.
5. Í reitnum **Stefna skýrslu** skal velja **Báðar** til að fylla út allar færslur úr innfluttri Excel-vinnubók í PDF-skýrslunni sem var búin til.
6. Veljið **Í lagi**.
7. Yfirfarið PDF-skjalið sem er búið til.

Eftirfarandi skýringarmynd sýnir dæmi um fyrstu síðu skýrslunnar sem er búin til.

![Fyrsta síða myndaðrar skýrslu.](media/rcs-ger-filloutpdf-generatedreport.png)

Eftirfarandi skýringarmynd sýnir dæmi um aðra síðu skýrslunnar sem er búin til.

![Önnnur síða myndaðrar skýrslu.](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)](tasks/er-design-reports-openxml-2016-11.md)
- [Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
