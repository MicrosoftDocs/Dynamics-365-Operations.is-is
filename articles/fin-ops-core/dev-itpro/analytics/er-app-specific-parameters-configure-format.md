---
title: Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila
description: Þetta efni útskýrir hvernig þú getur stillt ER-snið fyrir rafræna skýrslugerð til að nota færibreytur sem eru tilgreindar á lögaðila.
author: NickSelin
ms.date: 04/02/2021
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
ms.openlocfilehash: 2bf4d1ecad3e25299df7c87ffa2236736ddcac300a5ded779616b25920745d7e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765833"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Stilla ER snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Yfirlit

Í mörgum af sniðmátum rafrænnar skýrslugerðar (ER) sem þú verður að hanna verður þú að sía gögn með því að nota mengi gilda sem eru sértæk fyrir hverja lögaðila í þínu tilviki (til dæmis, sett af skattakóða til að sía skattaviðskipti). Eins og er, þegar síun af þessu tagi er stillt á ER sniði, eru gildi sem eru háð lögaðilanum (til dæmis skattakóða) notuð í tjáningu á ER sniði til að tilgreina reglur um síun gagna. Þess vegna er ER sniðið gert sértækt fyrir lögaðila og til að mynda nauðsynlegar skýrslur verður þú að stofna afleidd afrit af upprunalegu ER sniði fyrir hvern lögaðila þar sem þú þarft að keyra ER snið. Breyta þarf hverju afleiddu sniði rafrænnar skýrslugerðar til fá gildi ákveðins lögaðila inn í það, endurreiknað í hvert sinn sem upprunaleg (grunn)útgáfan hefur verið uppfærð, flutt úr prófunarumhverfi og flutt inn í vinnsluumhverfi þegar nota þarf það í framleiðsluskyni og svo framvegis. Því er vinna við þessa gerð af skilgreindri lausn rafrænnar skýrslugerðar flókin og tímafrek af ýmsum ástæðum:

-   Því fleiri sem lögaðilar eru, því meira verður að viðhalda skilgreiningum á ER sniði.
-   Viðhald ER stillinga krefst þess að notendur fyrirtækja hafi ER þekkingu.

Sértækar færibreytur fyrir ER-aðgerðir láta rafmagnsnotendur stilla gagnasíun á ER sniði þannig að hún byggist á mengi óhlutbundinna reglna. Hægt er að stilla þetta reglumengi til að nota gagnagjafana sem eru til á ER sniði. Notendur fyrirtækja geta síðan tilgreint raunverulegar reglur umfram ER ramma með því að nota notendaviðmótið (UI) sem er sjálfkrafa myndað út frá stillingum á samsvarandi ER sniði og núverandi lögaðilagögnum sem gagnagjafar ER sniðsins munu hafa aðgang að. Hægt er að flytja reglurnar sem eru tilgreindar fyrir ER snið úr núverandi lögaðila tilviksins Dynamics 365 Finance (Finance). Það er síðan hægt að flytja það inn í annan lögaðila annaðhvort sama tilviks Finance eða annars tilviks sem reglumengi fyrir sama ER snið.

## <a name="prerequisites"></a>Forkröfur

Til að ljúka dæmum í þessu efni verður þú að hafa aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Við mælum með að þú klárir skrefin í efninu [Stuðningur við færibreytur kalla á ER-gagnaveitur af gerðinni REIKNAÐUR REITUR](er-calculated-field-type.md). Ef þú hefur þegar lokið þessum skrefum geturðu sleppt skrefunum í hlutanum **Flytja ER stillingar inn í RCS** sem hér segir.

## <a name="import-er-configurations-into-rcs"></a>Flytja inn skilgreiningar inn í RCS

Einnig verður að sækja og geyma staðbundið eftirfarandi skilgreiningar fyrir rafræna skýrslugerð.

| **Lýsing á efni**                        | **Skrárnafn**                                        |
|------------------------------------------------|------------------------------------------------------|
| Sýnishorn af skilgreiningarskránni **ER-gagnalíkan**    | [Líkan til að læra breytur á calls.version.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| Sýnishorn af skilgreiningarskrá **ER-lýsigagna**      | [Lýsigögn til að læra breytur á calls.version.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| Sýnishorn af skilgreiningu **ER-líkanavörpunar** | [Vörpun til að læra breytur á calls.version.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| Sýnishorn af skilgreiningu **ER-sniðmáts**             | [Snimát til að læra breytur á calls.version.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Næst skráðirðu þig inn á RCS tilvikið.

Í þessu dæmi mun stofna skilgreiningu fyrir dæmi um sýnifyrirtæki, Litware, Inc. Áður en hægt er að ljúka þessu ferli verður að ljúka skrefunum í efninu [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md) í RCS.

1.  Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.
2.  Veldu **Skilgreiningar skýrslugerðar**.
3.  Flytja inn ER-skilgreiningar sem voru sóttar áður inn í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans og snið. Fyrir hverja ER-skilgreiningu skal fylgja þessum skrefum:

    1.  Veldu **Gengi**.
    2.  Veldu **Hlaða úr XML-skrá**.
    3.  Veljið **Vafra** til að velja skrá fyrir nauðsynlega skilgreiningu rafrænnar skýrslugerðar á XML-sniði.
    4.  Veljið **Í lagi**.

## <a name="review-the-er-solution-that-is-provided"></a>Farðu yfir þá ER-lausn sem er veitt

1.  Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.
2.  Veldu liðinn **Snið til að læra færibreytur á köll**.
3.  Veljið **Hönnuður**.
4.  Veldu **Stækka/Minnka**.

    ER-sniðmátið **Snið til að læra færibreytur á köll** er hannað til að búa til skattayfirlit á XML sniði sem sýnir nokkur stig skattheimtu (venjuleg, lækkuð og engin). Hvert stig hefur mismunandi fjölda smáatriða.

    ![Mörg stig af sniði rafrænnar skýrslugerðar, snið til að læra færibreytusímtöl.](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Á flipanum **Vörpun** stækkarðu liðina **Líkan**, **Gögn** og **Yfirlit**.

    Gagnagjafinn **Model.Data.Summary** skilar lista yfir skattfærslur. Þessar færslur eru teknar saman eftir skattkóðum. Fyrir þessa gagnaheimild hefur reiknaði reiturinn **Model.Data.Summary.Level** verið stilltur til að skila kóðanum fyrir skattlagningarstig hverrar samandreginnar skráar. Fyrir alla skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma skilar reiknaði reiturinn skattlagningarstigskóðanum (**Regluleg**, **Lækkuð**, **Engin** eða **Annað**) sem textagildi. Reiknaði reiturinn **Model.Data.Summary.Level** er notaður til að sía skrár úr gagnagjafanum **Model.Data.Summary** og slá inn síuð gögn í hvern XML-þátt sem táknar skattlagningarstig með því að nota reitina **Model.Data2.Level1**, **Model.Data2.Level2** og **Model.Data2.Level3**.

    ![Model.Data.Summary listi gagnaveitu skattfærsla.](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Reiknaði reiturinn **Model.Data.Summary.Level** hefur verið stilltur þannig að hann inniheldur ER-segð. Skattkóðar (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** og **InVAT0**) eru harðkóðaðir í þessari stillingu. Þess vegna er þetta ER snið háð lögaðilanum þar sem þessir skattakóðar voru stilltir.

    ![Model.Data.Summary.Level útreiknaður reitur með harðkóðuðum skattkóðum.](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Til að styðja við annað sett af skatt kóða fyrir hvern lögaðila verður þú að fylgja þessum skrefum:

    - Búðu til afleidda útgáfu af ER sniði fyrir hvern lögaðila.
    - Uppfæra skattakóða í reiknaða reitinn **Model.Data.Summary.Level**, byggt á stillingu lögaðila.

6.  Lokaðu síðunni **Sniðshönnuður**.

## <a name="create-a-derived-format"></a>Stofna afleitt sniðmát

Næst munt þú nota eiginleikann ER-forritasértækar færibreytur til að styðja við ólík sett af skattakóða fyrir hvern lögaðila á einu ER sniði.

1.  Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.
2.  Veldu liðinn **Snið til að læra færibreytur á köll**.
3.  Veljið **Stofna skilgreiningu**.
4.  Veldu valkostinn **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.
5.  Í reitnum **Heiti** slærðu inn **Sniðmát til að læra hvernig eigi að fletta upp LE-gögnum**.
6.  Veljið **Stofna skilgreiningu**.

## <a name="configure-a-derived-format"></a>Stilla afleitt snið

### <a name="add-a-format-enumeration"></a>Bæta við tölusetningu sniðs

Næst bætirðu við nýrri upptalningu á ER sniði. Gildi þessarar sniðupptalningar verða kynnt fyrir fyrirtækjanotendum sem munu tilgreina mengi lögaðilaháðra skattkóða fyrir hin ýmsu skattheimtustig sem notuð eru á ER sniði.

1.  Veljið **Hönnuður**.
2.  Veldu **Tölusetningar sniða**.
3.  Veljið **Bæta við**.
4.  Í reitinn **Heiti** slærðu inn **Listi yfir skattlagningarstig**.
5.  Veljið **Vista**.
6.  Á flipaum **Gildi tölusetningar sniðs** velurðu **Bæta við**.
7.  Í reitinn **Heiti** slærðu inn **Regluleg skattlagning**.
8.  Veldu aftur **Bæta við**.
9.  Í reitinn **Heiti** slærðu inn **Lækkuð skattlagning**.
10. Veldu aftur **Bæta við**.
11. Í reitinn **Heiti** slærðu inn **Engin skattlagning**.
12. Veldu aftur **Bæta við**.
13. Í reitinn **Heiti** skal færa inn **Annað**.

    ![Ný færsla á síðunni tölusetningar sniðs.](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Vegna þess að notendur fyrirtækja gætu notað mismunandi tungumál til að tilgreina skattalög sem eru háð lögaðilum, mælum við með að þú þýðir gildi þessarar talningar yfir á tungumálin sem eru stillt sem ákjósanleg tungumál fyrir þá notendur í Finance.

14. Veldu skrána **Engin skattlagning**.
15. Smelltu í reitinn **Merki**.
16. Veldu **Þýða**.
17. Á **Textaþýðing** svæðinu í **Kenni merkis** reitinn skal slá inn **LBL_LEVELENUM_NO**.
18. Í reitnum **Texti á sjálfgefnu tungumáli** slærðu inn **Engin skattlagning**.
19. Í reitnum **Tungumál** velurðu **DE**.
20. Í reitinn **Þýddur texti** skal færa inn **keine Besteuerung**.
21. Veldu **Þýða**.

    ![Textaþýðingar renna út.](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Veldu **Vista**.
23. Lokaðu síðunni **Tölusetningar sniða**.

### <a name="add-a-new-lookup-data-source"></a>Bættu við nýjum gagnagjafa

Næst bætirðu við nýjum gagnagjafa til að tilgreina hvernig notendur fyrirtækja munu tilgreina reglur sem eru háðar lögaðilum til að viðurkenna rétt skattlagningarstig fyrir hvert yfirlit yfir færsluskrá.

1.  Á flipanum **Vörpun** velurðu **Bæta við**.
2.  Veldu **Format enumeration\Lookup**.

    Þú varst að auðkenna að hver regla sem notendur fyrirtækja tilgreina fyrir viðurkenningu á skattaþrepum muni skila gildi upptalningar á ER sniði. Taktu eftir að gagnagjafagerðina **Uppflettingu** er hægt að nálgast undir blokkunum **Gagnalíkan** og **Dynamics 365 for Operations** til viðbótar við blokkina **Tölusetning sniðs**. Því er hægt að nota tölusetningar fyrir gagnalíkan rafrænnar skýrslugerðar og tölusetningar forrits til að tilgreina gerð gilda sem skilað er fyrir gagnagjafa af þeirri gerð. Frekari upplýsingar um gagnagjafana **Uppfletting** er að finna í [Skilgreina gagnagjafa uppflettingar til að nota eiginleika fyrir færibreytur forrits í rafrænni skýrslugerð](er-lookup-data-sources.md).
    
3.  Í reitinn **Heiti** skal færa inn **Val**.
4.  Í reitinn **Tölusetning sniðs** velurðu **Listi yfir skattlagningarstig**.

    Þú tilgreindir að fyrir hverja reglu sem er tilgreind í þessum gagnagjafa þurfi að velja eitt af gildunum í tölusetningarsniðinu **Listi yfir skattstig** sem skiluðu gildi.
    
5.  Veldu **Breyta leit**.
6.  Velja **Dálka**.
7.  Stækkaðu liðinn **Model**.
8.  Stækkaðu liðinn **Gögn**.
9.  Stækkaðu liðinn **Skattur**.
10. Veldu liðinn **Model.Data.Tax.Code**.
11. Veldu hnappinn **Bæta við** (hægri örin).

    ![Dálkar renna út.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Þú varst að tilgreina að fyrir hverja reglu sem er tilgreind í þessum gagnagjafa fyrir viðurkenningu á skattaþrepum, verður viðskiptanotandi að velja einn af skattakóðunum sem skilyrði. Listinn yfir skattakóða sem viðskiptanotandinn getur valið verður skilað af gagnagjafanum **Model.Data.Tax**. Vegna þess að þessi gagnaheimild inniheldur reitinn **Heiti** verður heiti skattakóðans sýnt fyrir hvert skattakóðagildi í uppflettingu sem er kynnt viðskiptanotanda.
    
12. Veldu **Í lagi**.

    ![Hönnunarsíða leitar.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Notendur fyrirtækja geta bætt við mörgum reglum sem skrám yfir þessa gagnaheimild. Hver skrá verður tölusett með línukóða. Reglur verða metnar til að auka línufjölda.

    Vegna þess að þú valdir reitinn **Skattakóði** sem skilyrði fyrir reglum í þessum gagnagjafa uppflettingar og þar sem **Skattakóði** er settur upp sem reitur af gagnagerðinni **Strengur** verður hver regla metin á keyrslutíma með því að bera saman skattakóðann sem er sendur til gagnagjafans með skattakóðanum sem er skilgreindur í þessari skrá gagnagjafa.

    Þegar regla sem fullnægir skilgreindum skilyrðum finnst skilar þessi gagnagjafi uppflettisgildi reglunnar sem er skilgreind í reitnum **Niðurstaða uppflettingar**. Ef engin regla finnst er undantekningu hent inn til að tilkynna notandanum að núverandi gagnagjafi geti ekki skilað réttu gildi.

13. Veljið **Vista**.
14. Lokaðu síðunni **Uppflettihönnuður**.
15. Veljið **Í lagi**.

    Taktu eftir að þú bætir við nýjum gagnagjafa sem skilar skattstigi sem gildi sniðatölusetningarinnar **Listi yfir skattastig** fyrir alla skattakóða sem er sendur til gagnaheimildarinnar sem frumgildi fyrir færibreytuna **Kóði** af gagnagerðinni **Strengur**.
    
    ![Sniðshönnuðarsíða með nýrri gagnaveitu.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Mat á skilgreindum reglum fer eftir gagnagerð reitanna sem hafa verið valdir til að skilgreina skilyrði þessara reglna. Þegar þú velur reit sem er stilltur sem reitur af annaðhvort gagnagerðinni **Tölulegt** eða **Dagsetning** munu viðmiðin verða frábrugðin viðmiðunum sem lýst var áðan fyrir gagnagerðina **Strengur**. Fyrir reitina **Tölulegt** og **Dagsetning** verður að tilgreina regluna sem gildissvið. Skilyrði reglunnar verður síðan talið fullnægt þegar gildi sem er sent til gagnagjafans er á skilgreindu sviðinu.
    
    Eftirfarandi skýringarmynd sýnir dæmi um þessa gerð uppsetningar. Í viðbót við reitinn **Model.Data.Tax.Code** í gagnagerðinni **Strengur** er reiturinn **Model.Tax.Summary.Base** í gagnagerðinni **Rauntími** notaður til að tilgreina skilyrði fyrir uppflettingu gagnagjafa.
    
    ![Hönnunarsíða leitar með viðbótardálkum.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Þar sem reitirnir **Model.Data.Tax.Code** og **Model.Tax.Summary.Base** eru valdir fyrir þennan uppflettingargagnagjafa verður sérhver regla þessa gagnagjafa stillt á eftirfarandi hátt:
    
    -   Í listanum sem er kynntur verður að velja gildi sniðatölusetningar **Listi yfir skattastil** sem skilað gildi.
    -   Færa verður inn skattakóðann sem skilyrði þessarar reglu. Aðeins skattakóðar sem veittir eru af gagnagjafanum **Model.Data.Tax** eiga við.
    -   Færa skal lágmarks- og hámarksgildi skattstofnupphæðar sem skilyrði þessarar reglu.

    Svona verður sérhver regla þessa gagnagjafa metin á keyrslutíma:
    -   Er kóðinn í gagnagerðinni **Strengur** sem var send í þennan gagnagjafa jafnt og skattakóði reglu?
    -   Fellur gildi gagnagerðarinnar **Rauntími** sem var send í þennan gagnagjafa á milli tiltekinna lágmarks- og hámarksgilda?

    Regla verður talin eiga við þegar bæði skilyrðin eru uppfyllt.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Þýddu merkimiða uppflettigagnagjafans sem bætt var við

Þar sem að fyrirtækjanotendur gætu notað mismunandi tungumál til að tilgreina lögaðilaháð mengi skattakóða mælum við með að þú þýðir merkimiða gagnagjafa uppflettinga sem þú bætir við svo að hann sé birtur á æskilegu tungumáli hvers notanda á samsvarandi síðu.

1.  Veldu gagnagjafann **Model.Data.Selector**.
2.  Veljið **Breyta**.
3.  Smelltu í reitinn **Merki**.
4.  Veldu **Þýða**.
5.  Á **Textaþýðing** svæðinu í **Kenni merkis** reitinn skal slá inn **LBL_SELECTOR_DS**.
6.  Í reitinn **Texti á sjálfgefnu tungumáli** slærðu inn **Velja skattastig eftir skattakóða**.
7.  Í reitnum **Tungumál** velurðu **DE**.
8.  Í reitinn **Þýddur texti** slærðu inn **Steuerebene für Steuerkennzeichen auswählen**.
9.  Veldu **Þýða**.
10. Veldu **Í lagi**.

    ![Eiginleiki gagnagjafa, renna út.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Bættu við nýjum reit til að nota stillta uppflettingu

1.  Stækkaðu liðinn **Model.Data**.
2.  Veldu liðinn **Model.Data.Summary**.
3.  Veljið **Bæta við**.
4.  Veldu **Aðgerðir/Reiknaður reitur**.
5.  Í reitinn **Heiti** slærðu inn **LevelByLookup**.
6.  Veljið **Breyta formúlu**.
7.  Í reitinn **Formúla** slærðu inn **Model.Selector (Model.Data.Summary.Code)**.
8.  Veljið **Vista**.

    ![Adding Model.Selector(Model.Data.Summary.Code) á síðu Formúluhönnuðarins.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Lokið síðunni **Formúluritill**.
10. Veldu **Í lagi**.

    ![Sniðshönnuður með nýrri viðbættri formúlu.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Athugaðu að reiknaði reiturinn **LevelByLookup** sem þú bættir við mun skila skattastiginu sem gildi sniðaupptalningarinnar **Listi yfir skattastig** fyrir hverja samantekna skrá skattafærslna. Skattakóði skrárinnar verður sendur til uppflettigagnagjafans **Model.Selector** og reglurnar fyrir þennan gagnagjafa verða notaðar til að velja rétt skattlagningarstig.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Bætið við nýjum sniðatölusetningarbundnum gagnagjafa

Næst bætirðu við nýjum gagnagjafa sem vísar til sniðatölusetningarinnar þú bættir við fyrr. Gildi þessa gagnagjafa verða seinna notuð í segð á ER-sniði.

1.  Veljið **Bæta við rót**.
2.  Veldu **Format enumeration\Enumeration**.
3.  Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.
4.  Í reitinn **Tölusetning sniðs** velurðu **Listi yfir skattlagningarstig**.
5.  Veljið **Vista**.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Breyttu núverandi reit til að nota leitina

Næst verður þú að breyta fyrirliggjandi reiknuðum reit þannig að hann notar skilgreindan uppflettingargagnagjafann til að skila réttu skattlagningargildi, allt eftir skattakóðanum.

1.  Veldu liðinn **Model.Data.Summary.Level**.
2.  Veljið **Breyta**.
3.  Veljið **Breyta formúlu**.

    Taktu eftir að núverandi tjáning reitarins **Model.Data.Summary.Level** inniheldur eftirfarandi harðkóðaða skattakóða:
    
    MÁL (@. Kóðinn, "VSK19", "Venjulegur", "InVAT19", "Venjulegur", "VSK7", "Minni", "InVAT7", "Minni", "ÞRIÐJA", "Enginn", "InVAT0", „Enginn“, „Annað“)

4.  Í ritinn **Formúla** slærðu inn **CASE(@.LevelByLookup, TaxationLevel. 'Regular taxation', 'Regular', TaxationLevel.'Reduated taxation ',' Reduced ', TaxationLevel.'No taxation', 'None', 'Other')**.

    ![Síða aðgerðarhönnuðar rafrænnar skýrslugerðar.](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Takið eftir að segð reitsins **Model.Data.Summary.Level** mun nú skila skattlagningarstiginu út frá skattkóða gildandi færslu og reglusafni sem viðskiptanotandi skilgreinir í uppflettingargagnagjafa **Model.Data.Selector**.
    
5.  Veljið **Vista**.
6.  Lokaðu síðunni **Formúluhönnuður**.
7.  Veljið **Í lagi**.
8.  Veljið **Vista**.
9.  Lokaðu síðunni **Sniðshönnuður**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Ljúktu uppkastsútgáfu af afleiddu sniði

1.  Á flýtiflipanum **Útgáfur** skal velja **Breyta stöðu**.
2.  Velja **Lokið**.
3.  Veljið **Í lagi**.

## <a name="export-completed-version-of-modified-format"></a>Flyttu út fullkláraða útgáfu af breyttu sniði

1.  Í skilgreiningatrénu skal velja atriðið **Snið til að læra hvernig á að fletta upp LE-gögnum**.
2.  Í flýtiflipanum **Útgáfur** skal velja færsluna sem er með stöðuna **Lokið**.
3.  Veldu **Gengi**.
4.  Veldu **Flytja út sem XML-skrá**.
5.  Veljið **Í lagi**.
6.  Vafrinn sækir skrána **Snið til að læra hvernig á að fletta upp LE data.xml**. Geymið þessa skrá á staðnum.

Endurtakið skrefin í þessum hluta fyrir yfirvörur á sniðinu **Snið til að læra hvernig á að fletta upp LE-gögnum** og geymið eftirfarandi skrár staðbundið:

-   Sniðmát til að læra færibreytur á köll.xml
-   Veldu Vörpun til að læra færibreytur á köll.xml
-   Líkan til að læra færibreytur á köll.xml

Til að læra hvernig á að nota skilgreinda rafræna skýrslugerðarsniðið **Snið til að læra hvernig á að fletta upp LE-gögnum** til að setja upp sett af skattkóðum sem tengjast lögaðila til að sía skattfærslur eftir mismunandi skattlagningarstigum, skal ljúka skrefunum í efnisatriðinu [Setja upp færibreytur rafræns skýrslugerðarsniðs fyrir hvern lögaðila](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)

[Setja upp færibreytur á sniði rafrænnar skýrslugerðar fyrir hvern lögaðila](er-app-specific-parameters-set-up.md)

[Skilgreina gagnaveitu uppflettingar til að nota eiginleikann fyrir færibreytur sem eru sértækar fyrir rafræna skýrslugerð](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
