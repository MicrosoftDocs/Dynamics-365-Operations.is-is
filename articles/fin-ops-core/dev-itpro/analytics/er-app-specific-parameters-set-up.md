---
title: Settu upp færibreytur ER sniðs á hvern lögaðila
description: Þetta efni útskýrir hvernig þú getur sett upp færibreytur í snið fyrir rafræna skýrslugerð (ER) á lögaðila.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681473"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Settu upp færibreytur ER sniðs á hvern lögaðila

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forkröfur

Til að ljúka þessum skrefum verðurðu fyrst að klára skrefin í efninu [Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md).

Til að ljúka dæmunum í þessu efni verður þú að hafa aðgang að Microsoft Dynamics 365 Finance (Fjármál) fyrir eitt af eftirfarandi hlutverkum:

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

## <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar

1.  Skráðu þig inn í umhverfið.
2.  Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.
3.  Veldu **Skilgreiningar skýrslugerðar**.
4.  Flyttu inn í núverandi tilvik af Finance stillingarnar sem þú fluttir út úr Regulatory Configuration Services (RCS) meðan þú varst að ljúka skrefunum í efninu [Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md). Fylgdu þessum skrefum fyrir hverja stillingu fyrir rafræna skýrslugerð (ER) í eftirfarandi röð: gagnamódel, vörpun líkana og snið.

    1. Veldu **Skipta út \> Hlaða úr XML-skrá**.
    2. Veljið **Vafra** til að velja skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.
    3. Veljið **Í lagi**.
    
    Eftirfarandi mynd sýnir stillingarnar sem þú verður að hafa þegar þú ert búin/n.

    ![Skilgreiningarsíða í ER](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Setja upp færibreytur fyrir fyrirtækið DEMF

Þú getur notað ER-rammana til að setja upp sértækar breytur fyrir forrit fyrir ER snið.

1.  Velja skal lögaðilann **DEMF**.
2.  Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
3.  Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm.PNG)
    
    Á síðunni **Forritsbundnar færibreytur** er hægt að stilla reglurnar fyrir gagnagjafann **Val** í sniðinu **Snið til að læra hvernig á að fletta upp LE-gögnum**.
    
    Ef grunn ER sniðið mun innihalda nokkra gagnagjafa af gerðinni **Uppfletting**, verður þú að velja viðeigandi gagnagjafa á flýtiflipanum **Uppflettingar** áður en þú getur byrjað að stilla reglumengi fyrir gagnagjafann.
    
    Fyrir hvern gagnagjafa er hægt að stilla aðskildar reglur fyrir hverja útgáfu af völdu ER sniði.
    
    Allt reglumengið fyrir alla uppflettigagnagjafa sem eru fáanlegir í valinni útgáfu af grunn-ER sniði samanstendur af forritssértæku færibreytunum fyrir ER sniðið.

4.  Veldu útgáfu **1.1.1** á ER sniði.
5.  Á flýtiflipanum **Skilyrði** velurðu **Bæta við**.
6.  Í reitnum **Kóði** í nýju skránni velurðu fellilistaörina til að opna leitina.

    Uppflettan sýnir lista yfir skattakóða fyrir val. Þessum lista er skilað af gagnagjafanum **Model.Data.Tax** sem hefur verið stilltur á grunn ER sniði. Vegna þess að þessi gagnagjafi inniheldur reitinn **Heiti** birtist nafn sérhvers skattakóða í leitinni.

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Veldu skattakóðann **VAT19** tax code.
8.  Í reitnum **Niðurstöður uppflettinar** í nýju skránni velurðu fellilistaörina til að opna leitina. Leitin sýnir lista yfir gildi fyrir TaxationLevel snið upptalningar fyrir val.

    Athugaðu að ef þýska er valin sem æskilegt tungumál notandans sem þú ert skráður inn sem, þá verða merkimiðar gildanna í uppflettingu á þýsku, að því tilskildu að þau hafi verið þýdd á grunn ER sniði. Að auki, ef merkimiði uppflettingargagnaheimildar hefur verið þýddur mun sá merkimiði birtast á æskilegu tungumáli notandans á flipanum **Uppflettingar**.

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Veldu gildið **Regluleg skattlagning**.

    Með því að bæta við þessa skrá skilgreinirðu eftirfarandi reglu: Alltaf þegar beðið er um **Val** uppflettingu gagnagjafa og skattakóðinn **VSK19** er samþykktur sem frumbreyta verður **Regluleg skattlagning** skilað sem umbeðnu skattlagningarstigi.

10. Veldu **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **InVAT19**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Regluleg skattlagning**.
    
11. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **VAT7**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Lægri skattlagning**.
    
12. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **InVAT7**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Lægri skattlagning**.
    
13. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **THIRD**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Engin skattlagning**.
    
14. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitnum **Kóði** velurðu skattakóðann **InVAT0**.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Engin skattlagning**.
    
15. Veldu aftur **Bæta við** og fylgdu síðan þessum skrefum:

    1. Í reitinn **Kóði** velurðu valkostinn **\*Ekki autt\***.
    2. Í reitnum **Niðurstaða uppflettingar** velurðu gildið **Annað**.
    
    Með því að bæta þessari skrá við skilgreinirðu eftirfarandi reglu: Alltaf þegar skattakóði sem er samþykktur sem frumbreyta uppfyllir engar af áðurnefndum reglum mun gagnagjafi uppflettingar skila **Annað** sem umbeðnu skattlagningarstigi.

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. Í reitnum **Staða** skal velja **Lokið**.

    Þegar þú keyrir ER snið útgáfu sem hefur annaðhvort stöðuna **Lokið** eða **Deilt** verður þetta reglumengi að vera með stöðuna **Lokið**. Annars verður framkvæmd grunn ER sniðsins rofin þegar sniðið reynir að hlaða gögnum úr þessu reglumengi þegar uppflettigagnagjafinn **Val** er keyrður.
    
    Þegar þú keyrir ER snið útgáfu sem hefur stöðuna **Drög** hefur grunn ER sniðið aðgang að þessu reglumengi, óháð stöðu þess.
    
17. Veljið **Vista**.
18. Lokaðu síðunni **Forritsbundnar færibreytur**.

## <a name="run-the-er-format-in-the-demf-company"></a>Keyra ER sniðið í DEMF fyrirtækinu

1.  Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
2.  Í aðgerðarúðunni skal velja **Keyra**.
3.  Í svarglugganum sem birtist skal smella á **Í lagi**.
4.  Sæktu yfirlitið sem er búin til og geymdu hana á staðnum.

    Taktu eftir því í myndaða uppgjörinu hefur skattakóðinn **InVAT7** verið settur á stigið **Minnkað** og samantektir á skattakóðunum **VSK19** og **InVA19** hafa verið settar á stigið **Reglulegt**. Þessi hegðun ræðst af stillingum í reglum sem eru háðir lögaðilum.
    
5.  Farðu í **Skattur \> Óbeinir skattar \> Virðisaukaskattur \> VSK-kóðar**.
6.  Veldu skattakóðann **InVAT7**.
7.  Á aðgerðarrúðunni, á flipanum **VSK-kóði**, í hópnum **Fyrirspurnir**, velurðu **Bókaður virðisaukaskattur** til að skoða upplýsingar um skatthlutfall og beitt skatthlutfall á hvern skattakóða.

    ![Síðan Bókaður virðisaukaskattur](./media/GER-AppSpecParms-Statement.PNG)

8.  Lokið síðunni Bókaður virðisaukaskattur.

## <a name="set-up-parameters-for-the-usmf-company"></a>Setja upp færibreytur fyrir fyrirtækið USMF

1.  Velja skal lögaðilann **USMF**.
2.  Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
3.  Í stillingatrénu stækkarðu liðinn **Líkan til að læra færibreytur á köll**, stækkar liðinn **Snið til að læra færibreytur á köll** og velur sniðmátið **Snið til að læra hvernig á að fletta upp LE-gögnum**.
4.  Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.
5.  Veldu útgáfu **1.1.1** á völdu ER sniði.
6.  Á flýtiflipanum **Skilyrði** velurðu **Bæta við**.
7.  Í reitnum **Kóði** í nýju skránni velurðu fellilistaörina til að opna leitina.

    Núna sýnir uppflettingin lista yfir skattakóða fyrir **USMF** fyrirtækjaskatt fyrir val.

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Veldu skattakóðann **EXEMPT**.
9.  Í reitnum **Niðurstaða uppflettingar** í nýju skránni velurðu gildið **Engin skattlagning**.
10. Veldu aftur **Bæta við**.
11. Í reitnum **Kóði** í nýju skránni velurðu valkostinn **\*Ekki autt\***.
12. Í reitnum **Niðurstaða uppflettingar** í nýju skránni velurðu gildið **Regluleg skattlagning**.
13. Í reitnum **Staða** skal velja **Lokið**.
14. Veljið **Vista**.

    ![Síðan ER-forritsbundnar færibreytur](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. Lokaðu síðunni **Forritsbundnar færibreytur**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Keyra ER sniðið í USMF fyrirtækinu

1.  Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
2.  Í aðgerðarúðunni skal velja **Keyra**.
3.  Í svarglugganum sem birtist skal smella á **Í lagi**.
4.  Sæktu yfirlitið sem er búin til og geymdu hana á staðnum.

    Taktu eftir því í tilkynningunni að þú hefur nú notað sama ER snið fyrir annan lögaðila en án þess að gera neinar breytingar á ER sniði.

## <a name="reuse-legal-entitydependent-parameters"></a>Endurnýta færibreytur sem eru háðir lögaðilum

### <a name="export-parameters"></a>Útflutningsfæribreytur

1.  Fara í **Fyrirtækisstjórnun \> Vinnusvæði \> Rafræn skýrslugerð**.
2.  Veldu **Skilgreiningar skýrslugerðar**.
3.  Í stillingatrénu sniðmátið velurðu sniðmátið **Snið til að læra hvernig eigi að fletta upp LE-gögnum**.
4.  Á Aðgerðarrúðunni, á flipanum **Stillingar** í flokkinum **Umsóknarbundnar færibreytur** veljið **Uppsetning**.
5.  Veldu útgáfu **1.1.1** á ER sniði.
6.  Á Aðgerðasvæðinu skal velja **Flytja út**.
7.  Sæktu skrána sem er búin til og geymdu hana á staðnum.

    Nú er búið að flytja út stillt mengi af forritasértækum breytum sem XML skrá.

### <a name="import-parameters"></a>Innflutningsfæribreytur

1.  Veldu útgáfu **1.1.2** á ER sniði.
2.  Á Aðgerðasvæðinu skal velja **Flytja inn**.
3.  Veldu **Já** til að staðfesta að þú viljir hnekkja gildandi forritsbreytum fyrir þessa sniðútgáfu.
4.  Veldu **Fletta** til að finna skrána sem hefur að geyma útfluttar forritsbundnar færibreytur fyrir útgáfu **1.1.1**.
5.  Veljið **Í lagi**.

    Útgáfa **1.1.2** af ER sniði hefur nú sömu forritssértæku færibreytur og þú stilltir upphaflega fyrir útgáfu **1.1.1**.
    
    Athugið að forritssértækar færibreytur á ER sniði eru háðar lögaðilum. Til að endurnýta notendasértæku breyturnar sem voru stilltar fyrir einn lögaðila í öðrum lögaðilum, verður þú að flytja þær út meðan þú ert skráður inn á fyrsta lögaðilinn og flytja þær síðan inn eftir að þú hefur skráð þig inn í hinn lögaðila.

    Þú getur líka notað þessa aðferð til að flytja ER-snið sem tengjast sérstökum breytum sem upphaflega voru stilltar í einu tilviki Finance í annað tilvik Finance.

    Hafðu í huga að ef þú stillir forritasértækar breytur fyrir eina útgáfu af ER sniði og flytur inn hærri útgáfu af sama sniði í núverandi tilvik Finance, þá verður gildandi forritssértæku breytum ekki beitt fyrir innfluttu útgáfuna.
    
    Hafðu einnig í huga að þegar þú velur skrá til innflutnings er uppbygging forritasértæku færibreytanna í þeirri skrá borin saman við uppbyggingu samsvarandi gagnagjafa af gerðinni **Uppfletting** í ER sniðinu sem er valið til innflutnings. Innflutningurinn er gerður þegar uppbygging hverrar forritasértækrar færibreytu passar við uppbyggingu samsvarandi gagnagjafa á ER sniði sem er valið til innflutnings. Ef uppbyggingar passa ekki saman færðu viðvörunarskilaboð sem segja að ekki sé hægt að gera innflutninginn. Ef þú þvingar framkvæmd á innflutningnum verða núverandi forritasértækar færibreytur fyrir valið ER snið hreinsaðar og það verður að setja þær upp á nýtt.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Samband á milli forritasértækra færibreytna og ER sniðs

Sambandi á milli ER sniðs og forritasértækum færibreyta þess er komið á með tilvikaóháðu sértæku auðkennisnúmeri ER sniðsins. Þess vegna, þegar þú fjarlægir ER snið úr Finance, eru forritasértæku færibreyturnar sem eru stilltar fyrir ER sniðið geymdar í núverandi tilviki Finance. Hægt er að fá aðgang að þeim hvenær sem ER-grunnsniðið er flutt aftur inn í þetta tilvik Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Fáðu aðgang að forritasértækum færibreytum með því að nota ER ramma

Í dæminu á undan hefur þú fengið aðgang að forritasértækum færibreytum á ER sniði með því að nota ER ramma. Þessi aðferð gerir þér ekki kleift að takmarka aðgang að forritasértækum breytum á tilteknu ER sniði. Fylgdu þessum skrefum ef þú verður að beita slíkum takmörkunum. 

1.  Annaðhvort endurnýtirðu núverandi valmyndaratriðið **ERSolutionAppSpecificParametersDesigner** eða útfærir þitt eigið valmyndaratriði **ERSolutionAppSpecificParametersDesigner**.

    ![Síðan Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Fylgið einu af eftirfarandi skrefum:

    1.  Búðu til nýjan hnapp fyrir valmyndaratriðið og tengdu hann við samsvarandi skrá úr töflunni **ERSolutionTable** með því að stilla eiginleikann **Gagnagjafi** á **ERSolutionTable**.
    
        ![Síðan Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Búðu til einfaldan hnapp og hnekktu eiginleikanum **Smellt** eins og sýnt er í eftirfarandi dæmi.
    
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