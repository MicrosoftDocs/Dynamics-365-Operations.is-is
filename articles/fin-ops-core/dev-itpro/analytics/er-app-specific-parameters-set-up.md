---
title: Settu upp færibreytur ER sniðs á hvern lögaðila
description: Þetta efni útskýrir hvernig þú getur sett upp færibreytur í snið fyrir rafræna skýrslugerð (ER) á lögaðila.
author: NickSelin
ms.date: 10/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0fce566bea6340b4016e559b1f5f1764a6881e28
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675394"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Settu upp færibreytur ER sniðs á hvern lögaðila

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Forkröfur

Til að ljúka þessum skrefum þarf fyrst að ljúka skrefunum í [Grunnstilla ER-snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md).

Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa aðgang að Microsoft Dynamics 365 Finance fyrir eitt af eftirfarandi hlutverkum:

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

## <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar
Til að flytja inn stillingar rafrænnar skýrslugerðar skal fylgja þessum skrefum: 

1. Skráðu þig inn í umhverfið.
2. Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.
3. Veldu **Skilgreiningar skýrslugerðar**.
4. Í núverandi tilviki af Finance skal flytja inn skilgreiningarnar sem þú fluttir út úr Regulatory Configuration Services (RCS) þegar þú varst að ljúka skrefunum í [Grunnstilla ER-snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md). Fylgdu þessum skrefum fyrir hverja skilgreiningu [Rafrænnar skýrslugerðar](general-electronic-reporting.md) í eftirfarandi röð: gagnalíkan, líkanavörpun og snið.

    1. Veldu **Skipta út \> Hlaða úr XML-skrá**.
    2. Veljið **Vafra** til að velja skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.
    3. Veljið **Í lagi**.

    Eftirfarandi mynd sýnir stillingarnar sem þú verður að hafa þegar þú ert búin/n.

    ![Skilgreiningarsíða í ER.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Setja upp færibreytur fyrir fyrirtækið DEMF

Þú getur notað ER-rammana til að setja upp sértækar breytur fyrir forrit fyrir ER snið.

1. Velja skal lögaðilann **DEMF**.
2. Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
3. Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.

    ![Færibreytusíða fyrir forrit rafrænnar skýrslugerðar til að setja upp færibreytur.](./media/GER-AppSpecParms-LookupForm.PNG)

    Á síðunni **Forritsbundnar færibreytur** er hægt að stilla reglurnar fyrir gagnagjafann **Val** í sniðinu **Snið til að læra hvernig á að fletta upp LE-gögnum**.

    Ef grunn ER sniðið mun innihalda nokkra gagnagjafa af gerðinni **Uppfletting**, verður þú að velja viðeigandi gagnagjafa á flýtiflipanum **Uppflettingar** áður en þú getur byrjað að stilla reglumengi fyrir gagnagjafann.

    Fyrir hvern gagnagjafa er hægt að stilla aðskildar reglur fyrir hverja útgáfu af völdu ER sniði.

    Allt reglumengið fyrir alla uppflettigagnagjafa sem eru fáanlegir í valinni útgáfu af grunn-ER sniði samanstendur af forritssértæku færibreytunum fyrir ER sniðið.

4. Veldu útgáfu **1.1.1** á ER sniði.
5. Á flýtiflipanum **Skilyrði** velurðu **Bæta við**.
6. Í reitnum **Kóði** í nýju skránni velurðu fellilistaörina til að opna leitina.

    Uppflettan sýnir lista yfir skattakóða fyrir val. Þessum lista er skilað af gagnagjafanum **Model.Data.Tax** sem hefur verið stilltur á grunn ER sniði. Vegna þess að þessi gagnagjafi inniheldur reitinn **Heiti** birtist nafn sérhvers skattakóða í leitinni.

    ![Uppfletting kóðareits á færibreytusíðu fyrir forrit rafrænnar skýrslugerðar.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. Veldu skattakóðann **VAT19** tax code.
8. Í reitnum **Niðurstöður uppflettinar** í nýju skránni velurðu fellilistaörina til að opna leitina. Leitin sýnir lista yfir gildi fyrir TaxationLevel snið upptalningar fyrir val.

    Athugaðu að ef þú valdir þýsku sem kjörtungumál fyrir notandann sem þú ert skráð(ur) inn sem, verða merkingar gildanna í uppflettingunni á þýsku, að því gefnu að þær hafi verið þýddar í grunnsniði rafrænnar skýrslugerðar. Að auki, ef merkimiði uppflettingargagnaheimildar hefur verið þýddur mun sá merkimiði birtast á æskilegu tungumáli notandans á flipanum **Uppflettingar**.

    ![Uppflettireitur þýddur á þýsku á færibreytusíðu fyrir forrit rafrænnar skýrslugerðar.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. Veldu gildið **Regluleg skattlagning**.

    Með því að bæta þessari færslu við skilgreinir þú eftirfarandi reglu: Þegar send er beiðni á gagnagjafa **Uppflettivals** og skattkóðinn **VAT19** er notaður sem breyta verður **Reglulegri skattlagningu** skilað sem umbeðið skattlagningarstig.

10. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **InVAT19**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Regluleg skattlagning**.

11. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **VAT7**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Lægri skattlagning**.

12. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **InVAT7**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Lægri skattlagning**.

13. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **THIRD**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Engin skattlagning**.

14. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **InVAT0**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Engin skattlagning**.

15. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitinn **Kóði** velurðu valkostinn **\*Ekki autt\***.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Annað**.

    Með því að bæta þessari síðustu færslu við skilgreinir þú eftirfarandi reglu: Þegar skattkóðinn sem er sendur sem breyta fullnægir ekki neinum af fyrri reglum mun gagnagjafi uppflettingar skila **Annað** sem umbeðnu skattlagningarstigi.

    ![Síðasta færsla sem bætt var við færibreytusíðu fyrir forrit rafrænnar skýrslugerðar.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. Í reitnum **Staða** skal velja **Lokið**.

    Þegar þú keyrir ER snið útgáfu sem hefur annaðhvort stöðuna **Lokið** eða **Deilt** verður þetta reglumengi að vera með stöðuna **Lokið**. Annars verður framkvæmd grunn ER sniðsins rofin þegar sniðið reynir að hlaða gögnum úr þessu reglumengi þegar uppflettigagnagjafinn **Val** er keyrður.

    Þegar þú keyrir ER snið útgáfu sem hefur stöðuna **Drög** hefur grunn ER sniðið aðgang að þessu reglumengi, óháð stöðu þess.

17. Veljið **Vista**.
18. Lokaðu síðunni **Forritsbundnar færibreytur**.

## <a name="run-the-er-format-in-the-demf-company"></a>Keyra ER sniðið í DEMF fyrirtækinu
Til að keyra ER-sniðið í DEMF-fyrirtækinu skaltu fylgja þessum skrefum: 

1. Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
2. Í aðgerðarúðunni skal velja **Keyra**.
3. Í svarglugganum sem birtist skal smella á **Í lagi**.
4. Sæktu yfirlitið sem er búin til og geymdu hana á staðnum.

    Í yfirlitinu sem búið er til er tekið fram að samantekt skattkóðans **InVAT7** sé á stiginu **Minnkað** og samantektir skattkóðanna **VAT19** og **InVA19** séu á stiginu **Reglulegt**. Þessi hegðun ræðst af stillingum í reglum sem eru háðir lögaðilum.

5. Farðu í **Skattur \> Óbeinir skattar \> Virðisaukaskattur \> VSK-kóðar**.
6. Veldu skattakóðann **InVAT7**.
7. Á aðgerðarrúðunni, á flipanum **VSK-kóði**, í hópnum **Fyrirspurnir**, velurðu **Bókaður virðisaukaskattur** til að skoða upplýsingar um skatthlutfall og beitt skatthlutfall á hvern skattakóða.

    ![Síðan Bókaður virðisaukaskattur.](./media/GER-AppSpecParms-Statement.PNG)

8. Lokaðu síðunni **Bókaður virðisaukaskattur**.

## <a name="set-up-parameters-for-the-usmf-company"></a>Setja upp færibreytur fyrir fyrirtækið USMF
Til að setja upp færibreytur fyrir USMF-fyrirtækið skal ljúka eftirfarandi skrefum: 

1. Velja skal lögaðilann **USMF**.
2. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
3. Í stillingatrénu stækkarðu liðinn **Líkan til að læra færibreytur á köll**, stækkar liðinn **Snið til að læra færibreytur á köll** og velur sniðmátið **Snið til að læra hvernig á að fletta upp LE-gögnum**.
4. Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.
5. Veldu útgáfu **1.1.1** á völdu ER sniði.
6. Á flýtiflipanum **Skilyrði** velurðu **Bæta við**.
7. Í reitnum **Kóði** í nýju skránni velurðu fellilistaörina til að opna leitina.

    Núna sýnir uppflettingin lista yfir skattakóða fyrir **USMF** fyrirtækjaskatt fyrir val.

    ![Skattkóðar fyrir skatt USMF-fyrirtækisins.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. Veldu skattakóðann **EXEMPT**.
9. Í reitnum **Niðurstaða uppflettingar** í nýju skránni velurðu gildið **Engin skattlagning**.
10. Veljið **Bæta við**.
11. Í reitnum **Kóði** í nýju skránni velurðu valkostinn **\*Ekki autt\***.
12. Í reitnum **Niðurstaða uppflettingar** í nýju skránni velurðu gildið **Regluleg skattlagning**.
13. Í reitnum **Staða** skal velja **Lokið**.
14. Veldu **Vista**.

    ![Síða sértækra færibreyta fyrir ER-forrit.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. Lokaðu síðunni **Forritsbundnar færibreytur**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Keyra ER sniðið í USMF fyrirtækinu
Til að keyra ER-sniðið í USMF-fyrirtækinu skal ljúka eftirfarandi skrefum:

1. Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
2. Í aðgerðarúðunni skal velja **Keyra**.
3. Í svarglugganum sem birtist skal smella á **Í lagi**.
4. Sæktu yfirlitið sem er búin til og geymdu hana á staðnum.

    Taktu eftir því í tilkynningunni að þú hefur nú notað sama ER snið fyrir annan lögaðila en án þess að gera neinar breytingar á ER sniði.

## <a name="reuse-legal-entitydependent-parameters"></a>Endurnýta færibreytur sem eru háðir lögaðilum

### <a name="duplicate-existing-parameters"></a>Afrita fyrirliggjandi færibreytur

#### <a name="export-parameters"></a>Útflutningsfæribreytur
Til að flytja út færibreytur skal ljúka eftirfarandi skrefum:

1. Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
4. Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.
5. Veldu útgáfu **1.1.1** á ER sniði.
6. Á Aðgerðasvæðinu skal velja **Flytja út**.
7. Sæktu skrána sem er búin til og geymdu hana á staðnum.

    Nú er búið að flytja út stillt mengi af forritasértækum breytum sem XML skrá.

#### <a name="import-parameters"></a>Innflutningsfæribreytur
Til að flytja inn færibreytur skal ljúka eftirfarandi skrefum:

1. Veldu útgáfu **1.1.2** á ER sniði.
2. Á Aðgerðasvæðinu skal velja **Flytja inn**.
3. Veldu **Já** til að staðfesta að þú viljir hnekkja gildandi forritsbreytum fyrir þessa sniðútgáfu.
4. Veldu **Fletta** til að finna skrána sem hefur að geyma útfluttar forritsbundnar færibreytur fyrir útgáfu **1.1.1**.
5. Veljið **Í lagi**.

    Útgáfa **1.1.2** af ER sniði hefur nú sömu forritssértæku færibreytur og þú stilltir upphaflega fyrir útgáfu **1.1.1**.

##### <a name="applicability-considerations"></a>Önnur atriði varðandi gildissvið

Færibreytur forritsins fyrir ER-snið eru háðar lögaðila. Til að endurnýta færibreytur forritsins sem voru skilgreindar fyrir einn lögaðila í öðrum lögaðila þarf að flytja þær út á meðan þú ert skráð(ur) inn í fyrri lögaðilanum. Flyttu þær síðan inn eftir að þú hefur skráð þig inn hjá hinum lögaðilanum.

Einnig er hægt að nota þessa útflutnings-innflutningsaðferð til að flytja forritsfæribreytur ER-sniðs sem voru upprunalega skilgreindar í einu tilviki af Finance í annað tilvik af Finance.

Ef þú stillir færibreytur tiltekins forrits fyrir eina útgáfu af ER-sniði og flytur síðan inn nýrri útgáfu af sama sniðinu í núverandi Finance-tilvik verða fyrirliggjandi færibreytur tiltekins forrits ekki notaður í innfluttu útgáfunni nema þú notir eiginleikann **Nota sértækar færibreytur fyrir forrit úr fyrri útgáfum sniða rafrænnar skýrslugerðar**. Nánari upplýsingar er að finna í hlutanum [Endurnota fyrirliggjandi færibreytur](#reuse-existing-parameters) síðar í þessu efnisatriði.

Þegar þú velur skrá til að flytja inn er skipulag færibreyta tiltekins forrits í þeirri skrá borið saman við skipulag samsvarandi gagnagjafa af gerðinni **Uppfletting** í ER-sniðinu sem er valið fyrir innflutning. Innflutningi er sjálfgefið aðeins lokið ef skipulag allra færibreyta tiltekins forrits passar við skipulag samsvarandi gagnagjafa í ER-sniðinu sem er valið fyrir innflutning. Ef skipulagið passar ekki saman koma upp viðvörunarboð sem gefa til kynna að ekki sé hægt að ljúka innflutningi. Ef þú þvingar innflutninginn hreinsast upp fyrirliggjandi færibreytur tiltekins forrits fyrir valið ER-snið og þú verður að setja þær upp frá grunni.

Frá og með Dynamics 365 Finance útgáfu 10.0.23 er hægt að breyta sjálfgefinni hegðun og koma í veg fyrir að fá viðvörunarboð með því að virkja eiginleikann **Stilla sértækar færibreytur fyrir forrit fyrir rafræna skýrslugerð við innflutning** á vinnusvæðinu **Eiginleikastjórnun**. Þegar þessi eiginleiki er virkjaður, ef skipulag færibreyta tiltekins forrits sem þú ert að flytja inn eru öðruvísi en skipulag samsvarandi gagnagjafa í ER-sniði markmiðs sem er valið fyrir innflutning mun innflutningurinn takast í eftirfarandi tilfellum:

- Búið er að breyta skipulagi á ER-sniði markmiðs með því að bæta nýjum skilyrðisdálkum við fyrirliggjandi gagnagjafa af gerðinni **Uppfletting**. Þegar innflutningi er lokið eru færibreytur tiltekins forrits uppfærðar. Í öllum innfluttum færslum af færibreytum tiltekins forrits eru gildin í öllum viðbættum skilyrðisdálkum frumstillt með sjálfgefnu gildi fyrir [gagnagerð](er-formula-supported-data-types-primitive.md) þess dálks.
- Búið er að breyta skipulagi á ER-sniði markmiðs með því að fjarlægja nokkra skilyrðisdálka úr fyrirliggjandi gagnagjöfum af gerðinni **Uppfletting**. Þegar innflutningi er lokið eru færibreytur tiltekins forrits uppfærðar. Í öllum innfluttum færslum af færibreytum tiltekins forrits er gildunum í öllum fjarlægðum skilyrðisdálkum eytt.
- Búið er að breyta skipulagi á ER-sniði markmiðs með því að bæta við nýjum gagnagjöfum af gerðinni **Uppfletting**. Þegar innflutningi er lokið er viðbættum uppflettingum bætt við færibreytur tiltekins forrits.
- Búið er að breyta skipulagi á ER-sniði markmiðs með því að fjarlægja nokkra fyrirliggjandi gagnagjafa af gerðinni **Uppfletting**. Þegar innflutningnum er lokið er öllum gervingum, sem tengjast gagnagjöfunum af gerðinni **Uppfletting** sem voru fjarlægðir úr ER-sniði markmiðs, eytt úr innfluttum færibreytum tiltekins forrits.

Þegar innflutningi er lokið, auk þeirra breytinga sem var verið að lýsa, er stöðu innfluttra færibreyta tiltekins forrits breytt í **Í vinnslu**. Viðvörunarboð gefa til kynna að breyta verður handvirkt sjálfkrafa leiðréttum færibreytum tiltekins forrits.

### <a name="reuse-existing-parameters"></a>Endurnýta fyrirliggjandi færibreytur

Frá og með Dynamics 365 Finance útgáfu 10.0.23 getur þú endurnotað færibreytur tiltekins forrits sem hafa verið skilgreindar fyrir eina útgáfu af ER-sniði þegar þú keyrir nýrri útgáfu af sama sniðinu. Til að gera þetta skal virkja eiginleikann **Nota sértækar færibreytur fyrir forrit úr fyrri útgáfum ER-sniða** á vinnusvæðinu **Eiginleikastjórnun**. Þegar þessi eiginleiki er virkjaður og þú keyrir eina útgáfu af ER-sniði sem reynir að lesa sértækar færibreytur forrits mun rafræn skýrslugerð reyna að finna sértækar færibreytur forrits sem hafa verið stilltar fyrir virka útgáfu af þessu sniði. Eða, þegar þær eru ekki tiltækar, fyrir næstu útgáfu fyrir neðan af þessu sniði.

> [!NOTE]
> Þú getur aðeins endurnotað sértækar færibreytur forrits innan núverandi lögaðila.
>
> Villa birtist á keyrslutíma þegar keyrð er nýrri útgáfa af ER-sniði þar sem reynt er að endurnýta sértækar færibreytur forritsins sem hafa verið stilltar fyrir eldri útgáfu af sama sniði og skipulagi að minnsta kosti eins gagnagjafa af gerðinni **Uppfletting** í nýrri útgáfu sniðs hefur verið breytt.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Samband á milli forritasértækra færibreytna og ER sniðs

Sambandi á milli ER sniðs og forritasértækum færibreyta þess er komið á með tilvikaóháðu sértæku auðkennisnúmeri ER sniðsins. Þess vegna, þegar þú fjarlægir ER snið úr Finance, eru forritasértæku færibreyturnar sem eru stilltar fyrir ER sniðið geymdar í núverandi tilviki Finance. Hægt er að nálgast þær þegar grunnsnið rafrænnar skýrslugerðar er endurinnflutt í þetta tilvik af Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Fáðu aðgang að forritasértækum færibreytum með því að nota ER ramma

Í dæminu á undan hefur þú fengið aðgang að forritasértækum færibreytum á ER sniði með því að nota ER ramma. Þessi aðferð gerir þér ekki kleift að takmarka aðgang að forritasértækum breytum á tilteknu ER sniði. Fylgdu þessum skrefum ef þú verður að beita slíkum takmörkunum. 

1. Annaðhvort endurnýtirðu núverandi valmyndaratriðið **ERSolutionAppSpecificParametersDesigner** eða útfærir þitt eigið valmyndaratriði **ERSolutionAppSpecificParametersDesigner**.

    ![Skjámynd valmyndaratriðis ERSolutionAppSpecificParametersDesigner.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. Fylgið einu af eftirfarandi skrefum:

    1. Búðu til nýjan hnapp fyrir valmyndaratriðið og tengdu hann við samsvarandi skrá úr töflunni **ERSolutionTable** með því að stilla eiginleikann **Gagnagjafi** á **ERSolutionTable**.

        ![Skjámynd af stillingum nýs valmyndaratriðis.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. Búðu til einfaldan hnapp og hnekktu eiginleikanum **Smellt** eins og sýnt er í eftirfarandi dæmi.

        Með því að nota þessa aðferð geturðu tilgreint sérstakt auðkenni lausnar (skilgreint með gildinu **GUID**) til að leyfa aðgang að forritasértækum færibreytum á aðeins tilteknu ER sniði og afrit sem eru afleidd af þeim.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Frekari upplýsingar

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
