---
title: Sjálfvirk prófun með rafrænni skýrslugerð
description: Þetta efni útskýrir hvernig hægt er að nota grunnlínueiginleika ramma rafrænnar skýrslugerðar (ER) til að gera sjálfvirka prófun á virkni.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: be641e1b2f90f4d19f7ed15e47413c0aa43d5073
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771445"
---
# <a name="automate-testing-with-electronic-reporting"></a>Sjálfvirk prófun með rafrænni skýrslugerð

[!include[banner](../includes/banner.md)]

Þetta efni útskýrir hvernig hægt er að nota ramma rafrænnar skýrslugerðar (ER) til að gera sjálfvirka prófun á sumri virkni. Dæmið í þessu efni sýnir hvernig á að gera sjálfvirka prófun á greiðsluvinnslu lánardrottins.

Forritið notar ER ramma til að búa til greiðsluskrár og samsvarandi skjöl meðan á greiðsluvinnslu lánardrottins stendur. ER-ramminn samanstendur af íhlutum gagnalíkans, líkanavörpunum og sniðs sem styðja greiðslu vinnslu fyrir mismunandi gerðir greiðslu og myndun skjala á mismunandi sniðum. Hægt er að sækja þessa þætti úr Microsoft Dynamics Lifecycle Services (LCS) og flytja þá inn í tilvikið.

Þú getur einnig sérsniðið hvern íhlut Microsoft og notað hann sem grundvöll eigin sérsniðins íhluta. Með því að búa til sérsniðna útgáfu geturðu gert breytingar sem styðja tilteknar kröfur. Til dæmis geturðu stillt ER-gagnalíkan og ER-líkanavörpun til að fá aðgang að forritsgögnum sem tengjast tilteknum viðskiptavini, eða þú getur breytt ER-sniði til að breyta útliti á myndun skjala.

Þú getur notað sérsniðin ER-snið til að vinna greiðsluskrár sem mynda lánardrottnagreiðslur og einnig til að vinna eftirlitsskýrslur. Sögugeymnin er studd í ER þáttum. Þess vegna getur Microsoft veitt uppfærðar útgáfur af ER-lausnum fyrir greiðsluvinnslu lánardrottins og þú getur sjálfkrafa sameinað uppfærða útgáfu með sérsniðnum þætti með því að endurreikna hana. Hins vegar verður þú að prófa endurreiknaða útgáfu til að tryggja að hún virki eins og þú átt von á.

ER-gagnalíkön og ER-líkanavarpanir eru algengar fyrir mörg ER-snið sem eru notuð til að vinna greiðslur af ólíkum gerðum og til að búa til lands-/svæðissértæk greiðsluskjöl. Þess vegna er afar æskilegt að gera notandasamþykki sjálfvirkt og samþættingarprófun þannig að það sé sjálfkrafa gert í mörgum fyrirtækjum en taki tillit til lands-/svæðissamhengi hvers markfyrirtækis, noti mismunandi gagnasöfn og svo framvegis.

Nánari upplýsingar um hvernig á að stofna sérsniðna útgáfu af sniði sem er byggt á sniðinu sem þú fékkst frá skilgreiningarveitunni eru að finna í [ER Uppfæra snið með því að nota nýja grunnútgáfu af viðkomandi sniði](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Lykilhugtök

Virkir kraftnotendur geta samið notandasamþykki og samþættingarprófun án þess að þurfa að skrifa frumkóða.

- Notaðu ER-grunnlínueiginleikann til að bera mynduð skjöl saman við aðaleintök. Nánari upplýsingar er að sjá í [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md).
- Notaðu verkskráningu til að ská prófunardæmi og innifela gunnlínumat. Nánari upplýsingar er að finna [Tilföng verkskráningar](../user-interface/task-recorder.md).
- Flokkaðu prófunardæmi fyrir nauðsynlegar prófunaraðstæður. Nánari upplýsingar er að finna í [Stofna og gera sjálfvirkt staðfestingarpróf notanda](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Notaðu Viðskiptaferlavinnslu (BPM) í LCS til að búa til söfn fyrir samþykktarprófanir fyrir notendur.
    - Notaðu BPM prófunarsöfn til að búa til prófunaráætlun og prófunarpakka í Microsoft Azure DevOps-þjónusta (Azure DevOps).

Virkir kraftnotendur geta keyrt prófanir fyrir notandasamþykki og samþættingu.

- Notaðu Regression Suite Automation Tool (RSAT) til að keyra prófunardæmi í æskilegum prófunarpakka.
- Tilkynntu niðurstöður prófana til Azure DevOps og notaðu þessa þjónustu til að kanna þessar niðurstöður.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að ljúka þessum verkum í efninu verður að ljúka við eftirfarandi forsendur:

- Nota grannfræði sem styður prófunarsjálfvirkni. Þú verður að hafa aðgang að tilviki í þessari grannfræði fyrir hlutverkið **Kerfisstjóri**. Þessi grannfræði verður að innihalda kynningargögn sem verða notuð í þessu dæmi. Nánari upplýsingar er að finna [Setja upp og nota umhverfi sem styður samfellda smíði og sjálfvirkni prófunar](../perf-test/continuous-build-test-automation.md).
- Til að keyra notandasamþykki og samþættingarprófanir sjálfkrafa verður þú að setja upp RSAT í grannfræðinni sem þú notar og skilgreina það á viðeigandi hátt. Nánari upplýsingar um hvernig á að setja upp og skilgreina RSAT og skilgreina það til að vinna með forritum Finance and Operations og Azure DevOps er að finna í [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Gefðu gaum að forsendum fyrir notkun tækisins. Eftirfarandi skýringarmynd sýnir dæmi um stillingar á RSAT. Blái ferhyrningurinn nær utan um breytur sem tilgreina aðgang að Azure DevOps. Græni ferhyrningurinn nær utan um breytur sem tilgreina aðgang að tilvikinu.

    ![RSAT-stillingar](media/GER-Configure.png "Skjámynd af svarglugganum RSAT-stillingar")

- Til að skipuleggja prófunardæmi í pakka til að tryggja rétta framkvæmdaröð, svo að hægt sé að safna klöddum um framkvæmd prófana til frekari skýrslugerðar og rannsókna, verðurðu að hafa aðgang að Azure DevOps úr notaðri grannfræði.
- Til að ljúka dæminu í þessu efni mælum við með því að þú sækir [ER-notkun fyrir RSAT-prófanir](https://go.microsoft.com/fwlink/?linkid=874684). Þessi zip-skrá inniheldur eftirfarandi verkleiðbeiningar:

    | Efni                                           | Skrárheiti og staðsetning |
    |---------------------------------------------------|------------------------|
    | Verkskráningardæmi til að undirbúa gögn til prófunar | Undirbúa\\Recording.xml |
    | Verkskráningardæmi til að vinna lánardrottinsgreiðslu   | Meðhöndla\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Undirbúa viðskiptaskuldaeininguna til að vinna lánardrottinsgreiðslur

1. Skráðu þig inn á tilvikið.
2. Sækja eftirfarandi ER-skilgreiningar úr LCS. Leiðbeiningar er að finna í [ER Flytja inn skilgreiningu úr Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).

    - **Greiðslulíkan** ER greiðslulíkan
    - **Vörpun greiðslulíkans 1611** ER skilgreining vörpunar greiðslulíkans
    - **BACS (UK)** ER sniðmátsskilgreining

    ![Skilgreiningar rafrænnar skýrslugerðar](media/GER-Configurations.png "Skjámynd af stillingasíðunni í rafrænum skýrslum")

3. Veldu **GBSI** sýnigagnafyrirtæki, sem er með lands-/svæðissamhengi í Bretlandi.
4. Skilgreina færibreytur viðskiptaskulda:

    1. Farðu í **Viðskiptaskuldir \> Greiðsluuppsetning \> Greiðsluhætti**.
    2. Veldu greiðsluháttinn **Rafrænt**.
    3. Skilgreindu valinn greiðsluhátt þannig að hann noti ER-sniðið **BACS (UK)** sem þú sóttir áður fyrir greiðslu lánardrottins:

        1. Á flýtiflipanum **Skráarsnið** stillirðu valkostinn **Almennt rafrænt útflutningssnið** á **Já**.
        2. Í reitnum **Skilgreining útflutningssniðs** velurðu **BACS (UK)**.

    ![Síðan Greiðsluhættir](media/GER-APParameters.png "Skjámynd af síðunni Greiðslumátar")

    > [!NOTE]
    > Ef þú ert með afleidda útgáfu af þessu ER-sniði sem var stofnuð til að styðja sérstillingar geturðu valið þessa skilgreiningu í greiðsluhættinum **Rafrænt**.

5. Búðu til dæmi um lánardrottinsgreiðslu:

    1. Farðu í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók**.
    2. Gakktu úr skugga um að þú hafir ekki bókað greiðslubókina.

        ![Síðan Heiti greiðslubókar](media/GER-APJournal.png "Skjámynd af síðunni Greiðslubók")

    3. Veldu **Línur** og sláðu inn línu sem er með eftirfarandi upplýsingar.

        | Svæði               | Dæmi um gildi   |
        |---------------------|-----------------|
        | Nafn lánardrottins         | GB\_SI\_000001  |
        | Debet               | 1,000.00        |
        | Gjaldmiðill            | GBP             |
        | Gerð mótlykils | Banki            |
        | Mótlykill      | GBSI OPER       |
        | Greiðsluháttur   | Rafrænt      |

    ![Síðan Greiðslur lánardrottna](media/GER-APJournalLines.png "Skjámynd af síðunni Greiðslur lánardrottna")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Undirbúa ER-ramma til að prófa greiðsluvinnslu lánardrottins

### <a name="configure-er-parameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Færibreytur rafrænnar skýrslugerðar**.
2. Á flipanum **Viðhengi**, í reitnum **Grunnlína** velurðu **Skrá** sem þá skjalategund sem rammi skjalastjórnunarkerfis (DM) notar til að halda skjölum sem tengjast grunnlínueiginleikanum sem DM-viðhengjum.

    ![Síða rafrænna skýrslufæribreyta](media/GER-ERParameters.png "Skjámynd af síðunni Færibreytur rafrænna skýrslna")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Myndaðu grunnlínuafrit af skjölum sem tengjast lánardrottni

1. Farðu í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók**.
2. Veldu **Línur**.
3. Veldu **Búa til greiðslur**.
4. Veldu greiðsluháttinn **Rafrænt**.
5. Veldu bankareikninginn **GBSI OPER**.
6. Stilltu valkostinn **Prenta eftirlitsskýrslu** á **Já**.
7. Sæktu myndað úttak sem zip-skrá.
8. Opnaðu skrána sem var sótt.
9. Dragðu út eftirfarandi skrár úr skránni sem var sótt:

    - **Skrá** greiðsluskrá í textaformi
    - **ERVendOutPaymControlReport** eftirlitsskýrsluskrá á XLSX-sniði

    ![Útdregnar skrár](media/GER-APJournalProcessed.png "Skjámynd af útdregnum skráarheitum í Windows Explorer")

### <a name="turn-on-the-er-baseline-feature"></a>Kveiktu á grunnlínueiginleikum ER

1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. í aðgerðarúðunni, á flipanum **Skilgreiningar** skaltu velja **Færibreytur notanda**.
3. Stilltu valkostinn **Keyra í kembistillingum** á **Já**.

Með því að kveikja á breytunni **Keyra í kembistillingum** þvingarðu ramma ER til að framkvæma eftirfarandi aðgerðir eftir framkvæmd á ER-sniði sem býr til skjöl á útleið:

1. Ákvarðaðu hvort grunnlína hafi verið skilgreind fyrir einhverja íhluti af framkvæmdu ER-sniði.
2. Ákvarðaðu hvort hver skiglreind grunnlína gildi við núverandi aðstæður (fyrirtækjakóði innskráðs fyrirtækis, skráarheiti og heiti skráarframlengingar myndaðs úttaks og svo framvegis).
3. Framkvæmdu eftirfarandi aðgerðir fyrir hverja viðeigandi grunnlínu:

    1. Berðu úttakið sem myndast við framkvæmd ER-sniðs saman við samsvarandi grunnlínu.
    2. Geymdu samanburðarniðurstöðurnar í ER kembingarkladda skilgreininga.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Skilgreina ER-grunnlínur fyrir greiðsluvinnslu lánardrottins

1. Opnið **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Skilgreiningar**.
2. Veldu **Grunnlínur**.
3. Veljið **Nýtt**.
4. Í reitnum **Tilvísun** velurðu sniðið **BACS (UK)**.
5. Veldu **Viðhengi**.
6. Bættu við nýrri gunnlínu fyrir greiðsluskrá lánardrottins:

    1. Veljið **Nýtt**.
    2. Í reitnum **Gerð** velurðu DM-skjalagerðina **Skrá** sem þú skilgreindir í ER-breytum til að geyma grunnlínugervingar.
    3. Flettu til að velja staðbundið vistuðu greiðsluskrána **Skrá** í textasniðinu.
    4. Í reitnum **Lýsing** slærðu inn **TXT-greiðsluskrá**.

7. Bættu við nýrri grunnlínu fyrir eftirlitsskýrsluna fyrir lánardrottinsgreiðsluna:

    1. Veljið **Nýtt**.
    2. Í reitnum **Gerð** velurðu DM-skjalagerðina **Skrá** sem þú skilgreindir í ER-breytum til að geyma grunnlínugervingar.
    3. Flettu til að velja staðbundið vistuðu eftirlitsskýrsluna **ERVendOutPaymControlReport** á XLSX-sniði.
    4. Í reitnum **Lýsing** slærðu inn **XLSX-eftirlitsskýrsla greiðslu**.

    ![Grunnlínur fyrir skrá lánardrottinsgreiðslu og eftirlitsskýrslu](media/GER-BaselineAttachments.png "Skjámynd af stillingasíðunni með greiðslu XLSX stjórnunarskýrslu valinn")

8. Lokið síðunni.
9. Á flýtiflipanum **Grunnlínur** velurðu **Nýtt** til að skilgreina grunnlínu fyrir greiðsluskrá:

    1. Nefndu línuna **Grunnlínustillingu fyrir greiðsluskrá**.
    2. Í reitnum **Heiti skráaríhlutar** velurðu **skrá** til að beita þessari grunnlínu við úttak ER-sniðsins sem myndar greiðsluskrána í textasniðinu BACS (UK).
    3. Í reitnum **Fyrirtæki** velurðu **GBSI** til að beita þessari grunnlínu þegar ER-sniðið **BACS (UK)** er keyrt í GBSI-fyrirtækinu.
    4. Í reitnum **Skráarheiti síu** slærðu inn **\*.TXT** til að beita þessari grunnlínu aðeins á úttök af sniðíhlutnum **skrá** sem hafa skráarendinguna **.txt**.
    5. Í reitnum **Grunngildi** velurðu **TXT-greiðsluskrá** þannig að þessi grunnlína sé notuð til samanburðar við myndað úttak.

10. Veldu **Nýtt** til að skilgreina grunnlínu fyrir eftirlitsskýrsluna:

    1. Nefndu línuna **Grunnlínustillingu fyrir eftirlitsskýrslu**.
    2. Í reitnum **Heiti skráaríhlutar** velurðu **ERVendOutPaymControlReport** til að beita þessari grunnlínu við úttak ER-sniðsins sem myndar eftirlitsskýrsluna.
    3. Í reitnum **Fyrirtæki** velurðu **GBSI** til að beita þessari grunnlínu þegar ER-sniðið **BACS (UK)** er keyrt í GBSI-fyrirtækinu.
    4. Í reitnum **Skráarheiti síu** slærðu inn **\*.XLSX** til að beita þessari grunnlínu aðeins á úttök af sniðíhlutnum **ERVendOutPaymControlReport** sem hafa skráarendinguna **.xlsx**.
    5. Í reitnum **Grunngildi** velurðu **Efitrlitsskýrsla XLSX-greiðslu** þannig að þessi grunnlína sé notuð til samanburðar við myndað úttak.

    ![Grunnlínur flýtiflipa á stillingasíðunni](media/GER-BaselineRules.png "Skjámynd af flýtiflipanum Grunnlínum á stillingasíðunni")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Skráðu prófanir til að sannreyna greiðsluvinnslu lánardrottins

Sem virkur kraftnotandi geturðu skráð eigin skref til að prófa greiðsluvinnslu lánardrottins. Við mælum með að þú spilir (og breytir, eftir því sem við á) verkskráninguna **Undirbúa\\Recording.xml** sem þú sóttir áður. Þessi skráning er notuð til að stilla öll prófunargögn í rétta stöðu. Þetta skref er nauðsynlegt vegna þess að hægt er að gera prófunina mörgum sinnum og hver prófun verður að nota gögn sem eru í sömu stöðu.

### <a name="reset-user-settings"></a>Endurstilla notandastillingar

1. Opnaðu sjálfgefið yfirlit.
2. Veldu hnappinn **Stillingar** (gírtáknið).
3. Veldu **Notendastillingar**.
4. Veldu **Notkunargögn**.
5. Veldu **Endurstilla**.
6. Veldu **Já** til að staðfesta að þú viljir endurstilla notkunargögn.
7. Lokið síðunni.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Skráðu skrefin til að undirbúa gögn til prófunar

1. Veldu hnappinn **Stillingar** (gírtáknið).
2. Veldu **Verkskráningu**.
3. Veldu **Spila skráningu**.
4. Veldu **Opna í þessari tölvu**.
5. Veldu **Skoða** og veldu staðbundið vistuðu skrána **Undirbúa\\Recording.xml**.
6. Velja **Ræsa**.
7. Haltu áfram að velja **Spila næsta skref í bið** þar til að öll skrefin í upptökunni hafa verið spiluð.

Þessi verkskráning framkvæmir eftirfarandi aðgerðir:

1. Stilltu stöðu unninnar greiðslulínu á **Ekkert**.

    ![Verkskráningarskref 3 til 4](media/GER-Recording1Review1.png "Skjámynd af verkskráningarskrefum 3 til 4")

2. Kveiktu á ER-notandabreytunni **Keyra í kembistillingum**.

    ![Verkskráningarskref 9 til 10](media/GER-Recording1Review2.png "Skjámynd af verkskráningarskrefum 9 til 10")

3. Hreinsaðu ER-kembikladdann sem inniheldur niðurstöður samanburðar á mynduðum skrám í grunnlínur.

    ![Verkskráningarskref 13 til 15](media/GER-Recording1Review3.png "Skjámynd af verkskráningarskrefum 13 til 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Skráðu skrefin til að prófa greiðsluvinnslu lánardrottins

Við mælum með að þú spilir (og breytir, eftir því sem við á) verkskráninguna **Vinna\\Recording.xml** sem þú sóttir áður. Þessi upptaka er notuð til að vinna lánardrottnagreiðslur og staðfesta samanburðarniðurstöður af mynduðum skjölum við samsvarandi grunnlínur.

1. Veldu hnappinn **Stillingar** (gírtáknið).
2. Veldu **Verkskráningu**.
3. Veldu **Spila skráningu**.
4. Veldu **Opna í þessari tölvu**.
5. Veldu **Skoða** og veldu staðbundið vistuðu skrána **Vinna\\Recording.xml**.
6. Velja **Ræsa**.
7. Haltu áfram að velja **Spila næsta skref í bið** þar til að öll skrefin í upptökunni hafa verið spiluð.

Þessi verkskráning framkvæmir eftirfarandi aðgerðir:

1. Ræstu vinnslu lánardrottnagreiðslna.
2. Veldu réttar keyrslutímabreytur og kveiktu á myndun eftirlitsskýrslu.

    ![Verkskráningarskref 3 til 8](media/GER-Recording2Review1.png "Skjámynd af verkskráningarskrefum 3 til 8")

3. Farðu í ER-kembikladdann til að skrá samanburðarniðurstöður á mynduðu úttaki við samsvarandi grunnlínur.

    Í ER-kembikladdanum birtast niðurstöður samanburðarins í reitnum **Myndaður texti**. Reitirnir **Sniðsþáttur** og **Sniðsslóð sem olli kladdafærslu** vísa til skráarþáttarins sem myndað úttak hefur verið borið saman við grunnlínuna fyrir.

    ![Færslur í keyrslukladdasíðu rafrænnar skýrslugerðar](media/GER-ERDebugLog.png "Skjáskot af færslum í keyrslukladdasíðu rafrænnar skýrslugerðar")

4. Samanburður á núverandi úttaki við grunnlínu er skráður með því að nota verskráningarkostinn **Staðfesta** og velja  **Núverandi gildi**.

    ![Notaðu villuleikarkostinn til samanburðar við núverandi gildi](media/GER-TRRecordValidation.png "Skjáskot af notkun villuleikarkosts til samanburðar við núverandi gildi")

    Eftirfarandi skýringarmynd sýnir hvernig skráð staðfestingarskref líta út í verkskráningunni.

    ![Verkskráningarskref 13 og 15](media/GER-Recording2Review2.png "Skjámynd af verkskráningarskrefum 13 og 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Bættu skráðum prófunum við Azure DevOps

1. Opnaðu Azure DevOps umhverfið.
2. Veldu verkið sem þú skilgreindir í RSAT-breytunum þegar þú [skilgreindir tólið](#prerequisites).
3. Veldu prófunaráætlunina sem þú skilgreindir í RSAT-breytunum þegar þú [skilgreindir tólið](#prerequisites).
4. Stofnaðu nýtt prófunarmál fyrir valda prófunaráætlun:

    1. Nefndu prófdæmið **Undirbúa gögn til að prófa vinnslu á rafrænum greiðslum lánardrottins**.
    2. Hengdu við skrána **Recording.xml** úr möppunni **Undirbúa** sem þú sóttir áður.

5. Stofnaðu nýtt prófunarmál fyrir valda prófunaráætlun:

    1. Nefndu prófunardæmið **Prófvinnsla á lánardrottnagreiðslum með því að nota ER-sniðið BACS (UK)**.
    2. Hengdu við skrána **Recording.xml** úr möppunni **Vinna** sem þú sóttir áður.

    ![Ný prófunarmál fyrir valda prófunaráætlun:](media/GER-RSAT-DevOps-Tests-Passed.png "Skjáskot af nýjum prófunarmálum fyrir valda prófunaráætlun:")

> [!NOTE]
> Gættu þess að framkvæmdaröðin sé rétt á þeim prófunum sem var bætt við.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Undirbúa RSAT til að keyra skráðar prófanir

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Hladdu prófunum úr Azure DevOps í RSAT

1. Opnaðu staðbundna RSAT-forritið í núverandi grannfræði.
2. Veldu **Hlaða** til að hlaða prófunum sem eru eins og stendur í Azure DevOps inn í RSAT.

    ![Próf hlaðin í RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Skjámynd af prófunum hlaðin í RSAT")

### <a name="create-automation-and-parameters-files"></a>Stofna sjálfvirkni- og færibreytuskrár

1. Í RSAT skaltu velja þær prófanir sem þú hlóðst úr Azure DevOps.
2. Veldu **Nýtt** til að stofna RSAT sjálfvirkni- og færibreytuskrár.

    ![RSAT-sjálfvirkni- og færibreytuskrár stofnaðar í RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Skjáskot af RSAT-sjálfvirkni- og færibreytuskrár stofnaðar í RSAT")

### <a name="modify-the-parameters-files"></a>Breyta færibreytuskrám

1. Í RSAT velurðu prófdæmið **Undirbúa gögn til að prófa vinnslu á rafrænum greiðslum lánardrottins**.
2. Veljið **Breyta**.
3. Í vinnubók sem er opnuð í Microsoft Excel, á vinnublaðinu **Almennt**, skaltu breyta fyrirtækjakóðanum í **GBSI**, vegna þess að þetta fyrirtæki verður notað fyrir prófunarframkvæmd.
4. Í RSAT velurðu prófunardæmið **Prófvinnsla á lánardrottnagreiðslum með því að nota ER-sniðið BACS (UK)**.
5. Veljið **Breyta**.
6. Í Excel-vinnubókinni sem er opnuð, í vinnublaðinu **Almennt**, skaltu breyta fyrirtækjakóðanum í **GBSI**.
7. Á vinnublaðinu **ERFormatMappingRunLogTable** skaltu athuga að reitirnir A:3 og C:3 innihalda textann í reitunum í ER-kembikladdatöflunni sem er notuð til að staðfesta niðurstöður samanburðar við úttak grunnlínunnar. Þessir textar verða notaðir til að meta ER-kembikladdaskrár sem eru búnar til við framkvæmd prófunar.

    ![ERFormatMappingRunLogTable vinnublað](media/GER-RSAT-RSAT-ExcelParameters.png "Skjámynd af ERFormatMappingRunLogTable vinnublaðinu")

## <a name="run-the-tests-and-analyze-the-results"></a>Keyrðu prófanirnar og greindu niðurstöðurnar

### <a name="run-the-tests-in-rsat"></a>Keyrðu prófanirnar í RSAT

1. Í RSAT veldurðu hlaðnar prófanir.
2. Veljið **Keyra**.

Athugaðu að prófunardæmin eru sjálfkrafa keyrð í forritinu með því að nota vafra.

### <a name="analyze-the-results-of-test-execution"></a>Greindu niðurstöður prófunarframkvæmdar

Niðurstöður prófunarinnar eru geymdar í RSAT. Athugaðu að báðar prófanirnar stóðust.

![Próf sem stóðust í RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Skjámynd af prófunum sem stóðust í RSAT")

Athugaðu að niðurstöður prófunar eru einnig sendar til Azure DevOps svo að þú getir gert frekari greiningu.

![Niðurstöður prófunar í Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Skjámynd af niðurstöðum prófsframkvæmda í Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Hermdu eftir aðstæðum þar sem prófanir mistakast

Þessi prófunarpakki verður að misheppnast þegar að minnsta kosti eitt af mynduðum úttökum stemmir ekki við samsvarandi grunnlínu. Til að ná þessum aðstæðum geturðu notað afleidda útgáfu þína af sniðinu **BACS (UK)** sem mun mynda greiðsluskrá sem hefur mismunandi efni en samsvarandi grunnlínu. Til að líkja eftir þessum aðstæðum geturðu notað sama sniðið af **BACS (UK)** en breytt greiðsluupphæðinni á unninni greiðslulínu.

1. Opnaðu forritið og farðu í **Viðskiptaskuldir \> Greiðslur \> Greiðslubók**.
2. Veldu **Línur**.
3. Veldu greiðslulínuna og veldu síðan **Greiðslustaða \> Enginn**.
4. Í reitnum **Debet** skaltu breyta gildinu úr **1.000,00** í **2.000,00**.
5. Veldu **Vista** til að vista breytingarnar.

### <a name="run-the-tests-in-rsat"></a>Keyrðu prófanirnar í RSAT

1. Í RSAT veldurðu hlaðnar prófanir.
2. Veljið **Keyra**.

Athugaðu að prófunardæmin eru sjálfkrafa keyrð í forritinu með því að nota vafra.

### <a name="analyze-the-results-of-test-execution"></a>Greindu niðurstöður prófunarframkvæmdar

Niðurstöður prófunarinnar eru geymdar í RSAT. Athugaðu að annað próf bilaði meðan á seinni framkvæmdinni stóð.

![Fallniðurstöður prófa í RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Skjámynd af fallniðurstöðum prófana í RSAT")

Athugaðu að niðurstöður prófunar eru einnig sendar til Azure DevOps svo að þú getir gert frekari greiningu.

![Fallniðurstöður prófa í Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Skjámynd af fallniðurstöðum prófana í Azure DevOps")

Þú getur fengið aðgang að stöðu hverrar prófunar. Þú getur einnig nálgast framkvæmdakladdann þannig að þú greinir ástæður fyrir bilun. Á eftirfarandi skýringarmynd sýnir framkvæmdakladdinn að bilun hafi átt sér stað út af muninum á innihaldi milli myndaðrar greiðsluskrár og grunnlínu hennar.

![Framkvæmdaskrá til að greina bilun í Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Skjámynd af framkvæmdaskránni til að greina bilun í Azure DevOps")

Eins og þú hefur séð, er þess vegna hægt að meta virkni ER-sniðs sjálfkrafa með því að nota RSAT sem prófunarvettvang og með því að nota prófunardæmi sem byggjast á verkskráningu og nota ER-grunnlínueiginleika.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Tilföng verkskráningar](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Stofna samþykkisprófun notanda og gera hana sjálfvirka](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Beita og nota umhverfi sem styðja samfellda smíði og sjálfvirkni prófana](../perf-test/continuous-build-test-automation.md)
- [Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi](er-trace-reports-compare-baseline.md)
- [Rafræn skýrslugerð Uppfærðu snið með því að taka upp nýja grunnútgáfu sniðs](tasks/er-upgrade-format.md)
- [Rafræn skýrslugerð Flytja inn skilgreiningu úr Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)
