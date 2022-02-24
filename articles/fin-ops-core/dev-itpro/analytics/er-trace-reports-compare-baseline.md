---
title: Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi
description: Þetta efnisatriði útskýrir hvernig hægt er að bera saman niðurstöður á mynduðum skýrslur rafrænnar skýrslugerðar (ER) við skýrslugildi grunnlínu.
author: NickSelin
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d89922bd10b6db17d3fee22409137d6ec966858b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682824"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi

[!include[banner](../includes/banner.md)]

Hægt er að rekja niðurstöður fyrir snið rafrænnar skýrslugerðar (ER) sem búa til rafræn skjöl á útleið. Þegar kveikt er á rakningu myndunar (með því að nota ER-notandafæribreytu **Keyra í kembiham**) er mynduð ný rakningarfærsla í aðgerðarskráningu rafrænnar skýrslugerðar í hvert sinn sem ER-skýrsla er keyrð. Eftirfarandi upplýsingar eru geymdar í hverri rakningu sem er mynduð:

- Allar viðvaranir sem voru myndaðar eftir villuleitarreglum
- Allar villur sem voru myndaðar eftir villuleitarreglum
- Allir myndaðar skrár sem eru geymdar sem viðhengi rakningarfærslunnar

Hægt er að geyma einstakar hugbúnaðarskrár grunnlínu fyrir hvaða snið rafrænnar skýrslugerðar sem er. Skrár eru álitnar grunnlínuskrár þegar þær lýsa væntanlegum niðurstöðum skýrslna sem eru keyrðar. Ef grunnlínuskrá er tiltæk fyrir ER-snið sem er keyrt á meðan kveikt er á rakningarmyndun geymir rakningin, til viðbótar við upplýsingarnar sem minnst var á áður, niðurstöður á samanburðinum á mynduðu rafrænu skjalsins við grunnlínuskrána. Í einum smelli er einnig hægt að fá myndaða rafræna skjalið og grunnlínuskrána í einni zip-skrá. Síðan er hægt að gera ítarlegan samanburð með því að nota ytri verkfæri eins og WinDiff.

Hægt er að meta rakninguna til að greina hvort rafrænu skjölin sem eru mynduð innihaldi væntanlegt efni. Hægt er að gera þetta mat í samþykktarprófsumhverfi notanda þegar kóðagrunninum hefur verið breytt (til dæmis þegar nýtt tilvik af hugbúnaðinu var flutt, bráðabót var sett upp eða kóðabreytingar voru virkjaðar). Þannig er hægt að tryggja að matið hafi ekki áhrif á framkvæmd á skýrslum rafrænnar skýrslugerðar sem eru notaðar. Fyrir margar skýrslur rafrænnar skýrslugerðar er hægt að gera matið í eftirlitslausum ham.

Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeiningarnar **ER Myndun skýrslna og samanburður á niðurstöðum (hluti 1)** og **ER Myndun skýrslna og samanburður á niðurstöðum (hluti 2)** sem eru hluti af viðskiptaferlinu **7.5.4.3 Prófun tækniþjónustu/lausna (10679)** og sem hægt er að hlaða niður af [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Þessar verkefnaleiðbeiningar fylgja þér í gegnum ferlið við að grunnstilla ramma rafrænnar skýrslugerðar til að nota grunnlínuskrár til að meta mynduð rafræn skjöl.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Dæmi: Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi

Þetta ferli útskýrir hvernig á að skilgreina ER-ramma til að safna upplýsingum um framkvæmd ER-sniðs og síðan meta niðurstöður þessara framkvæmda. Sem hluti af því mati eru mynduð skjöl borin saman við grunnlínuskrár þeirra. Í þessu dæmi muntu stofna nauðsynlegar ER-skilgreiningar fyrir sýnifyrirtækið, Litware, Inc. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Þessi skref er hægt að klára með því að nota hvaða gagnasafn sem er.

Til að ljúka skrefunum í þessu dæmi verður fyrst að ljúka skrefunum í [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar staðsetningar**, í kaflanum **Skilgreiningaveitur** skaltu staðfesta að skilgreiningaveitan fyrir sýnifyrirtækið Litware, Inc. sé skráð og að það sé merkt sem **Virkt**. Ef þú sérð skilgreiningarveituna ekki skaltu fylgja skrefunum í [Stofna skilgreiningaveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Skilgreina færibreytur skjalastjórnunar

1. Farðu í **Fyrirtækisstjórnun** \> **Skjalastjórnun** \> **Gerðir skjala** og búðu til nýja skjalagerð til að geyma grunnlínuskrár.
2. Í reitnum **Klasi** slærðu inn **Hengja skrá við**.
3. Í reitnum **Flokkur** slærðu inn **Skrá**.

![Síðan Gerðir skjala](media/GER-BaselineSample-SetupDocumentType.PNG "Skjámynd af skjalategundarsíðunni")

> [!NOTE]
> Skilgreina verður nýja skjalagerð með sama nafni fyrir hvert gagnasafn þar sem þú ætlar að nota ER-grunnlínuatriði.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Skilgreindu ER-breytur til að byrja að nota grunnlínueiginleikana

1. Í vinnusvæðinu **Rafræn skýrslugerð** í kaflanum **Skyldir tenglar**, velurðu **Færibreytur rafrænnar skýrslugerðar**.

    ![Vinnusvæði rafrænnar skýrslugerðar](media/GER-BaselineSample-ERWorkspace.PNG "Skjámynd af síðunni Vinnusvæði rafrænna skýrslna")

2. Á flipanum **Viðhengi**, í reitnum **Grunnlína**, slærðu inn eða velur þá skjalagerð sem þú varst að búa til.

    ![Viðhengisflipinn af síðunni Færibreytur rafrænna skýrslna](media/GER-BaselineSample-ERParameters.PNG "Skjámynd af Færibreytum rafrænna skýrslna")

3. Veldu **Vista** og lokaðu síðan síðunni **Færibreytur rafrænnar skýrslugerðar**.

### <a name="add-a-new-er-model-configuration"></a>Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð

1. Í vinnusvæðinu **Rafræn skýrslugerð**, í kaflanum **Skilgreiningar** velurðu reitinn **Skilgreiningar skýrslugerðar**.
2. Í aðgerðasvæðinu velurðu **Stofna skilgreiningu**.
3. Í fellilistanum, í reitnum **Heiti**, slærðu inn **Líkan til að læra ER-grunnlínur**.
4. Veldu **Stofna skilgreiningu** til að staðfesta stofnun nýrrar færslu ER-gagnalíkans.

![Stofna fellivalmynd stillinga](media/GER-BaselineSample-ModelAdd.PNG "Skjámynd af fellivalmyndinni Búa til stillingar")

### <a name="design-a-data-model"></a>Setja upp gagnalíkan

1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, velurðu **Hönnuður**.
2. Veljið **Nýtt**.
3. Í fellilistanum, í reitnum **Heiti** slærðu inn **Rót**.
4. Veljið **Bæta við**.
5. Veldu **Rótartilvísun**.
6. Veldu **Í lagi** og síðan **Vista**.
7. Lokaðu síðunni **Hönnuður líkana**.
8. Veljið **Breyta stöðu**.
9. Veldu **Ljúka** og síðan **Í lagi**.

![Skilgreiningasíða](media/GER-BaselineSample-ModelComplete.PNG "Skjámynd af síðunni Skilgreiningar")

### <a name="add-a-new-er-format-configuration"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð

1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, velurðu **Stofna skilgreiningu**.
2. Í fellilistanum, í reitahópnum **Nýtt**, velurðu **Sniðmát byggt á gagnalíkaninu Líkan til að læra ER-grunnlínur**.
3. Í reitnum **Heiti** slærðu inn **Sniðmát til að læra ER-grunnlínur**.
4. Veldu **Stofna skilgreiningu** til að staðfesta stofnun nýrrar færslu ER-sniðmáts.

![Stofna fellivalmynd stillinga](media/GER-BaselineSample-FormatAdd.PNG "Skjámynd af fellivalmyndinni Búa til stillingar")

### <a name="design-a-format"></a>Setja upp snið

Í þessu dæmi muntu stofna einfalt ER-sniði til að mynda XML-skjöl.

1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, velurðu **Hönnuður**.
2. Veljið **Bæta við rót**.
2. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í trénu velurðu **Almennt\\Skrá**.
    2. Í reitinn **Heiti** skal færa inn **Frálag**.
    3. Veljið **Í lagi**.

3. Veljið **Bæta við**.
4. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í trénu velurðu **XML\\Eining**.
    2. Í reitinn **Heiti** skal færa inn **Fylgiskjal**.
    3. Veljið **Í lagi**.

5. Í trénu velurðu **Úttak\\Skrá**.
6. Veljið **Bæta við**.
7. Í fellilistanum skaltu fylgja þessum skrefum:

    1. Í trénu skal velja **XML\\Eigind**.
    2. Í reitnum **Heiti** færirðu inn **Kenni**.
    3. Veljið **Í lagi**.

    ![Síða sniðshönnuðar](media/GER-BaselineSample-FormatLayoutDesign.PNG "Skjámynd af síðunni Sniðmátahönnuður")

8. Á flipanum **Vörpun** velurðu **Eyða**.
9. Veljið **Bæta við rót**.
10. Í fellilistanum, í trénu, velurðu **Almennt\\Innsláttarfæribreytur notanda** og fylgja síðan þessum skrefum:

    1. Í reitnum **Heiti** færirðu inn **Kenni**.
    2. Í reitnum **Merki** slærðu inn **Færa inn kenni**.
    3. Veljið **Í lagi**.

11. Í trénu velurðu **Úttak\\Fylgiskjal\\Kenni**.
12. Veldu **Binda** og síðan **Vista**.

![Síða sniðshönnuðar](media/GER-BaselineSample-FormatMappingDesign.PNG "Skjámynd af síðunni Sniðmátahönnuður")

Skilgreint snið mun mynda XML-skrá sem byggir á uppsettri uppbyggingu. Þetta XML inniheldur þáttinn **Rót** sem hefur eiginleikann **Kenni** sem er stillt á það gildi sem notandinn slær inn í svargluggann ER-svargluggi.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Mynda nýja grunnlínuskrá fyrir uppsett ER-snið

1. Á síðunni **Skilgreiningar**, á flýtiflipanum **Útgáfur**, velurðu **Keyra**.
2. Í reitnum **Skráðu kenni** slærðu inn **1**.
3. Veljið **Í lagi**.

    ![Svargluggi rafrænna skýrslufæribreyta](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Skjámynd af svarglugganum Færibreytur rafrænna skýrslna")

4. Vistaðu staðbundið afrit af skránni **out.Admin.xml** sem var mynduð, svo að þú getir notað hana seinna sem grunnlínu fyrir þetta ER-snið.

    ![Tilkynning um myndaða skrá á stillingasíðunni](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Skjámynd af tilkynningu um myndaða skrá á stillingasíðunni")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Skilgreindu ER-breytur sem nota grunnlínueiginleikana

1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, á flipanum **Skilgreiningar**, velurðu **Færibreytur notanda**.
2. Stilltu valkostinn **Keyra í kembistillingum** á **Já**.
3. Veljið **Í lagi**.

![Svarglugginn Notandafæribreytur](media/GER-BaselineSample-ERUserParameters.PNG "Skjámynd af svarglugganum Notandafæribreytur")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Bæta nýrri grunnlínuskrá við fyrir uppsett ER-snið

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Í aðgerðarúðunni velurðu **Grunnlínur**.

    ![Grunnlínuhnappur á stillingasíðunni](media/GER-BaselineSample-OpenBaselinePage.PNG "Skjámynd af hnappnum Grunnlínum á stillingasíðunni")

3. Í aðgerðarúðunni velurðu **Nýtt**.
4. Veldu ER-sniðið **Snið til að læra ER-grunnlínur** sem þú settir áður upp.
5. Veljið **Vista**.

![Síðan Grunnlínusnið rafrænnar skýrslugerðar](media/GER-BaselineSample-AddBaseline.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")

Grunnlínu er bætt við fyrir sniðið **Snið til að læra ER-grunnlínur**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Skilgreina reglu grunnlínu fyrir viðbætta grunnlínu

1. Á síðunni **Grunnlínur rafræns skýrslugerðarsniðs**, á aðgerðarsíðunni, velurðu hnappinn **Viðhengi** (klemmuspjaldstáknið).
2. Í aðgerðarúðunni velurðu **Nýtt** \> **Skrá**. Í ER-breytum ætti skjalategundin **Skrá** að hafa verið valin áður sem sú skjalategund sem er notuð til að geyma grunnlínuskrár.
3. Veldu **Fletta** og veldu skrána **out.Admin.xml** sem var búin til þegar þú keyrðir skilgreint ER-snið áður.

    ![Síðan Fylgiskjöl](media/GER-BaselineSample-UploadBaselineFile.PNG "Skjámynd af síðunni Viðhengi")

4. Lokaðu síðunni **Viðhengi**.
5. Á flipanum **Grunnlínur** velurðu **Nýtt**.
6. Í reitinn **Heiti** skal færa inn **Grunnlína 1**.
7. Í reitnum **Heiti skráaríhlutar** slærðu inn eða velur **Úttak**. Þetta gildi gefur til kynna að skilgreind grunnlína verði borin saman við skrá sem er mynduð með því að nota sniðþáttinn **Úttak**.
8. Í reitinn **Sía skráarheita** færirðu inn **\*.xml**.

    > [!NOTE]
    > Hægt er að skilgreina síu skráarheita. Þegar sía skráarheitis er skilgreind verður grunnlínuskráin aðeins notuð til að meta myndað úttak þegar heiti á framleiðslulistanum sem myndast uppfyllir þá síu.

9. Ef aðeins skal nota skilgreinda grunnlínu þegar ER-sniðið **Snið til að læra ER-grunnlínur** er keyrt af notendum sem eru skráðir inn í tiltekin fyrirtæki, velurðu þau fyrirtæki í reitnum **Fyrirtæki**.
10. Í reitnum **Grunngildi** slærðu inn eða velur viðhengið **out.Admin**.
11. Veljið **Vista**.

![Síðan Grunnlínusnið rafrænnar skýrslugerðar](media/GER-BaselineSample-SetupBaselineLine.PNG "Skjámynd af grunnlínusíðuni Rafrænt skýrslugerðarsnið")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Keyrðu uppsett ER-snið og endurskoðaðu skrána til að greina niðurstöðurnar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Í trénu, stækkarðu **Líkan til að læra ER-grunnlínur** og velur síðan **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.
3. Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
4. Í reitnum **Skráðu kenni** slærðu inn **1**.
5. Veljið **Í lagi**.
6. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Kembingarkladdar skilgreiningar**.

    ![Síðan Keyrsluskrár rafrænna skýrslufæribreyta](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Skjámynd af síðunni Keyrsluskrár rafrænna skýrslna")

    > [!NOTE]
    > Framkvæmdakladdinn inniheldur upplýsingar um niðurstöður samanburðar á myndaðri skrá við skilgreinda grunnlínu. Í þessu dæmi bendir kladdinn á að mynduð skrá og grunnlínan eru eins.

7. Veldu **Eyða öllu**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Keyrðu uppsett ER-snið og endurskoðaðu skrána til að greina niðurstöðurnar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Í trénu, stækkarðu **Líkan til að læra ER-grunnlínur** og velur síðan **Líkan til að læra ER-grunnlínur\\Snið til að læra ER-grunnlínur**.
3. Á flýtiflipanum **Útgáfur** velurðu **Keyra**.
4. Í reitnum **Skráðu kenni** slærðu inn **2**.
5. Veljið **Í lagi**.
6. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Kembingarkladdar skilgreiningar**.

    ![Síðan Keyrsluskrár rafrænna skýrslufæribreyta](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Skjámynd af síðunni Keyrsluskrár rafrænna skýrslna")

    > [!NOTE]
    > Framkvæmdakladdinn inniheldur upplýsingar um niðurstöður samanburðar á myndaðri skrá við skilgreinda grunnlínu. Í þessu dæmi bendir kladdinn á að mynduð skrá og grunnlínan eru ólíkar.

7. Veldu **Bera saman**.

> [!NOTE]
> Mynduð skrá og grunnlínuskráin eru í boði sem zip-skrá. Þú getur notað ytri verkfæri samanburðar eins og WinDiff til að bera saman skrárnar og skoða muninn.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina rafrænan skýrslugerðarramma (ER)](electronic-reporting-er-configure-parameters.md)
