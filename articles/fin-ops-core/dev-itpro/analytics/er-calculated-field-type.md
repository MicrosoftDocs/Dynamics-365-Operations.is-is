---
title: Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað
description: Þetta efni veitir upplýsingar um hvernig skal nota reitagerðina Reiknað fyrir ER-gagnagjafa.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550085"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað

[!include [banner](../includes/banner.md)]

Þetta efni útskýrir hvernig þú getur hannað gagnagjafa rafrænnar skýrslugerðar (ER) með því að nota gerðina **Reiknaður reitur**. Þessi gagnagjafi getur innihaldið ER-segð sem, þegar hún er keyrð, er hægt að stjórna með gildum færibreytufrumbreytanna sem eru skilgreind í bindingu sem kallar þennan gagnagjafa. Með því að skilgreina köll í færibreytur af slíkum gagnagjöfum er hægt að endurnýta staka gagnagjafa í mörgum bindingum, sem dregur úr heildarfjölda gagnagjafa sem verður að skilgreina í ER-líkanavörpunum eða ER-sniðmátum. Það einfaldar einnig skilgreinda ER-íhluti, sem dregur úr viðhaldskostnaði og notkunarkostnaði annarra neytenda.

## <a name="prerequisites"></a>Forkröfur
Til að ljúka dæmunum í þessu efnisatriði þarftu að hafa eftirfarandi aðgang:

- Aðgangur að einu af þessum hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

- Aðgang að tilviki Regulatory Configuration Service (RCS) sem hefur verið úthlutað fyrir sama leigjandann og fyrir Finance and Operations, fyrir eitt af eftirfarandi hlutverkum:

    - Þróunaraðili rafrænnar skýrslulausnar
    - Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
    - Kerfisstjóri

Úr [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) sækirðu þjappaða skrána **Stuðningur við færibreytur kallar á ER gagnagjafa af reitagerðinni Reiknað**. Hún inniheldur eftirfarandi ER-skilgreiningar sem verður að draga út og geyma á staðnum.

| **Efni**                           | **Skrárnafn**                                        |
|---------------------------------------|------------------------------------------------------|
| Sýnishorn af skilgreiningu gagnalíkans rafrænnar skýrslugerðar    | Líkan til að læra breytur á calls.version.1.xml     |
| Sýnishorn af skilgreiningu lýsigagna rafrænnar skýrslugerðar      | Lýsigögn til að læra breytur á calls.version.1.xml  |
| Sýnishorn af skilgreiningu líkanavörpunar rafrænnar skýrslugerðar | Vörpun til að læra breytur á calls.version.1.1.xml |
| Sýnishorn af skilgreiningu á sniði rafrænnar skýrslugerðar        | Snimát til að læra breytur á calls.version.1.1.xml  |

## <a name="sign-in-to-your-rcs-instance"></a>Skráðu þig inn á RCS tilvikið
Í þessu dæmi mun notandi stofna skilgreiningu fyrir sýnifyrirtækið Litware, Inc. Í RCS verður fyrst að ljúka skrefum ferlisins [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. Veldu á sjálfgefna mælaborðinu **Rafræn skýrslugerð**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Flytja inn sóttar skilgreiningar í RCS í eftirfarandi röð: gagnalíkan, lýsigögn, vörpun líkans, snið. Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:

    1. Veldu **Gengi.**
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Vafra** og veldu síðan nauðsynlega ER-skilgreiningu á XML-sniði.
    4. Veljið **Í lagi.**

## <a name="review-the-provided-er-solution"></a>Farðu yfir fyrirliggjandi ER-lausn

### <a name="review-model-mapping"></a>Farðu yfir vörpun líkans

1. Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.
2. Veldu **Vörpun til að læra færibreytur á köll**.
3. Veljið **Hönnuður**.
4. Veljið **Hönnuður**.  
   
Þessi ER-líkanavörpun er hönnuð til að gera eftirfarandi:

- Sæktu lista yfir skattakóða (gagnagjafinn **Skattur**) sem er að finna í töflunni   **TaxTable**.
- Sæktu lista yfir skattafærslur (gagnagjafinn **Trans**) sem er að finna í töflunni   **TaxTable**:
    
    - Flokka lista yfir sóttar færslur (gagnagjafinn **Gr**) eftir skattakóða.
    - Reiknaðu fyrir flokkaðar færslur eftirfarandi uppsöfnuð gildi á hvern   skattakóða:

        - Summa skattstofnsgilda.
        - Summa skattgilda.
        - Lágmarksgildi beitts skatthlutfalls.

Vörpun líkansins í þessari stillingu útfærir grunngagnalíkanið fyrir hvaða ER-snið sem er búið til fyrir þetta líkan og keyrt í Finance and Operations. Fyrir vikið verður innihald gagnafjafanna **Tax** og **Gr** berskjaldað fyrir ER-sniðum eins og óhlutbundnum gagnagjöfum.

  ![Hönnunarsíða fyrir líkanavörpun sem sýnir gagnagjafana Tax og Gr](media/er-calculated-field-type-01.png)

5.  Lokið síðunni **Hönnuður líkanavörpunar**.
6.  Lokið síðunni **Líkanavörpun**.

### <a name="review-format"></a>Skoðaðu sniðmátið

1. Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.
2. Veldu **Sniðmát til að læra færibreytur á köll**.
3. Veljið **Hönnuður**. Þetta ER-sniðmát er hannað til að gera eftirfarandi:

  - Myndaðu skattauppgjör á XML-sniði.
  - Settu fram eftirfarandi stig skattheimtu í skattauppgjöri: reglulega, lækkað og ekkert.
  - Settu fram margar upplýsingar á hverju skattlagningarstigi, með mismunandi fjölda smáatriða í hverju stigi.

  ![Síða sniðshönnuðar](media/er-calculated-field-type-02.png)

4. Veldu **Vörpun**.
5. Stækkaðu liðina **Líkan**, **Gögn,** og **Yfirlit**. 

   Reiknaði reiturinn **Model.Data.Summary.Level** inniheldur segðina sem skilar kóða skattlagningarstigsins (**Venjulegur**, **Dregið úr**, **Enginn,** eða **Annað**) sem textagildi fyrir hvaða skattakóða sem hægt er að sækja úr gagnagjafanum **Model.Data.Summary** á keyrslutíma.

  ![Hönnunarsíðan sniðmáta sem sýnir upplýsingar um gagnalíkanið til að læra færibreytur á köll](media/er-calculated-field-type-03.png)

6. Stækkaðu liðinn **Model**.**Data2**.
7. Stækkaðu liðinn **Model**.**Data2.Summary2**.
   
   Gagnagjafinn **Model**.**Data2.Summary2** er stillt til að flokka færsluupplýsingar gagnagjafans **Model.Data.Summary** skattlagningarstig (skilað af reiknaða reitnum **Model.Data.Summary.Level**) og reikna uppsafnanirnar.

  ![Hönunnarsíða sniðmáta sem sýnir upplýsingar um gagnagjafann Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. Farðu yfir reiknaða reiti **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, og **Model**.**Data2.Level3.** Þessir reiknaðir reitir eru notaðir til að sía **Model**.**Data2.Summary2** skráningalistann og skila aðeins skrám sem tákna tiltekið skattlagningarstig.
9. Lokaðu síðunni **Sniðshönnuður**.

## <a name="create-a-derived-format"></a>Stofna afleitt sniðmát
Þú getur bætt sniðið sem fylgir með því að bæta við einum reiknuðum reit til að sía tilskilið skattlagningarstig í stað þess að nota þrjá reiti sem fyrir eru: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** og **Model**.**Data2.Level3**. Hægt er að tilgreina tilskilt skattlagningarstig á þeim stað þar sem kallað verður á þennan nýja reiknaða reit.

1. Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.
2. Veldu **Sniðmát til að læra færibreytur á köll**.
3. Veljið **Stofna skilgreiningu**.
4. Veldu **Sæktu frá nafni: Snið til að læra breytur símtöl, Microsoft**.
5. Í reitnum **Heiti** slærðu inn **Sniðmát til að læra færibreytur á köll (sérsnið)**.
6. Veljið **Stofna skilgreiningu.**

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Stilla stika reiknaðan reit sem skilar lista yfir færslur

### <a name="start-adding-a-new-calculated-field"></a>Byrjaðu að bæta við nýjum reiknuðum reit

1. Veljið **Hönnuður**.
2. Veldu **Stækka/fella saman** til að stækka öll snið atriði.
3. Veldu **Vörpun**.
4. Stækkaðu liðinn **Model**.
5. Veldu liðinn **Model.Data2**.
6. Veljið **Bæta við**.
7. Veldu **Aðgerðir\\Reiknaður reitur**.
8. Í reitinn **Heiti** skal færa inn **Stig**.
9. Veljið **Breyta formúlu**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Skilgreindu færibreytu til að bæta við reiknuðum reit

1. Velja **færibreytur**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.
4. Í reitnum **Gerð** velurðu **Strengur**.

    Aðeins er hægt að nota frumstæðar gagnategundir til að tilgreina gerð frumbreytu færibreytunnar. Þess vegna er ekki hægt að nota gerðirnar **Skráalista**, **Skrá** og **Enum** í þessu skyni.

    Hámarksfjöldi færibreyta sem hægt er að tilgreina fyrir einn reiknaðan reit er 8.

    ![Upprunalisti færibreyta](media/er-calculated-field-type-05.png)

5. Veljið **Í lagi**.

Með því að bæta við þessa færibreytu tilgreinirðu það skilyrði sem verður að vera til staðar til að kalla þennan reiknaða reit. Þegar þú kallar þennan reiknaða reit þarftu að tilgreina rökin fyrir færibreytuna **Skattlagningarstig** sem gildi með sniðinu **Strengur**.

   Gakktu úr skugga um að þú skilgreinir eingöngu færibreytur fyrir þá reiknaðu reiti sem eru í gámi (annaðhvort **Skráalisti**, **Skrá**, eða **Gámur**).

   Stilla breytan er fáanleg á lista yfir gagnaveitur fyrir þennan reiknaða reit. Þú getur bætt við færibreytuna við stillta segð með því að velja **Bættu við gagnaveitu**.

   ![Gagnagjafareitir](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Skilgreindu segð til að bæta við reiknuðum reit

1. Í reitinn **Formúla** skal slá inn: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Veldu færibreytuna **Skattlagningarstig** á lista yfir gagnaveitur.
3. Veldu **Bæta við gagnagjafa**.
4. Í reitnum **Formúla** skal ljúka segðinni sem:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. Veljið **Vista**.

    ![Upplýsingar um reit gagnaveitu](media/er-calculated-field-type-07.png)

6. Lokaðu síðunni **Formúluhönnuður**.

### <a name="finish-adding-a-new-calculated-field"></a>Ljúktu við að bæta við nýjum reiknuðum reit

- Veljið **Í lagi**.

Á síðunni **Sniðmátshönnuður** krefst stillanlegur reiknaður reiturinn **Stig** frumbreytunnar **Strengur**.

![Stækkaður listi yfir reiknuð reitastig](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Notaðu stilla reiknaða reitinn til að binda sniðþætti

1. Veldu **Model.Data2.Levels** til að velja stilla reiknaða reitinn.
2. Veldu sniðmátsþáttinn **Statement.Taxation.Regular**.
3. Veldu **Binda**.
4. Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level1**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum valins sniðareiningar.

    Beitt bindandi hefur verið smíðað sem kall á reiknaða reitinn með breytu. Sjálfgefið er að nafnið á bundnu sniði er notað sem rök fyrir breytu útreiknaðan reit við eftirfarandi skilyrði:

      - Reiknaður reiturinn er stilltur til að nota eina breytu.
      - Gagnategund þessa færibreytu er skilgreind sem **Strengur**.

    Þegar nafn bundins sniðsþátta er tómt er heiti gagnaheimildar þessarar frumefnis notað í beinni bindingu.

5. Veldu sniðmátsþáttinn **Statement.Taxation.Reduced**.
6. Veldu **Binda**.
7. Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level2**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.
8. Veldu sniðmátsþáttinn **Statement.Taxation.None**.
9. Veldu **Binda**.
10. Veldu **Já** til að staðfesta að skipt sé um gagnagrunna sem nú er notaður, **Level3**, með nýju gagnaheimildinni, **Stig**, í öllum nestuðum sniðþáttum undir valinni sniðareiningu.

   Þegar þú tilgreinir færibreytuna á útreiknaða reitinn fyrir XML frumefnið sem táknar skattheimtu (t.d. **Model.Data2.Levels(„Reduced“)** sem textagildi), þú þarft ekki að gera það sama fyrir nestta XML eiginleika - bindingar þeirra erfa sjálfkrafa gildi frumbreytunnar sem er skilgreint á yfirstigi (**Model.Data2.Levels.aggregated.Base**, ekki **Model.Data2.Levels („Minni“).aggregated.Base**).

Endurtekin köll í reiknaða reiti með færibreytu eru ekki studd.

Þú getur valið **Breyta formúlu**, og breytt beitt-fyrir-vanræksröksemdum á breytubreytta reikna reitnum í valda bindingu. Ef þess frumbreytu vantar getur það valdið villum á keyrslutíma - notendur eru upplýstir um slíkar aðstæður þegar núverandi snið er staðfest.

![Tilkynning um villuviðvörun](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Skilgreindu reiknaðan reit með færibreytu til að skila skrá
Þegar reiknaður reitur með færibreytum skilar skrá þarftu að styðja við bindingu einstakra reita þessarar skráar til að forsníða þætti. Í slíkum tilvikum verður ekki um yfirbindingu að ræða sem inniheldur gildi frumbreytu til að kalla út reiknaðan reit fyrir breytu - þetta gildi verður að vera skilgreint í bindingu reits einnar skrár.

### <a name="start-adding-a-new-calculated-field"></a>Byrjaðu að bæta við nýjum reiknuðum reit

1. Veldu liðinn **Model.Data2**.
2. Veljið **Bæta við**.
3. Veldu **Aðgerðir\\Reiknaður reitur**.
4. Í reitinn **Heiti** skal færa inn **LevelRecord**.
5. Veljið **Breyta formúlu**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Skilgreindu færibreytu til að bæta við reiknuðum reit

1. Velja **færibreytur**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti** slærðu inn **Skattlagningarstig**.
4. Í reitnum **Gerð** velurðu **Strengur**.
5. Veljið **Í lagi**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Skilgreindu segð til að bæta við reiknuðum reit

1. Í reitnum **Formúla** skal færa inn eftirfarandi:  
    
    **FIRSTORNULL(\@.Levels(**

2. Veldu færibreytuna **Skattlagningarstig**.
3. Veldu **Bæta við gagnagjafa**.
4. Í reitnum **Formúla** skaltu bæta við **'Taxation Level'))** við það sem þú slóst inn í skref 1 til að klára segðina til:  
    
    **FIRSTORNULL(\@.Levels('Taxation Level'))**

5. Veljið **Vista**.
6. Lokaðu síðunni **Formúluhönnuður**.

### <a name="finish-adding-a-new-calculated-field"></a>Ljúktu við að bæta við nýjum reiknuðum reit

-   Veljið **Í lagi**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Notaðu stilla reiknaða reitinn til að binda sniðþætti

1. Útvíkkaðu **Model.Data2.LevelRecord** til að velja stilla reiknaða reitinn.
2. Útvíkkaðu gáminn **Model.Data2.LevelRecord.aggregated** í skilgreindum reiknaðum reit.
3. Veldu reitinn **Model.Data2.LevelRecord.aggregated.Base**.
4. Veldu sniðmátsþáttinn **Statement.Taxation.None**.
5. Veldu **Losa**.
6. Veldu sniðmátsþáttinn **Statement.Taxation.None.Base**.
7. Veldu **Binda**.
8. Veljið **Breyta formúlu**.
9. Breyta segð í **Model.Data2.LevelRecord(„None“).aggregated.Base**.

![Uppfærð segð](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Fjarlægðu reiknaða reiti sem ekki eru notaðir

1. Veldu **Model.Data2.Level1**.
2. Veljið **Eyða**.
3. Veldu **Model.Data2.Level2**.
4. Veljið **Eyða**.
5. Veldu **Model.Data2.Level3**.
6. Veljið **Eyða**.
7. Veljið **Vista**.

  > [!NOTE]
  > Þú notaðir aftur sama reiknaða reit **Model.Data2.Levels** nokkrum sinnum í sniðbindingum. Það er miklu auðveldara að nota og viðhalda einum reiknuðum reit í stað þess að gera þetta fyrir marga svipaða reiti.

8. Lokaðu síðunni **Sniðshönnuður**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Fullkláruð leiðrétt útgáfa af afleiddu sniði

1. Á flýtflipanum **Útgáfur** velurðu **Breyta stöðu**.
2. Velja **Lokið**.

## <a name="export-completed-version-of-a-derived-format"></a>Flyttu út fullkláraða útgáfu af afleiddu sniði

1. Veldu sniðmátið **Snið til að læra færibreytur í köll (sérsniðin)** í stillingartrénu.
2. Í flýtiflipanum **Útgáfur** velurðu lokna útgáfu 1.1.1.
3. Veldu **Gengi**.
4. Veldu **Flytja út sem XML-skrá**.
5. Geymdu sótta skilgreiningu á staðnum á XML-sniði.

## <a name="test-er-formats"></a>Prófa ER-snið 
Þú getur keyrt upphafsuppbót og endurbætt ER snið til að ganga úr skugga um að skilgreindir útreiknaðir reitir með færibreytur virki rétt.

### <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar
Þú getur flutt inn yfirfarnar stillingar úr RCS með því að nota ER-geymslu af gerðinni **RCS**. Ef þú hefur þegar gengið í gegnum skrefin í efninu, [Flytja inn rafrænar skýrslustillingar frá Regulatory Configuration Services](rcs-download-configurations.md), notaðu stilla ER geymslu til að flytja inn stillingar sem fjallað var um áður í þessu efni til umhverfisins. Að ð öðrum kosti skal fylgja þessum skrefum:

1. Veldu fyrirtækið **DEMF** og veldu á sjálfgefna yfirlitinu **Rafræn skýrsla**.
2. Veldu **Skilgreiningar skýrslugerðar**.
3. Flytja inn sóttar skilgreiningar úr Microsoft Download Center í eftirfarandi röð: gagnalíkan, vörpun líkans, snið. Ljúktu eftirfarandi skrefum fyrir hverja ER-skilgreiningu:

    1. Veldu **Gengi.**
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Vafra** til að velja nauðsynlega ER-skilgreiningu á XML-sniði.
    4. Veljið **Í lagi**.

4. Flytja út úr RCS lokið útgáfu 1.1.1 af sniðmátinu **Snið til að læra færibreytur í köll (sérsniðin)**:

    1. Veldu **Gengi.**
    2. Veldu **Hlaða úr XML-skrá**.
    3. Veldu **Fletta** til að velja staðbundið vistaða skrána **Snið til að læra færibreytur á köll (sérsniðin)** á XML sniði.
    4. Veljið **Í lagi**.

### <a name="run-er-formats"></a>Keyra ER-snið

1. Stækkaðu innihald liðarins **Líkan til að læra færibreytur á köll**.
2. Veldu **Sniðmát til að læra færibreytur á köll**.
3. Veldu **Keyra** á efsta borðanum.
4. Vistaðu úttakið á staðnum.
5. Veldu liðinn **Snið til að læra færibreytur á köll (sérsniðin)**.
6. Veldu **Keyra** á efsta borðanum.
7. Vistaðu úttakið á staðnum. 
8. Berðu saman innihald í mynduðu úttaki.

## <a name="additional-resources"></a>Frekari upplýsingar
[Formúluhönnuður í rafrænni skýrslugerð](general-electronic-reporting-formula-designer.md)
